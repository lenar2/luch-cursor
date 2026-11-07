# Cursor workflow: turn a bug report into a reviewable change

[← LUCH for Cursor](../README.md) · [Русский](CURSOR_WORKFLOW.ru.md)

## The situation

A user reports that a page or service stopped behaving as expected. The code is only half the picture; the selected test environment can show what is actually happening.

## The work

1. **Ground the task.** Open the exact issue and repository. Confirm the branch and the files in scope.
2. **Observe the environment.** If the user has paired a test server, ask LUCH for its status and a bounded diagnostic command. Do not substitute another server.
3. **Compare evidence.** Separate source-code facts from live observations and assumptions.
4. **Prepare a fix.** Make the smallest change that addresses the cause. Preserve the original and show the diff.
5. **Verify.** Run only the requested or approved checks. Report their actual output.
6. **Hand back control.** Leave merge, deployment, DNS changes and restarts to a separate explicit decision.

## A prompt to try

> Inspect this issue and the current repository. Check the status of the test server I selected. Compare the observed output with the relevant code, identify the most likely cause and prepare a minimal patch. Run the focused test only. Do not merge or deploy.

## Why Cursor and LUCH fit together

Cursor holds the code context. LUCH can add the selected browser, authorized files and paired server context. That lets the investigation cross the boundary between “the code looks right” and “the chosen environment reports this.” Exact tools depend on the live session and grants.

This is a designed workflow based on the Cursor plugin's skills, not a claim that this exact bug scenario has been run for every user.
