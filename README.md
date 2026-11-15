KAGE Glyph Editor - Documentation
(for build v. 2026-11-15-a-Ash)
 
This is a customised version of the GlyphWiki kage-editor. It keeps everything the original could do and adds new pens, new head/tail options, guide lines for Latin lettering, and a stroke-width control. Anything marked "(new)" below is an addition.

Quickstart
==========

1. Look to the lower right and press the Freedraw button once. It switches on.
2. In the large edit area on the upper left, click and drag to draw a few lines. They don't need to be precise; they are just objects to work on.
3. Press the Freedraw button again to switch it off.
4. Click on one of your lines.

The selected line is highlighted in red, and 2-4 orange dots appear on it (the number depends on the pen type). Click and drag an orange dot to reshape the line, or drag the line itself to move it.

Controls also appear in the lower left corner:
- The first drop-down menu chooses the pen type.
- The second chooses the head (start) of the line: a serif, corner, or other feature.
- The third chooses the tail (end) of the line in the same way.
- Below those are 2-4 pairs of numbers (again depending on the pen type). These are the X,Y coordinates of the dots, measured from the top left corner of the canvas. You can type a new number in one of these boxes to place a point exactly.

Selecting Lines
===============
 
- Click a line to select it. Click empty space to deselect.
- Hold Control and click to add lines to, or remove them from, the selection. All selected lines are highlighted in red.
- With several lines selected you cannot edit the points of a single line, but you can move or stretch the whole group.
- You can also drag a box around lines to select them.



The Buttons
===========
 
The row of buttons at the bottom of the edit area, from left to right:

Swap Direction: Reverses each selected line, so its head becomes its tail and vice versa. The shape does not change, but head/tail options switch ends.

Turn +90° / Turn -90°: Rotates the whole glyph (all lines) by exactly 90° clockwise or anticlockwise. The canvas turns with it; on a canvas that isn't square, the width and height are swapped. Parts (components taken from other glyphs) cannot be rotated and stay where they are; you will be warned if the glyph contains any.

Options...: This opens the options dialog box. More on this later.

Guides (new): A checkbox that switches the guide lines on and off without opening the Options dialog. See "Guide Lines" below.

Undo: This undoes the last change you made. Control-Z is a keyboard shortcut for this.

Redo: This redoes the last undo. Control-Y is a keyboard shortcut for this.

Select All: Selects all the lines. You can also select and deselect multiple lines by holding down the control key and clicking on lines. All selected lines are highlighted in red. When multiple lines are selected, you can't manipulated the points of one line by itself. You can however, move or stretch all selected lines as a group.

Invert Selection: All currently selected lines are de-selected, and any previously not selected lines are selected.

Copy / Paste / Cut: Copy puts the selected lines in memory, Paste adds them to the glyph, and Cut removes them and puts them in memory. If you paste twice, the second set lands exactly on top of the first, so move it before pasting again. Control-C/V/X are valid keyboard shortcuts for these.

Decompose: Breaks a selected part (a component borrowed from another glyph) into ordinary lines that you can edit one by one.

Freedraw: Switches the mouse-drawing mode on or off. While it is on, click and drag in the edit area to draw lines.

Load SVG: Loads any SVG saved by this editor. It is intended to be backwards-compatible, and can also load SVG images made by the original kage editor on the GlyphWiki website. An SVG that has no stored Width Multiplier is loaded at 100%.

Save SVG: Saves the glyph as an SVG file on your computer. The editing data and the current Width Multiplier are stored inside the file so it can be reopened later.
 
Save B/W PNG: Saves a PNG image with a white background.
 
Save Trans PNG: Saves a PNG image with a transparent background.

Keyboard Shortcuts
==================
 
Control-A         Select all
Control-I         Invert selection
Control-Z         Undo
Control-Y         Redo (Control+Shift+Z also works)
Control-C         Copy
Control-X         Cut
Control-V         Paste
Delete            Delete the selected lines
Esc               Deselect / cancel
Arrow keys        Move the selected lines 1 unit
Shift+Arrow keys  Move the selected lines 5 units

