
# Acceptance Tests: Two Sum

## Feature: Two Sum Function

### Scenario 1: Basic Example
**Given** an array of integers `[2, 7, 11, 15]` and target `9`
**When** the two sum function is called
**Then** it returns `[0, 1]` (indices of 2 and 7)

### Scenario 2: Different Order
**Given** an array `[3, 2, 4]` and target `6`
**When** the two sum function is called
**Then** it returns `[1, 2]` (indices of 2 and 4)

### Scenario 3: No Solution
**Given** an array `[1, 2, 3]` and target `10`
**When** the two sum function is called
**Then** it returns `null` or an empty result

### Scenario 4: Duplicate Numbers
**Given** an array `[3, 3]` and target `6`
**When** the two sum function is called
**Then** it returns `[0, 1]`

### Scenario 5: Negative Numbers
**Given** an array `[-1, -2, -3, 5, 10]` and target `7`
**When** the two sum function is called
**Then** it returns `[3, 4]` (indices of -3 and 10)
