---
title: 'iPic Opens Upload API: iPicUploader'
categories: iPic
---

# iPic

![](https://farm6.staticflickr.com/5599/31306139462_e0753838bf_o.jpg)

iPic could automatically upload images and save Markdown links on macOS.

- Upload images by drag & drop.
- Upload images by services with shortcut [Command + U].
- Upload copied images with shortcut [Shift + Command + U].
- Support Imgur, Flickr, Amazon S3 and other image hosts.
- Support image link of Markdown format.
- [Video introduction](http://toolinbox.net/en/iPic/)

[Download iPic](https://itunes.apple.com/app/id1101244278?ls=1&mt=12&at=1000lv4R&ct=iPic_home) and have a try.

# iPicUploader

iPic opens the ability to upload images. It means if your App also needs to upload images, no need to build from scratch. Just use iPicUploader, your App could also upload images to Imgur, Flickr, Amazon S3 and other image hosts.

<!-- more -->

## iPicUploader Usage

Upload image file:

```swift
let imageFilePath = "/Path/to/the/pic.jpg"

iPic.uploadImage(imageFilePath, handler: { (imageLink, error) in    
	if let imageLink = imageLink {
		// Image uploaded        
	   
	} else if let error = error {
		// Some error happened
	}
})

```

Upload image data:

```swift
let imageFilePath = "/Path/to/the/pic.jpg"
let imageData = NSData(contentsOfFile: imageFilePath)!

iPic.uploadImage(imageData, handler: { (imageLink, error) in    
	if let imageLink = imageLink {
		// Image uploaded        
	   
	} else if let error = error {
		// Some error happened
	}
})

```

Upload NSImage:

```swift
let imageFilePath = "/Path/to/the/pic.jpg"
let image = NSImage(contentsOfFile: imageFilePath)

iPic.uploadImage(image, handler: { (imageLink, error) in    
	if let imageLink = imageLink {
		// Image uploaded        
	   
	} else if let error = error {
		// Some error happened
	}
})

```

## iPicUploader Example

iPicUploader also includes a full example. You will feel easy to start. To run the example project, just clone current repository and open *iPicUploader.xcworkspace*.

Note: 

- As the demo needs to upload images by iPic, you need to [download iPic](http://toolinbox.net/html/DownloadiPicWithService.html) at first. 
- No worry, you will also be guided to download iPic in the example.
- The example already dealt with these cases:
  - If iPic wasn't installed, guide user to download.
  - If iPic wasn't running, launch iPic automatically.
  - If iPic is running but not compatible, guide user to download latest version.

Now, let's have a look how the example upload images.

### 1. Upload Images by Drag & Drop

![](https://farm6.staticflickr.com/5506/31414737496_4aab9bbfd8_o.gif)

As you can see, iPicUploader support uploads multi-images at a time.

### 2. Upload Images by Select Images Files

![](https://farm6.staticflickr.com/5327/31306114252_c1dafd7632_o.gif)

### 3. Upload Images by Copy Image and Paste

![](https://farm6.staticflickr.com/5612/31333335491_30d9a56377_o.gif)

Beside copy image files, you can also copy the image in other Apps to upload.

## Requirements

As iPic runs on macOS 10.11 and newer version, iPicUploader also needs macOS 10.11+

## Installation

iPicUploader is available through [CocoaPods](https://cocoapods.org/?q=ipicuploader). To install
it, simply add the following line to your Podfile:

```ruby
pod "iPicUploader"
```

## License

iPicUploader is available under the MIT license.


