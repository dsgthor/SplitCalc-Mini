# Security Policy 🔒

## 🛡️ Security Overview

SplitCalc is designed with privacy and security as core principles. As a client-side only application, we've implemented several security measures to protect user data and ensure safe operation.

## 🔐 Security Features

### Data Privacy
- **No Server Communication**: All data processing happens locally in your browser
- **No Data Collection**: We don't collect, store, or transmit any personal information
- **Local Storage Only**: Data persists using browser's localStorage on your device
- **No Analytics**: No tracking, analytics, or telemetry code included
- **No Third-Party Services**: Only TailwindCSS CDN for styling (no data transmission)

### Application Security
- **Client-Side Only**: No server-side code or database vulnerabilities
- **No Authentication**: No login system means no credential vulnerabilities
- **Input Sanitization**: All user inputs are properly validated and sanitized
- **XSS Protection**: Proper escaping of user-generated content
- **No External Dependencies**: Minimal attack surface with only essential CDN usage

### Browser Security
- **Same-Origin Policy**: Adheres to browser security policies
- **Content Security**: No inline scripts or unsafe evaluations
- **Local Storage**: Uses browser's built-in storage security
- **HTTPS Ready**: Compatible with secure HTTPS deployment

## 📊 Supported Versions

We provide security updates for the following versions:

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | ✅ Yes             |
| < 1.0   | ❌ No              |

## 🚨 Reporting a Vulnerability

We take security seriously. If you discover a security vulnerability in SplitCalc, please report it responsibly.

### How to Report
1. **Do NOT create a public GitHub issue** for security vulnerabilities
2. **Email us directly** at: [security@example.com] (replace with actual email)
3. **Include detailed information** about the vulnerability
4. **Provide steps to reproduce** the issue if possible

### What to Include
Please include the following information in your report:

```
Subject: [SECURITY] SplitCalc Vulnerability Report

Vulnerability Details:
- Type of vulnerability (XSS, injection, etc.)
- Location in code or URL where vulnerability exists
- Potential impact and severity
- Steps to reproduce
- Browser and version where tested
- Your contact information (optional)

Technical Details:
- Proof of concept code (if applicable)
- Screenshots or recordings (if helpful)
- Suggested fix (if you have one)
```

### Response Timeline
- **Acknowledgment**: Within 48 hours of report
- **Initial Assessment**: Within 1 week
- **Status Update**: Weekly updates on progress
- **Resolution**: Target fix within 30 days for critical issues

### Security Process
1. **Report Received**: We acknowledge receipt and begin investigation
2. **Vulnerability Confirmed**: We verify and assess the severity
3. **Fix Development**: We develop and test a security fix
4. **Release Preparation**: We prepare a security update
5. **Public Disclosure**: We release the fix and advisory (coordinated disclosure)

## 🛡️ Security Best Practices for Users

### Safe Usage
- **Use HTTPS**: Access SplitCalc through HTTPS when possible
- **Keep Browser Updated**: Use the latest version of your browser
- **Clear Sensitive Data**: Clear browser data if using on shared computers
- **Export Backup**: Regularly export your data for backup purposes

### Data Protection
- **Sensitive Information**: Avoid entering sensitive personal information in expense descriptions
- **Shared Devices**: Log out or clear data when using shared/public computers
- **Public Networks**: Be cautious when using on public Wi-Fi networks
- **Screen Sharing**: Be aware of screen sharing when handling financial data

### Secure Deployment
If hosting your own instance:
- **Use HTTPS**: Deploy with SSL/TLS certificate
- **Security Headers**: Implement proper security headers
- **Content Security Policy**: Configure CSP headers
- **Access Control**: Restrict access if needed

## 🔍 Security Auditing

### Self-Assessment
We regularly perform security assessments including:
- **Code Review**: Manual review of all code changes
- **Input Validation**: Testing of all user input handling
- **XSS Testing**: Cross-site scripting vulnerability testing
- **Dependency Audit**: Review of external dependencies (minimal)
- **Browser Compatibility**: Security testing across browsers

### Third-Party Security
- **CDN Security**: TailwindCSS is loaded from trusted CDN (cdnjs.cloudflare.com)
- **Supply Chain**: Minimal external dependencies reduce supply chain risks
- **Integrity Checks**: CDN resources use integrity hashes where possible

## 🔒 Privacy Commitment

### Data Handling
- **No Collection**: We do not collect any personal data
- **No Transmission**: No data is sent to external servers
- **No Storage**: We do not store data on any servers
- **No Sharing**: No data sharing as we don't have access to user data

### User Rights
- **Full Control**: Users have complete control over their data
- **Easy Deletion**: Data can be easily cleared from browser settings
- **Portability**: Data can be exported in standard JSON format
- **Transparency**: All code is open source and auditable

## 📋 Security Checklist for Contributors

When contributing code, please ensure:

### Code Security
- [ ] All user inputs are properly validated
- [ ] No use of `eval()` or similar dangerous functions
- [ ] Proper escaping of user-generated content
- [ ] No inline JavaScript in HTML
- [ ] No external script injection vulnerabilities

### Data Security
- [ ] No sensitive data logged to console
- [ ] Proper handling of user data in localStorage
- [ ] No data transmission to external services
- [ ] Clear data handling documentation

### Dependencies
- [ ] No new external dependencies without approval
- [ ] CDN resources from trusted sources only
- [ ] Integrity hashes for external resources
- [ ] Regular review of existing dependencies

## 🆘 Security Contact

For security-related inquiries:
- **Email**: [security@example.com] (replace with actual email)
- **Response Time**: Within 48 hours
- **Encryption**: PGP key available upon request

For general questions about security:
- **GitHub Issues**: Use for non-sensitive security questions
- **Documentation**: Refer to this security policy
- **Community**: Discuss in GitHub Discussions

## 🏆 Security Recognition

We appreciate security researchers who help keep SplitCalc secure:

### Hall of Fame
*Security researchers who have responsibly disclosed vulnerabilities will be listed here (with their permission).*

### Acknowledgments
- **Responsible Disclosure**: We follow coordinated disclosure practices
- **Credit**: Security researchers will be credited in release notes
- **Recognition**: Public acknowledgment for significant contributions

---

## 📚 Additional Resources

- **OWASP Guidelines**: We follow OWASP security best practices
- **Browser Security**: MDN Web Security documentation
- **Privacy Policy**: See README.md for privacy information
- **Code Audit**: All code is open source and auditable

---

**Last Updated**: January 2025
**Version**: 1.0

For the most current security information, always refer to this document in the main branch of the repository.