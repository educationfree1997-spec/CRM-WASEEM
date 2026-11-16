CRM WASEEM - VERSION 3 (installable app, works offline)
=======================================================

WHAT THIS IS
A private lead manager. After you put these files on a free HTTPS website and open
it once, Chrome or Edge can install it like a normal app: icon on the phone home
screen, its own window, and it opens with no internet.

Your leads are saved ONLY on the device you use (in the browser's IndexedDB storage).
There is no cloud database, no account, no monthly cost.

FILES (upload ALL of them, keep the icons folder)
  index.html            the whole app (design, logic, icons are inside this file)
  manifest.webmanifest  app name, icon, colours, standalone window
  service-worker.js     saves the app on the device so it opens offline
  icons/                icon-192.png, icon-512.png, icon-maskable-512.png
  README-INSTALL.txt    this file (optional to upload)

WHAT IS NEW IN VERSION 3
  * New design: gradient "today" panel on Home with a coloured pipeline bar,
    cleaner cards, initials avatars on leads, soft status badges, drawn icons,
    smoother light and dark themes, short opening splash screen.
  * Theme button moved to the top right corner (moon icon).
  * Home reminds you to back up when the last backup is older than 7 days.
  * Options > "Devices and sharing": Share app link button and a plain explanation
    of where data lives.
  * Same data format as Version 1 and 2. The eight lead statuses are unchanged.

-------------------------------------------------------
STEP 1 - FREE HOSTING ON GITHUB PAGES (once, on a computer)
-------------------------------------------------------
  1. Sign in at github.com. Click "+" (top right) > New repository.
     Name: crm-waseem    Visibility: Public    > Create repository.
     (Free GitHub Pages needs a Public repository. Only app files go there.
      Your leads are never uploaded.)
  2. On the new repository page click "uploading an existing file".
  3. Unzip CRM-WASEEM-PWA-v3.zip. Select EVERYTHING inside (index.html,
     manifest.webmanifest, service-worker.js, README-INSTALL.txt and the "icons"
     folder) and drag it into the upload area.
     index.html must be at the top level of the repository, not inside a folder.
  4. Click "Commit changes".
  5. Settings > Pages > Build and deployment: Source "Deploy from a branch",
     Branch "main", Folder "/ (root)" > Save.
  6. Wait 1-3 minutes, refresh. Your address appears:
        https://YOUR-GITHUB-NAME.github.io/crm-waseem/
  GitHub changes its screens sometimes; follow the on-screen wording.
  Other free static hosts (Netlify, Cloudflare Pages) also work: upload the same files.

  IMPORTANT: keep using the SAME address. Saved leads belong to that address.

-------------------------------------------------------
STEP 2 - INSTALL
-------------------------------------------------------
ANDROID (Chrome)
  1. Open your address in Chrome while online. Wait a few seconds.
  2. Tap "Install app" at the top of CRM WASEEM, or Chrome menu (3 dots) >
     "Install app" / "Add to Home screen" > Install.
  3. Open CRM WASEEM from the home screen once while online.
     After that it opens without internet.

WINDOWS - CHROME
  Open the address > click the install icon at the right end of the address bar
  (or 3 dots > "Cast, save and share" > "Install page as app") > Install.

WINDOWS - EDGE
  Open the address > 3 dots > Apps > "Install this site as an app" > Install.
  Tick "Create Desktop shortcut" / "Pin to Start" when asked.

-------------------------------------------------------
SHARING WITH OTHER PEOPLE
-------------------------------------------------------
  Send them your address (Options > Devices and sharing > Share app link).
  Each person installs their own copy. Each copy starts empty and keeps its own
  leads on that person's device. Nobody can see anyone else's leads.
  There is NO automatic sync between people or devices. Sync would need an online
  database service, which this app does not use.

-------------------------------------------------------
BACKUP, RESTORE, MOVING TO ANOTHER PHONE
-------------------------------------------------------
  Back up:  Data > "Full backup (JSON)". A file CRM-WASEEM-backup-DATE.json is saved
            in Downloads. It holds leads, notes, follow-up history, your option lists
            and the theme. Keep a copy in Google Drive, email or USB.
  Move:     send that file to the other phone/computer (WhatsApp, email, Drive),
            open CRM WASEEM there > Data > choose the file >
            "Restore (merge, keep existing)".
  Merge     adds missing leads and never overwrites or duplicates existing ones.
  Replace   makes the app match the file. It asks first and downloads a safety
            backup of the current data.
  CSV       Data > import a CSV (duplicates are matched on email, phone or website
            and skipped) or export all / filtered leads for Excel.
  WARNING   Clearing the browser's "site data", or uninstalling the app and choosing
            to remove its data, erases the leads on that device. Back up first.

  Coming from the old single file CRM-WASEEM.html or from Version 1 / 2 at a
  different address? Make a Full backup there, then Restore it here.
  Upgrading Version 1 / 2 at the SAME address: upload these files over the old ones,
  open the app online, close it and open it again. Your leads stay.

UPDATING LATER
  Replace the files on the website. In service-worker.js change  crm-waseem-v3  to
  crm-waseem-v4. Open the app online twice to receive the update. Data is not touched.

PRIVACY
  The app has no password. Anyone who can unlock your phone or computer and open the
  app can read the leads. Use a screen lock.
