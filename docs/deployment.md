# Finance deployment

Verified on 2026-11-23 (Asia/Saigon). Current source repository and production connection verified after migration.

- Repository: https://github.com/Tienkhoaa2908/quant-study, branch main.
- First production build from quant-study: 4f3d4fb45f3dd2dee8c6ab35774fc3db04d5a3a2, attributed to Tienkhoaa2908. Earlier finance commits are preserved in this repository history and UPSTREAM.md preserves inherited authorship.
- Vercel account/team: tienkhoaa2908; project finance-tienkhoaa2908.
- Production: https://finance-tienkhoaa2908.vercel.app.
- Existing production URL remains https://finance-tienkhoaa2908.vercel.app. First quant-study deployment: dpl_EvqH7jL5SEYRZw5ZrkAn1UVmEWC6, READY.
- Next.js 16.4.6, Node 24, root repository directory. Install npm ci; build npm run build.
- Vercel project is linked to GitHub repository Tienkhoaa2908/quant-study (GitHub repo ID 1469002574), production branch main, root directory. Pushes to main trigger production builds. The migration build was also verified through the authenticated CLI.
- No application environment variables, MongoDB or OAuth are needed for the finance learning flows. Progress is local to the browser with JSON backup import/export. Inherited server APIs are not finance progress synchronization.
- Upstream repository and its deployment were not changed.

## Releasing updates

Verify vercel whoami is tienkhoaa2908, the local project link targets finance-tienkhoaa2908, and Git author identity matches Tienkhoaa2908. Run content audit, unit tests, build and appropriate browser checks. Commit/push to quant-study/main; Vercel builds this branch automatically. Check that the resulting deployment reaches READY and the production URL serves the new commit. For a deliberate manual production deployment from the same checkout:

~~~sh
vercel deploy --prod --yes --scope tienkhoaa2908 --archive tgz --logs
~~~

Archive upload was used for the first quant-study deployment. GitHub App access to quant-study was then granted and native Git integration connected successfully. Never deploy from an unverified account/project link or print credentials.

## Verification

- Finance content audit: 36 lessons, 9 modules, 108 exercises; zero structure, prerequisite, formula-parity or KaTeX errors.
- Local production build passed. Full local suite: 123 TypeScript unit tests and 80 Playwright cases across desktop/mobile. After final small changes, 16 targeted unit cases passed again.
- Six Python project programs ran successfully; 5 maintained regression tests passed.
- Final lesson-introduction examples were rebuilt and passed the content audit before release.
- Vercel build/install passed, including inherited mathematics audits; install reported zero dependency vulnerabilities.
- Public production returned HTTP 200 and exposed 36 lessons. Eight production Playwright cases passed across desktop/mobile: learner/review flow, VI/EN, persisted drafts, storage failure handling, catalog search, project checklists/download, lab inputs and cross-tab updates.
- Desktop/mobile production screenshots inspected. Source and rendered math checks are technical validation, not a measured learning-outcome study.

Local run evidence is outside the repository in D:\ChatGPT\webtaichinh\research: full-build.log, full-unit-tests.log, full-e2e.log, final-targeted-tests.log, production-e2e.log, full-content-audit.json and finance-live-*.png. Legacy mathematics UI tests are preserved separately; they were not rerun as part of the finance E2E suite.
