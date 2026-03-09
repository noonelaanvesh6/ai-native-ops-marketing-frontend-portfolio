# Anvesh Portfolio — React v3

## Quick Start
```bash
npm install
npm run dev
```
Open http://localhost:5173

## Stack
- **React 18** + **Vite 5** + **React Router v6**
- **GSAP 3.12** — all animations, scroll reveals, magnetic buttons
- **Three.js** — WebGL particle wave hero background
- **Bootstrap 5** — responsive grid only

## Folder Structure
```
src/
├── components/
│   ├── Cursor.jsx      ← custom cursor + trail
│   ├── Layout.jsx      ← nav + footer
│   └── WebGLHero.jsx   ← Three.js particle grid
├── data/
│   └── content.js      ← ALL copy, blog posts, projects
├── pages/
│   ├── Home.jsx
│   ├── About.jsx
│   ├── Work.jsx
│   ├── Blog.jsx
│   ├── BlogPost.jsx
│   └── Contact.jsx
├── App.jsx             ← routes + page transitions
├── main.jsx
└── index.css           ← design system (tokens, components)
```

## Personalise Checklist
1. **content.js** — update PROFILE email/linkedin/phone, add real project descriptions
2. **public/** — add `Anvesh_Resume.pdf`, `your-photo.jpg`, project screenshots
3. Replace all `img-ph` placeholder divs with real `<img>` tags
4. **Contact.jsx** line ~70 — add your Calendly link
5. **Layout.jsx** — add your real GitHub URL in footer
6. **index.html** — add favicon.svg in /public

## Adding a New Blog Post
In `src/data/content.js`, add an object to `BLOG_POSTS`:
```js
{
  slug: 'my-new-post',
  emoji: '🚀',
  thumbBg: 'linear-gradient(135deg, #fff3e0, #ffe0b2)',
  tags: [{ text: 'SEO', cls: 'bt-seo' }],
  date: 'Mar 2025',
  readTime: '5 min read',
  title: 'My Post Title',
  excerpt: 'Short description shown on cards.',
  content: `<p>Full HTML content here...</p>`,
}
```

## Unicorn Studio WebGL
To add Unicorn Studio scenes:
1. Create a scene at app.unicorn.studio
2. Replace the WebGLHero component with their embed:
```jsx
<div data-us-project="your-scene-id" style={{position:'absolute',inset:0}} />
```
Add their script to index.html:
```html
<script src="https://cdn.unicorn.studio/v1.4/unicornStudio.umd.js"></script>
```

## Deploy to Vercel (free)
```bash
npm run build
npx vercel --prod
```
