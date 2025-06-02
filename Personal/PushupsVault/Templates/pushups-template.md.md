---
tags:
  - лицеви
date: <% tp.date.now("YYYY-MM-DD") %>
day: <% tp.date.now("dddd") %>
type: pushups
total: ${total}
series:
---
<%*
const date = tp.date.now("YYYY-MM-DD");
const day = tp.date.now("dddd");

// Попитай за броя лицеви във всяка серия
const s1 = await tp.system.prompt("Брой лицеви в 1-ва серия:");
const s2 = await tp.system.prompt("Брой лицеви във 2-ра серия:");
const s3 = await tp.system.prompt("Брой лицеви в 3-та серия:");

// Пресметни общия брой
const total = Number(s1) + Number(s2) + Number(s3);

tR += `---
tags: [лицеви]
date: ${date}
day: ${day}
type: pushups
total: ${total}
series:
  - ${s1}
  - ${s2}
  - ${s3}
---
// Пресметни общия брой  
const totalSeries = Number(s1) + Number(s2) + Number(s3);

💪 **Лицеви упори — ${date} (${day})**

🧮 **Серии:**
- 1-ва: ${s1}
- 2-ра: ${s2}
- 3-та: ${s3}

✅ **Общо:** ${total}
`;
%>
