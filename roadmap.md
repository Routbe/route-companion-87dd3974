# ROUT roadmap

## Refactor pass (component decomposition & tech debt)

- [ ] Split `src/pages/Admin.tsx` into `src/components/admin/` (AdminUserTable, AdminVerificationQueue, AdminAnalyticsSummary, AdminSettings)
- [ ] Split `src/components/dashboard/ProfileEditor.tsx` into `src/components/dashboard/editor/` (ProfileBasicInfoForm, ProfileLinksManager, ProfileThemePicker, ProfileHeaderPreview)
- [ ] Flatten `src/pages/routes/*` into `src/routes/*` (remove 16 wrapper files)
- [ ] Fix 50x `react-refresh/only-export-components` (move helpers/constants/types to `src/lib` / `src/types`)
- [ ] Fix 5x `react-hooks/exhaustive-deps` (QRPreview, QRInputFields, Index)
- [ ] Replace `any` in server/API functions with strict types
- [ ] Verify: 293 tests pass + `tsgo --noEmit` clean
- [ ] Keep /tmp/observability/build-errors.log clean (typecheck must pass before finishing)

## Rondleiding (/tour)
- [x] TourDesignStep + TourAccountStep
- [x] src/pages/Tour.tsx + src/routes/tour.tsx (mobile-first, sticky nav, autosave)
- [x] tour.* vertaalsleutels in nl/en/fr/de
- [x] CTA "Start de rondleiding" op About + startpagina
- [x] Onboarding voorvullen uit concept + concept opruimen
- [ ] Rondleiding op mobiel testen

## Open werk (nieuw gemeld)
- [ ] Hub-instellingen gratis account: dubbele "Identiteit, URL & badge" naast de profielkeuze bovenaan verwijderen
- [ ] Splits "Identiteitsverificatie & ROUT Badges"; badges verplaatsen naar "Links & components"
- [ ] Meer Pagina Bezoek Effects toevoegen
- [ ] Verified-badge (hand-met-keurmerk) tonen op u/-pagina van verified leden, per lid uitschakelbaar, meertalig (fallback Engels)
- [ ] Verified accounts: hun publieke pagina wordt niet echt aangemaakt — onderzoeken en fixen
- [ ] Routeplanner met kaart
- [ ] Admin-herbedraden voltooien

## Profielhub-naamruimte (gedaan)
- [x] Eén gedeelde handle-naamruimte (root, alias, root-domein) — src/lib/handle-namespace.server.ts + db/39
- [x] /u/<handle> valt niet meer terug op andermans rootprofiel
- [x] /api/claim-root weigert namen van andere accounts
- [x] Domeinenpaneel: expliciet "extra webadres, geen derde profiel"
- [ ] Later: e-mailalias (alias_status/alias_sync_*) in admin hernoemen naar "E-mailalias" om verwarring met profielalias te vermijden
