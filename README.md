# Venn Diagram Builder

A modern, interactive Venn diagram builder built with HTML5 Canvas and vanilla JavaScript.

## Features

### Diagram Types
- **Venn Diagrams** - Show all possible intersections, even if empty (classic representation)
- **Euler Diagrams** - Only show actual relationships that exist (circles separate when sets don't overlap)
- **Easy Toggle** - Switch between diagram types with radio buttons at the top

### Visual Enhancements
- **Text Symbol Operation Buttons** - Clear ∪ ∩ \ △ symbols displayed directly on colored buttons
- **Mathematical Notation** - Sets displayed as `A = {1, 2, 3}` with full element lists in sidebar
- **Color-Coded Sets** - Each set has a unique, vibrant color for easy identification
- **Clean Layout** - Maximized canvas space for optimal diagram viewing

### Interactive Features
- **Hover Tooltips** - Hover over any region to see:
  - Which set(s) the region belongs to (e.g., "A ∩ B" or "A only")
  - Elements in that specific region
  - Visual highlighting of the hovered region
- **Operation Highlighting** - When performing an operation, only the result regions are highlighted:
  - **Union (∪)**: Highlights all regions in either set
  - **Intersection (∩)**: Highlights only the overlapping region
  - **Difference (\)**: Highlights only regions in first set but not second
  - **Symmetric Difference (△)**: Highlights regions in either set but not both

### Set Operations
- **Union** (A ∪ B) - All elements in A or B
- **Intersection** (A ∩ B) - Elements in both A and B
- **Difference** (A \ B) - Elements in A but not in B
- **Symmetric Difference** (A △ B) - Elements in A or B but not both
- **Complement** (A') - All elements in the universal set U that are NOT in A

### Universal Set
- **Automatic Calculation** - U is automatically calculated as the union of all defined sets
- **Visual Rectangle** - Dashed rectangle drawn around all circles representing the universal set
- **Labeled** - Rectangle labeled with "U" in the corner
- **Complement Operations** - Enables complement operations showing elements outside a set

### Diagram Features
- **Multiple Sets** - Supports 2-4 sets simultaneously
- **Element Display** - Shows actual elements in each region of the diagram
- **Automatic Layout** - Circles positioned automatically based on number of sets
- **Region Detection** - Accurately detects all 3, 7, or 15 regions for 2, 3, or 4 sets

## Usage

### Getting Started
Simply open `index.html` in any modern web browser. No installation or build process needed!

```bash
# Open in default browser
xdg-open index.html
# or
firefox index.html
```

### Creating Sets
```
A={1,2,3}
B={3,4,5,6}
C={apple,banana,cherry}
```

### Performing Operations
```
A ∪ B    (union - all elements)
A ∩ B    (intersection - common elements)
A \ B    (difference - in A but not B)
A △ B    (symmetric difference - in A or B but not both)
A'       (complement - all elements NOT in A)
```

### Quick Operations
Click the colorful operation buttons to insert operation templates, then click Execute!

### Viewing Results
- **In the diagram**: Highlighted regions show the operation result
- **In tooltips**: Hover over regions to see elements
- **In the legend**: See all sets with their full element lists
- **In the status bar**: See the operation result in mathematical notation

## Examples

### Example 1: Basic Intersection
1. Start with default sets A={1,2,3,4} and B={3,4,5,6}
2. Click the "∩" button (Intersect)
3. Click "Execute"
4. Result: Only the overlapping region (containing 3,4) is highlighted

### Example 2: Euler Diagram with No Overlap
1. Create sets: `A={1,2,3}` and `B={4,5,6}`
2. Select "Euler Diagram" at the top
3. See circles completely separated (no overlap since sets don't share elements)

### Example 3: Three-Set Union
1. Switch back to "Venn Diagram"
2. Add a third set: `C={4,5,6,7}`
3. Type: `A ∪ B`
4. See all regions belonging to A or B highlighted

### Example 4: Difference
1. Type: `A \ B`
2. Only the left-exclusive region of A (containing 1,2) is highlighted

### Example 5: Complement Operation
1. Create set: `A={1,2,3,4}` and `B={3,4,5,6}`
2. Universal set U is automatically calculated as {1,2,3,4,5,6}
3. Type: `A'` (A complement)
4. Result: Highlights the region outside A but inside the universal set rectangle
5. Shows elements {5,6} which are in U but not in A

## Technical Details

- **Pure JavaScript** - No frameworks or libraries
- **HTML5 Canvas** - High-performance rendering
- **Single File** - Everything in one `index.html` file
- **Responsive** - Adapts to window size
- **Efficient** - Pixel-sampling algorithm for precise region highlighting

## File Structure

```
venn-diagram/
├── index.html          # Complete application (HTML + CSS + JavaScript)
└── README.md           # This file
```

## Browser Compatibility

Works in all modern browsers that support:
- HTML5 Canvas
- ES6 JavaScript (Set, arrow functions, template literals)
- CSS Grid and Flexbox

Tested on:
- Firefox 90+
- Chrome 90+
- Edge 90+

## Contributing

This is a single-file application. To modify:
1. Open `index.html` in your favorite editor
2. Make changes to HTML, CSS (in `<style>` tag), or JavaScript (in `<script>` tag)
3. Refresh browser to see changes

No build process required!

## License

Open source - feel free to use and modify!
