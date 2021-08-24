---
title: Evento DeviceDeparture
description: Ocorre quando um novo dispositivo é removido da lista de dispositivos retornados pelo método CachedDevices.
ms.assetid: 10451878-e685-4042-9f92-ba3a408c4da0
keywords:
- API de Streaming de Mídia do evento DeviceDeparture
topic_type:
- apiref
api_name:
- DeviceDeparture
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496fa0fcae3cba51228b37b5f06eb9b06c416322aad22f77be542274088eae32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712946"
---
# <a name="devicedeparture-event"></a>Evento DeviceDeparture

Ocorre quando um novo dispositivo é removido da lista de dispositivos retornados pelo [**método CachedDevices.**](idevicecontroller-cacheddevices.md)

## <a name="syntax"></a>Sintaxe


```C++
void DeviceDeparture();
```



## <a name="parameters"></a>Parâmetros

Esse evento não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Para manipular notificações desse evento, registre uma função de manipulador de eventos [**DeviceControllerHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) usando o [**método add \_ DeviceDeparture.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicedeparture) Para remover o registro do manipulador de eventos, use o [**método \_ remove DeviceDeparture.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicedeparture)

 

 