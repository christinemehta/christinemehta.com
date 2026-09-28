# christinemehta.com

A static site: five HTML pages, one stylesheet, one photo. No build step, no plugins, nothing to update except the words.

    index.html      About (home)
    writing.html    Writing, grouped by theme
    edited.html     Pieces Christine edited
    research.html   The human-rights research years
    contact.html    Contact
    assets/style.css
    assets/portrait.jpg
    CNAME           tells GitHub Pages the custom domain
    404.html, robots.txt, sitemap.xml, .nojekyll

## Publishing on GitHub Pages (free)

1. Create a free account at github.com if you don't have one.
2. Create a new repository named exactly `christinemehta.com` (public, empty — no README).
3. Upload every file in this folder to the repository, keeping the `assets` folder.
   The easiest way is the "Add file → Upload files" button on the empty repo page:
   drag the whole folder's contents in and click "Commit changes".
4. In the repository, open Settings → Pages. Under "Build and deployment", set
   Source to "Deploy from a branch", Branch to `main`, folder `/ (root)`, and Save.
5. On the same Pages screen, under "Custom domain", enter `www.christinemehta.com`
   and Save. (The CNAME file does the same thing; entering it here confirms it.)
   Tick "Enforce HTTPS" once it becomes available — usually within an hour of DNS resolving.

## Pointing the domain at GitHub

At the registrar where christinemehta.com is registered (the DNS settings page), add:

    Type   Host   Value
    CNAME  www    <your-github-username>.github.io.
    A      @      185.199.108.153
    A      @      185.199.109.153
    A      @      185.199.110.153
    A      @      185.199.111.153

Delete any old Squarespace records for `@` and `www` first (they'll usually point at
squarespace.com or ext-cust.squarespace.com). DNS changes take anywhere from a few
minutes to a day to propagate. The four A records make the bare domain
(christinemehta.com) redirect to www.

## Making changes later

Edit the HTML file, upload the new version to the repo (or tell Claude what to change),
and the site updates in about a minute. To swap the portrait, replace assets/portrait.jpg
with any 4:5 image.
