---
title: Propriedade TaskSettings. IdleSettings
description: Para scripts, Obtém ou define as informações que especificam como a Agendador de Tarefas executa tarefas quando o computador está em uma condição ociosa.
ms.assetid: 5205db6d-668e-498a-bbd5-edfcf66eec7f
keywords:
- Agendador de Tarefas da propriedade IdleSettings
- Propriedade IdleSettings Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade IdleSettings
topic_type:
- apiref
api_name:
- TaskSettings.IdleSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972d341d205ff5719f94a9c0a3b44f64c5678495
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757604"
---
# <a name="tasksettingsidlesettings-property"></a>Propriedade TaskSettings. IdleSettings

Para scripts, Obtém ou define as informações que especificam como a Agendador de Tarefas executa tarefas quando o computador está em uma condição ociosa. Para obter informações sobre condições ociosas, consulte [condições de ociosidade da tarefa](task-idle-conditions.md).

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```VB
TaskSettings.IdleSettings As IdleSettings
```



## <a name="property-value"></a>Valor da propriedade

Um objeto [**IdleSettings**](idlesettings.md) que especifica como a Agendador de tarefas trata a tarefa quando o computador entra em uma condição ociosa.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) do esquema de Agendador de tarefas.

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

 

 





