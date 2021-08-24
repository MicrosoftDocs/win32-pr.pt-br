---
title: Método CanWakeDevices de IBasicDevice
description: Recupera um valor que indica se o dispositivo pode ser a wake.
ms.assetid: AAD0597C-AD33-40EE-A5DA-27AC66375D38
keywords:
- API de Streaming de Mídia do método CanWakeDevices
- API de Streaming de Mídia do método CanWakeDevices, interface IBasicDevice
- API de Streaming de Mídia da interface IBasicDevice , método CanWakeDevices
topic_type:
- apiref
api_name:
- IBasicDevice.CanWakeDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3ebd0cfe9bf773d78297454d4a7643a74c3d6ea23aea01eeb54cd5c014ce73e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847666"
---
# <a name="ibasicdevicecanwakedevices-method"></a>Método IBasicDevice::CanWakeDevices

Recupera um valor que indica se o dispositivo pode ser a wake.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CanWakeDevices(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recebe um ponteiro para um valor booliana que é **True se** o dispositivo puder ser a wake.

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

 

 





