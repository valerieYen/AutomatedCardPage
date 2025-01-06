# Google Sites Profile Card Display
This guide will help you set up a dynamic profile card display on your Google Site. The display shows participant cards with photos, names, team numbers, and other information pulled from a Google Sheet.

## Prerequisites
- A Google Site where you want to display the cards
- A Google Sheet containing participant information
- Basic familiarity with Google Sites and Google Sheets

## Setup Instructions

### 1. Prepare Your Google Sheet
1. Create a new Google Sheet with the following columns:
   - `firstName`
   - `lastName`
   - `groupNumber`
   - `pronouns` (optional)
   - `major`
   - `year`
   - `hsUrl` (for profile photo URL)
   - `liUrl` (for LinkedIn profile URL)

2. Fill in your participant information
3. Make the sheet public:
   - Click "Share" in the top right
   - Change access to "Anyone with the link"
   - Set permission to "Viewer"

### 2. Set Up Sheety
1. Go to [sheety.co](https://sheety.co)
2. Create a new account or sign in
3. Create a new project
4. Paste your Google Sheet URL
5. Copy the generated API URL
** Note, somewhere Sheety will ask you what permissions you want to give it. This fiel only needs "READ" **

### 3. Add the Code to Google Sites
1. In Google Sites editor, click the `+` button to add an element
2. Choose "Embed"
   - Alternatively, just select "Embed" under the Insert tab
4. Click the `<>` (Embed code) option
5. Copy the entire HTML code provided
6. Replace `"YOUR SHEETY URL HERE"` with your Sheety API URL
7. Click "Next" and then "Insert"

## Troubleshooting
- If cards don't appear, check your browser console for errors
- Testing this code in localhost will load all information except for profile pictures, ensure everything works when you put the embed into the site
- Verify your Sheety URL is correct
- Ensure your Google Sheet is publicly accessible
- Check that column names in your sheet exactly match the ones used in the code
  - Verify this by using a "console.log()" on the json returned from Sheety to verify object attribute names

## Features
- Responsive card layout
- Sort participants by:
  - Name
  - Team number
  - Year (ascending and descending)
- Automatic fallback image for missing profile photos
- LinkedIn profile integration
- Cross-device compatibility

## Notes
- Profile photos should be hosted online at Imgur (when you host the photo, you must copy the image's address, not the link to the post)
- LinkedIn URLs must start with "https://" to display properly
