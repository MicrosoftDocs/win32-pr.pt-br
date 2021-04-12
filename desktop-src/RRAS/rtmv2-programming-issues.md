---
title: Problemas de programação do RTMv2
description: As funções RTMv2 são escritas com as seguintes suposições.
ms.assetid: c8c6f553-57cc-4eec-bbc0-b6b50897cc75
keywords:
- Problemas de programação, RTMv2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b607adc939ff72a4d9fee99c15f6aa5192fa4c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292150"
---
# <a name="rtmv2-programming-issues"></a><span data-ttu-id="111cb-104">Problemas de programação do RTMv2</span><span class="sxs-lookup"><span data-stu-id="111cb-104">RTMv2 Programming Issues</span></span>

<span data-ttu-id="111cb-105">As funções RTMv2 são escritas com as seguintes suposições.</span><span class="sxs-lookup"><span data-stu-id="111cb-105">RTMv2 functions are written with the following assumptions.</span></span>

-   <span data-ttu-id="111cb-106">As funções RTMv2 não alocam memória para o cliente.</span><span class="sxs-lookup"><span data-stu-id="111cb-106">RTMv2 functions do not allocate memory for the client.</span></span> <span data-ttu-id="111cb-107">O cliente deve sempre alocar memória.</span><span class="sxs-lookup"><span data-stu-id="111cb-107">The client must always allocate memory.</span></span>
-   <span data-ttu-id="111cb-108">Quando um cliente está cancelando o registro, ele deve executar operações de limpeza em si, como liberar toda a memória alocada.</span><span class="sxs-lookup"><span data-stu-id="111cb-108">When a client is unregistering, it must perform clean-up operations itself, such as releasing all memory allocated.</span></span>
-   <span data-ttu-id="111cb-109">Os clientes devem liberar identificadores corretamente; podem ocorrer vazamentos de memória se um cliente não observar essa prática.</span><span class="sxs-lookup"><span data-stu-id="111cb-109">Clients must release handles correctly; memory leaks can occur if a client does not observe this practice.</span></span>

 

 




