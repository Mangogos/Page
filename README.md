# Equipment Procurement Analysis

## What this is
一个可复用的设备更换/采购决策框架（不是某个具体行业案例）：当组织同时面对「修 vs 换 vs 买新」
时，用统一口径（NPV, opportunity cost, depreciation, residual value）比较三个方案：

- **Option 1** — Repair Equipment B + Dispose Equipment A + Acquire Equipment C
- **Option 2** — Dispose Equipment B + Keep Equipment A + Acquire Equipment C
- **Option 3** — Repair Equipment B + Keep Equipment A (no new acquisition)

Equipment C 内部再拆两层独立子决策：cash vs financing acquisition，Type 1 vs Type 2 configuration.

## Files
- `equipment-procurement-framework.html` — the explainer page (Drive-viewer-safe: no external
  font CDN, system font stacks only — the Weee artifact viewer sandboxes the iframe with no
  network access, so any external `<link>`/`<script src>` would silently fail).

## Status (as of 2026-09-23)
框架/方法论已定义完整，**尚未填入实际数字**。跑真正的 5yr/7yr NPV 对比、break-even 和
sensitivity analysis 需要以下输入（还没提供）：

- Equipment A: resale/disposal value, remaining useful life, annual maintenance/operating cost
- Equipment B: repair cost (quoted $3,500–$4,000), post-repair useful life, post-repair annual cost
- Equipment C (Type 1 & Type 2): purchase price, annual operating/maintenance cost, useful life, residual value at 5yr/7yr
- Financing terms: down payment, interest rate, loan term
- Organization's opportunity cost of capital / discount rate

## Judgment calls
- **Anonymization is deliberate and required by the user** — no references to any specific
  real-world industry, vehicle/transportation terms, brands, or personal financial details.
  Only generic terms (Equipment A/B/C, Acquisition, Financing, Residual Value, etc.).
- This explainer page is 中英夹杂 per the user's explicit request for this artifact. Once real
  numbers are supplied and the actual comparison tables/charts are built, confirm with the user
  whether those follow the same mixed-language style or go full English.

## How to rebuild / update
This is a static, self-contained HTML file — no build step. To update:
1. Edit the HTML directly (or regenerate via Claude).
2. Overwrite this same file at this same path (`equipment-procurement-framework.html`) so the
   Drive `fileId` — and therefore any link already shared — stays valid. Do not delete and
   recreate, and do not publish a "v2" file alongside it.
