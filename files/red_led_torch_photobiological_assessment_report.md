# Photobiological risk assessment — handheld red LED torch (632 nm)

## Internal assessment, and request for external review

| | |
|---|---|
| **From** | `[name]`, Laser Safety Officer |
| **To** | `[name]`, External Radiation Safety Advisor |
| **Date** | 2026-10-16 |
| **Ref** | `[document ref]` |
| **Device** | Handheld red LED torch, hunting type. `[manufacturer / model / serial]` |
| **Status** | Internal assessment — not a conformity statement. Issued for external review. |
| **Revision** | Rev. 2 — incorporates the repeat lab session of `[date]` and its uncertainty budget. Supersedes Rev. 1 (measured 160 W/m², no uncertainty treatment). |

> Fields in `[square brackets]` are to be completed before issue. They are facts
> about our instruments and procedures that are not established in the
> calculation record this report summarises.

---

## 0. Summary

A 632 nm handheld LED torch was assessed against IEC 62471 (photobiological
safety of lamps and lamp systems) and against the risk-assessment guidance in the
*non-binding guide to good practice for implementing Directive 2006/25/EC*
(hereafter "the guide"). Calculations were performed with an in-house tool
(Appendix C.5) using an in-house irradiance measurement of 188 W/m² at 200 mm,
stated to ±20 % (§2.5).

All configurations classify as IEC 62471 Exempt Group across the whole
uncertainty band. The guide's triviality screen, which determines whether a
source requires a formal risk assessment, gives different outcomes for the three
configurations:

| Configuration | % of exposure limit (best estimate) | At +20 % | Threshold | Trivial? |
|---|---|---|---|---|
| Part 1 — full brightness, 188 W/m² | 18.8 % | 22.6 % | 20 % | Not across the band — exceeded at the upper bound |
| Part 2 — dimmed, 18.8 W/m² (analogue) | 1.88 % | 2.26 % | 20 % | Yes; margin 8.9× at the upper bound |
| Part 3 — own-build, 4 emitters, full power | 18.8 % per source | 22.6 % | 5 % (20 %/4) | No — exceeded by 3.8× |

### Conclusions submitted for review

1. **Dimmed torch: trivial source.** At the 1/10 analogue current setting the
   binding criterion sits at 1.88 % of the exposure limit against the guide's
   ≈20 % criterion, and at 2.26 % at the +20 % end of the uncertainty band
   (margin 8.9×). The determination does not depend on the accuracy of our
   measurement.

2. **Full brightness: not determinable from our measurement.** The best estimate
   is 18.8 % of the exposure limit, below the 20 % threshold; the upper bound of
   our stated uncertainty is 22.6 %, above it. The determination is therefore not
   robust within the measurement that produced it. A band better than ±6.4 %
   would be required for robustness, and the two characterised uncertainty terms
   already exceed that in quadrature before the battery term is counted (§2.5).
   We therefore request the manufacturer's IEC 62471 test report before
   authorising internal use at maximum brightness.

3. **Multi-emitter own-build: external measurement proposed.** At full power such
   an array exceeds the guide's pro-rata triviality threshold by 3.8× at the best
   estimate and 4.5× at the upper bound. The result additionally depends on
   emitter spacing and on the collimator's apparent source size, neither of which
   our in-house setup can establish to the required confidence (§5). We propose
   engaging an external laboratory with traceable instrumentation to measure the
   completed assembly.

---

## 1. Background for non-specialist readers

*Specialist readers can proceed to §2.*

### Hazards considered

Visible light can injure the retina by two mechanisms: thermal injury (over
seconds) and photochemical injury (accumulating over minutes to hours, the
"blue light" hazard). The two have separate limits, separate units and separate
measurement rules. Ultraviolet and infrared can additionally injure the cornea
and lens. This torch emits no ultraviolet and no infrared, so only the two
retinal hazards apply.

### Calculation chain

Every number in this report follows the same chain. Each step is a physical
measurement or a formula from the standard; judgement enters only where flagged.

| Step | Quantity established | Input |
|---|---|---|
| 1 | Apparent source — the emitting patch the eye images | observation into the torch under operating conditions |
| 2 | α, the angular subtense of that patch | its width (11 mm) and the viewing distance (200 mm) |
| 3 | ω, the solid angle it subtends | its area (121 mm²) and the same distance |
| 4 | Applicable limits and the weighted irradiances | the emission wavelength (632 nm) |
| 5 | Radiance L = E/ω, the quantity the retinal limits use | steps 3 and 4 |
| 6 | Comparison against the limit, and the margin | step 5 and the standard's formulas |

### Two distinct questions

- **IEC 62471 risk group** — a product classification. Exempt Group means no
  photobiological hazard under foreseeable conditions. All configurations here
  are Exempt across the whole uncertainty band.
- **Triviality under the Directive** — a workplace risk-assessment question. The
  guide's test is whether exposure is below ≈20 % of the exposure limit,
  pro-rated by the number of sources a worker faces (guide §2.3 and §6.2).

The triviality screen is the stricter of the two, and is what separates the
configurations assessed here. A source can be Exempt Group and not trivial;
that is the case in Parts 1 and 3.

---

## 2. Scope, standard and method

### 2.1 Standard applied

