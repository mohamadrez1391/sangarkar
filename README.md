# Sangarkar E-Commerce Platform

A complete e-commerce platform for Sangarkar (سنگرکار) - heating and cooling equipment company with 47+ years of experience.

## Features

- **Full-featured E-commerce**: Products, categories, cart, checkout, orders
- **User Authentication**: JWT-based auth with registration, login, profile management
- **RTL Support**: Complete Persian/Farsi RTL layout
- **Dark Mode**: Toggle between light and dark themes
- **Responsive Design**: Mobile-first approach
- **SEO Optimized**: Meta tags, structured data, semantic HTML
- **Performance**: Code splitting, lazy loading, optimized images

## Tech Stack

### Backend
- Django 5.0
- Django REST Framework
- PostgreSQL 15
- JWT Authentication (SimpleJWT)
- Docker + Gunicorn + Nginx

### Frontend
- React 18
- Vite
- Tailwind CSS 3.4
- shadcn/ui components
- React Router
- Axios

## Project Structure

```
sangarkar-ecommerce/
├── backend/           # Django backend
├── frontend/          # React frontend
├── nginx/             # Nginx configuration
├── docker-compose.yml # Docker compose
└── README.md
```

## Getting Started

### Prerequisites

- Python 3.11+
- Node.js 18+
- PostgreSQL 15
- Docker (optional)

### Backend Setup

```bash
cd backend

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Set up environment variables
cp .env.example .env
# Edit .env with your settings

# Run migrations
python manage.py migrate

# Create superuser
python manage.py createsuperuser

# Run development server
python manage.py runserver
```

### Frontend Setup

```bash
cd frontend

# Install dependencies
npm install

# Run development server
npm run dev
```

### Docker Setup

```bash
# Build and run all services
docker-compose up --build

# Run in background
docker-compose up -d
```

## API Documentation

Access the API documentation at:
- Swagger UI: `http://localhost:8000/api/docs/`
- ReDoc: `http://localhost:8000/api/docs/`

## Default Credentials

- **Admin**: admin / admin123
- **Database**: postgres / postgres

## Environment Variables

### Backend (.env)

```
DJANGO_SECRET_KEY=your-secret-key
DEBUG=True
DB_NAME=sangarkar_db
DB_USER=postgres
DB_PASSWORD=postgres
DB_HOST=localhost
DB_PORT=5432
```

### Frontend (.env)

```
VITE_API_URL=http://localhost:8000
```

## Deployment

### Production

1. Update `.env` files with production values
2. Set `DEBUG=False`
3. Configure proper `SECRET_KEY`
4. Set up SSL certificates
5. Run with Docker Compose

### Vercel/Netlify (Frontend)

```bash
cd frontend
npm run build
# Deploy the `dist` folder
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support, email info@sangarkar.com or call +98 21 53709000.
