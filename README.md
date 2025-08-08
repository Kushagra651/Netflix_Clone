Netflix Clone - HTML & CSS
A responsive, front-end clone of the Netflix India homepage built entirely with modern HTML5 and CSS3. This project focuses on recreating the look and feel of the Netflix landing page, with a special emphasis on responsive design and advanced layout techniques.

(Feel free to replace this with a screenshot of your own project!)

✨ Features
Hero Section: A full-screen hero section with a background image, a semi-transparent overlay for text readability, and a call-to-action sign-up form.

Feature Showcase: Multiple sections that combine text and media (images with overlaid videos) to highlight key features.

FAQ Section: A clickable, accordion-style FAQ section.

Responsive Footer: A multi-column footer that adapts to different screen sizes.

Fully Responsive: The layout seamlessly adjusts from large desktop monitors down to mobile devices.

🛠️ Tech Stack & Concepts
This project was built to practice and demonstrate proficiency in modern front-end layout and styling techniques.

Responsive Design
Responsiveness was a core goal. The site is designed to be mobile-first and scales up to larger screens using several key CSS features:

@media Queries: Media queries are used to apply different styles at specific breakpoints. For example, the footer grid changes from 4 columns on desktop to 2 columns on tablets, and the main feature sections stack vertically on mobile screens to avoid horizontal overflow.

CSS

/* On screens smaller than 1300px */
@media screen and (max-width: 1300px) {
  .footer {
    /* Change from 4 columns to 2 */
    grid-template-columns: 1fr 1fr;
  }
  .first {
    /* Allow items to stack vertically */
    flex-wrap: wrap;
  }
}
Fluid Units (vw, %): Viewport-width (vw) and percentage (%) units are used for containers and font sizes, allowing elements to scale smoothly with the size of the browser window. For example, max-width: 80vw; on the navbar prevents it from becoming too wide on large screens.

CSS Flexbox
Flexbox is the primary tool used for one-dimensional layouts (rows or columns).

Navigation Bar: In the <nav>, display: flex and justify-content: space-between are used to push the logo to the far left and the buttons to the far right, creating a perfectly balanced layout.

Content Sections: The feature sections (e.g., "Enjoy on your TV") use display: flex and align-items: center to vertically center the text content next to the image/video content.

CSS Grid
CSS Grid is used for the two-dimensional layout in the <footer>.

Footer Layout: display: grid and grid-template-columns: 1fr 1fr 1fr 1fr create a perfect four-column grid for the footer links, which is much cleaner and more robust than older methods like floats.

Advanced Positioning
The project uses position: relative and position: absolute to create layered effects.

Hero Overlay: The main hero section has a <div> with position: relative. A child <div> with a black background and opacity: 0.4 is given position: absolute. This lifts it out of the normal flow and places it directly on top of the background image, darkening it so the white text is easy to read.

Video-in-TV Effect: A similar technique is used for the feature sections. The container div (.secImg) is set to position: relative. The <video> element inside it is then set to position: absolute, which allows it to be precisely positioned on top of the TV <img>, creating the illusion that the video is playing on the TV screen.

🚀 How to Run
Clone the repository:

Bash

git clone https://github.com/Kushagra651/Netflix_Clone.git
Navigate to the project directory:

Bash

cd Netflix_Clone
Open the index.html file in your favorite web browser.
