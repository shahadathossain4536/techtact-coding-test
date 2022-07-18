# Goal: Build a shopify app to optimize images

## Business Requirements:
- The plugin should be activated with a simple click-to-activate button instead of having to copy and paste code. (an option to be added via google tag manager is a plus)
- The plugin should not be invasive. It should not alter the images that are already uploaded by the shopify store owner and be served through a CDN
- It should automatically detect the <img /> used in the theme and make the required changes (in case a data attribute is being used to serve the images)
- Once the plugin is disabled there should not be any changes to the state of the shop before using the plugin
- It would be nice to have a timeframe to re-activate the plugin (in case disabled by mistake or for testing purposes)

## Technical Requirements:
- Before the target image is loaded, a blurred version of the image should be used as a placeholder using a CDN
- Target image should be converted to .webp
- Build a responsive source set for the target image and serve it according to device size
- Lazyloading should be enabled for the target image
- Gifs must be converted to video format (using webm/mpeg)
- Target image should not exceed the parent box dimensions, for example if the parent <div> has a width of 300px in a specific media query (device size) e.g. tablet, the image width should not be more than 300px.
- Target images should be cached if they are not changed for a day
