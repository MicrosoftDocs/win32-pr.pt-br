---
title: Método remove_ConnectionStatusChanged IBasicDevice
description: Anuidade o registro de um manipulador de eventos para o evento ConnectionStatusChanged. | Método remove_ConnectionStatusChanged IBasicDevice
ms.assetid: 577D9C50-486D-441A-A9FE-AF79D1FC2B52
keywords:
- REMOVE_CONNECTIONSTATUSCHANGED API de Streaming de Mídia
- remove_ConnectionStatusChanged API de Streaming de Mídia, interface IBasicDevice
- Interface IBasicDevice API de Streaming de Mídia , remove_ConnectionStatusChanged método
topic_type:
- apiref
api_name:
- IBasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 35b2f08b6df25f57d77f5c3677a4c6499370d9472202b6808073c5a75d1e2c34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599796"
---
# <a name="ibasicdeviceremove_connectionstatuschanged-method"></a>Método IBasicDevice::remove \_ ConnectionStatusChanged

Anuidade o registro de um manipulador de eventos [**para o evento ConnectionStatusChanged.**](connectionstatuschanged.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*token* \[ Em\]
</dt> <dd>

Uma referência a um token obtido do [**método \_ add ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) quando o manipulador de eventos foi registrado.

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

 

 





