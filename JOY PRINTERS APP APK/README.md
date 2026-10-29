# JOY PRINTERS Android app project

This Android app opens the existing JOY PRINTERS staff system inside an Android WebView:
https://timely-puppy-4d3a51.netlify.app/

It is a lightweight online wrapper, not a separate offline database. Staff sign in using their existing website accounts; records remain in the existing online Supabase backend.

## Build an APK using GitHub Actions (no Android SDK needed on your computer)

1. Sign in to GitHub and create a **new private repository** named `joy-printers-android`.
2. Extract this ZIP on your computer.
3. Upload the *contents* of this folder into the repository (the `.github` folder must be included). Commit them to the `main` branch.
4. In the GitHub repository, open **Actions**.
5. Select **Build JOY PRINTERS Android APK** and press **Run workflow**. (A push to `main` also triggers a build.)
6. Wait for the workflow to finish with a green check.
7. Open that completed workflow run, scroll to **Artifacts**, and download `JOY-PRINTERS-Android-APK`.
8. Extract the downloaded artifact ZIP. It contains `app-debug.apk`.
9. Transfer `app-debug.apk` to the Android phone and open it to install. Android may ask you to allow installing unknown apps for the app you used to open the file.

## Important
- Keep the GitHub repository private because it is your business app project.
- Never upload Supabase service-role/secret keys to this project. The app uses the existing public website URL only.
- This first APK loads the live website and requires an internet connection.
- It does not change the Netlify website or Supabase database.
- Before using real financial records, verify admin/staff permissions, receipt printing, and database row-level security.
- For Google Play distribution or a signed release APK, a separate release-signing step is needed. This workflow produces a debug APK for direct installation/testing.
