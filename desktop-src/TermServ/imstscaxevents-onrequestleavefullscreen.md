---
title: Método IMsTscAxEvents OnRequestLeaveFullScreen
description: Chamado quando o cliente solicita a saída do modo de tela inteira e a propriedade IMsTscAdvancedSettings Put \_ ContainerHandledFullScreen foi definida como um valor diferente de zero.
ms.assetid: db6ee012-8288-4360-98b2-12858ea65baa
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnRequestLeaveFullScreen
- Método OnRequestLeaveFullScreen Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnRequestLeaveFullScreen
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
ms.openlocfilehash: e814d6153e32fdf4fa498a6630fc9ca2908510e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644798"
---
# <a name="imstscaxeventsonrequestleavefullscreen-method"></a>Método IMsTscAxEvents:: OnRequestLeaveFullScreen

Chamado quando o cliente solicita a saída do modo de tela inteira e a propriedade [**IMsTscAdvancedSettings::p UT \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) foi definida como um valor diferente de zero.

## <a name="syntax"></a>Sintaxe


```C++
void OnRequestLeaveFullScreen();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

No modo de tela inteira manipulado por contêiner, o contêiner deve deixar o modo de tela inteira padrão em resposta a esse evento.

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





