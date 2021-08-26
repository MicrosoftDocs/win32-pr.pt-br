---
title: Propriedade TaskSettings.StopIfGoingOnBatteries
description: Para scripts, obtém ou define um valor booliana que indica que a tarefa será interrompida se o computador estiver indo para baterias.
ms.assetid: a133cba0-c93e-4963-83a3-7587e323fc6e
keywords:
- Propriedade StopIfGoingOnBatteries Agendador de Tarefas
- Propriedade StopIfGoingOnBatteries Agendador de Tarefas objeto , TaskSettings
- Objeto TaskSettings Agendador de Tarefas propriedade , StopIfGoingOnBatteries
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
ms.openlocfilehash: 229d5d3beef974e9ce8758f9bd81fc3217bd9c3fcf9bf37be137abe6515cc62a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974882"
---
# <a name="tasksettingsstopifgoingonbatteries-property"></a>Propriedade TaskSettings.StopIfGoingOnBatteries

Para scripts, obtém ou define um valor booliana que indica que a tarefa será interrompida se o computador estiver indo para baterias.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.StopIfGoingOnBatteries As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Um valor booliana que indica que a tarefa será interrompida se o computador estiver passando por baterias. Se True, a propriedade indicará que a tarefa será interrompida se o computador estiver indo para baterias. Se False, a propriedade indica que a tarefa não será interrompida se o computador estiver passando por baterias. O padrão é True. Consulte Comentários para obter mais detalhes.

## <a name="remarks"></a>Comentários

Ao ler ou escrever XML para uma tarefa, essa configuração é especificada no elemento [**StopIfGoingOnBatteries**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) do esquema Agendador de Tarefas aplicativo.

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

 

 





