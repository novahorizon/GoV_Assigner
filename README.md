# GoV_Assigner
Locally ran web app to randomly assign roles for comic dubbing.
- Export and Import Save files containing Performers, Projects, and Characters
- Track who wasn't assigned main characters between sessions and make them more likely to be chosen

Installation:
- Download the files and run index.html
- Add performers, then send them to Extras to put them in the pool for random selection. Drag and drop to manually assign roles.
- For an example save, you can import `RoleAssigner_save1769801809728.json`

<img width="2536" height="1262" alt="image" src="https://github.com/user-attachments/assets/ff1ac146-5e44-4ebd-9c61-e7d221054a4a" />

Notes:
- The random selection algorithm prioritizes people who were not assigned to main cast members. If you want to manually reset the penalty that a frequent reader receives, you can edit the .json file and set the "performed" value back to 0. This value is incremented by 1 if a performer was assigned to a character during the session (Max 9), and is decremented if they were inactive or only played extras. This value is recalculated when the file is saved, but only once per day. It references the timestamp in the filename of the last loaded save for this (and will alwways trigger on the first save if no save has been previously loaded.)
