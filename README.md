# teamsykmelding-automations

Et sett med cron-jobber som sjekker diverse ting og sender påminnelser til #teamsymelding-påminnelser på slack og andre automatiseringer.

Liste over påminnelser og når de kjøres (tidene er i UTC):

<!-- COMPUTER SAYS DON'T TOUCH THIS START -->

- **Backend (Java 21): Oppdatering av distroless digest** | Kl.06:45, på mandag
- **Frontend (node 22): Oppdatering av distroless digest** | Kl.06:30, på mandag
- **Gamle pull requests** | Kl.10:15, på tirsdag og fredag
- **Info om backend dependabot PR-er** | Kl.07:15, på mandag
- **Info om frontend dependabot PR-er** | Kl.07:15, på mandag
- **Repos med feil i CODEOWNERS** | Kl.06:45, på torsdag
- **Sjekk sårbarheter daglig for CRITICAL og HIGH** | Kl.07:03, hver dag
- **Sjekk sårbarheter ukentlig for MODERATE og LOW** | Kl.10:10, på fredag
- **Urørte repositories** | Kl.08:15, på onsdag

<!-- COMPUTER SAYS DON'T TOUCH THIS END -->

## Utvikling

Du må ha https://bun.sh for å kjøre dette lokalt.

Installer avhengigheter:

```bash
bun install
```

Opprett en `.env`-fil hvor du kan legge in Github `READER_TOKEN` og `SLACK_WEBHOOK_URL` for å utvikle lokalt dersom du ønsker det.

For å kjøre script:

```bash
bun run scripts/ditt-script.ts
```

Dersom du legger til eit nytt script, husk å kjøre følgende kommando:

```bash
bun run update-readme.ts
```
