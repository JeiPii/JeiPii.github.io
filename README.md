---

## Community Examples

Below are some fantastic examples of websites based on this template. If you wish to add your site to this list, open a pull request!

| Site                                          | Author                                             | Description/Features                                                                         | Source                                                 |
| --------------------------------------------- | -------------------------------------------------- | -------------------------------------------------------------------------------------------- | ------------------------------------------------------ |
| [enscribe.dev](https://enscribe.dev)          | [@jktrn](https://github.com/jktrn)                 | Heavily modified bento-style homepage with client interactivity, with custom MDX components! | [→](https://github.com/jktrn/enscribe.dev)             |
| [emile.sh](https://emile.sh)                  | [@echoghi](https://github.com/echoghi)             | A minimalist personal blog using the [flexoki](https://stephango.com/flexoki) theme          | [→](https://github.com/echoghi/v5)                     |
| [decentparadox.me](https://decentparadox.me)  | [@decentparadox](https://github.com/decentparadox) | A heavily customized personal portfolio with a sci-fi theme!                                 | [→](https://github.com/decentparadox/decentparadox.me) |
| [flocto.github.io](https://flocto.github.io/) | [@flocto](https://github.com/flocto)               | A slightly modified personal blog                                                            | [→](https://github.com/flocto/flocto.github.io)        |
| [dumbprism.me](https://www.dumbprism.me/)     | [@dumbprism](https://github.com/dumbprism)         | A customized portfolio inspired by enscribe's bento grid style adding my gist of UI          | [→](https://github.com/dumbprism/dumbprism-portfolio)  |
| [hyuki.dev](https://hyuki.dev/)               | [@snow0406](https://github.com/snow0406)           | A minimalist blog with a blue color scheme, focusing on simplicity!                          | [→](https://github.com/Snow0406/hyuki.dev)             |
| [ldd.cc](https://ldd.cc/)                     | [@xJoyLu](https://github.com/xjoylu)               | The cream of the idlers.                                                                     | [→](https://ldd.cc/)                                   |
| [rezarezvan.com](https://rezarezvan.com/)     | [@rezaarezvan](https://github.com/rezaarezvan)     | A academic blog with personal touches :).                                                    | [→](https://rezarezvan.com/)                           |
| [blog.z0x.ca](https://blog.z0x.ca/)           | [@z0x](https://z0x.ca)                             | _Very_ minimal version of erudite, stripping it down to the bare essentials                  | [→](https://git.z0x.ca/z0x/blog.z0x.ca/)               |

### Site Configuration

Edit the `src/consts.ts` file to update your site's metadata, navigation links, and social links:

```ts
export const SITE: Site = {
  title: 'astro-erudite',
  description: // ...
  href: 'https://astro-erudite.vercel.app',
  featuredPostCount: 2,
  postsPerPage: 3,
}

export const NAV_LINKS: SocialLink[] = [
  {
    href: '/blog',
    label: 'blog',
  },
  // ...
]

export const SOCIAL_LINKS: SocialLink[] = [
  {
    href: 'https://github.com/jktrn',
    label: 'GitHub',
  },
  // ...
]
```

### Color Palette

Colors are defined in `src/styles/global.css` in [OKLCH format](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value/oklch), using the [shadcn/ui](https://ui.shadcn.com/) convention:

```css
:root {
  --background: oklch(1 0 0);
  --foreground: oklch(0.145 0 0);
  --primary: oklch(0.205 0 0);
  --primary-foreground: oklch(0.985 0 0);
  --secondary: oklch(0.97 0 0);
  --secondary-foreground: oklch(0.205 0 0);
  --muted: oklch(0.97 0 0);
  --muted-foreground: oklch(0.556 0 0);
  --accent: oklch(0.97 0 0);
  --accent-foreground: oklch(0.205 0 0);
  --destructive: oklch(0.577 0.245 27.325);
  --border: oklch(0.922 0 0);
  --ring: oklch(0.708 0 0);
}

[data-theme='dark'] {
  /* ... */
}
```

### Favicons

Favicons are generated using [RealFaviconGenerator](https://realfavicongenerator.net/). To adjust the favicons, replace the files in the `public/` directory (such as `favicon.ico`, `favicon.svg`, `apple-touch-icon.png`, etc.) with your own. After updating the favicon files, you'll also need to adjust the references in `src/components/Favicons.astro` to match your new favicon filenames and paths:

```html
<!-- Replace these with the generated meta tags -->
<link rel="icon" type="image/png" href="/favicon-96x96.png" sizes="96x96" />
<link rel="icon" type="image/svg+xml" href="/favicon.svg" />
<link rel="shortcut icon" href="/favicon.ico" />
<link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png" />
<meta name="apple-mobile-web-app-title" content="astro-erudite" />
<link rel="manifest" href="/site.webmanifest" />
```
