---
title: Propriedade TaskSettings.Enabled
description: Para scripts, obtém ou define um valor booliana que indica que a tarefa está habilitada. A tarefa pode ser executada somente quando essa configuração é True.
ms.assetid: af8aa237-3402-4a82-b6ef-b713e1757d3a
keywords:
- Propriedades habilitadas Agendador de Tarefas
- Propriedade habilitada Agendador de Tarefas objeto , TaskSettings
- O objeto TaskSettings Agendador de Tarefas propriedade , Habilitado
topic_type:
- apiref
api_name:
- TaskSettings.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e7853177aecae963e4899a67d2ba5b39d1eaebdc75e25ce6e14523963a70c45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738157"
---
# <a name="tasksettingsenabled-property"></a>Propriedade TaskSettings.Enabled

Para scripts, obtém ou define um valor booliana que indica que a tarefa está habilitada. A tarefa pode ser executada somente quando essa configuração é True.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.Enabled As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se True, a tarefa será habilitada. Se False, a tarefa não está habilitada.

## <a name="remarks"></a>Comentários

Ao ler ou escrever XML para uma tarefa, essa configuração é especificada no elemento [**Enabled (settingsType)**](taskschedulerschema-enabled-settingstype-element.md) do esquema Agendador de Tarefas.

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

 

 





