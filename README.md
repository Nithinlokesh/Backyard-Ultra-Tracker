# Backyard Ultra Fuel Tracker PWA

## Files
- `index.html`: complete app UI and logic
- `manifest.webmanifest`: install metadata
- `service-worker.js`: offline cache
- `icons/icon.svg`: app icon

## Test locally
A service worker does not run correctly from a `file://` address. Serve this folder locally:

```bash
python -m http.server 8000
```

Open `http://localhost:8000` in a browser.

## Publish with GitHub Pages
1. Create a new GitHub repository.
2. Upload the four files while preserving the `icons` folder.
3. In repository Settings, open Pages.
4. Under Build and deployment, choose **Deploy from a branch**.
5. Select the `main` branch and `/ (root)`, then save.
6. Open the HTTPS Pages address GitHub provides.

## Install
- Android/Chrome: open the HTTPS site, then use **Install app** in the browser menu or the in-app Install button when shown.
- iPhone/Safari: open the HTTPS site, tap Share, choose **Add to Home Screen**, then Add.
- Desktop Chrome/Edge: open the HTTPS site and use the install icon/menu.

## Notes
- The app works offline after its first successful online load.
- Race data and custom buttons are stored in this browser/device with localStorage.
- Use **Export backup** before clearing browser data or moving to another phone.
- This version is single-device. A shared M/N/B/R live log needs a cloud database such as Supabase or Firebase.
- To force installed devices to refresh after editing assets, change `ultra-fuel-v1` in `service-worker.js` to a new value.
