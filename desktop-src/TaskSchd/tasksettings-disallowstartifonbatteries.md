---
title: Propriedade TaskSettings.DisallowStartIfOnBatteries
description: Para scripts, obtém ou define um valor booliana que indica que a tarefa não será iniciada se o computador estiver em execução em baterias.
ms.assetid: 5e13f168-a396-495f-a486-e64e8524c8cd
keywords:
- Propriedade DisallowStartIfOnBatteries Agendador de Tarefas
- Propriedade DisallowStartIfOnBatteries Agendador de Tarefas objeto , TaskSettings
- O objeto TaskSettings Agendador de Tarefas propriedade , DisallowStartIfOnBatteries
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
ms.openlocfilehash: 7e08e3e57a961f08a5f1ddae17c8334c9f1d3501b34590b1f98676195108444d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099716"
---
# <a name="tasksettingsdisallowstartifonbatteries-property"></a>Propriedade TaskSettings.DisallowStartIfOnBatteries

Para scripts, obtém ou define um valor booliana que indica que a tarefa não será iniciada se o computador estiver em execução em baterias.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.DisallowStartIfOnBatteries As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Um valor booliana que indica que a tarefa não será iniciada se o computador estiver em execução com baterias. Se True, a tarefa não será iniciada se o computador estiver em execução com baterias. Se False, a tarefa será iniciada se o computador estiver em execução com baterias. O padrão é True.

## <a name="remarks"></a>Comentários

Ao ler ou escrever XML para uma tarefa, essa configuração é especificada no [**elemento DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md) do esquema Agendador de Tarefas.

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

 

 