(On a Mac, use Command instead of Control.)


The Right-hand Column
=====================
 
Search box (top): Type or paste a Chinese hanzi or Japanese kanji and the editor searches the GlyphWiki database for matching glyphs. Results appear in the box below. Click one to copy all of its lines into the editor.
 
Preview (bottom right): A small version of the glyph as it will look when saved, without grid lines, guide lines or other helpers. Note that the thick black border of the edit box is a hard limit: anything drawn outside it is not saved or exported.

The Options Dialog: Left Column
===============================
 
Canvas size: Sets the width and height of the drawing area (20-200 each). A smaller canvas is useful for Latin letters, which are narrower than kanji.
 
Grid: Controls the grid lines. Enable turns them on or off. Origin X/Y set where the grid starts, and Spacing X/Y set the distance between lines. The default is a line every 20 units.
 
Font: Mincho or Gothic. This changes how the traditional Japanese pens are drawn: Mincho has thick verticals and thin horizontals (a standard Mincho vertical stroke is 12 units wide); Gothic draws every stroke at one even width (10 units). It primarily affects the six original pen types. For the new pen types, this control only affects the line width (12 vs. 10 units).
 
Center Line: Whether a thin line showing the exact path of a line is drawn. Hide shows none, Show Only Selection shows it only for selected lines, and Always Show shows it for every line.
 
Mask: Places a large shape (Circle, Rounded Square, Square or Diamond) behind the lines and inverts the colour of anything inside it. This can be used to make highlighted glyphs.
 
Language: The language of the interface. You probably want to leave this as English. The features added in this version are not translated, and always appear in English.
 
Close: Closes the dialog.



The Options Dialog: Right Column (new)
======================================
 
Guide Lines
-----------

Horizontal guide lines for drawing Latin (and related) letters. They are drawn over the grid, in a slightly darker grey, and underneath your lines. Each line marks a height measured down from the top of the canvas (the same Y value you see in the coordinate boxes).
 
Show Guide Lines: Master switch for all the guide lines. It is the same control as the Guides checkbox below the main buttons. Your guide settings are remembered by your browser; they are not stored inside saved SVG files.
 
Show Hover Handles: When ticked, a small square is attached to the right-hand end of each guide line. Hover the mouse over a square (even while Freedraw is on) and a label tells you what that line is and its Y value.
 
Preset: A list of common typefaces. Choosing one sets the Y values below to match that typeface's proportions. If you then change any Y value yourself, the menu changes to Custom. Choosing a preset sets the heights only; it does not change which lines are switched on.

The individual lines, each with its own tick box and Y value:
 
   Riser Top      top of tall letters such as b, d, h, k, l
   Caps Top       top of capital letters
   t-Top          top of the letter t (optional, off by default)
   Tittle Line    height of the dot on i and j (optional, off by default)
   X-Line         top of lower-case letters such as x, a, e, o
   Base Line      the line the letters sit on
   Faller Bottom  bottom of letters with tails such as g, j, p, q, y
 
The presets use these values (a 200-unit-high canvas):
 
                    Riser   Caps   t-Top   Tittle   X-Line   Base   Faller
   Cambria            12     18      38      17       56     146     188
   Courier            12     25      23       7       52     146     188
   Garamond           12     21      53      28       65     137     188
   Bodoni             12     12      34      16       62     135     188
   Futura             12     26      40      25       68     148     188
   Times New Roman    12     20      37      18       57     146     188
   Helvetica          12     19      27      12       49     149     188
   Verdana            12     18      22      12       51     150     188
   Uncial             32     12      56      39       71     156     188
 
The values were measured from real fonts, or from close look-alikes where the original was not available (Courier, Garamond, Bodoni, Futura and Uncial), and scaled so the whole letter height fills the canvas. Treat them as a starting point rather than an exact match. In Uncial the capitals are taller than the risers, so Caps Top is the highest line.

Stroke Width
------------

