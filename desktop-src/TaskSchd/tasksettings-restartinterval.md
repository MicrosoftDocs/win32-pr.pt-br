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
ms.openlocfilehash: f511e43ebb1d61fd80f2fcab34aba092704b8338
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644380"
---
# <a name="tasksettingsrestartinterval-property"></a>Propriedade TaskSettings. RestartInterval

Para scripts, Obtém ou define um valor que especifica por quanto tempo o Agendador de Tarefas tentará reiniciar a tarefa.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.RestartInterval As String
```



## <a name="property-value"></a>Valor da propriedade

Um valor que especifica quanto tempo o Agendador de Tarefas tentará reiniciar a tarefa. Se essa propriedade for definida, a propriedade [**RestartCount**](tasksettings-restartcount.md) também deverá ser definida. O formato para essa cadeia de caracteres é P <days> dt <hours> H <minutes> M <seconds> S (por exemplo, "PT5M" é de 5 minutos, "PT1H" é de 1 hora e "PT20M" é de 20 minutos). O tempo máximo permitido é de 31 dias e o tempo mínimo permitido é de 1 minuto.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**Interval**](taskschedulerschema-interval-restarttype-element.md) do esquema de Agendador de tarefas.

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
</dt> </dl>

 

 





