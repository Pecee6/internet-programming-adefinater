# Doctor Who Episodes Explorer - Variant A

## Core Requirements (60 points)
Same as base requirements.

## Edge Case Focus (25 points)

### Primary Focus (15 points)
1. **Null Companion Handling (8 points)**
   - Show "No Companion" for null values
   - Include companion in filters
   - Sort properly with null values
   - Consistent display across all views

2. **Date Format Handling (7 points)**
   - Parse all date formats correctly:
     - YYYY-MM-DD
     - DD/MM/YYYY
     - Month DD, YYYY
     - YYYY only
   - Sort chronologically regardless of format
   - Display in consistent format

### Secondary Focus (10 points)
1. **Error Display (5 points)**
   - Clear error messages for load failures
   - User-friendly error formatting
   - Error recovery options

2. **Basic Validation (5 points)**
   - Validate required fields
   - Check date formats
   - Report validation errors

## Advanced Features (Choose 2, 15 points)

### Available Options
1. **Performance Optimization (5 points)**
   - Handle 1000+ episodes smoothly
   - Implement virtualization
   - Optimize sorting/filtering

2. **Keyboard Navigation (5 points)**
   - Arrow key table navigation
   - Enter key sorting
   - Tab through filters

3. **Smart Relevance Sort (5 points)**
   - Exact match first
   - Contains search term second
   - Any field contains third

4. **Data Validation (5 points)**
   - Check for future dates
   - Validate rank values
   - Log validation issues