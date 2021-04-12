---
title: Serviços de Área de Trabalho Remota referência da API AudioEndpoint
description: Dá suporte a interfaces para registro de ponto de extremidade de áudio e transporte de dados.
ms.assetid: 0e3ea0e7-8c61-400e-b8ef-8a0403aedafa
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota Serviços de Área de Trabalho Remota, referência de API AudioEndpoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1958b21643083a14110ddad77f68024cc464dd36
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364250"
---
# <a name="remote-desktop-services-audioendpoint-api-reference"></a><span data-ttu-id="01925-104">Serviços de Área de Trabalho Remota referência da API AudioEndpoint</span><span class="sxs-lookup"><span data-stu-id="01925-104">Remote Desktop Services AudioEndpoint API reference</span></span>

<span data-ttu-id="01925-105">Um *ponto de extremidade de áudio* representa um dispositivo de áudio, uma API de áudio ou qualquer outra fonte de áudio ou coletor, e é usado para enviar dados ou consumir dados do mecanismo de áudio.</span><span class="sxs-lookup"><span data-stu-id="01925-105">An *audio endpoint* represents an audio device, audio API, or any other audio source or sink, and is used to send data to or consume data from the audio engine.</span></span> <span data-ttu-id="01925-106">Um ponto de extremidade de áudio deve ser conectado ao mecanismo de áudio por meio de uma *conexão*, e cada conexão pode ter apenas um ponto de extremidade conectado a ele.</span><span class="sxs-lookup"><span data-stu-id="01925-106">An audio endpoint must be connected to the audio engine through a *connection*, and each connection can have only one endpoint connected to it.</span></span> <span data-ttu-id="01925-107">Depois que um ponto de extremidade é registrado, o mecanismo de áudio anexa o ponto de extremidade à conexão.</span><span class="sxs-lookup"><span data-stu-id="01925-107">After an endpoint is registered, the audio engine attaches the endpoint to the connection.</span></span>

<span data-ttu-id="01925-108">Cada objeto de ponto de extremidade deve implementar as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="01925-108">Each endpoint object must implement the following interfaces:</span></span>

-   <span data-ttu-id="01925-109">[**IAudioEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint) para habilitar o mecanismo de áudio para obter informações sobre o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="01925-109">[**IAudioEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint) to enable the audio engine to get information about the endpoint.</span></span>
-   <span data-ttu-id="01925-110">[**IAudioEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt) para obter informações sobre o buffer de dados antes de executar uma passagem de processamento e notificar o ponto de extremidade quando a passagem for concluída.</span><span class="sxs-lookup"><span data-stu-id="01925-110">[**IAudioEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt) to get information about the data buffer before performing a processing pass and notifying the endpoint when the pass is complete.</span></span>
-   <span data-ttu-id="01925-111">A interface [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt) ou [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) , dependendo se o objeto de ponto de extremidade está capturando ou renderizando áudio.</span><span class="sxs-lookup"><span data-stu-id="01925-111">Either the [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt) or [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) interface, depending on whether the endpoint object is capturing or rendering audio.</span></span>
-   [<span data-ttu-id="01925-112">**IAudioDeviceEndpoint**</span><span class="sxs-lookup"><span data-stu-id="01925-112">**IAudioDeviceEndpoint**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
-   [<span data-ttu-id="01925-113">**IAudioEndpointControl**</span><span class="sxs-lookup"><span data-stu-id="01925-113">**IAudioEndpointControl**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)

<span data-ttu-id="01925-114">O mecanismo de áudio usa essas interfaces para obter informações sobre os pontos de extremidade que estão anexados ao mecanismo.</span><span class="sxs-lookup"><span data-stu-id="01925-114">The audio engine uses these interfaces to get information about the endpoints that are attached to the engine.</span></span> <span data-ttu-id="01925-115">A implementação do ponto de extremidade deve fornecer o mecanismo para entregar ou consumir dados do mecanismo, conforme especificado por essas interfaces.</span><span class="sxs-lookup"><span data-stu-id="01925-115">The endpoint implementation must provide the mechanism to deliver data to or consume data from the engine as specified by these interfaces.</span></span>

<span data-ttu-id="01925-116">O Serviços de Área de Trabalho Remota API AudioEndpoint dá suporte a tipos de enumeração, interfaces e estruturas.</span><span class="sxs-lookup"><span data-stu-id="01925-116">The Remote Desktop Services AudioEndpoint API supports enumeration types, interfaces, and structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="01925-117">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="01925-117">In this section</span></span>

-   [<span data-ttu-id="01925-118">Serviços de Área de Trabalho Remota tipos de enumeração AudioEndpoint</span><span class="sxs-lookup"><span data-stu-id="01925-118">Remote Desktop Services AudioEndpoint Enumeration Types</span></span>](terminal-services-audioendpoint-enumeration-types.md)
-   [<span data-ttu-id="01925-119">Serviços de Área de Trabalho Remota funções AudioEndpoint</span><span class="sxs-lookup"><span data-stu-id="01925-119">Remote Desktop Services AudioEndpoint Functions</span></span>](remote-desktop-services-audioendpoint-functions.md)
-   [<span data-ttu-id="01925-120">Serviços de Área de Trabalho Remota interfaces AudioEndpoint</span><span class="sxs-lookup"><span data-stu-id="01925-120">Remote Desktop Services AudioEndpoint Interfaces</span></span>](terminal-services-audioendpoint-interfaces.md)
-   [<span data-ttu-id="01925-121">Serviços de Área de Trabalho Remota estruturas AudioEndpoint</span><span class="sxs-lookup"><span data-stu-id="01925-121">Remote Desktop Services AudioEndpoint Structures</span></span>](terminal-services-audioendpoint-structures.md)

## <a name="remarks"></a><span data-ttu-id="01925-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="01925-122">Remarks</span></span>

<span data-ttu-id="01925-123">O Serviços de Área de Trabalho Remota API AudioEndpoint é para uso em cenários de Área de Trabalho Remota; Não é para aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="01925-123">The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.</span></span>

 

 




