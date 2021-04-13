---
title: Propriedade DailyTrigger. DaysInterval
description: Para scripts, Obtém ou define o intervalo entre os dias no agendamento.
ms.assetid: 13e9f6fd-62ee-4b19-8b3d-a6808e146340
keywords:
- Agendador de Tarefas da propriedade DaysInterval
- Propriedade DaysInterval Agendador de Tarefas, objeto DailyTrigger
- Objeto DailyTrigger Agendador de Tarefas, Propriedade DaysInterval
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
ms.openlocfilehash: 6499f3b900fe10b2a2527c2e2ee675cca3151204
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499420"
---
# <a name="dailytriggerdaysinterval-property"></a>Propriedade DailyTrigger. DaysInterval

Para scripts, Obtém ou define o intervalo entre os dias no agendamento.

## <a name="syntax"></a>Syntax


```VB
DailyTrigger.DaysInterval As short
```



## <a name="property-value"></a>Valor da propriedade

O intervalo entre os dias no agendamento.

## <a name="remarks"></a>Comentários

Um intervalo de 1 produz uma agenda diária. Um intervalo de 2 produz uma agenda de dia a cada outro.

Ao ler ou gravar seu próprio XML para uma tarefa, o intervalo de um agendamento diário é especificado usando o elemento [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) do esquema de Agendador de tarefas.

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
</dt> <dt>

[**DailyTrigger**](dailytrigger.md)
</dt> </dl>

 

 





