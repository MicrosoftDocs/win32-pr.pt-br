---
title: Método IDeviceController CachedDevices
description: Recupera uma coleção de ponteiros de interface IBasicDevice que representa a exibição armazenada em cache de todos os dispositivos DLNA que podem ser descobertos. | Método IDeviceController CachedDevices
ms.assetid: 94C2A7FF-5AF8-4F13-BBA5-54ED78C3BBF6
keywords:
- API de Streaming de Mídia do método CachedDevices
- Método CachedDevices API de Streaming de Mídia, interface IDeviceController
- API de Streaming de Mídia da interface IDeviceController, método CachedDevices
topic_type:
- apiref
api_name:
- IDeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9c624597fb88a45cc9ff91770f164e7c6e6e83ff5eb1b6369ded9d0fc1bbc225
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952636"
---
# <a name="idevicecontrollercacheddevices-method"></a>Método IDeviceController::CachedDevices

Recupera uma coleção de ponteiros de interface [**IBasicDevice**](ibasicdevice.md) que representa a exibição armazenada em cache de todos os dispositivos DLNA que podem ser descobertos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CachedDevices(
  [out] IVector< IBasicDevice > **value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recebe uma coleção enumerável de ponteiros de interface [**IBasicDevice.**](ibasicdevice.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDeviceController**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)
</dt> </dl>

 

