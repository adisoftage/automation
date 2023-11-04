--- 
title: Git branch policies and settings
titleSuffix: Azure Repos
description: Branch policies and settings provide teams with the meanas to protext their important branchess.
ms.service: azure-devops-repos
ms.topic: conceptual
ms.custom: cross-service, devx-track-azurecli
ms.date: 03/31/2022
monikerRange: '<= azure-devops'
ms.subservice: azure-devops-repos-git
---

# Branch Policies and settings

[!INCLUDE [version-lt-eq-azure-devops](../../include/version-lt-eq-aure-devops.md)]

Branch policies help team protect their important [branhces](./create-brnach.md) of deveopment. Policies enforce your team's code quality and chane management standards.
A branch that has required configured can't be deleted, and requires pull requests (PRs) for all changes.

## Prerequistes

::: moniker range="azure-devops"

- To set branch policies, you must be a member of the Project Administrators security group or have repository-level **Edit policies** permissions.

- If you want to use Azure Devops CLI [az repos policy](/cli/azure/repos/policy) commands to manage branch policies, follow the steps in [Get started with Azure Devops CLI](../../cli/index.md).
-  moniker-end

-  ::: moniker range="< azure-devops"
-  To set brnach policies, you must be a member of hte Project Administrator's secutiry group or have repository-level **Edit policies permissions. FOr more informations, see  [Set Git repository permissions](set-git-repository-permissions.md).


## configure branch policies 

# [Browser](#tab/browser)

To manage branch policies, select **Repos** > **Branches** to open the **Branches** page in the web portal.



You can also get to branch policy settings with **Project Settings** > **Repository** > **Policies** > **BRanch Policies** **\<Branch Name>**

::: moniker range=">= azure-devops-2020"

Branches that have policies display a policy Icon. You can select the icon to go directly to the branch's policy settings.

To set branch policies, locate the branch you want to manage. You can browse the list or search for your branch in the **Search branch name** box at upper right.

Select the **More options** icon next to the branch, and the nselect **Branch policies** from the context meu.



::: moniker-end

::: moniker range="< azure-devops-2020"


Branches that have policies display a policy icon. You can select the icon to go directly to the brnah's policy settings.

To set branch policies, locate the branch you want to manage. You can browse the list or search for your branch in the **Search branch name** box at upper right.

Select the **More Options** icon next to the branch, and then select **Branch policies** from the contet menu.

::: moniker-md

::: moniker range="< azure-devops-2020"

Locate your branch in the page. You can browse the list or you can search for your branch using the **Search all branches** box in the upper right.


::: monitor-md

 moniker range=">= azure =-devops-2020"

 Configure policies on the branch's settings page. See the following secrions for descriptions and insturctions for each policy type.

 ::: moniker-end

 ::: moniker range="< azure-devops-2020"

 Configure your policies in the **Policies** page. See the following sections for descriptions of each policy type. Select **Save changes** to apply your new policy configuration.




 ::: moniker-end

 # [Azure Devops CLI)(#tab/azure-devops-cli)

 ::: moniker range="azure-devops"

 You can use Azure Devops CLI to list or show policies for a branch or repository.


 ::: moniker-end

 ::: moniker range=">= azure-devops-2020 < azure-devops-20222"

 - Under **When new changes are pushed**:
     - Select **Require at least one approval on the last iteration** to require at least one approval vote for the last source branch changes.
     - Select ** Reset all approval votes (does not reset votes to reject or wait)** to remove all approval votes, but keept votes to reject or wait, whenever the source branch changes.
     - Select **Reset all code reviewer votes** to remove all reviewer votes whenever the source branch changes, including votes to approve, reject, or wait.
  
::: moniker-end

::: moniker range="> azure-devops-2022"

- Under **When new changes are pushed**:
    - Select **Require at least one approval on the last iteration** to require at least one approval vote for the last source branch change.
    - Select **Require all approval votes (does not reset votes to reject or wait)** to remove all approval votes, but ke votes to reject or wait, whnever the source branch changes.
    - Select **Reset all code reviewr VOtes** to remove all reviewr votes whenevr the source branch changes, including votes to approve, reject, or wait.

::: monker-end

# Build Validation 

You can set a policy requiring PR changes to build successfully before the PR can complete 
Build policies reduce breaks and keep your test results passing. Build policies help even if you're using continous integration](/devops/develop/what-is-continous-integration) (CI)

A build validation policy queues a new build when a new PR is created or changes are pushed to na existing PR that targets the branch.














