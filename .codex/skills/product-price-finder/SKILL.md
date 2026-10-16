---
name: product-price-finder
description: Search and compare online prices for any product, prioritizing delivery to Switzerland and checking Europe-wide options. Calculate realistic landed cost including shipping, import VAT/customs where applicable, and provide direct retailer links. Use when the user asks to find the cheapest price, compare stores, check a product deal, or compare cosmetics, watches, jewelry, fashion, electronics, or other goods.
---

# Product Price Finder — 全网商品比价

## Mission
When the user names a product, gives a product URL, or supplies an image, research current online listings and identify the lowest credible total cost for delivery to Switzerland. Search Switzerland first, then nearby/European stores that explicitly ship to Switzerland, then wider international sellers only when useful. Never claim to have checked the entire internet; describe the lowest price found among sources checked.

## Defaults
- Delivery destination: Switzerland. Ask for postal code only if it materially affects shipping; otherwise state the shipping assumption.
- Currency: CHF first; preserve original currency and state exchange-rate assumption/date when converting.
- Condition: new and genuine by default. Separate new, refurbished, pre-owned, open-box, and grey-market listings.
- Rank by lowest credible delivered price, not lowest headline price.
- Answer in Chinese unless asked otherwise.
- Accept scope modifiers such as “只看瑞士”, “只看欧洲”, “只看官方/授权店”, or a budget.

## Research workflow
1. Identify exact product: brand, name, model/SKU/reference, size, shade, volume, material, color, version, condition as relevant. Ask one concise question only if ambiguity materially changes results.
2. Search live web across Swiss official sites, authorized retailers, reputable Swiss stores and marketplaces; European official sites and reputable stores that ship to Switzerland; and international sellers only when delivery, authenticity, warranty, and import charges can be assessed. Search English, German, French, and Italian terms when useful.
3. Verify each product page: exact variant, current price, stock, seller identity, condition, direct URL, shipping to Switzerland, free-shipping threshold, delivery estimate, returns, and warranty.
4. Calculate estimated landed cost: discounted item price + shipping + mandatory handling + applicable import VAT/duties. Convert to CHF with a stated exchange-rate assumption. If a fee is unknown, label it “未确认”; never silently count it as zero.
5. Rank by estimated total cost to Switzerland. Distinguish lowest confirmed delivered total, lowest headline price, and best/safest purchase.
6. State date/time checked. If prices are behind login, geo-blocked, personalized, or dynamically rendered, disclose this. Search broader if initial coverage is weak.
7. Never claim “全欧洲/全网绝对最低”; say “在本次核查的网站中最低”.

## Category checks
### Cosmetics and skincare
Match exact product, shade, size and volume. Compare official brands, pharmacies, beauty retailers, department stores and reputable discounters. Check authenticity, sealed condition, seller identity and Switzerland shipping restrictions.

### Watches
Match exact reference, dial, bracelet/strap, size, movement and condition. Separate authorized dealers, grey-market and pre-owned. State manufacturer vs seller warranty, return policy, seller location and authenticity documentation. Flag implausibly low prices.

### Jewelry and luxury
Match reference, metal, stones/specification, size, color and condition. Separate official retail, authorized resale and pre-owned. Never present replicas, counterfeits, or “inspired by” goods as equivalent. Flag authentication, insured shipping, returns and warranty concerns.

### Other products
Match model, regional version, plug/voltage, dimensions, accessories, warranty and condition. Do not compare unlike bundles.

## Swiss cross-border taxes
- Check current Swiss Federal Office for Customs and Border Security (FOCBS/BAZG) and official tax guidance when estimating import VAT, customs, or postal/courier handling.
- Separate carrier clearance fees from tax/duty.
- Avoid double-counting Swiss VAT if the retailer explicitly collects it at checkout.
- If official rules or carrier fees cannot be verified, mark “到货税费/清关费待确认” rather than inventing a precise total.
- Never assume tourist VAT refunds apply to goods shipped to Switzerland; eligibility depends on country, export process, residency and retailer rules.

## Required output
Start with the cheapest credible option found and its estimated total delivered to Switzerland.

Use a comparison table:
| Rank | Store/country | Exact product & condition | Item price | Shipping | Estimated import/handling | Estimated total CHF | Stock/delivery | Warranty/returns | Direct link | Confidence |

Use “已确认”, “估算”, or “待确认” for price/fee confidence. Link directly to product pages. After the table, include:
- **推荐购买**: best overall option and why.
- **最低标价 vs 最低到手价**: explain differences.
- **风险提示**: authenticity, warranty, returns, shipping, taxes, currency.
- **核查时间**: date/time and sources checked.
- **下一步**: one concise question only if needed.

## Quality and safety
- Use live search and cite/link sources for prices, shipping, tax rules and retailer claims.
- Never invent shops, prices, discounts, shipping fees, stock, or delivery dates.
- Do not purchase, create accounts, or enter payment details.
- Clearly distinguish verified facts, estimates, and assumptions.
