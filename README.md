# মিস্ত্রি ডট কম / Mishtry.com

Bengali-first, responsive local skills marketplace prototype. Buildless HTML/CSS/JavaScript in `dist/`.

## Run

From this directory: `python3 -m http.server 4173 --directory dist`
Open http://localhost:4173. No dependencies or build required.

## Included

- Eight explicitly fictional worker profiles, skill keywords/categories, three Dhaka area centers, radius filtering using Haversine distance, availability and price/rating sort.
- Worker detail dialogs with sample reviews and explicit unverified status.
- Validated demo job request form; bookings stored only in this browser's localStorage; delete supported.
- Contact and worker-registration demonstrations with no external delivery or account creation.
- bKash payment simulation with no credentials, PIN, OTP or real transaction.
- Keyboard-accessible native dialogs, labelled controls, responsive mobile layout.

## Required before launch

Real worker database and customer/worker authentication; moderated registration and professional/identity verification; accurate geocoding and user location consent; worker availability and booking acceptance; pricing confirmation; messaging/calling integration; authorized bKash merchant credentials, server-side payment creation/execution/verification, idempotency and webhook handling; review eligibility/moderation; privacy, data retention and dispute handling policies. The current prototype provides none of these live integrations.

All people, ratings and reviews are demo data. Distances are approximate straight-line distances from selected area centers, not a user's actual location or travel routes. Google Fonts is optional; system sans-serif is the fallback. No analytics or location permission requests.

## Search-first redesign

The first screen now includes search, suggested queries, location/radius selectors and an interactive schematic Dhaka area map. Map counts reflect skill/query/availability filters; clicking an area selects its center and a 3 km radius. Whole Dhaka uses a 30 km radius. This is not GPS or a geographically precise map.

Gig-style cards feature illustrative stock photography, profile photos, rates and links to detailed profiles, portfolios, video slots, sample job history and reviews. Photos load from images.unsplash.com and are explicitly illustrative; they do not depict the named fictional workers or prove completed work.

Customer onboarding accepts a name and Bangladesh-format phone number as a demo. No OTP is sent; the phone is discarded. Only the name is kept in sessionStorage. No real authentication is implemented.

The worker profile studio supports description, skills, experience, starting rate, portrait, up to four work photos, and video file preview. Camera recording uses getUserMedia and MediaRecorder, requests permission only on a user click, stops after 60 seconds or closing the dialog, and supports video upload as a fallback. All media uses local object URLs; nothing is uploaded. Draft profiles exist in memory until page reload. New draft ratings and job counts begin at zero, with no editable ratings or history.

Production still needs media storage, video transcoding, moderation, authenticated profile ownership, real OTP, completed-job history and reviews tied to genuine bookings. Camera recording requires HTTPS or localhost and device permission.

## Gig actions

Cards now provide separate profile, hire and save actions. Saved sample worker IDs persist in localStorage and can be filtered using “সেভ করা”; draft worker saves only last for the current page. Direct hire opens the same customer onboarding/booking demo. Search examples are Bengali; review badges use a higher-contrast amber treatment. Hire hover motion respects prefers-reduced-motion.
