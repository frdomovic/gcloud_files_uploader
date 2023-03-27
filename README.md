This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `pages/index.tsx`. The page auto-updates as you edit the file.

[API routes](https://nextjs.org/docs/api-routes/introduction) can be accessed on [http://localhost:3000/api/hello](http://localhost:3000/api/hello). This endpoint can be edited in `pages/api/hello.ts`.

The `pages/api` directory is mapped to `/api/*`. Files in this directory are treated as [API routes](https://nextjs.org/docs/api-routes/introduction) instead of React pages.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Setting up NextJS with GCP Storage
Download the [Google Cloud SDK](https://cloud.google.com/sdk/docs/install) so you can use the `gcloud` CLI.
Run `gcloud auth login`.
Run `gcloud config set project nextjs-storage-bucket`.
Run `gcloud auth application-default login`
View your newly created bucket and add the bucket name to `.env.local` (see `.env.example`).
Create a new [service account](https://console.cloud.google.com/iam-admin/serviceaccounts) with a role of `Storage Object Creator`.
Click "Create Key" and save the JSON file.
Add the `project_id`, `client_email`, and `private_key` to `.env.local` (see `.env.example`).
Run `yarn dev` to start the Next app at `localhost:3000`.
Choose a `.json` or `.wasm` file.
You should see your file successfully uploaded to the bucket.