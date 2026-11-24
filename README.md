# Carpooler UTD

**A student carpool app prototype for University of Texas at Dallas commuters.** Drivers post rides, riders request seats, and both sides manage the trip from request to completion.

🚗 **Live demo:** [nurul-chowdhury.github.io/carpooler-utd](https://nurul-chowdhury.github.io/carpooler-utd/)

> This is a **simulated, front-end demo**. There are no real accounts or shared database: all activity is saved in your own browser, and every visitor starts with the same sample data. Figures marked *Demo data* are illustrative.

---

## The problem

Many UTD students commute from Plano, Frisco, Irving, and Dallas. Driving alone means parking costs, traffic stress, and emissions, while students heading to the same campus at the same times rarely find each other. Carpooler matches student drivers and riders on similar routes and handles the coordination in one place.

---

## Try it in 2 minutes

1. Click **Reset demo** in the yellow banner.
2. Choose **Demo as Driver** → **Post Ride**. Enter a general pickup area, choose **Recurring** or **One-time**, optionally tick accessibility features, and **Publish Ride**.
3. Switch to **Demo as Rider** → **Find Rides** → **Request Seat** on your ride.
4. Switch to **Demo as Driver** → **My Trips** → **Accept**. Open **Message** to chat with the rider.
5. Click **Mark complete**, rate the ride, and watch **Your impact** and **Carpool points** update.

Also try: **Cancel trip** (you'll be asked for a reason), the **Accessible rides** filter, and refreshing the page (your demo data persists).

---

## Features

**Trip lifecycle**
- Ride posting with validation: one-time (date) or recurring (weekday) schedules
- Seat requests, accept/decline, and live seat counts that update as seats are booked or released
- Role-specific trip cards: driver and rider each see only the actions and wording that apply to them
- Cancellation after acceptance with a reason (*No-show, Destination changed, Running late, Other*) that is shown to the other person
- Completion, 1–5 star ratings, and trip history

**Communication**
- In-trip messaging between driver and rider

**Accessibility**
- Optional ride features: front seat, space for a wheelchair or mobility aid, step-free pickup, service animal welcome
- **Priority seat hold**: drivers can hold one seat for accessibility-priority riders until 24 hours before departure, after which it opens to everyone
- *Accessible rides* filter

**Privacy and safety**
- Pickup by general area, not exact address
- University email domain shown as the verification concept

**Impact and incentives**
- Monthly savings and CO₂ avoided update when trips are completed
- Carpool points: riders +10, drivers +15, +5 bonus for accessible rides

**Adaptable**
- *University Setup* panel re-brands the app for another campus (e.g., UNT, SMU) by changing the name, email domain, and campus stops

---

## Design decisions

| Decision | Why |
|---|---|
| Priority seat **hold** instead of a permanently reserved seat | Always reserving a seat would cut capacity by a third to a half in small cars; a hold that releases 24 hours before departure prioritizes access without wasting seats |
| Accessibility **feature tags** | A reserved seat only helps if the car meets the rider's actual need (e.g., wheelchair space) |
| Both sides can cancel after acceptance, **with a reason** | Mirrors real rideshare apps; fair to the other person and useful reliability data |
| Higher points for drivers | Driver supply is usually the bottleneck in carpool platforms |
| Trip type as **One-time / Recurring** | Structured schedules prevent ambiguous entries and enable future matching |
| Browser storage for the demo | Shows the full journey without accounts or servers; a real version would need a backend |

---

## Built with

- HTML, CSS, and JavaScript in a single file (`index.html`)
- Browser `localStorage` for demo persistence
- Hosted on GitHub Pages
- Built with AI-assisted development (Figma Make). I defined the user journey, trip-state rules, and accessibility design, then tested each flow and iterated on the results.

---

## What a production version would need

- Real student accounts with university email verification
- A shared database and real-time messaging
- Map-based route matching
- Notifications, reporting and blocking, and admin moderation tools
- Partnerships with university transportation and accessibility offices

---

**Author:** Nurul Chowdhury, MS Business Analytics, The University of Texas at Dallas · [GitHub](https://github.com/nurul-chowdhury)
