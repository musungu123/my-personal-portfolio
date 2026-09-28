Joyce | Personal Portfolio

A responsive one-page portfolio website for Joyce, a beginner web developer. It is built with HTML, CSS and Tailwind CSS (via CDN), with no JavaScript framework and no build step. Open index.html in a browser and it works.

The site introduces Joyce, explains her background and skills, showcases three projects with live and source links, and gives visitors a way to get in touch.

Features
Sticky navigation bar with smooth scrolling to each section
Hero section with headline, intro, two calls to action and a portrait
About section with bio, skills and experience
Projects section with three project cards and live/source links
Contact section with email, social links and a contact form
Fully responsive layout for phones, tablets, laptops and large desktops
Accessibility features: skip link, semantic landmarks, labelled form fields, keyboard focus outlines, reduced-motion support
Animated highlight under the hero headline (disabled automatically for users who prefer reduced motion)
SEO basics: page title and meta description
Tech stack

Technology	Purpose
HTML5	Page structure and content (semantic elements)
CSS3 (style.css)	Fonts, colour variables, focus styles, hero animation
Tailwind CSS (CDN)	Layout, spacing, colours and responsive design through utility classes
Google Fonts	Bricolage Grotesque (headings) and DM Sans (body text)
Project structure
joyce-portfolio/
├── index.html    # All page content, structure and Tailwind classes
├── style.css     # Custom CSS that complements Tailwind
├── images/       # (optional) put your own photo here, e.g. joyce.jpg
└── README.md     # This file

style.css is linked with a relative path (href="style.css"). Do not write /style.css with a leading slash, because it breaks on GitHub Pages project sites (see Troubleshooting).

Page sections explained
Navigation (<header>)

A sticky bar containing the name "Joyce" and links to About, Projects and Contact. It stays at the top while scrolling and uses a translucent, blurred background. The nav wraps onto a second line on very narrow screens instead of overflowing.

Hero (#home)
A greeting, the main <h1> headline and a short introduction
Two buttons: View my projects (filled) and Contact me (outlined)
A circular portrait. On phones it appears above the text; from tablet width up it sits to the right.
About (#about)

A dark section split into two columns on larger screens:

Left: two short paragraphs about Joyce
Right: skill "pills" (HTML5, CSS3, Tailwind CSS, JavaScript, Responsive design, Git & GitHub) and an Experience list built with a description list (<dl>, <dt>, <dd>)
Projects (#projects)
Project	Description	Tech
Pictures (Captured Forever)	A photography showcase inspired by Aaron Siskind, with a responsive structure and clear typographic hierarchy	HTML, CSS
African Kismat Expeditions	A fully responsive travel and tourism site for luxury East African safaris	HTML, CSS, JavaScript
Akan Name Generator	Calculates a person's day of birth and assigns the matching Akan name from Ghanaian naming traditions	HTML, CSS, JavaScript

Each card has a Live site link and a Source code link. Cards are equal height, so the links line up along the bottom of every card.

Contact (#contact)
An invitation message, an email link and GitHub/LinkedIn links
A form with name, email and message fields, all required and all with labels
Footer

A dark strip with a copyright line. It sits outside <main>, as it should.

Responsive design

Tailwind is mobile-first: classes without a prefix apply to every screen size, and prefixed classes (sm:, md:, lg:, xl:) apply from that width upward.

Screen	Width	What changes
Phone	under 640px	Single column, portrait above text, full-width buttons, compact nav
Tablet	640px and up (sm:)	Projects in 2 columns (third card spans the full row), larger text and spacing
Laptop	768px and up (md:)	Hero, About and Contact become two columns
Desktop	1024px and up (lg:)	Projects in 3 columns, wider gaps, larger headline and portrait
Large desktop	1280px and up (xl:)	Content container widens from 64rem to 72rem

Extra safeguards: images never exceed their container, the page never scrolls sideways, and the email address wraps if it is too long for the screen.

To test, resize your browser slowly, or press F12 and use the device toolbar.

Accessibility
Skip link: press Tab on page load to reveal "Skip to content"
Semantic HTML: <header>, <nav>, <main>, <section>, <article>, <footer>
One <h1>, with headings in a logical order
Form labels linked to inputs with matching for and id, plus autocomplete attributes
Focus outlines on links, buttons and form fields for keyboard users
Alt text on the portrait; decorative project thumbnails are hidden from screen readers with aria-hidden="true"
Reduced motion: the hero animation and smooth scrolling switch off for users who request it