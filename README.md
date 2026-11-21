# cloud-itonami-isco-2434
Occupation reference: ISCO-08 (International Labour Organization, 2012), code 2434. This app is not produced, reviewed or endorsed by the ILO.
職業の参照: ISCO-08（国際労働機関 ILO、2012 年）のコード 2434。日本語の名称は当方の訳です。この app は ILO が作成・確認・推奨したものではありません。

Open Business Blueprint for **ISCO-08 2434**: Information and Communications Technology Sales Professionals — an ISCO
**Wave 0 (cognitive substrate)** occupation per ADR-2607121000:
pure-cognitive work, the LLM-first wave, **no robotics gate** —
eligible for actor implementation now.

**Maturity: `:implemented`** — ICTSalesAdvisor ⊣ ICTSalesGovernor as a
langgraph StateGraph (`intake → advise → govern → decide →
commit/hold`, human-approval interrupt), modeled on
cloud-itonami-isco-4311's bookkeeping actor. 13 tests / 27 assertions
green.

The licensing-quote HARD invariants — arithmetic and matrix lookup,
not a sales pitch:

1. **Seat-count ceiling** — the proposed seat count must not exceed
   the bundle's registered max-seats.
2. **Component compatibility** — every proposed component must be a
   member of the bundle's registered compatible-components set — an
   incompatible bundle is a matrix lookup, not a sales pitch.

Also HARD: unregistered/foreign bundle, unregistered organization,
non-`:propose` effect. Escalations (always human sign-off):
`:approve-enterprise-quote` (large-account commitment), low confidence
(< 0.6).

AGPL-3.0-or-later, forkable by any qualified operator. Part of the
[cloud-itonami](https://itonami.cloud) open business fleet.
