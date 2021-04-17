---
title: Propriedade TaskSettings. StopIfGoingOnBatteries
description: Para scripts, Obtém ou define um valor booliano que indica que a tarefa será interrompida se o computador estiver indo para baterias.
ms.assetid: a133cba0-c93e-4963-83a3-7587e323fc6e
keywords:
- Agendador de Tarefas da propriedade StopIfGoingOnBatteries
- Propriedade StopIfGoingOnBatteries Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade StopIfGoingOnBatteries
topic_type:
- apiref
api_name:
- TaskSettings.StopIfGoingOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aced436d653b6bbc02b4b36edea9046e3ac62392
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455692"
---
# <a name="tasksettingsstopifgoingonbatteries-property"></a>Propriedade TaskSettings. StopIfGoingOnBatteries

Para scripts, Obtém ou define um valor booliano que indica que a tarefa será interrompida se o computador estiver indo para baterias.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.StopIfGoingOnBatteries As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Um valor booliano que indica que a tarefa será interrompida se o computador estiver indo para baterias. Se for true, a propriedade indicará que a tarefa será interrompida se o computador estiver indo para as baterias. Se for false, a propriedade indicará que a tarefa não será interrompida se o computador estiver indo para baterias. O padrão é True. Consulte comentários para obter mais detalhes.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**StopIfGoingOnBatteries**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) do esquema de Agendador de tarefas.

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

 

 





