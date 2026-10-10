# ChongZhou Sun — WordPress / WooCommerce Developer

WordPress plugin author & troubleshooter. 10 years of frontend engineering (Vue/React), now focused on WordPress full-stack work: plugin diagnostics, WooCommerce fixes, performance and security.

**Public track record:** active contributor on [WordPress.org support forums](https://profiles.wordpress.org/sunchongzhou2026/) · resolved threads with client testimonials below.

---

## ✅ Case Study #001 — Database error blocking all plugin updates (Resolved ✓)

**Client:** WooCommerce store owner (WordPress.org user @haarbollen)
**Forum thread:** https://wordpress.org/support/topic/database-error-435/

**Problem:** Every plugin update failed with a MySQL error — `The SELECT would examine more than MAX_JOIN_SIZE rows` — and the error also appeared on the dashboard. The client's hosting provider could not figure it out.

**Diagnosis:** Instead of treating it as a hosting limit, I read the raw failing SQL. The `WHERE` clause filtered products by two meta keys — `_alg_wc_pvbur_visible` / `_alg_wc_pvbur_invisible` — a fingerprint that belongs to a third-party catalog-visibility plugin, not WooCommerce core. The premium plugin wasn't in the client's "updates available" list, which is why disabling the four pending-update plugins had no effect.

**Fix:** Deactivate the culprit plugin (updates immediately work again); the host-side `MAX_JOIN_SIZE` raise was only a workaround, not the cure.

**Result:** Thread marked **Resolved** by the client. Confirmed working.

> ⭐ **Client testimonial (public, on wordpress.org):**
> *"DraftLab AI found the cause of a database error that was blocking all plugin updates on my WooCommerce store — something even my host couldn't figure out. Quick, clear and professional. Thank you so much!"*
> — Mick (@haarbollen), thread starter

**Evidence:** [case-001-evidence-card.png](case-001-evidence-card.png) — full thread snapshot (diagnosis → fix → resolved → testimonial)

---

## 🔧 Skills

`WordPress` · `WooCommerce` · `PHP` · `MySQL` · `React` · `REST API` · `Plugin development` · `Security hardening` · `Performance optimization` · `AI integration`

## 📦 Projects

- **DraftLab AI** — WooCommerce AI product-description plugin (React admin panel + PHP REST API + Freemius licensing). Free version on WordPress.org.
