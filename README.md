# 본드수 계산기

두 유체의 밀도차에 따른 중력 효과와 계면장력 효과의 크기 비를 계산합니다.

- ID: E133
- App: https://nanalab.kr/eng-bond-number/
- Repository: https://github.com/NaNaCompany/eng-bond-number
- Formula: Bo = |ρ₁ − ρ₂|gL² / σ

## Model and data

서로 섞이지 않는 두 유체의 일정한 밀도와 계면장력을 사용합니다. 출력은 밀도차의 절댓값을 사용한 비음수 크기입니다. 상하 배치에 따른 계면 안정성이나 모양을 판정하지 않습니다.

Inputs normalize to SI. Repeated-input models support adding/removing actual input rows. Calculations, finite-number checks and physical-domain checks run locally; no external property database or solver API is used.

## Validation

Run node --test tests/*.test.mjs and python scripts/build-locales.py --check. tests/reference.json contains independently computed high-precision default and boundary references. The source notices distinguish original MIT work from citation-only external references.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.
