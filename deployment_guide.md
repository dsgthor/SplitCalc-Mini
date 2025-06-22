# Deployment Guide 🚀

This guide covers various methods to deploy SplitCalc to different hosting platforms. Since SplitCalc is a single-file static application, deployment is straightforward and flexible.

## 📋 Prerequisites

- SplitCalc `index.html` file
- Basic understanding of your chosen hosting platform
- Optional: Custom domain name
- Optional: SSL certificate (most platforms provide this automatically)

## 🌐 Hosting Platforms

### 1. Render (Recommended)
**Current live demo**: https://splitcalc-mini.onrender.com/

#### Setup Steps
1. **Create Render Account**
   - Sign up at [render.com](https://render.com)
   - Connect your GitHub account

2. **Deploy from GitHub**
   ```bash
   # Push your code to GitHub first
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

3. **Create Static Site**
   - Click "New" → "Static Site"
   - Connect your GitHub repository
   - Configure settings:
     - **Build Command**: Leave empty
     - **Publish Directory**: `/` (root directory)
     - **Environment**: Static Site

4. **Custom Domain (Optional)**
   - Go to Settings → Custom Domains
   - Add your domain name
   - Update DNS records as instructed

#### Render Configuration
Create `render.yaml` (optional):
```yaml
services:
  - type: web
    name: splitcalc
    env: static
    buildCommand: ""
    staticPublishPath: .
    routes:
      - type: rewrite
        source: /*
        destination: /index.html
```

### 2. Netlify
Easy deployment with great features for static sites.

#### Deploy via Drag & Drop
1. Visit [netlify.com](https://netlify.com)
2. Sign up for free account
3. Go to "Sites" → "Deploy manually"
4. Drag your `index.html` file to the deployment area
5. Your site will be live instantly!

#### Deploy via GitHub
1. **Connect Repository**
   - Go to "New site from Git"
   - Connect GitHub and select your repository

2. **Build Settings**
   - **Build command**: Leave empty
   - **Publish directory**: `/` (root)
   - **Branch**: `main`

3. **Deploy**
   - Click "Deploy site"
   - Your site will be available at `https://random-name.netlify.app`

#### Netlify Configuration
Create `_redirects` file:
```
/*    /index.html   200
```

Create `netlify.toml`:
```toml
[build]
  publish = "."

[[headers]]
  for = "/*"
  [headers.values]
    X-Frame-Options = "DENY"
    X-XSS-Protection = "1; mode=block"
    X-Content-Type-Options = "nosniff"
    Referrer-Policy = "strict-origin-when-cross-origin"
```

### 3. Vercel
Perfect for modern static sites with global CDN.

#### Deploy via CLI
```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel --prod
```

#### Deploy via GitHub
1. **Import Project**
   - Go to [vercel.com](https://vercel.com)
   - Click "New Project"
   - Import from GitHub

2. **Configuration**
   - **Framework Preset**: Other
   - **Build Command**: Leave empty
   - **Output Directory**: `.`
   - **Install Command**: Leave empty

#### Vercel Configuration
Create `vercel.json`:
```json
{
  "rewrites": [
    {
      "source": "/(.*)",
      "destination": "/index.html"
    }
  ],
  "headers": [
    {
      "source": "/(.*)",
      "headers": [
        {
          "key": "X-Frame-Options",
          "value": "DENY"
        },
        {
          "key": "X-XSS-Protection",
          "value": "1; mode=block"
        }
      ]
    }
  ]
}
```

### 4. GitHub Pages
Free hosting directly from your GitHub repository.

#### Setup Steps
1. **Enable GitHub Pages**
   - Go to repository Settings
   - Scroll to "Pages" section
   - Select source: "Deploy from a branch"
   - Choose branch: `main`
   - Folder: `/root`

2. **Access Your Site**
   - Site will be available at: `https://username.github.io/repository-name`
   - May take a few minutes to deploy

#### GitHub Pages Configuration
Create `.github/workflows/deploy.yml`:
```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]

permissions:
  contents: read
  pages: write
  id-token: write

jobs:
  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v3
      
      - name: Setup Pages
        uses: actions/configure-pages@v3
      
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v2
        with:
          path: '.'
      
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v2
```

### 5. Firebase Hosting
Google's hosting platform with excellent performance.

#### Setup Steps
1. **Install Firebase CLI**
   ```bash
   npm install -g firebase-tools
   ```

2. **Initialize Project**
   ```bash
   firebase login
   firebase init hosting
   ```

3. **Configure**
   - Select or create Firebase project
   - Public directory: `.` (current directory)
   - Single-page app: `Yes`
   - Overwrite index.html: `No`

4. **Deploy**
   ```bash
   firebase deploy
   ```

#### Firebase Configuration
`firebase.json`:
```json
{
  "hosting": {
    "public": ".",
    "ignore": [
      "firebase.json",
      "**/.*",
      "**/node_modules/**"
    ],
    "rewrites": [
      {
        "source": "**",
        "destination": "/index.html"
      }
    ],
    "headers": [
      {
        "source": "**",
        "headers": [
          {
            "key": "Cache-Control",
            "value": "max-age=3600"
          }
        ]
      }
    ]
  }
}
```

### 6. Surge.sh
Simple, single-command deployment.

#### Setup Steps
```bash
# Install Surge
npm install -g surge

