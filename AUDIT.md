# Automated site review: `www.thehatchgrp.com`

7 pages of `https://www.thehatchgrp.com`, read on 2026-11-10 by Suite Builder's crawler in a real browser, logged out, as a first-time visitor sees them. Nothing was sent, bought or signed in to. This review reads the public site as it is served. It also observes the site's own security guards, as a visitor's browser sees them. It sends nothing and attacks nothing.

## Links that need a look (1)

Each of these links answered an error or did not answer. A person is to look at every one, whatever the site means by it: nothing here is cleared by a rule. A link leaves this list only when the team lists it, with the status it answers, in the suite's expected-links block.

- `https://the-hatch-group-242355921.hubspotpagebuilder.net/privacy-policy?hsLang=en` answered 404; linked from /, /contact-us, /for-consultants, /why-choose-us, /for-clients and 2 more; broken (SITE-33)

**2 major, 6 minor.** Major: lets a visitor or a search engine down now. Minor: worth fixing. Info: said for the record; counts against nothing. Each finding lists every page the read saw it on.

## What this review checked

Of 40 checks, 38 ran on this crawl; 2 could not be confirmed.

<details>
<summary>The checks, by kind</summary>

Pages and links (11 of 11 ran)
- Pages that answer an error yet draw content
- Links that answer an error
- Links that redirect before they arrive
- Page titles that are shared or missing
- An address that cannot exist but answers as a page
- Chains of redirects
- Images that do not load: 60 of the 92 images checked
- Links that send visitors from https to http
- Links to other sites that lead nowhere
- Links that answer an error on purpose
- Links to other sites that did not answer the crawler

Markup, accessibility and search (13 of 13 ran)
- Links and buttons with nothing for a screen reader to say
- Form fields without a label
- Images with no address
- Placeholder text left on pages
- The viewport setting for phones
- Canonical links that point somewhere else
- Images without alt text
- The language each page declares
- The main heading of each page
- Links to a part of the page that is not there
- Descriptions for search results
- The year in the copyright notice
- Form fields whose only label is a placeholder

Loading and speed (5 of 7 ran)
- Scripts, style sheets and data requests that fail to load
- Errors thrown by the site's own scripts
- Pages slow to answer or to load
- Requests over plain http from an https page
- Requests to other sites' hosts that fail: not confirmed
- Pages that did not finish loading: not confirmed
- Other sites' scripts and style sheets that failed for the crawler

The site's own addresses, certificate and headers (9 of 9 ran)
- Addresses of the site that do not answer
- Response headers that browsers act on
- Server software and version announced in headers
- The certificate's end date, name and trust
- Whether the http address sends visitors to https
- The sitemap
- A contact for security reports (security.txt)
- One site answering at two names
- The certificate chain, as the crawler's machine sees it

Not confirmed: the crawl file records what such a check saw only when it saw something, so it cannot show whether the check ran and found nothing, or did not run.

</details>

## major SITE-07 At least 17 links and buttons on 3 pages have nothing for a screen reader to say

**Why it matters.** A blind visitor hears only "link" or "button", with no idea where it goes or what it does; accessibility law \(the ADA, the European Accessibility Act\) counts it, and so do automated accessibility audits.

**Likely fix.** Give each one words: visible text, an aria-label, or an alt on the image inside it \(an icon link to a cart: aria-label="Cart"\).

<details open>
<summary>7 links and buttons</summary>

- `/why-choose-us` \`\<a class="primary-btn"\>\`
- `/for-clients` \`\<a href="\#"\>\`
- `/our-team` \`\<a `` href="https://www.linkedin.com/in/greg-roth-a451548/">` ``
- `/our-team` \`\<a `` href="https://www.linkedin.com/in/erik-jacobs-7b60811/">` ``
- `/our-team` \`\<a `` href="https://www.linkedin.com/in/jpiehowski/">` ``
- `/our-team` \`\<a `` href="https://www.linkedin.com/in/alex-webb-6b39b181/">` ``
- `/our-team` \`\<a `` href="https://www.linkedin.com/in/sam-roth-29755a169/">` ``

</details>

## major SITE-33 1 link to another site leads nowhere: the page is gone

**Why it matters.** Sites move and close: a visitor who follows one of these links meets an error page, or nothing at all, on someone else's site, reached from this one.

