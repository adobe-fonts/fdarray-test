# FDArray Test

*FDArray Test* are two special-purpose CID-keyed OpenType/CFF fonts that are based on the Adobe-Identity-0 ROS (*ROS* stands for /Registry, /Ordering, and /Supplement, and refers to the /CIDSystemInfo dictionary entries that define the glyph set name for CID-based character collections). The Adobe-Identity-0 ROS is a special-purpose character collection whose use is not tied to a specific language, and FDArray Test are *special-purpose* OpenType fonts that are intended to render all Unicode code points using spacing (full-width or 1000-em) and marking glyphs that indicate the FDArray element to which it belongs (via a two-digit hexadecimal value), thus the reason why the Adobe-Identity-0 ROS was chosen as the basis for this OpenType font.

The *FDArray Test 257* font includes 257 glyphs, hence its name, but includes only 256 functional glyphs, one for each of its 256 FDArray elements (the architectural limit). GID+1 is assigned to the first FDArray element (with index 0), and GID+256 is assigned to the last FDArray element (with index 255). In other words, a single glyph is assigned to each of the 256 possible FDArray elements, except for the first FDArray element to which GID+0 (*.notdef*) is also assigned.

The *FDArray Test 65535* font includes 65,535 glyphs (the architectural limit), hence its name, but includes only 65,534 functional glyphs, 256 (254 for *xxxxFFxx*) for each of its 256 FDArray elements (the architectural limit). GIDs 1 through 256 (256 glyphs) are assigned to the first FDArray element (with index 0), and GIDs 65281 through 65534 (254 glyphs) are assigned to the last FDArray element (with index 255). In other words, up to 256 glyphs are assigned to each of the 256 possible FDArray elements, except for the first FDArray element to which GID+0 (*.notdef*) is also assigned, and last FDArray element to which only 254 glyphs are assigned..

Both fonts map 1,111,998 Unicode code points to their glyphs in blocks of up to 256 (*FDArray Test 257*) or 65,534 (*FDArray Test 65535*) glyphs. The 2,048 High and Low Surrogates (U+D800 through U+DFFF), the two noncharacters in the BMP and in each of the 16 Supplementary Planes (FFFE and FFFF), and the 32 noncharacters in the range U+FDD0 through U+FDEF are explicitly and intentionally excluded. The *FDArray Test 257* font maps glyphs in such a way that the seventh and eighth UTF-32 hexadecimal digits (aka the *least significant byte*) correspond to the FDArray element, but the *FDArray Test 65535* font maps glyphs in such a way that the fifth and sixth UTF-32 hexadecimal digits (aka the *second least significant byte*) correspond to the FDArray element.

As fully-functional OpenType fonts, the following 11 'sfnt' tables are included: BASE, CFF, DSIG, OS/2, cmap, head, hhea, hmtx, maxp, name, and post.

## Font installation instructions

* [macOS](https://support.apple.com/en-us/HT201749)
* [Windows](https://www.microsoft.com/en-us/Typography/TrueTypeInstall.aspx)
* [Linux/Unix-based systems](https://github.com/adobe-fonts/source-code-pro/issues/17#issuecomment-8967116)

## Building the font from source

### Requirements

To build the binary font file from source, you need to have installed the [Adobe Font Development Kit for OpenType](http://www.adobe.com/devnet/opentype/afdko.html) (AFDKO). The AFDKO tools are widely used for font development today, and are part of most font editor applications.

### Building the font

In this repository, all necessary files are in place for building the OpenType/CFF font, and the COMMANDS.txt file provides the command lines that are used.

## Getting Involved

For any suggestions for changes, please [create a new issue](https://github.com/adobe-fonts/fdarray-test/issues) for consideration.

