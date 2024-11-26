# Growth Business Development México

A modern, multilingual business development platform built with Next.js 13, focusing on expansion strategies and growth intelligence for the Mexican market.

**Last Updated: January 8, 2024 - 19:45 CST**

**Developed by [Develop.creaconstruye.com](https://develop.creaconstruye.com)**

## Features

- 🌐 Multilingual support (Spanish, English, Chinese)
- 🎨 Modern UI with Tailwind CSS and shadcn/ui
- 📱 Fully responsive design
- 💬 AI-powered chat assistant with n8n integration
- 📝 MDX blog system
- 🔄 Dynamic content management
- 🚀 Optimized for GCP deployment

## System Requirements

- Node.js 18.x or higher
- NPM 9.x or higher
- Docker and Docker Compose (for production)
- Google Cloud SDK
- n8n for workflow automation

## Environment Setup

1. Create `.env.local` file:
```bash
NEXT_PUBLIC_API_URL=http://localhost:3000
N8N_WEBHOOK_BASE_URL=http://localhost:5678
GCP_PROJECT_ID=your-project-id
GCP_REGION=your-region
```

2. For production, update `.env.production`:
```bash
NEXT_PUBLIC_API_URL=https://api.growthbdm.com
N8N_WEBHOOK_BASE_URL=https://n8n.growthbdm.com
```

## Development Setup

```bash
# Install dependencies
npm install

# Run development server
npm run dev

# Build for production
npm run build

# Start production server
npm start
```

## Docker Deployment

```bash
# Build Docker image
docker build -t growth-bdm .

# Run container
docker run -p 3000:3000 growth-bdm
```

## GCP Deployment

1. Initialize GCP configuration:
```bash
gcloud init
gcloud config set project your-project-id
```

2. Deploy to Cloud Run:
```bash
gcloud builds submit --tag gcr.io/$PROJECT_ID/growth-bdm
gcloud run deploy growth-bdm --image gcr.io/$PROJECT_ID/growth-bdm --platform managed
```

## n8n Integration

The platform integrates with n8n for workflow automation. Key workflows include:

- Lead management
- Email notifications
- CRM integration
- Document processing
- Analytics tracking

### Setting up n8n

1. Install n8n:
```bash
npm install n8n -g
```

2. Configure n8n environment:
```bash
export N8N_HOST=localhost
export N8N_PORT=5678
export N8N_PROTOCOL=http
```

3. Start n8n:
```bash
n8n start
```

## Project Structure

```
├── app/                    # Next.js 13 app directory
│   ├── [locale]/          # Locale-specific routes
│   ├── api/               # API routes
├── components/            # React components
├── lib/                   # Utility functions
├── messages/             # i18n translation files
├── posts/               # MDX blog posts
├── public/              # Static assets
├── deploy/              # Deployment configurations
│   ├── gcp/            # GCP-specific configs
│   └── n8n/            # n8n workflow templates
└── styles/             # Global styles
```

## Security Considerations

- All API endpoints are protected with rate limiting
- Environment variables are properly managed
- CORS is configured for production
- Security headers are implemented
- Regular security audits are performed

## Monitoring and Logging

- GCP Cloud Monitoring integration
- Error tracking with Sentry
- Performance monitoring with Lighthouse
- Custom logging middleware

## Backup and Recovery

- Automated database backups
- File system snapshots
- Disaster recovery procedures
- Regular testing of recovery processes

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is proprietary software. All rights reserved.

## Support

For technical support:
- Email: tech@growthbdm.com
- Website: https://growthbdm.com
- Phone: +52 (55) 2701 6354

---
Developed with ❤️ by [Develop.creaconstruye.com](https://develop.creaconstruye.com)