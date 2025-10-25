# Doctor Who Episodes Explorer - Variant B

## Core Requirements (60 points)
Same as base requirements.

## Edge Case Focus (25 points)

### Primary Focus (15 points)
1. **Multiple Writer Handling (8 points)**
   - Parse writer separators ("&", "and")
   - Display multiple writers clearly
   - Include in writer filter
   - Sort considering all writers

2. **Special Character Handling (7 points)**
   - Display quotes correctly
   - Handle apostrophes
   - Process slashes in titles
   - Support accented characters

### Secondary Focus (10 points)
1. **Array Handling (5 points)**
   - Process empty arrays
   - Display array counts
   - Sort with empty arrays

2. **General Text Processing (5 points)**
   - Trim whitespace
   - Normalize case for sorting
   - Handle missing text fields

## Advanced Features (Choose 2, 15 points)

### Available Options
1. **Performance Optimization (5 points)**
   - Optimize for large datasets
   - Implement lazy loading
   - Use efficient sorting

2. **Multi-column Sort (5 points)**
   - Shift+click to add sort levels
   - Clear sort indicators
   - Priority ordering

3. **Export CSV (5 points)**
   - Include all columns
   - Proper string escaping
   - Download functionality

4. **Data Validation (5 points)**
   - Required field checks
   - Format validation
   - Warning display