IEC 62471 applies. LEDs were within the scope of the laser standard IEC 60825-1
until Edition 3 (2007) removed them, on the basis that laser methodology applied
to an extended, incoherent, broad-beam source produces misleading
classifications. An LED torch is a lamp system, not a laser product.

Our tool implements both standards and does not default to either. For this
device the two give answers in different units: IEC 62471 limits a radiance,
W/(m²·sr); IEC 60825-1 limits a corneal irradiance, W/m². The laser-standard
figure (271 W/m² at 8 h) is in the same units as the raw measurement and would
read as a 69 % margin. It is not applicable to an LED and is not used anywhere in
this report.

### 2.2 Device and measurement

| Parameter | Value | How established |
|---|---|---|
| Peak wavelength | 632 nm | `[manufacturer datasheet / our measurement]` |
| Spectral width | ~20 nm FWHM assumed | typical for a high-power red LED; see §2.4 |
| Irradiance at 200 mm, full brightness | 188 W/m² ± 20 % | `[instrument make/model]`, most collimated setting; repeat session `[date]` |
| Irradiance at 200 mm, dimmed | 18.8 W/m² | analogue current control at 1/10 — see §2.3 |
| Apparent source | 11 mm square | visual estimate under operating conditions |
| Measurement distance | 200 mm | `[method]` |
| Beam setting | most collimated | worst case — see below |

**Beam setting.** Collimation concentrates the same flux into the smallest solid
angle, and radiance is flux per unit area per unit solid angle. Both applicable
limits are radiances, so the most collimated setting maximises the limited
quantity. §5.2 gives a second reason.

**Distance.** The Directive fixes no standard distance for this class of product.
200 mm is taken as approximately the closest a person's eye comes to a torch they
are holding. The assessor must choose a defensible distance and state it. These
results must not be rescaled to other distances by the inverse-square law: a
collimated beam does not follow it in the near field.

### 2.3 Dimming method: analogue current control

The torch dims by analogue current control, not by pulse-width modulation. The
consequences for the assessment:

- A PWM dimmer leaves the peak radiance unchanged and reduces only the
  time-average. The photochemical hazard is a cumulative dose and could be
  time-averaged; the thermal hazard is peak-driven and could not. The two hazards
  would have to be assessed on different numbers, and the standard's
  multiple-pulse criteria would apply.
- An analogue current reduction lowers the emission at every instant. The 1/10
  setting delivers 18.8 W/m² continuously, and both hazards are assessed on that
  single number with no pulsed-source treatment.

The geometry is also identical between the two settings: reducing the drive
current changes how hard the die is driven, not where its image forms or how
large it is. The apparent source remains 11 mm square, so α and ω carry over
unchanged.

### 2.4 Monochromatic treatment of the source

The LED is treated as monochromatic at its 632 nm peak. For this source the
treatment is exact rather than approximate:

Both applicable hazard weightings are flat across the LED's emission band
(598–666 nm): B(λ) = 0.001 throughout 600–700 nm, and R(λ) = 1.0 throughout
435–700 nm. Integrating a flat weighting against any lineshape gives
`weighting × total irradiance` independently of the lineshape. This was verified
by integrating a 20 nm FWHM Gaussian against both weightings; the result
reproduces the single-wavelength answer to 0.00 %. The assumed 20 nm linewidth
does not enter the hazard numbers.

Only the photometric figure (V(λ), used for the luminance screen in §3.2) is
lineshape-sensitive, at +3.6 %. It feeds no exposure limit.

The treatment does not generalise: for a white, blue or UV source B(λ) varies by
three orders of magnitude across the emission band and the spectrum must be
measured.

### 2.5 Measurement uncertainty

The guide requires the assessment to account for measurement uncertainty. Here
the measurement, not the calculation, is the limiting factor. Budget after a
second lab session with improved alignment control:

| Contribution | Magnitude | Type |
|---|---|---|
| Alignment and positioning repeatability | ± 10 % | established by repeat measurement |
| Detector calibration (accuracy on the reading) | ± 3 % | manufacturer's specification |
| Torch battery state of charge | not separately quantified | systematic, direction unknown |
| Overall stated band | ± 20 % | assessor's expanded estimate |

The two quantified terms combine in quadrature to √(10² + 3²) = 10.4 % as a
standard uncertainty; the conventional k = 2 coverage factor (≈95 % confidence)
expands that to 20.9 %. The stated ±20 % is therefore consistent with a k = 2
expanded uncertainty on the characterised terms, with the battery contribution
absorbed within it.

**Propagation.** The chain in §1 contains no non-linear step: every quantity from
the measured irradiance to a final margin is reached by multiplying or dividing
by a constant (`× W(λ)`, `÷ ω`, `÷ limit`). A ±20 % band on the irradiance is
therefore a ±20 % band on every margin in this report, with no propagation
arithmetic required.

**Sensitivity of the binding criterion.** The two soft inputs do not contribute
equally:

| Input | Uncertainty | Effect on the binding (blue-light) criterion |
|---|---|---|
| Irradiance | ± 20 % | directly proportional — ±20 % |
| Apparent source size | ± 20 % (visual estimate) | none |

