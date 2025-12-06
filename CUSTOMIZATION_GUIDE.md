# Website Customization Guide

This guide will help you customize your organization's website by replacing placeholder content with your actual information.

## Quick Start

All placeholder text is marked with `[Square Brackets]` throughout the HTML files. Simply search for `[` in each file and replace the bracketed text with your actual content.

## Files to Customize

### 1. index.html (Home Page)
- **Hero Section**: Replace organization name, tagline, and call-to-action button text
- **Mission Statement**: Add your organization's mission or key message
- **Features**: Update the 3 feature cards with your offerings (networking, development, service, etc.)
  - Change icons by visiting https://icons.getbootstrap.com and replacing the icon class names
  - Copy/paste feature card divs to add more features
- **Statistics**: Replace `[###]` with your actual numbers and labels
- **Events**: Add your upcoming events with titles, descriptions, and dates
- **Footer**: Update organization name, description, contact info, and social media links

### 2. about.html (About Page)
- **Page Header**: Update page title and subtitle
- **Who We Are**: Tell your organization's story (3 paragraphs recommended)
- **Testimonial**: Add a quote from a member or alumni
- **Mission, Vision, Values**: Define your organization's foundation
- **History Timeline**: Add key milestones in your organization's history
  - Copy/paste card divs to add more timeline entries
- **Core Values**: List and describe your organization's values
  - Copy/paste value divs to add more items

### 3. executive-board.html (Leadership Page)
- **Team Members**: Add your leadership team
  - Replace `[Name]`, `[Position/Role]`, and description for each member
  - To add photos: Replace `<i class="bi bi-person-fill"></i>` with:
    ```html
    <img src="path/to/photo.jpg" alt="Member Name" style="width:100%; height:100%; object-fit:cover;">
    ```
  - Copy/paste the team member card div to add more members
  - Use `col-lg-3` for 4 members per row, `col-lg-4` for 3 members per row
- **Social Links**: Update LinkedIn, email, and other social media links
- **Optional Sections**: Delete sections marked as "optional" if not needed

### 4. membership.html (Membership Page)
- **Benefits**: List membership benefits and what members gain
- **Pricing/Tiers**: Update membership types and pricing
- **Membership Form**: Customize form fields as needed
- **FAQ**: Add frequently asked questions about membership

### 5. resources.html (Resources Page)
- **Resource Categories**: Update resource links and categories
- **Events**: Add upcoming workshops, sessions, and events
- **Past Events**: Add recordings or materials from past events

### 6. contact.html (Contact Page)
- **Contact Information**: Update email, location, and office hours
- **Contact Form**: Customize form fields and subjects
- **Social Media**: Update social media links
- **FAQ**: Add frequently asked questions

## Common Customization Tasks

### Changing Colors
Edit `css/style.css` and update the CSS variables at the top:
```css
:root {
    --primary-color: #2563eb;    /* Main brand color */
    --primary-dark: #1d4ed8;     /* Darker shade */
    --primary-light: #3b82f6;    /* Lighter shade */
}
```

### Changing Icons
1. Visit https://icons.getbootstrap.com
2. Find the icon you want
3. Replace the icon class name, e.g., change `bi-people-fill` to `bi-star-fill`

### Adding/Removing Sections
- To add: Copy an existing section and paste it where you want
- To remove: Delete the entire `<section>...</section>` block
- Sections marked with "Instructions: This section is optional" can be safely deleted

### Adding Images
Store images in an `images/` folder and reference them:
```html
<img src="images/your-image.jpg" alt="Description">
```

### Updating Navigation
The same navigation menu appears on all pages. Update it in one file, then copy it to all other files to keep them consistent.

### Updating Footer
The footer appears on all pages. Like the navigation, update it in one file and copy to all other files.

## Social Media Links
Replace `#` in social media links with your actual URLs:
- LinkedIn: `https://linkedin.com/company/your-org`
- Instagram: `https://instagram.com/your-org`
- Twitter/X: `https://twitter.com/your-org`
- Facebook: `https://facebook.com/your-org`

## Forms
The contact and membership forms are HTML-only. To make them functional, you'll need to:
1. Set up a form processing service (e.g., Formspree, Google Forms, or your own backend)
2. Update the `<form>` tag's `action` attribute with the processing URL
3. Add `method="POST"` to the form tag

Example:
```html
<form action="https://formspree.io/f/your-form-id" method="POST">
```

## Testing Your Changes
1. Open each HTML file in a web browser
2. Check that all text has been replaced (no `[brackets]` remaining)
3. Verify all links work
4. Test on mobile devices (or use browser dev tools to simulate)
5. Check that images load correctly

## Tips
- Make small changes and preview frequently
- Keep backups of your files
- Use "Find and Replace" in your text editor to update repeated content (like organization name)
- Maintain consistent styling across pages
- Remove sections you don't need rather than leaving them with placeholder text

## Need Help?
- HTML basics: https://www.w3schools.com/html/
- Bootstrap documentation: https://getbootstrap.com/docs/5.3/
- Bootstrap Icons: https://icons.getbootstrap.com/

## Page-Specific Notes

### index.html
- This is your landing page - make it engaging!
- Consider adding high-quality images to the hero section background
- Keep the statistics accurate and update them regularly
- Feature your most important/upcoming events

### about.html  
- Tell a compelling story about your organization
- Use the testimonial section to add credibility
- Keep the history timeline concise but meaningful

### executive-board.html
- Add professional photos of team members if possible
- Keep role descriptions brief and clear
- Update this page each time leadership changes

### membership.html
- Clearly communicate the value of membership
- Make the sign-up process as simple as possible
- Address common concerns in the FAQ section

### resources.html
- Organize resources into clear categories
- Keep links up to date
- Add new resources regularly to keep content fresh

### contact.html
- Make it easy for people to reach you
- Respond to inquiries promptly
- Consider adding a map if you have a physical location