**Likely fix.** Point each link at where the page lives now, or take it out. The suite's link report asks every one again on each run, and fails when one that answered stops.

<details open>
<summary>1 link</summary>

- `https://the-hatch-group-242355921.hubspotpagebuilder.net/privacy-policy?hsLang=en` answered 404; linked from /, /contact-us, /for-consultants, /why-choose-us, /for-clients and 2 more

</details>

## minor SITE-15 1 page has no main heading; 1 page has several main headings \(h1\)

**Why it matters.** Screen reader users jump to the h1 to learn what a page is, and search engines read it as the page's subject; none, or several competing, says neither.

**Likely fix.** Give each page one h1 naming what it shows; the site's name in the header is not it.

<details open>
<summary>2 pages</summary>

- `/for-clients` no h1 with words shown
- `/for-clients/enterprise-platforms` 2 h1: \`SALESFORCE\`, \`MEET JUSTIN PIEHOWSKI\`

</details>

## minor SITE-24 2 security headers no page sends

**Why it matters.** Each header closes a door attackers use \(a downgrade to http, a script slipped in, the site framed in another to trick a click\). Security reviews and compliance checklists ask for them, and they cost a line of server configuration.

**Likely fix.** Add the missing headers in the web server or the CDN \(one setting each\), starting with X-Frame-Options or frame-ancestors.

<details open>
<summary>2 missing headers</summary>

- `/` no page of the site sends X-Frame-Options or frame-ancestors \(another site cannot frame it to trick a click\)
- `/` no page of the site sends X-Content-Type-Options: nosniff

</details>

## minor SITE-03 1 of the site's own links redirects before it arrives

**Why it matters.** Every click on one of these links costs an extra round trip before the page starts loading, and search engines see one page at two addresses.

**Likely fix.** Link to each page's final address \(with or without its trailing slash, as the server serves it\).

<details open>
<summary>1 link</summary>

- `/for-clients/enterprise-platforms?hsLang=en` 307 to /for-clients/enterprise-platforms

</details>

## minor SITE-16 1 link on 7 pages points to a part of the page that is not there

**Why it matters.** A visitor clicks and nothing happens: the link names a \#part no element on the page has.

**Likely fix.** Give the part it means the id the link names, or point the link at the right one.

<details open>
<summary>1 link</summary>

- `/` \`\<a href="\#main"\>\`, on 7 pages: /, /contact-us, /for-consultants and 4 more

</details>

## minor SITE-28 The site has no sitemap search engines can read

**Why it matters.** A sitemap tells search engines every page to index, and how fresh each is; without one they find pages only by following links, and one listing wrong addresses spends their visits on errors.

**Likely fix.** Publish /sitemap.xml listing each page's final address \(most site builders and CMSs have a setting or plugin for it\), and name it in robots.txt \(Sitemap: ...\).

<details open>
<summary>1 address</summary>

- `/sitemap.txt` answered 404

</details>

## minor SITE-29 The site publishes no security.txt, the file that tells security researchers whom to contact

**Why it matters.** Researchers who find a security problem look for /.well-known/security.txt to know whom to tell \(RFC 9116\); without it they may not report it, or report it publicly.

**Likely fix.** Publish /.well-known/security.txt with a Contact line \(an email address or a form\) and an Expires line.

<details open>
<summary>1 address</summary>

- `/.well-known/security.txt` answered 404

</details>

## info SITE-40 1 script or style sheet from other sites' hosts did not load on 1 page, as seen by an automated visitor: unconfirmed \(other sites may block automated visitors\); check in a browser

**Why it matters.** Another site's script or style sheet \(a video player, a widget, an analytics tag\) failed while the crawler read the page. Many such services refuse or slow an automated visitor while they serve a person, so this is not said as a fact about the site; when it also fails in a browser, the part of the page that uses it does not work.

**Likely fix.** Open the page in an ordinary browser with the developer tools' network tab and console. If the request fails there too, check the embed's address and the account with that service, or remove the embed.

<details open>
<summary>1 page</summary>

- `/why-choose-us` 1 request: `kit.fontawesome.com/383df7a0c3.js` \(403\)

</details>

Read by Suite Builder's crawler, which identifies itself in its User-Agent and obeys robots.txt.
