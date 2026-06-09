---
title: "Daily Schedule"
aliases:
  - "Schedule"
  - "Routine"
tags:
  - para/area
  - status/active
  - topic/productivity
created: {{date:YYYY-MM-DDTHH:mm:ssZ}}
updated: {{date:YYYY-MM-DDTHH:mm:ssZ}}
type: "area"
id: "{{date:YYYYMMDDHHmm}}"
source: ""
---

# Daily Schedule

<!-- INSTRUCTIONS: Replace all {{placeholders}} with your own data. -->
<!-- Delete this comment block when done. -->
<!-- Keep the schedule realistic — only fill in what you'll actually do. -->

> Daily routine — work, health, personal time, and rest balanced.

---

> **Note:** This is a _planned_ schedule template. Real actual times are logged in the daily note (`dailyNote/YYYY-MM-DD.md` Log table). Times here are estimates.

## Overview

```
  ┌──────────────────────────────────────────────┐
  │              SCHEDULE SNAPSHOT                │
  ├──────────────┬───────────────────────────────┤
  │  WAKE UP     │ {{wake_time}}                   │
  │  SLEEP       │ {{sleep_time}}                  │
  │  TOTAL HRS   │ {{awake_hours}} hours (awake)   │
  │  REVIEW      │ {{review_frequency}}            │
  └──────────────┴───────────────────────────────┘
```

---

## Weekday Schedule

<!-- INSTRUCTIONS: Fill in your weekday time blocks. Use 30min minimum granularity. -->
<!-- Category options: Career, Personal, Health, Income, Finance, Learning, Social -->

| Time        | Activity                   | Category | Duration | Notes                     |
| ----------- | -------------------------- | -------- | -------- | ------------------------- |
| {{time}}    | {{activity}}               | {{cat}}  | {{dur}}  | {{notes}}                 |
| {{time}}    | {{activity}}               | {{cat}}  | {{dur}}  | [[linked-area]]           |
| {{time}}    | {{activity}}               | {{cat}}  | {{dur}}  |                           |
| {{time}}    | {{activity}}               | {{cat}}  | {{dur}}  |                           |
| {{time}}    | {{activity}}               | {{cat}}  | {{dur}}  |                           |
| {{time}}    | {{activity}}               | {{cat}}  | {{dur}}  |                           |
| {{time}}    | {{activity}}               | {{cat}}  | {{dur}}  |                           |
| {{time}}    | {{activity}}               | {{cat}}  | {{dur}}  |                           |
| {{time}}    | {{activity}}               | {{cat}}  | {{dur}}  |                           |
| {{time}}    | {{activity}}               | {{cat}}  | {{dur}}  |                           |
| {{time}}    | {{activity}}               | {{cat}}  | {{dur}}  |                           |
| {{time}}    | {{activity}}               | {{cat}}  | {{dur}}  |                           |
| {{time}}    | {{activity}}               | {{cat}}  | —        |                           |

### Visual Timeline

<!-- INSTRUCTIONS: Rebuild this ASCII timeline to match your schedule above. -->

```
  {{start}} ── {{t2}} ──────── {{t3}} ──────── {{t4}} ── {{t5}} ──────── {{t6}}
  │ {{act}} │{{act}} │ {{act}}   │ {{act}}     │{{act}} │ {{act}}      │
  │        │       │           │            │       │              │
  ──────────────────────────────────────────────────────────────────────
  {{t6}} ── {{t7}} ── {{t8}} ──────── {{t9}} ──────── {{t10}} ── {{t11}}
  │{{act}} │{{act}} │{{act}}    │ {{act}}     │ {{act}}  │{{act}} │
  │        │       │           │            │         │       │
  ────────────────────────────────────────────────────────────────────
  {{t11}} ── {{t12}} ── {{t13}}
  │{{act}}  │{{act}}  │{{act}}
  │         │         │
  ──────────────────────
```

---

## Time Breakdown

<!-- INSTRUCTIONS: Sum up hours by category from the schedule above. -->

| Category                             | Hours | % of Day | Notes                           |
| ------------------------------------ | ----- | -------- | ------------------------------- |
| **{{cat_1}}**                        | {{h}} | {{pct}}  | {{notes}}                       |
| **{{cat_2}}**                        | {{h}} | {{pct}}  | {{notes}}                       |
| **{{cat_3}}**                        | {{h}} | {{pct}}  | {{notes}}                       |
| **{{cat_4}}**                        | {{h}} | {{pct}}  | {{notes}}                       |
| **{{cat_5}}**                        | {{h}} | {{pct}}  | {{notes}}                       |
| **Sleep**                            | {{h}} | —        | {{sleep_time}}–{{wake_time}}   |

---

## Daily Priorities

<!-- INSTRUCTIONS: Rank your top daily tasks by importance. -->

