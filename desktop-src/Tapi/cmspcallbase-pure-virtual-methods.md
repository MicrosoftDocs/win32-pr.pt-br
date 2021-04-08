---
description: Esses métodos devem ser substituídos por classes derivadas.
ms.assetid: 2ea9d35a-c87e-44f4-8dc6-618251c81fe4
title: Métodos virtuais puros CMSPCallBase
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d8dea4c1a240e362a4dc3a19b3c09a37a318947
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828519"
---
# <a name="cmspcallbase-pure-virtual-methods"></a><span data-ttu-id="d921c-103">Métodos virtuais puros CMSPCallBase</span><span class="sxs-lookup"><span data-stu-id="d921c-103">CMSPCallBase Pure Virtual Methods</span></span>

<span data-ttu-id="d921c-104">Esses métodos devem ser substituídos por classes derivadas.</span><span class="sxs-lookup"><span data-stu-id="d921c-104">These methods must be overridden by derived classes.</span></span>



| <span data-ttu-id="d921c-105">Métodos virtuais puros CMSPCallBase</span><span class="sxs-lookup"><span data-stu-id="d921c-105">CMSPCallBase pure virtual methods</span></span>                                 | <span data-ttu-id="d921c-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="d921c-106">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d921c-107">**MSPCallAddRef**</span><span class="sxs-lookup"><span data-stu-id="d921c-107">**MSPCallAddRef**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcalladdref)               | <span data-ttu-id="d921c-108">Método AddRef privado para o objeto de chamada.</span><span class="sxs-lookup"><span data-stu-id="d921c-108">Private AddRef method for the call object.</span></span>                                                                                              |
| [<span data-ttu-id="d921c-109">**MSPCallRelease**</span><span class="sxs-lookup"><span data-stu-id="d921c-109">**MSPCallRelease**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcallrelease)             | <span data-ttu-id="d921c-110">Método de liberação particular para o objeto de chamada.</span><span class="sxs-lookup"><span data-stu-id="d921c-110">Private Release method for the call object.</span></span>                                                                                             |
| [<span data-ttu-id="d921c-111">**Init**</span><span class="sxs-lookup"><span data-stu-id="d921c-111">**Init**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-init)                                 | <span data-ttu-id="d921c-112">Chamado pelo objeto de endereço MSP (no método [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) para inicializar o objeto de chamada msp.</span><span class="sxs-lookup"><span data-stu-id="d921c-112">Called by the MSP address object (in the method [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) to initialize the MSP call object.</span></span> |
| [<span data-ttu-id="d921c-113">**Desligar**</span><span class="sxs-lookup"><span data-stu-id="d921c-113">**ShutDown**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-shutdown)                         | <span data-ttu-id="d921c-114">Chamado pelo objeto de endereço MSP para desligar a chamada..</span><span class="sxs-lookup"><span data-stu-id="d921c-114">Called by the MSP address object to shut down the call..</span></span>                                                                                |
| [<span data-ttu-id="d921c-115">**InternalCreateStream**</span><span class="sxs-lookup"><span data-stu-id="d921c-115">**InternalCreateStream**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) | <span data-ttu-id="d921c-116">Chamado por [**CreateStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) para criar um objeto de fluxo.</span><span class="sxs-lookup"><span data-stu-id="d921c-116">Called by [**CreateStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) to create a stream object.</span></span>                                               |
| [<span data-ttu-id="d921c-117">**Createstreamobject**</span><span class="sxs-lookup"><span data-stu-id="d921c-117">**CreateStreamObject**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-createstreamobject)     | <span data-ttu-id="d921c-118">Chamado por [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) para criar um objeto de fluxo.</span><span class="sxs-lookup"><span data-stu-id="d921c-118">Called by [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) to create a stream object.</span></span>                                  |
| [<span data-ttu-id="d921c-119">**RemoveStream**</span><span class="sxs-lookup"><span data-stu-id="d921c-119">**RemoveStream**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-removestream)                 | <span data-ttu-id="d921c-120">Chamado pelo aplicativo para remover um fluxo da chamada</span><span class="sxs-lookup"><span data-stu-id="d921c-120">Called by the application to remove a stream from the call</span></span>                                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="d921c-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d921c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d921c-122">**CMSPCallBase**</span><span class="sxs-lookup"><span data-stu-id="d921c-122">**CMSPCallBase**</span></span>](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 
