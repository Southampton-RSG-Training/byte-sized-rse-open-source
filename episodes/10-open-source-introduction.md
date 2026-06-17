---
title: "Introduction"
teaching: 15
exercises: 0
---

:::::::::::::::::::::::::::::::::::::: questions 

- What is open source software?
- How can you use open source software in your projects?
- 

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Understand the different types of open source licenses.


::::::::::::::::::::::::::::::::::::::::::::::::

# Open Source Software

Open Source has transformed the research world over the last quarter century: the chances are any modern research software project relies in critical ways on open source software, whether it is Linux, SLURM, WebEngine, React, Python, R, NumPy, or PyTorch (or all of them!) or any of a vast array of other projects, big and small.

The power of open source is that it allows many different people and groups to contribute, debug and improve a piece of software, adapting it to changing needs and use-cases as time goes on.  Each user stands upon the shoulders of those who have contributed, and together the community produces something more substantial than any one person could possibly do themselves.

In most cases you will simply be a user of the open source software: if the software solves your problem adequately, you may never have the need or desire to contribute to the software you use.  But sometimes you run into a bug or a gap in functionality that means that the software can't do exactly what you need.

The good news is that open source software is just that: you can get the source code for the software with a little knowledge and some tools you can fix that bug or add that missing piece of functionality. And that often can be the end of the story: you've solved your problem and you can move on.

But that may not be the end of the story. Perhaps you want to use an open source library in software that you are distributing. Perhaps you think your changes might be valuable other people with the same problems that you've run into.  In these cases you may need to publish your code, and in some cases you might want to work with the community to incorporate your changes back into the original software. Or maybe you have code that you want to open source yourself.

In these cases you need to have an understanding of the licenses that protect open source code, the way that open source communities work, and the mechanics of contributing to someone else's project.

## How Open Source Works

A common perception is that open source software is "free" in the sense that it doesn't cost anything to use, but also in the sense that you are able to use it however you want.  However most open source software is not *completely* free to use. 

Software source is considered a creative work, and so is protected by copyright unless it has been placed in the public domain by the author or by copyright expiring.  By default you can't just copy the source code of a program and use it yourself.  So open source software usually comes with some sort of *license* which describes how you can and can't use it.  These licenses may be simple or complex, and may or may not place obligations on you if you use the source in certain ways.

The author or authors of a piece of software usually still control the copyright, and so they can choose to license the software in different ways and under different terms if they want to.  For example it is somewhat common for companies to open source their code under a restrictive license and offer a commercial license with less restrictive terms.

This course is going to mostly concentrate on software and software licenses, but there are notions of open source for other types of creative work, often using the Creative Commons licenses, which have many similarities to open source software licenses.  For example, this course itself is open source under a Creative Commons CC-BY 4.0 license.

::::::::::::::::: callout

## Patents and Trademarks

Copyright isn't the only type of intellectual property that may apply to software.

*Patents* can apply to software, particularly if it is part of a bigger system, and may restrict the ways that a piece of software can be used without separate licensing. Patents have a significantly shorter duration than sopyright. Some open source licenses, such as the Apache License 2.0 and GPL 3, have clauses regarding patents.

*Trademarks* may apply to open source software and prominent open source projects may have trademark protection.  This may affect how you can present your relationship to the software, how you use logos, and so on.  You may need to take some care when naming your project that it does not conflict with prominent project names.

If you have serious concerns about the intellectual property implications of the way that you want to use a piece of software you should consult with a lawyer.

:::::::::::::::::::::::::

## Open Source Licenses

