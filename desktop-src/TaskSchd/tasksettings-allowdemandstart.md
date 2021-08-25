---
title: Propriedade TaskSettings.AllowDemandStart
description: Para scripts, obtém ou define um valor booliana que indica que a tarefa pode ser iniciada usando o comando Executar ou o menu Contexto.
ms.assetid: 1eae19ae-3b4d-4eb2-82d0-685ef2729f36
keywords:
- Propriedade AllowDemandStart Agendador de Tarefas
- Propriedade AllowDemandStart Agendador de Tarefas objeto , TaskSettings
- Objeto TaskSettings Agendador de Tarefas propriedade , AllowDemandStart
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
ms.openlocfilehash: a48ecaf9010b4269ffff66b556d01cfccc057fd05207f619290af9e50f6c757f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959476"
---
# <a name="tasksettingsallowdemandstart-property"></a>Propriedade TaskSettings.AllowDemandStart

Para scripts, obtém ou define um valor booliana que indica que a tarefa pode ser iniciada usando o comando Executar ou o menu Contexto.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.AllowDemandStart As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se True, a tarefa poderá ser executado usando o comando Executar ou o menu Contexto. Se False, a tarefa não poderá ser executado usando o comando Executar ou o menu Contexto. O padrão é True.

## <a name="remarks"></a>Comentários

Quando essa propriedade é definida como True, a tarefa pode ser iniciada independentemente de quando qualquer gatilho iniciar a tarefa.

Ao ler ou escrever XML para uma tarefa, essa configuração é especificada no elemento [AllowStartOnDemand](taskschedulerschema-allowstartondemand-settingstype-element.md) do Agendador de Tarefas esquema.

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

 

 





