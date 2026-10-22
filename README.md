# Birzuu & Affu — Birthday Surprise Website ♡

A romantic, responsive, single-page birthday website with interactive wishes, 50 reasons, open-when letters, a relationship timeline, a quiz, a cake celebration, a gift reveal, and a final letter.

## 1. Run it on your computer
1. Extract the ZIP.
2. Open `index.html` in Chrome, Edge, Firefox, or Safari.
3. The page works without installing packages or setting up a backend.

## 2. Personalize names and the final letter
Open `index.html` in a text editor (VS Code is recommended). Near the bottom, find `const CONFIG = { ... }`.
The current names are already set to:
- Girlfriend: `Birzuu`
- Your name: `Affu`

You can edit `birthdayWishes`, `reasons`, `openWhen`, `timeline`, and `finalLetter`. Replace generic sample timeline text with real events, dates, and memories.

## 3. Your photos are already included

I've added the five photos you supplied into `assets/memories/` as `photo-1.jpg` through `photo-5.jpg`. They are wired into the first five permanent gallery slots. Add `photo-6.jpg` to fill the sixth slot if you'd like.

## 4. Add photos to the six permanent photo slots
The gallery has six permanent slots. To make photos appear in the published website:

1. Put your six image files in `assets/memories/`.
2. Rename them exactly:
   - `photo-1.jpg`
   - `photo-2.jpg`
   - `photo-3.jpg`
   - `photo-4.jpg`
   - `photo-5.jpg`
   - `photo-6.jpg`
3. If your image is a PNG or WEBP, either convert it to JPG or edit the corresponding path in the `defaultMemories` array in `index.html`.
4. In `index.html`, search for `const defaultMemories=[` and personalize the title/caption for each photo.
5. Save the file and refresh the page.

You can also click **Preview photos from my device** in the gallery, but those previews exist only in the current browser session. They are not automatically uploaded or saved to the website. Use the permanent photo slots for deployment.

Privacy tip: choose photos you are comfortable sharing with anyone who has the website link.

## 5. Background music is already included

I've added the MP3 you supplied as `assets/audio/birthday-music.mp3`. Open the site and click **Music: off** in the top bar to start playback. Browsers generally require a click before audio can play.

## 6. Add background music
1. Place your MP3 file at `assets/audio/birthday-music.mp3`.
2. Open the website and click **Music: off** in the top bar.
3. Most browsers require a click before music can start; the website intentionally does not autoplay music.
4. If your file has a different name, edit `musicPath` in the `CONFIG` object or change the audio source assignment.

Use a music file you own or are allowed to use. The website still works if no audio file is present.

## 7. Publish it online for free with Vercel
You need to upload the project folder to a GitHub repository first, then import it into Vercel.

### A. Put the project on GitHub
1. Sign in at https://github.com and create a new repository, for example `birzuu-birthday`.
2. Extract this ZIP.
3. Upload all project files and folders (`index.html`, `README.md`, and `assets/`) to the repository. Do not upload the ZIP file as the only repository content.
   - Easiest option: use GitHub's website and **Add file → Upload files**, then drag the extracted files/folders into the browser.
   - Keep `index.html` at the repository root.
4. Commit the files.

### B. Deploy with Vercel
1. Open https://vercel.com and sign in.
2. Choose **Add New → Project** and import the `birzuu-birthday` GitHub repository.
3. For this plain HTML site, no build command is required. If asked for a framework preset, choose **Other**; leave the build command empty and use `.` as the output directory if required by the current interface.
4. Click **Deploy**.
5. Vercel will give you a public link. Open that link on your phone to test the site, then send it to Birzuu.

When you change photos, music, or text later, upload/commit the updated files to GitHub and Vercel will redeploy.

## 8. Music and photo troubleshooting
- Music button does nothing: check the exact file path and filename, then try clicking again.
- A photo slot shows an emoji instead: check that the file exists at `assets/memories/photo-N.jpg` and the filename capitalization matches.
- Keep the images reasonably sized (around 1–2 MB each is a practical target) so the site loads quickly on mobile.

## Notes
- No backend, login, database, analytics, or personal data collection is included.
- The site is a static website. Anyone who has the public link may view the photos and messages you publish.
