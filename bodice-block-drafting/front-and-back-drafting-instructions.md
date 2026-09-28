# Front and back bodice block: timestamped drawing instructions

Source: [local automatic-caption transcript](../01-drafting-the-basic-pattern-set-from-scratch-basic-bodice-block-flat-patterning-ZYJXKh1_dSI.md), *Drafting the Basic Pattern Set from Scratch // Basic Bodice Block Flat Patterning*. Video: <https://www.youtube.com/watch?v=ZYJXKh1_dSI>.

Scope: approximately **12:54–35:18 front**, **35:18–52:31 back**. Later dart splitting, full-bust adjustment, seam allowances, and fitting are excluded. This is a reconstruction from the supplied captions, **not a visual verification of the video**. Timestamps identify the start of the relevant spoken instruction or calculation; the actual pencil stroke may occur later. Multiple strokes described together share a timestamp. Incorrect attempts are recorded in notes rather than prescribed as finished geometry.

## How to read and use the instructions

- Each numbered table row instructs drawing **one straight segment or one Bezier segment with two endpoints**. Point definitions and calculations are preparation, not additional drawing instructions.
- Each piece has its own SVG coordinate system: origin at the top-left, positive x rightward, positive y downward. **One SVG user unit = one inch**; for example, render a 12-by-21-unit drawing with `viewBox="0 0 12 21"`, `width="12in"`, and `height="21in"`. No seam allowance is included.
- Front center front is at x = 0 and the piece extends right. Back center back is at x = 11 and the piece extends left, reflecting the opposite orientation described at 35:29–35:56. For other measurements, replace 11 with the calculated back width throughout.
- Calculate the length in a row **before** drawing its segment. Coordinates are derived from measurements plus separately stated additions; displayed decimals are rounded and must not be used instead of the exact formulas.
- `dist(U,V) = sqrt((Vx−Ux)^2 + (Vy−Uy)^2)`; `unit(U,V) = (V−U)/dist(U,V)`. Vector multiplication and addition operate on both coordinates.
- **STATED** = clearly spoken; **DERIVED** = arithmetic/geometric consequence; **ASSUMED** = a provisional reconstruction; **UNRESOLVED** = missing or contradictory information requiring a check.
- The video includes fixed drafting guides, dart intake, and contour corrections. These are **not body measurements or ease**. It would be inaccurate to invent body-based formulas for them. Such exceptions are identified explicitly. Their body-measurement basis is **UNRESOLVED / not supplied**. Likewise, exact curve lengths cannot be obtained from body measurements alone; the curve models below add stated assumptions.

## Measurement and allowance ledger

All quantities are inches. These are the video's standardized size-18 chart values, not the speaker's personal measurements. Do not substitute bust circumference / 4 for a named arc or width measurement: the captions do not establish that equivalence. Measurement-taking landmarks are also not fully supplied.

| Piece / quantity | Body/chart measurement first | Addition or correction afterward | Draft value and evidence |
|---|---:|---:|---|
| Front full length | 19 1/8 | +1/8 allowance; purpose not specified | 19 1/4, 13:48–14:13 |
| Front across shoulder | 8 9/16 | −1/8 drafting correction, **not ease** | 8 7/16, 15:41–15:59 |
| Front center length | 15 5/8 | 0 | 15 5/8, 16:30–16:48 |
| Front bust arc | 11 5/8 | +1/4 allowance | 11 7/8, 17:14–17:25 |
| Front shoulder slope | **19 1/2 DERIVED** by subtracting the stated addition | +1/8 allowance | 19 5/8, 18:24–18:31 |
| Front bust depth | 10 1/4 | 0 | 10 1/4, 20:05–20:10 |
| Front shoulder length | 5 3/16 | 0 | 5 3/16, 20:24–20:27 |
| Front bust span | **3 11/16 DERIVED** if the caption's +1 1/4 is correct | +1 1/4, **purpose and transcription UNRESOLVED** | 4 15/16, 20:46–21:24; do not silently reinterpret the addition as +1/4 |
| Front across chest | **7 9/16 DERIVED** | +1/4 allowance | 7 13/16, 22:23–22:28 |
| Front dart placement | 4 1/16 initially | 0 | Later measured as 4 1/8 at 27:55; **conflict** |
| Front “new strap” | **19 11/16 DERIVED** | +1/8 allowance | 19 13/16, 23:49–24:00; exact measurement name/landmarks unclear |
| Front side length | 8 7/8 | 0 | 25:14–25:24; later approximate 9 is not adopted |
| Front waist arc | 8 5/8 | +1/4 explicitly called ease | 8 7/8 before subtracting B–F, 27:39–28:12 |
| Back full length | 19 | 0 | 36:06–36:18 |
| Back across shoulder | 8 13/16 | 0 | 36:30–36:38; position corrected at 40:34–40:46 |
| Back center length | 17 3/4 | 0 | 36:51–37:07 |
| Back arc | **10 1/4 DERIVED** | +3/4 allowance | 11, 37:29–37:43 |
| Back neck | **3 1/2 DERIVED** | +1/8 allowance | 3 5/8, 38:13–38:37 |
| Back shoulder slope | 18 1/2 | +1/8 allowance | 18 5/8, 38:48–38:58 |
| Back shoulder length | **UNRESOLVED** | +1/2 shoulder-dart provision | Repeated final total 6 1/16; implies body length 5 9/16. Captions also say 5 15/16 and 5 1/16; neither +1/2 yields 6 1/16 |
| Back dart placement | 4 1/16 | 0 | 43:34–43:46 |
| Back waist arc | 8 1/4 | +1 3/4 stated dart provision, **not ease** | 10, 43:50–44:12 |
| Back waist dart width | Not a body measurement | Fixed intake: **1 1/2 or 1 3/4, UNRESOLVED** | 44:18–44:29 says 1 1/2, conflicting with the preceding provision |
| Back side length | 8 7/8 | 0 | 45:10–45:29 |
| Back across back | **7 9/16 DERIVED** | +1/4 allowance | 7 13/16, 49:56–50:14 |

