---
marp: true
theme: custom
paginate: true
size: 16:9
style: |
  /* Custom theme specification */
  @import 'default';
  
  section {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
  }
  
  section.title {
    text-align: center;
    background: linear-gradient(45deg, #1e3c72 0%, #2a5298 100%);
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  
  section.background-image {
    background-image: url('https://images.unsplash.com/photo-1518773553398-650c184e0bb3?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80');
    background-size: cover;
    background-position: center;
    color: white;
    text-shadow: 2px 2px 4px rgba(0,0,0,0.8);
  }
  
  h1 {
    color: #FFD700;
    text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
    border-bottom: 3px solid #FFD700;
    padding-bottom: 10px;
  }
  
  h2 {
    color: #87CEEB;
    margin-bottom: 20px;
  }
  
  code {
    background-color: rgba(0,0,0,0.3);
    padding: 2px 6px;
    border-radius: 4px;
    color: #FFD700;
  }
  
  pre {
    background-color: rgba(0,0,0,0.4);
    border-left: 4px solid #FFD700;
    padding: 15px;
    border-radius: 8px;
  }
  
  .highlight {
    background-color: rgba(255, 215, 0, 0.2);
    padding: 10px;
    border-radius: 8px;
    border: 2px solid #FFD700;
  }
  
  .author-info {
    position: absolute;
    bottom: 20px;
    right: 20px;
    font-size: 0.8em;
    opacity: 0.8;
  }
---

<!-- _class: title -->
<!-- _paginate: false -->

# Technical Documentation with Marp

## Creating Maintainable Presentations for Software Teams

**Professional Documentation Standards**

<div class="author-info">
Contact: 22f1000662@ds.study.iitm.ac.in
</div>

---

# Table of Contents

## 📋 What We'll Cover

- **Introduction to Marp** - Modern presentation framework
- **Version Control Integration** - Git-friendly workflows  
- **Custom Styling** - Themes and directives
- **Mathematical Equations** - Algorithm complexity
- **Best Practices** - Maintainable documentation
- **Export Options** - Multiple output formats

---

# What is Marp?

## Markdown Presentation Ecosystem

**Marp** (Markdown Presentation) enables you to create slide presentations using pure Markdown syntax.

### Key Benefits:
- 📝 **Version Control Friendly** - Text-based, perfect for Git
- 🎨 **Highly Customizable** - CSS styling and themes
- 📊 **Multi-format Export** - PDF, HTML, PPTX, PNG
- ⚡ **Fast Development** - No complex GUI tools needed
- 🔄 **Reproducible Builds** - Consistent output across environments

```markdown
---
marp: true
theme: default
---
# Your slide content here
```

---

<!-- _class: background-image -->

# Working with Background Images

## Visual Impact in Technical Presentations

This slide demonstrates how to use **background images** effectively in Marp presentations for technical documentation.

### Implementation:
```css
section.background-image {
  background-image: url('your-image-url');
  background-size: cover;
  background-position: center;
  text-shadow: 2px 2px 4px rgba(0,0,0,0.8);
}
```

---

# Custom Theme Directives

## Marp-Specific Features

Marp provides powerful directives for slide customization:

| Directive | Purpose | Example |
|-----------|---------|---------|
| `<!-- _class: -->` | Apply CSS class to slide | `<!-- _class: title -->` |
| `<!-- _paginate: -->` | Control page numbers | `<!-- _paginate: false -->` |
| `<!-- _backgroundColor: -->` | Set slide background | `<!-- _backgroundColor: #1e3c72 -->` |
| `<!-- _color: -->` | Set text color | `<!-- _color: white -->` |

<div class="highlight">
💡 <strong>Pro Tip:</strong> Use leading underscores for slide-specific directives, without underscores for global settings.
</div>

---

# Mathematical Equations in Documentation

## Algorithm Complexity Analysis

When documenting algorithms, mathematical notation is essential:

### Time Complexity Examples:

**Linear Search:**
$$T(n) = O(n)$$

**Binary Search:**  
$$T(n) = O(\log n)$$

**Quick Sort Average Case:**
$$T(n) = O(n \log n)$$

**Matrix Multiplication:**
$$T(n) = O(n^3)$$

### Space Complexity:
For a recursive algorithm with depth $d$ and space $s$ per call:
$$S(n) = O(d \times s)$$

---

# Version Control Best Practices

## Git Integration Strategies

### Repository Structure:
```
project-docs/
├── presentations/
│   ├── slides.md          # Main presentation
│   ├── themes/
│   │   └── custom.css     # Theme files
│   └── assets/
│       └── images/        # Local images
├── exports/               # Generated outputs
│   ├── slides.pdf
│   ├── slides.html
│   └── slides.pptx
└── .github/
    └── workflows/
        └── build-slides.yml
```

### Automated Builds:
- **GitHub Actions** for automatic PDF generation
- **Version tagging** for release presentations  
- **Branch protection** for main presentation files

---

# Export and Distribution

## Multiple Output Formats

Marp CLI provides comprehensive export options:

### Command Examples:
```bash
# Export to PDF
marp slides.md --pdf

# Export to HTML with theme
marp slides.md --html --theme custom

# Export to PowerPoint
marp slides.md --pptx

# Watch mode for development
marp slides.md --watch --server
```

### CI/CD Integration:
```yaml
- name: Build presentations
  run: |
    npm install -g @marp-team/marp-cli
    marp slides.md --pdf --html --allow-local-files
```

---

# Advanced Styling Techniques

## CSS Customization

### Custom Animations:
```css
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

section h1 {
  animation: fadeInUp 0.8s ease-out;
}
```

### Responsive Design:
```css
section {
  font-size: clamp(16px, 2.5vw, 24px);
  padding: clamp(20px, 5vw, 60px);
}
```

---

# Best Practices Summary

## Maintainable Technical Documentation

### ✅ Do:
- Use semantic Markdown structure
- Keep themes in separate files
- Include version information
- Test exports regularly
- Document custom directives

### ❌ Avoid:
- Inline styles in Markdown
- Large embedded images
- Complex nested layouts
- Platform-specific paths
- Hardcoded dimensions

<div class="highlight">
<strong>Remember:</strong> Great technical documentation is clear, consistent, and easily maintainable by your entire team.
</div>

---

<!-- _class: title -->
<!-- _paginate: false -->

# Thank You

## Questions & Discussion

**Technical Documentation with Marp**  
*Creating Professional, Version-Controlled Presentations*

---

**Contact Information:**  
📧 22f1000662@ds.study.iitm.ac.in

**Resources:**  
🔗 [Marp Official Documentation](https://marp.app/)  
🔗 [GitHub Repository](https://github.com/marp-team/marp)

---

# Appendix: Quick Reference

## Essential Marp Syntax

```markdown
---
marp: true
theme: default
paginate: true
---

# Slide Title
Content goes here

---
<!-- _class: custom-class -->
# Special Slide
With custom styling
```

### Math Notation:
- Inline: `$E = mc^2$` → $E = mc^2$
- Block: `$$\sum_{i=1}^{n} x_i$$` → $$\sum_{i=1}^{n} x_i$$

**End of Presentation**
