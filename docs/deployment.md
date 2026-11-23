# Finance deployment

Verified on 2026-11-23 (Asia/Saigon).

- Repository: https://github.com/Tienkhoaa2908/quant-study, branch main.
- Application commit: 6e7309cddba7cd246d4e5c6c569c76db78ff7677.
- Vercel account/team: tienkhoaa2908; project finance-tienkhoaa2908.
- Production: https://finance-tienkhoaa2908.vercel.app.
- Deployment: https://finance-tienkhoaa2908-3qlml1734-tienkhoaa2908.vercel.app, READY.
- Next.js 16.4.6, Node 24, root repository directory. Install npm ci; build npm run build.
- Repository migration pending verification of the Git integration. The earlier production deployment was created with the authenticated CLI.
- No application environment variables, MongoDB or OAuth are needed for the finance learning flows. Progress is local to the browser with JSON backup import/export. Inherited server APIs are not finance progress synchronization.
- Upstream repository and its deployment were not changed.

## Releasing updates

Verify vercel whoami is tienkhoaa2908, the local project link targets finance-tienkhoaa2908, and Git author identity matches Tienkhoaa2908. Run content audit, unit tests, build and appropriate browser checks. Commit/push to quant-study/main. After checking the Vercel Git connection, deploy or verify the resulting production build:

~~~sh
vercel deploy --prod --yes --scope tienkhoaa2908 --archive tgz --logs
~~~

Archive upload was used because the initial individual-file upload did not complete during observation. That attempt was stopped before a deployment was created. Never deploy from an unverified account/project link or print credentials.

## Verification

- Finance content audit: 36 lessons, 9 modules, 108 exercises; zero structure, prerequisite, formula-parity or KaTeX errors.
- Local production build passed. Full local suite: 123 TypeScript unit tests and 80 Playwright cases across desktop/mobile. After final small changes, 16 targeted unit cases passed again.
- Six Python project programs ran successfully; 5 maintained regression tests passed.
- Final lesson-introduction examples were rebuilt and passed the content audit before release.
- Vercel build/install passed, including inherited mathematics audits; install reported zero dependency vulnerabilities.
- Public production returned HTTP 200 and exposed 36 lessons. Eight production Playwright cases passed across desktop/mobile: learner/review flow, VI/EN, persisted drafts, storage failure handling, catalog search, project checklists/download, lab inputs and cross-tab updates.
- Desktop/mobile production screenshots inspected. Source and rendered math checks are technical validation, not a measured learning-outcome study.

Local run evidence is outside the repository in D:\ChatGPT\webtaichinh\research: full-build.log, full-unit-tests.log, full-e2e.log, final-targeted-tests.log, production-e2e.log, full-content-audit.json and finance-live-*.png. Legacy mathematics UI tests are preserved separately; they were not rerun as part of the finance E2E suite.
