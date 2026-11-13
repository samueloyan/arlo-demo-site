# ARLO demo site

`site.json` is the content of the hero on [ops-demo.intertrace.ai](https://ops-demo.intertrace.ai): the headline, the tagline, an optional banner line and the accent colour.

ARLO changes it like a team member would. Ask ARLO on the demo site (for example "make the banner say we're live in Europe"), and its **Web** agent:

1. reads `site.json`,
2. opens a pull request with the change (Intertrace lets this run: it can be undone),
3. asks to publish it by merging the pull request. Intertrace holds that for a person to approve in the Intertrace inbox. Once approved, the merge runs and the site shows the change.

Engineering issues ARLO files while resolving tickets land in this repository's Issues, labelled `intertrace-demo`.

Fields, checked by the tool server before anything is written:

| Field | Limit |
|---|---|
| `headline` | 3–90 characters |
| `headline_accent` | 0–90 characters |
| `tagline` | 0–400 characters |
| `banner` | 0–140 characters, empty hides it |
| `accent` | one of `indigo`, `emerald`, `amber`, `rose`, `sky`, `violet` |

Everything on the demo is synthetic.