There are many different open source licenses in use in the thousands upon thousands of open source projects.  The [Open Source Initiative has a list of licenses](https://opensource.org/licenses) that it considers to be "open source", but even then there are open source licenses which don't match its definitions which may be useful for research code (for example, licenses which restrict commercial use).

But in general license fall into a few different general categories in terms of the *requirements* they place on use:

- **attribution requirements**: a requirement to acknowledge the use of the code, often by including a license file. These sorts of requirements are sometimes called "permissive".
- **source sharing requirements**: a requirement to distribute or link to source code, usually under the same license as the code.  These sorts of requirements are often called "copyleft" or "viral".
- **usage restrictions**: some limitation on the ways the code may be used, frequently things like restricting commercial use, or use in ways that they authors find unethical.

In general permissive licenses allow the software to be used as part of a closed source or commerical product.  Copyleft licenses usually prevent use in closed source software.

And terms of the license may take effect in a number of different ways, such as:

- *distributing* the code, whether source or binary, a stand-alone program, library, or in embedded hardware
- *running the code on a server* usable by others
- *using* the code for particular purposes

Most licenses are fairly easy to read, and for the most commonly used licenses there are often guides that give and idea of the *intent* of the license.  Even if you are within the letter of the license in what you are doing, breaking the intent of the license may bring negative attention from the people whose work you depend on.

Common examples of licenses are:

- [**BSD**](https://en.wikipedia.org/wiki/BSD_licenses): there are several variations on this, originally used by the "Berkeley Software Distribution" open source Unix. It is used by Python and a large number of Python packages. It is a permissive license.
- [**MIT**](https://en.wikipedia.org/wiki/MIT_License): a license originally used by networking software released by the Massachussetts Insitute of Technology. It is widely used in Javascript libraries. It is a permissive license.
- [**Apache**](https://en.wikipedia.org/wiki/Apache_License): a license originally used by the Apache web server. It is widely used and is the third most popular open source license. It is generally a permissive license.
- [**LGPL**](https://en.wikipedia.org/wiki/GNU_Lesser_General_Public_License): this is a license which allows permissive use when distributed in unmodified form, but requires publication of modifications.  As a result it can be used in closed source and commercial software.
- [**GPL**](https://en.wikipedia.org/wiki/GNU_General_Public_License): this is the original copyleft license, originally used by the Free Software Foundation for the GNU unix tools. The GPL version 2 is the license used by Linux and many other prominent projects.  It can be used in servers without sharing code, or called as a separate OS process, but otherwise requires distribution of software which *links* against it to also use the GPL license.
- [**AGPL**](https://en.wikipedia.org/wiki/GNU_Affero_General_Public_License): this is a variant of the GPL that requires that software on servers that use it provide source and installation instructions for the entire server-side system.  The [Server-Side Public License (SSPL)](https://en.wikipedia.org/wiki/Server_Side_Public_License) is a similar license used by some projects. ElasticSearch, MongoDB and Redis are major projects which use this type of license.

::::::::::::::::: callout

### License Example

The NumPy license is a permissive "3-clause BSD License":
```
Copyright (c) 2005-2025, NumPy Developers.
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are
met:

    * Redistributions of source code must retain the above copyright
       notice, this list of conditions and the following disclaimer.

    * Redistributions in binary form must reproduce the above
       copyright notice, this list of conditions and the following
       disclaimer in the documentation and/or other materials provided
       with the distribution.

    * Neither the name of the NumPy Developers nor the names of any
       contributors may be used to endorse or promote products derived
       from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
"AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT
OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
(INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
```

The license doesn't promise anything to the users of the code, but does require including the license text when redistributing the software, whether in source or binary form.

:::::::::::::::::::::::::

### Licenses and Industry

In academia liciensing is rarely a problem, but in industry, or when thinking of commercialization opportunities, more care needs to be taken.

When working on projects with industry partners, you may find that they can be very wary about the use of software with copyleft-style open source licenses, particularly when it comes to libraries.  While they are usually fine to use within an organisation, there is the risk that if software using them is given to a third party (such as a customer, contractor or partner) it may require giving them not just the source for the library, but also for proprietary code that uses the library.

On the other hand, when considering commercialisation, some companies will dual-license their code: anyone can use the code if they agree to a copyleft license (which requires them to share any proprietary code), but they also offer a more standard paid commercial license without the copyleft provisions.  This permits them to build a community around their software, but also to earn income from other commercial users.

## Using Open Source

If you are planning to incorporate open source software in your work, you should spend at least a little time assessing whether it is suitable for the purposes that you have in mind for it.

Key things you should consider include:

- licensing: is the license compatible with how you intend to use it? For eaxample GPL licensed code may not be suitable for use with a non-GPL licensed project.
- fitness for purpose: does the software actually solve your problem, is it compatible with your operating system and environment. Some experimentation may be needed.
- documentation: is there good documenation of how to use the software. If the codebase is small this may not be a major issue, but documentation is always helpful.
- code quality: is the code clean and well-designed. This is one of the advantages of open source software: you can always look at the code.  Are their tests, does the code have a consistent style, do the design choices make sense to you.
- community: is there a community of users of the software? Is development active on the software or has it been abandoned?
- ease of use: can you easily install it and its dependencies? Can you build it and package it? Can it be used as a library rather than a stand-alone application? Is its interface complicated?

Other than licensing and fitness of purpose, none of these things are deal-breakers. For example, abandoned code may need a little effort to get it working again, but if it fits your need perfectly then it is likely worth that effort.

When you use open source software in your projects, ensure that you adhere to any license requirements it imposes. In many cases it won't be any. For example if you are writing a Python library with dependencies and the user has to install everything using a package manager like `pip` then you are not "distributing" the dependencies, PyPI is.

But if you are distributing a built binary program, application, or hardware, then even with permissive licensing you may have to at least publish acknowledgement in the form required by the license.

Additionally, no matter what the license, you should follow citation guidelines for software: look for `CITATION.cff` files or `DOI` references and use them appropriately.

Here are some scenarios to think about:

::::::::::::::::: challenge

Your project involves building many robots to be given for free to schools to teach computer science. The robots run linux on a single board computer (for example, a Raspberry Pi). What are your obligations under the Linux GPL license?

:::::::::::::::::: solution

You are distributing Linux in a binary form (likely along with may other GPL programs). You need to include the copyright notice and disclaimer from the GPL code you are using, as well as information about how to get the linux source code. If you haven't modified the source, a link to the third party source you used (likely from the manufacturer of the SBC) is sufficient and should have been provided to you from wherever you got Linux from.

It doesn't matter that your project is non-commerical, but it may matter who *owns* the robots.

Any custom application code that you write for the robots is unaffacted by the GPL.

:::::::::::::::::::::::::::
:::::::::::::::::::::::::::

::::::::::::::::: challenge

You write a mobile application to help with data collection in the field.  The only users are within your research group.  The application uses a BSD licensed library in a critical way.  How do you need to acknolwedge the use of the library?

:::::::::::::::::: solution

You are using the BSD licensed code internally within your organization, so you are not distributing it and so you do not need to include the BSD license with your application.

However you should cite the library in any relevant papers about your project.

:::::::::::::::::::::::::::
:::::::::::::::::::::::::::

::::::::::::::::: challenge

You write a Python library which has a dependency on a library licensed under the GPL.  Users will normally install your software using a package manager like `pip` or `conda` to download your library and its dependencies.  What are your obligations under the GPL?  What are your *users* obligations under the GPL?

:::::::::::::::::: solution

Because your users are downloading the GPL library using a package maanger, you are not distributing the code yourself and so you have no obligations under the GPL.  You may license your code however you like, including a closed-source proprietary license.

If your *users* distribute software which includes your library and the GPL code (for example in an application) then *they* will likely be bound by the GPL and so their distributed software will be licensed under the GPL.  If your license is not compatible with the GPL (such as a proprietary closed-source license) then they may not be able to distribute their software.

:::::::::::::::::::::::::::
:::::::::::::::::::::::::::

::::::::::::::::: challenge

You are looking for how to implement a particular algorithm and find a GitHub repo with an implementation contained in a much larger library.  The library is MIT licensed.  You copy just the module that implements the algorithm into your code and make your code available via GitHub.  What are your obligations?

:::::::::::::::::: solution

Because the licenses depend on copyright, they become effective whenever usage goes beyond fair use.  A copying a few lines is probably fine, but a module is likely substantial enough that it is protected by the MIT license terms, and you will have to provide appropriate acknowledgement and include the license for that module.  You can license your code under any compatible license.

Note that if the code you copied had been GPL licensed you might have needed to license all your code under a GPL-compatible license.

:::::::::::::::::::::::::::
:::::::::::::::::::::::::::

::::::::::::::::: callout

### Using Open Source for AI Training

Open source codebases have been extensively used for training LLMs - this is a large part of the reason that they can produce working code.  However there are some legal questions which are still open at the time of writing:

- can code generated by an LLM be copyrighted (and therefore protected by licenses). In the UK the answer is yes, but the US copyright office guidance is that there should be significant human creative input (more than a single prompt).

- an LLM trained on copyrighted material is likely a derived work.  It is currently an open question about whether training an LLM on copyrighted source code falls under fair use, or whether any licenses on the software also apply to the LLM.  The Free Software Foundation hsa indicated that they believe that the GPL should apply to LLMs trained on GPL licensed code and that the model weights and related code whould be open sourced under the GPL.  This has not been tested in court.

Code generated by an LLM trained on licensed code is generally considered not to be bound by the licenses, just as binaries generated by a compiler are generally not bound by the compiler's license.

:::::::::::::::::::::::::

::::::::::::::::: keypoints

- open source software is in use everywhere throughout the modern software ecosystem, perticularly for research code
- open source software allows usage of software through licensing of copyright
- different licenses may impose different obligations
- "permissive" licenses typically require some sort of acknowledgement of the original authors, but allow use in closed-source code
- "copyleft" licenses require that software which uses them to also be open source
- assess open source software before using it
- ensure that you comply with licenses and cite it correctly

:::::::::::::::::::::::::::
