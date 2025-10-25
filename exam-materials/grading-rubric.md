# Doctor Who Episodes Explorer - Grading Rubric

## Tier 1: Basic Functionality (60 points)

### Data Loading (15 points)
| Criterion | Points | Requirements |
|-----------|---------|--------------|
| Fetch Implementation | 5 | • Correctly fetches data from endpoint<br>• Uses proper error handling |
| Loading State | 5 | • Shows loading indicator<br>• Hides when complete/error |
| Error Handling | 5 | • Displays user-friendly error messages<br>• Handles network failures |

### Table Display (10 points)
| Criterion | Points | Requirements |
|-----------|---------|--------------|
| Basic Structure | 5 | • All required columns present<br>• Proper HTML table structure |
| Data Formatting | 5 | • Correct display of nested data<br>• Basic text formatting |

### Column Sorting (15 points)
| Criterion | Points | Requirements |
|-----------|---------|--------------|
| Sort Implementation | 8 | • Correct ascending/descending toggle<br>• Proper sort logic for all types |
| Sort Indicators | 4 | • Clear visual indicators<br>• Shows current sort state |
| Performance | 3 | • Sorting completes without freezing UI<br>• Works with full dataset |

### Name Filtering (10 points)
| Criterion | Points | Requirements |
|-----------|---------|--------------|
| Filter Logic | 6 | • Case-insensitive matching<br>• Partial string matching |
| UI Implementation | 4 | • Input field works correctly<br>• Updates results in real-time |

### Basic Error Handling (5 points)
| Criterion | Points | Requirements |
|-----------|---------|--------------|
| Input Validation | 3 | • Prevents invalid interactions<br>• Handles empty/invalid input |
| UI Feedback | 2 | • Shows when no results match<br>• Clear error states |

### Loading State (5 points)
| Criterion | Points | Requirements |
|-----------|---------|--------------|
| Visual Indicator | 3 | • Clear loading animation/text<br>• Visible during data operations |
| State Management | 2 | • Proper show/hide timing<br>• No flickering/jumps |

## Tier 2: Edge Case Handling (25 points)

### Null/Missing Data (5 points)
| Criterion | Points | Requirements |
|-----------|---------|--------------|
| Companion Handling | 3 | • Shows "None" or "—" for null<br>• Consistent display |
| General Nulls | 2 | • Handles all potential null fields<br>• No "undefined" shown |

### Empty Arrays (3 points)
| Criterion | Points | Requirements |
|-----------|---------|--------------|
| Cast Display | 2 | • Shows "0" or appropriate message<br>• Consistent empty state |
| Array Handling | 1 | • No errors on empty arrays<br>• Proper display |

### Multiple Writers (3 points)
| Criterion | Points | Requirements |
|-----------|---------|--------------|
| Display Format | 2 | • Shows all writers clearly<br>• Proper separator usage |
| Sort Handling | 1 | • Correct sort with multiple writers |

### Date Handling (7 points)
| Criterion | Points | Requirements |
|-----------|---------|--------------|
| Format Support | 4 | • Handles all date formats<br>• Consistent display |
| Sort Logic | 3 | • Correct chronological sorting<br>• Handles invalid dates |

### Special Characters (4 points)
| Criterion | Points | Requirements |
|-----------|---------|--------------|
| Display | 2 | • Renders all special chars<br>• No escaping visible |
| Filtering | 2 | • Works with special chars<br>• Case insensitive |

### Error Messages (3 points)
| Criterion | Points | Requirements |
|-----------|---------|--------------|
| Clarity | 2 | • Clear error messages<br>• User-friendly wording |
| Display | 1 | • Proper placement<br>• Appropriate styling |

## Tier 3: Advanced Features (15 points)

### Feature 1 (Choose one: 5 points)
| Criterion | Points | Requirements |
|-----------|---------|--------------|
| Implementation | 3 | • Core functionality works<br>• Follows best practices |
| Integration | 2 | • Works with existing features<br>• Proper error handling |

### Feature 2 (Choose one: 5 points)
| Criterion | Points | Requirements |
|-----------|---------|--------------|
| Implementation | 3 | • Core functionality works<br>• Follows best practices |
| Integration | 2 | • Works with existing features<br>• Proper error handling |

### Documentation (5 points)
| Criterion | Points | Requirements |
|-----------|---------|--------------|
| Code Comments | 3 | • Explains complex logic<br>• Documents edge cases |
| Feature Usage | 2 | • Clear usage instructions<br>• Known limitations noted |

## Bonus Features (5 points each, max 25)
| Feature | Points | Requirements |
|---------|---------|--------------|
| Multi-column Sort | 5 | • Shift+click adds sort level<br>• Clear indicators |
| Era Filter | 5 | • Dropdown works<br>• Combines with other filters |
| Doctor Filter | 5 | • Populated from data<br>• Updates with data |
| Export CSV | 5 | • Includes all columns<br>• Proper escaping |
| Decade Groups | 5 | • Correct grouping<br>• Expandable sections |

## Deductions

### Console Errors (-5 points each)
- Uncaught exceptions
- TypeError or similar
- Network errors without handling

### Page Crashes (-10 points each)
- Unhandled exceptions causing crash
- Infinite loops
- Memory leaks

### Code Issues (-15 points each)
- Missing core requirements
- Incomplete implementation
- Non-functional features

## Partial Credit Guidelines

### Implementation Level
- Full points: Works perfectly
- 75%: Works with minor issues
- 50%: Partially implemented
- 25%: Attempted but major issues
- 0%: Not attempted/broken

### Code Quality Impact
- +10%: Exceptional code quality
- -10%: Poor code quality
- -20%: Severely problematic code

### Documentation Impact
- +5%: Excellent documentation
- -5%: Poor/missing documentation
- -10%: Misleading documentation