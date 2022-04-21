# Pillar-Modiolar Localization V2.3
<p align="center">
  <img width="400" height="400" src="./output.gif">
</p>

# How to install
This github contains four zip files. Choose the right zip according to whether you're analyzing spots or surfaces.
Choose the zip with the right Imaris version. The Imaris 9.7.2 scripts will work as long as Imaris does not change the format of the Excel outputs in newer versions.

To download the scripts, either download the full code containg all four releases in ZIP format from this screen or download the release you need from the 'Releases' tab on the right.

# Instructions
For detailed instructions, see the "Readme.txt" file that is bundled with the scripts.
1. Export your data from Imaris with the correct names for your spots and surfaces (i.e., "Ribbons","Nucleus","PSD","Pillar","Modiolar".
2. Convert the Imaris output from XLS to XLSX (a macro is bundled with the scripts to convert a batch of XLS files simultaneously).
3. Copy the XLSX file into the folder containing the scripts.
4. Run "Install packages.R" if this is your first time using this script. Run this again whenever you update from an older version of this script.
5. Open 'Synapse_script.R" and press "Source".

NOTE: if you only exported ribbon volumes, set "Ribbonsonly" to "TRUE" in "Synapse_script.R" before running the script. When running the script with only ribbon data, R will give the following error message: "In min(tmp) : no non-missing arguments to min; returning Inf". This can be ignored.

# Changelog:

Version 2.3
- Fixed bug in which processing multiple files would give error that the directories are already created.
- Fixed bug in which no unpaired ribbons/psds would delete the entire dataframe and induce a fatal error.

Version 2.2
- Added counts per inner hair cell for volume analysis scripts.
- Reorganized statistics. The output excell files now contain four sheets with different categories of data, since 45 columns on one sheet became too cluttered.
- Added a setting to make histograms and boxplots of the volumes in the output excel file for the volume analysis scripts.
- Added a setting to make barplots of the counts in the output excel file for the spot localization script.
- Removed redundant lines of code.

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
