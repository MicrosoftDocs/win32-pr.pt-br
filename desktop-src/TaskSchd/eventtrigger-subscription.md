---
title: Propriedade EventTrigger. Subscription
description: Para scripts, Obtém ou define uma cadeia de caracteres de consulta que identifica o evento que dispara o gatilho.
ms.assetid: 31d32426-3dd7-41f9-89cc-b13767871b74
keywords:
- Agendador de Tarefas de propriedade de assinatura
- Propriedade de assinatura Agendador de Tarefas, objeto EventTrigger
- Agendador de Tarefas de objeto EventTrigger, propriedade de assinatura
topic_type:
- apiref
api_name:
- EventTrigger.Subscription
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68ad05576e248d3ad6c2551a8654a9198ca3c0f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810450"
---
# <a name="eventtriggersubscription-property"></a>Propriedade EventTrigger. Subscription

Para scripts, Obtém ou define uma cadeia de caracteres de consulta que identifica o evento que dispara o gatilho.

## <a name="syntax"></a>Sintaxe


```VB
EventTrigger.Subscription As String
```



## <a name="property-value"></a>Valor da propriedade

Uma cadeia de caracteres de consulta que identifica o evento que dispara o gatilho.

## <a name="remarks"></a>Comentários

Ao ler ou gravar seu próprio XML para uma tarefa, a assinatura de evento é especificada usando o elemento [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) do esquema de Agendador de tarefas.

Para obter mais informações sobre como gravar uma cadeia de caracteres de consulta para determinados eventos, consulte [seleção de eventos](/previous-versions//aa385231(v=vs.85)) e [assinatura de eventos](../wes/subscribing-to-events.md).

## <a name="examples"></a>Exemplos

A cadeia de caracteres de consulta a seguir define uma assinatura para todos os eventos de nível 2 no canal do sistema:


```XML
"<QueryList>
    <Query Id='1'>
        <Select Path='System'>*[System/Level=2]</Select>
    </Query>
</QueryList>" 
```



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

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

