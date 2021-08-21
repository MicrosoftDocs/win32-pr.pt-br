---
title: Método de BasicDevice.remove_ConnectionStatusChanged
description: Cancela o registro de um manipulador de eventos para o evento ConnectionStatusChanged. | Método de BasicDevice.remove_ConnectionStatusChanged
ms.assetid: 537CA8FE-D2E1-4CC7-BB80-FBE36A2D4A1E
keywords:
- API de streaming de mídia do método remove_ConnectionStatusChanged
- API de streaming de mídia do método remove_ConnectionStatusChanged, interface BasicDevice
- API de streaming de mídia da interface BasicDevice, método remove_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- BasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89057195c23aa917c7338a8abb740817bb6af7896261cf1d31bcb37d5d5d5ab8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972495"
---
# <a name="basicdeviceremove_connectionstatuschanged-method"></a>Método BasicDevice. Remove \_ ConnectionStatusChanged

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

Uma referência a um token obtido do método [**Add \_ ConnectionStatusChanged**](basicdevice-add-connectionstatuschanged.md) quando o manipulador de eventos foi registrado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

