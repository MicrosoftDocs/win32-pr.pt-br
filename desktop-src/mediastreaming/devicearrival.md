---
title: Evento DeviceArrival
description: Ocorre quando um novo dispositivo é adicionado à lista de dispositivos retornada pelo método CachedDevices.
ms.assetid: C7CB49AE-C05F-4A2A-8A30-4B4BB7C7D9D2
keywords:
- API de streaming de mídia de evento DeviceArrival
topic_type:
- apiref
api_name:
- DeviceArrival
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79fbdd68ae6c77c6a0f3e7bbd3cf976b5d056987
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640623"
---
# <a name="devicearrival-event"></a><span data-ttu-id="4a2b5-104">Evento DeviceArrival</span><span class="sxs-lookup"><span data-stu-id="4a2b5-104">DeviceArrival event</span></span>

<span data-ttu-id="4a2b5-105">Ocorre quando um novo dispositivo é adicionado à lista de dispositivos retornada pelo método [**CachedDevices**](idevicecontroller-cacheddevices.md) .</span><span class="sxs-lookup"><span data-stu-id="4a2b5-105">Occurs when a new device is added to the list of devices returned by the [**CachedDevices**](idevicecontroller-cacheddevices.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a2b5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a2b5-106">Syntax</span></span>


```C++
void DeviceArrival();
```



## <a name="parameters"></a><span data-ttu-id="4a2b5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a2b5-107">Parameters</span></span>

<span data-ttu-id="4a2b5-108">Este evento não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4a2b5-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4a2b5-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4a2b5-109">Return value</span></span>

<span data-ttu-id="4a2b5-110">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4a2b5-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a2b5-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a2b5-111">Remarks</span></span>

<span data-ttu-id="4a2b5-112">Para lidar com notificações desse evento, registre uma função de manipulador de eventos [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) usando o método [**Add \_ DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicearrival) .</span><span class="sxs-lookup"><span data-stu-id="4a2b5-112">To handle notifications from this event, register a [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) event handler function using the [**add\_DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicearrival) method.</span></span> <span data-ttu-id="4a2b5-113">Para cancelar o registro do manipulador de eventos, use o método [**Remove \_ DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicearrival) .</span><span class="sxs-lookup"><span data-stu-id="4a2b5-113">To unregister the event handler, use the [**remove\_DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicearrival) method.</span></span>

 

 