# Bulk Emoji Renamer

Guide to export and import your custom emojis from one slack workspace to another without being an admin. This renamer currently supports jpg, gif, and png. Let me know if you'd like more file types, and I'll update the python function. 

## Export Your Emojis in Bulk from the Old Workspace

1. Install [Save All Resources](https://chrome.google.com/webstore/detail/save-all-resources/abpdnfjocnmdomablahdcfnoggeeiedb?hl=en-US) on Chrome extension.

2. Open your Developer Tools window on Chrome using Ctrl Shift J (on Windows), Ctrl Option J (on Mac), or Chrome's More Tools.

3. Click on **ResourceSaver**. Now you can download your resource files from your Custom Slack Emoji page.

4. Navigate to your workspace's custom emoji page: 'https://[workspace_name].slack.com/customize/emoji'.

5. Now scroll all the way through your workspace's emojis. This will store them in your **/top/emoji.slack-edge.com/T024FPYBQ/** folder. You can view it by going to the **Sources** tab in Developer Tools.

6. Once you have collected all the emojis, click Download on the **ResourcesSaver** tab. 

### Using the Emoji Renamer 

We'll now use the Emoji Renamer script to rename the files with their original workspace's names. Their folders currently have the files' original emoji names. They should have a similar file structure as **examples**. **favorites** contains some of my favorite slack emojis.

1. Now `git clone` the repo.

2. Rename **T024FPYBQ** to **emojis**. (Note: Feel free to test the repo's functionality by renaming **examples** to **emojis**.)

3. Place **emojis** inside the **emoji_renamer** directory.

4. Run `python emoji_renamer.py`. This will create a folder called **new_emojis** with all the renamed emoji files.

## Import Your Emojis in Bulk into the New Workspace

1. Download the [Neutral Face Emoji Tools](https://chrome.google.com/webstore/detail/neutral-face-emoji-tools/anchoacphlfbdomdlomnbbfhcmcdmjej) Chrome extension.

2. Navigate to your second workspace's custom emoji page and drop the renamed files into Neutral Face Emoji Tools' uploader. Slack throttles your uploads, so you will need to upload in batches. 

## Authors

[Dan Chiniara](https://github.com/djchinia)

## Acknowledgments

* Extracting Emojis from Slack (Firefox): https://gist.github.com/lmarkus/8722f56baf8c47045621 
* Renaming Files: https://www.geeksforgeeks.org/rename-multiple-files-using-python/ 
* Ariel Ahdoot for Emoji Inspiration and Sharing removebg: https://www.remove.bg/upload