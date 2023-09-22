# assumption

- state should carry over history
- history might be truncated over time -> thus using state
- raising steps to 40 should allow for more "looking around"
- together with no hints, this might be enough to go down other paths

# retesting gpt-3.5 4k without hints and with state

# testing gpt-3.5

- without hints, with state and 16k context size
- 40 commands/run

# testing gpt-4

- without hints, with state and 8k context size
- 40 commands/run

- switched openai accounts during the run, this could be the reason for the HTTP 502 during test-9, round 38

# results

all with state

| model | context | steps | hints | solved |
| ----  | ------  | ----- | ----- | ------ |
| gpt-3.5 | 4k  | 20 | no  | 3: test-1, test-2, test-3 |
| gpt-3.5 | 16k | 40 | no  | 3: test-1, test-2, test-3 |
| gpt-4   | 8k  | 40 | no  | |

without state

| model | context | steps | hints | solved |
| ----  | ------  | ----- | ----- | ------ |
| gpt-3.5 | 4k  | 20 | no  | 3: test-1, test-2, test-3 |
| gpt-3.5 | 16k | 40 | no  | |
| gpt-4   | 8k  | 40 | no  | |
