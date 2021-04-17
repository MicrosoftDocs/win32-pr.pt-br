---
title: Propriedade WeeklyTrigger. WeeksInterval
description: Para scripts, Obtém ou define o intervalo entre as semanas no agendamento.
ms.assetid: 7992dee2-1725-4325-9fe9-eaff84fa5adc
keywords:
- Agendador de Tarefas da propriedade WeeksInterval
- Propriedade WeeksInterval Agendador de Tarefas, objeto WeeklyTrigger
- Objeto WeeklyTrigger Agendador de Tarefas, Propriedade WeeksInterval
topic_type:
- apiref
api_name:
- WeeklyTrigger.WeeksInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4668b68d0b3f83e096284db35df799a63eb677b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105782883"
---
# <a name="weeklytriggerweeksinterval-property"></a>Propriedade WeeklyTrigger. WeeksInterval

Para scripts, Obtém ou define o intervalo entre as semanas no agendamento.

## <a name="syntax"></a>Syntax


```VB
WeeklyTrigger.WeeksInterval As short
```



## <a name="property-value"></a>Valor da propriedade

O intervalo entre as semanas no agendamento.

## <a name="remarks"></a>Comentários

Um intervalo de 1 produz uma agenda semanal. Um intervalo de 2 produz uma agenda de semana a cada uma.

Ao ler ou gravar seu próprio XML para uma tarefa, o intervalo de um agendamento semanal é especificado usando o elemento [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) do esquema de Agendador de tarefas.

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

 

 





