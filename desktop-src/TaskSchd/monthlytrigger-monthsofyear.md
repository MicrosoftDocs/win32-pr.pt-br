---
title: Propriedade MonthlyTrigger. MonthsOfYear
description: Para scripts, Obtém ou define os meses do ano durante os quais a tarefa é executada. | Propriedade MonthlyTrigger. MonthsOfYear
ms.assetid: cf26a815-7f4f-4b7a-8db8-a4bd9b77cf49
keywords:
- Agendador de Tarefas da Propriedade MonthsOfYear
- Propriedade MonthsOfYear Agendador de Tarefas, objeto MonthlyTrigger
- Objeto MonthlyTrigger Agendador de Tarefas, Propriedade MonthsOfYear
topic_type:
- apiref
api_name:
- MonthlyTrigger.MonthsOfYear
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ff6f08e257acf85a8a3f073f43c3c81e65817900f8154e1701ab73fe10c2368
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253776"
---
# <a name="monthlytriggermonthsofyear-property"></a>Propriedade MonthlyTrigger. MonthsOfYear

Para scripts, Obtém ou define os meses do ano durante os quais a tarefa é executada.

## <a name="syntax"></a>Syntax


```VB
MonthlyTrigger.MonthsOfYear As short
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



 

Ao ler ou gravar seu próprio XML para uma tarefa, os meses do ano são especificados usando o elemento [**months**](taskschedulerschema-months-monthlyscheduletype-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> <dt>

[**MonthlyTrigger**](monthlytrigger.md)
</dt> </dl>

 

 





