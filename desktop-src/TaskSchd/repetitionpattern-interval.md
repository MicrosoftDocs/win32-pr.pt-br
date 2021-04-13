---
title: Propriedade RepetitionPattern. Interval
description: Para scripts, Obtém ou define o período de tempo entre cada reinicialização da tarefa.
ms.assetid: c48bd304-21f3-435e-99f5-3b2da0078bb8
keywords:
- Agendador de Tarefas de propriedade de intervalo
- Propriedade Interval Agendador de Tarefas, objeto RepetitionPattern
- Agendador de Tarefas de objeto RepetitionPattern, propriedade Interval
topic_type:
- apiref
api_name:
- RepetitionPattern.Interval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d62bb821f4c5e61d344e21fafa4ba1265c73470
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499520"
---
# <a name="repetitionpatterninterval-property"></a>Propriedade RepetitionPattern. Interval

Para scripts, Obtém ou define o período de tempo entre cada reinicialização da tarefa.

## <a name="syntax"></a>Syntax


```VB
RepetitionPattern.Interval As String
```



## <a name="property-value"></a>Valor da propriedade

A quantidade de tempo entre cada reinicialização da tarefa. O formato para essa cadeia de caracteres é P <days> dt <hours> H <minutes> M <seconds> S (por exemplo, "PT5M" é de 5 minutos, "PT1H" é de 1 hora e "PT20M" é de 20 minutos). O tempo máximo permitido é de 31 dias e o tempo mínimo permitido é de 1 minuto.

## <a name="remarks"></a>Comentários

Se você especificar uma duração de repetição para uma tarefa, também deverá especificar o intervalo de repetição.

Ao ler ou gravar XML para uma tarefa, o intervalo de repetição é especificado no elemento [**Interval**](taskschedulerschema-interval-repetitiontype-element.md) do esquema de Agendador de tarefas.

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

 

 





