---
title: Critérios para entradas de serviço de nome
description: Critérios para entradas de serviço de nome com RPC (chamada de procedimento remoto).
ms.assetid: f9a7b935-7104-489c-93a8-0c3793d17348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb32314dc86b179ea98bdf07000dc5ea359bdc77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453649"
---
# <a name="criteria-for-name-service-entries"></a><span data-ttu-id="cce87-103">Critérios para entradas de serviço de nome</span><span class="sxs-lookup"><span data-stu-id="cce87-103">Criteria for Name Service Entries</span></span>

<span data-ttu-id="cce87-104">Os critérios a seguir são usados ao processar entradas de serviço de nome:</span><span class="sxs-lookup"><span data-stu-id="cce87-104">The following criteria are used when processing name service entries:</span></span>

-   <span data-ttu-id="cce87-105">Se você fornecer um nome de entrada não **nulo** para [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina), essa entrada será a única entrada pesquisada para identificadores de associação.</span><span class="sxs-lookup"><span data-stu-id="cce87-105">If you provide a non-**NULL** entry name for [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina), that entry will be the only entry searched for binding handles.</span></span> <span data-ttu-id="cce87-106">Se você passar **NULL**, todas as entradas no seu domínio de logon serão pesquisadas.</span><span class="sxs-lookup"><span data-stu-id="cce87-106">If you pass **NULL**, all entries in your logon domain will be searched.</span></span> <span data-ttu-id="cce87-107">Observe que isso não inclui domínios confiáveis.</span><span class="sxs-lookup"><span data-stu-id="cce87-107">Note that this does not include trusted domains.</span></span>
-   <span data-ttu-id="cce87-108">Se você fornecer um identificador de interface, os identificadores de associação serão retornados de uma entrada somente se a seção de interface da entrada contiver uma versão compatível desse UUID de interface.</span><span class="sxs-lookup"><span data-stu-id="cce87-108">If you provide an interface handle, binding handles are returned from an entry only if the interface section of the entry contains a compatible version of that interface UUID.</span></span> <span data-ttu-id="cce87-109">Ou seja, o número de versão principal deve ser o mesmo que o UUID de interface, enquanto o número de versão secundária deve ser igual ou maior que o seu.</span><span class="sxs-lookup"><span data-stu-id="cce87-109">That is, the major version number must be the same as your interface UUID, while the minor version number must be equal to or greater than yours.</span></span>
-   <span data-ttu-id="cce87-110">Se você fornecer um UUID de objeto, os identificadores de associação serão retornados de uma entrada somente se a seção UUID de objeto da entrada contiver esse UUID de objeto específico.</span><span class="sxs-lookup"><span data-stu-id="cce87-110">If you provide an object UUID, binding handles are returned from an entry only if the object UUID section of the entry contains that particular object UUID.</span></span>

<span data-ttu-id="cce87-111">Se uma entrada de serviço de nome sobreviver aos critérios descritos acima, todos os identificadores de ligação dessas entradas serão coletados.</span><span class="sxs-lookup"><span data-stu-id="cce87-111">If a name service entry survives the criteria described above, all the binding handles from those entries are gathered.</span></span> <span data-ttu-id="cce87-112">Identificadores com uma sequência de protocolo sem suporte pelo cliente são descartados e os identificadores restantes são retornados para você como a saída de [**RpcNsBindingLookupNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext).</span><span class="sxs-lookup"><span data-stu-id="cce87-112">Handles with a protocol sequence that is unsupported by the client are discarded and the remaining handles are returned to you as the output from [**RpcNsBindingLookupNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext).</span></span>

 

 




