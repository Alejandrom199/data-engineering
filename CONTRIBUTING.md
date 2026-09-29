# Contributing to OpenLearn Courses

Thank you for helping people learn! This registry grows through contributions:
new courses, new versions, fixes and reviews are all welcome.

## Ways to contribute

- **Fix or improve a course** — typos, outdated facts, clearer explanations,
  better diagrams, more questions. Edit the files under `courses/<id>/`, bump
  `version` in its `course.json` (patch for fixes, minor for new content) and
  open a pull request.
- **Add a new course** — see below.
- **Translate a course** — mock exams and the glossary can be offered in
  more languages. Add the language code to `langs` in the exam (or to
  `glossary.langs` in `course.json`) and a `translations.<code>` entry to every
  question or glossary term it serves; `content:validate` tells you what is
  missing. Any language code works (`en`, `pt-BR`…), not only English. See
  "Content languages" in the OpenLearn
  [content model](https://github.com/alenj0x1/open-learn/blob/main/docs/content-model.md).
- **Review pull requests** — accuracy and pedagogy reviews from people who know
  the topic are gold.
- **Propose a course or report a problem** — open an issue with the matching
  template.

## Adding a course

You need a checkout of [OpenLearn](https://github.com/alenj0x1/open-learn)
(Node.js 22.12+, `npm install && npm run build:shared`): it holds the course
standard, the authoring agents and the scripts.

1. **Author it** in the OpenLearn checkout, inside `content/courses/<course-id>/`:
   - with [Claude Code](https://code.claude.com): `/new-course <what you want to teach>`
     (research with sources → syllabus → lessons and labs → review), or
   - by hand: `npm run content:new -- course --id <course-id> --title "<title>"`,
     then units, lessons and labs (see `docs/content-model.md` and
     `docs/creating-a-course.md` there).
2. **Preview it** — `npm run dev` in OpenLearn shows local courses in *Cursos*.
3. **Validate it** — `npm run content:validate -- <course-id>` must report
   **0 errors**.
4. **Copy it here** — the whole folder, including `research/` (the notes and
   citations reviewers use to check facts; it is never shipped to instances),
   to `courses/<course-id>/` of your fork of this repository.
5. **Rebuild the registry** — from the OpenLearn checkout:
   ```bash
   npm run content:registry -- --root <path-to-this-repository>
   ```
   It validates every course, writes `archives/<id>-<version>.zip`, updates
   `registry.json` and the table in `README.md`. Commit all of it.
6. **Open a pull request** and fill in the template.

CI runs `npm run content:registry -- --check`: a pull request fails if any
course is invalid or if the generated files are not up to date.

## Rules

- Contributions are licensed under [CC BY-SA 4.0](LICENSE), like the rest of the
  courses: only submit material you have the right to license that way.
- Course ids are `kebab-case`, unique in this registry, and never reused for a
  different course.
- Every fact is traceable to a source listed in `research/`; prefer official
  documentation.
- Only include material you are allowed to redistribute. Write in your own
  words, never paste copyrighted text or real exam questions, and state the
  licenses of the sources you build on.
- Learner-facing text in the course language; keep the tone friendly and clear.
- Don't edit `registry.json` or `archives/` by hand — regenerate them.

## Review checklist (for maintainers and reviewers)

- [ ] CI is green.
- [ ] Facts match the cited sources; nothing outdated or invented.
- [ ] Lessons teach before they test; questions have one defensible answer and
      useful explanations.
- [ ] Sources and licenses are stated; nothing copied.
- [ ] `version` bumped when an existing course changes.
