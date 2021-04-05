---
title: Propriedade Trigger. Enabled
description: Para scripts, Obtém ou define um valor booliano que indica se o gatilho está habilitado.
ms.assetid: 8fb5a0cc-ddd4-430d-9593-95a4cb311f18
keywords:
- Propriedade habilitada Agendador de Tarefas
- Propriedade habilitada Agendador de Tarefas, objeto de gatilho
- Objeto disparador Agendador de Tarefas, Propriedade Enabled
topic_type:
- apiref
api_name:
- Trigger.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411bc36dcf03933e2b4cee2f575aaec3b8133846
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918209"
---
# <a name="triggerenabled-property"></a>Propriedade Trigger. Enabled

Para scripts, Obtém ou define um valor booliano que indica se o gatilho está habilitado.

## <a name="syntax"></a>Syntax


```VB
Trigger.Enabled As Boolean
```



## <a name="property-value"></a>Valor da propriedade

True se o gatilho estiver habilitado; caso contrário, false. O padrão é true.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, a propriedade Enabled é especificada usando o elemento [**Enabled**](taskschedulerschema-enabled-triggerbasetype-element.md) do esquema de Agendador de tarefas.

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

 

 





