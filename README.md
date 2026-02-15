# Wedding Website - Setup Instructions

## 📁 Folder Structure

Create the following folder structure on your computer or web hosting:

```
wedding-website/
│
├── index.html          (the main website file)
├── images/             (create this folder)
│   ├── img (1).JPG
│   ├── img (2).JPG
│   ├── img (3).JPG
│   └── ... up to img (200).JPG
│
└── videos/             (create this folder)
    ├── ceremony.mp4
    ├── reception.mp4
    └── firstdance.mp4
```

## 🔐 How to Change the Password

1. Open `index.html` in a text editor (Notepad, TextEdit, VS Code, etc.)
2. Find line 375 which says:
   ```javascript
   const CORRECT_PASSWORD = 'wedding2024';
   ```
3. Replace `'wedding2024'` with your desired password
4. Save the file

**Example:**
```javascript
const CORRECT_PASSWORD = 'OurSpecialDay2024';
```

## 📸 Where to Put Your Photos

1. Create a folder named `photos` in the same location as `index.html`
2. Copy all your wedding photos into this folder
3. Make sure your photos are named exactly as: `img (1).JPG`, `img (2).JPG`, etc.
4. The website will automatically load all 200 photos

**Important:** 
- The naming must be exact: `img (1).JPG` not `img(1).JPG` or `img 1.JPG`
- The file extension should be `.JPG` (uppercase)
- If your files have lowercase `.JPG`, that's fine too, just update line 378 in the code

## 🎥 Where to Put Your Videos

1. Create a folder named `videos` in the same location as `index.html`
2. Copy your video files into this folder
3. By default, the website expects these video files:
   - `ceremony.mp4`
   - `reception.mp4`
   - `firstdance.mp4`

### To Change Video Files or Add More Videos:

Open `index.html` and find lines 384-388:
```javascript
const videos = [
    { file: 'videos/ceremony.mp4', title: 'Wedding Ceremony' },
    { file: 'videos/reception.mp4', title: 'Reception Highlights' },
    { file: 'videos/firstdance.mp4', title: 'First Dance' }
];
```

**To add more videos:**
```javascript
const videos = [
    { file: 'videos/ceremony.mp4', title: 'Wedding Ceremony' },
    { file: 'videos/reception.mp4', title: 'Reception Highlights' },
    { file: 'videos/firstdance.mp4', title: 'First Dance' },
    { file: 'videos/speeches.mp4', title: 'Speeches' },
    { file: 'videos/bouquet-toss.mp4', title: 'Bouquet Toss' }
];
```

**To remove a video:** Simply delete the entire line

**If you don't have videos yet:** Delete all the lines between the square brackets `[ ]` so it looks like:
```javascript
const videos = [ ];
```

## ➕ How to Add More Photos Later

### Method 1: Add to the End
1. Continue numbering from where you left off
2. For example, if you have 200 photos and want to add 50 more:
   - Name the new photos: `img (201).JPG`, `img (202).JPG`, ... `img (250).JPG`
3. Update the total count in `index.html` on line 376:
   ```javascript
   const TOTAL_PHOTOS = 250;  // Changed from 200 to 250
   ```

### Method 2: Start Fresh
1. Rename all photos from 1 to however many you have total
2. Update the `TOTAL_PHOTOS` number accordingly

## 🌐 How to Use the Website

### Option 1: Use Locally (On Your Computer)
1. Simply double-click `index.html`
2. It will open in your web browser
3. Enter the password to view the website

**Limitations:** 
- Only works on your computer
- Others cannot access it

### Option 2: Upload to Web Hosting
1. Upload all files (index.html, photos folder, videos folder) to your web hosting
2. Share the website URL with family and friends
3. They can enter the password to view your wedding memories

**Recommended Free Hosting Options:**
- **Netlify** (easiest - drag and drop upload)
- **GitHub Pages**
- **Vercel**
- Any basic web hosting service

### Option 3: Upload to Google Drive/Dropbox (Alternative)
1. Zip the entire wedding-website folder
2. Upload to Google Drive or Dropbox
3. Share the zip file with family and friends
4. They download it and open index.html on their computer

## 🎨 Customization Tips

### Change Website Title and Heading:
- Line 6: Change `<title>Our Wedding Memories</title>`
- Line 253: Change `<h1>Our Wedding Memories</h1>`
- Line 254: Change `<p>Thank you for celebrating with us</p>`

### Change Color Scheme:
The current colors are warm brown/beige tones. To change:
- Line 45: `#8b7355` is the main brown color
- Line 81: `#d4a5a5` is the pink/rose color
- Search for these colors in the file and replace with your preferred colors

## 📱 Mobile-Friendly

The website is fully responsive and works perfectly on:
- Desktop computers
- Tablets
- Smartphones

## 🔒 Security Note

This password protection is **basic security** suitable for sharing with family and friends. It's not bank-level security, but it prevents casual access to your photos.

The password is stored in the HTML file, so anyone with technical knowledge could potentially find it if they view the page source. For most family sharing purposes, this is perfectly fine.

## ⚡ Performance Tips

**For Better Loading Speed:**
1. Compress/resize your photos before uploading (recommended: max 2000px width)
2. Use tools like TinyPNG or JPEGmini to reduce file sizes
3. For videos, use compressed MP4 files (H.264 codec works best)

## ❓ Troubleshooting

**Photos not showing:**
- Check that the `images` folder is in the same location as index.html
- Verify photo file names match exactly: `img (1).JPG`
- Check file extensions (.JPG vs .JPG)

**Videos not playing:**
- Ensure videos are in MP4 format
- Check that the `videos` folder exists
- Verify video file names match the code

**Password not working:**
- Check for typos in the password
- Password is case-sensitive
- Clear browser cache and try again

## 📧 Support

If you encounter any issues, check that:
1. All folders are in the correct location
2. File names match exactly
3. The password is typed correctly
4. You're using a modern web browser (Chrome, Firefox, Safari, Edge)

---

**Enjoy sharing your beautiful wedding memories! 💕**
