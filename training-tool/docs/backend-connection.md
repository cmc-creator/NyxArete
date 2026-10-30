# Frontend to Backend Connection

## Configure API Base
In browser dev tools console, set:

```javascript
localStorage.setItem("nyxApiBase", "https://your-backend-domain")
localStorage.setItem("nyxOrgSlug", "nyxarete")
```

Or edit `training-tool/runtime-config.js`:

```javascript
window.NYX_API_BASE = "https://your-backend-domain"
window.NYX_ORG_SLUG = "nyxarete"
```

Then refresh the page.

## Runtime Behavior
- On Start Experience, frontend creates a backend attempt.
- During scenarios and assessment, events are posted to backend.
- On Submit Completion, attempt status is finalized and scored.
- Each posted event also includes an xAPI-shaped statement for LMS export and analytics interoperability.

## Branding
- NyxArete workforce training for psychiatric acute inpatient care.
- Trademark and Copyright (c) NyxArete.

## Fallback Mode
If `nyxApiBase` is not configured, the training app runs standalone with local export only.

## Existing Deployments
The platform defaults to the `nyxarete` organization slug. Configure the actual
organization slug in runtime config and the login/password-recovery forms when
connecting an existing backend. Changing frontend defaults does not rename an
organization or migrate users, attempts, certificates, or saved browser settings.
Live organization data must be reviewed and migrated separately before changing
an existing tenant's slug. Do not run the seed as a tenant rename operation.