“Allowance” above does not establish whether the original author intended wearing ease, balance compensation, or another drafting adjustment. Only front waist +1/4 is explicitly identified as ease in these captions. No further ease is added here.

## Bezier convention and length calculation

For endpoints U and V and controls C1 and C2, a cubic segment is:

`b(t) = (1−t)^3 U + 3(1−t)^2 t C1 + 3(1−t)t^2 C2 + t^3 V`, for `0 ≤ t ≤ 1`.

Its required model length is calculated **before drawing** as:

`BezLen(U,C1,C2,V) = integral[0..1] |3(1−t)^2(C1−U) + 6(1−t)t(C2−C1) + 3t^2(V−C2)| dt`.

Evaluate numerically after resolving the inputs, for example by adaptive quadrature. This is a length calculation, not a claim that the captions state a curve length. SVG syntax is `M Ux Uy C C1x C1y C2x C2y Vx Vy`; a straight segment is `M Ux Uy L Vx Vy`. Controls determine shape and are **not additional connected endpoints**.

Two provisional models are used:

- **Gentle waist curve W(U,V):** C1 = `(Ux+(Vx−Ux)/3, Uy)`; C2 = `(Ux+2(Vx−Ux)/3, Vy)`. This gives horizontal endpoint tangents and a small smooth change in height, consistent with “slightly curved.” It is an assumption, not a recovered French-curve tracing. Check seam/dart truing later.
- **Neckline quarter-ellipse model:** `k = 4(sqrt(2)−1)/3 ≈ 0.55228475`. Explicit controls below give a vertical tangent at the shoulder-neck endpoint and a horizontal tangent at center front/back. This is a reasonable provisional smooth neckline, but the caption's diagonal offsets cannot be verified and are not claimed to be satisfied.

For armholes, the captions do not determine reliable tangents or curvature, and the speaker explicitly misses a guide point on the back. These are **straight-line substitutes**, not invented fitted curves. Their lengths are only placeholder chord lengths; final armhole arc lengths remain **UNRESOLVED**.

## Front: coordinate construction

These definitions use a consistent provisional reconstruction. In particular, I is assumed to lie on the top horizontal through A; the captions do not explicitly state that constraint. If this assumption fails on video review, I, N, and all dependent coordinates must change.

