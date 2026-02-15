# Wedding Gallery Website 💕

A beautiful, password-protected wedding gallery website with a romantic pink and gold theme.

## Features ✨

- **Password Protection**: Secure access with password screen (Password: `shadi2026`)
- **Dynamic Image Loading**: Automatically loads images from the `images` folder
- **Responsive Design**: Works perfectly on desktop, tablet, and mobile devices
- **Lightbox Gallery**: Click any image to view in fullscreen with navigation
- **Video Section**: Display wedding video
- **Download Instructions**: Helpful guide for downloading all photos
- **Beautiful Animations**: Smooth transitions and hover effects throughout

## Setup Instructions 📋

### 1. File Structure

Create the following folder structure:

```
wedding-gallery/
├── index.html
├── style.css
├── script.js
├── video.mp4 (your wedding video)
└── images/
    ├── img (1).JPG
    ├── img (2).JPG
    ├── img (3).JPG
    └── ... (up to img (100).JPG)
```

### 2. Adding Your Images

1. Create a folder named `images` in the same directory as `index.html`
2. Place your wedding photos in the `images` folder
3. **IMPORTANT**: Name your images exactly as: `img (1).JPG`, `img (2).JPG`, `img (3).JPG`, etc.
   - Use this format: `img (NUMBER).JPG`
   - Include the space between "img" and the number
   - Use capital `.JPG` extension
4. If you have more or fewer than 100 images:
   - Open `script.js`
   - Find the line: `const TOTAL_IMAGES = 100;`
   - Change `100` to your actual number of images

### 3. Adding Your Video

1. Place your wedding video file in the same directory as `index.html`
2. Name it `video.mp4`
3. If your video has a different name or format:
   - Open `index.html`
   - Find: `<source src="video.mp4" type="video/mp4">`
   - Update the filename and type accordingly

### 4. Changing the Password

To change the password:
1. Open `script.js`
2. Find the line: `const CORRECT_PASSWORD = 'shadi2026';`
3. Replace `shadi2026` with your desired password

### 5. Running the Website

Simply open `index.html` in any web browser:
- Double-click the file, or
- Right-click and select "Open with" → Your preferred browser

## Usage Guide 🎯

### For Guests:

1. **Enter Password**: Type `shadi2026` and click "View Gallery"
2. **Browse Photos**: Scroll through the beautiful photo grid
3. **View Fullscreen**: Click any photo to see it in fullscreen mode
   - Use arrow buttons or keyboard arrows to navigate
   - Press ESC or click X to close
4. **Watch Video**: Click the "Video" tab to watch the wedding video
5. **Download Photos**: Click the "Download" tab for instructions to save all photos

### Navigation:

- **Photos Tab** 📷: View all wedding photos in a grid layout
- **Video Tab** 🎬: Watch the wedding video
- **Download Tab** ⬇️: Instructions for downloading all images

### Keyboard Shortcuts (in Lightbox):

- `←` Left Arrow: Previous image
- `→` Right Arrow: Next image
- `ESC`: Close lightbox

## Customization Options 🎨

### Change Colors

Edit `style.css` and modify these variables at the top:

```css
:root {
    --blush-pink: #FFE4E1;      /* Light pink background */
    --rose-pink: #FFB6C1;        /* Medium pink accents */
    --deep-pink: #FF69B4;        /* Primary pink */
    --gold: #FFD700;             /* Gold accents */
    /* ... more colors */
}
```

### Change Fonts

The website uses:
- **Great Vibes**: Elegant script font for titles
- **Italiana**: Sophisticated serif for headings
- **Lora**: Readable serif for body text

To change fonts, edit the Google Fonts link in `index.html`.

### Modify Text Content

All text content can be edited directly in `index.html`:
- Main title: "Our Wedding Day"
- Subtitle: "A celebration of love and togetherness"
- Footer message: "Thank you for celebrating with us!"

## Technical Details 🔧

### Browser Compatibility

- ✅ Chrome (recommended)
- ✅ Firefox
- ✅ Safari
- ✅ Edge
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

### Performance Features

- Lazy loading for images (loads images as you scroll)
- Smooth animations with CSS
- Optimized for mobile devices
- Responsive image grid

### Image Format Support

The script looks for `.JPG` files by default. If your images have different extensions:
- Open `script.js`
- Find: `const imagePath = `images/img (${i}).JPG`;`
- Change `.JPG` to your extension (e.g., `.jpg`, `.jpeg`, `.png`)

## Troubleshooting 🔍

### Images Not Showing?

1. **Check file names**: Must be exactly `img (1).JPG`, `img (2).JPG`, etc.
2. **Check folder**: Images must be in a folder named `images`
3. **Check extension**: Must be `.JPG` (or update script if using different format)
4. **Check browser console**: Press F12 to see any error messages

### Video Not Playing?

1. **Check file name**: Must be `video.mp4` in the same folder as `index.html`
2. **Check format**: Browser may not support the video codec. Try converting to H.264 MP4
3. **File size**: Very large videos may not play smoothly. Consider compressing the video

### Password Not Working?

1. **Check spelling**: Password is case-sensitive: `shadi2026`
2. **Check script**: Make sure `script.js` is in the same folder as `index.html`
3. **Browser console**: Press F12 to check for JavaScript errors

## Security Note 🔒

This is a **client-side password protection**. The password is stored in the JavaScript file, which means:
- It prevents casual access
- **It is NOT suitable for highly sensitive content**
- Anyone who views the page source can find the password

For stronger security, consider:
- Using a proper backend authentication system
- Hosting on a platform with built-in password protection
- Using a service like Netlify with password protection

## Deployment Options 🌐

### Option 1: Local Use
- Just open `index.html` in a browser
- Share the folder with guests via USB/email

### Option 2: Web Hosting
- Upload all files to any web hosting service
- Free options: GitHub Pages, Netlify, Vercel
- Share the URL with guests

### Option 3: Cloud Storage
- Upload to Google Drive or Dropbox
- Share the folder link (with password in a separate message)

## Support & Credits 💝

Created with love for your special day!

**Technologies Used:**
- HTML5
- CSS3
- Vanilla JavaScript
- Google Fonts (Great Vibes, Italiana, Lora)

---

**Enjoy sharing your beautiful wedding memories!** 💕✨

For any issues or questions, refer to the troubleshooting section above.
