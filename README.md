# Élan Aesthetics Website

A premium, responsive aesthetic clinic website built for **Élan Aesthetics**. The experience combines editorial art direction with clear conversion paths for consultation requests, treatment discovery, and WhatsApp enquiries.

## Project overview

The site is designed as a polished clinic landing page that can also serve as a strong frontend portfolio project. It includes a luxury visual system, responsive navigation, treatment storytelling, a service menu, a before-and-after results gallery, an appointment request modal, an enquiry form, FAQs, and a floating WhatsApp chat action.

> **Content note:** The treatment photography and patient-result cards in this demo are illustrative placeholders. Replace them with approved, consented clinic photography before using the site for a real medical business.

## Features

- Responsive, mobile-first layout for phones, tablets, and desktop screens.
- Custom EA monogram logo and Élan Aesthetics wordmark.
- Sticky navigation with a mobile menu and anchored section navigation.
- Editorial hero section with primary consultation calls to action.
- Treatment overview cards for skin health, facial aesthetics, and hair and scalp care.
- Before-and-after results gallery with filters for specific treatment types: skin rejuvenation, facial balancing, lip enhancement, and signature glow facial.
- Service menu with treatment groupings, starting prices, and consultation links.
- Practitioner profile, clinic philosophy, journal cards, FAQ accordion, and contact section.
- Appointment request modal with date, time, treatment, and message fields.
- Client-side enquiry confirmation state for the contact form.
- Floating WhatsApp chat widget with a pre-filled enquiry message.
- SEO-friendly title, description, Open Graph metadata, semantic headings, and image alt text.

## Technology

- React 19
- TypeScript
- Vite
- Tailwind CSS 4
- Lucide React icons
- Wouter-compatible WebDev scaffold
- pnpm

## Project structure

```text
client/
  index.html
  public/
    images/          # Included in the GitHub/Vercel export
  src/
    components/      # Reusable UI and scaffold components
    contexts/        # Theme context
    pages/
      Home.tsx       # Main Élan Aesthetics page
    App.tsx
    index.css        # Global design tokens and responsive styling
server/
shared/
package.json
README.md
```

## Run locally

Use Node.js 20 or newer and pnpm.

```bash
pnpm install
pnpm dev
```

Vite will start a local development server. Open the local URL shown in the terminal.

## Production build

```bash
pnpm check
pnpm build
```

The production frontend is generated in `dist/public`.

## Deploy to Vercel

1. Create a public GitHub repository and upload the contents of this project.
2. In Vercel, select **Add New Project** and import the GitHub repository.
3. Use the following project settings:

```text
Framework preset: Vite
Build command: pnpm build
Output directory: dist/public
Install command: pnpm install
```

4. Deploy the project.

The repository export includes local image files under `client/public/images`, so the Vercel deployment does not depend on the original WebDev storage paths.

## Deploy to Netlify

Use the same repository with the following settings:

```text
Build command: pnpm build
Publish directory: dist/public
```

## Customization guide

### Brand and contact details

Update the clinic name, phone number, email, address, opening hours, and WhatsApp number in `client/src/pages/Home.tsx`. The current values are sample content for the Élan Aesthetics concept.

### Treatment pricing

Edit the `priceMenu` array near the top of `client/src/pages/Home.tsx`. Each service group contains a title, description, and list of treatment names with starting prices.

### Before-and-after filters

Edit the `resultGallery` array and filter labels in the `before-after` section. The filter buttons match each gallery item's `title`, which makes it straightforward to add or rename treatment-specific filters.

### Images

For the GitHub/Vercel export, replace the files in `client/public/images` and update the `IMG` object in `client/src/pages/Home.tsx` if filenames change. Use only photography that the clinic owns or has permission to publish, especially for patient-result imagery.

### WhatsApp

Replace the placeholder number in the WhatsApp links with the clinic's international-format WhatsApp number. Keep the pre-filled message concise and appropriate for a first enquiry.

### Form handling

The current forms demonstrate the complete client-side experience but do not send data to a backend or email inbox. Connect the submit handlers to a secure form provider, booking system, CRM, or server endpoint before production use. Do not place private API keys in frontend code.

## Accessibility and content considerations

The interface uses semantic headings, labeled form controls, visible button states, responsive touch targets, and alternative text for imagery. Before launch, verify the final copy, consent language, privacy policy, and medical claims with the clinic owner or appropriate professional adviser.

## License

This project is provided as a portfolio and website starter project. Replace the sample imagery, copy, contact information, and legal content before commercial use.

## References

[1]: https://react.dev/ "React documentation"
[2]: https://vite.dev/ "Vite documentation"
[3]: https://tailwindcss.com/docs "Tailwind CSS documentation"
[4]: https://vercel.com/docs "Vercel documentation"
