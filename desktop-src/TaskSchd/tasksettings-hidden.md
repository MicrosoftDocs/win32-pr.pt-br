---
title: Propriedade TaskSettings. Hidden
description: Para scripts, Obtém ou define um valor booliano que indica que a tarefa não estará visível na interface do usuário.
ms.assetid: 84a3d0b3-30f0-4356-b6cf-9bee3091612f
keywords:
- Agendador de Tarefas de propriedade oculta
- Propriedade Hidden Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade Hidden
topic_type:
- apiref
api_name:
- TaskSettings.Hidden
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5a04ea67c6385e13235e10795dd2a7b250f2237f381ba2ca4f77a72832f9258
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118857158"
---
# <a name="tasksettingshidden-property"></a>Propriedade TaskSettings. Hidden

Para scripts, Obtém ou define um valor booliano que indica que a tarefa não estará visível na interface do usuário. No entanto, os administradores podem substituir essa configuração por meio do uso de um "comutador mestre" que torna todas as tarefas visíveis na interface do usuário.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.Hidden As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se **for true**, o valor indicará que a tarefa não estará visível na interface do usuário. Se **for false**, a tarefa ficará visível na interface do usuário. O padrão é **False**.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**oculto (settingstype)**](taskschedulerschema-hidden-settingstype-element.md) do esquema de Agendador de tarefas.

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

 

 





