# Editing the EarlySight website

The main page is one file: `index.html`. The blog is explained under "Write a blog post". Changes go live a minute or two after you commit.

## Change some wording
1. Click `index.html`, then the pencil icon (Edit).
2. Press Ctrl + F and search for the sentence you want to change.
3. Retype the words only. Leave the tags around them (`<p>`, `</p>`, `<h2>` and so on) alone.
4. Click **Commit changes**.

Every version is kept. To undo, open `index.html` → **History**, pick the earlier version and copy its text back.

## Where each section is (search for these words)
| Section | Search for |
|---|---|
| Headline and intro | `Spot the change` |
| Example chart | `Two pupils, one autumn term` |
| Why it matters | `visible in October` |
| What it spots | `What your MIS` |
| For your staff | `The right list for each role` |
| Pilot findings | `What we found` |
| Trust section | `Cyber Essentials certified` |
| Brochure download and form | `Free brochure` |
| Demo request and email address | `Request a demo` |
| Footer | `company number` |
| Menu at the top | `aria-label="Main"` |

## Write a blog post
Posts appear on earlysight.co.uk/blog, newest first, a minute or two after you commit.

1. Open `_templates/new-post.md` and copy everything in it.
2. Go back to the top of the repository and click **Add file → Create new file**.
3. For the name, type `_posts/` and then the date and a short title joined by hyphens, ending `.md`. For example: `_posts/2026-10-27-five-things-attendance-hides.md`. The part after the date becomes the web address: earlysight.co.uk/blog/five-things-attendance-hides/.
4. Paste the template and replace its wording. The lines between the two `---` lines are the settings:
   - `title`: the headline.
   - `description`: one or two sentences. They appear under the headline, on the blog page, and in the preview when the link is shared on LinkedIn or X.
   - `image`, `image_alt`, `caption`: the picture at the top. No picture? Delete those three lines, and the share preview uses the standard EarlySight image instead.
5. Click **Commit changes**.

**Pictures:** open the `assets/blog` folder, click **Add file → Upload files**, and drag the picture in. Then use its name in the post, for example `/assets/blog/typical-week.png`. Captions on anything from the dashboard: "Invented demo school data."

**Dates:** a post dated in the future doesn't appear until that date has passed and the site is next updated. To publish straight away, use today's date.

**Change or remove a post:** open it in `_posts`, then use the pencil (edit) or the three dots → **Delete file**.

**Something wrong?** If a post doesn't appear within five minutes, open the **Actions** tab: a red cross means the site didn't build. Click it to see which file it was. The usual cause is a missing `---` line or a stray quote mark in the settings at the top.

## Other files
- `CNAME` holds the web address. Don't change it.
- `assets/` holds the favicon, the logo used in the email footer, the brochure (`EarlySight_SLT_brochure.pdf`) and its cover picture (`brochure-cover.webp`). To update the brochure, upload a new PDF with the same name.
- The brochure form is built into `index.html` (search for `Get the brochure`). Each sign-up is emailed to admin@earlysight.co.uk by FormSubmit (formsubmit.co), and the download button appears straight after. To send sign-ups to a different address, search for `formsubmit.co/ajax/` and change the email after it.
- `analytics/` and `discover/` forward visitors from the old Wix page addresses.
- **The blog:**
  - `blog/index.html` is the list of posts. It updates itself.
  - `_posts/` holds the posts, one file each.
  - `_layouts/` holds the look of the blog pages. You won't need to change these.
  - `assets/blog/` holds the blog's pictures, its stylesheet (`blog.css`) and `social-default.png`, the preview picture used when a post has none.
  - `_config.yml` holds the blog's settings. The main page doesn't use it.
  - `_templates/new-post.md` is the template to copy for each post. It isn't published.
