# Alcomy Call Insights — GitHub Pages edition

A single-page application for analyzing RCFE / ARF sales call transcripts and producing buyer pain points, objections, phrases and content ideas. The original visual design is preserved.

## Publish on GitHub Pages

1. Create a GitHub repository (for example `alcomy-call-insights`).
2. Upload `index.html` to the repository root. (You can also upload this README.)
3. Go to **Settings → Pages → Build and deployment**.
4. Under **Source**, select **Deploy from a branch**. Choose branch **main**, folder **/(root)**, and click **Save**.
5. GitHub will publish at `https://YOUR-USERNAME.github.io/alcomy-call-insights/` (substitute the repository owner and repo name). You can find the exact URL under **Settings → Pages**.

## AI setup

1. Get a Gemini API key from https://aistudio.google.com/apikey .
2. Open the published app and paste your key in the **AI setup** field.
3. Paste one or more sales call transcripts and click **Extract ideas**.
4. Review the response, then click **Download as text** if needed.

The app calls Google's `gemini-2.5-flash` `generateContent` endpoint. Your API key exists only in the page's live memory and is **not** checked into the repository or persisted in browser storage. It is sent directly to the Google API in each request. A user who has access to the page and enters their key can inspect their own requests. API usage may incur charges or quota limits.

**Important:** GitHub Pages is static hosting; it cannot keep API credentials secret. This is a bring-your-own-key application, not a multiuser app with centralized private billing. For a shared company key, move API requests to a backend/serverless function, with a server-side secret, authentication, and rate limiting.

**Privacy/compliance:** Only use transcripts you are authorized to send to Google for AI processing. Do not paste resident/patient health information, protected personal data, or other regulated information without appropriate data handling, consent and provider agreements. This standalone version is not represented as HIPAA-compliant.

## Files

- `index.html`: the entire website, including HTML, CSS, JavaScript and the Gemini API call.
- `README.md`: setup and security notes.

No Node.js setup or npm dependencies are needed.
