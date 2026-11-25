# ShiftSwap — Project Log

**Name:** Christian Luke  
**Startup:** ShiftSwap  
**Live Site:** https://christianluke55.github.io/ShiftSwap/

---

## Session 1: Setting Up GitHub and Building the First Version
**Nov 12 — Driver:** Christian Luke  

For my first session, I created a public GitHub repository called ShiftSwap, turned on GitHub Pages so the site has a live link that works on both my laptop and my phone, and created the `project-notes/` folder with `BUSINESS_CASE.md` and `PROJECT_LOG.md`. From there, I built the initial `index.html` file using plain HTML, CSS, and JavaScript without any outside libraries or frameworks. I wanted a visitor to understand the site right away, so I set up a clear top section for a fictional hockey and sporting-goods shop called *SlapShot Outfitters*, along with live shift numbers, a form to post open shifts, filter buttons, and the *Network Density & Shift-Fill Simulator*.

*Prompts I Used:*
- *"Make a one-page website in index.html for an app called ShiftSwap where workers at a hockey store called SlapShot Outfitters can post and pick up open shifts. Do not use any outside libraries or anything that needs to be installed."*
- *"Put a stats bar at the top, a form where people can post a new shift, filter buttons, and a slider that shows how more workers using the app helps more shifts get covered."*

**Committed?** Yes — `"Initial ShiftSwap site and project notes setup"`

---

## Session 2: Testing on Mobile and Fixing Layout & Filter Bugs
**Nov 15 — Driver:** Christian Luke  

In my second session, I opened the live GitHub Pages link on my phone and shrunk my laptop browser window to see how the buttons, forms, and simulator sliders worked on smaller screens. Testing it like a real user helped me catch three issues that needed fixing:

1. *Buttons Looking Squished on Phone Screens:* On narrow screens under 520px wide, clicking "Claim Shift" opened the name input box and the Confirm/Cancel buttons right next to the shift text, making the layout wrap awkwardly. *How I Fixed It:* I added a CSS rule for screens under 520px so the claim box moves onto its own clean row underneath the shift details.
2. *New Shifts Disappearing Under the Active Filter:* When the shift board was filtered to "Covered Only" and I posted a brand-new open shift, it looked like the shift did not get added because the filter stayed stuck on "Covered Only." *How I Fixed It:* I changed the form submit function so posting a new shift automatically switches the filter back to "All Shifts."
3. *Blank Spaces Claiming a Shift:* Typing just spaces into the name box allowed a shift to be marked as covered without a real employee name. *How I Fixed It:* I added a `.trim()` check in JavaScript so the form requires actual text before claiming a shift.

*Prompts I Used:*
- *"When I click Claim Shift on my phone the name box and buttons look squished next to the text. Can you make them drop down to the next line on small screens?"*
- *"If the filter is on Covered Only and I post a new shift, it doesn't show up. Make it switch back to All Shifts when I post one, and stop people from claiming a shift by just typing spaces."*

**Committed?** Yes — `"Fix mobile stacking and shift filter bugs"`

---

## Session 3: Making the Sample Shifts Realistic & Improving the Visual Design
**Nov 18 — Driver:** Christian Luke  

In my third session, I wanted the shift board to look like an actual retail store schedule instead of generic placeholder text. I updated the sample shifts so they matched real hockey shop tasks—like skate sharpening counter coverage, stick-fitting floor help, and weekend register shifts—with realistic employee names, times, and status badges. I also cleaned up the colors, spacing, and card borders so open shifts and covered shifts are easy to tell apart at a quick glance.

*Prompts I Used:*
- *"Change the sample shifts so they sound like real jobs at a hockey shop, like skate sharpening, fitting skates, and working the register, with real-sounding names."*
- *"Make it easier to tell which shifts are open and which ones are covered with better badges and spacing."*

**What broke, and how I fixed it:** Adding longer role descriptions pushed the status badges slightly off-center on smaller screens. Adjusting the card header layout kept the role title and status badge lined up cleanly on both desktop and mobile.

**Committed?** Yes — `"Update realistic shift data and improve card badge layout"`

---

## Session 4: Fixing the Page Reload Bug & Checking Rubric Deductions
**Nov 21 — Driver:** Christian Luke  

In my fourth session, I noticed that submitting a new shift on the live page was reloading the browser, adding a `?` to the end of the URL, and leaving Open Shifts stuck at `0`. I opened the browser Console (`F12`) and saw an `Uncaught SyntaxError` caused by a missing closing `});` right after the `reset-board-btn` click listener, which stopped the rest of the JavaScript (including `e.preventDefault()` on the form) from running. Fixing the closing bracket around `reset-board-btn` and changing `- {` to `* {` in the CSS reset got the board loading and submitting shifts properly. I also replaced `"Sparx sharpener"` in the placeholder text with `"Skate sharpener"` so there were no real brand names in the code.

*Prompts I Used:*
- *"When I click Post Shift to Board the page reloads, adds a question mark to the link, and leaves Open Shifts at 0. Fix the submit button and check the brackets near reset-board-btn."*
- *"Replace Sparx sharpener in the placeholder with Skate sharpener so there are no real brand names in the site."*

**What broke, and how I fixed it:** Because `reset-board-btn` was missing its closing `});` right before the simulator code, the browser threw a syntax error and skipped the `post-shift-form` submit listener. Moving `renderShifts();` outside `.forEach(...)` and adding `});` closed the listener properly and stopped the page from reloading.

**Committed?** Yes — `"Fix reset-board-btn closing bracket and remove brand name"`

---

## Session 5: Writing the Business Case and Checking Rubric Rules
**Nov 24 — Driver:** Christian Luke  

