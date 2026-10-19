# Meetra website

Static website for Meetra Technologies Ltd. The homepage explains the Meetra mobility service, the passenger journey, and FAQs. Passenger waitlist signups are collected by Google Forms and stored in the linked Google Sheet.

## Files

- `index.html` — homepage
- `rider-signup.html` — branded page embedding the passenger waitlist form, with a direct-form fallback link
- `assets/meetra-logo.png` — official Meetra logo
- `vercel.json` — clean URLs and the `/rider-signup` route

## Waitlist form and responses

- Public form: https://docs.google.com/forms/d/e/1FAIpQLSdlMzTA7BjKblUUwGGikQUoASXECiY_954YcgibzhQx1yXlVQ/viewform
- Response Sheet: https://docs.google.com/spreadsheets/d/1MhLOLcjvpFOfw5SVWVSsFm3dWmvMggQObU7Q_YZTIUY/edit?gid=2004111001#gid=2004111001

The form is published to anyone with its responder link. Form responses are stored in the linked Sheet. Manage the form and Sheet access from the Meetra Google account. The site does not need a database, API key, or environment variables for waitlist collection.

## Deploy to Vercel

1. Put the contents of this folder at the root of a Git repository and push it to the Git provider you use with Vercel.
2. In Vercel, create a project and import that repository.
3. Set the project root to this folder if it is inside a larger repository.
4. Select **Other** as the framework preset. Leave the build and install commands empty; set the output directory to `.`.
5. Deploy. Vercel serves the HTML and image files directly; no build step is required.
6. If using a custom domain, add it in the Vercel project settings and apply the DNS records Vercel provides.

The included `vercel.json` enables clean URLs, so `/rider-signup` routes to the waitlist page. The website links to the public Google Form from that page.

## Before announcing the site

- Open the deployed homepage and check the mobile layout and all navigation and CTA links.
- Submit one clearly marked internal test response to confirm the form and linked Sheet work end to end, then delete that test response if it should not remain in the waitlist. Do not use real commuter data for testing.
- Confirm the Meetra team members who need to process signups can access the response Sheet.
- Add the final privacy notice and terms links when those documents are ready.

Google Forms, the response Sheet, and the hosting project are separate services. Changes to the local website files are not live until the project is deployed again.
