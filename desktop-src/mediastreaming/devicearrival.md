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
ms.openlocfilehash: ed65c2b1c37eb91f9bf0a0c060fb76b85cd1f5b3d06b6ff1ab795ec89a0db6bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721206"
---
# <a name="devicearrival-event"></a>Evento DeviceArrival

Ocorre quando um novo dispositivo é adicionado à lista de dispositivos retornada pelo método [**CachedDevices**](idevicecontroller-cacheddevices.md) .

## <a name="syntax"></a>Sintaxe


```C++
void DeviceArrival();
```



## <a name="parameters"></a>Parâmetros

Este evento não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Para lidar com notificações desse evento, registre uma função de manipulador de eventos [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) usando o método [**Add \_ DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicearrival) . Para cancelar o registro do manipulador de eventos, use o método [**Remove \_ DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicearrival) .

 

 