---
title: Propriedade TaskSettings. AllowDemandStart
description: Para scripts, Obtém ou define um valor booliano que indica que a tarefa pode ser iniciada usando o comando executar ou o menu de contexto.
ms.assetid: 1eae19ae-3b4d-4eb2-82d0-685ef2729f36
keywords:
- Agendador de Tarefas da propriedade AllowDemandStart
- Propriedade AllowDemandStart Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade AllowDemandStart
topic_type:
- apiref
api_name:
- TaskSettings.AllowDemandStart
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 657ba45e0809b74803e27de70fae52576fcf2a26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369332"
---
# <a name="tasksettingsallowdemandstart-property"></a>Propriedade TaskSettings. AllowDemandStart

Para scripts, Obtém ou define um valor booliano que indica que a tarefa pode ser iniciada usando o comando executar ou o menu de contexto.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.AllowDemandStart As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se for true, a tarefa poderá ser executada usando o comando Run ou o menu de contexto. Se for false, a tarefa não poderá ser executada usando o comando executar ou o menu de contexto. O padrão é True.

## <a name="remarks"></a>Comentários

Quando essa propriedade é definida como true, a tarefa pode ser iniciada independentemente de quando os gatilhos iniciam a tarefa.

Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [AllowStartOnDemand](taskschedulerschema-allowstartondemand-settingstype-element.md) do esquema de Agendador de tarefas.

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

 

 





