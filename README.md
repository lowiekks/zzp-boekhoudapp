# SoloLedger – Smart & Simple Bookkeeping for the Self-Employed

**SoloLedger** is een innovatieve boekhoudapp ontworpen voor zelfstandigen in hoofd- of bijberoep. De app automatiseert het volledige proces van factuurherkenning, bankkoppeling, btw-verwerking en stockbeheer via slimme AI-modules – met een ultrasimpele, intuïtieve gebruikersinterface.

---

## Table of Contents

- [Why SoloLedger?](#why-sololedger)
- [Features](#features)
- [UI/UX Principles](#uiux-principles)
- [Tech Stack](#tech-stack)
- [Modules](#modules)
- [Setup & Installation](#setup--installation)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)

---

## Why SoloLedger?

Boekhouden is een van de grootste frustraties voor kleine zelfstandigen. Bestaande tools zijn vaak:

- Te technisch of verwarrend voor leken
- Te duur voor parttime ondernemers
- Te veel gericht op klassieke boekhouders
- Niet geautomatiseerd, traag en manueel

**SoloLedger** lost deze problemen op:

### Zelfstandigen ergeren zich aan:

| Frustratie                                | Oplossing door SoloLedger                     |
|-------------------------------------------|-----------------------------------------------|
| Te veel boekhoudjargon en tabellen        | Simpele taal, AI-voorstellen, contextueel UI |
| Alles manueel toevoegen                   | OCR, e-mail sync, bankkoppeling, smart rules |
| Moeilijk contact met de boekhouder        | Boekhouder-login, commentaar bij transacties |
| Geen overzicht van financiële status      | Live dashboards, alerts, kwartaalvooruitblik |
| Geen kennis van aftrekbaarheid / btw      | AI-suggesties met uitleg per kost             |
| Geen integratie met webshop / stock       | Shopify/WooCommerce link, automatisch stockbeheer |
| Te hoge prijs voor parttime gebruikers    | Betaalbare, modulaire pricing zonder overbodige functies |

---

## Features

### Boekhoudautomatisatie
- OCR-ondersteuning (PDF/bonnetjes)
- Banktransacties koppelen via PSD2 APIs
- Slimme AI-categorisatie (boekhoudregels)

### Realtime dashboard
- Omzet, kosten, winst, openstaande facturen
- Automatische alerts: overschrijding drempelbedragen, lage kaspositie

### Facturatie & on-the-go betalen
- Directe factuur maken, QR-betaling of link
- Facturen automatisch gekoppeld aan klanten en stock

### Stockbeheer
- Aankopen automatisch aan voorraad toevoegen
- Overzicht per categorie, meldingen bij lage voorraad

### Eenvoudig samenwerken met je boekhouder
- Exporteer kwartaalrapport of geef toegang tot documenten
- Boekhoudermodus met lees- of schrijfrechten

### Integraties
- WooCommerce, Shopify, Stripe, Mollie
- Google Drive / Dropbox documentback-up

---

## UI/UX Principles

SoloLedger zet gebruiksgemak en minimalisme centraal.  

**Designfilosofie:**
- “No clutter, just clarity”
- Mobielvriendelijk & toegankelijk
- Taalgebruik afgestemd op zelfstandigen zonder boekhoudkennis
- Geen overbodige knoppen of irrelevante instellingen

**Concreet:**
- Clean interfaces met duidelijke iconen
- Progressieve onboarding (stel alles geleidelijk in)
- Contextuele uitleg: “Wat betekent dit?” tooltips
- Donker/licht modus

---

## Tech Stack

- **Frontend:** React Native (cross-platform), Tailwind UI, TypeScript
- **Backend:** Node.js + Express, Python voor AI-engine
- **Database:** PostgreSQL + Redis (cache)
- **OCR Engine:** Tesseract.js + Google Vision API fallback
- **AI/ML:** OpenAI API + custom rules engine (Node + Python hybrid)
- **Bankkoppeling:** PSD2 / Nordigen / Klarna Open Banking
- **Storage:** AWS S3, Firebase voor media
- **CI/CD:** GitHub Actions + Vercel (frontend) / Railway (backend)

---

## Modules

| Module               | Status   | Beschrijving                                                      |
|----------------------|----------|-------------------------------------------------------------------|
| `invoiceScanner`     | ✅        | OCR van PDF’s, scans en foto's, extractie leverancier/bedrag     |
| `bankSync`           | ✅        | Automatische transactiekoppeling via PSD2 API                    |
| `smartBookingAI`     | ✅        | AI-voorstellen voor kostenplaatsen, btw en logica                |
| `realtimeDashboard`  | ⚙️        | Omzet/kosten analyse, kwartaalprognoses                          |
| `stockManager`       | ⚙️        | Productbeheer gekoppeld aan aankopen en verkopen                 |
| `factuurModule`      | ✅        | Facturen maken, versturen, opvolging                             |
| `bookkeeperPortal`   | ⚙️        | Exporteer alles per kwartaal of geef toegang met rechtenbeheer  |

---

## Setup & Installation

```bash
# Clone repository
git clone https://github.com/yourorg/sololedger.git
cd sololedger

# Install dependencies
npm install

# Start dev environment
npm run dev