---
title: Método OnLoginComplete IMsTscAxEvents
description: Chamado quando o controle de cliente fez logon com êxito em um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD), seguindo a exibição da caixa de diálogo Windows Logon.
ms.assetid: acb345a6-3153-4b8f-ac51-fe0c19fa750a
ms.tgt_platform: multiple
keywords:
- Método OnLoginComplete Serviços de Área de Trabalho Remota
- Método OnLoginComplete Serviços de Área de Trabalho Remota interface , IMsTscAxEvents
- Interface IMsTscAxEvents Serviços de Área de Trabalho Remota , método OnLoginComplete
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLoginComplete
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6c89b494a250652e054e245eb0de3267a860bec1a193c7dc953f93fd0800c2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138429"
---
# <a name="imstscaxeventsonlogincomplete-method"></a>Método IMsTscAxEvents::OnLoginComplete

Chamado quando o controle de cliente fez logon com êxito em um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD), seguindo a exibição da caixa de diálogo Windows Logon.

## <a name="syntax"></a>Sintaxe


```C++
void OnLoginComplete();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Implemente esse método no seu sink de eventos para receber uma notificação de que o controle concluiu o logon.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como manipular esse evento usando o Visual Basic script. A suposição neste exemplo é que o objeto de controle é denominado "MsRdpClient".

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for Conexão Web de Área de Trabalho Remota](requirements-for-remote-desktop-web-connection.md).


```VB
Sub MsRdpClient.OnLoginComplete()
    Msgbox("Login has completed")
End sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Imstscaxevents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





