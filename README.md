# GHSS Karapattu Website — Setup & Maintenance Guide

This is a plain HTML/CSS website (no database, no monthly fees, no builder
lock-in) for Government Higher Secondary School, Karapattu. It is built to
be published for free using **GitHub Pages**, and to be easy for
non-technical school staff to update afterwards.

## What's in this folder

```
index.html        Home page
about.html         History, mission, leadership
academics.html      Classes and streams offered
facilities.html    Library, computer lab, playground, etc.
admissions.html    How to apply, documents required
notices.html       Announcements list (the page you'll edit most often)
gallery.html       Photos
contact.html       Address, phone, email, map, contact form
css/style.css       All colors, fonts, spacing — one file controls the look
js/main.js          Small script for the mobile menu — you shouldn't need to touch this
images/logo.svg     Placeholder school emblem — replace with the real one if you have it
```

Every page marked with a yellow "✏️ Editable placeholder" box contains a
fact that could not be confirmed publicly (phone number, exact Higher
Secondary groups, staff names, fees, timings). Please have the Head
Master's office fill these in before the site goes live.

---

## Step 1 — Publish the site for free with GitHub Pages

GitHub Pages hosting is completely free forever, has no ads, and is very
reliable — a good fit for a school with no IT budget.

1. Go to [github.com](https://github.com) and create a free account (use a
   school email if you have one, e.g. `karapattugovt@gmail.com` style
   address works fine too).
2. **To get the address `https://ghss-kpt.github.io` exactly:** the GitHub
   *username* itself has to be `ghss-kpt` (GitHub gives every account a free
   `your-username.github.io` address). So when creating the account in
   Step 1, set the username to `ghss-kpt` (check it's available on the
   signup form — if taken, try `ghss-kpt-official` or similar). Then:
   - Click the **+** icon (top right) → **New repository**
   - Repository name: exactly `ghss-kpt.github.io` (this exact name makes
     GitHub serve it at the root address instead of a sub-path)
   - Set it to **Public**
   - Click **Create repository**

   (If you'd rather keep a personal/existing GitHub account and don't mind
   a longer address, use any username and any repository name — the site
   will then live at `https://your-username.github.io/repository-name/`.)
3. On the new repository page, click **uploading an existing file**.
4. Drag and drop *all* the files and folders from this package
   (`index.html`, `about.html`, the `css` folder, the `js` folder, the
   `images` folder, everything) into the upload box, then click
   **Commit changes**.
5. Go to the repository's **Settings** tab → **Pages** (left sidebar).
6. Under "Build and deployment" → **Source**, choose **Deploy from a
   branch**. Under **Branch**, choose `main` and folder `/ (root)`, then
   **Save**.
7. Wait 1–2 minutes, then refresh the page. GitHub will show your live
   website address, something like:
   `https://YOUR-USERNAME.github.io/karapattu-school-website/`

That's it — the site is now live and free, with no expiry.

### Optional: use a nicer web address
- A free option: keep the `github.io` address above and share that.
- A paid option (~₹500–900/year): buy a domain like `ghsskarapattu.in` or
  `.school.in` from any Indian registrar (BigRock, GoDaddy, Namecheap) and
  point it at GitHub Pages. This is optional — everything works without it.

---

## Step 2 — Updating the site later (no coding tools needed)

You don't need to install anything. All edits can be made directly on
github.com from any browser, even a phone:

1. Log in to github.com and open your repository.
2. Click the file you want to change (e.g. `notices.html`).
3. Click the pencil (✏️) "Edit this file" icon.
4. Make your change directly in the text box. HTML looks unfamiliar at
   first, but you're mostly just changing text between tags like
   `<li>...</li>` — don't delete the `<` and `>` symbols themselves.
5. Scroll down, add a short note like "Updated admission notice", and
   click **Commit changes**.
6. The live site updates automatically within about a minute.

**Adding a new notice** (the most common update): open `notices.html`,
find the block that starts with `<ul class="notice-list">`, and paste a
new line like the ones already there, at the top of the list:

```html
<li><span class="date">15 Aug 2026</span><span class="tag">General</span> Independence Day celebration at 9:00 AM.</li>
```

**Adding a real photo**: click "Add file" → "Upload files" inside the
`images` folder, upload a `.jpg` (keep it under ~300 KB so it loads fast
on mobile data), then edit `gallery.html` and change one `<img src="...">`
line to point to your new file name.

---

## Alternative: Google Sites (fully drag-and-drop, zero code)

If nobody at the school wants to ever touch HTML, an even simpler option
is **Google Sites** (sites.google.com — free with any Google account):
you build pages by dragging text and image boxes, no code at all, and it
publishes to a free `sites.google.com/view/...` address. The trade-off is
less design control and a less "official" looking web address unless you
attach a paid domain. I've written this site as plain HTML/CSS
specifically because it's ready to publish right now — but if your team
would rather use Google Sites, the content in each page above (headings,
facts, notice format) can simply be copy-pasted into it.

---

## Free extras worth adding later

- **Google Forms** — free, no-code way to collect admission enquiries or
  feedback, more reliable than the `mailto:` form on the Contact page.
- **Google Search Console** (free) — lets you see how many people find
  the site via Google search.
- **A school Gmail address** (free) — e.g. `ghsskarapattu@gmail.com` — so
  the contact form and public email look official.

---

## Facts used to draft this site

Pulled from public school-directory listings for GHSS Karapattu, Uthangarai
Block, Krishnagiri District (PIN 635207): established 1963, co-educational,
Tamil medium, Classes 6–12, ~23 teachers, 12 classrooms, library with
~2,670 books, 14 computers, playground, accessibility ramps, medical
check-ups, and Mid-Day Meal Scheme. These are a reasonable starting point
but should be verified and corrected by the school office — third-party
directories are not always accurate or current.

**Note on identity:** there is more than one "GHSS Karapattu" listed in
Tamil Nadu (this one in Krishnagiri district's Uthangarai block, and a
separate school by a similar name in Tiruvannamalai district). This site
was drafted for the **Krishnagiri district** school. If you meant the
Tiruvannamalai school instead, just update the address/district text
across the pages — the structure and design stay the same.
