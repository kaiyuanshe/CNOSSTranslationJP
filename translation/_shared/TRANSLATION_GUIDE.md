# Chinese Government and Public-Policy Document Translation Guide

This guide defines reusable rules for publishing Japanese translations of Chinese government and public-policy documents in this repository.

## Source policy

- Treat the original Chinese document as authoritative.
- Use an official web publication to confirm metadata such as issuing bodies, issue date, and document number.
- Do not use an English translation as the primary source.
- Do not guess missing or illegible text. Record unresolved source problems explicitly.
- Extract embedded PDF text before considering OCR. Use OCR only when ordinary extraction fails, and disclose its use.

## Source transcription

- Preserve the source title, headings, hierarchy, numbered items, policy names, document references, organization names, dates, figures, units, and percentages.
- Remove only layout artifacts such as page numbers, line-wrap breaks, and spaces inserted between Chinese characters.
- Preserve paragraph boundaries and punctuation. Do not rewrite, summarize, modernize, or silently correct the Chinese source.
- Compare the cleaned transcription with rendered pages and, where available, the official HTML publication.

## Japanese style

- Use natural, formal Japanese suitable for a published policy document.
- Preserve the original hierarchy and numbering.
- Avoid word-for-word Chinese constructions when they are unnatural in Japanese, but do not soften, strengthen, omit, or reinterpret the policy meaning.
- Preserve ideological and political wording faithfully and neutrally.
- Keep all figures, units, dates, percentages, document references, and proper names consistent with the source.
- Use Japanese punctuation and typography consistently. Retain the source's full-width corner brackets for named documents.
- Avoid Simplified Chinese in the Japanese body except where required for an official name, a source citation, or an explicitly identified original title.

## Terminology

- Use `translation/_shared/glossary.tsv` as the source of truth for recurring terms.
- Do not silently change entries marked `confirmed`.
- Add important missing terms as `needs-review`, with a concise note describing the uncertainty or intended context.
- Translate `工业和信息化部` and `工信部` as `工業情報化部`.
- Prefer natural policy language over slogan-like literal expressions. For example, choose `現場導入` or `実用化` for `落地` according to context, and `エコシステム` for `生态` when it denotes an industry ecosystem.

## Explanations for Japanese readers

- Add an explanation only when a China-specific administrative, legal, industrial-policy, or technical term would otherwise be unclear.
- Keep explanations short, factual, and neutral. Do not add political commentary.
- Clearly separate any added note from the source text using:

  > **日本語版注：**

- Do not present editorial context as part of the original document.
- Explain the concrete mechanism rather than reproducing an opaque slogan. For automotive policy, terms that may need brief context include smart connected vehicles, vehicle-road-cloud integration, V2X, OTA updates, battery swapping, vehicle-grid interaction, and carbon-footprint accounting.

## Publication metadata

- Each translation directory should include a README listing the Chinese and Japanese titles, issuing bodies, issue date, confirmed document number, authoritative source, local files, status, credits, and authorization status.
- State that the Japanese translation is unofficial unless official authorization has been confirmed.

## Validation and review

- Compare Arabic numerals, percentages, years, units, and document reference numbers between the Chinese and Japanese files.
- Check that all headings and numbered items are present and in order.
- Search the Japanese body for remaining Simplified Chinese and review each occurrence.
- Validate relative Markdown links and ensure every glossary row has exactly five tab-separated columns.
- Review the complete diff before committing. Do not commit, push, or open a pull request until explicitly requested.
