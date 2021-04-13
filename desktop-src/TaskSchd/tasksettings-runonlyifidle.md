---
title: Propriedade TaskSettings. RunOnlyIfIdle
description: Para scripts, Obtém ou define um valor booliano que indica que o Agendador de Tarefas executará a tarefa somente se o computador estiver em uma condição ociosa.
ms.assetid: fca1d98e-0544-4301-a709-1e0dae762e07
keywords:
- Agendador de Tarefas da propriedade RunOnlyIfIdle
- Propriedade RunOnlyIfIdle Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade RunOnlyIfIdle
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8256b2a3d1dd96db9a8f29b49ce10f6c2fdb266d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369458"
---
# <a name="tasksettingsrunonlyifidle-property"></a>Propriedade TaskSettings. RunOnlyIfIdle

Para scripts, Obtém ou define um valor booliano que indica que o Agendador de Tarefas executará a tarefa somente se o computador estiver em uma condição ociosa.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.RunOnlyIfIdle As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se for true, a propriedade indicará que o Agendador de Tarefas executará a tarefa somente se o computador estiver em uma condição ociosa. O padrão é False.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md) do esquema de Agendador de tarefas.

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

 

 





