# Consulting Platform

A comprehensive React-based consulting business platform designed for professional consulting services and strategic business solutions.

## Features

- **Multiple Home Layouts**: 10 different home page variations
- **Complete Business Pages**: About, Services, Team, Projects, Contact
- **Modern Design**: Clean and professional UI/UX
- **React 18**: Built with the latest React features  
- **Bootstrap 5**: Responsive design framework
- **Supabase Integration**: Backend-as-a-Service for data management
- **Animations**: Smooth animations with Animate.css and WOW.js
- **Mobile Responsive**: Optimized for all devices
- **SEO Optimized**: Meta tags and structured data
- **Contact Forms**: Multiple contact form variations
- **Team Management**: Showcase team members and expertise
- **Service Portfolio**: Display consulting services and case studies
- **Blog System**: News and insights section
- **Pricing Tables**: Service pricing and packages

## Quick Start

1. **Clone the repository**
   ```bash
   git clone [repository-url]
   cd consulting-platform
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env
   ```
   Edit `.env` with your Supabase credentials:
   ```
   REACT_APP_SUPABASE_URL=https://your-project.supabase.co
   REACT_APP_SUPABASE_ANON_KEY=your-anon-key
   ```

4. **Start development server**
   ```bash
   npm start
   ```

5. **Build for production**
   ```bash
   npm run build
   ```

## Supabase Setup

1. Create a new project at [supabase.com](https://supabase.com)
2. Get your project URL and anonymous key from Settings > API
3. Update the environment variables in `.env`

### Database Schema Examples

```sql
-- Contact submissions table
CREATE TABLE contacts (
  id BIGSERIAL PRIMARY KEY,
  name TEXT NOT NULL,
  email TEXT NOT NULL,
  subject TEXT,
  message TEXT NOT NULL,
  created_at TIMESTAMP WITH TIME ZONE DEFAULT NOW()
);

-- Service inquiries table
CREATE TABLE inquiries (
  id BIGSERIAL PRIMARY KEY,
  service_type TEXT NOT NULL,
  company_name TEXT,
  contact_person TEXT NOT NULL,
  email TEXT NOT NULL,
  phone TEXT,
  message TEXT,
  created_at TIMESTAMP WITH TIME ZONE DEFAULT NOW()
);

-- Newsletter subscriptions table
CREATE TABLE newsletter (
  id BIGSERIAL PRIMARY KEY,
  email TEXT UNIQUE NOT NULL,
  subscribed_at TIMESTAMP WITH TIME ZONE DEFAULT NOW()
);
```

## Project Structure

```
src/
├── components/          # Reusable UI components
│   ├── about/          # About section components
│   ├── banner/         # Hero banner components
│   ├── blog/           # Blog components
│   ├── footer/         # Footer variants
│   ├── header/         # Header and navigation
│   ├── service/        # Service components
│   └── team/           # Team components
├── home/               # Home page layouts
├── inner/              # Internal pages
├── onepage/            # One-page variants
├── data/               # Static data
└── lib/                # Utility functions and Supabase config
```

## Available Scripts

- `npm start` - Start development server
- `npm run build` - Build for production  
- `npm test` - Run tests
- `npm run eject` - Eject from Create React App

## Home Page Layouts

1. **HomeOne** - Classic consulting layout
2. **HomeTwo** - Corporate business focus
3. **HomeThree** - Modern agency style
4. **HomeFour** - Digital transformation focus
5. **HomeFive** - Strategic consulting
6. **HomeSix** - Creative agency variant
7. **HomeSeven** - Technology consulting
8. **HomeEight** - Professional services
9. **HomeNine** - Business growth focus
10. **HomeTen** - Startup consulting

## Pages Included

- **Multiple Home Layouts** - Various business focuses
- **About Pages** - Company information and values
- **Service Pages** - Consulting service offerings
- **Team Pages** - Team member profiles and expertise
- **Project/Case Studies** - Portfolio and success stories
- **Blog Pages** - Insights and industry news
- **Contact Pages** - Contact forms and information
- **Pricing Pages** - Service packages and pricing

## Customization

### Styling
- CSS files located in `public/assets/css/`
- Component-specific styles in respective component files
- Responsive design with Bootstrap 5

### Content
- Update static data in `src/data/` directory
- Modify component content in their respective files
- Replace images in `public/assets/images/` directory

### Branding
- Replace logo in header components
- Update favicon and manifest in `public/` directory
- Modify site title and description in `public/index.html`

## Dependencies

### Core
- React 18.3.1
- React Router DOM 6.26.1
- Bootstrap 5.3.3

### Supabase & Data
- @supabase/supabase-js
- react-query

### UI Components & Animations
- React Bootstrap 2.10.4
- Animate.css 4.1.1
- WOW.js 1.2.2
- Swiper 11.1.10
- React CountUp 6.5.3

### Utilities
- React Scroll 1.9.0
- React Intersection Observer 9.13.0

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

This project is licensed under the MIT License.

## Support

For support and questions, please contact the development team or create an issue in the repository.
