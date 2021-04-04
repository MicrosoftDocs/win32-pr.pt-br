---
title: Propriedade MonthlyDOWTrigger. MonthsOfYear
description: Para scripts, Obtém ou define os meses do ano durante os quais a tarefa é executada. | Propriedade MonthlyDOWTrigger. MonthsOfYear
ms.assetid: 4ab7ab43-9c9b-4cd3-be8f-1989b83e8cf3
keywords:
- Agendador de Tarefas da Propriedade MonthsOfYear
- Propriedade MonthsOfYear Agendador de Tarefas, objeto MonthlyDOWTrigger
- Objeto MonthlyDOWTrigger Agendador de Tarefas, Propriedade MonthsOfYear
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
ms.openlocfilehash: c345cd3de12d7dba3450f62bdb18bfdcee496b13
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837869"
---
# <a name="monthlydowtriggermonthsofyear-property"></a>Propriedade MonthlyDOWTrigger. MonthsOfYear

Para scripts, Obtém ou define os meses do ano durante os quais a tarefa é executada.

## <a name="syntax"></a>Syntax


```VB
MonthlyDOWTrigger.MonthsOfYear As short
```



## <a name="property-value"></a>Valor da propriedade

Uma máscara de bits bit que indica os meses do ano durante os quais a tarefa é executada.

## <a name="remarks"></a>Comentários

A tabela a seguir mostra o mapeamento da máscara de bits bit que é usada por essa propriedade.



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



 

Ao ler ou gravar XML para uma tarefa, os meses do ano de um calendário mensal de dia da semana são especificados pelo elemento [**months**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) do esquema de Agendador de tarefas.

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

 

 





