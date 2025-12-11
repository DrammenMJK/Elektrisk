# CAT6 Wiring Cheat-Sheet for XBus Lenz, RS-485 + Power

| Pair | Colours (Stripe + Solid) | Function        | Assignment                         |
|------|----------------------------|------------------|-------------------------------------|
| 2    | White/Orange + Orange      | RS-485 Bus       | **A = White/Orange**, **B = Orange** |
| 1    | White/Blue + Blue          | Power Feed 1     | **+V = Blue**, **0V = White/Blue**   |
| 3    | White/Green + Green        | Power Feed 2     | **+V = Green**, **0V = White/Green** |
| 4    | White/Brown + Brown        | Spare / Shield Ref / Not Used | Keep unused or tie Brown to 0V at one end only |

## Notes
- Keep **A and B on Pair 2** only.  
- Use **Pair 1 and Pair 3 in parallel** to reduce voltage drop to controllers.  
- Join +V wires together and 0V wires together at every panel.  
- Do **not** use Pair 4 for power unless needed; keep Brown pair isolated or tied to 0V only at the base station end.  
- Only connect cable shield to ground at **one end** (LZV200 side).

---------------

# CAT6 Wiring Cheat-Sheet for Lenz RS-485 + Power

| Pair | Colours (Stripe + Solid) | Function        | Assignment                         |
|------|----------------------------|------------------|-------------------------------------|
| 2    | White/Orange + Orange      | RS-485 Bus       | **A = White/Orange**, **B = Orange** |
| 1    | White/Blue + Blue          | Power Feed 1     | **+V = Blue**, **0V = White/Blue**   |
| 3    | White/Green + Green        | Power Feed 2     | **+V = Green**, **0V = White/Green** |
| 4    | White/Brown + Brown        | Spare / Not Used | Keep unused or tie Brown to 0V at one end only |

---

# Daisy-Chain Installation Instructions

### Trunk Layout
Use a **single continuous CAT6 cable** as the RS-485 trunk.  
All 20 connector panels must be wired **in series**, not in a star.

At each panel:
- Bring the CAT6 **in**,  
- Bring the CAT6 **out**,  
- Join each conductor colour-to-colour (A-A, B-B, +V to +V, 0V to 0V).  
- Keep stubs to panel sockets as short as possible.

Both power pairs (Blue pair and Green pair) must be **passed through every panel** and joined in parallel.

### RS-485 Termination
Use **exactly two terminations**:

1. **Base station end (LZV200):**  
   Built-in 150 Ω + bias network → **leave as is**.

2. **Far end of the CAT6 trunk:**  
   Add a **100 Ω resistor** across **A and B**  
   (White/Orange ↔ Orange).

No other terminations anywhere along the chain.

### Shielding
- The CAT6 S/FTP shielding (individual pair shields + outer shield) must run **unbroken through every panel** from end to end.
- At intermediate panels and at the far end, the shield must **not be connected to any terminal, pin, or ground** — simply pass it straight through.
- The shield is connected to ground **only at the LZV200 end**.  
  Nowhere else.

This keeps the shield effective along the whole cable but prevents ground loops and noise injection into the RS-485 pair.


### Power Distribution
- Use **Pair 1 and Pair 3 together** for power.  
- Join both +V wires (Blue + Green) together at every panel.  
- Join both 0V wires (White/Blue + White/Green).  
- Feed panel sockets from these combined nodes.

This halves voltage drop and keeps the supply stable for all LH101 controllers.

---