| Point / variable | Exact coordinate or definition | Approximate coordinate / status |
|---|---|---|
| A | `(0,0)` | top construction origin |
| B | `(0,19.25)` | full-length lower origin |
| C | `(8.4375,0)` | across-shoulder reference |
| D | `(0,19.25−15.625)` | `(0,3.625)`, center-front neck |
| E | `(11.875,19.25)` | bust-arc lower reference |
| G | `(8.4375,19.25−sqrt(19.625²−8.4375²))` | `(8.4375,1.531388)`, upper intersection on C vertical |
| I | `(Gx−sqrt(5.1875²−Gy²),0)` | `(3.481190,0)`, **ASSUMED top-line intersection** |
| H | `G + (10.25/19.625)(B−G)` | `(4.030653,10.785695)`, bust-depth reference |
| J | `(0,Hy)` | `(0,10.785695)` |
| K | `(4.9375,Hy)` | `(4.9375,10.785695)`, bust/dart apex |
| L | `(0,(Dy+Jy)/2)` | `(0,7.205347)` |
| M | `(7.8125,Ly)` | `(7.8125,7.205347)` |
| F0 | `(4.0625,19.25)` | initial dart-placement mark |
| F | `(4.0625,19.4375)` | **ASSUMED** lowered waist/dart endpoint, using the 3/16 drop |
| N | `(11.875,sqrt(19.8125²−(11.875−Ix)²))` | `(11.875,17.946563)`, lower strap intersection |
| O | `(Nx,Ny−8.875)` | `(11.875,9.071563)`, underarm |
| P0 | `(Nx−1.25,Ny)` | `(10.625,17.946563)`, **ASSUMED inward offset direction** |
| P | `O + 8.875 unit(O,P0)` | `(10.637217,17.859823)`, corrected side-waist endpoint |
| w | `(8.625+0.25)−4.0625` | `4.8125`, remaining front waist length |
| Q | `P + w unit(P,F)` | dart-base construction point on P–F |
| R | `K + dist(K,F) unit(K,Q)` | equal-length second preliminary dart endpoint |
| Z | `(F+R)/2` | midpoint of dart base; no line implied |
| T | `K + 0.625 unit(K,Z)` | **ASSUMED** dart tip centered toward base, 5/8 from apex |
| V | `(Ix,Dy)` | `(3.481190,3.625)`, neckline construction corner |
| uM, dM | nonnegative unknown guide extents | **UNRESOLVED**, vertical guide above/below M |
| o | unknown positive inward guide extent | **UNRESOLVED**, horizontal underarm guide length |

The initial shoulder-slope and shoulder-length circles select the upper/inward solution. Likewise, the strap construction selects the lower intersection. These are geometric inferences, not extra spoken measurements.

**Front reconciliation choices:** the 4 1/16 dart placement is retained rather than the later 4 1/8 ruler reading. The latter would give `w = 4.75`, the speaker's result at 28:27; the retained value gives `w = 4.8125`. F is interpreted as the lowered point after the 3/16 instruction, while the waist subtraction uses the original horizontal B–F0 body placement, not the slightly longer sloping B–F distance. These label conventions need visual confirmation. The direction O→P0 is shortened to the exact side length to obtain P, following 26:04–26:07; a literal uncorrected P0 would make that side too long.

The calculated D–J distance is `7.160695`, whereas the speaker measures `7.125` at 21:41. Half of the measured value is `3.5625`; half of the analytic value is `3.580347`. The table uses the analytic geometry and preserves this discrepancy for review.

### Front drawing instructions

Rows may reuse a preliminary guideline as a final edge. Temporary and superseded lines should be distinguishable from the final contour.

