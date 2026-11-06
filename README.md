# Project Guide

A Codex skill for taking a software project from a rough idea to a maintained release. It interviews in rounds, recommends practical choices, writes a reviewable plan, then builds in small checked steps **only after you ask it to start building**. It works in the user's language and adapts to web, mobile, backend, and other software projects.

สกิลสำหรับค่อย ๆ ถาม วางแผน แบ่งงาน ลงมือทำ ส่งมอบ และดูแลโปรเจ็กต์ซอฟต์แวร์ต่อ โดยเริ่มเขียนโค้ดหลังจากคุณตรวจแผนและสั่งให้เริ่มทำเท่านั้น

## Install in Codex

With [GitHub CLI's skill command](https://cli.github.com/manual/gh_skill_install):

```sh
gh skill install porchyy/full project-guide --agent codex --scope user
```

Or ask Codex: `$skill-installer install project-guide from https://github.com/porchyy/full/tree/main/skills/project-guide`.

For a manual install, download the repository ZIP and copy [`skills/project-guide`](skills/project-guide/) to your user skills directory:

- Windows: `%USERPROFILE%\.agents\skills\project-guide\`
- macOS/Linux: `~/.agents/skills/project-guide/`

Check that the installed directory contains `SKILL.md`, then start a new Codex session and invoke `$project-guide`. The skill needs no plugins, dependencies, or scripts.

## Use

Invoke `$project-guide` with your idea, or ask Codex to help plan and build a project collaboratively. For example:

> `$project-guide` I want a booking app for a small studio. Ask me what matters and plan it before writing code.

หรือใช้ภาษาไทย: `$project-guide ช่วยถามและวางแผนเว็บจองคิวให้ชัดก่อน แล้วค่อยเริ่มเขียนโค้ดเมื่อฉันสั่ง`

You can accept its recommended answers in a batch. The skill records decisions in the project's existing planning documents, or in `.project-guide/plan.md` when no suitable document exists. Review and correct the plan, then explicitly tell it to **start building**. It will work through small slices and report checks and remaining work. You can resume later by invoking the skill in the same project.

The skill does not choose a framework, hosting provider, or UI style for every project. Those decisions follow the project's requirements and existing code.

## Repository layout

```text
skills/
  project-guide/
    SKILL.md    Skill instructions
README.md      Installation and usage
LICENSE        Reuse terms
```

## License

See [`LICENSE`](LICENSE).

