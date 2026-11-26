# Breltz Bags: Return-Aware Growth (one-pager)

**The real problem.** Breltz says "returns are 30% and eating margin". The data on the call points somewhere else. Returns are a symptom of a **promise gap**: what ads and listings promise about size, laptop fit and colour is not what arrives. The growth engine then amplifies the gap. Meta only receives the purchase event, so it keeps scaling the creatives that over-promise. Free returns remove the cost of buying the wrong thing. Data sits in 4–6 systems, so Farhan, Pooja and Sneha each argue from a different gut feeling.

**Evidence from the call**
- "30%" mixes RTO (COD refusals, ~6% of website orders) with customer-initiated returns (21–22%). The fixes tried so far (₹49 COD fee, pincode exclusion) only touch RTO. [02:15, 02:32]
- **It's not quality:** 75–80% of Commuter returns are Grade A (unused), only 4–5% are transit damage, and stricter vendor QC changed nothing. [06:56, 13:57]
- **Ads over-promise:** the "16-inch" overlay (spec is 15.6") was added in March; the 5× hero video uses a petite creator and probably a 13" laptop; tickets say "mine doesn't fit like that". Returns rose around April, as Commuter ads were scaled hard. [10:15–10:50, 04:29]
- **Colour:** Sage and Dusty Rose have the highest return %; the Dusty Rose paid ad is a golden-hour, filtered reel. [11:06–11:30, 14:09]
- **Channel gap:** Amazon (size-with-person image, 2,400 reviews) returns 13–14%. Website (cm in a hidden tab, PDF size guide) 21–22%. Myntra (stale v1 photos, "30 L" title) 31%. [03:05, 12:41, 13:11]
- **Meta never learns about returns**, and no one joins ad → order → return → reason. [09:12, 14:44]
- Free returns raised conversion 18% but their effect on returns was "never looked at separately"; shoppers bracket two colours in sales. [11:50, 12:18]

**Options considered**

| Option | Verdict |
|---|---|
| Paid returns | Hits bracketing only, gives up the 18% conversion gain; CEO won't trade growth |
| Vendor / QC work | Ruled out by Grade-A data; already tried |
| COD fees, pincode blocks | RTO only; already tried, hurt conversion |
| Cut ad spend | Explicitly ruled out |
| Dashboard only | Insight with no action |
| Content fixes only | Fast, but nothing stops the next bad creative or fixes Meta's optimisation |
| **Closed loop: Measure → Diagnose → Prevent → Optimise → Recover** | **Chosen:** addresses every root cause and gives each stakeholder an outcome |

**Solution (prototype in `index.html`)**
1. **Returns command center:** join Shopify, returns sheet, Freshdesk, Meta and creator codes on order ID; AI-tag ticket text into real reasons; split RTO from customer returns; cut by SKU, colour, channel, ad, first-time vs repeat.
2. **Net-ROAS scorecard:** rank ads after returns and logistics, so scale/kill rules use profit.
3. **Claim checker and listing monitor:** check ad copy and every channel's listing against one product spec before they go live.
4. **Meta CAPI feedback** (roadmap): return-adjusted value so Advantage+ stops favouring buyers who return.
5. **Smart return flow:** structured reason, fit help, colour exchange, bracketing detection, with save and exchange outcomes.

**What I would measure**
- North star: website customer-initiated returns 21–22% → below 12% in two quarters. Business: contribution margin 9% → at least 18%.
- Guardrails: website conversion and revenue growth stay flat or up.
- Leading indicators: Grade-A return share, "fit" and "colour" reason share, Myntra Commuter return rate after the listing fix, net-vs-Meta ROAS gap, save rate in the return flow, share of returns with a structured reason, share of orders joined to an ad.
- Validation: A/B test the size image on the product page; holdout the corrected creatives; before/after on the Myntra listing and the "16-inch" copy.

**Risks and assumptions.** All prototype numbers are illustrative; real ones come after the data join. Attribution stays partial (~40% of Shopify orders have a source), so use a waterfall of creator code, then UTM, then Meta click ID, then survey, with confidence labels. The causal link from "16-inch" and filtered reels to returns still has to be confirmed on real data. Reaching 12% may also need the policy lever.
