# Pagudpud Integrated School Faculty Management System
## PostgreSQL + Cloudinary Production Version

This version is designed for real online use. It does not depend on Render's temporary file storage for your important data.

## What is new

- PostgreSQL database for teacher records, schedules, accounts, reports, and settings
- Cloudinary storage for uploaded teacher profile pictures
- Render-ready Node.js web app
- Professional Home Page
- Embedded public school logo file included in `public/school-logo.png`
- Term settings: 1st Term, 2nd Term, 3rd Term

## Render settings

Build Command:

```bash
npm install
```

Start Command:

```bash
npm start
```

## Required environment variables

Add these in Render > Environment:

```env
NODE_ENV=production
SESSION_SECRET=change-this-to-a-long-random-secret
DATABASE_URL=your-postgresql-connection-string
ADMIN_EMAIL=admin@pis.edu.ph
ADMIN_PASSWORD=ChangeMeAdmin123!
ADMIN_NAME=System Administrator
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
CLOUDINARY_FOLDER=pis-fms-profile-pictures
```

## Database options

You can use any PostgreSQL provider:

- Supabase PostgreSQL
- Neon PostgreSQL
- Railway PostgreSQL
- Render PostgreSQL

Copy the provider's PostgreSQL connection string into `DATABASE_URL`.

## Cloudinary

Create a free Cloudinary account, then copy:

- Cloud name
- API key
- API secret

These values are used for profile picture uploads.

## Local testing

Create `.env` from `.env.example`, then run:

```bash
npm install
npm start
```

Open:

```text
http://localhost:3000
```

## Important

Do not upload `.env` to GitHub. Keep all passwords and API keys inside Render Environment Variables only.
