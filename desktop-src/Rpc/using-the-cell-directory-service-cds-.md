---
title: Usando o CDS (serviço de diretório de células)
description: Se você tiver CDS, poderá usá-lo em vez do Microsoft Locator.
ms.assetid: df4b8db1-08f1-4ed8-895d-236199289e87
keywords:
- RPC de chamada de procedimento remoto, tarefas, usando o serviço de diretório de célula
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0029bf78308d6963d615daa04eaf87f3617ebbb2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635929"
---
# <a name="using-the-cell-directory-service-cds"></a><span data-ttu-id="9b097-104">Usando o CDS (serviço de diretório de células)</span><span class="sxs-lookup"><span data-stu-id="9b097-104">Using the Cell Directory Service (CDS)</span></span>

<span data-ttu-id="9b097-105">Se você tiver CDS, poderá usá-lo em vez do Microsoft Locator.</span><span class="sxs-lookup"><span data-stu-id="9b097-105">If you have CDS, you can use it instead of Microsoft Locator.</span></span> <span data-ttu-id="9b097-106">Altere as entradas do registro, conforme mostrado:</span><span class="sxs-lookup"><span data-stu-id="9b097-106">Change the registry entries as shown:</span></span>

``` syntax
HKEY_LOCAL_MACHINE
    Software
        Microsoft
            Rpc
                Name Service
                    NetworkAddress
 
HKEY_LOCAL_MACHINE
    Software
        Microsoft
            Rpc
                Name Service
                    Endpoint
```

<span data-ttu-id="9b097-107">A alteração dessas entradas apontará para um computador de gateway que esteja executando o NSID.</span><span class="sxs-lookup"><span data-stu-id="9b097-107">Changing these entries will point to a gateway computer that is running the NSID.</span></span> <span data-ttu-id="9b097-108">Isso será usado como o localizador mestre.</span><span class="sxs-lookup"><span data-stu-id="9b097-108">This will be used as the master locator.</span></span> <span data-ttu-id="9b097-109">No caso de uma falha, não haverá nenhuma pesquisa por uma substituição.</span><span class="sxs-lookup"><span data-stu-id="9b097-109">In the event of a crash, there will be no search for a replacement.</span></span>

 

 




