# Changelog 📜

All notable changes to SplitCalc will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]
### Planned Features
- Expense categories and filtering
- Multiple currency support
- Receipt image upload
- Group templates for recurring splits
- Advanced settlement optimization

---

## [1.0.0] - 2024-01-XX
### 🎉 Initial Release
The first stable release of SplitCalc with core expense splitting functionality.

#### ✨ Added
- **Core Functionality**
  - Member management (add/remove participants)
  - Expense tracking with title, amount, payer, and participants
  - Automatic balance calculation and settlement suggestions
  - Real-time balance updates
  
- **Advanced Features**
  - Expense history with removal options
  - Calculation history (save/restore up to 3 calculations)
  - Complete data export/import in JSON format
  - Auto-save using localStorage
  - Detailed calculation breakdown with methodology
  
- **User Interface**
  - Modern gradient-based design
  - Fully responsive layout (desktop, tablet, mobile)
  - Smooth animations and transitions
  - Intuitive controls with select all/deselect all options
  - Touch-friendly mobile interface
  
- **Technical Features**
  - Single-file architecture for easy deployment
  - No external dependencies (except TailwindCSS CDN)
  - Client-side only operation (works offline)
  - Cross-browser compatibility
  - Local data persistence

#### 🔧 Technical Details
- **Architecture**: Single HTML file with embedded CSS and JavaScript
- **Styling**: TailwindCSS via CDN for responsive design
- **Storage**: localStorage for data persistence
- **Performance**: Optimized for fast loading and smooth interactions
- **Compatibility**: Supports all modern browsers

#### 🚀 Deployment
- Live demo available at: https://splitcalc-mini.onrender.com/
- Can be deployed to any static hosting service
- Works offline after first load

---

## Version History Format

### [Version] - Date
#### 🎉 Added
- New features

#### 🔧 Changed  
- Changes in existing functionality

#### 🐛 Fixed
- Bug fixes

#### 🗑️ Removed
- Removed features

#### 🔒 Security
- Security improvements

#### ⚡ Performance
- Performance improvements

---

## Development Milestones

### Pre-Release Development
- **Concept Phase**: Initial idea and planning
- **Core Development**: Basic expense splitting functionality
- **UI/UX Enhancement**: Modern design implementation
- **Feature Expansion**: Advanced features and data management
- **Testing & Optimization**: Cross-browser testing and performance optimization
- **Documentation**: Comprehensive documentation and guides

### Release Preparation
- **Beta Testing**: Internal testing and bug fixes
- **Performance Optimization**: Final performance improvements
- **Documentation Review**: Complete documentation audit
- **Deployment Setup**: Live demo deployment

---

## Contributing to Changelog

When contributing to SplitCalc, please update this changelog:

### Guidelines
1. **Format**: Follow the established format above
2. **Categories**: Use appropriate categories (Added, Changed, Fixed, etc.)
3. **Description**: Provide clear, concise descriptions
4. **User Impact**: Focus on user-facing changes
5. **Technical Details**: Include relevant technical information

### Example Entry
```markdown
### [1.1.0] - 2024-XX-XX
#### ✨ Added
- Expense category filtering for better organization
- Dark mode toggle for better user experience
- Keyboard shortcuts for power users

#### 🔧 Changed
- Improved mobile layout for better touch interactions
- Enhanced calculation display with better formatting

#### 🐛 Fixed
- Fixed balance calculation edge case with zero amounts
- Resolved mobile keyboard overlapping input fields
- Fixed export filename generation on Safari

#### ⚡ Performance
- Optimized rendering for large expense lists
- Reduced memory usage for calculation history
```

---

## Release Process

### Version Numbering
- **Major (X.0.0)**: Breaking changes, major new features
- **Minor (1.X.0)**: New features, backward compatible
- **Patch (1.1.X)**: Bug fixes, small improvements

### Release Checklist
- [ ] Update version number in code
- [ ] Update CHANGELOG.md
- [ ] Test across all supported browsers
- [ ] Verify mobile responsiveness
- [ ] Update live demo
- [ ] Create GitHub release
- [ ] Update documentation if needed

---

**For the complete history of changes, see the [GitHub Releases](https://github.com/yourusername/splitcalc/releases) page.**