<%*
const day = tp.date.now("dddd");
let theme = "General / Study";
let work = [];
let personal = [];
let linkedin = [];

// Monday
if (day === "Monday") {
  theme = "Project / Assignment Day";
  work.push("- [ ] Capstone project work (4–5 hrs)");
  personal.push("- [ ] SORBA admin (1.5 hrs)");
  linkedin.push("- [ ] Comment on 3–5 LinkedIn posts (15–20 min)");
}
// Tuesday
else if (day === "Tuesday") {
  theme = "Python (AM) -> SQL (PM)";
  work.push("- [ ] Python learning / practice (AM)");
  work.push("- [ ] SQL / data engineering practice (PM)");
  personal.push("- [ ] Personal admin (1 hr): budget, appointments, inbox");
}
// Wednesday
else if (day === "Wednesday") {
  theme = "Bootcamp Day 1 (process Tuesday session)";
  work.push("- [ ] Watch Tuesday lab and lecture (~4 hrs)");
  work.push("- [ ] Career Development (1 hr)");
  linkedin.push("- [ ] Reply to post comments / engage (15 min)");
}
// Thursday
else if (day === "Thursday") {
  theme = "Project / Assignment Day";
  work.push("- [ ] Capstone project work (4–5 hrs)");
  personal.push("- [ ] SORBA admin (1.5 hrs)");
}
// Friday
else if (day === "Friday") {
  theme = "Bootcamp Day 2 (process Thursday session)";
  work.push("- [ ] Watch Thursday lab and lecture (~4 hrs)");
  work.push("- [ ] Tech Talk (1 hr)");
  personal.push("- [ ] Personal admin (1 hr)");
  personal.push("- [ ] Meal plan for next week (30–45 min): plan -> grocery list -> order");
  linkedin.push("- [ ] Write and publish weekly LinkedIn post (30–45 min)");
}
// Saturday
else if (day === "Saturday") {
  theme = "Catch-up / Light Study / Weekly Assignment";
  work.push("- [ ] Bootcamp weekly assignment work (2–3 hrs)");
  work.push("- [ ] Finish any bootcamp items not done");
  work.push("- [ ] Review notes or rewatch sections");
}
// Sunday
else if (day === "Sunday") {
  theme = "Weekly Review and Prep";
  work.push("- [ ] Weekly note review");
  work.push("- [ ] Plan next week's assignment blocks");
  personal.push("- [ ] Check personal calendar and appointments");
  linkedin.push("- [ ] Light scroll / reflect (10–15 min)");
  linkedin.push("- [ ] Capture next week’s post idea");
}

const workBlock = work.join("\n");
const personalBlock = personal.join("\n");
const linkedinBlock = linkedin.join("\n");

let out = "";
out += "**Date:** " + tp.date.now("YYYY-MM-DD, dddd") + "\n\n";
out += "**Day Theme:**\n" + theme + "\n\n";

out += "**Recurring:**\n";
out += "**Work / Learning:**\n" + (workBlock ? workBlock : "- (none)") + "\n\n";
out += "**Personal:**\n" + (personalBlock ? personalBlock : "- (none)") + "\n\n";
out += "**LinkedIn / Networking:**\n" + (linkedinBlock ? linkedinBlock : "- (none)") + "\n\n";

out += "**Open Tasks:**\n\n";
out += "| Task | Due Date |\n";
out += "| ---- | -------- |\n";
out += "|      |          |\n\n";

out += "**Completed Tasks:**\n\n";
out += "| Task | Due Date |\n";
out += "| ---- | -------- |\n";
out += "|      |          |\n\n";

out += "**New Tasks:**\n\n";
out += "| Task | Due Date |\n";
out += "| ---- | -------- |\n";
out += "|      |          |\n\n";

out += "**Notes / Thoughts / Wins:**\n\n";

out += "**Time Tracking (optional):**\n";
out += "- Planned deep work: \n";
out += "- Actual deep work: \n\n";

out += "**End-of-Day Check-in (with ChatGPT):**\n";
out += "Here is what I finished today, here is what is still open, and here is what is new.\n";
out += "Update my running task list and generate a fresh plan for the next day.\n";

tR += out;
-%>
