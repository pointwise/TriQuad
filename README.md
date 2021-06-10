# TriQuad
Copyright 2021 Cadence Design Systems, Inc. All rights reserved worldwide.

A Glyph script that automatically creates a structured topology given a compatible loop of three connectors.

## Operation
This script allows the user to select a loop of three connectors that define the outer edge of a triangular region to be meshed with structured grids. Geometrically, there are a couple of inherent limitations on the dimensions of each of the edges. First, the triangle inequality requires that none of the three side have a dimension exceeding the sum of the other two. Second, integer "lengths" (dimensions) of each leg require that the sum of all three edges is odd. Otherwise, it is impossible to create a dimensionally balanced set of domains using this approach. The script automatically tests that both of these conditions are met. Also note that there exists a single unique solution for a given set of three edges, and therefore the domains generated are deterministic.

When running the script, there are two methods of selecting the edges of the triangular region: Select the three edges prior to executing the script (works only for versions of Pointwise after 17.2R2), or when prompted to select the connectors after executing the script.

Due to the nature of the domains created (large discontinuity in gridline angle between adjacent domains), the script will always run the three domains through the elliptic solver in order to obtain a smooth mesh.


![ScriptImage](https://raw.github.com/pointwise/TriQuad/master/ScriptImage.png)

## Disclaimer
This file is licensed under the Cadence Public License Version 1.0 (the "License"), a copy of which is found in the LICENSE file, and is distributed "AS IS." 
TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE LAW, CADENCE DISCLAIMS ALL WARRANTIES AND IN NO EVENT SHALL BE LIABLE TO ANY PARTY FOR ANY DAMAGES ARISING OUT OF OR RELATING TO USE OF THIS FILE. 
Please see the License for the full text of applicable terms.
