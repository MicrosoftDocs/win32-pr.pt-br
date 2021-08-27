---
title: Propriedade Trigger.EndBoundary
description: Para scripts, obtém ou define a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.
ms.assetid: f34e6ba8-f6ef-43a0-8e3a-76c6a5f1ac04
keywords:
- Propriedade EndBoundary Agendador de Tarefas
- Propriedade EndBoundary Agendador de Tarefas , objeto Trigger
- Disparar objeto Agendador de Tarefas propriedade , EndBoundary
topic_type:
- apiref
api_name:
- Trigger.EndBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4f2b72100a7b981246788b38572c014a722c126115ab5a77d77eb7d96273f5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010446"
---
# <a name="triggerendboundary-property"></a>Propriedade Trigger.EndBoundary

Para scripts, obtém ou define a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.

## <a name="syntax"></a>Syntax


```VB
Trigger.EndBoundary As String
```



## <a name="property-value"></a>Valor da propriedade

A data e a hora em que o gatilho é desativado. A data e a hora devem estar no seguinte formato: AAAA-MM-DDTHH:MM:SS(+-)HH:MM. Por exemplo, a data de 11 de outubro de 2005 às 1:21:17 no fuso horário do Pacífico seria escrita como 2005-10-11T13:21:17-08:00. A seção (+-)HH:MM do formato descreve o fuso horário como um determinado número de horas à frente ou atrás Tempo Universal Coordenado (Hora média de Greenwich).

## <a name="remarks"></a>Comentários

Ao ler ou escrever XML para uma tarefa, a propriedade habilitada é especificada usando o [**elemento EndBoundary**](taskschedulerschema-endboundary-triggerbasetype-element.md) do Agendador de Tarefas esquema.

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

 

 





