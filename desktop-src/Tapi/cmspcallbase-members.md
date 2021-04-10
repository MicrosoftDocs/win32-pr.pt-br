---
description: A lista a seguir contém os membros do CMSPCAllBase.
ms.assetid: a3193639-e0c4-4851-a879-551eca8023f9
title: Membros do CMSPCallBase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ddae67d85a64a5a443727b3950054957c7f24f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169672"
---
# <a name="cmspcallbase-members"></a><span data-ttu-id="b0d7c-103">Membros do CMSPCallBase</span><span class="sxs-lookup"><span data-stu-id="b0d7c-103">CMSPCallBase Members</span></span>



| <span data-ttu-id="b0d7c-104">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="b0d7c-104">Member type</span></span>                   | <span data-ttu-id="b0d7c-105">Nome</span><span class="sxs-lookup"><span data-stu-id="b0d7c-105">Name</span></span>             | <span data-ttu-id="b0d7c-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0d7c-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0d7c-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="b0d7c-107">IUnknown</span></span>                      | <span data-ttu-id="b0d7c-108">\*\_pFTM m</span><span class="sxs-lookup"><span data-stu-id="b0d7c-108">\*m\_pFTM</span></span>        | <span data-ttu-id="b0d7c-109">Ponteiro para o Marshaller com thread livre.</span><span class="sxs-lookup"><span data-stu-id="b0d7c-109">Pointer to the free threaded marshaller.</span></span>                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="b0d7c-110">CMSPAddress\*</span><span class="sxs-lookup"><span data-stu-id="b0d7c-110">CMSPAddress\*</span></span>                 | <span data-ttu-id="b0d7c-111">\*\_pMSPAddress m</span><span class="sxs-lookup"><span data-stu-id="b0d7c-111">\*m\_pMSPAddress</span></span> | <span data-ttu-id="b0d7c-112">O ponteiro para o objeto de endereço MSP.</span><span class="sxs-lookup"><span data-stu-id="b0d7c-112">The pointer to the MSP address object.</span></span> <span data-ttu-id="b0d7c-113">Ele será usado para obter os terminais padrão se o aplicativo não selecionar nenhum.</span><span class="sxs-lookup"><span data-stu-id="b0d7c-113">It is used to get the default terminals if the application doesn't select any.</span></span> <span data-ttu-id="b0d7c-114">Ele também transporta um Refcount (via [**MSPAddressAddRef**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref), não AddRef) para que o endereço agregado não seja descontinuado enquanto a chamada ainda estiver ativa, mas o endereço da TAPI 3 não é AddRef'ed.</span><span class="sxs-lookup"><span data-stu-id="b0d7c-114">It also carries a refcount (via [**MSPAddressAddRef**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref), not AddRef) so that the aggregated address will not go away while the call is still alive, but TAPI 3's address is not AddRef'ed.</span></span> |
| <span data-ttu-id="b0d7c-115">\_identificador MSP</span><span class="sxs-lookup"><span data-stu-id="b0d7c-115">MSP\_HANDLE</span></span>                   | <span data-ttu-id="b0d7c-116">\*\_htCall m</span><span class="sxs-lookup"><span data-stu-id="b0d7c-116">\*m\_htCall</span></span>      | <span data-ttu-id="b0d7c-117">O identificador para chamar TAPI3's.</span><span class="sxs-lookup"><span data-stu-id="b0d7c-117">The handle to TAPI3's call.</span></span> <span data-ttu-id="b0d7c-118">Usado para acionar eventos de chamada.</span><span class="sxs-lookup"><span data-stu-id="b0d7c-118">Used to fire call events.</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="b0d7c-119">DWORD</span><span class="sxs-lookup"><span data-stu-id="b0d7c-119">DWORD</span></span>                         | <span data-ttu-id="b0d7c-120">\_dwMediaType m</span><span class="sxs-lookup"><span data-stu-id="b0d7c-120">m\_dwMediaType</span></span>   | <span data-ttu-id="b0d7c-121">Bitmask dos tipos de mídia nesta chamada.</span><span class="sxs-lookup"><span data-stu-id="b0d7c-121">Bitmask of the media types on this call.</span></span>                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="b0d7c-122">CMSPArray <ITStream \*></span><span class="sxs-lookup"><span data-stu-id="b0d7c-122">CMSPArray <ITStream \*></span></span> | <span data-ttu-id="b0d7c-123">\_fluxos m</span><span class="sxs-lookup"><span data-stu-id="b0d7c-123">m\_Streams</span></span>       | <span data-ttu-id="b0d7c-124">A lista de objetos de fluxo na chamada.</span><span class="sxs-lookup"><span data-stu-id="b0d7c-124">The list of stream objects in the call.</span></span>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="b0d7c-125">CMSPCritSection</span><span class="sxs-lookup"><span data-stu-id="b0d7c-125">CMSPCritSection</span></span>               | <span data-ttu-id="b0d7c-126">bloqueio de m \_</span><span class="sxs-lookup"><span data-stu-id="b0d7c-126">m\_lock</span></span>          | <span data-ttu-id="b0d7c-127">O bloqueio que protege as listas de fluxos.</span><span class="sxs-lookup"><span data-stu-id="b0d7c-127">The lock that protects the stream lists.</span></span>                                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="b0d7c-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b0d7c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0d7c-129">**CMSPCallBase**</span><span class="sxs-lookup"><span data-stu-id="b0d7c-129">**CMSPCallBase**</span></span>](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 



