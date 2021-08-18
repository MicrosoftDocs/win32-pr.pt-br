---
title: Propriedade MonthlyDOWTrigger.MonthsOfYear
description: Para scripts, obtém ou define os meses do ano durante os quais a tarefa é executado. | Propriedade MonthlyDOWTrigger.MonthsOfYear
ms.assetid: 4ab7ab43-9c9b-4cd3-be8f-1989b83e8cf3
keywords:
- Propriedade MonthsOfYear Agendador de Tarefas
- Propriedade MonthsOfYear Agendador de Tarefas objeto , MonthlyDOWTrigger
- Objeto MonthlyDOWTrigger Agendador de Tarefas propriedade , MonthsOfYear
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.MonthsOfYear
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f8dc9752cf241218a95a9816824bc6ccf560f47c3445df9e5f40406381de3b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253816"
---
# <a name="monthlydowtriggermonthsofyear-property"></a>Propriedade MonthlyDOWTrigger.MonthsOfYear

Para scripts, obtém ou define os meses do ano durante os quais a tarefa é executado.

## <a name="syntax"></a>Sintaxe


```VB
MonthlyDOWTrigger.MonthsOfYear As short
```



## <a name="property-value"></a>Valor da propriedade

Uma máscara bit a bit que indica os meses do ano durante os quais a tarefa é executado.

## <a name="remarks"></a>Comentários

A tabela a seguir mostra o mapeamento da máscara bit a bit usada por essa propriedade.



| Mês     | Valor hex. | Valor decimal |
|-----------|-----------|---------------|
| Janeiro   | 0X01      | 1             |
| Fevereiro  | 0x02      | 2             |
| Março     | 0X04      | 4             |
| Abril     | 0X08      | 8             |
| Mai       | 0X10      | 16            |
| Junho      | 0X20      | 32            |
| Julho      | 0x40      | 64            |
| Agosto    | 0X80      | 128           |
| Setembro | 0X100     | 256           |
| Outubro   | 0X200     | 512           |
| Novembro  | 0X400     | 1024          |
| Dezembro  | 0X800     | 2.048          |



 

Ao ler ou escrever XML para uma tarefa, os meses do ano de um calendário mensal do dia da semana são especificados pelo elemento [**Months**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) do esquema Agendador de Tarefas.

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

 

 





