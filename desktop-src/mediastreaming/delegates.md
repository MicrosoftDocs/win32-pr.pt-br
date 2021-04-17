---
title: Delegados
description: A API de streaming de mídia fornece as seguintes funções de manipulador de eventos.
ms.assetid: CDE7B829-D0D1-479D-9B35-4445E711AF58
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23fbf0f44a0822fd0c8914833b0696fcb9aacad
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104499029"
---
# <a name="delegates"></a><span data-ttu-id="9d565-103">Delegados</span><span class="sxs-lookup"><span data-stu-id="9d565-103">Delegates</span></span>

<span data-ttu-id="9d565-104">A [API de streaming de mídia](media-streaming-api-portal.md) fornece as seguintes funções de manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="9d565-104">The [Media Streaming API](media-streaming-api-portal.md) provides the following event handler functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9d565-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="9d565-105">In this section</span></span>



| <span data-ttu-id="9d565-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="9d565-106">Topic</span></span>                                                                                   | <span data-ttu-id="9d565-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d565-107">Description</span></span>                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d565-108">[**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9d565-108">[**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))</span></span><br/>                   | <span data-ttu-id="9d565-109">Representa a função que manipulará o evento [**ConnectionStatusChanged**](connectionstatuschanged.md) , que notifica o cliente sobre as alterações no status de conexão de rede do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9d565-109">Represents the function that will handle the [**ConnectionStatusChanged**](connectionstatuschanged.md) event which notifies the client of changes in the device s network connection status.</span></span><br/>               |
| <span data-ttu-id="9d565-110">[**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9d565-110">[**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85))</span></span><br/>       | <span data-ttu-id="9d565-111">Representa a função que manipulará os eventos [**DeviceArrival**](devicearrival.md) e [**DeviceDeparture**](devicedeparture.md) que notificam o cliente sobre as alterações na lista de dispositivos armazenados em cache.</span><span class="sxs-lookup"><span data-stu-id="9d565-111">Represents the function that will handle the [**DeviceArrival**](devicearrival.md) and [**DeviceDeparture**](devicedeparture.md) events which notify the client of changes in the list of cached devices.</span></span><br/> |
| <span data-ttu-id="9d565-112">[**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9d565-112">[**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85))</span></span><br/> | <span data-ttu-id="9d565-113">Representa a função que manipulará o evento [**RenderingParametersUpdate**](renderingparametersupdate.md) , que notifica o cliente sobre uma atualização para qualquer um dos parâmetros de controle de RENDERIZAÇÃO de DMR s.</span><span class="sxs-lookup"><span data-stu-id="9d565-113">Represents the function that will handle the [**RenderingParametersUpdate**](renderingparametersupdate.md) event which notifies the client of an update to any of the DMR s rendering control parameters.</span></span><br/>  |
| <span data-ttu-id="9d565-114">[**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9d565-114">[**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85))</span></span><br/> | <span data-ttu-id="9d565-115">Representa a função que manipulará o evento [**TransportParametersUpdate**](transportparametersupdate.md) , que notifica o cliente sobre uma atualização para qualquer um dos parâmetros de transporte de DMR.</span><span class="sxs-lookup"><span data-stu-id="9d565-115">Represents the function that will handle the [**TransportParametersUpdate**](transportparametersupdate.md) event which notifies the client of an update to any of the DMR s transport parameters.</span></span><br/>          |



 

 

