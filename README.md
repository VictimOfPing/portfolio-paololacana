# Studio Dentistico Dott. Paolo Lacana

[![Next.js](https://img.shields.io/badge/Next.js-15-000000?logo=nextdotjs&logoColor=white)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=111111)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![CSS](https://img.shields.io/badge/CSS-Custom-1572B6?logo=css3&logoColor=white)](src/app/globals.css)
[![Live](https://img.shields.io/badge/Live-paololacanastudiodentistico.it-1f7a5c)](https://www.paololacanastudiodentistico.it)

Patient-facing website for a dental practice in Sassari, Italy. The project turns a local healthcare brief into a fast, mobile-first website with clear treatment pages, direct contact paths, structured SEO data, and real studio photography.

## Project Snapshot

| Area | Details |
| --- | --- |
| Client / sector | Studio Dentistico Dott. Paolo Lacana / Dental clinic and local healthcare |
| Main problem | Patients needed one clear place to understand treatments, opening hours, emergency contacts, location, and booking options before calling the studio. |
| Delivered result | Live Next.js website with 11 service pages, local SEO metadata, JSON-LD structured data, sitemap, cookie consent, and mobile-ready phone / WhatsApp CTAs. |
| Live URL | [paololacanastudiodentistico.it](https://www.paololacanastudiodentistico.it) |

## Screenshot

![Homepage desktop screenshot](docs/screenshots/home-desktop.png)

## Tech Stack

| Layer | Tools |
| --- | --- |
| Frontend | ![Next.js](https://img.shields.io/badge/Next.js-15-000000?logo=nextdotjs&logoColor=white) ![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=111111) ![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript&logoColor=white) |
| Styling | ![CSS](https://img.shields.io/badge/Custom_CSS-responsive-1572B6?logo=css3&logoColor=white) |
| UI and motion | ![Lucide](https://img.shields.io/badge/Lucide_React-icons-f56565) ![GSAP](https://img.shields.io/badge/GSAP-animation-88CE02?logo=greensock&logoColor=111111) |
| SEO | Next Metadata API, dynamic Open Graph image, Dentist / Service JSON-LD, sitemap, robots.txt |
| Quality | ![ESLint](https://img.shields.io/badge/ESLint-9-4B32C3?logo=eslint&logoColor=white) TypeScript strict project structure |

## Core Features

- **Local healthcare SEO:** canonical metadata, Open Graph / Twitter cards, dynamic OG image, `Dentist` schema, service-level JSON-LD, sitemap, and robots configuration.
- **Service content system:** all treatments are managed from `src/lib/site-data.ts` and rendered through static App Router service pages.
- **Conversion-focused contact paths:** phone, WhatsApp, appointment triggers, open-status indicator, copy buttons, and urgent-care CTAs are visible across the main user flows.
- **Patient-oriented service discovery:** searchable and filterable services explorer covering prevention, care, rehabilitation, surgery, children, and emergencies.
- **Trust-building visual identity:** real studio, team, and room photography served through `next/image`, plus a consistent clinic logo and favicon set.

## Architecture

The application uses the Next.js App Router with static, SEO-friendly routes:

```text
src/app/
  page.tsx                    Homepage and primary patient journey
  chi-siamo/page.tsx          Studio and team presentation
  servizi/page.tsx            Searchable services overview
  servizi/[slug]/page.tsx     Static treatment detail pages
  contatti/page.tsx           Contact, hours, address, and request form
  privacy-policy/             Legal content
  cookie-policy/
  terms-of-service/

src/components/
  SiteChrome.tsx              Header, footer, navigation, cookie banner shell
  ServicesExplorer.tsx        Client-side search and category filtering
  ContactForm.tsx             Client-side request preparation and validation
  OpenStatus.tsx              Opening-hours state indicator

src/lib/
  site-data.ts                Single source of truth for clinic data and services
  seo.ts                      Metadata, canonical URLs, JSON-LD, indexable routes

public/
  img/                        Studio, team, and treatment photography
```

No database is required for the current scope. The contact form intentionally prepares the request on the client side and directs patients to confirm by phone, which fits the studio's existing appointment workflow.

## Results and Impact

- Published a live digital presence for a Sassari dental clinic at `www.paololacanastudiodentistico.it`.
- Built 11 indexable treatment pages from one typed content source, reducing duplicated page logic.
- Added structured data and local SEO foundations for the clinic, treatments, address, opening hours, and canonical URLs.
- Prioritized mobile patient actions with direct call, WhatsApp, copy-to-clipboard, and emergency-oriented CTAs.
- Included privacy, cookie, and terms pages so the public site is ready for real patient traffic.

## Run Locally

```bash
npm install
npm run dev
```

Production checks:

```bash
npm run lint
npm run build
```

## Links and Contact

- Live site: [paololacanastudiodentistico.it](https://www.paololacanastudiodentistico.it)
- Repository: [github.com/VictimOfPing/studio-dentistico](https://github.com/VictimOfPing/studio-dentistico)
- Portfolio / developer profile: [github.com/VictimOfPing](https://github.com/VictimOfPing)
- Project contact: [codingplugin@gmail.com](mailto:codingplugin@gmail.com)
