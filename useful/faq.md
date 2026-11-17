# 📘 Frequently Asked Questions (FAQ)

This page provides our most frequently asked questions regarding our service.

## Which DNS record types are supported?

We support the following DNS record types:

* `A`
* `AAAA`
* `CNAME`
* `DS`
  * *Note: Can only be used alongside `NS` records.*
* `MX`
* `NS`
  * *Note: Only approved in specific cases. See [Who can use NS records?](#who-can-use-ns-records) for details.*
* `SRV`
* `TXT`

---

## Why does my domain still redirect to the has-a.space homepage?

This usually happens due to browser caching. [Clear your browser cache](https://support.google.com/accounts/answer/32050) and try again.

---

## Can I use a CNAME record with other record types?

No, unless the domain is proxied. A `CNAME` cannot be combined with other record types (`A`, `MX`, `TXT`, etc.) in the same record set. For exceptions and setup instructions, see [Proxying Your Domain](https://docs.has-a.space/domain-structure/#-proxied-optional).

---

## How long does it take for my pull request to be merged?

We're a team of volunteers, and has-a.space is a side project for us, so review times can vary. We'll get to your PR as soon as we can.

---

## Which platforms or services are supported?

While you can use almost any service, these are the most commonly used with has-a.space:

* GitHub Pages
* Netlify
* Railway

---

## Can I create nested subdomains (e.g., `sub.example.has-a.space`)?

Yes! You can nest subdomains as deeply as you'd like. To create one, name your file like `blog.example.json`. You **must own** `example.has-a.space` to register `blog.example.has-a.space`.

---

## I get an SSL error using GitHub Pages. How do I fix it?

Go to your GitHub Pages settings for your repository and **enable "Enforce HTTPS"**. This resolves most SSL issues.

---

## Can I become a maintainer or join the has-a.space team?

We don't accept direct applications. Team members are **handpicked**, often based on community involvement and support activity. Even then, it does **not guarantee** a position.

---

## I accidentally leaked sensitive data in my PR, what can I do?

* If **your PR containing sensitive information has not been merged**, contact us immediately:

  * Email: [admin@has-a.space](mailto:admin@has-a.space)
  * Discord: [our server](https://discord.gg/KFEN5E3PyR)

* If your PR **has already been merged**, we cannot retroactively remove it.

---

## Can I use my domain for a Minecraft server?

Yes, use an `A` record and an `SRV` record.
Refer to this [Namecheap article](https://www.namecheap.com/support/knowledgebase/article.aspx/9765/2208/how-can-i-link-my-domain-name-to-a-minecraft-server) for guidance.

> ⚠️ Root subdomains (e.g., `yourname.has-a.space`) **must relate to software development** as required in our [Terms of Service](https://has-a.space/terms).
> Use a *nested* subdomain (e.g., `mc.yourname.has-a.space`) for Minecraft.

---

## Who can use NS records?

We **allow** NS records only when:

* The standard DNS record types we support aren't sufficient.
* A provider (e.g. Aternos) **requires** NS delegation and **does not** have any other method of setting up a subdomain.
  * This is mostly regarding SaaS providers, **not** DNS providers like Cloudflare or deSEC.

We **do not allow** NS records for:

* Self hosting
  * **Note**: This can vary from case to case
* Convenience or ease of use
* Unverifiable or unsupported claims
* Non-functional or placeholder purposes
* Self hosting websites that can be easily hosted on a free platform like GitHub Pages
* If we have security or abuse concerns
* New users of has-a.space
  * If you have not had an has-a.space subdomain for at least 30 days, you will be denied due to security reasons.
* Users that have abused has-a.space subdomains in the past

> ⚠️ **We reserve the right to deny any NS request at our discretion for any reason.**

All NS record requests are reviewed on a case by case basis by the service owner.

Any PRs that clearly lack approved reasoning or evidence can be immediately denied by any maintainer, without a review from the service owner.
If denied by another maintainer, you do reserve the right to request a more thorough review from the service owner, which is possible by requesting the maintainer to escalate the PR.

> How long will it take for my NS record request to be reviewed?

Times can vary, usually within 24-72 hours, however in some rare cases it can take up to 2 weeks.

---

## Why are NS records restricted?

NS records give full control over DNS for a subdomain. That opens the door to misuse, abuse, and security concerns. To protect the community and domain integrity, we must be strict about who receives NS delegation.

---

## How can I update or delete my has-a.space subdomain?

Follow these steps:

1. **Review the [documentation](https://docs.has-a.space) and [ToS](https://has-a.space/terms)**.
2. **Open your JSON file** (in `/domains/your-subdomain.json`).
3. **Make your changes** (or delete the file if you're removing your domain).
4. **Commit the changes** to your fork.
5. **Push** them to your GitHub fork.
6. **Open a pull request** from your forked repo.
7. **Wait for approval and merging** by a maintainer.

> 💡 Keep an eye on your pull request, we may request changes before merging.

## Why does my PR have the "low priority" label?

This is because you have mentioned or messaged maintainers to get your PR approved.