The blue-light criterion is independent of the apparent source size, because ω_B
is fixed by the standard's 110 mrad field rather than by the source (§3.4), and
limit d is flat for any α ≥ 11 mrad. The criterion is proportional to the
irradiance, which is the quantity our non-traceable measurement establishes least
well. The remedies proposed in §3.7 and §5.4 therefore concern traceable
radiometry rather than improved geometry.

---

## 3. Part 1 — Torch at full brightness (188 W/m²)

### 3.1 Geometry

The apparent source is neither the LED die nor the front lens. It is the
collimator's magnified image of the die, approximately 11× linear magnification
of a ~1 mm square chip. The square shape supports this: LED dies are square,
lenses and reflectors are round, so a square emitting patch behind a round
aperture is an image of the die.

| Quantity | Value | Derivation |
|---|---|---|
| α, per axis | 54.99 mrad | 2·arctan(11 mm / 400 mm) |
| α, effective | 54.99 mrad | square source: both axes clamped to [1.7, 100] mrad *then* averaged (IEC 62471 §4.2.2 specifies that order) |
| ω, source | 3.025 msr | 121 mm² / (200 mm)² |

α takes a width and ω takes an area; they feed different formulas and are not
redundant.

### 3.2 Preliminary screening

The guide offers a screen (§2045) by which a white-light general lighting source
below 10⁴ cd/m² needs no retinal assessment. It was not relied on: this is not a
white-light general lighting source, and the luminance is above the threshold in
any case.

- Photopic irradiance = 188 × V(632) = 188 × 0.2446 = 46.0 W/m²
- Illuminance = 46.0 × 683 lm/W = 31 413 lux
- Luminance = 31 413 / 3.025 msr = 1.04 × 10⁷ cd/m² — 1 038× the screen

The luminance also fixes the limiting aperture at 3 mm (IEC 62471 §4.2.1:
>10 cd/m² and >0.25 s exposure ⇒ constricted pupil).

> **Note for the H&S advisor.** V(632) = 0.245, so about a quarter of this
> torch's radiometric output registers as visible brightness, while R(632) = 1.0
> places all of it in the retinal-thermal hazard. Per unit of apparent
> brightness, red light is therefore about 4× more hazardous than green-yellow
> light. Blink aversion and pupil constriction are both triggered by apparent
> brightness, so apparent dimness is not evidence of safety for a red source.
> The margins below are radiometric and are not observable by eye.

### 3.3 Applicable limits

| Weighting | Band | Value at 632 nm | Applies? |
|---|---|---|---|
| S(λ) actinic UV | 180–400 nm | out of band | No — no UV emission |
| UVA, unweighted | 315–400 nm | out of band | No |
| B(λ) blue light | 300–700 nm | 0.001 | Yes — limit d |
| R(λ) retinal thermal | 380–1400 nm | 1.0 | Yes — limit g |
| IR, cornea/lens | 780–3000 nm | out of band | No — no IR emission |

The three "No" entries follow from the 632 nm peak and ~20 nm linewidth; they are
not gaps in the data.

### 3.4 The two averaging solid angles

ω is not used directly. The Directive specifies the measurement field of view
each retinal hazard is averaged over, with ω_used = max(ω_source, ω_γ)
(guide §2082–2095):

| Hazard | Field of view γ | ω_γ | ω used | Set by |
|---|---|---|---|---|
| Blue light (limit d) | 110 mrad | 0.01 sr | ω_B = 0.01 sr | γ — the source is 3.3× smaller than the field |
| Retinal thermal (limit g) | 11 mrad | 0.0001 sr | ω_A = 3.025 msr | the source — 30× larger than the field |

**Origin of γ.** A photochemical injury accumulates over long exposures, during
which involuntary eye movement distributes the retinal image over roughly
110 mrad, so the limit is written as a radiance averaged over that field. A
thermal injury occurs too quickly for eye movement to contribute, so its field is
ten times tighter. The `max()` prevents division by a solid angle smaller than
the eye holds still on.

ω_B = 0.01 sr is therefore a property of the standard rather than of this torch.
It is the same value in each of the guide's Appendix D examples. This is used in
§2.5 and §5.3.

### 3.5 Radiance and comparison with the limits

| | Blue light (limit d) | Retinal thermal (limit g) |
|---|---|---|
| Weighted irradiance | E_B = 188 × 0.001 = 0.188 W/m² | E_R = 188 × 1.0 = 188 W/m² |
| ÷ its own ω | ÷ 0.01 sr | ÷ 3.025 msr |
| Measured radiance | L_B = 18.8 W/(m²·sr) | L_R = 62 149 W/(m²·sr) |
| Exposure limit | 100 W/(m²·sr) | 509.2 kW/(m²·sr) |
| Limit formula | flat, for α ≥ 11 mrad, t > 10 000 s | 2.8×10⁷ / C_α, C_α = 54.99 mrad |
| Result | 18.8 % of limit (81.2 % headroom) | 12.2 % of limit (87.8 % headroom) |

E_R equals the raw measured irradiance exactly because R(632) = 1.0. For this
source, total irradiance and R(λ)-weighted effective irradiance are the same
number.

**Exposure duration.** Limit g decreases with duration and flattens above 10 s,
so the long-duration branch is the global minimum. Assessing against it covers
every shorter exposure, and no assumption about viewing duration enters the
assessment.

### 3.6 Classification

