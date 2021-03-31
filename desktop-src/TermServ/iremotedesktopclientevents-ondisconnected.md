---
title: Método OnDisconnect IRemoteDesktopClientEvents
description: Chamado quando o controle de cliente foi desconectado de uma sessão remota.
ms.assetid: EA26B530-0AA8-49D6-8E3C-E53179FC5104
ms.tgt_platform: multiple
keywords:
- Método OnDisconnect Serviços de Área de Trabalho Remota
- Método OnDisconnect Serviços de Área de Trabalho Remota, interface IRemoteDesktopClientEvents
- Serviços de Área de Trabalho Remota de interface IRemoteDesktopClientEvents, método ondisconnectd
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
ms.openlocfilehash: 4bd59b03fe9cb23309d53773289291c8a791935a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644870"
---
# <a name="iremotedesktopclienteventsondisconnected-method"></a>Método IRemoteDesktopClientEvents:: OnDisconnect

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

*disconnectReason* \[ no\]
</dt> <dd>

O motivo para o evento de desconexão.

</dd> <dt>

*ExtendedDisconnectReason* \[ no\]
</dt> <dd>

Informações estendidas para o evento de desconexão.

</dd> <dt>

*disconnectErrorMessage* \[ no\]
</dt> <dd>

A mensagem de erro para o evento de desconexão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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

 

 





