---
title: In-Context e funções de gancho fora de contexto
description: Ao registrar uma função de gancho com SetWinEventHook, os clientes especificam se a função de Hook está no contexto ou fora de contexto. Esses termos descrevem o local da memória da função de gancho relativa ao espaço de endereço do servidor.
ms.assetid: 6876d74a-9c15-4f89-92ad-d072d9b528f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d96bff36f47b5e7fb0ad2e98d5a5347e2bc747
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160185"
---
# <a name="in-context-and-out-of-context-hook-functions"></a><span data-ttu-id="82b4c-104">In-Context e funções de gancho fora de contexto</span><span class="sxs-lookup"><span data-stu-id="82b4c-104">In-Context and Out-of-Context Hook Functions</span></span>

<span data-ttu-id="82b4c-105">Ao registrar uma função de gancho com [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook), os clientes especificam se a função de Hook está *no contexto* ou *fora de contexto*.</span><span class="sxs-lookup"><span data-stu-id="82b4c-105">When registering a hook function with [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook), clients specify whether the hook function is *in-context* or *out-of-context*.</span></span> <span data-ttu-id="82b4c-106">Esses termos descrevem o local da memória da função de gancho relativa ao espaço de endereço do servidor.</span><span class="sxs-lookup"><span data-stu-id="82b4c-106">These terms describe the memory location of the hook function relative to the server's address space.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="82b4c-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="82b4c-107">In this section</span></span>

-   [<span data-ttu-id="82b4c-108">Funções de gancho no contexto</span><span class="sxs-lookup"><span data-stu-id="82b4c-108">In-Context Hook Functions</span></span>](in-context-hook-functions.md)
-   [<span data-ttu-id="82b4c-109">Precauções da função de gancho no contexto</span><span class="sxs-lookup"><span data-stu-id="82b4c-109">In-Context Hook Function Precautions</span></span>](in-context-hook-function-precautions.md)
-   [<span data-ttu-id="82b4c-110">Funções de gancho fora do contexto</span><span class="sxs-lookup"><span data-stu-id="82b4c-110">Out-of-Context Hook Functions</span></span>](out-of-context-hook-functions.md)

 

 