Checked against all three groups' criteria, the source satisfies Exempt Group on
both applicable hazards. The Exempt/RG1 boundary corresponds to 1 000 W/m² at
this geometry, a factor of 5.3 above the measurement, so the classification holds
at the top of the uncertainty band as well (225.6 W/m² → Exempt, 4.4× clear).

The risk-group classification is therefore not in question. The remainder of this
section concerns the Directive's triviality screen.

### 3.7 Triviality screen

Applying the guide's criterion (§2.3, §6.2 — *"less than 20 % of the ELV for a
full working day"*) across the uncertainty band of §2.5:

| | Irradiance | Blue light | Thermal | Binding | vs 20 % screen | Trivial? |
|---|---|---|---|---|---|---|
| Lower bound, −20 % | 150.4 W/m² | 15.04 % | 9.76 % | 15.0 % | 1.33× margin | Yes |
| Best estimate | 188 W/m² | 18.80 % | 12.20 % | 18.8 % | 1.06× margin | Yes |
| Upper bound, +20 % | 225.6 W/m² | 22.56 % | 14.65 % | 22.6 % | 0.89× — over | No |

The triviality determination for the full-brightness torch is satisfied at the
best estimate and at the lower bound, and not satisfied at the upper bound. It is
therefore not robust within the stated measurement uncertainty: the measurement
as performed does not determine the outcome of the screen.

#### Measurement accuracy required

The chain is linear (§2.5), so the requirement inverts directly:

| | Value |
|---|---|
| Irradiance sitting exactly on the 20 % screen | 200 W/m² |
| Our best estimate | 188 W/m² |
| Headroom on the best estimate | 1.064×, i.e. 6.4 % |
| Band required for a determination robust across the band | better than ± 6.4 % |
| Band available | ± 20 % |
| Highest irradiance robustly trivial at ± 20 % | 167 W/m² (0.89× our measurement) |

±6.4 % is not reachable by more careful use of the present setup. It requires a
traceably calibrated detector, a characterised spectral responsivity at 632 nm, a
mapped beam so that the true peak is known rather than sampled, and a controlled
drive condition. The two already-characterised terms — 10 % alignment and 3 %
detector — exceed 6.4 % in quadrature before the battery term is counted.
Eliminating the battery term entirely would still leave ≈10.4 % standard,
≈21 % expanded.

The limiting factor is therefore the absolute radiometric calibration, which a
traceable measurement provides and ours does not.

#### Recommendation

Obtain the manufacturer's IEC 62471 classification report for this model before
authorising routine internal use at maximum brightness. It is a document the
manufacturer should already hold, it is produced with traceable instrumentation
under the standard's own measurement conditions, and it settles the question at
lower cost than building a traceable measurement capability in-house.

**Interim control measure.** Pending that report, §4 shows the dimmed setting is
trivial across the band. We propose that routine work use the dimmed setting,
with full brightness restricted to `[specify: e.g. authorised short-duration
field use only]` until the manufacturer's report is on file.

---

## 4. Part 2 — Torch dimmed to 1/10 (18.8 W/m²)

The torch dims by analogue current control (§2.3), so the 1/10 setting delivers
18.8 W/m² continuously. Both hazards are assessed on that number, with no
peak-versus-average question and no pulsed-source treatment. The geometry is
identical to Part 1 — reducing the drive current does not move or resize the
die's image — so α = 54.99 mrad and ω = 3.025 msr carry over unchanged, as do
both exposure limits.

### 4.1 Results

| | Blue light (limit d) | Retinal thermal (limit g) |
|---|---|---|
| Weighted irradiance | E_B = 0.0188 W/m² | E_R = 18.8 W/m² |
| Measured radiance | L_B = 1.88 W/(m²·sr) | L_R = 6 215 W/(m²·sr) |
| Exposure limit | 100 W/(m²·sr) | 509.2 kW/(m²·sr) |
| Result | 1.88 % of limit (98.1 % headroom) | 1.22 % of limit (98.8 % headroom) |

Luminance is 1.04 × 10⁶ cd/m² (104× the ICNIRP screen), so the 3 mm limiting
aperture still applies.

Classification: Exempt Group. The Exempt/RG1 boundary at 1 000 W/m² is a factor
of 53 above the dimmed level.

### 4.2 Triviality screen across the uncertainty band

The ±20 % band of §2.5 applies unchanged, being a property of the measurement
rather than of the setting:

| | Irradiance | Blue light | Thermal | Binding | vs 20 % screen | Trivial? |
|---|---|---|---|---|---|---|
| Lower bound, −20 % | 15.0 W/m² | 1.50 % | 0.98 % | 1.50 % | 13.3× margin | Yes |
| Best estimate | 18.8 W/m² | 1.88 % | 1.22 % | 1.88 % | 10.6× margin | Yes |
| Upper bound, +20 % | 22.6 W/m² | 2.26 % | 1.46 % | 2.26 % | 8.9× margin | Yes |

The determination holds across the whole band, with 8.9× of margin at the
worst point. The measurement would have to be in error by a factor of
approximately 8 in the unfavourable direction to change the outcome, against
6.4 % for the full-brightness case (§3.7).

### 4.3 Conclusion

