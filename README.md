# Social Echo Client

A React-based social media application.

## Environment Variables

This application uses environment variables for configuration. Create the following files:

### Development (.env.local)
```bash
REACT_APP_API_URL=http://127.0.0.1:4000
```

### Production (.env.production)
```bash
REACT_APP_API_URL=https://your-production-api-url.com
```

## Local Development

1. Install dependencies:
```bash
npm install
```

2. Create environment file:
```bash
cp .env.example .env.local
```

3. Update `.env.local` with your local API URL

4. Start development server:
```bash
npm start
```

## Netlify Deployment

### Option 1: Environment Variables in Netlify Dashboard

1. Go to your Netlify site dashboard
2. Navigate to **Site settings** → **Environment variables**
3. Add the following variables:
   - `REACT_APP_API_URL` = `https://your-production-api-url.com`

### Option 2: Using netlify.toml (Recommended)

1. Update the `netlify.toml` file with your actual API URLs
2. Commit and push to trigger a new deployment

### Option 3: Build-time Environment Variables

You can also set environment variables during build:

```bash
REACT_APP_API_URL=https://your-api-url.com npm run build
```

## Important Notes

- Environment variables must start with `REACT_APP_` to be accessible in React
- The `.env.local` file is gitignored and should contain your local development settings
- The `.env.production` file can be committed to git for team reference
- Always use HTTPS URLs for production API endpoints

## Troubleshooting

If environment variables are not working in Netlify:

1. Check that variables start with `REACT_APP_`
2. Verify variables are set in Netlify dashboard
3. Clear Netlify cache and redeploy
4. Check build logs for any errors
