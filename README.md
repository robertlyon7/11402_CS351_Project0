# Two Sum Problem

Given an array of integers and a target sum, find two distinct indices whose values add up to the target. Return the indices in any order. This is a classic problem that can be efficiently solved using a hash map to track seen values while iterating through the array.

## Requirements

### Programming Language & Tools
- **Language**: C++ 20
- **Data Structure**: STL `vector`
- **Build System**: CMake
- **Testing**: Google Test (gtest)
- **CI/CD**: GitHub Actions
- **Containerization**: Docker

### Implementations
1. **TwoSumArray**: Brute force approach with nested loops, O(n²) time complexity
2. **TwoSumHashTable**: Hash map approach for O(n) time complexity

### Test Cases
- Empty array
- Array with two elements that sum to target
- Array with no valid pair
- Negative integers
- Duplicate values
- Large arrays

### Continuous Integration
- GitHub Actions workflow to automatically compile and run tests on push
- Docker image for consistent test environment across platforms

### Deliverables
- Source code with both implementations
- Unit tests covering all test cases
- Dockerfile for containerized builds
- GitHub Actions workflow configuration
- CMakeLists.txt for build automation

## GitHub Actions Configuration

### Workflow Setup
Create `.github/workflows/test.yml` to automatically compile and test on every push:

```yaml
name: Build and Test

on: [push, pull_request]

jobs:
   test:
      runs-on: ubuntu-latest
      
      steps:
         - uses: actions/checkout@v3
         
         - name: Install dependencies
            run: |
               sudo apt-get update
               sudo apt-get install -y cmake g++ libgtest-dev
         
         - name: Build project
            run: |
               mkdir build
               cd build
               cmake ..
               make
         
         - name: Run tests
            run: ./build/TwoSumTest
```

### Docker Integration
Alternatively, use Docker for consistent environment:

```yaml
         - name: Build Docker image
            run: docker build -t two-sum:latest .
         
         - name: Run tests in container
            run: docker run two-sum:latest ./build/TwoSumTest
```

### Workflow Triggers
- Automatically runs on push to any branch
- Runs on pull requests for validation
- Optional: Schedule weekly test runs with `schedule` trigger

### Test Output
- GitHub displays pass/fail status on commits
- Detailed logs available in Actions tab
- Failed tests block merge to main branch (optional protection rule)