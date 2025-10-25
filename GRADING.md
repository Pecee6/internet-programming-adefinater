# Grading Guide - Doctor Who Episodes Explorer Exam

## Quick Reference

- **Total Points:** 100
- **Passing Grade:** 60
- **Students:** 70
- **Estimated Grading Time:** 3-4 hours (with automation)

---

## Grading Process

### Step 1: Automated Testing (30 minutes)

1. Run the test harness on all submissions:
   ```bash
   npm run grade-all
   ```

2. This generates `grading-results.json` with automated scores

3. Review flagged submissions (crashes, missing files, etc.)

### Step 2: Spot Checks (2 hours)

Randomly review 15-20 submissions for:
- Advanced features (manual verification)
- Code quality (for borderline cases)
- Edge case handling (visual inspection)

### Step 3: Final Review (1 hour)

- Check plagiarism flags
- Verify automated scores
- Add bonus points for exceptional work
- Deduct for serious issues (non-functional, copied)

---

## Detailed Rubric

### Tier 1: Basic Requirements (60 points)

#### Data Loading (15 points)
- [ ] **10 pts** - Successfully fetches data from API
- [ ] **3 pts** - Shows loading indicator
- [ ] **2 pts** - Handles/displays errors gracefully

**Common Issues:**
- Incorrect API URL
- No error handling (fails silently)
- Loading indicator never disappears

#### Episode Display (20 points)
- [ ] **15 pts** - All required columns displayed correctly
  - Rank, Title, Series, Era, Year, Director, Writer, Doctor, Companion, Cast count
- [ ] **3 pts** - Proper formatting (Doctor/Companion with parentheses)
- [ ] **2 pts** - Table structure is semantic and accessible

**Common Issues:**
- Missing columns
- Displaying raw JSON (e.g., "[object Object]")
- Year not extracted from date
- Companion showing "undefined" or "null"

#### Basic Sorting (15 points)
- [ ] **8 pts** - Clicking headers sorts table
- [ ] **4 pts** - Toggle ascending/descending on re-click
- [ ] **3 pts** - Visual indicator of sort direction