| Step | Start time | Calculate length first (inches) | Single drawing instruction, including two endpoint coordinates |
|---|---|---|---|
| F01 | 13:06 (dimension begins 13:48) | `19.125 + 0.125 = 19.25` | Draw the vertical A–B construction line from **(0,0)** to **(0,19.25)**. |
| F02 | 13:29 (dimension begins 15:41) | `8.5625 − 0.125 = 8.4375` | Draw the horizontal A–C line from **(0,0)** to **(8.4375,0)**. |
| F03 | 14:29 (dimension begins 17:14) | `11.625 + 0.25 = 11.875` | Draw the horizontal B–E line from **(0,19.25)** to **(11.875,19.25)**. |
| F04 | 16:08 | `3`, fixed construction guide; no body formula supplied | Draw the C vertical guide from **(8.4375,0)** to **(8.4375,3)**. |
| F05 | 16:30 | `15.625 + 0 = 15.625` | Draw/retrace B–D upward on the center-front reference from **(0,19.25)** to **(0,3.625)**. |
| F06 | 17:01 | `4`, fixed construction guide; no body formula supplied | Draw the D horizontal guide from **(0,3.625)** to **(4,3.625)**. |
| F07 | 17:44 | `11`, fixed construction guide; no body formula supplied | Draw the E vertical guide from **(11.875,19.25)** to **(11.875,8.25)**. |
| F08 | 18:20 | `19.5 + 0.125 = 19.625` | Draw the shoulder-slope diagonal B–G from **(0,19.25)** to **(8.4375,1.531388)**. |
| F09 | 20:05 | `10.25 + 0 = 10.25` | Draw/retrace the bust-depth segment G–H from **(8.4375,1.531388)** to **(4.030653,10.785695)**. |
| F10 | 20:24 | `5.1875 + 0 = 5.1875` | Draw the shoulder G–I from **(8.4375,1.531388)** to **(3.481190,0)**; I is **ASSUMED** as above. |
| F11 | 20:46 | `3.6875 + 1.25 = 4.9375`, addition **UNRESOLVED** | Draw the horizontal bust guide J–K from **(0,10.785695)** to **(4.9375,10.785695)**, passing H. |
| F12 | 21:41 | `(15.625 − (19.25−Hy))/2 = (Jy−Dy)/2 ≈ 3.580347` | Draw/retrace D–L from **(0,3.625)** to **(0,7.205347)**; spoken ruler result differs. |
| F13 | 22:19 | `7.5625 + 0.25 = 7.8125` | Draw the across-chest line L–M from **(0,7.205347)** to **(7.8125,7.205347)**. |
| F14 | 22:49 | `uM+dM`, **UNRESOLVED** construction length | Draw the vertical M guide from **(7.8125,7.205347−uM)** to **(7.8125,7.205347+dM)**. |
| F15 | 23:05 | `4.0625 + 0 = 4.0625` | Draw/retrace the waist-placement line B–F0 from **(0,19.25)** to **(4.0625,19.25)**. |
| F16 | 23:32 | `0.1875`, fixed contour correction, not ease | Draw the F0–F drop from **(4.0625,19.25)** to **(4.0625,19.4375)**; relabeling the lower point F is **ASSUMED**. |
| F17 | 23:49 | `19.6875 + 0.125 = 19.8125` | Draw the strap diagonal I–N from **(3.481190,0)** to **(11.875,17.946563)**. |
| F18 | 25:14 | `8.875 + 0 = 8.875` | Draw/retrace the side-length reference N–O from **(11.875,17.946563)** to **(11.875,9.071563)**. |
| F19 | 25:32 | `1.25`, fixed waist-shaping offset, not ease | Draw the inward offset N–P0 from **(11.875,17.946563)** to **(10.625,17.946563)**; inward direction is **ASSUMED**. |
| F20 | 25:57 (resumed 26:28) | `8.875 + 0 = 8.875` | Draw the corrected side seam O–P from **(11.875,9.071563)** to **(10.637217,17.859823)**. |
| F21 | 26:15 (corrects misread P–E) | `dist(P,F) = sqrt((Px−4.0625)²+(Py−19.4375)²)` | Draw the preliminary waist guide P–F from **(Px,Py)** to **(4.0625,19.4375)**. |
| F22 | 26:54 | `o`, **UNRESOLVED** guide length; no body formula supplied | Draw the underarm horizontal guide from O **(11.875,9.071563)** to **(11.875−o,9.071563)**. |
| F23 | 27:27 | `(8.625 + 0.25) − 4.0625 = 4.8125`; spoken alternative `4.75` | Draw/retrace the retained outer-waist segment P–Q from **(Px,Py)** to **(Px+w(Fx−Px)/dist(P,F), Py+w(Fy−Py)/dist(P,F))**. |
| F24 | 29:23 | `dist(K,F) = sqrt((4.0625−4.9375)²+(19.4375−Hy)²)` | Draw the first preliminary dart leg K–F from **(4.9375,Hy)** to **(4.0625,19.4375)**. |
| F25 | 29:38 | `dist(K,Q)`, with Q determined by the body-based waist remainder above | Draw the second preliminary dart leg K–Q from **(4.9375,Hy)** to **(Qx,Qy)**. |
| F26 | 29:46 | `0.625`, fixed apex setback, not ease | Draw the dart-tip construction segment K–T from **(4.9375,Hy)** to **(4.9375+0.625(Zx−Kx)/dist(K,Z), Hy+0.625(Zy−Ky)/dist(K,Z))**. |
| F27 | 30:09 | `dist(T,F)` using the 5/8 setback | Draw the first shortened final dart leg T–F from **(Tx,Ty)** to **(4.0625,19.4375)**. |
| F28 | 30:14 | `dist(K,F)`; spoken approximate `8.5` is not imposed on the reconstructed geometry | Draw the equalized preliminary second dart leg K–R from **(4.9375,Hy)** to **(Kx+dist(K,F)(Qx−Kx)/dist(K,Q), Ky+dist(K,F)(Qy−Ky)/dist(K,Q))**. |
| F29 | 30:09 (endpoint R established by 30:51) | `dist(T,R)` | Draw the second shortened final dart leg T–R from **(Tx,Ty)** to **(Rx,Ry)**. |
| F30 | 30:57 | `BezLen(B,(Fx/3,By),(2Fx/3,Fy),F)` | Draw the provisional waist Bezier B–F from **(0,19.25)** to **(4.0625,19.4375)** with controls **(1.354167,19.25)** and **(2.708333,19.4375)**. |
| F31 | 31:10 | `BezLen(R,(Rx+(Px−Rx)/3,Ry),(Rx+2(Px−Rx)/3,Py),P)` | Draw the provisional outer-waist Bezier R–P from **(Rx,Ry)** to **(Px,Py)** with controls **(Rx+(Px−Rx)/3,Ry)** and **(Rx+2(Px−Rx)/3,Py)**. |
| F32 | 31:21 (routing clarified 31:46–32:24) | `dist(G,M) = sqrt((7.8125−8.4375)²+(Ly−Gy)²)`; actual arc length **UNRESOLVED** | Draw the **straight substitute for the upper armhole curve** from G **(8.4375,1.531388)** to M **(7.8125,7.205347)**. |
| F33 | 31:21 (routing clarified 32:20) | `dist(M,O) = sqrt((11.875−7.8125)²+(Oy−Ly)²)`; actual arc length **UNRESOLVED** | Draw the **straight substitute for the lower armhole curve** from M **(7.8125,7.205347)** to O **(11.875,9.071563)**; using O itself as the final endpoint is **ASSUMED** from the squared O guide. |
| F34 | 32:46 | `Dy−Iy = 3.625`, derived from front full and center lengths | Draw the neck-corner guide I–V from **(3.481190,0)** to **(3.481190,3.625)**. |
| F35 | 33:05 | `BezLen(I,(Ix,k*Dy),(k*Ix,Dy),D)` | Draw the provisional neckline Bezier I–D from **(3.481190,0)** to **(0,3.625)** with controls **(3.481190,k*3.625)** and **(k*3.481190,3.625)**. |

