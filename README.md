# MedPlain — Understand your lab results, in plain language

Paste a lab result or prescription, get every line explained in plain English,
plus 3 questions to ask your doctor. Built for the UnivaBio hackathon
(AI for Human Health).

## The flow

1. **Paste:** paste a lab result, or tap a sample (CBC, Cholesterol / Lipid
   Panel, Blood Sugar HbA1c, Prescription).
2. **Understand:** per-line cards — your value vs the typical range, a visual
   range bar, a plain-language "What this means", and a flag
   (In / Above / Below typical range). Unknown lines are skipped, never guessed.
3. **Ask:** 3 questions for your doctor, generated from the flagged lines,
   with a copy button.
4. **Learn:** glossary of 12 medical terms in plain English.
5. **Print:** print / save-as-PDF button.

## Safety

Educational information only — not medical advice, diagnosis, or treatment.
A disclaimer banner appears on every screen. The app never names a condition
and never recommends treatment. If you feel seriously unwell, seek urgent care.

## Modes

- **Demo mode (default):** built-in rule parser. Works fully with no key.
- **Live mode:** optional Gemini API key (localStorage only) for AI
  explanations; any error falls back silently to the rule parser.

## Run it

Open `index.html` in any browser. Zero install, no build step, no backend.

## Live demo

https://yowanda.github.io/medplain/

## Privacy

No user data leaves the browser except the optional Gemini request. No
tracking, no account. Pasted text is escaped before display, so pasted
content is never executed as code.
