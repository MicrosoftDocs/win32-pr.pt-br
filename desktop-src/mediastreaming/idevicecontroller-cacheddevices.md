---
title: Método IDeviceController CachedDevices
description: Recupera uma coleção de ponteiros de interface IBasicDevice que representa a exibição armazenada em cache de todos os dispositivos DLNA detectáveis. | Método IDeviceController CachedDevices
ms.assetid: 94C2A7FF-5AF8-4F13-BBA5-54ED78C3BBF6
keywords:
- API de streaming de mídia do método CachedDevices
- API de streaming de mídia do método CachedDevices, interface IDeviceController
- API de streaming de mídia da interface IDeviceController, método CachedDevices
topic_type:
- apiref
api_name:
- IDeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69be1faea277fa8999ae5ddf3658aaa61a1116b9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930512"
---
# <a name="idevicecontrollercacheddevices-method"></a>Método IDeviceController:: CachedDevices

Recupera uma coleção de ponteiros de interface [**IBasicDevice**](ibasicdevice.md) que representa a exibição armazenada em cache de todos os dispositivos DLNA detectáveis.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CachedDevices(
  [out] IVector< IBasicDevice > **value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do fora\]
</dt> <dd>

Recebe uma coleção enumerável de ponteiros de interface [**IBasicDevice**](ibasicdevice.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDeviceController**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)
</dt> </dl>

 

