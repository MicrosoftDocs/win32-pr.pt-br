---
title: Método IRemoteDesktopClientEvents OnAutoReconnecting
description: Chamado quando o controle de cliente tenta restabelecer automaticamente uma conexão com uma sessão remota.
ms.assetid: 299408A9-ED14-42F4-B324-AF4C86FEDABE
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnAutoReconnecting
- Método OnAutoReconnecting Serviços de Área de Trabalho Remota, interface IRemoteDesktopClientEvents
- Serviços de Área de Trabalho Remota de interface IRemoteDesktopClientEvents, método OnAutoReconnecting
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnAutoReconnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74c37919384727fdf51aad004349478798a3ffd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499784"
---
# <a name="iremotedesktopclienteventsonautoreconnecting-method"></a>Método IRemoteDesktopClientEvents:: OnAutoReconnecting

Chamado quando o controle de cliente tenta restabelecer automaticamente uma conexão com uma sessão remota.

## <a name="syntax"></a>Sintaxe


```C++
void OnAutoReconnecting(
  [in] long         disconnectReason,
  [in] long         ExtendedDisconnectReason,
  [in] BSTR         disconnectErrorMessage,
  [in] VARIANT_BOOL networkAvailable,
  [in] long         attemptCount,
  [in] long         maxAttemptCount
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

</dd> <dt>

*NetworkAvailable* \[ no\]
</dt> <dd>

Se a rede está disponível.

</dd> <dt>

*attemptCount* \[ no\]
</dt> <dd>

Que tente isso.

</dd> <dt>

*maxAttemptCount* \[ no\]
</dt> <dd>

O número máximo de tentativas de reconexão será executado.

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

 

 





