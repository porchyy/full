---
name: project-guide
description: Guide a software project from discovery through UX, architecture, small implementation steps, delivery, and maintenance. Use when the user wants a project planned and built collaboratively; start with questions and a reviewable plan before writing code.
---

# Project Guide

Guide the whole project without rushing past decisions. Work in the user's language. Adapt the depth of each phase to the project's size and existing work.

## 1. Discover

Read the available request, repository, docs, and current state first. Identify the user's intended project directory; the current working directory may be a skill checkout or another unrelated workspace. Find facts yourself; ask the user for choices, goals, and constraints you cannot infer. If there is no project directory yet, work from the idea.

Restate the goal and define what a successful first usable version would do. Separate confirmed facts, assumptions, recommendations, and open decisions. Do not prescribe a stack before learning the constraints.

## 2. Interview in rounds

Map decisions by dependency. In each round, ask the questions that can be answered now; hold dependent questions for a later round. For each question, give a recommended answer and a short reason or tradeoff. Let the user accept recommendations together. Revisit the map after each answer.

Cover only relevant areas:

- Users, core journeys, scope, success criteria, budget, time, and constraints.
- UX flows, screens, accessibility, visual direction, content, and languages when there is a user interface.
- Data, permissions, privacy, integrations, and failure cases when the product handles them.
- Frontend, backend, hosting, operations, and technology choices when those choices affect delivery.

Stop interviewing when the decisions needed for the next planning or build step are settled. Record later decisions as deferred with a trigger for revisiting them. Do not make the user answer questions whose answers can be found in the project.

## 3. Plan before code

Present a reviewable plan in the user's language:

1. Problem, users, agreed scope, and first usable outcome.
2. Recommended UX and technical approach, with reasons and meaningful alternatives.
3. Ordered small work slices; each has an observable result and a check for completion.
4. Impact on existing code, data, users, integrations, and operations; risks and unresolved decisions.
5. The first slice ready to build.

For an existing project, trace the relevant flow and callers before proposing changes. Reuse existing conventions and dependencies. Include data and migration safety where applicable. Show the plan to the user and incorporate corrections. Planning may include sketches, specifications, and documentation; **do not write or modify implementation code until the user explicitly asks to begin building after seeing the plan**. An earlier "build now" request does not carry across this gate. Agreement with recommendations alone is not a start instruction; ask for a fresh start instruction after the plan is visible.

## 4. Keep durable state

When the intended project workspace exists, reuse its planning or issue documents if they already serve this purpose. Otherwise keep one concise `.project-guide/plan.md` there with the goal, decisions and reasons, deferred questions, ordered slices, current status, and next action. Update it at phase boundaries so another session can continue. Keep secrets and personal data out. If the project location is unknown or does not exist, provide a portable summary in the conversation until one is chosen; do not write project state into an unrelated directory.

## 5. Build in slices

After the explicit start instruction, implement the first ready slice using the project's patterns. Check the behavior that matters, including relevant accessibility, security, and data safety. Report what changed, evidence it works, remaining risks, and the next slice. Continue through the agreed plan; pause for a new material decision or an action that needs authorization. If discoveries change scope or architecture, revise the plan with the user before following the new path.

## 6. Deliver and maintain

Before calling the project done, verify the agreed success criteria and provide the needed run, deployment, recovery, and maintenance instructions. Record known limitations and ownership of recurring tasks. Deploy, publish, or send information externally only with authorization. For later changes, resume from the recorded state, inspect the current project, and repeat only the discovery and planning needed for that change.

## Conversation contract

- Ask in manageable rounds, not a fixed questionnaire. Explain technical terms when they arise.
- Recommend a default when useful, but label it as a recommendation and keep the user's decision visible.
- Show progress and the next action at each boundary. Do not silently treat a plan as permission to code.
- A small project may move through phases quickly; a large one may span sessions. The gates remain the same.

