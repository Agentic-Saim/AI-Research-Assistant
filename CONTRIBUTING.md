# Contributing to IntellectAI

Thank you for your interest in contributing to IntellectAI! We welcome contributions from the community and are grateful for any help you can provide.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [How to Contribute](#how-to-contribute)
- [Development Workflow](#development-workflow)
- [Coding Standards](#coding-standards)
- [Pull Request Guidelines](#pull-request-guidelines)
- [Reporting Bugs](#reporting-bugs)
- [Suggesting Features](#suggesting-features)

## Code of Conduct

By participating in this project, you agree to abide by our code of conduct. Please be respectful, inclusive, and constructive in all interactions.

## Getting Started

### 1. Fork the Repository

Click the "Fork" button on GitHub to create your own copy of the repository.

### 2. Clone Your Fork

```bash
git clone https://github.com/YOUR_USERNAME/IntellectAI.git
cd IntellectAI
```

### 3. Set Up Development Environment

```bash
# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Copy environment variables
cp .env.example .env
# Edit .env with your API keys
```

### 4. Run Tests

```bash
# Run the test suite
python -m pytest tests/

# Or run the main application
python main.py "test topic"
```

## How to Contribute

There are many ways to contribute to IntellectAI:

### 🐛 Bug Fixes
- Find and fix reported bugs
- Look for issues labeled `good-first-issue` or `help-wanted`

### ✨ New Features
- Implement new research tools
- Add export formats (PDF, HTML, JSON)
- Improve the web interface
- Enhance the CLI experience

### 📚 Documentation
- Improve existing documentation
- Add code comments and docstrings
- Create usage examples
- Write tutorials

### 🧪 Testing
- Add unit tests for existing code
- Create integration tests
- Improve test coverage

### 🎨 Code Quality
- Refactor code for better readability
- Optimize performance
- Reduce API costs
- Improve error handling

## Development Workflow

### 1. Create a Branch

```bash
git checkout -b feature/your-feature-name
# or
git checkout -b fix/issue-description
```

**Branch naming conventions:**
- `feature/` - New features
- `fix/` - Bug fixes
- `docs/` - Documentation changes
- `refactor/` - Code refactoring
- `test/` - Test additions/improvements

### 2. Make Your Changes

- Follow the coding standards below
- Keep changes focused and minimal
- Add tests for new functionality
- Update documentation as needed

### 3. Test Your Changes

```bash
# Run existing tests
python -m pytest tests/ -v

# Test the CLI
python main.py "your test topic"

# Test the API (if applicable)
python -m uvicorn api.index:app --reload
```

### 4. Commit Your Changes

```bash
git add .
git commit -m "type: brief description of changes"
```

**Commit message format:**
- `feat:` - New feature
- `fix:` - Bug fix
- `docs:` - Documentation
- `refactor:` - Code refactoring
- `test:` - Test changes
- `chore:` - Maintenance tasks

Example: `feat: add PDF export functionality`

### 5. Push and Create a Pull Request

```bash
git push origin feature/your-feature-name
```

Then create a Pull Request on GitHub with a clear description.

## Coding Standards

### Python Style Guide

- Follow **PEP 8** guidelines
- Use **4 spaces** for indentation (no tabs)
- Maximum line length: **88 characters** (compatible with Black formatter)
- Use **type hints** for function signatures

### Code Organization

```python
# Good example with type hints and docstring
def search_web(query: str, max_results: int = 10) -> list[dict]:
    """
    Search the web for a given query and return results.
    
    Args:
        query: The search query string
        max_results: Maximum number of results to return
        
    Returns:
        List of dictionaries containing search results
    """
    # Implementation here
    pass
```

### Best Practices

1. **Error Handling**: Always handle errors gracefully
   ```python
   try:
       result = api_call()
   except APIError as e:
       logger.error(f"API call failed: {e}")
       raise
   ```

2. **Logging**: Use appropriate log levels
   ```python
   logger.debug("Detailed debug info")
   logger.info("Normal operational message")
   logger.warning("Warning message")
   logger.error("Error occurred")
   ```

3. **Documentation**: Add docstrings to all public functions and classes

4. **Type Safety**: Use Pydantic models for data validation

5. **No Hardcoded Values**: Use environment variables or config files

## Pull Request Guidelines

### Before Submitting

- [ ] Your code follows the coding standards
- [ ] You have added tests for new functionality
- [ ] All tests pass successfully
- [ ] You have updated documentation as needed
- [ ] Your commits are clean and well-described

### PR Template

When creating a Pull Request, please include:

```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Documentation update
- [ ] Refactoring

## Testing
How did you test these changes?

## Screenshots (if applicable)
Add screenshots to demonstrate UI changes

## Related Issues
Closes #issue_number
```

## Reporting Bugs

We use GitHub Issues to track bugs. When reporting a bug, please include:

1. **Description**: Clear and detailed description
2. **Steps to Reproduce**: Exact steps to reproduce the issue
3. **Expected Behavior**: What you expected to happen
4. **Actual Behavior**: What actually happened
5. **Environment**: Python version, OS, dependencies
6. **Logs**: Relevant error logs or stack traces

**Template:**
```markdown
**Describe the bug**
A clear description of what the bug is.

**To Reproduce**
1. Run command '...'
2. Enter input '...'
3. See error

**Expected behavior**
A clear description of what you expected to happen.

**Error logs**
```
Paste error logs here
```
```

## Suggesting Features

We love hearing your ideas! To suggest a feature:

1. Open an issue with the label `enhancement`
2. Provide a clear description of the feature
3. Explain why it would be valuable
4. Include implementation ideas if possible

## Questions?

If you have any questions or need help, feel free to:
- Open an issue
- Join discussions on existing issues
- Reach out to the maintainers

---

Thank you for contributing to IntellectAI! 🎉
