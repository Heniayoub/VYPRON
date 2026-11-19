VYPRON — Full-stack-ready app (Supabase backend)
Includes:
- Real Supabase email/password authentication
- Hosted PostgreSQL database
- CRUD screens for clients, agents, services, orders, subscriptions
- Row Level Security (RLS): each authenticated user can only access their own rows

SETUP FROM PHONE:
1) Create a Supabase account and a new project (free tier may have limits).
2) In Supabase dashboard, open SQL Editor; paste schema.sql and run.
3) Project Settings -> API: copy Project URL and anon/public key. Never use service_role secret.
4) Open config.js in this package and replace placeholders with your Project URL and anon/public key.
5) Upload all files to a GitHub repository using browser.
6) Create Cloudflare Pages project linked to GitHub. Framework preset None. Build command blank. Output directory root (./).
7) Deploy. Visit the generated pages.dev address.
8) For safer signup settings, configure email confirmation and strong passwords in Supabase Auth.

IMPORTANT:
This is functional software that connects to real authentication and a database after configuration and deployment. It is not deployed for you; credentials, project setup and deployment require your actions. Test it thoroughly before real customer use. No payments are processed; subscriptions are tracked only. A responsible adult should help manage hosting/account ownership and any payments/legal setup.
