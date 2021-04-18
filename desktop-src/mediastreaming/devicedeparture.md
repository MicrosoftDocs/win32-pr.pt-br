---
title: Evento DeviceDeparture
description: Ocorre quando um novo dispositivo é removido da lista de dispositivos retornada pelo método CachedDevices.
ms.assetid: 10451878-e685-4042-9f92-ba3a408c4da0
keywords:
- API de streaming de mídia de evento DeviceDeparture
topic_type:
- apiref
api_name:
- DeviceDeparture
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e225afcbe8b373b22584eaa3d9fcb09e1eff29c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105815445"
---
# <a name="devicedeparture-event"></a><span data-ttu-id="73498-104">Evento DeviceDeparture</span><span class="sxs-lookup"><span data-stu-id="73498-104">DeviceDeparture event</span></span>

<span data-ttu-id="73498-105">Ocorre quando um novo dispositivo é removido da lista de dispositivos retornada pelo método [**CachedDevices**](idevicecontroller-cacheddevices.md) .</span><span class="sxs-lookup"><span data-stu-id="73498-105">Occurs when a new device is removed from the list of devices returned by the [**CachedDevices**](idevicecontroller-cacheddevices.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="73498-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73498-106">Syntax</span></span>


```C++
void DeviceDeparture();
```



## <a name="parameters"></a><span data-ttu-id="73498-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73498-107">Parameters</span></span>

<span data-ttu-id="73498-108">Este evento não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="73498-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="73498-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="73498-109">Return value</span></span>

<span data-ttu-id="73498-110">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="73498-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="73498-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="73498-111">Remarks</span></span>

<span data-ttu-id="73498-112">Para lidar com notificações desse evento, registre uma função de manipulador de eventos [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) usando o método [**Add \_ DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicedeparture) .</span><span class="sxs-lookup"><span data-stu-id="73498-112">To handle notifications from this event, register a [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) event handler function using the [**add\_DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicedeparture) method.</span></span> <span data-ttu-id="73498-113">Para cancelar o registro do manipulador de eventos, use o método [**Remove \_ DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicedeparture) .</span><span class="sxs-lookup"><span data-stu-id="73498-113">To unregister the event handler, use the [**remove\_DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicedeparture) method.</span></span>

 

 