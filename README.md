# cell2md
Save a cell array to file as a nicely formatted markdown table. 
  
```
USAGE: cell2md(X, varargin)
```
---

## INPUT

**X**: cell array to write (can be numeric or char array, in which case it will be converted to a cell array)

## VARARGIN (Name, Value Pairs)
- **outfile**: name for output file (default: cell2md_YYYY_MM_dd) 
- **hdrnames**: name for column headers (default: first row of X) 
- **alignment**: horz alignment for columns (can be 1x1 char to use same alignment for all columns, or 1 x size(X,2) cell array to use column-specific alignments)

---
## EXAMPLE USAGE 

Save with default filename and alignment with column headers A, B, C
```
X = num2cell(rand(10, 3)); 
cell2md(X, 'hdr', {'A' 'B' 'C'});
```
