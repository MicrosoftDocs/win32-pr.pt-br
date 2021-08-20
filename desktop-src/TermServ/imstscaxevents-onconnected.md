---
title: Método onconnected IMsTscAxEvents
description: Chamado quando o controle de cliente está no processo de estabelecer uma conexão com um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).
ms.assetid: 9c26d112-c070-4870-93d5-2fcc84a1331f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método onconnected
- Método onconnected Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método onconnected
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a9dfa60dee2c470e54c1900bc94aef5cdcb38835aa5e112f9ab5da0a9cce449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118853836"
---
# <a name="imstscaxeventsonconnected-method"></a>Método IMsTscAxEvents:: onconnected

Chamado quando o controle de cliente está no processo de estabelecer uma conexão com um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).

## <a name="syntax"></a>Sintaxe


```C++
void OnConnected();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Implemente esse método em seu coletor de eventos para receber uma notificação de que o controle estabeleceu uma conexão com um servidor de Host da Sessão RD.

Consulte o evento [**IMsTscAxEvents:: OnLoginComplete**](imstscaxevents-onlogincomplete.md) para obter mais informações sobre como chamar esse método.

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

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

 

 





