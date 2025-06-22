# Contributing to SplitCalc 🤝

Thank you for considering contributing to SplitCalc! We appreciate your interest in making this expense-splitting tool even better.

## 🌟 Ways to Contribute

### 🐛 Bug Reports
- Search existing issues before creating new ones
- Use the bug report template
- Include detailed steps to reproduce
- Mention your browser and version
- Add screenshots for UI issues

### 💡 Feature Requests  
- Check if the feature already exists or is planned
- Use the feature request template
- Explain the use case clearly
- Consider how it fits with existing functionality

### 📝 Code Contributions
- Follow our development guidelines
- Test your changes thoroughly
- Maintain the single-file architecture
- Keep it lightweight and fast

### 📚 Documentation
- Fix typos and improve clarity
- Add examples and use cases
- Update outdated information
- Translate documentation

## 🚀 Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Basic knowledge of HTML, CSS, JavaScript
- Text editor or IDE
- Git for version control

### Development Setup
1. **Fork the repository**
   ```bash
   git clone https://github.com/YOUR_USERNAME/splitcalc.git
   cd splitcalc
   ```

2. **Create a development branch**
   ```bash
   git checkout -b feature/your-feature-name
   # or
   git checkout -b fix/bug-description
   ```

3. **Make your changes**
   - Edit `index.html` (single file application)
   - Test in multiple browsers
   - Ensure responsive design works

4. **Test locally**
   ```bash
   # Option 1: Direct file open
   open index.html
   
   # Option 2: Local server (recommended)
   python -m http.server 8000
   # Visit http://localhost:8000
   ```

## 📋 Development Guidelines

### Code Style
- **Indentation**: 2 spaces (no tabs)
- **Naming**: camelCase for JavaScript, kebab-case for CSS
- **Comments**: Clear, concise comments for complex logic
- **Functions**: Small, focused functions with descriptive names

### Architecture Constraints
- **Single File**: All code must remain in `index.html`
- **No External Dependencies**: Only TailwindCSS via CDN allowed
- **Vanilla JavaScript**: No frameworks or libraries
- **Browser Storage**: Use localStorage only (no external APIs)

### Testing Checklist
- [ ] Works in Chrome/Chromium
- [ ] Works in Firefox  
- [ ] Works in Safari
- [ ] Works in Edge
- [ ] Mobile responsive (test on actual devices)
- [ ] Touch interactions work properly
- [ ] Offline functionality intact
- [ ] Data persists correctly
- [ ] Export/Import functions work
- [ ] All calculations are accurate

### Performance Guidelines
- Keep the file size minimal
- Optimize images and assets
- Use efficient algorithms
- Minimize DOM manipulations
- Test with large datasets

## 🔄 Pull Request Process

### Before Submitting
1. **Update documentation** if needed
2. **Test thoroughly** across browsers
3. **Check responsiveness** on different screen sizes
4. **Verify accessibility** basics
5. **Ensure backward compatibility**

### Pull Request Template
```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature  
- [ ] Documentation update
- [ ] Performance improvement
- [ ] Code refactoring

## Testing
- [ ] Tested in Chrome
- [ ] Tested in Firefox
- [ ] Tested in Safari  
- [ ] Tested on mobile
- [ ] Verified calculations accuracy

## Screenshots
Add screenshots for UI changes

## Additional Notes
Any additional context or considerations
```

### Review Process
1. **Automated checks** (if any) must pass
2. **Code review** by maintainers
3. **Testing verification** on multiple browsers
4. **Documentation review** if applicable
5. **Final approval** and merge

## 🏷️ Commit Message Guidelines

### Format
```
type(scope): short description

Longer description if needed

Fixes #123
```

### Types
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, etc.)
- `refactor`: Code refactoring
- `perf`: Performance improvements
- `test`: Adding or updating tests
- `chore`: Maintenance tasks

### Examples
```bash
feat: add expense category filtering
fix: resolve balance calculation for edge cases
docs: update installation instructions
style: improve mobile layout spacing
refactor: optimize settlement calculation algorithm
```

## 🐛 Bug Report Template

When reporting bugs, please include:

```markdown
**Describe the bug**
Clear description of what the bug is

**To Reproduce**
Steps to reproduce the behavior:
1. Go to '...'
2. Click on '...'
3. Enter '...'
4. See error

**Expected behavior**
What you expected to happen

**Screenshots**
Add screenshots if applicable

**Environment:**
- Browser: [e.g. Chrome 120]
- OS: [e.g. Windows 11]
- Device: [e.g. Desktop/Mobile]
- Screen size: [if relevant]

**Additional context**
Any other context about the problem
```

## 💡 Feature Request Template

```markdown
**Is your feature request related to a problem?**
Clear description of the problem

**Describe the solution you'd like**
Clear description of what you want to happen

**Describe alternatives you've considered**
Alternative solutions or features you've considered

**Use case**
Specific scenario where this would be helpful

**Additional context**
Mockups, examples, or other context
```

## 📊 Priority Labels

We use these labels to organize issues:

- `🔥 urgent`: Critical bugs affecting core functionality
- `🚀 enhancement`: New features and improvements  
- `🐛 bug`: Confirmed bugs
- `📚 documentation`: Documentation improvements
- `🎨 ui/ux`: User interface and experience improvements
- `🔧 maintenance`: Code maintenance and refactoring
- `❓ question`: Questions and discussions
- `👍 good first issue`: Good for newcomers

## 🤔 Questions and Support

- **General questions**: Create a GitHub issue with the `question` label
- **Feature discussions**: Start a GitHub discussion
- **Bug reports**: Use the bug report template
- **Live demo**: [https://splitcalc-mini.onrender.com/](https://splitcalc-mini.onrender.com/)

## 📜 Code of Conduct

### Our Pledge
We are committed to providing a welcoming and inclusive experience for everyone, regardless of background or identity.

### Expected Behavior
- Be respectful and constructive
- Focus on what's best for the community
- Show empathy towards others
- Give and receive feedback gracefully

### Unacceptable Behavior
- Harassment or discrimination
- Trolling or insulting comments
- Publishing private information
- Any conduct inappropriate in a professional setting

### Enforcement
Issues can be reported to project maintainers. All complaints will be reviewed and investigated promptly and fairly.

## 🙏 Recognition

Contributors will be recognized in:
- GitHub contributor list
- Release notes for significant contributions
- Special thanks section for major features

Thank you for helping make SplitCalc better! 🎉