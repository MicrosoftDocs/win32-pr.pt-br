---
title: Método IMsTscAxEvents OnLoginComplete
description: Chamado quando o controle de cliente tiver feito logon com êxito em um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD), seguindo a exibição da caixa de diálogo de logon do Windows.
ms.assetid: acb345a6-3153-4b8f-ac51-fe0c19fa750a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnLoginComplete
- Método OnLoginComplete Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnLoginComplete
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
ms.openlocfilehash: 74d6b63f74ed99c8af939bafdc8a55a41e33b404
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499467"
---
# <a name="imstscaxeventsonlogincomplete-method"></a>Método IMsTscAxEvents:: OnLoginComplete

Chamado quando o controle de cliente tiver feito logon com êxito em um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD), seguindo a exibição da caixa de diálogo de logon do Windows.

## <a name="syntax"></a>Sintaxe


```C++
void OnLoginComplete();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Implemente esse método em seu coletor de eventos para receber uma notificação de que o controle concluiu o logon.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como lidar com esse evento usando Visual Basic código de script. A suposição neste exemplo é que seu objeto de controle é denominado "MsRdpClient".

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).


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

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





