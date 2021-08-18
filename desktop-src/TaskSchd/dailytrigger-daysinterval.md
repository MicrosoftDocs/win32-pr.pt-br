---
title: Propriedade DailyTrigger.DaysInterval
description: Para scripts, obtém ou define o intervalo entre os dias na agenda.
ms.assetid: 13e9f6fd-62ee-4b19-8b3d-a6808e146340
keywords:
- Propriedades DaysInterval Agendador de Tarefas
- Propriedade DaysInterval Agendador de Tarefas objeto , DailyTrigger
- Objeto DailyTrigger Agendador de Tarefas propriedade , DaysInterval
topic_type:
- apiref
api_name:
- DailyTrigger.DaysInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4355e6c2a26b197224141018fa5a1d85e7d31e211ac47dc84a9e8c9ef3750fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139489"
---
# <a name="dailytriggerdaysinterval-property"></a>Propriedade DailyTrigger.DaysInterval

Para scripts, obtém ou define o intervalo entre os dias na agenda.

## <a name="syntax"></a>Syntax


```VB
DailyTrigger.DaysInterval As short
```



## <a name="property-value"></a>Valor da propriedade

O intervalo entre os dias na agenda.

## <a name="remarks"></a>Comentários

Um intervalo de 1 produz uma agenda diária. Um intervalo de 2 produz uma agenda a cada dia.

Ao ler ou escrever seu próprio XML para uma tarefa, o intervalo de uma agenda diária é especificado usando o elemento [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) do esquema Agendador de Tarefas dados.

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
</dt> <dt>

[**DailyTrigger**](dailytrigger.md)
</dt> </dl>

 

 





