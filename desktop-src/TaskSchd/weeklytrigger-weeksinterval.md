---
title: Propriedade WeeklyTrigger.WeeksInterval
description: Para scripts, obtém ou define o intervalo entre as semanas na agenda.
ms.assetid: 7992dee2-1725-4325-9fe9-eaff84fa5adc
keywords:
- Propriedades WeeksInterval Agendador de Tarefas
- Propriedade WeeksInterval Agendador de Tarefas objeto , WeeklyTrigger
- Objeto WeeklyTrigger Agendador de Tarefas propriedade , WeeksInterval
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
ms.openlocfilehash: 547ebc8617d625df3dd0e8dba167bb60682185dfb13897c49524d1894789c933
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080256"
---
# <a name="weeklytriggerweeksinterval-property"></a>Propriedade WeeklyTrigger.WeeksInterval

Para scripts, obtém ou define o intervalo entre as semanas na agenda.

## <a name="syntax"></a>Syntax


```VB
WeeklyTrigger.WeeksInterval As short
```



## <a name="property-value"></a>Valor da propriedade

O intervalo entre as semanas na agenda.

## <a name="remarks"></a>Comentários

Um intervalo de 1 produz uma agenda semanal. Um intervalo de 2 produz um agendamento a cada outra semana.

Ao ler ou escrever seu próprio XML para uma tarefa, o intervalo de uma agenda semanal é especificado usando o elemento [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) do esquema Agendador de Tarefas dados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