**LSO position.** We propose recording the torch at its 1/10 analogue setting as
a trivial source under guide §2.3, requiring no further assessment and no control
measures beyond ordinary sensible use. Per guide §747 the record need not be
elaborate; we recommend keeping one.

---
## 5. Part 3 — Device of our own construction (same emitter, similar optic)

We were asked whether this assessment can be extended to a device built in-house
using the same LED and a similar collimator, including an assembly carrying
several emitters behind a common objective.

Our position is that it cannot, and that this case requires external measurement.
The reasons are set out below.

### 5.1 The guide on "similar" sources

Guide §2.3, verbatim:

> Differences in, for example, the curvature of a reflector, the thickness of a
> glass cover or the manufacturer of a fluorescent lamp can have a considerable
> effect on the optical radiation produced by a source. Each example is therefore,
> strictly speaking, unique to the particular type and model of source which has
> been examined.

Optical similarity is therefore not equivalence. The two subsections below
quantify how far the result can move for this device.

### 5.2 Apparent source size: discontinuity at α = 11 mrad

The apparent source size is set by the collimator's magnification, and the
assessment is discontinuous in it.

Below α = 11 mrad, which at 200 mm corresponds to an apparent source of
2.200 mm, the standard expresses the blue-light limit as an irradiance rather
than a radiance. The margin changes by a factor of 100 across that boundary:

| Apparent source | Blue-light limit form | Measured vs limit | Group |
|---|---|---|---|
| 2.21 mm | radiance, 100 W/(m²·sr) | 18.8 % | Exempt |
| 2.19 mm | irradiance, 0.01 W/m² | 1 880 % | RG1 |

The step is not an artefact of our tool. The standard's two forms are
constructed to agree where the source's own solid angle is 10⁻⁴ sr
(100 W/(m²·sr) × 10⁻⁴ sr = 0.01 W/m²), i.e. at α = 10 mrad, within 21 % of the
actual 11 mrad switch point. The 100× step is the γ-averaging factor
(ω_γ / 10⁻⁴ sr = 0.01/0.0001 = 100): above the boundary a small source's power is
averaged over the 110 mrad field, diluting it 100-fold, and the standard does not
extrapolate that into a regime where it would understate the hazard. The step is
conservative at every point.

Consequence for an own-build: the measured torch has an 11 mm apparent source, a
factor of 5 above the boundary. That margin exists because the collimator
magnifies the ~1 mm die about 11×. A similar optic with a longer focal length
would image the die smaller while delivering the same or greater beam irradiance,
and could fall below the boundary. At fixed irradiance, smaller apparent sources
are the more hazardous ones, so tighter collimation at equal beam irradiance
increases the hazard. The magnifying collimator is part of what makes this torch
Exempt, and focal length is a safety-relevant parameter on any in-house build.

### 5.3 Multiple emitters: dependence on separation

For an assembly of several emitters behind one objective, the controlling
question is how the sources are treated. The guide's four-source worked example,
D.1.5 (a bank of four fluorescent lamps), states:

> The photopic effective irradiance was measured and is 1 788 mW m⁻². This was
> from four lamps: as each lamp is a separate visual source, each contributes
> 447 mW m⁻² to the total.

The same worked example applies both conventions:

| Hazard type | Treatment | Does separation matter? |
|---|---|---|
| Corneal (UV, IR) | irradiances add — the cornea intercepts everything. D.1.5 uses the four-lamp total for limits a and b. | No |
| Retinal | assessed per resolvable source — separate retinal images fall on different tissue and do not add. D.1.5 uses the per-lamp share for limits d and g. | Yes, for one of the two |

Applied to a four-emitter array of our LEDs, each delivering 188 W/m² (total
752 W/m² at a point), with all four separately visible:

| Treatment | Blue light | Retinal thermal | Group |
|---|---|---|---|
| (a) Per source — guide D.1.5 method | 18.8 % of limit | 12.2 % of limit | Exempt |
| (b) Merged into one 22 mm block | 62.1 % of limit | 22.2 % of limit | Exempt |
| (c) Total irradiance, one source's geometry | 75.2 % of limit | 48.8 % of limit | Exempt |

All three are Exempt, but the blue-light figure spans a factor of four according
to the choice of divisor. Two results explain the spread:

- **Retinal thermal is nearly independent of separation.** Radiance is not
  additive for sources side by side: tiling four gives 4× the flux over 4× the
  area, leaving the radiance unchanged (verified exactly). Only α grows, and it
  clamps at 100 mrad, which caps the entire effect at the clamp ratio of 1.82×
  for any number of emitters in any arrangement.
- **Blue light does depend on separation**, because ω_B is pinned at the
  γ-derived 0.01 sr and does not grow with the source. A single 11 mm emitter
  fills 0.30 of that field, leaving 3.3× of spare capacity for additional
  emitters. The effect is bounded at that 3.3×, since an average over a field
  cannot exceed the peak radiance within it.

