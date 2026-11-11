# K1 Dribbling Curriculum

Project page for the 3-stage AMP + PPO dribbling curriculum on the Booster K1 (NomadZ).

## Videos
Put the three Notion videos here (Notion: hover video → ••• → Download):

- `assets/videos/stage1.mp4`  (Notion file `Unknown.mp4`)
- `assets/videos/stage2.mp4`  (Notion file `Unknown-2.mp4`)
- `assets/videos/stage3.mp4`  (Notion file `Dribbling_policy.mp4`)

GitHub rejects files over 100 MB; compress with
`ffmpeg -i in.mp4 -vcodec libx264 -crf 28 -preset veryfast -an out.mp4` if needed.

## Deploy
```bash
git init && git add . && git commit -m "K1 dribbling project page"
gh repo create k1-dribbling --public --source=. --push
gh api repos/{owner}/k1-dribbling/pages -X POST -f "source[branch]=main" -f "source[path]=/"
```
Or: repo Settings → Pages → Deploy from branch `main`, folder `/ (root)`.
Site URL: `https://<username>.github.io/k1-dribbling/`
