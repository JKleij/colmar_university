COLMAR UNIVERISTY


-- INTRODUCTION --

This is the final assignment for the "Learn How to Build Websites" course from the Codecademy.

The objective was to build a website from scratch. A wireframe was provided giving some design details on the structure and dimenstions of the website while viewing in desktop and mobile mode. Furthermore the necessary assets (images, video and icons) were provided. These documents have been included in the GitHub folder (design subfolder).

While fonts and colors were not provided I chose to stay as close as possible to the used fonts and colors within the wireframe (because I liked this design).

css file (style.css) setup in such a way that it read top to bottom and right to left in accordance with the html file (index.html). This way another user should have an easier time navigating all css. Also tried to have a naming convention that gives further indication to what section you are and on what location of the page. Used text to create some headers to make it even more clear. Hope that is helpful.


-- DESIGN DECISIONS --

TEXT HEADERS:
Decided to use headers h1, h3 and h5 for the different section and sub-headings. This way there are some headers in between left in case of future changes. Furthermore use paragraph (p) for regular text within the different sections. The anchors (a) are used for hyperlink references but shouldn't add any styling except for the navigation bar.


IMAGES:
1. I tested the shrinking/growing of the website on a large screen (34"). I noticed that while growing the window, certain images stopped increasing in size. I tried to fix that with adding flex-grow: 1 in style.css but that didn't fix it. I now assume that it is because the image cannot grow beyond its original dimensions. To test this I increased the image dimensions to the maximum needed at 34" and after that the images continued to scale as desired.

I first tried another way to solve it by using an empty <div> with a background image. But I thought it was mentioned that you shouldn't use empty <div>'s so didn't do that in the end. Tried it out though but box height was not a result of the background image but of content of the box. So walked away from this idea also because I didn't want to hard code heights to compensate.

?? Question: is there another (better/easier) way to do this and make an image scale beyond its original dimensions?


TILES IN START LEARNING SECTION:
First designed the section in such a way that picture + text was inside a tile (courses-tile) and gave the tile a 16px margin. The six tiles are inside a container (courses-container). To get 3 tiles on a row I first maximized the max width to 31%. However, this way I could not control the margin in between the tiles and the number of tiles on a row while shrinking or growing the window. Decided to add another box around the tile (courses-box) and gave that a padding. This way I could maintain 3 tiles on a row while also controlling the space in between the tiles to be 16px as per design, even when shrinking/growing the window. But then the white background of the text section (courses-tiles-text) gave me some headache because the text-wrapping on resizing the window caused differences in the heights between the text-sections of the different tiles (e.g. some text only consumed one row while others were already on two). I could not give the entire tile a white background because then also the padding between the tiles would become white. So I solved this difference in height with @media statements at the different breakpoint to control minimum height for the text-sections to ensure all the six text-sections of the tiles have the same height at all dimensions.

?? Question: is there another (better/easier) way to do this and make all course tiles have automatically the same height across all rows?


REFERENCES (HYPERLINKS):
For the "Start here" in the main-banner section and the courses tiles in the main-courses section I chose to make the entire box the hyperlink. This way a user doesn't need to find the hyperlink (e.g. the header h3) but can just click anywhere in the tile. That seemed more convenient to me.


DESKTOP VERSUS MOBILE:
Created breakpoint at 950px where I changed to mobile design. Selected this breakpoint because found that the right-hand side tiles in the main-information section became too small and I wanted to swap to the column orientation. Could have designed like an intermediate between desktop and mobile (e.g. iPad) but didn't want to complicate the project anymore and think that the mobile design at 950px also works well.

Decided not to change the font-size as I think it still looks good at smaller sizes. Tested my work using Chrome and IE and Opera browsers. From screen size width of 350px up to 3440px. Found no issues between them.


OTHER:
Used slightly bigger ColmarAcademy logo in header because thought 32px was too small.

Kept background color for 'Start here' button in mobile version identical to desktop version because of consistency (why would it need to be different)

Overruled bottom padding of 24px for gray courses containers for mobile design because top and bottom should be equal (to my opinion).

Kept footer section same in both desktop and mobile with 16px 24px 32px padding because didn't want it to get too small in mobile version as there are hyperlink in there.

As I had the same issue with the video in the thesis-section at larger screen sizes I changed video section (left) to 55% (versus 60%) to avoid section to stop growing beyond the video maximum width of 1920 px.