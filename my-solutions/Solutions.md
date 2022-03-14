This folder is for any extra Javascript files, CSS files, or images needed for your solution

My solution entailed adding an ORU logo, moving the divs lower so that fallback text is visible when the iframe does not load.

Fundamentally, the reason Brave does not show the iframe is due to its ad blocking feature. This is pretty easy to disable. My fallback text prompts users to disable their ad blocker if they wish to fully engage with the embedded virtual tour.

The ideal solution would be able respond to the missing embed directly somehow, rather than require a visual redesign of the site. A popup message on site load warning users to disable ad blocking could also function as an alternative.

Given more time, I would spend more time looking for JavaScript could that would be able to discern the absence of the embedded iframes. The most promising solution I found involved using Vue.js to add a wrapper to the HTML that reads the load time of the embed. If the embed takes 10 seconds to show up, the code assumes that it will never load, and displays a fallback.