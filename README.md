# GhostEAD – Ghost Course Hunter (`tool_ghostead`)

A Moodle administration plugin that identifies **ghost courses** (abandoned, empty, or unused courses) and allows administrators to **hide** or **archive** them in bulk, safely and reversibly.

> Status: **0.3.0 – alpha**. Test in a staging environment before using in production.
>
> Compatibility: **Moodle 3.7 or higher** (PHP 7.1+). The code avoids newer PHP syntax to ensure compatibility with older installations.

## How it works

Each course receives a **Ghost Score ranging from 0 to 100**:

| Indicator | Points |
|---|---:|
| No access during the inactivity period (default: 6 months) | 40 |
| No enrolled students | 25 |
| No teachers | 15 |
| Empty course (up to 1 activity, the automatically created announcements forum) | 20 |

Only courses with a score equal to or higher than the configured minimum (default: 60) are displayed in the list. Courses created within the last 30 days are excluded.
