---
description: O objeto sensor representa um sensor específico.
ms.assetid: b969a153-d957-4323-bafe-6f8d62b0a627
title: O objeto sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6034c008edf75b16a8156ab53ff66a418261d965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754115"
---
# <a name="the-sensor-object"></a><span data-ttu-id="00b5f-103">O objeto sensor</span><span class="sxs-lookup"><span data-stu-id="00b5f-103">The Sensor Object</span></span>

<span data-ttu-id="00b5f-104">O objeto sensor representa um sensor específico.</span><span class="sxs-lookup"><span data-stu-id="00b5f-104">The sensor object represents a particular sensor.</span></span>

<span data-ttu-id="00b5f-105">A API do sensor representa cada sensor como um objeto de sensor.</span><span class="sxs-lookup"><span data-stu-id="00b5f-105">The Sensor API represents each sensor as a sensor object.</span></span> <span data-ttu-id="00b5f-106">Você pode trabalhar com um objeto de sensor específico por meio de sua interface [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) .</span><span class="sxs-lookup"><span data-stu-id="00b5f-106">You can work with a particular sensor object through its [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) interface.</span></span> <span data-ttu-id="00b5f-107">Essa interface permite que você:</span><span class="sxs-lookup"><span data-stu-id="00b5f-107">This interface enables you to:</span></span>

-   <span data-ttu-id="00b5f-108">Recupere metadados sobre o sensor, como sua ID, tipo ou nome amigável.</span><span class="sxs-lookup"><span data-stu-id="00b5f-108">Retrieve metadata about the sensor, such as its ID, type, or friendly name.</span></span>
-   <span data-ttu-id="00b5f-109">Recupere informações sobre os dados específicos que o sensor pode fornecer.</span><span class="sxs-lookup"><span data-stu-id="00b5f-109">Retrieve information about the specific data the sensor can provide.</span></span>
-   <span data-ttu-id="00b5f-110">Recupere os dados de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="00b5f-110">Retrieve the data, synchronously.</span></span>
-   <span data-ttu-id="00b5f-111">Recuperar informações de estado, como se o sensor está pronto.</span><span class="sxs-lookup"><span data-stu-id="00b5f-111">Retrieve state information, such as whether the sensor is ready.</span></span>
-   <span data-ttu-id="00b5f-112">Especifique quais eventos seu programa receberá.</span><span class="sxs-lookup"><span data-stu-id="00b5f-112">Specify which events your program will receive.</span></span>
-   <span data-ttu-id="00b5f-113">Especifique a interface de retorno de chamada que a API do sensor pode usar para fornecer ao seu programa notificações de eventos.</span><span class="sxs-lookup"><span data-stu-id="00b5f-113">Specify the callback interface that the Sensor API can use to provide your program with event notifications.</span></span>

 

 



