# Project Guide

A Codex skill for taking a software project from a rough idea to a maintained release. It interviews in rounds, recommends practical choices, writes a reviewable plan, then builds in small checked steps **only after you ask it to start building**. It works in the user's language and adapts to web, mobile, backend, and other software projects.

สกิลสำหรับค่อย ๆ ถาม วางแผน แบ่งงาน ลงมือทำ ส่งมอบ และดูแลโปรเจ็กต์ซอฟต์แวร์ต่อ โดยเริ่มเขียนโค้ดหลังจากคุณตรวจแผนและสั่งให้เริ่มทำเท่านั้น

## Install

Copy the [`project-guide`](project-guide/) directory into your Codex skills directory:

- Windows: `%USERPROFILE%\.codex\skills\project-guide\`
- macOS/Linux: `~/.codex/skills/project-guide/`

The installed directory must contain `SKILL.md`. Restart or refresh Codex's skill list if needed. The skill has no required plugins, dependencies, or scripts.

## Use

Invoke `$project-guide` with your idea, or ask Codex to help plan and build a project collaboratively. For example:

> `$project-guide` I want a booking app for a small studio. Ask me what matters and plan it before writing code.

หรือใช้ภาษาไทย: `$project-guide ช่วยถามและวางแผนเว็บจองคิวให้ชัดก่อน แล้วค่อยเริ่มเขียนโค้ดเมื่อฉันสั่ง`

You can accept its recommended answers in a batch. The skill records decisions in the project's existing planning documents, or in `.project-guide/plan.md` when no suitable document exists. Review and correct the plan, then explicitly tell it to **start building**. It will work through small slices and report checks and remaining work. You can resume later by invoking the skill in the same project.

The skill does not choose a framework, hosting provider, or UI style for every project. Those decisions follow the project's requirements and existing code.

## Repository layout

```text
project-guide/
  SKILL.md      Skill instructions
README.md       Installation and usage
LICENSE         Reuse terms
```

## License

See [`LICENSE`](LICENSE).

