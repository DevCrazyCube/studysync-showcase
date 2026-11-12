<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="docs/hero-dark.png">
  <img src="docs/hero-light.png" alt="Four StudySync screens on a phone: a week's path, a missed answer with the right one shown, a flashcard and an opened chest" width="100%">
</picture>

# StudySync

**Your course in Moodle or Canvas, turned into practice. Week by week.**

[![Status: pre-launch](https://img.shields.io/badge/status-pre--launch-2f55d4?style=for-the-badge)](https://studysync.nl)
[![Source: private](https://img.shields.io/badge/source-private-1c3494?style=for-the-badge)](#what-this-repository-is)
[![Works with Moodle and Canvas](https://img.shields.io/badge/works%20with-Moodle%20%C2%B7%20Canvas-f2b632?style=for-the-badge)](#how-it-works)

[studysync.nl](https://studysync.nl) · [@studysyncnl](https://www.instagram.com/studysyncnl)

</div>

## What this repository is

An explainer. It holds this page and the pictures on it, and no source code: the app's code is in a
private repository. Every picture is a screenshot of the current app on a demo account with made-up
courses, in the light or dark theme to match your GitHub theme. The one exception is Live: its
pictures show the new Live design, which is being built now.

StudySync is pre-launch. It has no customers yet and runs as a private beta behind invite codes.

## What it does

A student connects their school's learning platform once. StudySync reads the course, keeps what is
study material, and makes practice from it for every week of the course:

| | |
| --- | --- |
| **Flashcards** | From every part of the week's material, with spaced repetition: a card you miss comes back tomorrow, a card you know comes back after 1, 3, 7, 14 and then 30 days |
| **A quiz per week** | Ten multiple-choice questions over the week's material |
| **A cheatsheet per course** | The course on one page |
| **A path per course** | Each week is a short row of steps, so there is always one obvious next thing to do |

The practice is made by AI and labelled as AI-made on every card and question. The course material
stays the reference.

## How it works

```mermaid
flowchart LR
    A[Moodle or Canvas] -->|the student connects once| B[Sync]
    B --> C{Study material?}
    C -->|slides, readers, code, lecture video links| D[AI makes cards, a quiz and a cheatsheet]
    C -->|rubrics, schedules, announcements| X[left out]
    D --> E[The week's path]
    E --> F[Practice, review, rewards]
```

1. **Connect.** Moodle with a personal web-service token; Canvas through the school's own sign-in.
2. **Sync.** Courses, weeks, files and deadlines come in. Rubrics, schedules, attendance lists and
   other course admin are left out, and a section with nothing to learn gets no deck.
3. **Generate.** All of the material is used, in chunks when it is long. Nothing is sampled away.
4. **Practise.** The week's steps, then a week check. Cards you practised come back when they are due.

## The week's path

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="docs/desk-path-dark.png">
  <img src="docs/desk-path-light.png" alt="A course's path on a desktop: the week's banner, then round keys for Terms, Meaning, Recall and Mixed, the path chest and the week check, with the week's place beside the trail" width="100%">
</picture>

Each week of a course is a place on a campus, and its steps stand along a trail: match the words,
pick the meaning, type it, all of it mixed, then the week check. The next step is the lit one, and
your own character waits beside it.

<table>
  <tr>
    <td width="25%"><picture><source media="(prefers-color-scheme: dark)" srcset="docs/phone-home-dark.png"><img src="docs/phone-home-light.png" alt="Home on a phone: the next step on its campus picture, today's goal with its chest, the cards to review and the courses"></picture></td>
    <td width="25%"><picture><source media="(prefers-color-scheme: dark)" srcset="docs/phone-path-dark.png"><img src="docs/phone-path-light.png" alt="A week's path on a phone"></picture></td>
    <td width="25%"><picture><source media="(prefers-color-scheme: dark)" srcset="docs/phone-question-dark.png"><img src="docs/phone-question-light.png" alt="Pick the meaning: What is sampling bias? with four answers"></picture></td>
    <td width="25%"><picture><source media="(prefers-color-scheme: dark)" srcset="docs/phone-not-quite-dark.png"><img src="docs/phone-not-quite-light.png" alt="A missed answer: Not quite, with the right answer below"></picture></td>
  </tr>
  <tr>
    <td align="center"><b>Home</b><br>One next step</td>
    <td align="center"><b>Path</b><br>The week as steps</td>
    <td align="center"><b>A step</b><br>Pick the meaning</td>
    <td align="center"><b>A miss</b><br>"Not quite", never a red buzzer</td>
  </tr>
</table>

## Cards and quizzes

<table>
  <tr>
    <td width="25%"><picture><source media="(prefers-color-scheme: dark)" srcset="docs/phone-card-front-dark.png"><img src="docs/phone-card-front-light.png" alt="The front of a flashcard: What is a p-value?"></picture></td>
    <td width="25%"><picture><source media="(prefers-color-scheme: dark)" srcset="docs/phone-card-back-dark.png"><img src="docs/phone-card-back-light.png" alt="The back of the flashcard, with Again and Got it"></picture></td>
    <td width="25%"><picture><source media="(prefers-color-scheme: dark)" srcset="docs/phone-quiz-dark.png"><img src="docs/phone-quiz-light.png" alt="A week quiz question with four answers"></picture></td>
    <td width="25%"><img src="docs/live-phone-pads.png" alt="StudySync Live on a phone: four big answer keys, A to D, under a progress bar"></td>
  </tr>
  <tr>
    <td align="center"><b>Card, front</b></td>
    <td align="center"><b>Card, back</b><br>Again or Got it</td>
    <td align="center"><b>Week quiz</b><br>No answer key is sent before you answer</td>
    <td align="center"><b>Live</b><br>The phone is the buzzer</td>
  </tr>
</table>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="docs/desk-match-dark.png">
  <img src="docs/desk-match-light.png" alt="Match the pairs on a desktop: terms on the left, meanings on the right, the student's character beside them" width="100%">
</picture>

## Live, for the whole class

<img src="docs/live-lobby.png" alt="The Live lobby on the big screen: join at studysync.nl/live with a six-digit code and a QR code, 24 players standing as their characters with made-up names" width="100%">

**Live** is a quiz for the whole class, on Canvas courses a teacher teaches: the teacher opens a lobby
on the big screen and phones join with the code. The question stays on the screen; phones only show
the answer keys. By default every player gets a made-up name and a made-up character, so the board
says nothing about who is who.

<table>
  <tr>
    <td width="50%"><img src="docs/live-reveal.png" alt="The reveal on the big screen: how the class answered, as four columns, the right one marked, with why it is right"></td>
    <td width="50%"><img src="docs/live-podium.png" alt="The podium: the top three characters on their plinths with crowns, and how much the class got right together"></td>
  </tr>
  <tr>
    <td align="center"><b>The reveal</b><br>How the class answered, and why</td>
    <td align="center"><b>The podium</b><br>The top three, crowned</td>
  </tr>
</table>

<table>
  <tr>
    <td width="25%"><img src="docs/live-phone-name.png" alt="A phone after joining: You are Steady Heron, with a made-up character"></td>
    <td width="25%"><img src="docs/live-phone-pads.png" alt="The phone during a question: four big answer keys"></td>
    <td width="25%"><img src="docs/live-phone-correct.png" alt="The phone after the reveal: Correct, plus 846 points, the character cheering"></td>
    <td width="25%"><img src="docs/live-phone-podium.png" alt="The phone at the end: 2nd place, on the podium, look at the screen"></td>
  </tr>
  <tr>
    <td align="center"><b>Join</b><br>A made-up name</td>
    <td align="center"><b>Answer</b><br>The phone is the buzzer</td>
    <td align="center"><b>Reveal</b><br>Your own result only</td>
    <td align="center"><b>End</b><br>Your place</td>
  </tr>
</table>

<sub>The Live pictures show the new Live design, drawn from the approved prototype. It is being built
now; until it ships, the app still shows the previous Live screens.</sub>

## Rewards, without a shop that takes money

<table>
  <tr>
    <td width="25%"><img src="docs/phone-chest-climb-light.png" alt="A week chest on a dark screen, rarity Common, three taps to go"></td>
    <td width="25%"><img src="docs/phone-chest-light.png" alt="The opened chest, now Rare: 40 diamonds and a streak freeze"></td>
    <td width="25%"><picture><source media="(prefers-color-scheme: dark)" srcset="docs/phone-shop-dark.png"><img src="docs/phone-shop-light.png" alt="The Shop on a phone: this week's pick, a telescope, unlocked at level 15"></picture></td>
    <td width="25%" valign="top">
      <br>
      <b>Earned by studying, never bought.</b><br><br>
      Studying pays XP and diamonds. Diamonds unlock things for your character and its room.
      Nothing in StudySync can be bought with money. What a chest holds is fixed when you earn
      it; the taps only show it, and the odds are in the Shop.<br><br>
      A school decides whether rewards are on at all.
    </td>
  </tr>
  <tr>
    <td align="center"><b>A chest</b><br>Common to start</td>
    <td align="center"><b>Opened</b><br>What it held</td>
    <td align="center"><b>Shop</b><br>Unlock, never buy</td>
    <td></td>
  </tr>
</table>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="docs/desk-shop-dark.png">
  <img src="docs/desk-shop-light.png" alt="The Shop on a desktop: departments on the left, this week's pick, a telescope (reach level 15, then 650 diamonds), and the week's picks" width="100%">
</picture>

<table>
  <tr>
    <td width="50%"><picture><source media="(prefers-color-scheme: dark)" srcset="docs/desk-cell-dark.png"><img src="docs/desk-cell-light.png" alt="Make your cell: shapes, colours, eyes, mouth, hair and moves"></picture></td>
    <td width="50%"><picture><source media="(prefers-color-scheme: dark)" srcset="docs/desk-study-dark.png"><img src="docs/desk-study-light.png" alt="Study on a desktop: continue, the cards due, and the courses as campuses"></picture></td>
  </tr>
  <tr>
    <td align="center"><b>Your cell</b><br>Every student has a character that studies along</td>
    <td align="center"><b>Study</b><br>Every course is its own campus</td>
  </tr>
</table>

## For schools

- **Students' own access.** Each student's material comes in through that student's own access to
  the learning platform.
- **Staff see little.** Staff accounts a school sets up see a roster with last activity and
  programme totals. Nobody on staff sees a student's answers, scores or rewards.
- **Tokens stay on the server.** Learning-platform tokens are encrypted (AES-256-GCM) and never
  reach the browser; files are downloaded through the server.
- **AI is labelled.** Every card and question says it is AI-generated, with its sources and a way
  to give feedback.
- **Calm mode.** One switch, or the device's reduced-motion setting, and nothing moves on its own.
- **Data location.** The database is in the EU.

Brightspace, Blackboard and other platforms are not supported yet.

## Built with

| Part | What |
| --- | --- |
| Frontend | Next.js 16, TypeScript (strict), CSS variables, Zustand, Framer Motion |
| Backend | Node.js, Express, PostgreSQL, a Postgres-backed job queue |
| AI | Anthropic Claude for cards, quizzes, cheatsheets and summaries; Google Gemini as a fallback, unless a school's deployment is pinned to Anthropic |
| Checks | Type checks and tests on every push; tests that fail when a rule is broken, such as an untrue claim on the website or an answer key sent too early |

The drawings (the campus, the characters, the chests, the icons) are the app's own SVG, drawn in
code. There are no stock illustrations.

## How it is built

By one person directing AI coding agents, mostly [Claude Code](https://claude.com/claude-code). The
direction, the rules the agents work under, and the checking are mine. The skills that came out of
that work are public: see [my profile](https://github.com/DevCrazyCube).

## Not in this repository

- The source code.
- Numbers about users. There are none to show before launch.
- A price. Pricing is discussed with schools.

## Contact

[studysync.nl](https://studysync.nl) · [@studysyncnl on Instagram](https://www.instagram.com/studysyncnl) · [Joyren Terken on LinkedIn](https://www.linkedin.com/in/joyren-terken-0bb02429a)

<sub>Screenshots taken 2026-11-12 from the current app. © 2026 Joyren Terken. The pictures and text here are not open source; ask before reusing them.</sub>
