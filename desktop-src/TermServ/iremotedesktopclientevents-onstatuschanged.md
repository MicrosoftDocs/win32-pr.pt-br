---
title: Método onstatuschanged do IRemoteDesktopClientEvents (Locationapi. h)
description: Chamado quando o controle de cliente atualizou seu status.
ms.assetid: AAFBDC9E-C8B5-4924-AA69-82EF09996AF7
ms.tgt_platform: multiple
keywords:
- Método onstatuschanged Serviços de Área de Trabalho Remota
- Método onstatuschanged Serviços de Área de Trabalho Remota, interface IRemoteDesktopClientEvents
- Interface IRemoteDesktopClientEvents Serviços de Área de Trabalho Remota, método onstatuschanged
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b17e42e75072033f952c7ef790365d6a363a5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455867"
---
# <a name="iremotedesktopclienteventsonstatuschanged-method"></a>Método IRemoteDesktopClientEvents:: onstatuschanged

Chamado quando o controle de cliente atualizou seu status.

## <a name="syntax"></a>Sintaxe


```C++
void OnStatusChanged(
   long statusCode,
   BSTR statusMessage
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*statusCode* 
</dt> <dd>

O novo código de status.

</dd> <dt>

*statusMessage* 
</dt> <dd>

O texto da mensagem de status.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                           |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>Locationapi. h</dt> </dl>       |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents é definido como 079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





