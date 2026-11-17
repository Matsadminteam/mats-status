# MATS site check (public, no secrets)

Every 5 minutes GitHub opens the live site's health page (`https://matsapp.org/api/health`). If it fails twice in a
row, an urgent alert goes to the owner's phone through the free **ntfy** app; when it works again, a "back up" alert.
One alert per change. Change request 74 in the main project.

- The alert channel is the hidden repository secret `NTFY_TOPIC` (the owner's private topic name in the ntfy app).
- Test it: Actions > Site check > Run workflow (test ticked) - the phone should ring.
- Public on purpose: GitHub Actions are free and unlimited for public repositories, so this uses none of the private
  repositories' monthly minutes. A monthly step keeps the schedule from being paused.