F11 has two endpoints; H is only a point lying on its straight segment. F12, F15, and F26 turn narrated point placement into explicit finite construction segments to make the reconstruction auditable; they are not claims that the speaker separately inks each of those segments.

**Dart equalization ambiguity:** 30:09 says redraw from the shortened tip, but 30:19–30:24 refers to equality measured from K. F28 follows the latter and F29 reconnects the shortened tip. If video review instead establishes equalization from T, replace R with `T + dist(T,F) unit(T,Q)` and recalculate F29–F31. Do not assume both interpretations give the same dart.

**Front neckline missing guide:** 32:30 describes a curve passing an “angle line” by 1/8; 33:05 briefly says 1/4 before correcting to 1/8. Neither the angle-line endpoint nor its construction length is recoverable from the captions. No fictitious angle segment has been inserted. F35's control points do **not** certify this offset.

## Back: coordinate construction

The corrected across-shoulder location is used from the outset. The mistaken initial mark and the tentative 45-degree interpretation at 39:14 are not retained.

| Point / variable | Exact coordinate or definition | Approximate coordinate / status |
|---|---|---|
| A | `(11,0)` | top of center-back construction reference |
| B | `(11,19)` | lower center back |
| C | `(11−8.8125,0)` | `(2.1875,0)`, corrected reference |
| D | `(11,19−17.75)` | `(11,1.25)`, center-back neck |
| E | `(11−(10.25+0.75),19)` | `(0,19)` |
| F | `(11−(3.5+0.125),0)` | `(7.375,0)`, shoulder-neck point |
| G | `(2.1875,19−sqrt(18.625²−8.8125²))` | `(2.1875,2.591756)` |
| s | adopted shoulder total | `6.0625`, **PROVISIONAL**; underlying body measurement conflicts |
| H | `F + s unit(F,G)` | `(1.951702,2.709565)` |
| V | `(Fx,Dy)` | `(7.375,1.25)`, neckline construction corner |
| I | `(11−4.0625,19)` | `(6.9375,19)`, inner waist-dart base |
| J | `(11−(8.25+1.75),19)` | `(1,19)`, outer waist reference |
| M | `(Jx,Jy+0.1875)` | `(1,19.1875)`, lowered side-waist point |
| N | `(0,My−sqrt(8.875²−(Mx−0)²))` | `(0,10.369018)`, **ASSUMED** intersection with E vertical |
| d | actual waist dart intake | **UNRESOLVED**: 1.5 spoken, 1.75 used in B–J provision |
| K | `(Ix−d,19)` | `(6.9375−d,19)` |
| L | `((Ix+Kx)/2,19)` | `(6.9375−d/2,19)` |
| O | `(Lx,19−(8.875−1))` | `(6.9375−d/2,11.125)` |
| I1 | `O + (dist(O,I)+0.125) unit(O,I)` | extended inner dart base, **ASSUMED ray extension** |
| K1 | `O + (dist(O,K)+0.125) unit(O,K)` | extended outer dart base, **ASSUMED ray extension** |
| P | `(F+H)/2` | shoulder midpoint, using exact `s/2 = 3.03125` |
| Q | `P + 3 unit(P,O)` | shoulder dart tip |
| R0 | `P + 0.25 unit(P,F)` | **ASSUMED** neck-side shoulder-dart mark |
| U0 | `P + 0.25 unit(P,H)` | **ASSUMED** armhole-side shoulder-dart mark |
| e | shoulder-dart extension past R0 | **UNRESOLVED**: 1/8 at 48:12 versus apparent 1/2 at 48:24 |
| R | `Q + (dist(Q,R0)+e) unit(Q,R0)` | final neck-side shoulder-dart endpoint |
| U | `Q + dist(Q,R) unit(Q,U0)` | equalized outer shoulder-dart endpoint |
| S | `(11,Dy+17.75/4)` | `(11,5.6875)`, **ASSUMED measured downward from D** |
| T | `(11−(7.5625+0.25),Sy)` | `(3.1875,5.6875)` |
| hE | unknown E-guide height | **UNRESOLVED**, must at least reach N |
| uT, dT | unknown vertical guide extents at T | **UNRESOLVED** |
| theta | angle of neckline corner guide | **UNRESOLVED**; 45 degrees is plausible but not stated |
| W | `(7.375+0.375*cos(theta),1.25−0.375*sin(theta))` | **ASSUMED inward/upward quadrant** for neck guide |

