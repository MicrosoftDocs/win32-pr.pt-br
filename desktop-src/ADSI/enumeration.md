---
title: Enumeração
description: Acessar e manipular dados com ADSI fornece vários exemplos de enumeração. Você também pode enumerar os filhos de objetos de contêiner. Esses filhos são objetos em si, em vez de apenas propriedades em objetos.
ms.assetid: 1db19b00-8e43-4fc0-9099-1a1135219600
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, código de exemplo Visual Basic, usando IADsContainer para enumerar objetos
- contêineres ADSI, usando IADsContainer para enumerar filhos do contêiner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ba90e86282939486b79ee09cd17352841e733e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915904"
---
# <a name="enumeration"></a><span data-ttu-id="53ce4-107">Enumeração</span><span class="sxs-lookup"><span data-stu-id="53ce4-107">Enumeration</span></span>

<span data-ttu-id="53ce4-108">[Acessar e manipular dados com ADSI](accessing-and-manipulating-data-with-adsi.md) fornece vários exemplos de enumeração.</span><span class="sxs-lookup"><span data-stu-id="53ce4-108">[Accessing and Manipulating Data with ADSI](accessing-and-manipulating-data-with-adsi.md) provides several examples of enumeration.</span></span> <span data-ttu-id="53ce4-109">Você também pode enumerar os filhos de objetos de contêiner.</span><span class="sxs-lookup"><span data-stu-id="53ce4-109">You can also enumerate the children of container objects.</span></span> <span data-ttu-id="53ce4-110">Esses filhos são objetos em si, em vez de apenas propriedades em objetos.</span><span class="sxs-lookup"><span data-stu-id="53ce4-110">These children are objects themselves, rather than just properties on objects.</span></span>

<span data-ttu-id="53ce4-111">O exemplo a seguir usa a interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) para enumerar os filhos do contêiner.</span><span class="sxs-lookup"><span data-stu-id="53ce4-111">The following example uses the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface to enumerate the children of the container.</span></span>


```VB
Dim Container as IADsContainer
Dim Child as IADs

Set Container = GetObject("LDAP://MyServer/DC=MyDomain,DC=Fabrikam,DC=com")
 
For Each Child in Container
     Debug.Print Child.Name
Next Child
```



 

 




