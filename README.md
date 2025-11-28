# Live Hindustan Clone -- AST Assignment


------------------------------------------------------------------------

## 📝 Project Overview

This project is a simplified **front-page clone of the LiveHindustan
news portal**, built using **Next.js**. The objective was to demonstrate
key Next.js concepts such as **Dynamic Routing**, **Incremental Static
Regeneration (ISR)**, and **Image Optimization**, implemented in a
realistic news portal layout.

The UI is designed to be clean, functional, and fully responsive across
mobile and desktop devices while ensuring efficient data fetching and
smooth performance.

------------------------------------------------------------------------

## 🚀 Key Features

### 🔥 Hero Section

A visually appealing hero banner highlighting the top story with a
gradient overlay, similar to the LiveHindustan homepage.

### 📱 Responsive Grid Layout

-   3-column layout on desktop\
-   Stacked vertical layout on mobile\
-   Uniform and intuitive browsing experience

### 📰 Dynamic News Pages

Each news item routes to a dynamic page at `/news/[id]`, where the full
details of the article are displayed.

### 📊 Trending Sidebar

A right-aligned static sidebar that enhances the overall structure and
gives the feel of a real news portal.

### 🛡 Robust Error Handling

Handled cases such as missing data, broken image URLs, and unexpected
errors to prevent UI crashes.

------------------------------------------------------------------------

## 🛠️ Tech Stack & Implementation Choices

### 1. Next.js -- Pages Router

Used the **Pages Router** because the assignment required the use of
`getStaticProps`, which aligns naturally with this routing method.

### 2. ISR (Incremental Static Regeneration)

Configured ISR using:

``` js
revalidate: 60
```

**Why ISR?**

-   Ensures the website remains fast with static HTML\
-   Keeps content fresh by regenerating pages every 60 seconds\
-   Ideal balance between SSR and SSG for a news website

### 3. Tailwind CSS

Tailwind enabled rapid UI development with utility-first classes and
made responsive design extremely efficient.

### 4. Local Mock Data

Instead of using a real API, I used mock data stored in:

`/src/data/mockNews.js`

**Reason:**

-   Avoids API rate limits\
-   No dependency on API keys\
-   Allows easy testing of edge cases (long headlines, missing
    summaries, etc.)

------------------------------------------------------------------------

## 🐛 Challenges & Learnings

### 🔧 1. Folder Structure Mistake

Initially, the Next.js app was accidentally created inside another
folder, causing import path errors and module issues. Fixed by
reorganizing the directories properly under `/src`.

### 🖼 2. Image Optimization Restrictions

Next.js blocked external image URLs until I manually allowed the domain
in:

``` js
images: {
  domains: ['images.unsplash.com'],
}
```

This helped me understand the strict but useful nature of Next.js image
security.

------------------------------------------------------------------------

## 🤖 AI Usage & Reflection (Part D)

### ✔ Helpful AI Contributions

-   Generated the mock dataset quickly\
-   Suggested Tailwind class patterns like\
    `grid grid-cols-1 md:grid-cols-3 gap-4`

### ❌ Where Manual Intervention Was Necessary

-   AI suggested an incorrect folder structure → fixed manually\
-   AI-provided placeholder images were broken → replaced with working
    Unsplash URLs

This showed that AI is useful for speed but still needs human oversight.

------------------------------------------------------------------------

## ▶️ How to Run Locally

1.  Clone the repository\
2.  Install dependencies:

``` bash
npm install
```

3.  Start the development server:

``` bash
npm run dev
```

4.  Open the app in your browser:

```{=html}
<!-- -->
```
    http://localhost:3000

------------------------------------------------------------------------

## 📌 Conclusion

This project helped reinforce core Next.js concepts in a practical way
while also improving my responsive UI design skills using Tailwind. The
combination of ISR, dynamic routing, and error handling made the
application feel both real and performant.

------------------------------------------------------------------------
