# ShiftSwap Business Case Report

## 1. The Idea
Last summer I worked on the floor at a hockey gear store, and I saw right away how hard it is for hourly workers to get their shifts covered. At SlapShot Outfitters, a busy shop selling hockey equipment and sports gear, people had to text coworkers one by one or leave paper notes whenever they couldn't work. That caused a lot of stress on busy days like weekends when lines of customers were waiting.

For example, when someone on the skate sharpening counter got sick or had something come up, they’d scramble to find a replacement by messaging colleagues one at a time. Managers had the extra headache of making sure the replacement actually knew how to operate the sharpening machine. On busy days, not having the right person there to run key stations caused delays and annoyed customers.

ShiftSwap is a website I developed to address this problem—a place where employees and managers can easily post, claim, and manage shifts. Instead of juggling group chats and calls, everyone can see open shifts in one online spot, accessible from any phone or computer. Employees add details about the time, work area, and any required skills. Then coworkers with the right experience can claim shifts quickly, with just one click.

Stores would pay a monthly subscription. The free plan works for up to 10 employees, perfect for small teams. The Pro Store plan, at $39 per month, covers unlimited staff and includes handy features like skill tags and manager approvals. For businesses with multiple locations, a discounted Multi-Store Regional plan applies.

ShiftSwap also has to be super simple for workers to use. Most hourly employees are busy and won't bother with a site that feels confusing. The layout keeps things clear so people can log in, check the shift details, and claim a spot in just a few clicks. Managers get their own dashboard to approve swaps and watch the schedule, and making everything this straightforward will get staff to actually use it every day.

## 2. Where IT Creates Value
If you look at Porter's Value Chain, ShiftSwap helps a store by improving both daily operations and how staff get managed.

On the store floor, missing someone at the skate sharpening counter or cash register slows everyone down and loses sales during busy rushes. ShiftSwap fixes this by putting every open shift on one page where coworkers can grab them fast, instead of dealing with messy group chats and phone calls.

For managers, scheduling becomes much simpler. Instead of sending message after message to find coverage, managers can see which shifts are open, who’s claimed them, and how fast the gaps are being filled. The system also tracks data on employee reliability and skills, helping managers make smarter decisions.

Saving just a few hours a week on making schedules makes the $39 monthly price worth it. Having reliable shift coverage also stops mistakes and keeps customers from waiting around.

ShiftSwap makes communication between workers and managers way better, too. When everybody uses the same site, messages don't get lost and nobody is confused about who is working. Managers can check the schedule right away instead of asking around for updates, giving them more time to help customers and run the floor.

## 3. Network Effects
ShiftSwap gets more useful as more people at one store start using it. This is a direct network effect, where having more coworkers log in regularly makes it much easier to get shifts covered.

There is also a cross-sided effect because three groups all help each other out: workers posting shifts, workers wanting extra hours, and managers keeping track of the schedule.

When I worked at the hockey shop, if only a few people checked the site, open shifts would sit there and you still had to text coworkers one by one. Once most of the team logs in, shifts get grabbed fast, which keeps everyone happy and helps the store run better.

Our plan to get started focuses on a single store like SlapShot Outfitters, which has about 20 to 30 employees:
- **Single-Store Rollout:** Start ShiftSwap at one busy shop so we can build a steady group of users before going anywhere else.
- **Manager-Backed Onboarding:** Put this week's schedule up on the board for free at first, and ask the manager to tell staff to use ShiftSwap instead of sending texts.
- **Adjacent Expansion:** Once it works well there, bring it to nearby stores and hockey shops that share staff and managers so the network grows naturally.

Down at the bottom of the site, our "Network Density & Shift-Fill Simulator" shows how much easier it is to cover shifts when more people join in. When only a few workers use it, open shifts are tough to fill, but once most of the team is on board, the fill rate goes over 85% and saves managers hours every week.

Getting staff to check the site often is key to making this work. Managers can remind workers to look at ShiftSwap when their shift starts or whenever they want extra hours. Once people see it actually helps them get coverage or pick up work, they will keep coming back, building a habit that makes the site more useful over time.