In my fifth session, I wrote `project-notes/BUSINESS_CASE.md` (around 1,500 words) explaining ShiftSwap's value proposition, network effects, VRIN moat, and cloud/risk decisions. After saving it, I checked the whole repository and live site to make sure there were no outside libraries, real brand logos, fake login or payment forms, or footer text calling it a student prototype.

*Prompts I Used:*
- *"Does my business case cover everything on the rubric, and is it around 1,500 words?"*

**Committed?** Yes — `"Draft business case and verify rubric rules"`

---

## Session 6: Cleaning Up the Project Log and Verifying Markdown Preview
**Nov 25 — Driver:** Christian Luke  

In my final session, I updated `project-notes/PROJECT_LOG.md` so all of my work sessions, bug fixes, tables, and reflection were complete and matched my repository history. I checked both `BUSINESS_CASE.md` and `PROJECT_LOG.md` in GitHub's Preview tab to confirm that every heading, bullet point, and table lined up cleanly before submitting.

*Prompts I Used:*
- *"Check if my tables and headings in PROJECT_LOG.md line up right in GitHub preview."*

**What broke, and how I fixed it:** Earlier I accidentally pasted triple backticks around a section in `PROJECT_LOG.md`, which made GitHub display it as a raw code block instead of formatted text. Removing those backticks fixed the Preview view immediately.

**Committed?** Yes — `"Complete project log sessions, tables, and reflection"`

---

## Things That Broke

| Date | What went wrong | What I tried | What finally fixed it |
| :--- | :--- | :--- | :--- |
| Nov 15 | Claim Shift input box and buttons looked squished on my phone | Shrunk the font size first, which made the buttons too hard to tap | Added a CSS rule for screens under 520px so the claim box moves onto its own clean row below the shift info |
| Nov 15 | Posting a new shift while filtered to "Covered Only" made the new shift look like it disappeared | Thought the submit button was broken and clicked it twice | Made the form submit function automatically reset the filter back to "All Shifts" |
| Nov 15 | Typing just spaces into the claim name box let a shift be marked as covered | Tested entering blank spaces to see if empty names were blocked | Added `.trim()` in JavaScript so the form requires actual letters before claiming a shift |
| Nov 18 | Longer retail role titles pushed the shift status badge off-center on narrow screens | Shortened the role text | Adjusted the shift card header alignment so badges stay aligned on both phone and laptop views |
| Nov 21 | Clicking Post Shift to Board reloaded the page, added `?` to the URL, and left Open Shifts at 0 | Checked the HTML form tags and searched for `preventDefault()` first | Opened the browser Console, found the missing closing `});` after `reset-board-btn`, and closed the click listener properly |

---

## What a Real Commercial Version Would Need

Right now, ShiftSwap runs in browser memory and resets when you refresh the page. If this were launched as a real paid app for retail stores, it would need:

| Feature we faked or skipped | Why a real company would need it | How hard / expensive? |
| :--- | :--- | :--- |
| Real user logins and roles | Workers should only claim shifts they are trained for (like skate sharpening), and managers need to approve swaps before overtime happens | Medium: use a login service (SaaS), around $50–$200/month as stores grow |
| Shared cloud database | Right now shifts only live in one browser and reset on refresh; coworkers need to see the same live shift board | Medium: a hosted PostgreSQL database (PaaS) plus developer setup |
| SMS and push notifications | Retail workers do not sit at a computer all day, so they need instant text alerts when an urgent shift opens up | Easy to Medium: connect an SMS API (SaaS) paying a few cents per text |
| Payroll and schedule sync | Managers do not want to enter approved shift swaps twice into their official payroll and scheduling software | Hard: requires API integrations and ongoing maintenance |
| Store subscription billing | Stores need a secure way to pay their monthly fee without the startup handling credit card numbers directly | Easy: use a payment processor (SaaS) taking ~2.9% + $0.30 per charge |
| Security, privacy, and audit logs | Employee names, phone numbers, and schedules must be protected, and managers need a record of who approved each swap | Medium: HTTPS encryption, role permissions, and encrypted backups |

---

## Business Reflection: What Building With AI Taught Me About Software

I had no idea how easy it would be to create a working website without much coding skills before I started ShiftSwap. I discovered how much AI can help in developing software after finishing this project. I created a website with features like shift counters, filters, and a simulator by giving it simple instructions. It might have taken a developer several days to create something like this from scratch.

I still had to spend time testing the website and fixing issues even though AI assisted me in writing the majority of the code. I tried it on my computer and phone and discovered problems. For example, when I went to post a shift, the page kept reloading and the claim box did not fit correctly on smaller screens. I discovered that rather than simply stating that something is broken, AI functions better when I describe precisely what I did, what happened, and what I want it to do.

Another important thing I learned is that a company doesn't always gain from having code that works. Other students or businesses might easily replicate ShiftSwap's basic functions because AI makes website development easier. It's likely that a larger scheduling firm could easily develop a comparable website. This shows that ShiftSwap cannot be distinguished only by its code and design.

ShiftSwap would need actual stores and employees to use it on a regular basis in order to succeed. Also, it must build trust and be incorporated into the way managers set up shifts. For example, evaluating dependable workers and simplifying shift changes might encourage retailers to continue using the app. A company may not want to switch platforms if it relies on ShiftSwap on a weekly basis and continues to see its benefits.

Overall, this project taught me that AI can make building software faster and less expensive, but it cannot guarantee a business will succeed. A good idea and a working website are only the beginning. A business also needs customers, trust, and something useful that makes people want to keep coming back. Those things could help ShiftSwap compete over time.
