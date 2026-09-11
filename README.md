# Docs&Loyalty

A simple iOS app for keeping photo copies of documents, government items, business paperwork, and loyalty cards in one place.

Built with SwiftUI, with support for iPhone.

## Features

### Documents and loyalty cards
- Separate tabs for **Docs&Gov Items** and **Loyalty**.
- Organize documents into Personal, Government, Business, and Other categories.
- Search items by title within each tab.
- Rearrange items using drag and drop.
- Delete items with a dedicated deletion mode.

### Capture and crop
- Add images using the camera or photo library.
- Adjust all four corners to crop and correct perspective.
- Capture the back of a document and keep both sides together.

### Loyalty views
- Switch between a detailed list and a compact grid.
- Grid tiles display the store name and icon.
- Optionally provide a store URL to fetch its favicon.

### Full-screen viewing
- Tap an item to view its images full screen.
- Two-sided documents display both images vertically.
- Screen brightness temporarily increases to maximum and is restored when viewing ends.

### PDF sharing
- Share an individual item through the standard iOS share sheet.
- Export images centered on various size pages.
- Choose a standard object size or enter dimensions manually.
- Preserve image proportions, with each side on a separate page.

Physical dimensions are selected by the user, not automatically measured by the camera.

### Collection cloning
- Export all items from both tabs as a `.docsandloyalty` archive.
- Transfer the archive using AirDrop or other compatible sharing options.
- Import it on another device with Docs&Loyalty installed.
- Matching names receive numbered suffixes instead of overwriting existing items.

### Localization
- English and Croatian.
- English is the fallback for unsupported languages.
- Language selection uses the standard iOS per-app settings.

## Usage

### Add an item

1. Select the appropriate tab.
2. Choose **Add**.
3. Enter a title and, for documents, select a category.
4. For loyalty cards, optionally enter the store URL.
5. Take a photo or select an existing image.
6. Adjust the crop and save.

When capturing a document with the camera, you can also add its back side.

### Organize your collection

Use the search field to filter items by title. Open the actions menu to add, delete, or reorder items. In the Loyalty tab, use the display menu to switch between list and grid layouts.

### Share one item

Open the item, tap **Share**, choose its physical dimensions, and share the generated PDF through an available app.

### Clone all items

Tap the clone icon beside the app title and confirm the warning. The exported archive includes items from every tab, not just the current search results.

## Technology

- Swift and SwiftUI
- UIKit integration for camera capture and system sharing
- Perspective-corrected image cropping
- Local image and metadata persistence
- PDF generation
- English and Croatian localization resources

## Storage and Privacy

Items are stored locally on the device. Providing a store URL enables a network request to retrieve its favicon.

Documents may contain sensitive information. Review the selected item before sharing a PDF, and remember that cloning exports the entire collection.

## Limitations

- Stored images are photo copies, not replacements for original documents or official digital credentials.
- The app does not provide OCR, payment functionality, or Apple Wallet integration.
- Accurate physical sizing in PDFs requires a standard format selection or manually entered dimensions.
- Available sharing destinations depend on the apps installed on the device.
