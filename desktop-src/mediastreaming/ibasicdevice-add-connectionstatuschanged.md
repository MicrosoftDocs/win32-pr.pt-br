---
title: Método add_ConnectionStatusChanged IBasicDevice
description: Registra um manipulador de eventos para o evento ConnectionStatusChanged. | Método add_ConnectionStatusChanged IBasicDevice
ms.assetid: 1A4CCEFE-B6B6-4AFD-9296-EE923B9EF399
keywords:
- ADD_CONNECTIONSTATUSCHANGED API de Streaming de Mídia
- add_ConnectionStatusChanged API de Streaming de Mídia, interface IBasicDevice
- Interface IBasicDevice API de Streaming de Mídia , add_ConnectionStatusChanged método
topic_type:
- apiref
api_name:
- IBasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55e90ea1f90ccd5b1e141b0e4071213abfe6f4a05a85d3c0d4ced505e1b0f164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952656"
---
# <a name="ibasicdeviceadd_connectionstatuschanged-method"></a>Método IBasicDevice::add \_ ConnectionStatusChanged

Registra um manipulador de eventos para o [**evento ConnectionStatusChanged.**](connectionstatuschanged.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT add_ConnectionStatusChanged(
  [in]          ConnectionStatusHandler *handler,
  [out, retval] EventRegistrationToken  *token
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*manipulador* \[ Em\]
</dt> <dd>

Uma [**função de manipulador de eventos ConnectionStatusHandler.**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))

</dd> <dt>

*token* \[ out, retval\]
</dt> <dd>

Referência a um token que pode ser usado para não fazer o registro do manipulador de eventos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Para registrar o manipulador de eventos registrado por esse método, passe o valor *do token* para o método [**remove \_ ConnectionStatusChanged.**](ibasicdevice-remove-connectionstatuschanged.md)

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

