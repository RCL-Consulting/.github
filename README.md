# RCL-Consulting/.github

The RCL Consulting organisation profile on GitHub. `profile/README.md` is what github.com/RCL-Consulting
shows; this file is not shown there.

The logos in `profile/` and the images in `social-preview/` are pinned from
[rcl-brand](https://github.com/RCL-Consulting/rcl-brand) (private); `SOURCE.json` records the commit and
hashes. Change the brand in Claude Design, sync rcl-brand, then copy the files again and update
`SOURCE.json`. Never edit a logo here.

Brand rules for anything written here: "we", sentence case, plain and factual, no emoji, no badges.
Name only public repositories.

## Social previews

`social-preview/` renders the 1280 × 640 cards GitHub shows when a public repository is shared.
With rcl-brand checked out beside this repo:

```
python -m http.server 8790 --directory ..          # from this folder
# open http://localhost:8790/rcl-org-profile/social-preview/card.html?repo=OpenDLO
```

Each card is one entry in `cards.json`: the text, a photograph from rcl-brand's Photography, and its
`crop` and `zoom` (CSS `background-position` / `background-size`). Crop so that structure fills the
panel: no skyline, river, street or people. Render by screenshotting the `#card` element at a 1280 × 640
viewport (Claude does this with the Playwright browser) into `social-preview/out/<repo>.png`, then upload
each in the repository's Settings → General → Social preview; GitHub has no API for it. Keep each under 1 MB.
