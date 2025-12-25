# YouTube-Screenshot-Notes-Generator

A **Google Colab project** to automatically generate **compact PDF notes** from YouTube videos using screenshots. This tool extracts key frames from a video at regular intervals and arranges them in a PDF to help with study notes, revision, or documentation purposes.


---

## Features

- ✅ **Single-cell Colab workflow**: download video → extract screenshots → create PDF → auto-download.  
- ✅ **Customizable screenshot interval**: control how frequently screenshots are taken.  
- ✅ **Compact PDF**: multiple screenshots per page to reduce empty space and total pages.  
- ✅ **Automatic resizing**: adjusts images to fit page while maintaining aspect ratio.  
- ✅ **Error handling**: handles invalid URLs, download failures, and missing frames gracefully.  
- ✅ **No manual upload required**: everything works from the YouTube link input.

---

## Requirements

- Google Colab
- Python 3.x
- Libraries:
  - `yt-dlp`
  - `opencv-python`
  - `Pillow`
  - `reportlab`

These libraries are automatically installed in the Colab notebook.

---

## How to Use

1. Open the notebook in **Google Colab**.
2. Run the single cell.
3. Enter the **YouTube video URL** when prompted.
4. The notebook will:
   - Download the video.
   - Extract screenshots at the specified interval.
   - Generate a PDF with multiple screenshots per page.
5. The PDF will automatically download to your device.

---

## Configuration

Inside the notebook, you can customize:

```python
SCREENSHOT_INTERVAL_SEC = 30   # Take a screenshot every 30 seconds
IMAGES_PER_PAGE = 2            # Number of screenshots per PDF page
OUTPUT_DIR = "yt_notes"        # Folder to save screenshots and PDF
PDF_NAME = "youtube_notes_compact.pdf"
