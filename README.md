# Using Bing Images to Create a Mask Compliance Classifier

### Summary
By scraping 17,000 images from Bing a small Convolutional Neural Network was able to be trained to accurately detect whether an image contains a masked person. 

Scraped images were made square and downsized to a reasonable size. 

Multiple edge cases were accounted for:
* Covered, but non-compliant faces. The model was trained to consider hands over mouths/noses as unmasked.
* Non-human entities. The model was trained to consider anything not human as neither masked nor unmasked.
The use case being that an automatic entry system doesn't need to display a message if the detected image is not a human attempting to use the machine.
* Multiple mask types were considered valid, including bandanas, surgical masks, and N95s.
