---
title: Propriedade IdleSettings. RestartOnIdle
description: Para scripts, Obtém ou define um valor booliano que indica se a tarefa é reiniciada quando o computador entra em uma condição ociosa mais de uma vez.
ms.assetid: c77b6f5f-659c-4aa0-a5f7-39c01e5ca65e
keywords:
- Agendador de Tarefas da propriedade RestartOnIdle
- Propriedade RestartOnIdle Agendador de Tarefas, objeto IdleSettings
- Objeto IdleSettings Agendador de Tarefas, Propriedade RestartOnIdle
topic_type:
- apiref
api_name:
- IdleSettings.RestartOnIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e80b2e523f2f19222292eac7752847a72291c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761812"
---
# <a name="idlesettingsrestartonidle-property"></a>Propriedade IdleSettings. RestartOnIdle

Para scripts, Obtém ou define um valor booliano que indica se a tarefa é reiniciada quando o computador entra em uma condição ociosa mais de uma vez.

## <a name="syntax"></a>Syntax


```VB
IdleSettings.RestartOnIdle As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Um valor booliano que indica se a tarefa deve ser reiniciada quando o computador entrar em uma condição ociosa mais de uma vez. O padrão é False.

## <a name="remarks"></a>Comentários

Essa propriedade só será usada se a propriedade [**IdleSettings. StopOnIdleEnd**](idlesettings-stoponidleend.md) for definida como true.

Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> <dt>

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

 





