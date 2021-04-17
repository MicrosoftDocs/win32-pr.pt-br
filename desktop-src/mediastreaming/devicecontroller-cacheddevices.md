---
title: Método DeviceController. CachedDevices
description: Recupera uma coleção de ponteiros de interface IBasicDevice que representa a exibição armazenada em cache de todos os dispositivos DLNA detectáveis. | Método DeviceController. CachedDevices
ms.assetid: 89CFA4BB-EDA8-461A-A3A0-A84CBDA99EA4
keywords:
- API de streaming de mídia do método CachedDevices
- API de streaming de mídia do método CachedDevices, interface DeviceController
- API de streaming de mídia da interface DeviceController, método CachedDevices
topic_type:
- apiref
api_name:
- DeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0bb39e03a9788e0c444f682b61d39fc1c65781b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105785185"
---
# <a name="devicecontrollercacheddevices-method"></a>Método DeviceController. CachedDevices

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



| Código de retorno                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**DeviceController**](/previous-versions/windows/desktop/legacy/hh828842(v=vs.85))
</dt> </dl>

 

