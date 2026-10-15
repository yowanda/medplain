# MedPlain — Devpost write-up

## Elevator pitch

Understand your lab results, in plain language. MedPlain turns a lab report
full of jargon into clear per-line explanations — plus 3 questions to ask
your doctor.

## Inspiration

A friend received a lipid panel, saw "LDL 165" and "HDL 38", and had no idea
what any of it meant — or what to ask at the follow-up. Lab portals hand
patients numbers without understanding. The gap is not more data; it is
translation. MedPlain closes it.

## What it does

Paste a lab result or prescription, or tap a sample (CBC, Cholesterol / Lipid
Panel, Blood Sugar HbA1c, Prescription). Every line becomes a card: your value
vs the typical range, a visual range bar, a plain-language "What this means",
and a flag. Unknown lines are skipped, never guessed. Then 3 questions for
your doctor, generated from the flagged lines, with a copy button. A 12-term
glossary explains jargon like HDL, LDL, and HbA1c in plain English. A print
button produces a clean handout.

## How we built it

Single-file HTML + CSS + vanilla JavaScript. Zero install, no backend.
Demo mode runs on a built-in rule parser, so it works with no key. Live mode
adds an optional Gemini key for AI explanations, with silent fallback to the
rule parser on any error. Keys live in browser localStorage only.

## Challenges we ran into

The hardest part was what NOT to say. A health explainer must never sound
like a diagnosis, so every explanation uses "above/below the typical range —
ask your doctor what it means for you" phrasing, and the app refuses to name
conditions or recommend treatment. We verified this by scanning the whole
file for diagnosis and treatment phrasing.

## Accomplishments that we're proud of

A health tool that is genuinely useful and genuinely honest: patients leave
understanding their numbers and knowing what to ask, without ever being told
they have a condition.

## What we learned

In health, clarity is a safety feature. Plain language is not dumbing down —
it is the difference between a patient who can advocate for themselves and
one who cannot.

## What's next for MedPlain

More report types (imaging summaries, discharge notes), multilingual
explanations, and a clinician-reviewed explanation library.

## Built with

HTML, CSS, JavaScript, Google Gemini
