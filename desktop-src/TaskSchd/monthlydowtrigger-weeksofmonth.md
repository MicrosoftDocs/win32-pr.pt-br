---
title: Propriedade MonthlyDOWTrigger. WeeksOfMonth
description: Para scripts, Obtém ou define as semanas do mês durante as quais a tarefa é executada.
ms.assetid: 62c3b654-622e-4a71-b77e-1b3fd5fb46b8
keywords:
- Agendador de Tarefas da propriedade WeeksOfMonth
- Propriedade WeeksOfMonth Agendador de Tarefas, objeto MonthlyDOWTrigger
- Objeto MonthlyDOWTrigger Agendador de Tarefas, Propriedade WeeksOfMonth
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.WeeksOfMonth
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7efea628e6eefdef07bdc50b9719a7c404f78bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454843"
---
# <a name="monthlydowtriggerweeksofmonth-property"></a>Propriedade MonthlyDOWTrigger. WeeksOfMonth

Para scripts, Obtém ou define as semanas do mês durante as quais a tarefa é executada.

## <a name="syntax"></a>Syntax


```VB
MonthlyDOWTrigger.WeeksOfMonth As short
```



## <a name="property-value"></a>Valor da propriedade

Uma máscara de bits bit que indica os dias da semana durante os quais a tarefa é executada.

## <a name="remarks"></a>Comentários

A tabela a seguir mostra o mapeamento da máscara de bits bit que é usada por essa propriedade.



| Semana                     | Valor hex | Valor decimal |
|--------------------------|-----------|---------------|
| Primeira semana do mês  | 0X01      | 1             |
| Segunda semana do mês | 0x02      | 2             |
| Terceira semana do mês  | 0X04      | 4             |
| Quarta semana do mês | 0X08      | 8             |



 

Ao ler ou gravar XML para uma tarefa, os dias da semana de um calendário mensal de dia da semana são especificados pelo elemento [**Weeks**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) .

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

 

 





