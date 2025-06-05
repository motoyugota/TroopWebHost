# Troopwebhost Gallery
## Adding Galleries
1. Add a Json file to Google Drive.
   1. See [Json Format](#json-format) below to generate the Json file.
   2. Edit using https://texteditor.co/
   3. Share the file and copy the Share link.
2. Add a custom page to the site.
   1. Update the HTML file
      1. Replace `[JsonFileUrl]` with the shared link from Google Drive.
      2. Paste the content into the source for the custom page.
3. Add a new Section to the home page
   1. Choose "My Content" for `Section Type`
   2. Update the Widget HTML
      1. Get the URL for the gallery page
         1. Go to the gallery page
         2. Click on the Question Mark in the header
         3. Click on "About This Site"
         4. Copy the URL from the popup
      2. Replace `[ViewAllUrl]` with the  URL found in the previous step
      3. Replace `[JsonFileUrl]` with the shared link from Google Drive.

## Json Format:

    {
        "albums": [
            {
                "coverPhotoBaseUrl": "[CoverImageUrl]",
                "title": "[GalleryName]",
                "shareUrl": "[GalleryShareUrl]"
            }
        ]
    }

### Google Photos

* `GalleryShareUrl`
  1. Click on the Share icon in the album and click "Copy Link".
  2. Use this URL for the `GalleryShareUrl` value.
* `CoverImageUrl` 
  1. Choose an image in the gallery to use as the cover image. 
  2. Click on the Share icon for the photo and click "Copy Link".
  3. Open an Incognito/Private browser window
  4. Go to the share link in this window
  5. Right click on the photo and choose "Copy Image Link"
  6. Use this URL for the `CoverImageUrl` value.

### iCloud Photo Album

* `GalleryShareUrl`
  1. [Get the share URL]
* `CoverImageUrl`
  1. iCloud doesn't have a way to share an individual image
  2. Choose in image in the gallery to use as the cover image
  3. Download the image
  4. Upload the image to Google Drive, or anything else that lets you publicly share an image
  5. Get the share link for this image
  6. Use this URL for the `CoverImageUrl` value.