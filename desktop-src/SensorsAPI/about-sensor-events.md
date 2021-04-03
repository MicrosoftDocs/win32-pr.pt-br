---
description: A API do sensor pode fornecer notificações de eventos.
ms.assetid: 2400619c-ee9c-4662-ae57-6d4bc317e730
title: Sobre eventos de API do sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e941dca86d5b7ec3aa9922220c1232b10429f60a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829640"
---
# <a name="about-sensor-api-events"></a><span data-ttu-id="ba6db-103">Sobre eventos de API do sensor</span><span class="sxs-lookup"><span data-stu-id="ba6db-103">About Sensor API Events</span></span>

<span data-ttu-id="ba6db-104">A API do sensor pode fornecer notificações de eventos.</span><span class="sxs-lookup"><span data-stu-id="ba6db-104">The Sensor API can provide event notifications.</span></span>

<span data-ttu-id="ba6db-105">Ao se registrar para receber eventos, por meio de [**ISensor:: SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) ou [**ISensorManager:: SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink), você deve fornecer um ponteiro para uma interface de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="ba6db-105">When you register to receive events, through either [**ISensor::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) or [**ISensorManager::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink), you must provide a pointer to a callback interface.</span></span> <span data-ttu-id="ba6db-106">Você deve implementar os métodos da interface de retorno de chamada em seu código.</span><span class="sxs-lookup"><span data-stu-id="ba6db-106">You must implement the methods of the callback interface in your code.</span></span> <span data-ttu-id="ba6db-107">A API do sensor define as seguintes interfaces de retorno de chamada:</span><span class="sxs-lookup"><span data-stu-id="ba6db-107">The Sensor API defines the following callback interfaces:</span></span>

-   <span data-ttu-id="ba6db-108">[**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span><span class="sxs-lookup"><span data-stu-id="ba6db-108">[**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span></span> <span data-ttu-id="ba6db-109">Implemente essa interface para receber eventos de sensores.</span><span class="sxs-lookup"><span data-stu-id="ba6db-109">Implement this interface to receive events from sensors.</span></span> <span data-ttu-id="ba6db-110">Os sensores podem notificar seu aplicativo sobre novos dados, alterações no estado do sensor, desconexão do sensor e eventos personalizados definidos pelo fabricante do sensor.</span><span class="sxs-lookup"><span data-stu-id="ba6db-110">Sensors can notify your application about new data, changes in sensor state, sensor disconnection, and custom events defined by the sensor manufacturer.</span></span>
-   <span data-ttu-id="ba6db-111">[**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents).</span><span class="sxs-lookup"><span data-stu-id="ba6db-111">[**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents).</span></span> <span data-ttu-id="ba6db-112">Implemente essa interface para receber eventos do Gerenciador de sensores.</span><span class="sxs-lookup"><span data-stu-id="ba6db-112">Implement this interface to receive events from the sensor manager.</span></span> <span data-ttu-id="ba6db-113">O Gerenciador de sensor pode notificar seu aplicativo quando um sensor se conecta e, portanto, pode estar disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="ba6db-113">The sensor manager can notify your application when a sensor connects, and therefore may be available for use.</span></span>

<span data-ttu-id="ba6db-114">Você pode cancelar as notificações de eventos chamando [**SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) novamente, desta vez passando um valor **nulo** por meio do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ba6db-114">You can cancel event notifications by calling [**SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) again, this time passing a **NULL** value through the parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba6db-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ba6db-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba6db-116">Usando eventos de API do sensor</span><span class="sxs-lookup"><span data-stu-id="ba6db-116">Using Sensor API Events</span></span>](using-sensor-api-events.md)
</dt> </dl>

 

 
