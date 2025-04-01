# Collaboration Guidelines

## Getting Started

1. Fork the repository
2. Clone your fork locally
3. Set up the development environment following the instructions in the main README.md
4. Create a new branch for your work

## Code Style

- Follow PEP 8 style guide for Python code
- Use meaningful variable and function names
- Add docstrings to all functions and classes
- Include type hints where appropriate
- Keep functions focused and single-purpose
- Add comments to explain complex logic

## Git Workflow

1. Create a branch for your feature/fix:
```bash
git checkout -b feature/your-feature-name
```

2. Make your changes and commit them:
```bash
git add .
git commit -m "Description of changes"
```

3. Push to your fork:
```bash
git push origin feature/your-feature-name
```

4. Create a Pull Request from your fork to the main repository

## Jupyter Notebook Guidelines

1. Clear all outputs before committing
2. Use markdown cells to document analysis steps
3. Keep code cells focused and single-purpose
4. Include requirements and dependencies at the top of the notebook
5. Use relative paths for data files

## Data Management

- Raw data should be placed in `02_data/02.01_raw/`
- Document data sources and preprocessing steps
- Include data dictionaries where applicable
- Do not commit large data files (use .gitignore)

## Documentation

- Update README.md when adding new features
- Document any new dependencies in requirements.txt
- Add docstrings to all new functions
- Include examples in documentation where helpful

## Code Review Process

1. All changes must be reviewed before merging
2. Reviewers should check for:
   - Code style compliance
   - Documentation completeness
   - Test coverage
   - Performance considerations
   - Security implications

## Questions and Support

- Open an issue for bug reports or feature requests
- Use pull request discussions for code-related questions
- Contact the research team for project-specific questions

## License and Attribution

- All contributions must comply with the project license
- Cite sources and references where applicable
- Respect intellectual property rights
