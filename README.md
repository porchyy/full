# Full

A skill for Antigravity (`agy`) and Codex for taking a software project from a rough idea to a maintained release. It interviews in rounds, recommends practical choices, writes a reviewable plan, then builds in small checked steps **only after you ask it to start building**. It works in the user's language and adapts to web, mobile, backend, and other software projects.

สกิลสำหรับค่อย ๆ ถาม วางแผน แบ่งงาน ลงมือทำ ส่งมอบ และดูแลโปรเจ็กต์ซอฟต์แวร์ต่อ โดยเริ่มเขียนโค้ดหลังจากคุณตรวจแผนและสั่งให้เริ่มทำเท่านั้น (รองรับคำสั่ง `/full` ใน Antigravity / AGY และ `$full` ใน Codex)

## Install

### Antigravity / AGY & Codex (Manual Install)

Download or clone the repository and copy [`skills/full`](skills/full/) to your user skills directory:

- Windows: `%USERPROFILE%\.agents\skills\full\`
- macOS/Linux: `~/.agents/skills/full/`

Check that the installed directory contains `SKILL.md`.

### Codex CLI

With [GitHub CLI's skill command](https://cli.github.com/manual/gh_skill_install):

```sh
gh skill install porchyy/full full --agent codex --scope user
```

Or ask Codex: `$skill-installer install full from https://github.com/porchyy/full/tree/main/skills/full`.

## Use

- **In Antigravity / AGY**: Type `/full` or `$full` followed by your project prompt:
  > `/full ช่วยถามและวางแผนเว็บจองคิวให้ชัดก่อน แล้วค่อยเริ่มเขียนโค้ดเมื่อฉันสั่ง`

- **In Codex**:
  > `$full I want a booking app for a small studio. Ask me what matters and plan it before writing code.`

You can accept its recommended answers in a batch. The skill records decisions in the project's existing planning documents, or in `.full/plan.md` (or `.project-guide/plan.md`) when no suitable document exists. Review and correct the plan, then explicitly tell it to **start building**. It will work through small slices and report checks and remaining work. You can resume later by invoking the skill in the same project.

## Repository layout

```text
skills/
  full/
    SKILL.md    Skill instructions
README.md      Installation and usage
LICENSE        Reuse terms
```

## License

See [`LICENSE`](LICENSE).
