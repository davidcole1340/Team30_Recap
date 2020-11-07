class: title-slide
count: false
.logo-title[]

# Main Title
### Sub Title

.TitleAuthor[Author Name]

---

layout: true
name: template_slide

.logo-slide[]
.footer[[Author Name](https://www.linkedin.com/in/authorname), Department of Electrical, Computer and Software Engineering (2020)]

---
name: S1

# Embedding a Video

.center[<iframe width="975" height="430" src="https://www.youtube.com/embed/fHCemviY06Y?modestbranding=0&autohide=1&controls=0&playsinline=0&autoplay=0" frameborder="50" allow="encrypted-media" allowfullscreen></iframe>]

---
name: S2

# Single Column Slide with Image 

- Checkout https://remarkjs.com/#1 for more information
- .center .left and .right tags can be used to allign the immage
 - top, middle and bottom can also be used

.center[<img src="img/intro/UoAMap.png" height="300">]

---
name: S3

# Two Column Format

.left-column[
- Use .left-column and .right-column 
 - Sub bullet point
- Bullet point 2
 - Sub bullet point
- Bullet point 3
]

.right-column[
.right[<img src="img/intro/UoAEng.png" width="300px">]
]

---

class: title-slide
layout: false
count: false
.logo-title[]

# Section Separation
### Sub Title of the Section

---

layout: true
name: template_slide

.logo-slide[]
.footer[[Author Name](https://www.linkedin.com/in/authorname), Department of Electrical, Computer and Software Engineering (2020)]

---
name: S4

# Adding Equations

- Adding an in-line equation
 - `\(L_{pt}\)` and `\(L_{st}\)` are in-line
- Adding an equation 
\\[M = k\sqrt{L\_{pt}L\_{st}}\\]
- Another in-line equation `\(n = \frac{N_{pt}}{N_{st}} = \sqrt{\frac{L_{pt}}{L_{st}}}\)`
- Note the use of \ for subscripts which differs from Latex

---
name: S5

# Adding Slide Notes

- Press 'P' to view the notes in the presenter mode
- Although a T equivalent transformer model can be used to model the coils, the coupled inductor model is widely used when analysing an IPT system in the phasor-domain
- In the coupled inductor model, `\(L_{pt}\)` and `\(L_{st}\)` represent the self-inductances of primary and pick-up coils
- `\(V_{sr}\)` represents voltage induced across `\(L_{st}\)` due to current `\(I_{pt}\angle 0\)` flowing through `\(L_{pt}\)` and is given by
\\[V\_{sr} = \omega MI\_{pt}e^{j\pi/2}\\]
- Similarly, `\(V_{pr}\)` represents voltage induced across `\(L_{pt}\)` due to `\(I_{st}\angle\theta\)` and is given by
\\[V\_{pr} = \omega MI\_{st}e^{j(\theta+\pi/2)}\\]

???

If the current through primary coil is `\(I_{pt} \sin (\omega t)\)` then,
\\[\phi\_{m} \propto I\_{pt} \sin (\omega t) \\]
The voltage induced on the pick-up coil is therefore,
\\[v\_{sr} \propto \frac{\mathrm{d} \phi\_{m} }{\mathrm{d} t} \\]
\\[v\_{sr} \propto \omega I\_{pt} \cos (\omega t) \\]
Since `\(M\)` represent the coupling between the two coils,
\\[v\_{sr} = \omega M I\_{pt} \cos (\omega t) \\]
In the phasor-domain,
\\[V\_{sr} = \omega M I\_{pt} e^{j\pi/2} \\]

---
name: S6

# Zoom when Hover Over Image

.questions[
The image below should expand when mouse over it. There are two zoom classes defined above.

When placed `\(100 mm\)` apart the primary and pick-up coils of an IPT system each measures `\(18.73 \mu H\)`. `\(k\)` between the two coils is measured as 10%. The primary uses LCL compensation and is energised using a `\(50 V_{rms}\)` sinusoidal voltage source, `\(V_{pi}\)`, that has a frequency of `\(85 \mathit{kHz}\)`. 
]

.left-column[
- Show that `\(C_{pi}\)` has to be `\(374.4 nF\)` to ensure `\(I_{pt}=10A_{rms}\)`
- Show that `\(C_{pt}\)` has to be `\(374.4 nF\)` 
- Develop a simulation model in LTSpice 
 - `\(L_{pi}\)` can be added a `\(50 m \Omega\)` ESR to help reach SS faster
- With the aid of this model show that 
 - `\(P_{o} \approx 50W\)`
]

.right-column[
.zoom175[
.center[<img src="img/netw/EgPPTLCLSPCompM1.png" width="300px">]
.center[<img src="img/netw/EgPPTLCLSPCompM2.png" width="300px">]
]
]

---
name: S7

# HTML Table 

<table class="tg" style="undefined;table-layout: fixed; width: 650px; margin-left:auto; margin-right:auto;">
  <colgroup>
  <col style="width: 325px">
  <col style="width: 325px">
  </colgroup>
  <thead>
    <tr>
      <th class="tg-dzaw"><span style="color:white">MCUs</span></th>
      <th class="tg-dzaw"><span style="color:white">FPGAs & CPLDs</span></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td class="tg-jayl">Fixed circuitry</td>
      <td class="tg-jayl">Flexible circuitry</td>
    </tr>
    <tr>
      <td class="tg-sabo">Executes software</td>
      <td class="tg-sabo">Described by software</td>
    </tr>
    <tr>
      <td class="tg-ig71">Sequential</td>
      <td class="tg-ig71">Parallel</td>
    </tr>
    <tr>
      <td class="tg-sabo">Low processing power</td>
      <td class="tg-sabo">High processing power</td>
    </tr>
    <tr>
      <td class="tg-ig71">General applications</td>
      <td class="tg-ig71">Specific applications</td>
    </tr>
    <tr>
      <td class="tg-sabo"><b>Low power consumption</b></td>
      <td class="tg-sabo">High power consumption</td>
    </tr>
    <tr>
      <td class="tg-ig71"><b>Cheap & widespread</b></td>
      <td class="tg-ig71">Expensive but becoming more widely used</td>
    </tr>
    <tr>
      <td class="tg-sabo"><b>Cheaper development tools</b></td>
      <td class="tg-sabo">Expensive development tools</td>
    </tr>
    <tr>
      <td class="tg-ig71"><b>Easier to get started</b></td>
      <td class="tg-ig71">Harder to get started</td>
    </tr>
  </tbody>
</table>

---
name: S8

# Jumping to a Slide

You can read [here](#S3) for more infromation

---
name: S9

# C Code Example

You can add code like this. 

```c
int a;
for( a = 10; a < 20; a = a + 1 )
{
  printf("value of a: %d\n", a);
}
```


---

class: title-slide
layout: false
count: false
.logo-title[]

# Acknowledgements
#### Special thanks to XX 
#### for their valuable feedback.

---

class: title-slide
layout: false
count: false
.logo-title[]

# Questions?
### Thank you