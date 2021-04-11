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
ms.openlocfilehash: fdd39309774a61c4fd115ff09e16428101439a0b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172788"
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

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

