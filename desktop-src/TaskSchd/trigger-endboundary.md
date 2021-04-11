---
title: Propriedade Trigger. endboundal
description: Para scripts, Obtém ou define a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.
ms.assetid: f34e6ba8-f6ef-43a0-8e3a-76c6a5f1ac04
keywords:
- Agendador de Tarefas de propriedade endboundal
- Propriedade endboundal Agendador de Tarefas, objeto Trigger
- Objeto disparador Agendador de Tarefas, Propriedade endboundal
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
ms.openlocfilehash: b385dddf186484bc17cff9f92d979cd64381335d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009150"
---
# <a name="triggerendboundary-property"></a>Propriedade Trigger. endboundal

Para scripts, Obtém ou define a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.

## <a name="syntax"></a>Syntax


```VB
Trigger.EndBoundary As String
```



## <a name="property-value"></a>Valor da propriedade

A data e a hora em que o gatilho é desativado. A data e a hora devem estar no seguinte formato: YYYY-MM-DDTHH: MM: SS (+-) HH: MM. Por exemplo, a data de outubro de 11, 2005 às 1:21:17 no fuso horário do Pacífico, seria escrita como 2005-10-11T13:21:17-08:00. A seção (+-) HH: MM do formato descreve o fuso horário como um determinado número de horas à frente ou atrás do tempo universal coordenado (Greenwich Mean Time).

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, a propriedade Enabled é especificada usando o elemento [**Endboundal**](taskschedulerschema-endboundary-triggerbasetype-element.md) do esquema de Agendador de tarefas.

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
</dt> </dl>

 

 





