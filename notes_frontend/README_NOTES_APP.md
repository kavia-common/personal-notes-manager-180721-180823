# Ocean Notes - Svelte Frontend

A modern SvelteKit-based notes application with a sidebar, top bar, and editor pane. Notes are persisted locally via `localStorage`. No external services or environment variables are required.

Features:
- Create, edit, and delete notes
- Autosave changes
- Search/filter by title and content
- Persistent storage in your browser
- Ocean Professional theme: primary #2563EB, secondary/success #F59E0B, error #EF4444, background #f9fafb, surface #ffffff, text #111827

Getting started:
1. Install dependencies:
   npm install

2. Start the dev server:
   npm run dev

3. Open the app at:
   http://localhost:3000

Build and preview:
- Build: npm run build
- Preview: npm run preview

Notes:
- All data is stored locally in your browser under the key `notes_app_state_v1`.
- You can reset all notes by clearing that key from DevTools or using notesStore.resetAll() in console.
