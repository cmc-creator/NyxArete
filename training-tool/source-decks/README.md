# Source Deck Drop Zone

Place approved PowerPoint source files for your organization in this folder.
No client source decks are bundled with the platform.

Then run the extraction script from `training-tool/`:

```powershell
pwsh ./tools/extract-pptx-slides.ps1
```

This generates:
- `docs/deck-slide-inventory.csv`
- `docs/deck-merge-map.csv`

Review generated materials for client-specific branding before publishing them.
