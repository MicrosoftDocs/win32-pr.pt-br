---
description: Métodos virtuais puros CMSPCallBase-esses métodos devem ser substituídos por classes derivadas.
ms.assetid: 2ea9d35a-c87e-44f4-8dc6-618251c81fe4
title: Métodos virtuais puros CMSPCallBase
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8da8530ab3dae737bf1407f00d5d4a415a1437e3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094454"
---
# <a name="cmspcallbase-pure-virtual-methods"></a><span data-ttu-id="b6970-103">Métodos virtuais puros CMSPCallBase</span><span class="sxs-lookup"><span data-stu-id="b6970-103">CMSPCallBase Pure Virtual Methods</span></span>

<span data-ttu-id="b6970-104">Esses métodos devem ser substituídos por classes derivadas.</span><span class="sxs-lookup"><span data-stu-id="b6970-104">These methods must be overridden by derived classes.</span></span>



| <span data-ttu-id="b6970-105">Métodos virtuais puros CMSPCallBase</span><span class="sxs-lookup"><span data-stu-id="b6970-105">CMSPCallBase pure virtual methods</span></span>                                 | <span data-ttu-id="b6970-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6970-106">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6970-107">**MSPCallAddRef**</span><span class="sxs-lookup"><span data-stu-id="b6970-107">**MSPCallAddRef**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcalladdref)               | <span data-ttu-id="b6970-108">Método AddRef privado para o objeto de chamada.</span><span class="sxs-lookup"><span data-stu-id="b6970-108">Private AddRef method for the call object.</span></span>                                                                                              |
| [<span data-ttu-id="b6970-109">**MSPCallRelease**</span><span class="sxs-lookup"><span data-stu-id="b6970-109">**MSPCallRelease**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcallrelease)             | <span data-ttu-id="b6970-110">Método de liberação particular para o objeto de chamada.</span><span class="sxs-lookup"><span data-stu-id="b6970-110">Private Release method for the call object.</span></span>                                                                                             |
| [<span data-ttu-id="b6970-111">**Init**</span><span class="sxs-lookup"><span data-stu-id="b6970-111">**Init**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-init)                                 | <span data-ttu-id="b6970-112">Chamado pelo objeto de endereço MSP (no método [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) para inicializar o objeto de chamada msp.</span><span class="sxs-lookup"><span data-stu-id="b6970-112">Called by the MSP address object (in the method [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) to initialize the MSP call object.</span></span> |
| [<span data-ttu-id="b6970-113">**Desligar**</span><span class="sxs-lookup"><span data-stu-id="b6970-113">**ShutDown**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-shutdown)                         | <span data-ttu-id="b6970-114">Chamado pelo objeto de endereço MSP para desligar a chamada..</span><span class="sxs-lookup"><span data-stu-id="b6970-114">Called by the MSP address object to shut down the call..</span></span>                                                                                |
| [<span data-ttu-id="b6970-115">**InternalCreateStream**</span><span class="sxs-lookup"><span data-stu-id="b6970-115">**InternalCreateStream**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) | <span data-ttu-id="b6970-116">Chamado por [**CreateStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) para criar um objeto de fluxo.</span><span class="sxs-lookup"><span data-stu-id="b6970-116">Called by [**CreateStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) to create a stream object.</span></span>                                               |
| [<span data-ttu-id="b6970-117">**Createstreamobject**</span><span class="sxs-lookup"><span data-stu-id="b6970-117">**CreateStreamObject**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-createstreamobject)     | <span data-ttu-id="b6970-118">Chamado por [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) para criar um objeto de fluxo.</span><span class="sxs-lookup"><span data-stu-id="b6970-118">Called by [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) to create a stream object.</span></span>                                  |
| [<span data-ttu-id="b6970-119">**RemoveStream**</span><span class="sxs-lookup"><span data-stu-id="b6970-119">**RemoveStream**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-removestream)                 | <span data-ttu-id="b6970-120">Chamado pelo aplicativo para remover um fluxo da chamada</span><span class="sxs-lookup"><span data-stu-id="b6970-120">Called by the application to remove a stream from the call</span></span>                                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="b6970-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b6970-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6970-122">**CMSPCallBase**</span><span class="sxs-lookup"><span data-stu-id="b6970-122">**CMSPCallBase**</span></span>](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 
