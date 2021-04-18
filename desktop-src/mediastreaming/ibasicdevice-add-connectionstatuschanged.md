---
title: Método de add_ConnectionStatusChanged IBasicDevice
description: Registra um manipulador de eventos para o evento ConnectionStatusChanged. | Método de add_ConnectionStatusChanged IBasicDevice
ms.assetid: 1A4CCEFE-B6B6-4AFD-9296-EE923B9EF399
keywords:
- API de streaming de mídia do método add_ConnectionStatusChanged
- API de streaming de mídia do método add_ConnectionStatusChanged, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método add_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- IBasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0028e6f3dad1670974178b0f07a59f74dffdc06f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105781491"
---
# <a name="ibasicdeviceadd_connectionstatuschanged-method"></a>Método IBasicDevice:: Add \_ ConnectionStatusChanged

Registra um manipulador de eventos para o evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT add_ConnectionStatusChanged(
  [in]          ConnectionStatusHandler *handler,
  [out, retval] EventRegistrationToken  *token
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*manipulador* \[ no\]
</dt> <dd>

Uma função de manipulador de eventos [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) .

</dd> <dt>

*token* \[ do out, retval\]
</dt> <dd>

Referência a um token que pode ser usado para cancelar o registro do manipulador de eventos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Para cancelar o registro do manipulador de eventos que foi registrado por esse método, passe o valor do *token* para o método [**Remove \_ ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) .

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

