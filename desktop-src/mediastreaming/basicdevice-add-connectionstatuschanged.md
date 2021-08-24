---
title: Método de BasicDevice.add_ConnectionStatusChanged
description: Registra um manipulador de eventos para o evento ConnectionStatusChanged. | Método de BasicDevice.add_ConnectionStatusChanged
ms.assetid: FFAA0981-508C-4300-9CA9-24C6AFC1183D
keywords:
- API de streaming de mídia do método add_ConnectionStatusChanged
- API de streaming de mídia do método add_ConnectionStatusChanged, interface BasicDevice
- API de streaming de mídia da interface BasicDevice, método add_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- BasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a416770a0ea3a4d317a2308fc9f5c9d940e89900aabbc7651ceb93b789454338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462256"
---
# <a name="basicdeviceadd_connectionstatuschanged-method"></a>BasicDevice. Adicione o \_ método ConnectionStatusChanged

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

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Para cancelar o registro do manipulador de eventos que foi registrado por esse método, passe o valor do *token* para o método [**Remove \_ ConnectionStatusChanged**](basicdevice-remove-connectionstatuschanged.md) .

## <a name="see-also"></a>Confira também

<dl> <dt>

[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

