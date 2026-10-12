# Standalone comprehension and figure audit

This revision was built by checking the slide deck against the uploaded thesis source and then asking what a viewer could reconstruct **from the presentation alone**.

## Thesis through-line

The starting question is how restrictive bounded average cycle-basis length is in bounded-degree graphs. The two main approaches are to add local cycles and to exploit spanning-tree certificates. Chapter 2 shows that triangle-basis completion by edge addition is APX-hard. Chapter 3 builds high-girth graphs with short-basis linear-size bounded-degree extensions through 2-lifts; low-stretch maps and entropy bounds rule out broad bounded-fiber layering approaches for most regular graphs, and give an exponential upper bound on graphs admitting short WCBs. Chapter 4 turns to random MST probabilities: fundamental cuts encode order constraints, and random removal of prescribed tree edges leads to common rare-interval bounds for the path in K_n and the double spiral in the grid.

## Essential steps, made more visible in the slides

1. **Chapter 2:** no triangle through restored edge uv -> any valid completion must touch u or v; a vertex cover gives vv' edges -> each C_uv becomes two triangles. The reverse map is not just CK: tree components of K in the original layer cause an excess of one vertex, removed safely using structural lemmas. The resulting L-reduction has alpha=beta=1.
2. **Chapter 3:** every lifted edge yields a 4-cycle through two projection edges. G_m itself has large minimum average cycle length because its girth grows; the host H_m has basis average 4+o(1). For WCB counting, new edges are ordered in layers and every layer-i cycle uses a shortest path through previous layers touching layer i-1. The strengthened S-distance entropy bound makes the cost of a layer depend on |S_{i-1}|, so costs sum to O(n).
3. **Chapter 4:** the Lyons--Peres formula expresses MST probabilities through cuts after random deletion of tree edges. In K_n, the only obstruction to a nearly maximal cut is a long surviving path interval. In the grid, the double-spiral pivot lies in every fundamental cycle but one, so the analogous obstruction is a long surviving central component. Count unlikely interval certificates at multiple scales to bound the expectation by exp(O(sqrt(n) log n)).

## Precision checks on the figures

- The Chapter 2 reduction picture for P4 was compared edge-by-edge with the source: f0 has 8 vertices, 9 edges, cycle rank 2, and two distinguished 4-cycles corresponding to the two wheel hubs. Both are fundamental cycles for an appropriate spanning tree.
- The 2-partition diagram replaces every K4 edge with a path of length 3 (two subdivision vertices per edge).
- The 2-lift diagram shows actual cycle covers C3 -> C6 -> C12; the 4-cycle diagram is the general lifted-edge projection square.
- The C8 -> C4 -> P4 folding diagram now names the paired fibers, and the closing quotient edge has distance 3 in P4.
- **All six 16x16 double-spiral panels were checked edge-by-edge** against the monochromatic-edge flip rule in the thesis. Panels A/B start with all 256 ring edges; C/D represent the first and second flips; E has all seven flips; F removes f and adds e*. The final tree has 256 vertices, 255 edges, maximum degree 2, and two endpoints. All 225 non-tree edges except f have a fundamental cycle containing e*.
- Independent construction checks on grids of size 4x4, 8x8, and 16x16 all pass.

## Important scope distinctions

- The main counting theorem concerns **short weakly fundamental** cycle bases, not arbitrary MCBs. The general MCB counting question remains open.
- The obstruction from Chapter 3 rules out the particular bounded-fiber low-stretch **layering scheme** for most regular graphs; it is not a theorem excluding every possible short embedding.
- The bridge from tree stretch to MST probability is conceptual. The thesis does not prove that lower stretch always means higher MST probability.
- The talk gives proof sketches, not all technical case splits or every line of the random-interval calculation. The detailed reverse-map configurations appear in the four-slide appendix; the thesis contains their complete intended proofs.

## Presentation use

The 48-page deck contains 44 main slides followed by four technical Chapter 2 appendix slides. It is compiled with XeLaTeX. `figures/diagrams.tex` and `figures/spiral_frames.tex` contain editable TikZ, not screenshots.
