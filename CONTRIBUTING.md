# Contributing to BEACON

Thank you for your interest in contributing to BEACON!

This guide explains how to contribute CAD designs and 3D models to the project.

---

## Before You Start

### Understanding Our Workflow

We use a **fork-first workflow**. This means:
- You work on your own copy (fork) of the repository
- Changes are proposed via Pull Requests from your fork
- This keeps the main repository clean and organized

---

## Fork-First Workflow

### Step 1: Fork the Repository

1. Click the "Fork" button on the repository page
2. This creates your personal copy at `github.com/YOUR-USERNAME/beacon`

### Step 2: Clone Your Fork

```bash
git clone https://github.com/YOUR-USERNAME/beacon.git
cd beacon

git remote add upstream https://github.com/The-OASIS-Project/beacon.git
```

### Step 3: Create a Feature Branch

```bash
git checkout -b type/description
```

---

## File Guidelines

### Required Formats

| Type | Required | Optional |
|------|----------|----------|
| 3D Printable | `.stl` | `.3mf` |
| CAD Source | `.step` | Native format (`.f3d`, `.FCStd`) |
| Reference | `.png` | `.jpg` |

### Naming Convention

```
[Component]-[Version]_[Variant].[ext]

Examples:
- HorizonHUD-MK3.17_v7_p1.stl
- Jetson_Sling_Base_v2.stl
- headphone clamp bottom v3.stl
```

### Version Numbering

- Increment version number for design changes
- Use `_p1`, `_p2`, etc. for multi-part assemblies
- Use descriptive variants: `_large`, `_tight`, `_slim`

---

## Design Standards

### Print Considerations

- Design for 0.2mm layer height unless noted
- Minimize support requirements where possible
- Consider print orientation in design
- Test fit with mating components

### File Quality

- Manifold/watertight STL meshes
- Reasonable polygon count (not excessively high)
- Correct scale (millimeters)
- Proper orientation (Z-up)

### Documentation

For new components, include:
- Reference image showing the part
- Brief description in PR
- Print settings if non-standard
- Assembly notes if multi-part

---

## Contribution Types

### New Components

1. Create design in your CAD software
2. Export `.stl` (for printing) and `.step` (for editing)
3. Add reference image
4. Place in appropriate directory
5. Submit PR with description

### Design Improvements

1. Import existing `.step` file
2. Make modifications
3. Increment version number
4. Export new files
5. Submit PR explaining changes

### Bug Fixes

Common issues to fix:
- Non-manifold geometry
- Incorrect dimensions
- Print failures
- Fit issues with other components

---

## Pull Request Process

### Before Submitting

- [ ] Files follow naming convention
- [ ] STL is manifold/watertight
- [ ] STEP file included for editable source
- [ ] Reference image provided (for new parts)
- [ ] Tested print (if possible)

### PR Description Template

```markdown
## Summary
Brief description of the component or change.

## Type of Change
- [ ] New component
- [ ] Design improvement
- [ ] Bug fix (geometry issues)
- [ ] Documentation

## Files Added/Changed
List of files

## Print Settings (if applicable)
- Layer height:
- Infill:
- Supports:
- Material:

## Testing
How was this tested? (printed, fit-checked, etc.)
```

---

## Code of Conduct

We are committed to providing a welcoming and inclusive environment.
Please be respectful and constructive in all interactions.

---

## Getting Help

- **Questions**: Open a GitHub Discussion or Issue
- **Design Issues**: Open an issue describing the problem
- **O.A.S.I.S. Ecosystem**: See [S.C.O.P.E.](https://github.com/malcolmhoward/the-oasis-project-meta-repo) for cross-project coordination