## 4. Can It Be Copied?
In 2026, it is pretty fast to build a basic site like ShiftSwap, especially when you use AI tools. Anyone with some tech skills could throw a simple shift board together over a weekend. That means just having the idea and basic features won't stop people from copying it.

To stand out, ShiftSwap builds advantages that are tougher to copy, which lines up with the VRIN framework:
- **Valuable:** ShiftSwap tracks real info on who shows up reliably, who knows how to do special jobs like sharpening skates or working cash, and which times are hardest to cover.
- **Rare:** Every store has its own mix of shifts and workers, so this data belongs to that specific business and rivals do not have it.
- **Inimitable:** Building up real shift and attendance history takes months of daily use. A brand-new competitor cannot just drop that data in overnight.
- **Non-substitutable:** Basic spreadsheets or group chats do not track and organize this kind of info nearly as smoothly.

As workers get used to checking ShiftSwap to manage their shifts and pick up extra hours, it creates switching costs. Moving to a different tool means training the whole crew again and probably losing organized records that managers rely on.

Even if another company copies the site, getting managers to switch, hooking it up to payroll, and moving months of attendance history would be a huge headache.

Building good relationships with the stores that use ShiftSwap is another way to stand out. When managers find the platform useful and workers like using it, they are much more likely to tell other businesses about it. Helpful customer support and steady updates will keep stores happy over time. That matters because simply having a working site is not enough to build a real business. Stores need a solid reason to keep paying every month instead of switching to something else.

## 5. Cloud and Operations
Turning the website into a real business takes more tech than the basic version I built. It needs user accounts, manager controls, a database to store skills and shift history, safe monthly payments, alerts, and strong privacy protection.

Rather than renting its own servers (IaaS), it makes sense to use managed cloud services:
- **PaaS (Platform as a Service):** Hosting the app and database in the cloud with automatic updates and backups saves time and hassle for a small team.
- **SaaS (Software as a Service):** Using existing solutions for payments and messaging avoids building those complicated systems from scratch.

Of course, relying on outside providers has risks — price hikes or outages could disrupt ShiftSwap. Regular data backups would protect against this, making it easier to switch providers if needed.

As the business grows, ShiftSwap would also need to make sure the website can handle more employees and stores at the same time. A system that works for one store might struggle if hundreds of locations start using it. The company would need to test the website regularly and fix problems before they affect customers. It would also be important to have someone available to help managers and employees if they have trouble logging in, posting shifts, or using the platform. These steps would help keep the service reliable as more businesses join.

## 6. Risks and Ethics
Because ShiftSwap deals with work schedules and personal details, it has to take privacy and fairness seriously.
- **Employee Privacy:** ShiftSwap shows shift times and keeps phone numbers for alerts, so only approved staff at that store can get in. Coworkers cannot see each other's phone numbers, and all the data is encrypted.
- **Fair Treatment:** Managers might misuse reliability scores to block certain workers from picking up shifts unfairly. To stop that, every qualified worker sees open shifts at the same time. Private notes let staff explain stuff like getting sick or having a family emergency directly to the manager without everyone else seeing.

The goal is to keep scheduling transparent and fair, so everyone gets a chance at shifts based on skills and availability, not biases.

Another concern is making sure employees are not pressured into taking extra shifts. Just because someone is available does not mean they should feel forced to work. ShiftSwap should make it super clear that picking up an extra shift is optional and workers get to choose what fits their schedule. Managers should also respect employees who cannot take extra hours. This would help create a fair workplace where the platform makes scheduling easier without adding more pressure to workers.

Overall, ShiftSwap is meant to solve a problem that I have personally seen while working in retail. It gives employees an easier way to find coverage and gives managers more time to focus on running the store. While there are challenges with getting people to use the platform and competing with other businesses, it has the potential to make shift scheduling faster, easier, and more organized.

AI Disclosure: Used Gemini to brainstorm structure, check rubric alignment, and format sections; all arguments, examples, and wording are my own.
