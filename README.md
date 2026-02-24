# docsify-note-template
KaTeX & mhchem support, reading progress bar, theme toggle... All in Docsify!

Perfect for those wanting to create their site for sharing notes(exp Chemistry!)

TIP: If you are running this on Cloudflare Pages, the code below is recommended to add as `_worker.js` in the root folder

```javascript
export default {
  async fetch(request, env) {
    const url = new URL(request.url);
    if (url.hostname.endsWith('.pages.dev')) {
      return Response.redirect(`https://yourdomain.com${url.pathname}${url.search}`, 301);
      // return new Response("Access Denied", { status: 403 });
    }
    return env.ASSETS.fetch(request);
  },
}; //for cloudflare deployment
```



