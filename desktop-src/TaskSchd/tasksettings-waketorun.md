---
title: Propriedade TaskSettings. WakeToRun
description: Para scripts, Obtém ou define um valor booliano que indica que o Agendador de Tarefas ativará o computador quando for hora de executar a tarefa.
ms.assetid: 51f83637-5bae-48c6-b750-b4467e651cec
keywords:
- Agendador de Tarefas da propriedade WakeToRun
- Propriedade WakeToRun Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade WakeToRun
topic_type:
- apiref
api_name:
- TaskSettings.WakeToRun
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b563fd1ecd27914e84043b85c44f0cf5262e9fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644475"
---
# <a name="tasksettingswaketorun-property"></a>Propriedade TaskSettings. WakeToRun

Para scripts, Obtém ou define um valor booliano que indica que o Agendador de Tarefas ativará o computador quando for hora de executar a tarefa.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.WakeToRun As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se for true, a propriedade indicará que o Agendador de Tarefas ativará o computador quando for hora de executar a tarefa.

## <a name="remarks"></a>Comentários

Quando o serviço de Agendador de Tarefas ativa o computador para executar uma tarefa, a tela pode permanecer desativada, mesmo que o computador não esteja mais no modo de suspensão ou hibernação. A tela será ativada quando o Windows Vista detectar que um usuário voltou a usar o computador.

Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**WakeToRun**](taskschedulerschema-waketorun-settingstype-element.md) do esquema de Agendador de tarefas.

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

 

 





