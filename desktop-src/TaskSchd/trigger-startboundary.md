---
title: Propriedade Trigger.StartBoundary
description: Para scripts, obtém ou define a data e a hora em que o gatilho é ativado.
ms.assetid: 0687cdda-e72c-47cd-ac0c-0de2f8afc3e8
keywords:
- Propriedade StartBoundary Agendador de Tarefas
- Propriedade StartBoundary Agendador de Tarefas , objeto Trigger
- Disparar objeto Agendador de Tarefas propriedade , StartBoundary
topic_type:
- apiref
api_name:
- Trigger.StartBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b49fa865c215c3190b2d081390c98eec1336ffb00a4bf1e9dd9d94226105e96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002074"
---
# <a name="triggerstartboundary-property"></a>Propriedade Trigger.StartBoundary

Para scripts, obtém ou define a data e a hora em que o gatilho é ativado.

## <a name="syntax"></a>Syntax


```VB
Trigger.StartBoundary As String
```



## <a name="property-value"></a>Valor da propriedade

A data e a hora em que o gatilho é ativado. A data e a hora devem estar no seguinte formato: AAAA-MM-DDTHH:MM:SS(+-)HH:MM. Por exemplo, a data de 11 de outubro de 2005 às 1:21:17 no fuso horário do Pacífico seria escrita como 2005-10-11T13:21:17-08:00. A seção (+-)HH:MM do formato descreve o fuso horário como um determinado número de horas à frente ou atrás Tempo Universal Coordenado (Greenwich Mean Time).

## <a name="remarks"></a>Comentários

Ao ler ou escrever XML para uma tarefa, o limite inicial do gatilho é especificado no [**elemento StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) do Agendador de Tarefas esquema.

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

 

 





