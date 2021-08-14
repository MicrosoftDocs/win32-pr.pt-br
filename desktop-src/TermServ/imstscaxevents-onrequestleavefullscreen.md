---
title: Método OnRequestLeaveFullScreen IMsTscAxEvents
description: Chamado quando o cliente solicita para sair do modo de tela inteira e a propriedade IMsTscAdvancedSettings put ContainerHandledFullScreen foi definida como um valor diferente \_ de zero.
ms.assetid: db6ee012-8288-4360-98b2-12858ea65baa
ms.tgt_platform: multiple
keywords:
- Método OnRequestLeaveFullScreen Serviços de Área de Trabalho Remota
- Método OnRequestLeaveFullScreen Serviços de Área de Trabalho Remota interface , IMsTscAxEvents
- Interface IMsTscAxEvents Serviços de Área de Trabalho Remota , método OnRequestLeaveFullScreen
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestLeaveFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74f82cd71942f559039a175fdfff9319cae5ea35a73d4698760be4642a23c448
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757332"
---
# <a name="imstscaxeventsonrequestleavefullscreen-method"></a>Método IMsTscAxEvents::OnRequestLeaveFullScreen

Chamado quando o cliente solicita para sair do modo de tela inteira e a propriedade [**IMsTscAdvancedSettings::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) foi definida como um valor diferente de zero.

## <a name="syntax"></a>Sintaxe


```C++
void OnRequestLeaveFullScreen();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

No modo de tela inteira manipulado pelo contêiner, o contêiner deve deixar o modo de tela inteira padrão em resposta a esse evento.

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for Conexão Web de Área de Trabalho Remota](requirements-for-remote-desktop-web-connection.md).

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

 

 





