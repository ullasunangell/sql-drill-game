# SQL Drill Game

A self-contained, gamified web app for drilling SQL fundamentals under timed, exam-style conditions. It's built to build speed and intuition for reading queries and predicting their results, which is what SQL assessments and technical interviews actually test.

https://sql-drill-game.netlify.app

## Why this exists

SQL assessments reward more than knowing the syntax. Marks get lost on the classic traps: `= NULL` instead of `IS NULL`, `NOT IN` returning nothing when a `NULL` sneaks into the list, `WHERE` vs `HAVING`, or a `LEFT JOIN` quietly turning into an inner join because of a filter in the wrong clause. This tool turns passive reading into active, timed retrieval practice across the full breadth of a SQL fundamentals syllabus, so that none of it is a surprise on the day.

## How it works

- **90-second timed drills**: a table, query, or concept question is shown, you work out the result under time pressure, then reveal and self-grade
- **Reveal-first grading**: see the correct answer and explanation before marking yourself right or wrong, so every question reinforces the concept either way
- **Smart question selection**: the picker prioritises topics with fewer attempts first and cycles through every question in a topic before repeating any, so you see the full easy-to-hard range
- **Topic mastery tracking**: per-topic accuracy bars (Shaky / Getting there / Locked in) persist across sessions, so weak spots are visible at a glance
- **Daily + all-time stats**: today's session resets independently from lifetime score and mastery data, so a reset never wipes long-term progress. On the same browser and device, a normal refresh won't touch your stats
- **Readiness goal**: a target (85% overall accuracy, minimum reps per topic) that flags when every topic has been drilled enough, at high enough accuracy, to trust the number
- **Streaks and badges**: lightweight gamification to keep repetition engaging

## Topics covered

SQL basics and syntax; `SELECT` and `DISTINCT`; `WHERE` with `AND` / `OR` / `NOT`; `ORDER BY` and `TOP` / `LIMIT`; `NULL` values and null functions; `INSERT` / `UPDATE` / `DELETE`; aggregate functions (`MIN`, `MAX`, `COUNT`, `SUM`, `AVG`); `LIKE`, wildcards, `IN` and `BETWEEN`; aliases; joins (inner, left, right, full, self, and the accidental Cartesian product); `UNION` / `UNION ALL`; `GROUP BY` and `HAVING`; `EXISTS` / `ANY` / `ALL`; `SELECT INTO` and `INSERT INTO SELECT`; `CASE`; stored procedures; create, drop and alter for databases and tables; constraints (`NOT NULL`, `UNIQUE`, primary and foreign keys, `CHECK`, `DEFAULT`); indexes and auto increment; dates; views; and SQL injection with parameterised queries and prepared statements.

## Tech

Single-file HTML/CSS/vanilla JavaScript: no build step, no framework, no backend. Progress is saved to the browser's `localStorage`, so it persists across sessions on the same device without an account or server.

## Running locally

Clone the repo and open `index.html` directly in a browser.

```bash
git clone https://github.com/<your-username>/sql-drill-game.git
cd sql-drill-game
open index.html
```

## Deployment

Deployed as a static site via Netlify. Any static host (GitHub Pages, Vercel, Netlify) works the same way, since there's no server-side component.
