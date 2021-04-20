---
title: Propriedade TaskSettings. RestartInterval
description: Para scripts, Obtém ou define um valor que especifica por quanto tempo o Agendador de Tarefas tentará reiniciar a tarefa.
ms.assetid: ad6f254d-55a8-478e-984e-a459f22043b5
keywords:
- Agendador de Tarefas da propriedade RestartInterval
- Propriedade RestartInterval Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade RestartInterval
topic_type:
- apiref
api_name:
- TaskSettings.RestartInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f127c5d434b5cb1e6dec6d8a3c68ee343fa00ffc
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734141"
---
# <a name="tasksettingsrestartinterval-property"></a>Propriedade TaskSettings. RestartInterval

Para scripts, Obtém ou define um valor que especifica por quanto tempo o Agendador de Tarefas tentará reiniciar a tarefa.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```VB
TaskSettings.RestartInterval As String
```



## <a name="property-value"></a>Valor da propriedade

Um valor que especifica quanto tempo o Agendador de Tarefas tentará reiniciar a tarefa. Se essa propriedade for definida, a propriedade [**RestartCount**](tasksettings-restartcount.md) também deverá ser definida. O formato dessa cadeia de caracteres é `P<days>DT<hours>H<minutes>M<seconds>S` (por exemplo, "PT5M" é de 5 minutos, "PT1H" é de 1 hora e "PT20M" é de 20 minutos). O tempo máximo permitido é de 31 dias e o tempo mínimo permitido é de 1 minuto.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**Interval**](taskschedulerschema-interval-restarttype-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





