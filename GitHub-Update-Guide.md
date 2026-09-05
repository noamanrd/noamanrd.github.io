# Update Noaman’s website on GitHub — v6

Use **Noaman-Muhammad-GitHub-Pages-Upload-v6.zip**. It is ready to upload and includes the new scientific illustrations, CV-based publications and nm@nuovofilm.com.

## 1. Back up your current website

Open your existing repository, normally:

https://github.com/noamanrd/noamanrd.github.io

Choose **Code → Download ZIP** and keep it as a backup. Use the existing repository; do not delete or recreate it.

## 2. Extract the new Upload ZIP

Right-click the downloaded ZIP and choose **Extract All** on Windows, or double-click it on macOS.

You will see `index.html`, `index.rsc`, `404.html`, `favicon.svg`, `.nojekyll`, the guide and the folders `assets`, `illustrations` and `expertise`.

**Upload these extracted contents, not the ZIP or an enclosing folder.** `index.html` must appear directly on your repository’s main Code page.

## 3. Replace the website files

1. Open the repository’s **Code** tab and select **main**.
2. Choose **Add file → Upload files**.
3. Drag in all extracted files and the complete `assets`, `illustrations` and `expertise` folders.
4. Wait for all uploads to finish.
5. Write the commit message: `Update portfolio to v6 — scientific illustrations and CV publications`.
6. Choose **Commit directly to the main branch**, then **Commit changes**, if your repository allows it. If GitHub requires a branch, use a pull request and merge it when ready.

Matching paths replace the old files. New image and asset paths are added. Leave older unused assets in place for this update; there is no need to delete folders first. Preserve an existing `CNAME` file if you use a custom domain.

The Upload ZIP contains fewer than 100 files, with every file below GitHub’s 25 MiB browser limit. The larger source package is for future editing and is not the package to upload here.

## 4. Confirm Pages settings

Go to **your repository’s Settings → Pages**, not your account’s Settings.

https://github.com/noamanrd/noamanrd.github.io/settings/pages

| Setting | Value |
| --- | --- |
| Source | Deploy from a branch |
| Branch | main |
| Folder | /(root) |

Click **Save** if needed. If these settings are already correct, leave them as they are. A screen showing only **Verified domains** is your account-level settings; return to the repository.

Keep `.nojekyll` at the repository root. If it was hidden when you extracted the ZIP and the repository does not have one, choose **Add file → Create new file**, name it `.nojekyll`, enter `Static export`, and commit.

## 5. View the updated website

Open **Actions** and wait for the newest Pages deployment to succeed. Then open the address displayed in **Settings → Pages**, normally:

https://noamanrd.github.io

If the old design remains, wait for deployment to finish and use **Ctrl + Shift + R** on Windows/Linux or **Command + Shift + R** on macOS. An incognito/private window also helps rule out cached files.

Check that:

- All eight projects have distinct full-colour illustrations.
- **Explore case** opens the correct project; **Escape** closes it.
- Research lists the ACS Sensors article, nickel-carbides article and Springer chapter with DOI links.
- The HKUST-1/SO₂ manuscript is separately marked **In submission process**.
- Contact opens an email to **nm@nuovofilm.com**.
- Navigation, images and text work on your phone.

## Future updates

For the next package, repeat steps 1–5. You normally do not change Pages settings again.

To edit it yourself, use **Noaman-Muhammad-Editable-Source-v6.zip**. Edit `app/page.tsx` for general content, `lib/publications.ts` for publication citations and `app/editorial.css` for design. Follow the source README to rebuild, then upload all the new `dist/client` contents together.

Do not edit only the compiled `index.html`: React also carries content in JavaScript. Do not mix the optional source-based GitHub Actions workflow with the prebuilt upload method.

## Troubleshooting

| Problem | Check |
| --- | --- |
| Home page is 404 | Repository name, root-level index.html and successful Pages deployment |
| Missing images or styles | Upload the complete assets, illustrations and expertise folders beside index.html |
| Old design is still visible | New deployment succeeded; hard-refresh or use a private window |
| Pages shows Verified domains | Open repository Settings rather than account Settings |

To undo an update, restore the relevant previous files from your backup or revert the update commit using Git/GitHub Desktop. Keep the repository and its history.

Official references:

- https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository
- https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

Instructions checked 5 September 2026. Preparing this package does not change your live GitHub website.
