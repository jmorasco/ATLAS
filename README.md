# ATLAS Market Intelligence Terminal

A public, mobile-friendly, **free and no-login** financial market reference dashboard, designed in Midnight Navy & Electric Blue.

## Public URL
After configuring GitHub Pages to publish with GitHub Actions:
https://jmorasco.github.io/ATLAS/

## One-time GitHub Pages enablement
1. Open https://github.com/jmorasco/ATLAS/settings/pages
2. Under **Build and deployment → Source**, select **GitHub Actions**.
3. Navigate to https://github.com/jmorasco/ATLAS/actions/workflows/deploy-pages.yml and click **Run workflow**, or commit another update to the site.
4. Confirm the **Publish ATLAS** step succeeds. The URL above becomes live once deployment completes.

## Source and accuracy policy
* The scheduled workflow refreshes source observations every two hours (GitHub schedule is best-effort).
* 10-year/30-year US yields: Federal Reserve H.15 series through FRED, **daily observations**.
* Brent and WTI: FRED-hosted EIA daily spot benchmarks, **not futures**.
* Gold/silver: gold-api.com keyless spot feed; Coinbase Exchange supplies BTC/USD.
* Spot VIX: FRED Cboe VIX daily history, **not futures**.
* DJIA, Nasdaq Composite, and S&P 500 cash-index values: linked to original FRED series, deliberately **not republished** because third-party distribution rights have not been established.
* Quotes include original observation timestamps, provider identification, and stale/unavailable labels. No synthetic market numbers are supplied.
* The public site's manual refresh checks its last **published snapshot**; it does not bypass the GitHub Actions publication cadence.
* Economic events and earnings are linked to official/public schedules. The static application does **not** claim a complete real-time calendar.
* Historical charts only appear when the provider returned real source observations.

## Security and cost
GitHub Pages hosting is free on public repositories, with no visitor account required. The workflow uses public keyless endpoints and the built-in GitHub Actions token; it stores no provider credentials.

## Verification
The initial GitHub Actions run successfully executed Node syntax checks, fetched **8 of 11 instrument observations**, and committed a market snapshot. If Pages setup fails with "Get Pages site failed: Not Found", enable Pages under repository Settings first.

Repository: https://github.com/jmorasco/ATLAS
