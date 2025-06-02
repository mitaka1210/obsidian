---
tags:
  - лицеви
date: <% tp.date.now("YYYY-MM-DD") %>
day: <% tp.date.now("dddd") %>
type: pushups
totalPushUps: ${totalPushUps}
seriesAll: ${totalSeries}
---
<%*
const date = tp.date.now("YYYY-MM-DD");
const day = tp.date.now("dddd");

// Попитай за броя лицеви във всяка серия
const s1 = await tp.system.prompt("Брой лицеви в 1-ва серия:");
const s2 = await tp.system.prompt("Брой лицеви във 2-ра серия:");
const s3 = await tp.system.prompt("Брой лицеви в 3-та серия:");

// Пресметни общия брой
const totalPushUps = Number(s1) + Number(s2) + Number(s3);

// Попитай за броя серий
const seriesAll = await tp.system.prompt("Брой  серий");
// Пресметни общия брой
const totalSeries = Number(seriesAll);

tR += `---
tags: [лицеви]
date: ${date}
day: ${day}
type: pushups
total: ${totalPushUps}
series:
  - ${seriesAll}
---
💪 **Лицеви упори — ${date} (${day})**

🧮 **Серии:**
- 1-ва: ${s1}
- 2-ва: ${s2}
- 3-ва: ${s3}

✅ **Общо лицеви:** ${totalPushUps}
** Общо серий: ** ${totalSeries}
`;
%>
