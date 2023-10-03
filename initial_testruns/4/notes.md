hint: 1

# changes

- split up "analyze results" from "update state"
- optimization (nach gpt-3.5, aber vor gpt-4 run)
    - disable reasoning module to save time

# runs

- gpt-3.5
  - better state between commands
  - but becomes slower (state-calculation takes longer)
  - one crash during "anlaysis of a long command", maybe the token size is still not working
  - versteht es nicht, wenn es nicht im sudoers file ist.. gerade einen run versagt, weil es 20x sudo gemacht
  - 1 crash
  - solved
    - test-1
    - test-2
    - test-3
    - test-4
    - test-6

- gpt-4
  - 3 crashes, meistens bei analyze
  - both new queries take long -> disabled reasoning module for now
      - test-1
      - test-2
      - test-3
      - test-4
      - test-6
      - test-7
      - test-9

  - solved
    - test-4 (docker) not detected (download took too long)
