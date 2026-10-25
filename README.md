# hci-project
# Recall Lab: Impact of AI Assistance on Human Memory

**Live demo:** https://axbeerah.github.io/hci-project/

A working prototype for our Human-Computer Interaction semester project (Milestone 1). It supports an experiment on how working with an AI assistant changes what people remember about their own work, and whether an AI that asks questions instead of giving answers reduces that effect.

## Group members

- Aabeerah Iqbal (29080)
- Mahnoor Mughal (29166)
- Syed M Abdullah Yousuf (29067)

## Research question

How does AI assistance affect memory for, and ownership of, a completed task compared with unaided work, and does a metacognitive (friction-based) AI design reduce any negative effect?

## What the app does

Participants complete three short tasks (write an email, summarise a passage, solve a logic puzzle). Each task is done in a different condition:

| Condition | Description |
|---|---|
| Alone | No assistant. Only a text box. |
| Standard AI | Chat assistant that streams a complete answer immediately. An "Insert into my answer" button copies it across. |
| Metacognitive AI | Chat coach that never writes the answer. It asks planning and reflection questions and declines requests to write the text. |

After each task the app collects:

- Three 7-point ratings: mental demand, self-efficacy, and ownership.
- Immediate free recall of what the participant submitted.
- Interaction logs: time on task, edits, pastes, messages sent, AI text inserted, and the full chat transcript.

A Day-7 follow-up screen collects delayed recall of each answer, and a researcher view shows all data as a table and CSV.

## Experimental design

- Within-subjects, three conditions, about 30 participants.
- Conditions rotate across three groups in a Latin square. The participant ID (P01, P02, P03, ...) sets the group automatically, so each condition is paired with each task and each position equally often.
- Tasks are in a fixed order: email, summary, logic puzzle.

| Group | Task 1 (Email) | Task 2 (Summary) | Task 3 (Logic) |
|---|---|---|---|
| A (P01, P04, ...) | Alone | Standard AI | Metacognitive AI |
| B (P02, P05, ...) | Standard AI | Metacognitive AI | Alone |
| C (P03, P06, ...) | Metacognitive AI | Alone | Standard AI |

## Design notes

- **Scripted AI responses.** Both assistants use pre-written, task-specific responses so every participant sees identical AI content. This keeps the comparison controlled (a Wizard-of-Oz style prototype). A live language model could replace them in future work.
- **Local data storage.** Data is saved in the browser (localStorage) and is never uploaded. Run all sessions, including the Day-7 follow-up and the researcher view, on the same browser and device.
- **Recall scoring.** The app computes a word-overlap score as a rough proxy. The main analysis uses manual idea-unit scoring by two coders.

## How to run

Open the live demo link, or download `index.html` and open it in any modern browser. There is nothing to install.

1. Enter a participant ID (for example `P01`) and start session 1.
2. Complete the three tasks, ratings, and recall screens.
3. After 7 days, choose "Day-7 follow-up" with the same ID.
4. Use "Researcher view" to see and copy the data as CSV.

## Repository contents

- `index.html`: the complete application (HTML, CSS, and JavaScript in one file).
- `README.md`: this file.

## References

- Joo et al. (2026). https://www.tandfonline.com/doi/epdf/10.1080/01443410.2026.2618717
- Shen & Yoon (2025). The Dark Addiction Patterns of Current AI Chatbot Interfaces. CHI Extended Abstracts. https://dl.acm.org/doi/10.1145/3706599.3720003
