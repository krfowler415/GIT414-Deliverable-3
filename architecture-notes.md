GIT 414 - Deliverable 3 - CSS Architecture Notes Project: Desert After Dark

This builds on the CSS architecture I created for Deliverable 2. I kept the same basic homepage preview and expanded the responsive layouts using the techniques covered in Module 3. The goal is to make the existing components adjust better to different screen sizes before adding the final animal content, photographs, and remaining pages.

Organization:
I kept everything in one stylesheet and maintained the same cascade layers built from Deliverable 2 (reset, base, layout, components, utilities, states, overrides, and print). I also added the new responsive rules to those existing sections instead of reorganizing or replacing the stylesheet.

Colors and other values:
I kept my original Desert After Dark color palette. Prickly Pear Pink is now used for hover effects on the navigation, site title, and animal cards. Ocotillo Orange is still used for buttons, Palo Verde Green for the Fun Fact component, and Desert Sand for links and keyboard focus outlines. I also made the animal category tags smaller and changed them to a neutral color.

I updated the typography to use Figtree for headings and Outfit for body text and navigation, with fallback fonts included. I also used clamp() to make some text sizes and spacing more flexible.

Components and interactions:
The main container uses logical properties to control its width and spacing. The Featured Animals section uses CSS Grid with minmax(), repeat(), and auto-fit to adjust the cards based on the available space. The cards display with images above the text on wider screens, two horizontal image-and-text cards on medium screens, and three horizontal cards stacked vertically on narrow screens.

I also added a responsive navigation hamburger menu for narrow screens. The full navigation is visible on larger screens, while the mobile menu slides in from the right. The site title now works as the Home link.

The Fun Fact component uses a container query to change from a stacked layout to two columns when its container reaches 34rem. The default layout remains readable without container-query support. I didn't use subgrid because the current components don't need their internal rows aligned across separate cards.

What I changed from Deliverable 2:
Most changes involved improving the existing responsive layouts, spacing, typography, navigation, and alignment.

The breakpoints are based on where the navigation and animal cards need additional room, rather than targeting specific devices. I also added preference queries for reduced motion and increased contrast.

The page still uses placeholder animal information and photographs. The hero section will also receive more visual attention later, once I've decided how I want to incorporate wildlife imagery or other graphics.

Testing: 
The preview was checked in Chromium and Firefox using responsive mode at different widths. There was no horizontal scrolling in those checks, and the animal card layouts adjusted as intended.

I also tested the page at 200% browser zoom and confirmed that the content remained usable. Keyboard focus, mobile navigation, current-page behavior, reduced-motion and increased-contrast preferences, and the container-query fallback were also checked during development.

The print-media CSS rules were reviewed, but I still need to check the actual browser Print Preview. The animal content, photographs, and remaining pages will come later.
