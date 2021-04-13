---
title: Propriedade MonthlyDOWTrigger. DaysOfWeek
description: Para scripts, Obtém ou define os dias da semana durante os quais a tarefa é executada.
ms.assetid: dd9b2463-69a1-4e77-a8f7-26b186d3d02d
keywords:
- Agendador de Tarefas da Propriedade DaysOfWeek
- Propriedade DaysOfWeek Agendador de Tarefas, objeto MonthlyDOWTrigger
- Objeto MonthlyDOWTrigger Agendador de Tarefas, Propriedade DaysOfWeek
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15344650dabdec2bcbacf91397b37b97ce3f0772
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455713"
---
# <a name="monthlydowtriggerdaysofweek-property"></a>Propriedade MonthlyDOWTrigger. DaysOfWeek

Para scripts, Obtém ou define os dias da semana durante os quais a tarefa é executada.

## <a name="syntax"></a>Syntax


```VB
MonthlyDOWTrigger.DaysOfWeek As short
```



## <a name="property-value"></a>Valor da propriedade

Uma máscara de bits bit que indica os dias da semana durante os quais a tarefa é executada.

## <a name="remarks"></a>Comentários

A tabela a seguir mostra o mapeamento da máscara de bits bit que é usada por essa propriedade.



| Dia da semana | Valor hex | Valor decimal |
|-------------|-----------|---------------|
| Sunday      | 0x01      | 1             |
| Monday      | 0x02      | 2             |
| Terça-feira     | 0x04      | 4             |
| Quarta-feira   | 0x08      | 8             |
| Quinta-feira    | 0x10      | 16            |
| Friday      | 0x20      | 32            |
| Sábado    | 0x40      | 64            |



 

Ao ler ou gravar XML para uma tarefa, os dias da semana de um calendário mensal de dia da semana são especificados pelo elemento [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MonthlyDOWTrigger**](monthlydowtrigger.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





