

# DRAFT Guidance for creators of MakerDAO assets on how to assign Copyright to Dai Foundation

  

This document contains guidance for how individual contributors to MakerDAO can assign copyright to Dai Foundation who is set up to be the guardian of MakerDAO’s intangible assets. The document also includes guidance for Github repository administrators on how to ensure that the software contributed has its copyright assigned to Dai Foundation.

  
  

# Assigning Software Copyright

  
  
  

A). Source code: Contributors are encouraged to follow the guidelines in this article: 
https://matija.suklje.name/how-and-why-to-properly-write-copyright-statements-in-your-code \


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

B). For Github repository admins to cover occasional contributions and other cases where the copyright clause may not be included in the source files, setup the Github repository for the software with a Contributor License Agreement (CLA) assistant such that contributors will sign the CLA from within a pull request. See the appendix for CLA setup details

C). Add a **COPYRIGHT** file to the Github repository similar to a LICENSE file with the following content

```

The copyright holder for the code in this repository is:

© {$year_of_repository_creation} Dai Foundation <www.daifoundation.org>

```
Example:
```

The copyright holder for the code in this repository is:

© 2022 Dai Foundation <www.daifoundation.org>

```
NOTE: If you have your code in another Github project than the `makerdao` project, then notify Dai Foundation about the location of the software. Do this by sending an email to support@daifoundation.org specifying where your repository resides.

## What to do if I am contributing to software that already has other copyright holders than the Dai Foundation

In the case where the software being developed has other copyright holders than the Dai Foundation those copyright holders shall be listed together with the Dai Foundation.

For example, If contributing to a file in the DSS project that originally is written by rain, then specify the following:

```

SPDX-FileCopyrightText: © 2018 Rain <rainbreak@riseup.net>
SPDX-FileCopyrightText: © 2022 Dai Foundation <www.daifoundation.org>

SPDX-License-Identifier: AGPL-3.0-or-later

```
 
Please note that while Maker Foundation transferred all Maker Protocol software copyrights to Dai Foundation, there may still exist code snippets that include copyright statements referring to Maker Ecosystem Growth Holdings, INC. (MEGH). In such a case, do replace "Maker Ecosystem Growth Holdings, INC." with Dai Foundation while keeping the year of first contribution. 

For example, if the code includes
`Copyright (C) 2018 Maker Ecosystem Growth Holdings, INC.` then update the statement like this:
`SPDX-FileCopyrightText: © 2018 Dai Foundation <www.daifoundation.org>`

You may wonder whether this is ok, since Dai Foundation only was created in 2019. It is ok because the prior contributor (MEGH) has transferred it copyrights to Dai Foundation. The statement in the example above shall be read as: "The copyright for the software that was created from 2018 and onwards belong to Dai Foundation".  

# Appendix

## Contributor License Agreement (CLA) assistant setup

*&lt; NOTE: this section is to be updated with a link to the local CLA assistant that TechOps will set up if CLA tests are satisfactory. DO NOT use the current link for any production purposes!*

**To try out a test CLA integration create a Pull Request for https://github.com/daifoundation/docs**

*Ref: [https://github.com/cla-assistant/cla-assistant](https://github.com/cla-assistant/cla-assistant) >*
### Setup
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