---
title: Propriedade TaskSettings.RunOnlyIfIdle
description: Para scripts, obtém ou define um valor booliana que indica que o Agendador de Tarefas executará a tarefa somente se o computador estiver em uma condição ociosa.
ms.assetid: fca1d98e-0544-4301-a709-1e0dae762e07
keywords:
- Propriedade RunOnlyIfIdle Agendador de Tarefas
- Propriedade RunOnlyIfIdle Agendador de Tarefas objeto , TaskSettings
- Objeto TaskSettings Agendador de Tarefas propriedade , RunOnlyIfIdle
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
ms.openlocfilehash: ed423dc4cd34a03bd3b76401284a4d6bfb98270e7c0d0feed0a45046a82e7d3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990816"
---
# <a name="tasksettingsrunonlyifidle-property"></a>Propriedade TaskSettings.RunOnlyIfIdle

Para scripts, obtém ou define um valor booliana que indica que o Agendador de Tarefas executará a tarefa somente se o computador estiver em uma condição ociosa.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.RunOnlyIfIdle As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se True, a propriedade indicará que o Agendador de Tarefas executará a tarefa somente se o computador estiver em uma condição ociosa. O padrão é False.

## <a name="remarks"></a>Comentários

Ao ler ou escrever XML para uma tarefa, essa configuração é especificada no elemento [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md) do Agendador de Tarefas esquema.

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

 

 





