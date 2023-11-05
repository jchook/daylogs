Daylogs
=======

![Status](https://img.shields.io/badge/Status-Experimental-red)

Daylogs enables the plaintext accounting equivalent of a workhour tracking
system, to-do list, and journal.

You can easily keep a cohesive record of workhours and daily notes using simple
markdown files and use a few dead-simple plaintext tools to generate
timesheets, invoices, to-do lists, or rediscover critical information from your
journal.

Since the data is "just markdown" and the default tools are "just bash", the
entire ecosystem is hackable and extensible with minimal effort.


Format Example
--------------

See an example Daylog below to demonstrate the format I have used since 2018.

```markdown
# Project Name

- Time entry 1
- Time entry 2

4.5h

## Notes

Freeform notes here including:

- [ ] An incomplete to-do item
- [x] A completed to-do item

Here I typically paste detailed error messages, sql queries, and other
important information that doesn't have a canonical home, but can be useful at
a later date.


# Personal

Here I can log some personal notes about my day. I can also have personal
projects such as diet, exercise, etc where I track specifics over time.

```

Approach
--------

Each day has a single master document where all types of information can be
easily recorded, offering minimal friction and a simple organization strategy.

My sister-in-law first demonstrated this approach to me when she was at Uni.
Instead of organizing her notebooks by course, she would store notes and
information chronologically in a unified notebook. This seems counter-intuitive
at first, but it exhibits a strangely satisfying compatibility with the way
memory and the mind work. It may seem hard to appreciate until you try it.

Chiefly, this approach enables a very low-friction process of recording key
information for any subject, requiring only a heading and a date on each entry,
without tedious bookkeeping of any kind.

Combined with tools of the digital age, one can easily compartmentalize and
group related information aftwards. This frees up your active mind and workflow
to simply record the information, without worrying about organizing it beyond
a simple date and heading.

This approach is very compatible with other productivity modalities such as GTD
(Getting Things Done). It is analgous to the "inbox" mechanism that can be
automatically and/or manually sorted at a later time, when it's time to address
the bigger picture.


Tools
-----

Again, the tools consist of dead-simple bash scripts that can be used to
quickly start new daylogs, glean information from existing daylogs, or search
daylogs.

Scripts respect the environment variable `DAYLOGS_HOME` which defaults to `~/.daylogs`.

The base system provides three very simple helper scripts:

- `daylog` - create a new daylog or modify an existing daylog in `$EDITOR`
- `todo` - list to-dos across a subset of daylogs
- `hours` - list hours across a subset of daylogs


Motivation
----------

Many tools exist for freelancers to log their time, generate invoices, manage
expenses, to-dos, etc. However, many of these tools come with crippling
friction, limitations, or disjointed approaches that add a burdon to recording
key information while maintaining a focused workflow.

- Time tracking apps add unnecessary friction
  - Can result in unlogged or improperly logged work hours
  - Can become a job in itself to maintain
  - Add just enough burdon to break concentration when already in a good flow
  - e.g. Web-based solutions require a slow log-in process
  - e.g. Desktop solutions only work exclusively on macOS or Windows
  - e.g. Companion mobile apps provide only limited capabilities
- They typically do not provide a unified solution for logging notes and information
  - Cannot keep notes and detailed descriptions alongside workhour logs
  - Requires special software that is not hackable/extensible by the user
- They focus solely on business concerns, and do not provide a holistic approach to lifestyle and work.
  - Attaching copious notes related to workhour logs can be extremely valuable in the event of an employer dispute or recurring issues.
  - Feeling free to attach images, diary entries, etc turns the daylogs into a lifelong journal of daily activity that can be used for a wide range of tasks such as tracking habits, diet, etc and providing a meaningful organized record for posterity.