**Common Issues:**
- Sort doesn't actually change order
- No visual feedback
- Only works once (doesn't toggle)
- Era sorting not in correct order

#### Basic Filtering (10 points)
- [ ] **7 pts** - Name filter works (case-insensitive, partial match)
- [ ] **3 pts** - Filter updates display in real-time or on interaction

**Common Issues:**
- Case-sensitive filtering
- Only exact matches work
- Filter doesn't actually filter
- Crashes on empty input

---

### Tier 2: Robust Implementation (25 points)

#### Edge Case Handling (15 points)

**Missing Companions (5 points)**
- [ ] **5 pts** - Displays placeholder text (e.g., "No companion")
- [ ] **0 pts** - Shows "null", "undefined", or crashes

**Empty Cast Arrays (3 points)**
- [ ] **3 pts** - Shows "0" or handles gracefully
- [ ] **0 pts** - Shows undefined, crashes, or renders incorrectly

**Multiple Writers (4 points)**
- [ ] **4 pts** - Displays full writer string correctly
- [ ] **2 pts** - Displays but sorting is broken
- [ ] **0 pts** - Displays incorrectly or crashes

**Special Characters (3 points)**
- [ ] **3 pts** - Handles apostrophes, quotes, slashes without issues
- [ ] **0 pts** - Crashes or displays incorrectly

**Testing These:**
- Check Episode 2 (null companion, empty cast)
- Check Episode 3 (multiple writers)
- Check Episode 4 (apostrophe in title)

#### Multiple Filter Support (5 points)
- [ ] **3 pts** - Era filter dropdown works
- [ ] **2 pts** - Name + Era filters work together (AND logic)

**Common Issues:**
- Filters override each other
- Only one filter works at a time
- OR logic instead of AND logic

#### Enhanced Sorting (5 points)
- [ ] **3 pts** - All columns are sortable
- [ ] **2 pts** - Doctor/Companion sort by actor name (not object)
- [ ] **Bonus 1 pt** - Era sorts in correct order (Classic → Modern → Recent)

**Common Issues:**
- Some columns not sortable
- Sorting by object reference instead of value
- Era sorting alphabetically

---

### Tier 3: Advanced Features (15 points)

Students must complete **at least 2** features. Give 5 points for each **fully working** feature.

#### Option A: Additional Filters (5 points)
- [ ] **3 pts** - Doctor filter dropdown (populated from data)
- [ ] **2 pts** - Companion filter dropdown (populated from data)

**Verification:**
- Check that dropdowns are dynamically generated
- Test filtering by each

#### Option B: Cast Details (5 points)
- [ ] **5 pts** - Interactive cast display (click or hover)
- [ ] **3 pts** - Shows cast but interaction is clunky
- [ ] **0 pts** - Just shows number (no interaction)

**Verification:**
- Click cast count on Episode 1
- Should show "Carey Mulligan (Sally Sparrow)" etc.

#### Option C: Broadcast Decade (5 points)
- [ ] **3 pts** - Decade column added and calculated correctly
- [ ] **2 pts** - Formatted as "1960s", "2000s" etc.
- [ ] **Bonus 1 pt** - Decade is sortable

**Verification:**
- Check formatting
- Test sorting

#### Option D: Plot Preview (5 points)
- [ ] **3 pts** - Shows first 50 chars without cutting words
- [ ] **2 pts** - Truncates with "..."
- [ ] **Bonus 1 pt** - Click to expand

**Verification:**
- Check Episode 1 plot truncation
- Ensure no mid-word cuts

#### Option E: Data Validation (5 points)
- [ ] **3 pts** - Console warnings for data issues
- [ ] **2 pts** - Displays count of warnings

**Verification:**
- Open console
- Should see warnings for Episode 3 (null series)

#### Option F: Performance Optimization (5 points)
- [ ] **3 pts** - Code includes optimization techniques
- [ ] **2 pts** - Comment explains optimization strategy

**Verification:**
- Check for: debouncing, event delegation, memo-ization
- Read comment for understanding

#### Option G: Keyboard Navigation (5 points)
- [ ] **5 pts** - Tab, Enter, Arrow keys work as described
- [ ] **0 pts** - Partially works or doesn't work

**Verification:**
- Tab through filters
- Arrow keys on table headers
- Enter to activate

#### Option H: Custom Feature (5 points)
- [ ] **5 pts** - Creative, useful, well-implemented feature with explanation
- [ ] **3 pts** - Feature works but not exceptional
- [ ] **1 pt** - Feature present but broken or trivial

**Verification:**
- Check comment explaining the feature
- Test the feature

---

## Grade Bands

### 90-100 (Excellent)
- All basic requirements working
- Handles all edge cases gracefully
- At least 2 advanced features fully implemented
- Code is clean and understandable
- UI is polished

### 75-89 (Good)
- All basic requirements working
- Handles most edge cases
- At least 1 advanced feature
- Code works but may have minor issues
- UI is functional

### 60-74 (Passing)
- Basic requirements mostly working
- Some edge case handling
- May have bugs but core functionality works
- UI is basic but functional

### 40-59 (Needs Improvement)
- Basic requirements partially working
- Poor or no edge case handling
- Significant bugs or crashes
- UI has problems

### 0-39 (Failing)
- Core requirements don't work
- Crashes on basic operations
- Minimal effort or non-functional

---

## Common Red Flags

### Automatic Deductions

**Major Issues (-10 to -20 points):**
- Code doesn't run at all
- Missing required files
- Crashes on loading the page
- Completely non-functional sorting or filtering

**Minor Issues (-5 points each):**
- Crashes on specific edge cases
- Missing error handling
- UI is confusing or broken

**Plagiarism (0 points, academic integrity review):**
- Identical code to another student
- Copied from online source without understanding
- LLM-generated code with no modifications

### Bonus Points (+1 to +5)

- Exceptionally clean code
- Creative and useful additional features
- Excellent error handling
- Accessibility considerations
- Performance optimizations with documentation

---

## Automated Test Checklist

The test harness (`test-harness.js`) checks:

1. ✓ Page loads without errors
2. ✓ Data fetching works
3. ✓ Table displays episodes
4. ✓ All required columns present
5. ✓ Sorting changes order
6. ✓ Filter reduces results
7. ✓ Null companion doesn't crash
8. ✓ Empty cast doesn't crash
9. ✓ Multiple writers display
10. ✓ Special characters in titles

---

## Time-Saving Tips

### For Quick Grading:

1. **Use the automated test** - Gets you 70% of the way there
2. **Focus on edge cases** - Most variance is here
3. **Spot check advanced features** - Don't test every feature on every submission
4. **Flag for review** - Mark suspicious submissions, deal with them later
5. **Use grade bands** - Don't agonize over 83 vs 85, use ranges

### Efficiency Tricks:

- Open multiple submissions in tabs
- Use browser dev tools to check console
- Test same interactions on each (e.g., sort by era)
- Keep notes on common issues
- Grade in batches by score range

---

## Handling Common Situations

### "My code works on my machine!"
- Test in the same environment (same browser)
- Check for external dependencies
- Verify API URL is correct

### Partial Credit
- If sorting works but indicator doesn't: 12/15
- If filter works but crashes on empty: 7/10
- Use judgment, favor students when reasonable

### Borderline Cases (59-61 range)
- Check for effort and understanding
- Look at code comments
- Consider partial credit generously
- Lean toward passing if close

### Exceptional Work
- Add bonus points (up to +5)
- Note it for future reference
- Consider mentioning in feedback

---

## Final Checklist

Before submitting final grades:

- [ ] All 70 submissions reviewed
- [ ] Automated scores verified
- [ ] Spot checks completed
- [ ] Plagiarism flags investigated
- [ ] Grade distribution looks reasonable
- [ ] Feedback prepared (if required)
- [ ] Grades entered in system

---

## Questions During Grading?

Common questions and answers:

**Q: Student used a library not mentioned - is that OK?**
A: If it works and shows understanding, yes. Deduct only if it breaks.

**Q: Code is messy but works - should I deduct?**
A: No, unless specified in rubric. Focus on functionality.

**Q: Student did 3 advanced features - extra credit?**
A: Yes, up to +5 bonus points for exceptional work.

**Q: Obvious LLM code but works perfectly?**
A: That's fine. The point is to teach LLM usage. If they handled edge cases, they understood it.

**Q: Grade distribution is too high/low?**
A: Review the rubric. Adjust curve if needed, but be fair and consistent.

---

**Remember:** The goal is to assess understanding and practical skills. Be fair, be consistent, and give credit for effort and learning.
