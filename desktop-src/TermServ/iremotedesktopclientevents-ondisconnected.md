---
title: Método OnDisconnected IRemoteDesktopClientEvents
description: Chamado quando o controle de cliente foi desconectado de uma sessão remota.
ms.assetid: EA26B530-0AA8-49D6-8E3C-E53179FC5104
ms.tgt_platform: multiple
keywords:
- Método OnDisconnected Serviços de Área de Trabalho Remota
- Método OnDisconnected Serviços de Área de Trabalho Remota interface , IRemoteDesktopClientEvents
- Interface IRemoteDesktopClientEvents Serviços de Área de Trabalho Remota , método OnDisconnected
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnDisconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e93ebf7c85e4015539cbbcc15723cdfed9c7d181741925c1a97c93ccc4326eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124896"
---
# <a name="iremotedesktopclienteventsondisconnected-method"></a>Método IRemoteDesktopClientEvents::OnDisconnected

Chamado quando o controle de cliente foi desconectado de uma sessão remota.

## <a name="syntax"></a>Sintaxe


```C++
void OnDisconnected(
  [in] long disconnectReason,
  [in] long ExtendedDisconnectReason,
  [in] BSTR disconnectErrorMessage
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*disconnectReason* \[ Em\]
</dt> <dd>

O motivo do evento de desconexão.

</dd> <dt>

*ExtendedDisconnectReason* \[ Em\]
</dt> <dd>

Informações estendidas para o evento de desconexão.

</dd> <dt>

*disconnectErrorMessage* \[ Em\]
</dt> <dd>

A mensagem de erro para o evento de desconexão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                           |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                 |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents é definido como 079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





