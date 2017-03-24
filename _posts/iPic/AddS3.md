
---
title: 'Add Amazon S3 in iPic'
categories: iPic
---

Amazon Simple Storage Service ([Amazon S3](https://aws.amazon.com/s3/)) is easy to use object storage, with a simple web service interface to store and retrieve any amount of data from anywhere on the web. For more introductions, please refer to [Getting Started with Amazon Simple Storage Service](http://docs.aws.amazon.com/AmazonS3/latest/gsg/GetStartedWithS3.html)


# Add Amazon S3 in iPic

Open iPic's `Preferences`, clicks `Image Host`, and add `Amazon S3`.

![](https://farm6.staticflickr.com/5720/30641250313_2fcd39ec47_o.png)

Here is the introductions for all parts:

- `Bucket`
  - Same with the bucket in Amazon S3
- `Access Key` and `Secret Key`
  - Refer to [AWS Identity and Access Management (IAM) ](http://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html)
- `Http Prefix`
  - The endpoint for Amazon S3 bucket, e.g., *https://ipic-test.s3.amazonaws.com*

After fill all the parts, clicks the **Validate** button. If all the information above is correct, you can see the link of **Passed** in the right.

<!-- more -->

Beside the basic configuration above, Amazon S3 also supports several advanced ones. Click the 'Advanced' button in right of `Http Prefix`, you can see the following setting page.

![](https://farm6.staticflickr.com/5441/30641252243_a5b27a2da8_o.png)

- `Http Prefix`
  - Same with what ever introduced.
- `Filename Prefix`
  - Could understand as the folder in Amazon S3
  - For example, if you want iPic upload all images in `blog` folder, just input `blog` here. The image link will like *https://ipic-test.s3.amazonaws.com/blog/pic.jpg*
- `Filename`
  - The filename saved in Amazon S3. Now iPic supports these 3 kinds of filename.
  - `Only Filename` e.g.,  `pic.jpg`
  - `Date-Filename` e.g., `2016-06-16-pic.jpg`
  - `Random` e.g., `jk8l1.jpg`, could help to shorten the link.
- `Http Suffix`
  - Any characters in the end of the link.

After all, clicks **Apply** to save.