At 46:42 the captions say “past L and K,” but L was explicitly the dart center. The working interpretation is **past I and K**, giving two symmetric waist-dart legs. This must be checked visually. “Past” is modeled as a 1/8 extension along each dart ray, not as a vertical 1/8 drop; a vertical-drop interpretation gives slightly different coordinates.

With J fixed at its stated 10-inch location, `d = 1.5` leaves a horizontal waist remainder of `10−1.5 = 8.5`, whereas `d = 1.75` leaves `8.25`, equal to the stated waist arc. The unexplained 1/4 difference must not be silently called ease. This is only a horizontal diagnostic, not a calculation of the curved finished waist seam.

### Back drawing instructions

| Step | Start time | Calculate length first (inches) | Single drawing instruction, including two endpoint coordinates |
|---|---|---|---|
| B01 | 35:22 (dimension begins 36:06) | `19 + 0 = 19` | Draw the A–B center reference from **(11,0)** to **(11,19)**. |
| B02 | 36:30; correction 40:34 | `8.8125 + 0 = 8.8125` | Draw the corrected A–C shoulder-width line from **(11,0)** to **(2.1875,0)**. |
| B03 | 36:43; follows corrected C at 40:46 | `3`, fixed construction guide; no body formula supplied | Draw the corrected C vertical guide from **(2.1875,0)** to **(2.1875,3)**. |
| B04 | 36:51 | `17.75 + 0 = 17.75` | Draw/retrace B–D upward from **(11,19)** to **(11,1.25)**. |
| B05 | 37:15 | `4`, fixed construction guide; no body formula supplied | Draw the D horizontal guide from **(11,1.25)** to **(7,1.25)**. |
| B06 | 37:29 | `10.25 + 0.75 = 11` | Draw the back-width B–E line from **(11,19)** to **(0,19)**. |
| B07 | 37:48 | `hE`, **UNRESOLVED** guide length | Draw the E vertical guide from **(0,19)** to **(0,19−hE)**. |
| B08 | 38:13 | `3.5 + 0.125 = 3.625` | Draw/retrace the back-neck width A–F from **(11,0)** to **(7.375,0)**. |
| B09 | 38:41; successful retry 41:20 | `18.5 + 0.125 = 18.625` | Draw the shoulder-slope diagonal B–G from **(11,19)** to **(2.1875,2.591756)**. |
| B10 | 39:19; successful retry 42:02–43:18 | `S_body + 0.5 = s`; adopted `5.5625+0.5=6.0625`, **body value UNRESOLVED** | Draw the preliminary shoulder F–H from **(7.375,0)** to **(1.951702,2.709565)** along the ray through G. |
| B11 | 43:23 | `19−17.75 = 1.25` | Draw the neckline-corner guide F–V from **(7.375,0)** to **(7.375,1.25)**. |
| B12 | 43:34 | `4.0625 + 0 = 4.0625` | Draw/retrace the waist dart-placement B–I line from **(11,19)** to **(6.9375,19)**. |
| B13 | 43:50 | `8.25 + 1.75 dart provision = 10`, no stated ease | Draw/retrace the lower-width B–J line from **(11,19)** to **(1,19)**. |
| B14 | 44:18 | `d`, **UNRESOLVED** fixed dart intake: 1.5 versus 1.75 | Draw/retrace the dart-base I–K segment from **(6.9375,19)** to **(6.9375−d,19)**. |
| B15 | 44:43 | `0.1875`, fixed contour correction, not ease | Draw the J–M drop from **(1,19)** to **(1,19.1875)**. |
| B16 | 45:10 | `8.875 + 0 = 8.875` | Draw the side seam M–N from **(1,19.1875)** to **(0,19.1875−sqrt(8.875²−1²))**; E-line intersection is **ASSUMED**. |
| B17 | 45:45 | `8.875 − 1 = 7.875`; 1-inch subtraction is a fixed dart-height rule | Draw the waist-dart center L–O from **(6.9375−d/2,19)** to **(6.9375−d/2,11.125)**. |
| B18 | 46:42 | `sqrt((d/2)²+7.875²) + 0.125` | Draw the inner extended dart leg O–I1 from **(6.9375−d/2,11.125)** to **(Ox+(dist(O,I)+0.125)(Ix−Ox)/dist(O,I), Oy+(dist(O,I)+0.125)(Iy−Oy)/dist(O,I))**. |
| B19 | 46:42 (second leg narrated 47:02) | `sqrt((d/2)²+7.875²) + 0.125` | Draw the outer extended dart leg O–K1 from **(6.9375−d/2,11.125)** to **(Ox+(dist(O,K)+0.125)(Kx−Ox)/dist(O,K), Oy+(dist(O,K)+0.125)(Ky−Oy)/dist(O,K))**. |
| B20 | 46:58 | `BezLen(B,(Bx+(I1x−Bx)/3,By),(Bx+2(I1x−Bx)/3,I1y),I1)` | Draw the provisional inner-waist Bezier B–I1 from **(11,19)** to **(I1x,I1y)** with controls **(11+(I1x−11)/3,19)** and **(11+2(I1x−11)/3,I1y)**. |
| B21 | 47:10 | `BezLen(K1,(K1x+(1−K1x)/3,K1y),(K1x+2(1−K1x)/3,19.1875),M)` | Draw the provisional outer-waist Bezier K1–M from **(K1x,K1y)** to **(1,19.1875)** with controls **(K1x+(1−K1x)/3,K1y)** and **(K1x+2(1−K1x)/3,19.1875)**. |
| B22 | 47:21 | `(S_body+0.5)/2 = s/2 = 3.03125` provisionally; spoken rounded result is 3 | Draw/retrace the half-shoulder F–P segment from **(7.375,0)** to **((7.375+Hx)/2,Hy/2)**. |
| B23 | 47:44 | `3`, fixed shoulder-dart length; no body formula supplied | Draw the shoulder-dart center P–Q from **(Px,Py)** to **(Px+3(Ox−Px)/dist(P,O), Py+3(Oy−Py)/dist(P,O))**. |
| B24 | 47:55 | `0.25`, half of the 0.5 shoulder-dart provision | Draw/retrace the neck-side dart-width P–R0 segment from **(Px,Py)** to **(Px+0.25(Fx−Px)/dist(P,F), Py+0.25(Fy−Py)/dist(P,F))**. |
| B25 | 48:09 | `dist(Q,R0)+e`, **e UNRESOLVED**; later ruler reading about `3.375` at 48:42–48:50 | Draw the extended neck-side shoulder-dart leg Q–R from **(Qx,Qy)** to **(Qx+(dist(Q,R0)+e)(R0x−Qx)/dist(Q,R0), Qy+(dist(Q,R0)+e)(R0y−Qy)/dist(Q,R0))**. |
| B26 | 48:29 | `dist(F,R)` using body shoulder length, dart provision, and unresolved e | Draw the final inner shoulder F–R from **(7.375,0)** to **(Rx,Ry)**. |
| B27 | 48:34 | `0.25`, other half of the 0.5 shoulder-dart provision | Draw/retrace the armhole-side dart-width P–U0 segment from **(Px,Py)** to **(Px+0.25(Hx−Px)/dist(P,H), Py+0.25(Hy−Py)/dist(P,H))**. |
| B28 | 48:53 | `dist(Q,R)` to equalize the two shoulder-dart legs | Draw the outer shoulder-dart leg Q–U from **(Qx,Qy)** to **(Qx+dist(Q,R)(U0x−Qx)/dist(Q,U0), Qy+dist(Q,R)(U0y−Qy)/dist(Q,U0))**. |
| B29 | 49:09 | `dist(U,H)` | Draw the final outer shoulder U–H from **(Ux,Uy)** to **(Hx,Hy)**. |
| B30 | 49:22 | `17.75/4 = 4.4375`, not the rounded 4.43 | Draw/retrace D–S downward from **(11,1.25)** to **(11,5.6875)**; starting from D is **ASSUMED**. |
| B31 | 49:56 | `7.5625 + 0.25 = 7.8125` | Draw the across-back S–T line from **(11,5.6875)** to **(3.1875,5.6875)**. |
| B32 | 50:16 | `uT+dT`, **UNRESOLVED** guide length | Draw the T vertical guide from **(3.1875,5.6875−uT)** to **(3.1875,5.6875+dT)**. |
| B33 | 50:32 | `dist(H,N)`; actual armhole arc length **UNRESOLVED** | Draw the **straight substitute for the back armhole curve** from H **(Hx,Hy)** to N **(0,19.1875−sqrt(8.875²−1²))**. |
| B34 | 51:43 | `0.375`, fixed neckline shaping guide; angle **UNRESOLVED** | Draw the neckline diagonal V–W from **(7.375,1.25)** to **(7.375+0.375*cos(theta),1.25−0.375*sin(theta))**. |
| B35 | 51:51 | `BezLen(F,(7.375,k*1.25),(11−k*3.625,1.25),D)` | Draw the provisional neckline Bezier F–D from **(7.375,0)** to **(11,1.25)** with controls **(7.375,k*1.25)** and **(11−k*3.625,1.25)**. |

