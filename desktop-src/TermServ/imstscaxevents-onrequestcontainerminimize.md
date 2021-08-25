---
title: Método OnRequestContainerMinimize de IMsTscAxEvents
description: Chamado quando o usuário pressiona o botão Minimizar na barra de conexão no modo de tela inteira. O acionamento desse evento é uma solicitação que o aplicativo de contêiner se minimiza.
ms.assetid: fc052f9b-cf59-4d5a-ba39-571627b72f2a
ms.tgt_platform: multiple
keywords:
- Método OnRequestContainerMinimize Serviços de Área de Trabalho Remota
- Método OnRequestContainerMinimize Serviços de Área de Trabalho Remota interface , IMsTscAxEvents
- Interface IMsTscAxEvents Serviços de Área de Trabalho Remota método , OnRequestContainerMinimize
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestContainerMinimize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 344bd85d8d224a5901517c55c8e0a95c854ed246e74a9d0c8def1eebae515305
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125056"
---
# <a name="imstscaxeventsonrequestcontainerminimize-method"></a>Método IMsTscAxEvents::OnRequestContainerMinimize

Chamado quando o usuário pressiona o **botão Minimizar** na barra de conexão no modo de tela inteira. O acionamento desse evento é uma solicitação que o aplicativo de contêiner se minimiza.

## <a name="syntax"></a>Sintaxe


```C++
void OnRequestContainerMinimize();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método só será chamado se o modo de tela inteira manipulado pelo contêiner estiver habilitado – consulte [**IMsTscAdvancedSettings::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) para obter mais informações.

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

 

 