Width Multiplier: A global control, from 10% to 200% (default 100%), that multiplies the width of every line you draw. The edit area, the preview and all saved images follow it. When drawing Latin letters, about 70% is suggested; at 100% the strokes look very bold, because the standard stroke is designed for the dense strokes of kanji. At 70% a standard Mincho vertical stroke is 8.4 units wide instead of 12.
 
The multiplier is saved inside each SVG file you save. SVG files that don't contain one, including every file from the original editor, open at 100%. Opening a file sets the multiplier to that file's value.




The Pen, Head and Tail Types
============================
 
The Pen menu is divided into four groups.
 
Original pens
-------------

Straight Line, Curve, Bend Line, Bend Curve, Cmplx. Curve and Vert. Slash. These six were in the original editor and are designed for drawing kanji in Mincho or Gothic style. Their head and tail options are unchanged from the original.
 
With the Straight Line in Mincho style, a mostly horizontal line is drawn thin and ends with a triangular scale at the tail. A mostly upright line is drawn thick and ends with a small triangular wedge at the tail.
 
With the Vert. Slash, the intended use is to draw it from top to bottom. For best results the first three points should be in a perfectly straight line, and the fourth point can be moved freely.
 
Rune pens (new)
---------------

Rune Line: A straight line of standard width (12 units at 100%), the same thickness along its whole length whichever way it points. Two points.

Rune Bend: Three points; the middle point is where the line turns. The two arms meet in a clean mitred corner, which stays sharp down to 30° between the arms and is flattened (bevelled) below that.
 
Head and tail options for both:

* Free: plain flat end
* Diamond: a diamond-shaped end; Left, Middle or Right sets which side the point falls on.
* Wedge, Sharp (Left/Right): a long 45° triangular end
* Wedge (Left/Middle/Right): a shorter triangular end, the same length as the Mincho tail on a vertical Straight Line
* Connect (H) / (V): see "Connect" below
 
Brush pens (new)
----------------

Brush Curve (three points) and Brush Cmplx. (four points). A round-tipped brush that gets thicker where the curve turns more tightly (up to 250% of the standard width), which gives a natural brush feel.
 
Head options:

* Round (100%, 130%, 160%, 200%): a round end that is that percentage of the line's width
* Round Taper (75%, 50%, 25%): the line narrows towards the starting end, to that percentage of its width.

Tail options:

* Round (100%): A simple rounded end.
* Round Taper (75%, 50%, 25%): A taper spreads over the last half of the line's length.
 
Nib pens (new)
--------------

Nib Line (two points), Nib Curve (three points) and Nib Cmplx. (four points). These imitate a broad-edged pen, so the thickness depends on the direction of travel: strokes running top-left to bottom-right are 150% wide, horizontal and vertical strokes are 100%, and strokes running top-right to bottom-left are 50%.
 
Head and tail options:

* Free: The line ends in a simple straigt edge.
* Level Serif (0°), Slant Serif (45°), Upright Serif (90°), Reverse Serif (135°): a small serif cut at the given angle
* Wedge (Left), Wedge (Right): short triangular ends
* Connect (H) / (V): see "Connect" below
 
Connect (H) and Connect (V) (new)
---------------------------------

These cut the end of a line flat so that two lines meeting at a point join cleanly, without a spike or a gap. Use Connect (H) for lines that run roughly horizontally and Connect (V) for lines that run roughly vertically. Each only works within a limited angle (for example, Connect (V) needs a line within 60° of vertical). If the line is outside the limit, the end is drawn as Free and an error message appears at the bottom left of the edit area.
 
Joining two nib or rune lines
-----------------------------

If two lines meet at the same angle, their thicknesses match where they meet, whichever ends are joined. If they meet at different angles the nib pens will differ in thickness there, because a nib's width follows its direction.
 
 
Tips
====
 
- Save often. Use Save SVG to keep your work; the glyph is not stored on the server.
- For a Latin letter: set the Canvas size to what you need, tick Guides, choose a Preset, set the Width Multiplier to about 70%, and draw with the Nib or Rune pens.
- Parts that are borrowed from other glyphs can't be rotated or edited as lines until you press Decompose.
 
 
