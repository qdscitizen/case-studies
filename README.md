# ChongZhou Sun — WordPress / WooCommerce Developer

WordPress plugin author & troubleshooter. 10 years of frontend engineering (Vue/React), now focused on WordPress full-stack work: plugin diagnostics, WooCommerce fixes, performance and security.

**Public track record:** active contributor on [WordPress.org support forums](https://profiles.wordpress.org/sunchongzhou2026/) · resolved threads with client testimonials below.

---

## ✅ Case Study #001 — Database error blocking all plugin updates

**Client:** WooCommerce store owner (WordPress.org user [@haarbollen](https://wordpress.org/support/users/haarbollen/))
**Forum thread:** https://wordpress.org/support/topic/database-error-435/
**Status:** Resolved ✓ · with public client testimonial

### Problem

Every plugin update failed with a MySQL error — `The SELECT would examine more than MAX_JOIN_SIZE rows` — and the same error appeared on the dashboard. The client's hosting provider could not identify the cause.

### Diagnosis

Instead of treating it as a hosting config issue, I read the raw failing SQL. Its `WHERE` clause filtered products by two meta keys — `_alg_wc_pvbur_visible` / `_alg_wc_pvbur_invisible` — a **fingerprint belonging to a third-party catalog-visibility plugin**, not WooCommerce core.

That plugin was a premium one, so it never appeared in the client's "updates available" list — which is exactly why disabling the four pending-update plugins had no effect.

### Fix

Deactivate the culprit plugin → plugin updates work immediately again. Raising the host-side `MAX_JOIN_SIZE` would have been a workaround only; the real fix was removing the trigger.

### Result

Thread marked **Resolved** by the client.

> ⭐ **Client testimonial (public, on wordpress.org):**
> *"DraftLab AI found the cause of a database error that was blocking all plugin updates on my WooCommerce store — something even my host couldn't figure out. Quick, clear and professional. Thank you so much!"*
> — Mick (@haarbollen), thread starter

### Evidence

| File | What it is |
|---|---|
| [20261010/case-001-original-thread-fullpage.png](20261010/case-001-original-thread-fullpage.png) | Full original thread, as it appeared on wordpress.org (diagnosis → fix → resolved → testimonial) |
| [20261010/WPorg-case001-database-error-435.html](20261010/WPorg-case001-database-error-435.html) | Saved copy of the thread |
| [20261010/case-001-review-zh.html](20261010/case-001-review-zh.html) | Detailed review write-up (CN) |

---

## 🔧 Skills

`WordPress` · `WooCommerce` · `PHP` · `MySQL` · `React` · `REST API` · `Plugin development` · `Security hardening` · `Performance optimization` · `AI integration`

## 📦 Projects

- **DraftLab AI** — WooCommerce AI product-description plugin. React admin panel + PHP REST API layer + Freemius licensing. Free version on WordPress.org.

## 📁 Repository layout

```
case-studies/
├── README.md
└── YYYYMMDD/          ← one folder per case, dated
    ├── <case>*.png    ← evidence screenshots
    ├── <case>*.html   ← saved thread / write-up
```

---

*Contact: open an issue or reach me on the WordPress.org support forums.*
