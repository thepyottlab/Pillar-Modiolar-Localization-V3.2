# Pillar-Modiolar-Localization-V2.1
This github contains four zip files. Choose the right zip according to whether you're analyzing spots or surfaces.
Choose the zip with the right Imaris version. The Imaris 9.7.2 scripts will work as long as Imaris does not change the format of the Excel outputs in newer versions.

To download the scripts, either download the full code containg all four releases in ZIP format from this screen or download the release you need from the 'Releases' tab on the right.

Changelog:
  Version 2.1
- Fixed a bug in which no average/median/counts would be outputted if no spots have the ID 'Rib0' or 'PSD0'.
- Fixed 3D figure renders. Now shows spots in correct size and the pillar/modiolar axis is now transparent.
- Fixed 'NAs introduced by coercion' after principal component analysis.
- Fixed a bug in which the reformatting script would give an error message that the column names are automatically changed.
- Fixed a bug in which pressing 'source' would not work properly. It is no longer needed to run each line manually anymore. 
- Introduced various checkpoints with status updates throughout the script.
- Added a setting to select whether only ribbons or both ribbons and PSDs are analyzed.
- Updated the euclidian distance section to automatically remove data of unpaired/orphan ribbons or PSDs (setting ribbonsonly = TRUE reverses this).
- Added counts of unpaired modiolar/pillar ribbons/PSDs.

  Version 2.0
- It is no longer needed to manually reformat the Imaris Excel sheets. The script does it automatically.
- The output of the script is neatly organized and formatted.
- Descriptive statistics, such as means and medians are added.
- All relevant data is bundled into a single output file.
- Seperate versions for spots or surfaces in the older or newer Imaris versions are added.
