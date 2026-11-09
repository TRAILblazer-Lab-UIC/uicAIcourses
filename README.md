# Explore Undergraduate AI Courses at UIC

A self-contained course browser for the 83 AI-related **undergraduate** courses (90 listings) in the University of Illinois Chicago 2026–2027 Undergraduate Catalog. Graduate-only courses (500-level and above) are not included. A few listed courses are limited to graduate or professional programs; the widget marks them "Program-restricted". It has no database, no server and no outside libraries, and makes no network requests: course data is built into the file, and links to the UIC catalog open in a new tab.

**Live demo:** https://trailblazer-lab-uic.github.io/uicAIcourses/

Course titles, descriptions and prerequisites are quoted word for word from the UIC catalog (checked November 5, 2026). The plain-language guide for each course was written by Claude, an AI assistant, from the catalog text, and is not an official UIC description.

## Files
| File | What it is |
|---|---|
| `index.html` | The widget as a full page (the live demo) |
| `uic-ai-courses.js` | The widget as one script file |
| `uic-ai-courses-embed.html` | The widget as one paste-in block (`<div>` + `<script>`) |
| `UIC-AI-Courses-Guide.pdf` | The printable course guide, linked from the widget header |

## Adding it to another site

**1. Paste into page code.** Copy everything in `uic-ai-courses-embed.html` and paste it into the page's HTML where the widget should appear.

**2. Load the script from this site.**
```html
<div data-uic-ai-courses></div>
<script src="https://trailblazer-lab-uic.github.io/uicAIcourses/uic-ai-courses.js" defer></script>
```

**3. iframe (for a CMS that strips `<script>` tags).**
```html
<iframe src="https://trailblazer-lab-uic.github.io/uicAIcourses/" title="Explore Undergraduate AI Courses at UIC"
        style="width:100%;height:1400px;border:0"></iframe>
```

To link straight to a course, add its code to the page URL, for example `https://trailblazer-lab-uic.github.io/uicAIcourses/#course=CS-412`.

### Options (attributes on the `<div>`)
| Attribute | Values | Default |
|---|---|---|
| `data-tab` | `explore`, `pathways`, `ready`, `saved` (starting tab) | `explore` |
| `data-deeplink` | `on`: keeps the open course in the URL hash | off |
| `data-pdf` | URL of the PDF for the "Download all courses as a PDF" button | `https://trailblazer-lab-uic.github.io/uicAIcourses/UIC-AI-Courses-Guide.pdf` |

The widget runs inside a Shadow DOM, so the host site's CSS won't change its look and its CSS won't leak out. It uses UIC navy and red, works from 320 px phones up, and supports keyboard navigation and screen readers. "My list" is saved only in each visitor's own browser.

## Undergraduate catalog information only
All courses come from the UIC Undergraduate Catalog. Not every course is offered every semester. Check with the department or an advisor before planning a schedule.
