---
title: Propriedade Trigger. StartBoundary
description: Para scripts, Obtém ou define a data e a hora em que o gatilho é ativado.
ms.assetid: 0687cdda-e72c-47cd-ac0c-0de2f8afc3e8
keywords:
- Agendador de Tarefas da propriedade StartBoundary
- Agendador de Tarefas da propriedade StartBoundary, objeto de gatilho
- Objeto disparador Agendador de Tarefas, propriedade StartBoundary
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
ms.openlocfilehash: 141e7e4d80d090e92ecb951917f60f972587d4b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644473"
---
# <a name="triggerstartboundary-property"></a>Propriedade Trigger. StartBoundary

Para scripts, Obtém ou define a data e a hora em que o gatilho é ativado.

## <a name="syntax"></a>Syntax


```VB
Trigger.StartBoundary As String
```



## <a name="property-value"></a>Valor da propriedade

A data e a hora em que o gatilho é ativado. A data e a hora devem estar no seguinte formato: YYYY-MM-DDTHH: MM: SS (+-) HH: MM. Por exemplo, a data de outubro de 11, 2005 às 1:21:17 no fuso horário do Pacífico, seria escrita como 2005-10-11T13:21:17-08:00. A seção (+-) HH: MM do formato descreve o fuso horário como um determinado número de horas à frente ou atrás do tempo universal coordenado (Greenwich Mean Time).

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, o limite de início do gatilho é especificado no elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) do esquema de Agendador de tarefas.

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

 

 





