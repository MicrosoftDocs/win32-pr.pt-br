---
title: Método IBasicDevice CanWakeDevices
description: Recupera um valor que indica se o dispositivo pode ser ativado.
ms.assetid: AAD0597C-AD33-40EE-A5DA-27AC66375D38
keywords:
- API de streaming de mídia do método CanWakeDevices
- API de streaming de mídia do método CanWakeDevices, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método CanWakeDevices
topic_type:
- apiref
api_name:
- IBasicDevice.CanWakeDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08a893ac880a426f604f2dc1c73173585e507cc0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006612"
---
# <a name="ibasicdevicecanwakedevices-method"></a>Método IBasicDevice:: CanWakeDevices

Recupera um valor que indica se o dispositivo pode ser ativado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CanWakeDevices(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do fora\]
</dt> <dd>

Recebe um ponteiro para um valor booliano que é **verdadeiro** se o dispositivo puder ser ativado.

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

 

 





