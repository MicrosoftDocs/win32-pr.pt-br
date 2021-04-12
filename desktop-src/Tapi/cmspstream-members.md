---
description: A lista a seguir contém os membros do CMSPStream.
ms.assetid: 792a29ac-ebbb-4bb2-bebf-fbf870b18e84
title: Membros do CMSPStream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dacee41ff95cdf16c7cd50c2e39017d9dfa7e83c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091656"
---
# <a name="cmspstream-members"></a><span data-ttu-id="66f27-103">Membros do CMSPStream</span><span class="sxs-lookup"><span data-stu-id="66f27-103">CMSPStream Members</span></span>



| <span data-ttu-id="66f27-104">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="66f27-104">Member type</span></span>                     | <span data-ttu-id="66f27-105">Nome</span><span class="sxs-lookup"><span data-stu-id="66f27-105">Name</span></span>                | <span data-ttu-id="66f27-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="66f27-106">Description</span></span>                                                                                                                                |
|---------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66f27-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="66f27-107">IUnknown</span></span>                        | <span data-ttu-id="66f27-108">\*\_pFTM m</span><span class="sxs-lookup"><span data-stu-id="66f27-108">\*m\_pFTM</span></span>           | <span data-ttu-id="66f27-109">Ponteiro para o Marshaller com thread livre.</span><span class="sxs-lookup"><span data-stu-id="66f27-109">Pointer to the free threaded marshaller.</span></span>                                                                                                   |
| <span data-ttu-id="66f27-110">DWORD</span><span class="sxs-lookup"><span data-stu-id="66f27-110">DWORD</span></span>                           | <span data-ttu-id="66f27-111">\_dwState m</span><span class="sxs-lookup"><span data-stu-id="66f27-111">m\_dwState</span></span>          | <span data-ttu-id="66f27-112">O estado atual do fluxo.</span><span class="sxs-lookup"><span data-stu-id="66f27-112">The current state of the stream.</span></span>                                                                                                           |
| <span data-ttu-id="66f27-113">PROCESSAMENTO</span><span class="sxs-lookup"><span data-stu-id="66f27-113">HANDLE</span></span>                          | <span data-ttu-id="66f27-114">\_hAddress m</span><span class="sxs-lookup"><span data-stu-id="66f27-114">m\_hAddress</span></span>         | <span data-ttu-id="66f27-115">O endereço no qual esse fluxo está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="66f27-115">The address on which this stream is being used.</span></span>                                                                                            |
| <span data-ttu-id="66f27-116">DWORD</span><span class="sxs-lookup"><span data-stu-id="66f27-116">DWORD</span></span>                           | <span data-ttu-id="66f27-117">\_dwMediaType m</span><span class="sxs-lookup"><span data-stu-id="66f27-117">m\_dwMediaType</span></span>      | <span data-ttu-id="66f27-118">O [**tipo de mídia**](tapimediatype--constants.md) desse fluxo (áudio, vídeo, etc.).</span><span class="sxs-lookup"><span data-stu-id="66f27-118">The [**media type**](tapimediatype--constants.md) of this stream (audio, video, etc.).</span></span>                                                    |
| <span data-ttu-id="66f27-119">direção do TERMINAL \_</span><span class="sxs-lookup"><span data-stu-id="66f27-119">TERMINAL\_DIRECTION</span></span>             | <span data-ttu-id="66f27-120">\_direção m</span><span class="sxs-lookup"><span data-stu-id="66f27-120">m\_Direction</span></span>        | <span data-ttu-id="66f27-121">A [**direção**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction) desse fluxo (entrada ou saída).</span><span class="sxs-lookup"><span data-stu-id="66f27-121">The [**direction**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction) of this stream (incoming or outgoing).</span></span>                                                         |
| <span data-ttu-id="66f27-122">CMSPCallBase</span><span class="sxs-lookup"><span data-stu-id="66f27-122">CMSPCallBase</span></span>                    | <span data-ttu-id="66f27-123">\*\_pMSPCall m</span><span class="sxs-lookup"><span data-stu-id="66f27-123">\*m\_pMSPCall</span></span>       | <span data-ttu-id="66f27-124">Ponteiro para o objeto de chamada.</span><span class="sxs-lookup"><span data-stu-id="66f27-124">Pointer to the call object.</span></span>                                                                                                                |
| <span data-ttu-id="66f27-125">IGraphBuilder</span><span class="sxs-lookup"><span data-stu-id="66f27-125">IGraphBuilder</span></span>                   | <span data-ttu-id="66f27-126">\*\_pIGraphBuilder m</span><span class="sxs-lookup"><span data-stu-id="66f27-126">\*m\_pIGraphBuilder</span></span> | <span data-ttu-id="66f27-127">Ponteiro para interfaces de objeto de gráfico.</span><span class="sxs-lookup"><span data-stu-id="66f27-127">Pointer to graph object interfaces.</span></span>                                                                                                        |
| <span data-ttu-id="66f27-128">IMediaControl</span><span class="sxs-lookup"><span data-stu-id="66f27-128">IMediaControl</span></span>                   | <span data-ttu-id="66f27-129">\*\_pIMediaControl m</span><span class="sxs-lookup"><span data-stu-id="66f27-129">\*m\_pIMediaControl</span></span> | <span data-ttu-id="66f27-130">Ponteiro para a interface de controle de mídia.</span><span class="sxs-lookup"><span data-stu-id="66f27-130">Pointer to the media control interface.</span></span>                                                                                                    |
| <span data-ttu-id="66f27-131">CMSPArray <ITTerminal \*></span><span class="sxs-lookup"><span data-stu-id="66f27-131">CMSPArray <ITTerminal \*></span></span> | <span data-ttu-id="66f27-132">\_terminais m</span><span class="sxs-lookup"><span data-stu-id="66f27-132">m\_Terminals</span></span>        | <span data-ttu-id="66f27-133">A lista de terminais no fluxo.</span><span class="sxs-lookup"><span data-stu-id="66f27-133">The list of terminals on the stream.</span></span>                                                                                                       |
| <span data-ttu-id="66f27-134">CMSPCritSection</span><span class="sxs-lookup"><span data-stu-id="66f27-134">CMSPCritSection</span></span>                 | <span data-ttu-id="66f27-135">bloqueio de m \_</span><span class="sxs-lookup"><span data-stu-id="66f27-135">m\_lock</span></span>             | <span data-ttu-id="66f27-136">O bloqueio que protege o objeto de fluxo.</span><span class="sxs-lookup"><span data-stu-id="66f27-136">The lock that protects the stream object.</span></span> <span data-ttu-id="66f27-137">O objeto Stream nunca deve adquirir o bloqueio e, em seguida, chamar um método MSPCall que possa ser bloqueado.</span><span class="sxs-lookup"><span data-stu-id="66f27-137">The stream object should never acquire the lock and then call an MSPCall method that might lock.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="66f27-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="66f27-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66f27-139">**CMSPStream**</span><span class="sxs-lookup"><span data-stu-id="66f27-139">**CMSPStream**</span></span>](/windows/desktop/api/Mspstrm/nl-mspstrm-cmspstream)
</dt> </dl>

 

 



