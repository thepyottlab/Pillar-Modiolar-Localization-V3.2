# Pillar-Modiolar-Localization-V2
Updates in this version:

- It is no longer needed to manually reformat the Imaris Excel sheets. The script does it automatically.
- The output of the script is neatly organized.
- Descriptive statistics, such as means and medians are added.
- All relevant data is bundled into a single output file.

This github contains four zip files. Choose the right zip according to whether you're analyzing spots or surfaces.
Choose the zip with the right Imaris version. The Imaris 9.7.2 scripts will work as long as Imaris does not change the format of the Excel outputs.

To download the scripts, either download the full code containg all four releases in ZIP format from this screen or download the release you need from the 'Releases' tab on the right.

Known bugs:
- If the spots localization script does not contain spots with the ID 'Rib0' or 'PSD0', all calculated values will be deleted. To omit this, give the first PSD or ribbon pointID the value '0'