# Deploy (from project directory)
surge
```

#### Configuration
Create `CNAME` file for custom domain:
```
your-domain.com
```

### 7. AWS S3 + CloudFront
Enterprise-grade hosting with global CDN.

#### Setup Steps
1. **Create S3 Bucket**
   - Go to AWS S3 Console
   - Create bucket with your domain name
   - Enable static website hosting

2. **Upload Files**
   - Upload `index.html` to bucket
   - Set public read permissions

3. **Configure CloudFront**
   - Create CloudFront distribution
   - Point to S3 bucket
   - Configure custom error pages

#### S3 Bucket Policy
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::your-bucket-name/*"
    }
  ]
}
```

## 🔧 Configuration Options

### Security Headers
Add these headers for better security:

```
X-Frame-Options: DENY
X-XSS-Protection: 1; mode=block
X-Content-Type-Options: nosniff
Referrer-Policy: strict-origin-when-cross-origin
Content-Security-Policy: default-src 'self' https://cdnjs.cloudflare.com; style-src 'self' 'unsafe-inline' https://cdnjs.cloudflare.com; script-src 'self' 'unsafe-inline'
```

### Performance Optimization
- **Gzip Compression**: Enable on your hosting platform
- **Caching**: Set appropriate cache headers
- **CDN**: Use a global CDN for better performance

### Custom Domain
Most platforms support custom domains:
1. Add domain in platform settings
2. Update DNS records:
   - **A Record**: Point to platform's IP
   - **CNAME**: Point to platform's domain
3. Configure SSL (usually automatic)

## 📱 PWA Configuration (Optional)

To make SplitCalc work offline and installable:

### Create Manifest File
`manifest.json`:
```json
{
  "name": "SplitCalc - Split Expenses Easily",
  "short_name": "SplitCalc",
  "description": "Split expenses among groups easily",
  "start_url": "/",
  "display": "standalone",
  "background_color": "#ffffff",
  "theme_color": "#4F46E5",
  "icons": [
    {
      "src": "icon-192.png",
      "sizes": "192x192",
      "type": "image/png"
    },
    {
      "src": "icon-512.png",
      "sizes": "512x512",
      "type": "image/png"
    }
  ]
}
```

### Add Service Worker
Create `sw.js` for offline functionality:
```javascript
const CACHE_NAME = 'splitcalc-v1';
const urlsToCache = [
  '/',
  '/index.html',
  'https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css'
];

self.addEventListener('install', event => {
  event.waitUntil(
    caches.open(CACHE_NAME)
      .then(cache => cache.addAll(urlsToCache))
  );
});

self.addEventListener('fetch', event => {
  event.respondWith(
    caches.match(event.request)
      .then(response => response || fetch(event.request))
  );
});
```

## 🔍 Testing Deployment

### Pre-Deployment Checklist
- [ ] Test on multiple browsers
- [ ] Verify mobile responsiveness
- [ ] Check all functionality works
- [ ] Test offline capability (if PWA)
- [ ] Validate HTML and CSS
- [ ] Test with different screen sizes

### Post-Deployment Verification
- [ ] Site loads correctly
- [ ] All features work as expected
- [ ] Performance is acceptable
- [ ] Security headers are present
- [ ] Custom domain works (if configured)
- [ ] SSL certificate is valid

### Performance Testing
Use these tools to test your deployed site:
- **Google PageSpeed Insights**: https://pagespeed.web.dev/
- **GTmetrix**: https://gtmetrix.com/
- **WebPageTest**: https://www.webpagetest.org/

## 🚨 Troubleshooting

### Common Issues

#### 404 Errors
- Ensure `index.html` is in the root directory
- Check platform-specific routing configuration
- Verify build/publish directory settings

#### Styling Issues
- Confirm TailwindCSS CDN is accessible
- Check for CORS issues with external resources
- Verify CSS is loading correctly

#### Performance Issues
- Enable gzip compression
- Optimize images (if any)
- Use appropriate caching headers
- Consider using a CDN

#### Mobile Issues
- Test on actual mobile devices
- Check viewport meta tag
- Verify touch interactions work

### Getting Help
- Check hosting platform documentation
- Review error logs (if available)
- Test locally first
- Contact hosting platform support

## 📊 Monitoring

### Analytics (Optional)
If you want to track usage:
- Google Analytics
- Plausible Analytics
- Simple Analytics

### Uptime Monitoring
- UptimeRobot
- Pingdom
- StatusCake

### Performance Monitoring
- New Relic
- DataDog
- Google Search Console

---

## 🎯 Recommended Setup

For most users, we recommend:
1. **Render** or **Netlify** for ease of use
2. **GitHub Pages** for open source projects
3. **Vercel** for advanced features
4. **Firebase** for Google ecosystem integration

Choose based on your needs:
- **Simple deployment**: Netlify drag & drop
- **GitHub integration**: GitHub Pages or Render
- **Custom domain**: Any platform (all support it)
- **Enterprise**: AWS S3 + CloudFront

---

**Need help with deployment? Create an issue on GitHub or contact the maintainers!** 🚀