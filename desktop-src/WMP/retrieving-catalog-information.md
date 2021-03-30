---
title: Recuperando Informações do catálogo
description: Recuperando Informações do catálogo
ms.assetid: f2ec795f-6e6f-4c0c-9332-f1e96524221a
keywords:
- Lojas online do Windows Media Player, recuperando informações do catálogo
- lojas online, recuperando informações do catálogo
- Digite 1 lojas online, recuperando informações do catálogo
- Armazenamentos online do Windows Media Player, informações de diagnóstico em catálogos
- lojas online, informações de diagnóstico em catálogos
- Digite 1 lojas online, informações de diagnóstico em catálogos
- Armazenamentos online do Windows Media Player, catcomp.exe
- lojas online, catcomp.exe
- Digite 1 lojas online, catcomp.exe
- catcomp.exe
- informações de diagnóstico em catálogos
- Recuperando Informações do catálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e721d6ba3e4d6b5106cf44446d4c96ed842ccd61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636644"
---
# <a name="retrieving-catalog-information"></a><span data-ttu-id="746f8-115">Recuperando Informações do catálogo</span><span class="sxs-lookup"><span data-stu-id="746f8-115">Retrieving Catalog Information</span></span>

<span data-ttu-id="746f8-116">Você pode exibir informações de diagnóstico em um catálogo executando catcomp com a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="746f8-116">You can display diagnostic information on a catalog by running catcomp with the following syntax:</span></span>


```C++
catcomp info <catalogpath> [track|artist|album] [ID]
```



<span data-ttu-id="746f8-117">Por exemplo, o comando a seguir exibe informações sobre um catálogo inteiro, incluindo a versão, a localidade e as informações internas em itens de catálogo:</span><span class="sxs-lookup"><span data-stu-id="746f8-117">For example, the following command displays information on an entire catalog, including the version, locale, and internal information on catalog items:</span></span>


```C++
catcomp info C:\Catalog210\catalog.wmdb
```



<span data-ttu-id="746f8-118">A seguir são exibidas informações para o roteiro com a ID 3256:</span><span class="sxs-lookup"><span data-stu-id="746f8-118">The following displays information for the track with ID 3256:</span></span>


```C++
catcomp info C:\Catalog210\catalog.wmdb track 3256
```



 

 




