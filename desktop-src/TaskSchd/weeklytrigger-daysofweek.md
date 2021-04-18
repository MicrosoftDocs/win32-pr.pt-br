---
title: Propriedade WeeklyTrigger. DaysOfWeek
description: Para scripts, Obtém ou define os dias da semana em que a tarefa é executada.
ms.assetid: 79f279d4-d6d2-428b-bbed-226e4eaaefb6
keywords:
- Agendador de Tarefas da Propriedade DaysOfWeek
- Propriedade DaysOfWeek Agendador de Tarefas, objeto WeeklyTrigger
- Objeto WeeklyTrigger Agendador de Tarefas, Propriedade DaysOfWeek
topic_type:
- apiref
api_name:
- WeeklyTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f0a27ef031e7baf46d2d3c0e33c23fb505c7ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499850"
---
# <a name="weeklytriggerdaysofweek-property"></a>Propriedade WeeklyTrigger. DaysOfWeek

Para scripts, Obtém ou define os dias da semana em que a tarefa é executada.

## <a name="syntax"></a>Syntax


```VB
WeeklyTrigger.DaysOfWeek As short
```



## <a name="property-value"></a>Valor da propriedade

Uma máscara de bits bit que indica os dias da semana em que a tarefa é executada.

## <a name="remarks"></a>Comentários

A tabela a seguir mostra o mapeamento da máscara de bits bit que é usada por essa propriedade.



| Mês     | Valor hex. | Valor decimal |
|-----------|-----------|---------------|
| Sunday    | 0X01      | 1             |
| Monday    | 0x02      | 2             |
| Terça-feira   | 0X04      | 4             |
| Quarta-feira | 0X08      | 8             |
| Quinta-feira  | 0X10      | 16            |
| Friday    | 0x20      | 32            |
| Sábado  | 0X40      | 64            |



 

Ao ler ou gravar seu próprio XML para uma tarefa, os dias da semana são especificados usando o elemento [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) do esquema de Agendador de tarefas.

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

 

 





