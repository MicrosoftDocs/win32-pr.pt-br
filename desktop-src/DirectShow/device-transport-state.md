---
description: Estado de transporte do dispositivo
ms.assetid: 15edded0-207c-41e8-81fe-deb6335045eb
title: Estado de transporte do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05f52ea846c79be6cb2d011b635da358f7ecd0a2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370338"
---
# <a name="device-transport-state"></a><span data-ttu-id="dcbee-103">Estado de transporte do dispositivo</span><span class="sxs-lookup"><span data-stu-id="dcbee-103">Device Transport State</span></span>

<span data-ttu-id="dcbee-104">Para recuperar o estado atual do dispositivo, como reproduzir, pausar ou parar, chame o método de [**\_ modo IAMExtTransport:: Get**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-get_mode) .</span><span class="sxs-lookup"><span data-stu-id="dcbee-104">To retrieve the current state of the device, such as play, pause, or stop, call the [**IAMExtTransport::get\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-get_mode) method.</span></span> <span data-ttu-id="dcbee-105">O método recupera uma constante que indica o estado do dispositivo:</span><span class="sxs-lookup"><span data-stu-id="dcbee-105">The method retrieves a constant that indicates the device state:</span></span>



| <span data-ttu-id="dcbee-106">Valor</span><span class="sxs-lookup"><span data-stu-id="dcbee-106">Value</span></span>                    | <span data-ttu-id="dcbee-107">Estado do Dispositivo</span><span class="sxs-lookup"><span data-stu-id="dcbee-107">Device State</span></span> |
|--------------------------|--------------|
| <span data-ttu-id="dcbee-108">\_reproduzir modo \_ Ed</span><span class="sxs-lookup"><span data-stu-id="dcbee-108">ED\_MODE\_PLAY</span></span>           | <span data-ttu-id="dcbee-109">Reproduzir</span><span class="sxs-lookup"><span data-stu-id="dcbee-109">Play</span></span>         |
| <span data-ttu-id="dcbee-110">\_parada do modo Ed \_</span><span class="sxs-lookup"><span data-stu-id="dcbee-110">ED\_MODE\_STOP</span></span>           | <span data-ttu-id="dcbee-111">Stop</span><span class="sxs-lookup"><span data-stu-id="dcbee-111">Stop</span></span>         |
| <span data-ttu-id="dcbee-112">\_congelamento do modo Ed \_</span><span class="sxs-lookup"><span data-stu-id="dcbee-112">ED\_MODE\_FREEZE</span></span>         | <span data-ttu-id="dcbee-113">Pausar</span><span class="sxs-lookup"><span data-stu-id="dcbee-113">Pause</span></span>        |
| <span data-ttu-id="dcbee-114">\_modo Ed \_ FF</span><span class="sxs-lookup"><span data-stu-id="dcbee-114">ED\_MODE\_FF</span></span>             | <span data-ttu-id="dcbee-115">Avanço rápido</span><span class="sxs-lookup"><span data-stu-id="dcbee-115">Fast-forward</span></span> |
| <span data-ttu-id="dcbee-116">\_modo Ed \_ Rebo</span><span class="sxs-lookup"><span data-stu-id="dcbee-116">ED\_MODE\_REW</span></span>            | <span data-ttu-id="dcbee-117">Rewind</span><span class="sxs-lookup"><span data-stu-id="dcbee-117">Rewind</span></span>       |
| <span data-ttu-id="dcbee-118">\_registro de modo Ed \_</span><span class="sxs-lookup"><span data-stu-id="dcbee-118">ED\_MODE\_RECORD</span></span>         | <span data-ttu-id="dcbee-119">Record</span><span class="sxs-lookup"><span data-stu-id="dcbee-119">Record</span></span>       |
| <span data-ttu-id="dcbee-120">\_congelamento de \_ registro do modo Ed \_</span><span class="sxs-lookup"><span data-stu-id="dcbee-120">ED\_MODE\_RECORD\_FREEZE</span></span> | <span data-ttu-id="dcbee-121">Gravar-pausar</span><span class="sxs-lookup"><span data-stu-id="dcbee-121">Record-pause</span></span> |



 

<span data-ttu-id="dcbee-122">O código a seguir verifica o estado do dispositivo:</span><span class="sxs-lookup"><span data-stu-id="dcbee-122">The following code checks the device state:</span></span>


```C++
LONG State;
hr = MyDevCap.pTransport->get_Mode(&State);
if (SUCCEEDED(hr))
{
    switch (State)
    {
        case ED_MODE_PLAY:
        // ... 
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="dcbee-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dcbee-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcbee-124">Controlando uma camcorder DV</span><span class="sxs-lookup"><span data-stu-id="dcbee-124">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



