---
description: Notificação de remoção de dispositivo
ms.assetid: 0b96231a-f990-4c1c-8d00-cafeb3985ab3
title: Notificação de remoção de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c84fa280e0adbc1d0eec9043fbb2f1446487f0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103920096"
---
# <a name="device-removal-notification"></a><span data-ttu-id="d3585-103">Notificação de remoção de dispositivo</span><span class="sxs-lookup"><span data-stu-id="d3585-103">Device Removal Notification</span></span>

<span data-ttu-id="d3585-104">Se o usuário remover um dispositivo Plug and Play que o grafo estava usando, o Gerenciador de grafo de filtro posta um evento de [**\_ \_ perda de dispositivo EC**](ec-device-lost.md) .</span><span class="sxs-lookup"><span data-stu-id="d3585-104">If the user removes a Plug and Play device that the graph was using, the filter graph manager posts an [**EC\_DEVICE\_LOST**](ec-device-lost.md) event.</span></span> <span data-ttu-id="d3585-105">Se o dispositivo ficar disponível novamente, o Gerenciador de grafo de filtro publicará outro evento de **\_ \_ perda de dispositivo EC** .</span><span class="sxs-lookup"><span data-stu-id="d3585-105">If the device becomes available again, the filter graph manager posts another **EC\_DEVICE\_LOST** event.</span></span> <span data-ttu-id="d3585-106">No entanto, o estado anterior do filtro de captura não é mais válido.</span><span class="sxs-lookup"><span data-stu-id="d3585-106">However, the previous state of the capture filter is no longer valid.</span></span> <span data-ttu-id="d3585-107">O aplicativo deve recriar o grafo para usar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d3585-107">The application must rebuild the graph to use the device.</span></span>

<span data-ttu-id="d3585-108">O DirectShow não envia nenhum evento quando um novo dispositivo é conectado.</span><span class="sxs-lookup"><span data-stu-id="d3585-108">DirectShow does not send any event when a new device is plugged in.</span></span> <span data-ttu-id="d3585-109">Para saber quando um novo dispositivo está disponível, o aplicativo pode monitorar \_ as mensagens da janela do WM DEVICECHANGE.</span><span class="sxs-lookup"><span data-stu-id="d3585-109">To learn when a new device is available, the application can monitor WM\_DEVICECHANGE window messages.</span></span> <span data-ttu-id="d3585-110">Para obter mais informações, consulte "gerenciamento de dispositivo" na documentação do Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="d3585-110">For more information, see "Device Management" in the Platform SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3585-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d3585-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3585-112">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="d3585-112">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 



