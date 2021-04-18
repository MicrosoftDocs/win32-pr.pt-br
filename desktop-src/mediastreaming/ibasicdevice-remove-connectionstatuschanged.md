---
title: Método de remove_ConnectionStatusChanged IBasicDevice
description: Cancela o registro de um manipulador de eventos para o evento ConnectionStatusChanged. | Método de remove_ConnectionStatusChanged IBasicDevice
ms.assetid: 577D9C50-486D-441A-A9FE-AF79D1FC2B52
keywords:
- API de streaming de mídia do método remove_ConnectionStatusChanged
- API de streaming de mídia do método remove_ConnectionStatusChanged, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método remove_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- IBasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c2bfa2886774ad637e66385a057c9d4e21efe0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105764492"
---
# <a name="ibasicdeviceremove_connectionstatuschanged-method"></a>Método IBasicDevice:: Remove \_ ConnectionStatusChanged

Cancela o registro de um manipulador de eventos para o evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*token* \[ do no\]
</dt> <dd>

Uma referência a um token obtido do método [**Add \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) quando o manipulador de eventos foi registrado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





