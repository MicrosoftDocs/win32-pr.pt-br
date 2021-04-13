---
title: Propriedade TaskSettings. Enabled
description: Para scripts, Obtém ou define um valor booliano que indica que a tarefa está habilitada. A tarefa pode ser executada somente quando essa configuração for verdadeira.
ms.assetid: af8aa237-3402-4a82-b6ef-b713e1757d3a
keywords:
- Propriedade habilitada Agendador de Tarefas
- Propriedade Enabled Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade Enabled
topic_type:
- apiref
api_name:
- TaskSettings.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6805d7b754ac2c3553d5fde91826ffa192b91d97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369740"
---
# <a name="tasksettingsenabled-property"></a>Propriedade TaskSettings. Enabled

Para scripts, Obtém ou define um valor booliano que indica que a tarefa está habilitada. A tarefa pode ser executada somente quando essa configuração for verdadeira.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.Enabled As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se for true, a tarefa será habilitada. Se for false, a tarefa não estará habilitada.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**habilitado (settingstype)**](taskschedulerschema-enabled-settingstype-element.md) do esquema de Agendador de tarefas.

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

 

 





