# Beacon Journal 📡

## 2025-01-01 - Static HTML Multi-Version SEO Optimization

**Learning:** Static single-page applications or legacy multi-version web apps without a build system often lack fundamental crawler signals (`robots.txt`, `sitemap.xml`, canonical URLs, meta descriptions, and JSON-LD structured data). Adding `WebApplication` and `WebSite` JSON-LD schemas alongside self-referencing canonical URLs ensures clear search engine indexing without risk of duplicate content penalties across versioned subdirectories (`/` vs `/v1/`).

**Action:** Always verify JSON-LD schema validity with `json.loads` / parser scripts, maintain exact canonical URL trailing-slash consistency, and pair `robots.txt` with a valid `sitemap.xml`.
