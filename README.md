# Card Studio — browser-local GitHub edition

A free static Pokémon collection and binder planner. No sign-in, database account, billing account, cloud sync, or ChatGPT login.


All files in this package are generic and contain no personal name, email, collection, credential, or account profile. GitHub still shows your username and public account/commit information; changing your email privacy does not remove old commits. This package is for the new repository, not the separate hosted sign-in edition.

## Where the collection saves
Clicking Save card and changing a binder automatically save to this browser's localStorage. A banner confirms local saves and shows the last recovery-backup download time on this browser. Closing the browser or restarting normally preserves the data. Clearing site data, using private browsing, switching browser profiles, changing site addresses, or losing the device can lose access.

Your collection is not uploaded to GitHub. Someone opening the website link in their own browser gets their own empty collection. Someone using your same unlocked browser profile can see its locally saved cards. This app does not password-lock or encrypt browser storage.

## Move between Mac, iPhone, and iPad without syncing
1. Finish making changes on one device.
2. Click **Download recovery backup**. It downloads a `.json` file; you do not need to open or edit it.
3. Save that file in iCloud Drive, or transfer it another way.
4. Open the same website on the other device. Choose **Restore from backup** and select the latest file.
5. Import replaces that browser's current collection after confirmation. Export any work you want to keep before replacing it.
6. After editing on the second device, download a new recovery backup before returning to the first.

Devices hold separate copies. There is no automatic merging or syncing. Use one device at a time to avoid keeping different versions. iCloud transfers the file only when you save it there; it does not automatically sync this website's browser data. Keep extra backup copies independently.

## Organize cards
- **Owned cards** and **Wishlist** are separate navigation sections.
- On Wishlist, **Got it → Owned** changes the saved entry's ownership in one click, including its binder status.
- Owned entries have **Move to Wishlist**, with confirmation.
- Filter either section by category; search by name, card ID, or category.
- Card details record printing, quantity, condition, and categories. A marketplace reference does not adjust for condition.

## Binder planner
- Create named 4-, 9-, or 12-pocket binders and multiple pages.
- Choose cards by picture from the shelf or tap a pocket for a visual picker. Catalog search can add wanted cards directly.
- **✓ Owned** and **♡ Wanted** badges show status. Finish labels help distinguish entries.
- Tap a shelf card and then pockets to place it; Stop placing card exits this mode. Drag-and-drop is optional on desktop. Touch devices can use tap controls throughout.
- Tap a filled pocket for details, remove, or Move / swap. Move to another page and choose a destination for cross-page swaps.
- Add, duplicate, delete, or jump to pages. Undo layout reverses recent layout edits during this session.
- Binder wishlist lists wanted entries for that binder. Got it marks an entry owned across all plans.
- Layouts reference saved entries; they do not reserve physical copies or change quantities.

## Excel export
**Export Excel workbook** downloads a real `.xlsx`, including:
- **Owned:** a calculated view of owned entries.
- **Wishlist:** wanted entries with a yellow **Acquired?** Yes/No dropdown. Set Yes to add that row to Owned. Completed rows stay highlighted as your record; No reverses it.
- **All cards:** the exported source records supporting the calculated view.

Automatic workbook updates require Excel 2021+ or Microsoft 365. Other spreadsheet apps may display the snapshot, but automatic behavior is not verified there. Leave Excel calculation on Automatic and leave the Owned formula/spill cells intact. Workbook edits do not update the website. Exporting again creates a new workbook from the website, not a merge of previous Excel edits.

Export includes card/set/number/language/finish, quantities, conditions, categories, binder locations, price references, Central Time timestamps, and image links. It does not embed photos. Missing prices remain Unavailable, distinct from real zero quotes. **Excel does not restore the website: use the JSON recovery backup for that.**

## Card catalog and prices
Card data and images are requested from TCGdex. Catalog coverage is not guaranteed to include every printing ever made. Images and USD prices may be missing or mismatched. Check valuable cards independently. No paid API keys are used.

The page checks cards due for a refresh on opening, then hourly while the browser runs. Manual Refresh prices is available. The banner shows the last successful fetch and next check in America/Chicago time: CDT in summer and CST in winter. Each card shows the provider's price date. Provider updates follow their own schedule; fetching today does not guarantee a new price today. Closed or sleeping browsers do not run checks.

## Device support and privacy
The interface is responsive for modern iPhone/iPad Safari, Chrome, and Mac browsers. It uses tap-based binder controls, native file import/download, and UTF-8 Excel export. Internet is needed for fresh catalog, images, and prices. The app makes no analytics or external-font requests and uses a no-referrer policy. Card data/image providers and GitHub still receive ordinary network traffic; this is not anonymous browsing.

## Verification
JavaScript syntax and deterministic tests passed for old backup compatibility, visual binder state, wishlist acquisition, cross-page moves/undo, quantity preservation, Excel package/XML structure and acquisition/reversal, and CDT/CST labels. Native testing on a physical iPhone/iPad has not been performed. No source file contains login, syncing, or database setup credentials.

## Custom cards
Use **Add custom card** in Explore or your collection for cards missing from the catalog. Enter name, set, number, status, categories, condition, quantity and optional manual USD value. Photos are resized/re-encoded locally (original EXIF location metadata is discarded). Photos use browser space, so download recovery backups regularly. Custom cards work in binders, Owned/Wishlist and Excel. Excel includes manual values and a photo-backup note; custom photos are retained in recovery backups, not embedded into Excel. Open a saved custom card and choose **Edit custom details / photo** to change it. Manual values never refresh automatically.

To update an existing GitHub Pages site, download a recovery backup first, then upload these files to the same repository root and commit. Keep the same website address to retain browser-local data.
