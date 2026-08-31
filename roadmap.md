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
