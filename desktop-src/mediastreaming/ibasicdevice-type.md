---
title: Método IBasicDevice Type
description: Recupera um valor de enumeração que indica o tipo de dispositivo do dispositivo DLNA.
ms.assetid: D9FB3A02-7796-4ACB-B7D3-D171D1D9B77F
keywords:
- API de Streaming de Mídia do método de tipo
- Método de tipo API de Streaming de Mídia, interface IBasicDevice
- API de Streaming de Mídia da interface IBasicDevice, método type
topic_type:
- apiref
api_name:
- IBasicDevice.Type
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 433b255615a3fb57d59589b09a4a8b3e0f4cec5c02115bc737041d1fd94a197f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100620"
---
# <a name="ibasicdevicetype-method"></a>Método IBasicDevice::Type

Recupera um valor de enumeração que indica o tipo de dispositivo do dispositivo DLNA.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Type(
  [out] DeviceTypes *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recebe um ponteiro para um [**valor DeviceTypes.**](devicetypes.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





