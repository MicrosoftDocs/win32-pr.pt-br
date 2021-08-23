---
title: Objeto IdleSettings
description: Objeto de script que especifica como o Agendador de Tarefas executa tarefas quando o computador está em uma condição ociosa.
ms.assetid: d303596a-0a84-4056-9f7a-5a9512852002
keywords:
- Objeto IdleSettings Agendador de Tarefas
- Objeto IdleSettings Agendador de Tarefas , descrito
topic_type:
- apiref
api_name:
- IdleSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7597f2232d95d6ddd5f8001be8cf88178ccf5dacd3694c2a8e179d371e54c898
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659596"
---
# <a name="idlesettings-object"></a>Objeto IdleSettings

Um objeto de script que especifica como o Agendador de Tarefas executa tarefas quando o computador está em uma condição ociosa. Para obter informações sobre condições ociosas, consulte [Condições ociosas da tarefa](task-idle-conditions.md).

## <a name="members"></a>Membros

O **objeto IdleSettings** tem estes tipos de membros:

- [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O **objeto IdleSettings** tem essas propriedades.

> [!NOTE]
> As *configurações IdleDuration* *e WaitTimeout* foram preterida. Eles ainda estão presentes na interface do usuário Agendador de Tarefas e seus métodos de interface ainda podem retornar valores válidos, mas não são mais usados.

| Propriedade                                                       | Tipo de acesso           | Descrição                                                                                                                                                     |
|:---------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RestartOnIdle**](idlesettings-restartonidle.md)<br/> | Leitura/gravação<br/> | Obtém ou define um valor booliana que indica se a tarefa é reiniciada quando o computador entra em uma condição ociosa mais de uma vez.<br/>            |
| [**StopOnIdleEnd**](idlesettings-stoponidleend.md)<br/> | Leitura/gravação<br/> | Obtém ou define um valor booliana que indica que o Agendador de Tarefas encerrará a tarefa se a condição ociosa terminar antes que a tarefa seja concluída.<br/> |
| **Preterido:** [ **IdleDuration**](idlesettings-idleduration.md)<br/>   | Leitura/gravação<br/> | Obtém ou define um valor que indica a quantidade de tempo que o computador deve estar em um estado ocioso antes da tarefa ser executado.<br/>                            |
| **Preterido:** [ **WaitTimeout**](idlesettings-waittimeout.md)<br/>     | Leitura/gravação<br/> | Obtém ou define um valor que indica a quantidade de tempo que o Agendador de Tarefas aguardará a ocorrência de uma condição ociosa.<br/>                             |

## <a name="remarks"></a>Comentários

Ao ler ou escrever XML para uma tarefa, essa configuração é especificada no elemento [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) do Agendador de Tarefas esquema.

Se uma tarefa for disparada por um gatilho ocioso, a propriedade [**IdleSettings.WaitTimeout**](idlesettings-waittimeout.md) será ignorada.

> [!NOTE]
> *IdleSettings.IdleDuration* *e IdleSettings.WaitTimeout* foram preterido.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |

## <a name="see-also"></a>Confira também

[Agendador de Tarefas objetos](task-scheduler-objects.md)

[Agendador de Tarefas](task-scheduler-start-page.md)
