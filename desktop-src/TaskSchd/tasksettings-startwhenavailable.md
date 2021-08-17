---
title: Propriedade TaskSettings.StartWhenAvailable
description: Para scripts, obtém ou define um valor booliana que indica que o Agendador de Tarefas pode iniciar a tarefa a qualquer momento após a hora agendada ter passado.
ms.assetid: 911de67c-baf8-4346-9b4c-e39e5f96c0fe
keywords:
- Propriedade StartWhenAvailable Agendador de Tarefas
- Propriedade StartWhenAvailable Agendador de Tarefas objeto , TaskSettings
- O objeto TaskSettings Agendador de Tarefas propriedade , StartWhenAvailable
topic_type:
- apiref
api_name:
- TaskSettings.StartWhenAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0ed43a04bba63d0e760866684df15c4cae5e80a1b3338d122408756f4cec46e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757919"
---
# <a name="tasksettingsstartwhenavailable-property"></a>Propriedade TaskSettings.StartWhenAvailable

Para scripts, obtém ou define um valor booliana que indica que o Agendador de Tarefas pode iniciar a tarefa a qualquer momento após a hora agendada ter passado.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.StartWhenAvailable As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se True, a propriedade indica que o Agendador de Tarefas pode iniciar a tarefa a qualquer momento após a hora agendada ter passado. O padrão é False.

## <a name="remarks"></a>Comentários

Essa propriedade se aplica somente a tarefas baseadas em tempo com um limite final ou tarefas baseadas em tempo definidas para repetir infinitamente.

As tarefas iniciadas após a hora agendada (devido à propriedade [**StartWhenAvailable**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable) que está sendo definida como True) são enfileirasdas na fila de tarefas do serviço Agendador de Tarefas e são iniciadas após um atraso. O atraso padrão é de 10 minutos.

Ao ler ou escrever XML para uma tarefa, essa configuração é especificada no [**elemento StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md) do Agendador de Tarefas esquema.

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

 

 





