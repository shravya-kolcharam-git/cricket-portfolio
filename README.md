# Shravya Kolcharam – Cricket

Live site: https://shravya-kolcharam-git.github.io/cricket-portfolio/

## Add a post (Instagram, YouTube, blog, photo, video)
1. Open the site with `?owner=1` at the end of the address, go to **Social**, press **+ Add a post**.
2. Paste the link, choose where it belongs (Highlights, International, DCB domestic, Private and friendlies, Training, Coaching) and press Add.
3. To make it public for everyone, press **Copy my additions** and paste the result into `social-data.js` (inside `window.SOCIAL_SEED=[ ... ]`), then commit.

Instagram and YouTube links play embedded; blog links become cards.
Videos tab is empty for now; photos older than 2023 are 480px copies.

## Adding pictures, videos and posts without Claude (owner only)

1. Open `https://shravya-kolcharam-git.github.io/cricket-portfolio/admin.html`.
2. Create a private key once: GitHub, Settings, Developer settings, Personal access tokens, Fine-grained tokens, Generate new token.
   - Resource owner: your account. Expiration: 90 days.
   - Repository access: **Only select repositories**, then `cricket-portfolio` only.
   - Permissions: **Contents: Read and write**. Leave everything else at No access.
3. Paste the token on the admin page and press Connect. It stays in your own browser only. Never put it in a chat, a file or the repository.
4. Add photos, a video (MP4, up to 40 MB) or a link. The page saves to `media.json`, `social-extra.json` and the `m/` folder. The site updates in 1 to 2 minutes (hard refresh).

Safety: without the token the admin page can change nothing. Photos are resized and lose GPS data before upload. If a token is ever exposed, delete it in GitHub settings and create a new one.
