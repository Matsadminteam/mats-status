# MATS site check (public, no secrets)

Every 5 minutes GitHub opens the live site's health page (`https://matsapp.org/api/health`). If it fails twice in a
row, the run fails with "MATS site is DOWN" and GitHub emails the Matsadminteam account about the failed run.
One email per outage. Change request 74 in the main project.

- Test it: Actions > MATS site DOWN alert > Run workflow (test ticked): the run fails on purpose and the email should arrive.
- Public on purpose: GitHub Actions are free and unlimited for public repositories, so this uses none of the private
  repositories' monthly minutes. A monthly step keeps the schedule from being paused.
