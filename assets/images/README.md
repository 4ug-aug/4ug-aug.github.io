# Images Directory

This directory contains all the images for your Jekyll site. Here's how to organize them:

## Directory Structure

```
assets/images/
├── projects/           # Project-related images
│   ├── project-name-thumb.jpg     # Thumbnail (400x300px recommended)
│   ├── project-name-hero.jpg      # Hero image (1200x600px recommended)
│   ├── project-name-1.jpg         # Screenshots
│   └── project-name-2.jpg
├── blog/              # Blog post images
│   ├── post-title-featured.jpg
│   └── post-title-inline.jpg
├── avatars/           # Profile pictures
│   └── avatar.jpg
└── site/              # Site-wide images
    ├── logo.png
    └── favicon.ico
```

## Image Guidelines

### Project Images

**Thumbnails** (`thumbnail` in front matter):
- **Size**: 400x300px (4:3 aspect ratio)
- **Format**: JPG or PNG
- **Purpose**: Shows in project cards on homepage and projects page
- **Optimization**: Compress for web (keep under 100KB)

**Hero Images** (`hero_image` in front matter):
- **Size**: 1200x600px (2:1 aspect ratio)
- **Format**: JPG
- **Purpose**: Large header image on individual project pages
- **Optimization**: Compress for web (keep under 300KB)

**Screenshots** (`screenshots` array in front matter):
- **Size**: Any reasonable size (maintain aspect ratio)
- **Format**: JPG or PNG
- **Purpose**: Gallery showing project features
- **Optimization**: Compress for web

### Blog Images

**Featured Images**:
- **Size**: 800x400px (2:1 aspect ratio)
- **Format**: JPG
- **Purpose**: Header image for blog posts
- **Usage**: Add `image: "/assets/images/blog/post-name.jpg"` to post front matter

### Avatar

**Profile Picture**:
- **Size**: 200x200px (square)
- **Format**: JPG or PNG
- **Purpose**: Author profile in sidebar and about page
- **Usage**: Update path in `_config.yml` under `author.avatar`

## Adding Images to Projects

1. **Add image files** to the appropriate subdirectory
2. **Update project front matter**:

```yaml
---
title: "My Project"
thumbnail: "/assets/images/projects/my-project-thumb.jpg"
hero_image: "/assets/images/projects/my-project-hero.jpg"
screenshots:
  - "/assets/images/projects/my-project-1.jpg"
  - "/assets/images/projects/my-project-2.jpg"
thumbnail_alt: "Screenshot of the main interface"
hero_alt: "Project overview showing key features"
---
```

## Image Optimization Tips

1. **Compress images** before uploading (use tools like TinyPNG)
2. **Use appropriate formats**:
   - JPG for photos and complex images
   - PNG for simple graphics and transparency
   - WebP for modern browsers (if supported)
3. **Optimize for different screen sizes**
4. **Add alt text** for accessibility
5. **Keep file sizes reasonable** for fast loading

## Responsive Images

The site automatically handles responsive images. Your images will:
- Scale appropriately on mobile devices
- Maintain aspect ratios
- Load efficiently with lazy loading
- Support dark mode where applicable

## Tools for Image Processing

- **Online**: TinyPNG, Squoosh.app, Canva
- **Desktop**: GIMP, Photoshop, Sketch
- **Command line**: ImageMagick, sharp
- **Batch processing**: Consider automating with scripts

Remember to commit and push your images to your repository for them to appear on your live site! 