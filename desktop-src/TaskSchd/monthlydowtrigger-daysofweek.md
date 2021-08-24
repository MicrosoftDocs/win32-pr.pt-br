---
title: Propriedade MonthlyDOWTrigger.DaysOfWeek
description: Para scripts, obtém ou define os dias da semana durante os quais a tarefa é executado.
ms.assetid: dd9b2463-69a1-4e77-a8f7-26b186d3d02d
keywords:
- Propriedade DaysOfWeek Agendador de Tarefas
- Propriedade DaysOfWeek Agendador de Tarefas objeto , MonthlyDOWTrigger
- Objeto MonthlyDOWTrigger Agendador de Tarefas propriedade , DaysOfWeek
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
ms.openlocfilehash: 0b9abf5dcd33c92d402f8ed6047a2fd80a0d5905bae075110931cfb8f83aa10a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517456"
---
# <a name="monthlydowtriggerdaysofweek-property"></a>Propriedade MonthlyDOWTrigger.DaysOfWeek

Para scripts, obtém ou define os dias da semana durante os quais a tarefa é executado.

## <a name="syntax"></a>Syntax


```VB
MonthlyDOWTrigger.DaysOfWeek As short
```



## <a name="property-value"></a>Valor da propriedade

Uma máscara bit a bit que indica os dias da semana durante os quais a tarefa é executado.

## <a name="remarks"></a>Comentários

A tabela a seguir mostra o mapeamento da máscara bit a bit usada por essa propriedade.



| Dia da semana | Valor hexaxa | Valor decimal |
|-------------|-----------|---------------|
| Sunday      | 0x01      | 1             |
| Monday      | 0x02      | 2             |
| Terça-feira     | 0x04      | 4             |
| Quarta-feira   | 0x08      | 8             |
| Quinta-feira    | 0x10      | 16            |
| Friday      | 0x20      | 32            |
| Sábado    | 0x40      | 64            |



 

Ao ler ou escrever XML para uma tarefa, os dias da semana de um calendário mensal do dia da semana são especificados pelo [**elemento DaysOfWeek.**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MonthlyDOWTrigger**](monthlydowtrigger.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





