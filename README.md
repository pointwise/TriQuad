# TriQuad
A Glyph script that automatically creates a structured topology given a compatible loop of three connectors.

## Operation
This script allows the user to select a loop of three connectors that define the outer edge of a triangular region to be meshed with structured grids. Geometrically, there are a couple of inherent limitations on the dimensions of each of the edges. First, the triangle inequality requires that none of the three side have a dimension exceeding the sum of the other two. Second, integer "lengths" (dimensions) of each leg require that the sum of all three edges is odd. Otherwise, it is impossible to create a dimensionally balanced set of domains using this approach. The script automatically tests that both of these conditions are met. Also note that there exists a single unique solution for a given set of three edges, and therefore the domains generated are deterministic.

When running the script, there are two methods of selecting the edges of the triangular region: Select the three edges prior to executing the script (works only for versions of Pointwise after 17.2R2), or when prompted to select the connectors after executing the script.

Due to the nature of the domains created (large discontinuity in gridline angle between adjacent domains), the script will always run the three domains through the elliptic solver in order to obtain a smooth mesh.


![ScriptImage](https://raw.github.com/pointwise/TriQuad/master/ScriptImage.png)

## Disclaimer
Scripts are freely provided. They are not supported products of
Pointwise, Inc. Some scripts have been written and contributed by third
parties outside of Pointwise's control.

TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE LAW, POINTWISE DISCLAIMS
ALL WARRANTIES, EITHER EXPRESS OR IMPLIED, INCLUDING, BUT NOT LIMITED
TO, IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR
PURPOSE, WITH REGARD TO THESE SCRIPTS. TO THE MAXIMUM EXTENT PERMITTED
BY APPLICABLE LAW, IN NO EVENT SHALL POINTWISE BE LIABLE TO ANY PARTY
FOR ANY SPECIAL, INCIDENTAL, INDIRECT, OR CONSEQUENTIAL DAMAGES
WHATSOEVER (INCLUDING, WITHOUT LIMITATION, DAMAGES FOR LOSS OF BUSINESS
INFORMATION, OR ANY OTHER PECUNIARY LOSS) ARISING OUT OF THE USE OF OR
INABILITY TO USE THESE SCRIPTS EVEN IF POINTWISE HAS BEEN ADVISED OF THE
POSSIBILITY OF SUCH DAMAGES AND REGARDLESS OF THE FAULT OR NEGLIGENCE OF
POINTWISE.
	 

