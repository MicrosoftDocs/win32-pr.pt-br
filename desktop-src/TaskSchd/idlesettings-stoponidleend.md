---
title: Propriedade IdleSettings. StopOnIdleEnd
description: Para scripts, Obtém ou define um valor booliano que indica que o Agendador de Tarefas encerrará a tarefa se a condição de ociosidade terminar antes de a tarefa ser concluída.
ms.assetid: 5908bf6b-227a-4234-a741-82cf38163171
keywords:
- Agendador de Tarefas da propriedade StopOnIdleEnd
- Propriedade StopOnIdleEnd Agendador de Tarefas, objeto IdleSettings
- Objeto IdleSettings Agendador de Tarefas, Propriedade StopOnIdleEnd
topic_type:
- apiref
api_name:
- IdleSettings.StopOnIdleEnd
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f475c0a05d43cf0fbdd7097c1ee083f9040b07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824254"
---
# <a name="idlesettingsstoponidleend-property"></a>Propriedade IdleSettings. StopOnIdleEnd

Para scripts, Obtém ou define um valor booliano que indica que o Agendador de Tarefas encerrará a tarefa se a condição de ociosidade terminar antes de a tarefa ser concluída.

## <a name="syntax"></a>Syntax


```VB
IdleSettings.StopOnIdleEnd As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Um valor booliano que indica que o Agendador de Tarefas encerrará a tarefa se a condição ociosa terminar antes de a tarefa ser concluída.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) do esquema de Agendador de tarefas.

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
</dt> <dt>

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

 





