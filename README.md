# GoV_Assigner
Locally ran web app to randomly assign roles for comic dubbing.
- Export and Import Save files containing Performers, Projects, and Characters
- Track who wasn't assigned main characters between sessions and make them more likely to be chosen

Installation:
- Download the files and run index.html
- Add performers, then send them to Extras to put them in the pool for random selection. Drag and drop to manually assign roles.
- If you want images, upload them according to the Example Project folder at images/ProjectName/CharacterName. The example images work with the project in `ExampleSave.json`.

<img width="2557" height="1262" alt="image" src="https://github.com/user-attachments/assets/8d84e319-7ca1-4917-a91a-92abc804ae26" />

Notes:
- The random selection algorithm prioritizes people who were not assigned to main cast members. If you want to manually reset the penalty that a frequent reader receives, you can edit the .json file and set the "performed" value back to 0. This value is incremented by 1 if a performer was assigned to a character during the session (Max 9), and is decremented if they were inactive or only played extras. This value is recalculated when the file is saved, but only once per day. It references the timestamp in the filename of the last loaded save for this (and will alwways trigger on the first save if no save has been previously loaded.)
- The character images function expects to find the image in an `images` folder at the same level as the `index.html`. Load the ExampleSave for an example on how to do this, and click on any "No Image Found" box to show information on where you need to put that image.


