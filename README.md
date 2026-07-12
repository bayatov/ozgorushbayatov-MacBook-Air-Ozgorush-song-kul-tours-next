# Song-Kul Tours

Premium booking website built with Next.js 15, TypeScript, Tailwind CSS, Framer Motion, React Hook Form, Zod, Supabase and Stripe-ready route handlers.

## Run locally

1. Copy `.env.example` to `.env.local` and add your Supabase, Stripe and (optional) Resend credentials.
2. Install packages with `npm install`.
3. Start with `npm run dev`.

## Supabase table

Create a `bookings` table containing: `tour_id`, `first_name`, `last_name`, `email`, `phone`, `country`, `date`, `adults`, `children`, `total`, `requests`.

The booking flow stores the request, sends a Resend confirmation when configured, and then redirects to Stripe Checkout. Without service credentials it remains a safe front-end demo and shows a success state.

## Admin panel

Set `ADMIN_PASSWORD` and `ADMIN_SESSION_SECRET` in `.env.local`, then open `/admin`. The dashboard is protected by an HTTP-only signed session cookie. Add a `status` text column to the `bookings` table (default: `new`) to enable status management.
# ozgorushbayatov-MacBook-Air-Ozgorush-song-kul-tours-next
