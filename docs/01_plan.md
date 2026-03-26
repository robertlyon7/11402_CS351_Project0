
# Two Sum Problem - Solution Plan

## Problem Statement
Find two numbers in an array that add up to a target sum and return their indices.

## Approach

### Solution 1: Hash Map (Optimal)
- **Time Complexity:** O(n)
- **Space Complexity:** O(n)
- Use a hash map to store values and their indices
- For each number, check if `target - num` exists in the map
- Return indices when match is found

### Solution 2: Brute Force
- **Time Complexity:** O(n²)
- **Space Complexity:** O(1)
- Nested loops to check all pairs
- Simple but inefficient for large datasets

## Implementation Steps
1. Create hash map to track seen numbers
2. Iterate through array once
3. For each element, calculate complement (`target - current`)
4. Check if complement exists in hash map
5. Return indices or continue to next element

## Testing
- Test with valid pairs
- Test with no solution
- Test with duplicate numbers
- Test edge cases (empty array, single element)
