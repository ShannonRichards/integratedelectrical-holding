Integrated Subsidiaries — Holding Pages
Generated: 2025-08-19 17:25

Contains:
- integratedcooling/index.html
- integratedplumbing/index.html
- integratedelectrical/index.html

Deploy per site:
1) Create a GitHub repo (e.g., integratedcooling-holding).
2) Upload the matching index.html at the repo ROOT and commit to default branch.
3) Azure → Create Static Web App → Source: GitHub → pick repo/branch.
   Build preset: Custom/Other
   App location: /
   Output location: (blank)
   API location: (blank)
   If the workflow errors about package.json, add: skip_app_build: true under the action 'with:' block.
4) Custom Domain:
   - Add 'www.<domain>.ky' in Azure; in GoDaddy set CNAME www → <your-swa>.azurestaticapps.net
   - Forward root '<domain>.ky' → 'https://www.<domain>.ky' (301, no masking).
