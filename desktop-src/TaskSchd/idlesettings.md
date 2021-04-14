---
title: Objeto IdleSettings
description: Objeto de script que especifica como a Agendador de Tarefas executa tarefas quando o computador está em uma condição ociosa.
ms.assetid: d303596a-0a84-4056-9f7a-5a9512852002
keywords:
- Agendador de Tarefas de objeto IdleSettings
- Agendador de Tarefas de objeto IdleSettings, descrito
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
ms.openlocfilehash: 819ff226386f30483de96fac6213b35d7dd51a52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369470"
---
# <a name="idlesettings-object"></a>Objeto IdleSettings

Um objeto de script que especifica como a Agendador de Tarefas executa tarefas quando o computador está em uma condição ociosa. Para obter informações sobre condições ociosas, consulte [condições de ociosidade da tarefa](task-idle-conditions.md).

## <a name="members"></a>Membros

O objeto **IdleSettings** tem estes tipos de membros:

- [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **IdleSettings** tem essas propriedades.

> [!NOTE]
> As configurações *IdleDuration* e *WaitTimeout* são preteridas. Eles ainda estão presentes na interface do usuário Agendador de Tarefas, e seus métodos de interface ainda podem retornar valores válidos, mas não são mais usados.

| Propriedade                                                       | Tipo de acesso           | Descrição                                                                                                                                                     |
|:---------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RestartOnIdle**](idlesettings-restartonidle.md)<br/> | Leitura/gravação<br/> | Obtém ou define um valor booliano que indica se a tarefa é reiniciada quando o computador entra em uma condição ociosa mais de uma vez.<br/>            |
| [**StopOnIdleEnd**](idlesettings-stoponidleend.md)<br/> | Leitura/gravação<br/> | Obtém ou define um valor booliano que indica que o Agendador de Tarefas encerrará a tarefa se a condição de ociosidade terminar antes de a tarefa ser concluída.<br/> |
| **Preterido**: [ **IdleDuration**](idlesettings-idleduration.md)<br/>   | Leitura/gravação<br/> | Obtém ou define um valor que indica a quantidade de tempo que o computador deve estar em um estado ocioso antes que a tarefa seja executada.<br/>                            |
| **Preterido**: [ **WaitTimeout**](idlesettings-waittimeout.md)<br/>     | Leitura/gravação<br/> | Obtém ou define um valor que indica a quantidade de tempo que o Agendador de Tarefas aguardará a ocorrência de uma condição ociosa.<br/>                             |

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) do esquema de Agendador de tarefas.

Se uma tarefa for disparada por um gatilho ocioso, a propriedade [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) será ignorada.

> [!NOTE]
> *IdleSettings. IdleDuration* e *IdleSettings. WaitTimeout* são preteridos.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |

## <a name="see-also"></a>Confira também

[Objetos Agendador de Tarefas](task-scheduler-objects.md)

[Agendador de Tarefas](task-scheduler-start-page.md)
