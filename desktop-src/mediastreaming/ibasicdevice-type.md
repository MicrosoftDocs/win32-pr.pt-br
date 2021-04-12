---
title: Método de tipo IBasicDevice
description: Recupera um valor de enumeração que indica o tipo de dispositivo do dispositivo DLNA.
ms.assetid: D9FB3A02-7796-4ACB-B7D3-D171D1D9B77F
keywords:
- API de streaming de mídia do método de tipo
- API de streaming de mídia do método de tipo, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método Type
topic_type:
- apiref
api_name:
- IBasicDevice.Type
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a69f0671c82363ff61179c0120b3db8f6e755de9
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2020
ms.locfileid: "104366896"
---
# <a name="ibasicdevicetype-method"></a>Método IBasicDevice:: Type

Recupera um valor de enumeração que indica o tipo de dispositivo do dispositivo DLNA.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Type(
  [out] DeviceTypes *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do fora\]
</dt> <dd>

Recebe um ponteiro para um valor [**DeviceTypes**](devicetypes.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