The back armhole instruction initially names H, T, and N, but at 51:33 the speaker explicitly says the drawn curve does not hit T. B33 therefore does not falsely claim to reconstruct a curve through all three. A final curve requires video tracing or a supplied intermediate point/tangent; the straight chord is only a placeholder.

The back neckline's 3/8 diagonal is documented in B34, but its angle and exact relationship to the finished curve are missing. B35 is an independent provisional quarter-ellipse model, not a claim that it passes W. If passing W is confirmed later, revise the Bezier controls accordingly and recalculate its length.

## Information to supply or verify before treating this as a finished pattern

| Priority | Missing or conflicting information | Where to cross-check | What changes |
|---|---|---|---|
| High | Front I constrained to top line A–C? | 20:24–20:36 | Neckline, strap intersection, side and waist positions |
| High | Front bust-span addition really 1 1/4, and what does that addition represent? | 20:46–21:24 | K, dart position, all dart/waist geometry |
| High | Front F means original point or the lowered point; use 4 1/16 or 4 1/8? | 23:05–23:41; 27:48–28:31 | Waist subtraction and dart bases |
| High | Front P offset direction and exact correction to equal side length | 25:32–26:49 | P, Q, R and outer waist |
| High | Equalize front dart legs from K or shortened tip T? Is the setback vertical or centered on the dart? | 29:46–30:51 | Final dart endpoint R and outer waist |
| High | Actual back body shoulder length and final total | 39:26–39:36; 42:02–43:18 | H, shoulder dart, armhole |
| High | Back waist intake 1 1/2 or 1 3/4, and whether B–J provision should change | 43:50–44:29 | Back dart and waist |
| High | Back waist legs extend past I/K, not L/K; extension along rays or vertically? | 46:42–47:17 | Back waist contour |
| High | Back shoulder extension 1/8 or 1/2; actual endpoint shown | 48:09–49:09 | Shoulder dart and shoulder edges |
| Medium | Back N lies on the E vertical; S lies one quarter of D–B below D | 45:19–45:33; 49:22–49:47 | Armhole/side geometry |
| Medium | Front underarm guide endpoint and actual armhole shape; back armhole shape bypassing T | 26:54–27:18; 31:21–32:24; 50:32–51:35 | Replace straight armhole substitutes with Beziers |
| Medium | Neckline angle guides and curve relationship | 32:30–33:21; 51:43–52:05 | Replace provisional neck controls |
| Low | Guide extents uM, dM, o, hE, uT, dT | 22:49; 26:54; 37:48; 50:16 | Construction display only, unless used to locate curve endpoints |

