# Setup Instructions

## Environment Variables Setup

### For Local Development

1. Create a `.env` file in the root directory with the following variables:

```env
# MongoDB Connection
MONGODB_URI=mongodb+srv://project_fpv:4VpCHDwGY01PTfjw@cluster1.amczncu.mongodb.net/projectfpv?retryWrites=true&w=majority&appName=Cluster1

# JWT Secret Key
JWT_SECRET=your-super-secret-jwt-key-change-this-in-production

# Server Port (for localhost only)
PORT=5000

# CORS Origins (comma-separated for multiple origins)
CORS_ORIGIN=http://localhost:3000

# Node Environment
NODE_ENV=development
```

2. Install dependencies:
```bash
npm install
```

3. Run the server:
```bash
npm start
# or for development with auto-reload
npm run dev
```

### For Vercel Deployment

1. Go to your Vercel project settings
2. Navigate to "Environment Variables"
3. Add the following environment variables:
   - `MONGODB_URI` - Your MongoDB connection string
   - `JWT_SECRET` - Your JWT secret key (use a strong random string)
   - `CORS_ORIGIN` - Your frontend URL(s), comma-separated (e.g., `https://yourdomain.com,https://www.yourdomain.com`)
   - `NODE_ENV` - Set to `production`

4. Deploy to Vercel:
```bash
vercel --prod
```

## Important Notes

- The `.env` file is already in `.gitignore` and will not be committed to version control
- Never commit secrets to version control
- For production, use strong, randomly generated secrets
- The server automatically detects if it's running on Vercel and adjusts accordingly
- MongoDB connection is optimized for serverless functions with connection pooling

## Testing

- Health check: `GET /api/health`
- The server works on both localhost and Vercel without code changes

