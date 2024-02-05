# PDF File analysis

<details>

<summary><strong>Learn AWS hacking from zero to hero with</strong> <a href="https://training.hacktricks.xyz/courses/arte"><strong>htARTE (HackTricks AWS Red Team Expert)</strong></a><strong>!</strong></summary>

Other ways to support HackTricks:

* If you want to see your **company advertised in HackTricks** or **download HackTricks in PDF** Check the [**SUBSCRIPTION PLANS**](https://github.com/sponsors/carlospolop)!
* Get the [**official PEASS & HackTricks swag**](https://peass.creator-spring.com)
* Discover [**The PEASS Family**](https://opensea.io/collection/the-peass-family), our collection of exclusive [**NFTs**](https://opensea.io/collection/the-peass-family)
* **Join the** 💬 [**Discord group**](https://discord.gg/hRep4RUj7f) or the [**telegram group**](https://t.me/peass) or **follow** us on **Twitter** 🐦 [**@hacktricks_live**](https://twitter.com/hacktricks_live)**.**
* **Share your hacking tricks by submitting PRs to the** [**HackTricks**](https://github.com/carlospolop/hacktricks) and [**HackTricks Cloud**](https://github.com/carlospolop/hacktricks-cloud) github repos.

</details>

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

\
Use [**Trickest**](https://trickest.com/?utm\_campaign=hacktrics\&utm\_medium=banner\&utm\_source=hacktricks) to easily build and **automate workflows** powered by the world's **most advanced** community tools.\
Get Access Today:

{% embed url="https://trickest.com/?utm_campaign=hacktrics&utm_medium=banner&utm_source=hacktricks" %}

From: [https://trailofbits.github.io/ctf/forensics/](https://trailofbits.github.io/ctf/forensics/)

PDF is an extremely complicated document file format, with enough tricks and hiding places [to write about for years](https://www.sultanik.com/pocorgtfo/). This also makes it popular for CTF forensics challenges. The NSA wrote a guide to these hiding places in 2008 titled "Hidden Data and Metadata in Adobe PDF Files: Publication Risks and Countermeasures." It's no longer available at its original URL, but you can [find a copy here](http://www.itsecure.hu/library/file/Biztons%C3%A1gi%20%C3%BAtmutat%C3%B3k/Alkalmaz%C3%A1sok/Hidden%20Data%20and%20Metadata%20in%20Adobe%20PDF%20Files.pdf). Ange Albertini also keeps a wiki on GitHub of [PDF file format tricks](https://github.com/corkami/docs/blob/master/PDF/PDF.md).

The PDF format is partially plain-text, like HTML, but with many binary "objects" in the contents. Didier Stevens has written [good introductory material](https://blog.didierstevens.com/2008/04/09/quickpost-about-the-physical-and-logical-structure-of-pdf-files/) about the format. The binary objects can be compressed or even encrypted data, and include content in scripting languages like JavaScript or Flash. To display the structure of a PDF, you can either browse it with a text editor or open it with a PDF-aware file-format editor like Origami.

[qpdf](https://github.com/qpdf/qpdf) is one tool that can be useful for exploring a PDF and transforming or extracting information from it. Another is a framework in Ruby called [Origami](https://github.com/mobmewireless/origami-pdf).

When exploring PDF content for hidden data, some of the hiding places to check include:

* non-visible layers
* Adobe's metadata format "XMP"
* the "incremental generation" feature of PDF wherein a previous version is retained but not visible to the user
* white text on a white background
* text behind images
* an image behind an overlapping image
* non-displayed comments

There are also several Python packages for working with the PDF file format, like [PeepDF](https://github.com/jesparza/peepdf), that enable you to write your own parsing scripts.

<details>

<summary><strong>Learn AWS hacking from zero to hero with</strong> <a href="https://training.hacktricks.xyz/courses/arte"><strong>htARTE (HackTricks AWS Red Team Expert)</strong></a><strong>!</strong></summary>

Other ways to support HackTricks:

* If you want to see your **company advertised in HackTricks** or **download HackTricks in PDF** Check the [**SUBSCRIPTION PLANS**](https://github.com/sponsors/carlospolop)!
* Get the [**official PEASS & HackTricks swag**](https://peass.creator-spring.com)
* Discover [**The PEASS Family**](https://opensea.io/collection/the-peass-family), our collection of exclusive [**NFTs**](https://opensea.io/collection/the-peass-family)
* **Join the** 💬 [**Discord group**](https://discord.gg/hRep4RUj7f) or the [**telegram group**](https://t.me/peass) or **follow** us on **Twitter** 🐦 [**@hacktricks_live**](https://twitter.com/hacktricks_live)**.**
* **Share your hacking tricks by submitting PRs to the** [**HackTricks**](https://github.com/carlospolop/hacktricks) and [**HackTricks Cloud**](https://github.com/carlospolop/hacktricks-cloud) github repos.

</details>
