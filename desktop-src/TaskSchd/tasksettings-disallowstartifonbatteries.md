---
title: Propriedade TaskSettings. DisallowStartIfOnBatteries
description: Para scripts, Obtém ou define um valor booliano que indica que a tarefa não será iniciada se o computador estiver sendo executado em baterias.
ms.assetid: 5e13f168-a396-495f-a486-e64e8524c8cd
keywords:
- Agendador de Tarefas da propriedade DisallowStartIfOnBatteries
- Propriedade DisallowStartIfOnBatteries Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade DisallowStartIfOnBatteries
topic_type:
- apiref
api_name:
- TaskSettings.DisallowStartIfOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35a7fde3012b25dfeab65e6e6088bb1d950892d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086111"
---
# <a name="tasksettingsdisallowstartifonbatteries-property"></a>Propriedade TaskSettings. DisallowStartIfOnBatteries

Para scripts, Obtém ou define um valor booliano que indica que a tarefa não será iniciada se o computador estiver sendo executado em baterias.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.DisallowStartIfOnBatteries As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Um valor booliano que indica que a tarefa não será iniciada se o computador estiver sendo executado em baterias. Se for true, a tarefa não será iniciada se o computador estiver sendo executado em baterias. Se for false, a tarefa será iniciada se o computador estiver sendo executado em baterias. O padrão é True.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md) do esquema de Agendador de tarefas.

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

 

 





