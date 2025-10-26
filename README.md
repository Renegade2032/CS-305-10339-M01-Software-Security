1Client & Software Requirements (summary)
Artemis Financial is a mid-sized financial services company that works with a lot of sensitive customer information. They wanted help reviewing and tightening the security of their web app. The main focus was on making sure data transfers were secure (TLS), improving how the app handles input and errors, checking for risky dependencies, and setting up a repeatable process to keep things secure in the future.
 What I did well & why secure coding matters
“I kicked things off by going through the OWASP Top 10 list and just checking the code for anything that looked risky — stuff like data leaks, injection problems, or weak login setups. When I spotted issues, I made a quick plan for how to fix each one. I also ran a quick dependency and static check early on, which turned up a few outdated libraries that needed to be fixed.
“Writing secure code matters a lot — it’s what keeps people’s info safe and helps the company keep its good name. One weak spot can turn into a big (and expensive) mess later, so it’s better to handle it before it happens.”
Most challenging or helpful part of the assessment
“The trickiest part was deciding what to fix first. There were a handful of issues, but some were way more serious than others.” Creating a simple risk matrix made that process a lot clearer and helped me line up what mattered most to the client. That part turned out to be one of the most useful steps overall.
How I increased layers of security & how I’d assess in the future
I used a few layers to make the app stronger:
“I turned on HTTPS/TLS and added secure headers like HSTS and CSP to lock things down more.”
“I tightened up input checks and made sure the app cleaned its outputs to help block injection and XSS stuff.”
Locked down authentication and cut down the amount of info that shows in error messages.
Ran SCA and static analysis to find any weak dependencies.
“If I had to do this again, I’d still lean on tools like Dependency-Check, SpotBugs, and a quick DAST scan. I’d also keep the threat model fresh so new risks don’t sneak up on us.”
Resources, tools, and practices to reuse
“I leaned a lot on OWASP Top 10 and ASVS checklists, plus a few cheatsheets for setting up secure headers.”
Tools that helped: OWASP Dependency-Check for SCA, SpotBugs with FindSecBugs for static scans, and a simple DAST scan in CI.
Good habits to keep: threat modeling early, using least privilege, validating inputs, encoding outputs, and setting CI checks that stop builds on serious issues.
 What I’d show a future employer
I’d show the security report and the steps I used to find and fix the issues. It’s a clear example of how I can spot risks and improve a system without breaking functionality. I’d also share some before-and-after examples — like how I added security headers or cleaned up risky dependencies — to show the real impact of the changes.
