# PhotoSheet

**Print one, two, or four photos on a single A4 sheet — directly in your browser.**

PhotoSheet is a lightweight tool for arranging and printing photos. Select images, rotate and crop them, set spacing in millimeters, and check the result in a preview. The entire application lives in one HTML file and requires no installation, account, or backend.

## Features

- **Flexible layouts:** one A4 photo area, two approximately A5-sized areas, or four approximately A6-sized areas.
- **Portrait and landscape:** choose the orientation that suits your photos.
- **Precise spacing:** set outer margins and photo spacing from 0 to 30 mm, including decimal values such as `2.4` or `2,4`.
- **Image import:** load JPG, PNG, and WebP files individually, select multiple files, or drag and drop an image onto a photo area.
- **Crop controls:** fit the entire photo or fill the area, rotate in 90° steps, zoom up to 3×, and adjust horizontal and vertical positioning.
- **White border trimming:** automatically detect and remove white image borders, with an option to preserve them.
- **Quick arrangement:** swap photos 1 and 2 or fill all visible slots with photo 1.
- **Print preview:** view photo area dimensions, enable optional cut guides, and check approximate image resolution with a warning below 150 dpi.
- **Local processing:** photos stay in your browser and are not uploaded by the application.

## Quick start

1. Download the repository as a ZIP file and extract it, or clone it:

   ```bash
   git clone https://github.com/NoAuthZone/PhotoSheet.git
   cd PhotoSheet
   ```

2. Open `PhotoSheet.html` in a modern browser.
3. Select your photos and adjust the layout.
4. Click **Print A4 sheet** to open the print dialog.

No additional libraries, packages, or build steps are required. Once downloaded, the application can also be used offline.

## Usage

### Configure the layout

Use **Photos per sheet** to select one, two, or four photo areas. Choose portrait or landscape under **A4 orientation**. **Outer margin** controls the space around the sheet, while **Photo spacing** controls the gaps between photos.

With two photos, the areas are stacked vertically in portrait orientation and placed side by side in landscape orientation. Four photos use a 2 × 2 grid. The actual dimensions are shown below the layout settings and depend on the selected margins and spacing.

### Select photos

Use **Select multiple photos**, choose a file for an individual slot, or drag an image file onto the desired photo area. Multiple files are loaded in the order supplied by the file picker. A sheet can hold up to four photos.

### Adjust each photo

| Control | Effect |
| --- | --- |
| **Fit entire photo** | Fits the whole photo within the area. White space may remain, depending on its aspect ratio. |
| **Fill area / crop** | Fills the entire area and crops any image content extending beyond its edges. |
| **Rotate 90°** | Rotates the photo by 90 degrees per click. |
| **Zoom** | Enlarges the photo from 1× to 3×. |
| **Horizontal / Vertical** | Adjusts the photo's position within its area. |
| **Reset crop and rotation** | Resets rotation, zoom, and positioning while keeping the selected fit mode. |
| **Remove** | Removes the photo from its slot. |

**Trim white borders from photos** is enabled by default. Disable it when white borders are part of the image and should be preserved.

## Printing at the correct size

Check these settings in the print dialog:

1. **Paper size:** A4.
2. **Orientation:** match the orientation selected in PhotoSheet.
3. **Scale:** 100% or actual size.
4. **Headers and footers:** disabled.
5. **Paper and quality:** select photo paper and a suitable high-quality setting in the printer driver.
6. **Page count:** the print preview should show exactly one page.

Printing to the edge of the sheet with a **0 mm outer margin** requires a printer that supports borderless printing. Otherwise, set an appropriate outer margin. The final output also depends on your browser and printer driver.

You can also save the sheet as a PDF through the print dialog if your browser or operating system provides that option.

## Privacy and technical details

PhotoSheet processes selected images locally using JavaScript and the Canvas API. The current source code includes no external libraries, analytics, or upload functionality. The HTML file contains the complete interface, styles, and application logic.

Photo areas are rendered to canvas at a target resolution of **300 dpi**. The effective image resolution depends on the original image, the photo area dimensions, and the zoom level. An approximate dpi value is displayed for each photo.

Selected photos and settings are not saved persistently. Reloading or closing the page clears the arrangement.

## Project structure

```text
PhotoSheet/
├── PhotoSheet.html   # Complete browser application
├── LICENSE           # MIT license
└── README.md         # Project overview and instructions
```

## Contributing

Bug reports and feature suggestions are welcome through [GitHub Issues](https://github.com/NoAuthZone/PhotoSheet/issues). To contribute changes, fork the repository and submit a pull request.

## License

PhotoSheet is released under the [MIT License](LICENSE).

Copyright © 2026 NoAuthZone.
