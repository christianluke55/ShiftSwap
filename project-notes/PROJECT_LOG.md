# ShiftSwap — Project Log

## Session 1: Setting Up GitHub and Building the First Version
For my first session, I created a public GitHub repository called `ShiftSwap`, turned on GitHub Pages so the site has a live link that works on both my laptop and my phone, and created the `project-notes/` folder with `BUSINESS_CASE.md` and `PROJECT_LOG.md`. From there, I built the initial `index.html` file using plain HTML, CSS, and JavaScript without any outside libraries or frameworks. I wanted a visitor to understand the site right away, so I set up a clear top section for a fictional hockey and sporting-goods shop called **SlapShot Outfitters**, along with live shift numbers, a form to post open shifts, filter buttons, and the **Network Density & Shift-Fill Simulator**.

**Prompts I Used:**
* *"Build a complete, self-contained single-file web application (`index.html`) for ShiftSwap, an internal shift-trading and coverage platform for hourly retail staff and floor managers at a hockey and sporting-goods shop (SlapShot Outfitters)."*
* *"Include a clear top section explaining what the site does, a live metrics bar, an interactive shift board to post/claim/filter shifts, and a simulator showing how staff participation improves shift coverage."*

---

## Session 2: Testing on Mobile and Fixing Layout & Filter Bugs
In my second session, I opened the live GitHub Pages link on my phone and shrunk my laptop browser window to see how the buttons, forms, and simulator sliders worked on smaller screens. Testing it like a real user helped me catch three issues that needed fixing:

1. **Buttons Looking Squished on Phone Screens:** On narrow screens under 520px wide, clicking "Claim Shift" opened the name input box and the Confirm/Cancel buttons right next to the shift text, making the layout wrap awkwardly. **How I Fixed It:** I added a CSS rule for screens under 520px so the claim box moves onto its own clean row underneath the shift details.
2. **New Shifts Disappearing Under the Active Filter:** When the shift board was filtered to "Covered Only" and I posted a brand-new open shift, it looked like the shift did not get added because the filter stayed stuck on "Covered Only." **How I Fixed It:** I changed the form submit function so posting a new shift automatically switches the filter back to "All Shifts."
3. **Blank Spaces Claiming a Shift:** Typing just spaces into the name box allowed a shift to be marked as covered without a real employee name. **How I Fixed It:** I added a `.trim()` check in JavaScript so the form requires actual text before claiming a shift.

**Prompts I Used:**
* *"Fix mobile stacking on phone screens so the inline claim input and buttons sit on their own clean row below the shift info."*
* *"Make sure posting a new shift resets the status filter to All Shifts and blocks blank spaces in the claim name input."*

---

## Session 3: Writing the Business Case and Final Check
In my final session, I wrote `project-notes/BUSINESS_CASE.md` (around 1,500 words) explaining ShiftSwap's value proposition, network effects, VRIN moat, and cloud/risk decisions. After saving it, I checked the whole repository and live site to make sure there were no outside libraries, real brand logos, fake login or payment forms, or footer text calling it a student prototype.

---

## What a Real Commercial Version Would Need
Right now, ShiftSwap runs in the browser and resets when you refresh the page. If this were launched as a real paid app for retail stores, it would need:
* **Real User Accounts:** Separate logins for regular store staff (who post and claim shifts) and floor managers (who approve swaps and make sure nobody accidentally goes into overtime).
* **A Backend Database:** A cloud database (like PostgreSQL) so shifts, store rosters, and staff skill tags (like who is certified to run the skate sharpener) stay saved across everyone's phones.
* **Text and Push Notifications:** Automated SMS alerts (using a service like Twilio) or phone notifications so qualified coworkers find out right away when an urgent shift opens up.
* **Payroll and Schedule Sync:** Connections to retail systems like Square, Lightspeed, or ADP so approved shift swaps update the official schedule automatically.
* **Payments and Security:** Stripe billing to charge stores monthly, plus encrypted passwords and secure HTTPS connections.

---

## Business Reflection: What Building With AI Taught Me About Software
Building ShiftSwap with AI showed me how fast and cheap it has become to create working software. Within a couple of sessions, I was able to turn plain-English instructions into a responsive website with live counters and a working simulator—something that used to take a developer days to write from scratch. The key takeaway I had from this process is that because anyone can copy the same website features in an afternoon using AI, the code itself is not a real business advantage. For a product like ShiftSwap to actually survive against competitors, its value has to come from things AI cannot copy overnight—like getting an entire store's staff using the app every week, building up data on which employees reliably show up for claimed shifts, and fitting into the manager's daily scheduling routine so switching to another tool feels like too much hassle.
