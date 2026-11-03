# Lunara — Your own universe (hackathon prototype)

A calm, private-by-default web prototype for the Meta AI Developer Hackathon,
Startup Track, theme **Build for Your World**.

## What it is

Write down a memory in your own words. Lunara turns it into a personal
constellation you can revisit. The prototype is deliberately small:

- One page, no build step, no dependencies, no account.
- A memory becomes a deterministic constellation: the same words always draw
  the same sky, so a constellation can be shared and revisited without a server.
- Memories are stored only in the visitor's browser (`localStorage`).
  Nothing typed here is uploaded by this prototype. "Clear all" deletes them.
- A sample memory button lets a judge see a finished constellation in one click.

## How to run it

Open `index.html` in any modern browser, or serve this folder:

```sh
python3 -m http.server 8000
# then open http://127.0.0.1:8000/
```

No API key, no install, no network call is required to run it.

## What is real, and what is not

Honest scope for judging:

- Real: deterministic constellation generation, canvas rendering, local save /
  reopen / delete, keyboard-accessible saved list, reduced-motion-friendly design.
- Prototype story text: generated locally from templates in `index.html`.
  It is not a live hosted-model call.
- Future adapter (not wired to a live key in this build): a hosted model could
  replace `storyFor()` to write the constellation story, and a hosted image
  model could replace the canvas nebula wash. Doing that would require an
  API key and a server-side proxy, which this prototype intentionally avoids
  so it can run privately and offline.
- This is a web prototype for the hackathon. It is not the Lunara iPhone app,
  and no claim is made here that the iPhone app is shipped.

## Demo script (3 minutes)

1. (0:00–0:30) Open the page. State the idea in one sentence: memories become
   a universe you own, privately.
2. (0:30–1:30) Click "Try a sample memory". Show the constellation, read the
   story line, and point out the star count.
3. (1:30–2:30) Type a new memory of your own, create it, reopen it from
   "Saved constellations", then use "Clear all" to show deletion.
4. (2:30–3:00) Close on privacy: no account, no upload, everything stays
   in the browser — and on the honest next step, a hosted-model story adapter.

## License

MIT. See `LICENSE`.
