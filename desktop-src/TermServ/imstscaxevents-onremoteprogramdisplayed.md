---
title: Método IMsTscAxEvents OnRemoteProgramDisplayed
description: Chamado quando um programa do RemoteApp é exibido.
ms.assetid: 24f5ea52-0c13-4024-9448-5c2c1896ca8b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnRemoteProgramDisplayed
- Método OnRemoteProgramDisplayed Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnRemoteProgramDisplayed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteProgramDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df50f9a536b367b203f395d9c856562b8967d8a5830704a2e9bbb4c69152f202
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058814"
---
# <a name="imstscaxeventsonremoteprogramdisplayed-method"></a>Método IMsTscAxEvents:: OnRemoteProgramDisplayed

Chamado quando um programa do RemoteApp é exibido.

## <a name="syntax"></a>Sintaxe


```C++
VOID OnRemoteProgramDisplayed(
  [in] VARIANT_BOOL vbDisplayed,
  [in] ULONG        uDisplayInformation
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*vbDisplayed* \[ no\]
</dt> <dd>

Indica se o programa RemoteApp é exibido ou oculto.

</dd> <dt>

*uDisplayInformation* \[ no\]
</dt> <dd>

As informações de exibição.

<dt>

<span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>

<span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>**\_falha APPDISPLAY \_ Rail**


</dt> <dd>

A reconexão automática está em andamento.

</dd> <dt>

<span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>

<span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>**\_DESKTOPHOOKED APPDISPLAY \_ Rail**


</dt> <dd>

A contagem de RemoteApps acabou de entrar em zero.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Implemente esse método em seu coletor de eventos para receber uma notificação de que um RemoteApp foi exibido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



 

 





