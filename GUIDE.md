# Golan Cleaner Pro: feature and use guide

[العربية](GUIDE.ar.md) · [Overview](README.md) · [Downloads and full source](https://github.com/GOLAN2CODE/golan-cleaner-pro/releases)

## Purpose and access

Version **0.11.1 / code 14** is an Android 9/API 28+ storage and file-management preview with three main areas: Clean, Files and Saved. It works on areas Android allows you to access. Installing the APK does not grant permission to all storage or automatically authorize deletion.

Download the debug APK and checksums from Releases, install and choose the function you need. Grant storage/folder access manually: Android 9 uses storage permissions, Android 10 may require a selected folder, and Android 11+ optionally supports all-files access. App-private/system paths and protected Android areas remain restricted. Revoking permission prevents later work that needs that access.

## Clean: review before removing

Start a scan of the selected accessible scope to get measured results and suggestions. Interpret the displayed scope and any incomplete results: a folder scan does not represent every file on the phone. Review candidates individually; age, filename, size or a duplicate suggestion does not by itself prove a file is unwanted.

Reviewed file removal first creates a verified private recovery copy and durable record before unlinking the original. Limits include 100 files per review and 256 MiB per file. The shared recovery budget is 1 GiB with a 16 MiB reserve. Restore creates a fresh name instead of overwriting. Recovery copies consume storage until you explicitly remove them; deleting them permanently ends that recovery option. Uninstalling or clearing app data also destroys the private recovery store, so it is not an independent backup. Empty-folder removal does not promise a file recovery copy.

Automatic cleanup is OFF by default and needs separate explicit configuration. Approve up to eight exact folders and limited old temporary/cache contents, with a minimum age of 14 days. It checks unchanged observations at least 30 seconds apart and fresh authority before removal. Each run is limited to 20 files/16 MiB with a cooperative 60-second budget. Daily scheduling is optional, inexact and resource-constrained; storage permission alone never enables it. Private browser caches cannot be universally cleaned; manual Android settings links are separate operations.

## Files and device tools

Browse allowed folders, search/sort the current folder and select items for the supported actions. Depending on access/backend, these include details, open/share, new folder, rename, file copy/move and reviewed removal. Listings are limited to 2,000 direct entries and identify incomplete output. No recursive folder mutation or overwrite is promised. Device information, visible-app permission details and Android-confirmed uninstall help review the phone without silently removing applications.

## Saved: selected future notifications

Enable archiving separately after its disclosure, manually grant notification access and select apps/conversations with independent text/image choices. The output is private encrypted records and images that eligible future notifications actually offer with a readable URI grant. An image may be a thumbnail. Limits include 8 MiB per image and 128 MiB of private image reservations.

**Video acquisition/downloading is not implemented.** Video/MP4 counters are diagnostics, not saved-video results. The app cannot prevent sender deletion, retrieve older unseen messages or guarantee attachments from every messaging app. It is not universal media recovery.

## Costs and computer FAQ

The APK has no Internet permission. No personal billed API key or payment integration was found in the reviewed source. Cleaning, file actions and the local archive do not require a running computer, Codex or this chat. Separate apps, shared exports and mobile network use may still have their own costs. Keep the phone configured for the permissions/background behavior needed by any optional scheduled or notification function.