The relevant separation is 20 mm centre-to-centre at 200 mm (a 100 mrad angular
pitch, the γ field's own size). Below it the emitters share the photochemical
averaging field and the blue-light figure rises; at and above it only one emitter
can occupy the field at a time and separation ceases to matter.

Treatment (c) returns L_B = 75.2 W/(m²·sr), above the emitters' own radiance of
62.1 W/(m²·sr), which is physically unattainable. This is the cost of the guide's
stated "err on the side of caution" shortcut (§2087) rather than an error, and
indicates that a field-restricted measurement would recover real margin.

### 5.4 Triviality screen and proposal

Guide §6.2 pro-rates the triviality threshold by the number of sources a worker
faces:

> For a single source, if the exposure at the location of the worker is less than
> 20 % of the ELV for a full working day, then it might be considered trivial.
> However, if there are 10 such sources, then the exposure from each source would
> need to be less than 2 % of the ELV to be considered trivial.

For four sources the pro-rata threshold is 20 % / 4 = 5 % per source. With the
§2.5 uncertainty band applied:

| Configuration | Per source, best estimate | At +20 % | Threshold | Verdict |
|---|---|---|---|---|
| Four emitters at full power | 18.8 % (3.8× over) | 22.6 % (4.5× over) | 5 % | Not trivial at either end of the band |
| Four emitters at 1/10 setting | 1.88 % (2.7× margin) | 2.26 % (2.2× margin) | 5 % | Passes across the band |

At full power the array exceeds the triviality threshold by a factor of 3.8 at
the best estimate and 4.5 at the upper bound, while every treatment still
classifies as Exempt Group. The dimmed array passes across the band, but we do
not propose relying on that, for three reasons:

1. **Compounding uncertainty.** The §2.5 band applies to each emitter, and an
   array multiplies the opportunities for a hot spot, a mis-set unit or an
   unequal battery state. The 2.2× margin at the upper bound is not large against
   that.
2. **Arrangement dependence.** Spacing below 20 mm pitch changes the blue-light
   figure by up to 3.3×, and apparent source size has the 100× discontinuity of
   §5.2. Neither parameter can be held or verified to the required confidence on
   an in-house build.
3. **Proximity to the Exempt threshold.** The packed-array Exempt threshold is
   302 W/m² per emitter, 1.6× above the measured 188 W/m². Drive current is a
   parameter liable to be raised on an in-house build without a safety review.

**Recommendation.** Before any multi-emitter assembly is put into use, engage an
external laboratory with traceable instrumentation to measure the completed
assembly as built. We would request specifically:

- a beam map establishing the true peak irradiance rather than a single-point
  reading;
- the apparent source size of the actual optic as built;
- the emitter spacing as assembled, against the 20 mm criterion of §5.3;
- a stated measurement uncertainty, so that the triviality determination can be
  made robustly across the band rather than marginally (the limitation identified
  in §3.7).

We would supply this report and our calculation record as background, and have
the laboratory's result supersede them.

---

## 6. Summary of LSO conclusions

| # | Configuration | IEC 62471 group | Trivial per guide? | LSO position |
|---|---|---|---|---|
| 1 | Torch, full brightness (188 W/m² ± 20 %) | Exempt (across band) | Not across the band — 18.8 % best estimate, 22.6 % at +20 %, vs a 20 % screen | Our measurement does not determine this. Obtain the manufacturer's IEC 62471 report before authorising routine use at maximum brightness. Interim: use the dimmed setting. |
| 2 | Torch, 1/10 analogue (18.8 W/m²) | Exempt (across band) | Yes — 1.88 % best estimate, 2.26 % at +20 %, margin 8.9× at the worst point | Record as a trivial source. No further action. |
| 3 | Own-build, multiple emitters, full power | Exempt | No — 18.8 % per source vs 5 % pro-rata, 3.8× over at best estimate | Seek external advice. External laboratory measurement with traceable instrumentation on the completed assembly. |

In all three cases our position is to follow the guide's advice rather than to
rely on our own instrumentation at the margins.

---

## 7. Questions for the RSA

1. Do you accept the 20 % / pro-rata triviality criterion (guide §2.3, §6.2) as
   the applicable gate for these decisions, given that all configurations are
   Exempt Group under IEC 62471?
2. **Part 1.** Do you agree that a determination whose outcome changes within the
   stated measurement uncertainty (§3.7: 18.8 % best estimate, 22.6 % at +20 %,
   against a 20 % screen) should be treated as unresolved rather than as a pass
   on the best estimate? And is the manufacturer's IEC 62471 report the
   appropriate remedy, rather than our attempting a ±6.4 % measurement?
3. **Uncertainty treatment.** We have taken ±20 % as a k = 2 expanded uncertainty
   on a 10.4 % standard uncertainty (§2.5), with the battery term absorbed rather
   than characterised. Would you expect the battery contribution to be measured
   separately, and would you combine the terms in quadrature as we have?
4. **Part 3.** For a multi-emitter assembly, which of treatments (a), (b) or (c)
   in §5.3 would you expect a test house to apply, and would you specify a
   minimum emitter pitch (we calculate 20 mm at 200 mm) as a design requirement?
5. **Limit g.** We compute the retinal-thermal limit from the formula
   (2.8×10⁷/C_α = 509 kW/(m²·sr) at α = 55 mrad) rather than transcribing the
   280 kW/(m²·sr) that recurs in the guide's Appendix D tables (Appendix C.1).
   Do you concur? The verdict is unaffected either way.
6. Is there any aspect of the method in §2 that you would want re-done before
   countersigning the Part 2 triviality determination?

---

## Appendix A — Glossary

| Term | Meaning |
|---|---|
| **α** (alpha) | *Angular subtense* — the angular width of the apparent source, in radians or milliradians. Larger α gives a larger retinal image. |
| **ω** (omega) | *Solid angle* — the two-dimensional analogue of an angle, in steradians (sr). Equals source area ÷ distance². |
| **γ** (gamma) | *Measurement field of view* — the cone the instrument averages over. Fixed by the Directive per hazard: 110 mrad photochemical, 11 mrad thermal. |
| **Irradiance (E)** | Power arriving per unit area at the eye, W/m². The measured quantity. |
| **Radiance (L)** | Power leaving the source per unit area per unit solid angle, W/(m²·sr). The quantity the retinal limits use. L = E/ω. |
| **B(λ)** | Blue-light weighting, modelling photochemical retinal injury. Peaks ~435–440 nm. |
| **R(λ)** | Retinal thermal weighting, modelling thermal retinal injury, 380–1400 nm. |
| **V(λ)** | Photopic luminous efficiency — the eye's brightness response. Not a hazard weighting. |
| **C_α** | α in mrad, clamped to [1.7, 100]. Scales the thermal limit as 2.8×10⁷/C_α. |
| **ELV** | Exposure Limit Value — the Directive's legal limit. |
| **Limit d** | Blue-light (photochemical) retinal limit for a large source: 100 W/(m²·sr) for exposures over 10 000 s. |
| **Limit g** | Retinal thermal limit: 2.8×10⁷/C_α W/(m²·sr) for exposures over 10 s. |
| **Exempt Group** | IEC 62471's least restrictive class — no photobiological hazard under foreseeable conditions. |
| **Trivial source** | The guide's risk-assessment category: exposure below ≈20 % of the ELV, pro-rated by source count. A stricter gate than Exempt Group. |
| **Standard uncertainty** | A measurement uncertainty expressed as one standard deviation. |
| **Expanded uncertainty / k** | Standard uncertainty multiplied by a coverage factor k. k = 2 gives approximately 95 % confidence. |
| **Traceable** | Calibrated against a national measurement standard through an unbroken documented chain. Our measurement is not. |

## Appendix B — Formulas used, with citations

| Quantity | Formula | Source |
|---|---|---|
| Angular subtense | α = 2·arctan(s / 2d) | geometry; exact form, not the small-angle approximation |
| Non-circular source | clamp each axis to [α_min, α_max] *then* average | IEC 62471 §4.2.2 (order is specified) |
| α_min, α_max | 1.7 mrad, 100 mrad | IEC 62471 §4.2.2 |
| Solid angle | ω = A / d² | definition |
| Averaging solid angle | ω_used = max(ω_source, ω_γ) | guide §2093–2095 |
| ω_γ | 0.01 sr (γ=110 mrad, limit d); 0.0001 sr (γ=11 mrad, limit g) | Directive Table 2.5, as quoted in the guide |
| Radiance | L = E / ω | definition |
| Weighted irradiance | E_w = Σ E_λ(λ)·W(λ)·Δλ | IEC 62471 §5.3.2 |
| Limit d (α ≥ 11 mrad) | L_B ≤ 10⁶/t for t ≤ 10 000 s; 100 W/(m²·sr) above | Directive Annex I (c)/(d), IEC 62471 Eq. 4.5 |
| Limit d (α < 11 mrad) | E_B ≤ 100/t W/m² for t ≤ 10 000 s; 0.01 W/m² above | Directive Annex I (e)/(f), IEC 62471 Eq. 4.7 |
| Limit g | L_R ≤ 2.8×10⁷/C_α for t > 10 s | Directive Annex I (g), IEC 62471 Eq. 4.9 |
| Limiting aperture | 3 mm if L_v > 10 cd/m² and t > 0.25 s; else 7 mm | IEC 62471 §4.2.1 |
| Luminance | L_v = 683·E_v / ω | guide §2049 |
| Triviality screen | < ≈20 % of ELV, single source; pro-rata by source count | guide §2.3, §6.2 |
| Uncertainty combination | u = √(Σ u_i²); U = k·u, k = 2 | standard metrological practice |

**Source of ω_γ.** The Directive states ω_γ = 0.01 sr and 0.0001 sr to one
significant figure. Deriving them geometrically from the stated field angles
gives πγ²/4 = 0.0095 sr and 0.000095 sr. We use the stated values throughout, on
the basis that ω_γ is a constant defined by the standard rather than a property
of the torch to be re-derived to higher precision than the regulator states it.

## Appendix C — Limitations, caveats and known issues

### C.1 Limit g computed rather than transcribed from the guide's tables

The guide's Appendix D comparison tables state limit g as 280 kW/(m²·sr). We
compute 509 kW/(m²·sr) for α = 55 mrad.

Both are consistent with the same formula. 2.8×10⁷/C_α gives exactly 280 kW only
when C_α = 100 mrad, i.e. for sources at or beyond the clamp ceiling. The guide's
examples that quote 280 kW and have α past 100 mrad (D.1.5 at 295 mrad, D.1.12 at
110 mrad, D.1.21 at 575 mrad) agree with our tool exactly. Two examples (D.1.15
and D.1.16, both data projectors at α = 20 mrad) also state 280 kW, where the
formula gives 1 400 kW; we take that to be a transcription or OCR artefact in
that document, since the same constant cannot hold across a 29× range of the one
variable it depends on.

The verdict is unaffected by the discrepancy. At full brightness our L_R is
12.2 % of our computed 509 kW and 22.2 % of the guide's 280 kW — Exempt either
way, and below the 20 % screen on the thermal criterion under our figure though
marginally over it under the guide's. The thermal criterion is not the binding
one in any configuration (blue light is), so no conclusion in §6 is affected. The
dimmed torch is at 1.22 % and 2.22 % respectively.

### C.2 Not implemented in our tool

- Multiple-pulse criteria for repetitively pulsed sources. Not required here,
  because the dimmer is analogue (§2.3); it would be required for a PWM-dimmed
  variant.
- Ultrashort-pulse retinal-thermal brackets; the IRA-only short-pulse bracket.
- The "IR hazard without a strong visual stimulus" criterion — not applicable to
  a visible red source, noted for completeness.
- No photometric V(λ) table. The CIE 1924 values used in §3.2 were transcribed
  into the calculation record from the published table, not taken from the tool.

### C.3 Defect in our tool, not affecting these results

Our tool's unit-checking wrapper for the irradiance→radiance conversion documents
that it validates its solid-angle argument. It does not: it accepts milliradian
and degrees silently, because the unit library treats steradian and radian alike
as dimensionless. Supplying `3.025 mrad` where `3.025 msr` was meant gives the
correct answer (the milli- prefixes coincide); supplying degrees returns a
silently wrong number.

These results are unaffected: ω was derived in steradian from first principles
(§3.1) and the guard was not relied on. The defect is on our register to fix.

### C.4 Terminology corrections from our working notes

Rev. 1 working notes recorded the irradiance as "a radiance" and the solid angle
in "mrad". Both numbers were correct; both unit labels were wrong:

- W/m² is an irradiance, not a radiance. A radiance is W/(m²·sr) and is derived
  by dividing by the source's solid angle. Reading the irradiance figure as a
  radiance directly would understate the retinal-thermal quantity by 331×.
- ω = 3.025 is in millisteradian (msr), not milliradian. ω is a solid angle;
  mrad is a plane angle.

### C.5 Provenance of the calculation

Calculations were performed with an in-house tool
(`ray_tracing_shapely.optical_elements.eye_safety`). It has been checked against
five of the guide's Appendix D worked examples (D.1.5, D.1.12, D.1.15, D.1.16,
D.1.21), reproducing every stated limit value exactly except the limit-g figure
discussed in C.1. It has not been validated against a reference laboratory and
is not accredited. The full calculation record, including the executed derivation
of every number in this report and the uncertainty analysis of §2.5, is available
as `eye_safety_red_led_torch_didactic.ipynb` and can be supplied on request.

