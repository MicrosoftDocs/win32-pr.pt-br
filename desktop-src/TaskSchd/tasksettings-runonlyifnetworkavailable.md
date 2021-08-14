---
title: Propriedade TaskSettings. RunOnlyIfNetworkAvailable
description: Para scripts, Obtém ou define um valor booliano que indica que o Agendador de Tarefas executará a tarefa somente quando uma rede estiver disponível.
ms.assetid: 1a2b085f-0572-47d3-ac1f-0032c8427af0
keywords:
- Agendador de Tarefas da propriedade RunOnlyIfNetworkAvailable
- Propriedade RunOnlyIfNetworkAvailable Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade RunOnlyIfNetworkAvailable
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfNetworkAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 193d235276ffc37513c95b5ae0a4cef5a6e84cd0bc7d8bea7fab67a262110080
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354843"
---
# <a name="tasksettingsrunonlyifnetworkavailable-property"></a>Propriedade TaskSettings. RunOnlyIfNetworkAvailable

Para scripts, Obtém ou define um valor booliano que indica que o Agendador de Tarefas executará a tarefa somente quando uma rede estiver disponível.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.RunOnlyIfNetworkAvailable As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se for true, a propriedade indicará que o Agendador de Tarefas executará a tarefa somente quando uma rede estiver disponível. O padrão é False.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