The document intentionally leaves unresolved quantities symbolic rather than inventing measurements. Once they are supplied, all dependent point coordinates and straight/Bezier lengths can be recalculated from the formulas above. The two armhole substitutes must be replaced before using the outlines as garment patterns.

## Numerical audit of resolved formulas

These values use the provisional front choices and adopted back shoulder total described above. They are not additional video measurements. Values are inches, rounded to six decimals; calculations use unrounded coordinates. Bezier arc lengths use composite Simpson integration with 10,000 subintervals.

| Front point | Calculated SVG coordinate |
|---|---|
| Q | (5.957562, 18.982759) |
| R | (6.011360, 19.415074) |
| Z | (5.036930, 19.426287) |
| T | (4.944692, 11.410653) |

| Step / quantity | Calculated length |
|---|---:|
| F21 | 6.761358 |
| F24 | 8.695939 |
| F25 | 8.260289 |
| F27 | 8.075180 |
| F28 | 8.695939 |
| F29 | 8.075180 |
| F30 | 4.067688 |
| F31 | 4.925818 |
| F32 | 5.708278 |
| F33 | 4.470645 |
| F35 | 5.582543 |
| B33 armhole substitute chord | 7.904199 |
| B35 provisional neck Bezier | 4.060148 |

Back shoulder midpoint P = **(4.663351, 1.354782)**. Other back dart-dependent lengths remain symbolic because d and e conflict in the captions.

The reconstructed final front dart legs T–F and T–R are equal because T is placed on the symmetry axis of the equalized preliminary dart. Their calculated length differs from the speaker’s approximate 8.5-inch ruler reading; verify the original endpoint labels and truing sequence. The provisional waist Beziers are not constrained to preserve the original horizontal waist-arc totals: changing endpoints and adding curvature changes seam length. Exact waist seam-length preservation remains UNRESOLVED pending those checks and curve refinement.