## Appendix D — Measurement uncertainty, itemised

§2.5 states the budget and its consequences. This appendix records the individual
contributions, including those absorbed into the ±20 % band.

| Source of uncertainty | Estimated effect | Direction | Affects |
|---|---|---|---|
| Alignment and positioning repeatability | ± 10 % | either | both criteria, proportionally |
| Detector calibration on the reading | ± 3 % | either | both criteria, proportionally |
| Torch battery state of charge | not separately quantified | systematic, unknown | both criteria, proportionally |
| Absolute radiometric calibration, non-traceable | `[to be established]` | unknown systematic | both criteria, proportionally |
| Single-point measurement; beam peak not mapped | not included in the ± 20 % | understates | both criteria, proportionally |
| Die thermal state at measurement | 10–20 % | likely understates | both criteria |
| Detector spectral responsivity at 632 nm | `[to be established]` | unknown | both criteria |
| Apparent source size, visual estimate "about 11 mm" | ± 20 % | either | retinal thermal only — see §2.5 |
| Measurement distance | ± 2 % | either | both, weakly |
| Monochromatic treatment of the LED | 0.00 % | — | neither (see §2.4) |

Two items are outside the ±20 % band. The single-point measurement (the beam peak
has not been mapped) and the die thermal state are procedural gaps rather than
instrument uncertainties, and both act in the same direction: 188 W/m² is more
likely to understate the worst-case peak than to overstate it. The true value is
therefore, if anything, more likely to sit in the upper half of the band, where
the triviality screen of §3.7 is not satisfied.

Recommended improvements, in priority order, should the question need to be
settled in-house:

1. Map the beam to find the true peak rather than sampling one point. This is the
   largest unquantified gap and costs only time.
2. Obtain a traceable calibration for the detector, or borrow a calibrated
   instrument. This is the binding constraint on the ±6.4 % requirement.
3. Characterise the battery-state contribution by measuring at full and depleted
   charge. Low cost, but per §3.7 not sufficient: eliminating it entirely still
   leaves ≈21 % expanded uncertainty.
4. Measure at a controlled die temperature, or state the warm-up condition.

Items 1 and 2 together would be needed to approach ±6.4 %; item 3 alone would not
change any conclusion. This is why §3.7 recommends obtaining the manufacturer's
report rather than pursuing this list.

---

*Prepared by `[name]`, Laser Safety Officer, `[company]`. Calculation record:*
*`notebooks/eye_safety_red_led_torch_didactic.ipynb`. Supersedes Rev. 1.*
