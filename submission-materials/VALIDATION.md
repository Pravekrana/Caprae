# Validation evidence

Validation was performed on Windows with the bundled Python 3.12 runtime and Microsoft Edge driven through Playwright on 7 October 2026. All input datasets in these checks were synthetic. The final application was started through the included PowerShell launcher on port 8765, using an isolated SQLite database.

## Results

| Check | Observed result |
| --- | --- |
| Focused backend suite | 10 tests passed; independent final run completed in 1.989 seconds |
| Browser workflow | 12 check groups passed; no uncaught browser errors |
| Fixture import | 12 source rows yielded 11 canonical companies; one duplicate merged |
| Default criteria | 6 priority companies; one company without source provenance |
| Repeated import | No extra canonical companies; backend regression also verifies unchanged provenance |
| Local benchmark | 1,000 distinct-domain synthetic companies inserted in 0.567 seconds in a fresh database |
| Walkthrough playback | 108.148 seconds, 1600 by 900 pixels, WebM VP9; no playback error |
| Visual review | Desktop, mobile, import, company details, filtered queue, and all six video scenes inspected |
| Windows launch | Runtime version detection skips unavailable Python shims and finds a working Python 3.10+ runtime |

The benchmark measures one local import, excluding application startup. It is not a throughput, concurrency, or production capacity claim. The earlier implementation took 8.004 seconds on the same 1,000-row shape; duplicate lookup and indexed identity matching were subsequently improved. Times can vary with the machine and system load.

## Reproduce the backend suite

From the application folder, run:

```sh
python3 -m unittest discover -s tests -v
```

On Windows, use a working Python executable or the launcher-discovered runtime with the same arguments. The tests create temporary databases and exercise missing-field scoring, location matching, invalid numbers, duplicate identity, conflicts and source retention, repeated imports, limits, durable API mutations, content-type/origin validation, and path handling.

## Browser check groups

1. Start with an empty workspace and confirm its initial state.
2. Import the included demo CSV and confirm 11 company rows; the populated queue must hide its empty state.
3. Re-import and confirm the company count remains 11.
4. Open Northstar IT and confirm six factor explanations.
5. Confirm its evidence retains the second Trade association source.
6. Shortlist the company and filter to shortlist; confirm one row.
7. Clear filters, select Priority, and confirm six rows under the default buy box.
8. Download CSV and confirm it contains the filtered priority cohort and excludes Clearwater HVAC.
9. Search for a nonexistent company and confirm the empty state.
10. Change the revenue minimum to 9,000,000 and confirm Northstar's revenue factor loses its points.
11. Inspect the 390-pixel mobile layout; the page must not overflow horizontally, and the company table can scroll within its container.
12. Confirm the browser reports no uncaught application errors.

Final visual inspection also checked source-gap counts, selection labels, and system font fallback. The walkthrough was checked through native browser playback, including duration, dimensions, and representative frames from each of its six scenes.

## What is unverified

Authenticated SaaSquatch behavior, real company scraping, contact deliverability, customer conversion, acquisition outcomes, sustained concurrent load, cloud deployment, and a live CRM integration were not tested or represented as complete. The score is a deterministic review aid. No customer or third-party dataset is distributed.
