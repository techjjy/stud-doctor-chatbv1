# Doctor Bernd: spoken virtual patient quiz

A voice-enabled, adaptive oral examination for fourth-year medical students. Doctor Bernd, their professor, **speaks** his questions aloud and students answer **by voice** (or by typing). He presents a five-month-old infant with prolonged fever, poor feeding and a rash, then questions the student on the differential diagnosis, the medical tests to recommend and the treatment. He asks for the final diagnosis towards the end and never reveals it before then.

- **Voice**: the browser reads Doctor Bernd aloud and turns the student's speech into text (Chrome, Edge or Safari; typing always works).
- **No abbreviations**: every term is spoken and written in full.
- **Adaptive quizzing**: harder follow-ups after strong answers, hints after weak ones.
- **Red herring** midway separates strong from average students.
- **Hold** (button or say "hold") pauses the conversation, his voice and the microphone. **Continuation** (button or say "continuation") resumes and repeats the last question.
- Saying **stop** ends the session. Doctor Bernd then reviews every quiz question with the student, scores each domain and recommends reading.

## Files

| File | Where it goes |
|---|---|
| `index.html` | This GitHub repository (the page students open) |
| `README.md` | This GitHub repository |
| `worker.js` | **Not** in GitHub. Paste it into your Cloudflare Worker's code editor |

The case, the diagnosis and Doctor Bernd's instructions live only in `worker.js` on Cloudflare. `WORKER_URL` near the top of the script in `index.html` must be your Worker's address.
