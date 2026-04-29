# SI-HMI Pekanbaru Frontend PRD & API Integration

## Overview
A public-facing React frontend for SI-HMI Pekanbaru built with Vite, TypeScript, Tailwind CSS, and TanStack Query.

## Design System: "The Intellectual Editorial"
- **Typography:** Newsreader (Headings), Inter (Body).
- **Colors:** Deep Green (#00450d), Forest Green (#1b5e20), Gold accents, Neutral Surfaces.
- **Philosophy:** High-end editorial, Golden Ratio layouts, expansive whitespace, glassmorphism.

## API Integration Strategy
- Base URL: `http://127.0.0.1:8000`
- Client: Axios/Fetch wrapper in `src/lib/api.ts`.
- State Management: TanStack Query for caching and server state.
- Forms: React Hook Form + Zod.

## Page Roadmap
1. **Home:** `/api/v1/home/` - Multi-section hero, news, events summary.
2. **Organization:** Profile, Management, and Chairman History.
3. **Programs & Events:** List and slug-based detail views.
4. **News & Gallery:** Categorized lists and detail pages.
5. **Registration:** Directory of forms (linking to Google Forms).
6. **Interaction:** Contact form and News Upload Request with tracking.

## Static Screen Coverage

| Static Screen | Backend API Contract | Status |
| --- | --- | --- |
| `home_page/code.html` | `GET /api/v1/home/` | Available |
| `organization_profile/code.html` | `GET /api/v1/organization/profile/` | Available |
| `branch_management/code.html` | `GET /api/v1/organization/management/` | Available |
| `chairman_history/code.html` | `GET /api/v1/organization/chairmen/` | Available |
| `programs_directory/code.html` | `GET /api/v1/programs/` | Available |
| `program_detail/code.html` | `GET /api/v1/programs/:slug/` | Added |
| `events_directory/code.html` | `GET /api/v1/events/` | Available |
| `event_detail/code.html` | `GET /api/v1/events/:slug/` | Added |
| `news_archive/code.html` | `GET /api/v1/news/`, `GET /api/v1/news/categories/` | Available |
| `news_article_detail/code.html` | `GET /api/v1/news/:slug/` | Available |
| `gallery_page/code.html` | `GET /api/v1/gallery/`, `GET /api/v1/gallery/categories/` | Added |
| `registration_forms_directory/code.html` | `GET /api/v1/registration-forms/` | Available |
| `contact_page/code.html` | `POST /api/v1/contact-messages/` | Added |
| `news_upload_request/code.html` | `POST /api/v1/news-requests/`, `POST /api/v1/news-requests/:id/payment/` | Available |
| `track_news_request/code.html` | `GET /api/v1/news-requests/track/:tracking_code/` | Added |

## API Field Mapping Notes

- Navigation must map from `home.navigation`: `title`, `url`, `location`, `sort_order`.
- Program detail must map: `title`, `slug`, `category`, `description`, `content`, `image`, `icon`, `button_text`, `button_link`, `registration_form_url`.
- Event detail must map: `title`, `slug`, `description`, `content`, `image`, `location`, `start_date`, `end_date`, `start_time`, `end_time`, `registration_form_url`.
- News archive filters must map from `news/categories`: `id`, `name`, `slug`, `description`.
- Gallery filters must map from `gallery/categories`: `id`, `name`, `slug`, `description`.
- Registration buttons must use `google_form_url`, never `href="#"` in final React implementation.
- News request success must show backend `tracking_code` UUID, not a handcrafted code.

## Static Navigation Status

All static `code.html` screens are linked with relative HTML paths for prototype navigation. There are no remaining `href="#"` placeholders. External Google Form buttons use a temporary `https://forms.google.com` placeholder and must be replaced with backend `google_form_url` / `registration_form_url` when converted to React.
