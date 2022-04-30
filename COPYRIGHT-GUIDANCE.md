<!-- Output copied to clipboard! -->

<!-----

Yay, no errors, warnings, or alerts!

Conversion time: 0.291 seconds.


Using this Markdown file:

1. Paste this output into your source file.
2. See the notes and action items below regarding this conversion run.
3. Check the rendered output (headings, lists, code blocks, tables) for proper
   formatting and use a linkchecker before you publish this page.

Conversion notes:

* Docs to Markdown version 1.0β33
* Sat Apr 30 2022 04:53:00 GMT-0700 (PDT)
* Source doc: DRAFT MakerDAO Copyright Guidance
* Tables are currently converted to HTML tables.

WARNING:
You have 2 H1 headings. You may want to use the "H1 -> H2" option to demote all headings by one level.

----->


<p style="color: red; font-weight: bold">>>>>>  gd2md-html alert:  ERRORs: 0; WARNINGs: 1; ALERTS: 0.</p>
<ul style="color: red; font-weight: bold"><li>See top comment block for details on ERRORs and WARNINGs. <li>In the converted Markdown or HTML, search for inline alerts that start with >>>>>  gd2md-html alert:  for specific instances that need correction.</ul>

<p style="color: red; font-weight: bold">Links to alert messages:</p>
<p style="color: red; font-weight: bold">>>>>> PLEASE check and correct alert issues and delete this message and the inline alerts.<hr></p>



# DRAFT Guidance for creators of MakerDAO assets on how to assign Copyright to Dai Foundation

This document contains guidance for how individual contributors to MakerDAO can assign copyright to Dai Foundation who is set up to be the guardian of MakerDAO’s intangible assets. The document also includes guidance for Github repository administrators on how to ensure that the software contributed has its copyright assigned to Dai Foundation.


# Assigning Software Copyright



1. Source code: Contributors are encouraged to follow the guidelines in this article:  \
https://matija.suklje.name/how-and-why-to-properly-write-copyright-statements-in-your-code \
 \
In a nutshell use the following format in each source file:

    ```
SPDX-FileCopyrightText: © {$year_of_file_creation} Dai Foundation <www.daifoundation.org>
SPDX-License-Identifier: {$SPDX_license_name}
```



For a list of license identifiers see [https://spdx.org/licenses/](https://spdx.org/licenses/)

For example, for a smart contract initially created in 2022, add the following to all source files


```
SPDX-FileCopyrightText: © 2022 Dai Foundation <www.daifoundation.org>
SPDX-License-Identifier: AGPL-3.0-or-later
```




2. For Github repository admins to cover occasional contributions and other cases where the copyright clause may not be included in the source files, setup the Github repository for the software with a Contributor License Agreement (CLA) assistant such that contributors will sign the CLA from within a pull request. See the appendix for CLA setup details
3. Add a COPYRIGHT file to the Github repository similar to a LICENSE file with the following content

    ```
The copyright holder for the code in this repository is: 
© {$year_of_repository_creation}  Dai Foundation <www.daifoundation.org>
```



Example:


```
The copyright holder for the code in this repository is: 
© 2022 Dai Foundation <www.daifoundation.org>
```



## What to do if I am contributing to software that already has other copyright holders than the Dai Foundation

In the case where the software being developed has other copyright holders than the Dai Foundation those copyright holders shall be listed together with the Dai Foundation.

For example, If contributing to a file in the DSS project that originally is written by rain, then specify the following:


```
SPDX-FileCopyrightText: © 2018 Rain <rainbreak@riseup.net>
SPDX-FileCopyrightText: © 2022 Dai Foundation <www.daifoundation.org>
SPDX-License-Identifier: AGPL-3.0-or-later
```



# Appendix 


# Contributor License Agreement (CLA) assistant setup

&lt; NOTE: this section is to be updated with a link to the local CLA assistant that TechOps will set up if CLA tests are satisfactory. DO NOT use the current link for any production purposes!

Ref: [https://github.com/cla-assistant/cla-assistant](https://github.com/cla-assistant/cla-assistant)  >

To set up your Github repository to check that contributors have signed a Contributor License Agreement and enable them to do so if they haven’t, do the following:



* Go to [https://cla-assistant.io/](https://cla-assistant.io/)
* Make sure that you are signed with the Github user that is admin on the Github repository that you want to set up the integration for
* Click “Configure CLA”, and specify
    * 1) the repository you want to set up CLA assistant for
    * 2) the location of the CLA - specify \
[https://gist.github.com/daifoundationadmin/e698f568fb9db41454d2a79f4ebfd592](https://gist.github.com/daifoundationadmin/e698f568fb9db41454d2a79f4ebfd592)
    * 3) Do not enter anything for the options under this point
* Click the LINK button - and that’s it

Now, When contributors create a Pull Request, the CLA assistant checks whether they have signed the CLA, and blocks the PUll Request until the CLA is signed