| #   | Task                          | Time Block  | Hours | Linked              |
| --- | ----------------------------- | ----------- | ----- | ------------------- |
| 1   | {{task}}                      | {{time}}    | {{h}}  | [[linked-area]]     |
| 2   | {{task}}                      | {{time}}    | {{h}}  | [[linked-area]]     |
| 3   | {{task}}                      | {{time}}    | {{h}}  |                     |
| 4   | {{task}}                      | {{time}}    | {{h}}  |                     |
| 5   | {{task}}                      | {{time}}    | {{h}}  | [[linked-area]]     |
| 6   | {{task}}                      | {{time}}    | {{h}}  |                     |
| 7   | {{task}}                      | {{time}}    | {{h}}  |                     |
| 8   | {{task}}                      | {{time}}    | {{h}}  |                     |

---

## Weekend Variations

<!-- INSTRUCTIONS: Describe how weekends differ from weekdays. -->

| Day           | Schedule                                                                                                              |
| ------------- | --------------------------------------------------------------------------------------------------------------------- |
| **Saturday**  | {{saturday_description}}                                                                                             |
| **Sunday**    | {{sunday_description}}                                                                                               |

### Saturday Schedule

| Time        | Activity                       | Category | Duration |
| ----------- | ------------------------------ | -------- | -------- |
| {{time}}    | {{activity}}                   | {{cat}}  | {{dur}}  |
| {{time}}    | {{activity}}                   | {{cat}}  | {{dur}}  |
| {{time}}    | {{activity}}                   | {{cat}}  | {{dur}}  |
| {{time}}    | {{activity}}                   | {{cat}}  | {{dur}}  |
| {{time}}    | {{activity}}                   | {{cat}}  | {{dur}}  |
| {{time}}    | {{activity}}                   | {{cat}}  | {{dur}}  |
| {{time}}    | {{activity}}                   | {{cat}}  | {{dur}}  |
| {{time}}    | {{activity}}                   | {{cat}}  | {{dur}}  |
| {{time}}    | {{activity}}                   | {{cat}}  | {{dur}}  |
| {{time}}    | {{activity}}                   | {{cat}}  | —        |

### Sunday Schedule

| Time        | Activity                       | Category | Duration |
| ----------- | ------------------------------ | -------- | -------- |
| {{time}}    | {{activity}}                   | {{cat}}  | {{dur}}  |
| {{time}}    | {{activity}}                   | {{cat}}  | {{dur}}  |
| {{time}}    | {{activity}}                   | {{cat}}  | {{dur}}  |
| {{time}}    | {{activity}}                   | {{cat}}  | {{dur}}  |
| {{time}}    | {{activity}}                   | {{cat}}  | {{dur}}  |
| {{time}}    | {{activity}}                   | {{cat}}  | {{dur}}  |
| {{time}}    | {{activity}}                   | {{cat}}  | {{dur}}  |
| {{time}}    | {{activity}}                   | {{cat}}  | {{dur}}  |
| {{time}}    | {{activity}}                   | {{cat}}  | {{dur}}  |
| {{time}}    | {{activity}}                   | {{cat}}  | —        |

---

## Weekly Time Summary

<!-- INSTRUCTIONS: Calculate total hours per category across all 7 days. -->

| Category                             | Weekday (5d) | Saturday | Sunday  | **Total/Week** |
| ------------------------------------ | ------------ | -------- | ------- | -------------- |
| **{{cat_1}}**                        | {{h}} hrs    | {{h}} hrs | {{h}} hrs | **{{h}} hrs**  |
| **{{cat_2}}**                        | {{h}} hrs    | {{h}} hrs | {{h}} hrs | **{{h}} hrs**  |
| **{{cat_3}}**                        | {{h}} hrs    | {{h}} hrs | {{h}} hrs | **{{h}} hrs**  |
| **{{cat_4}}**                        | {{h}} hrs    | {{h}} hrs | {{h}} hrs | **{{h}} hrs**  |
| **{{cat_5}}**                        | {{h}} hrs    | {{h}} hrs | {{h}} hrs | **{{h}} hrs**  |

```
  ┌─────────────────────────────────────────────────────────┐
  │                    WEEKLY TIME PIE                        │
  ├──────────────┬────────────────────────────────────────────┤
  │  {{cat_1}}   │ {{bars}}  {{h}} hrs ({{pct}}%)             │
  │  {{cat_2}}   │ {{bars}}  {{h}} hrs ({{pct}}%)             │
  │  {{cat_3}}   │ {{bars}}  {{h}} hrs ({{pct}}%)             │
  │  {{cat_4}}   │ {{bars}}  {{h}} hrs ({{pct}}%)             │
  │  {{cat_5}}   │ {{bars}}  {{h}} hrs ({{pct}}%)             │
  └──────────────┴────────────────────────────────────────────┘
```

---

## Weekly Review Checklist

<!-- INSTRUCTIONS: Define what you review each week and when. -->

| Day    | Time    | What to Review                                        |
| ------ | ------- | ----------------------------------------------------- |
| {{day}} | {{time}} | {{review_item_1}}                                    |
| {{day}} | {{time}} | {{review_item_2}}                                    |
| {{day}} | {{time}} | {{review_item_3}}                                    |
| {{day}} | {{time}} | {{review_item_4}}                                    |
| {{day}} | {{time}} | Plan next week priorities                            |

---

## References

<!-- INSTRUCTIONS: Link to all related files in your vault. -->

- [[me]] — big goals and master task list
- {{additional_links}}
