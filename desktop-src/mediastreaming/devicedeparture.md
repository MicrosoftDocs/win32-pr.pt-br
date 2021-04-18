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
# <a name="devicedeparture-event"></a>Evento DeviceDeparture

Ocorre quando um novo dispositivo é removido da lista de dispositivos retornada pelo método [**CachedDevices**](idevicecontroller-cacheddevices.md) .

## <a name="syntax"></a>Sintaxe


```C++
void DeviceDeparture();
```



## <a name="parameters"></a>Parâmetros

Este evento não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Para lidar com notificações desse evento, registre uma função de manipulador de eventos [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) usando o método [**Add \_ DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicedeparture) . Para cancelar o registro do manipulador de eventos, use o método [**Remove \_ DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicedeparture) .

 

 