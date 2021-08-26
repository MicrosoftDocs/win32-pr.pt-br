---
title: Propriedade EventTrigger.Subscription
description: Para scripts, obtém ou define uma cadeia de caracteres de consulta que identifica o evento que aciona o gatilho.
ms.assetid: 31d32426-3dd7-41f9-89cc-b13767871b74
keywords:
- Propriedade de assinatura Agendador de Tarefas
- Propriedade subscription Agendador de Tarefas objeto , EventTrigger
- Objeto EventTrigger Agendador de Tarefas , propriedade Subscription
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
ms.openlocfilehash: 6d83225faa022de6e4a0823be3db971c71da503a885a46c1941fc1e5578f711b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100226"
---
# <a name="eventtriggersubscription-property"></a>Propriedade EventTrigger.Subscription

Para scripts, obtém ou define uma cadeia de caracteres de consulta que identifica o evento que aciona o gatilho.

## <a name="syntax"></a>Syntax


```VB
EventTrigger.Subscription As String
```



## <a name="property-value"></a>Valor da propriedade

Uma cadeia de caracteres de consulta que identifica o evento que aciona o gatilho.

## <a name="remarks"></a>Comentários

Ao ler ou escrever seu próprio XML para uma tarefa, a assinatura de evento é especificada usando o elemento [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) do esquema Agendador de Tarefas aplicativo.

Para obter mais informações sobre como escrever uma cadeia de [caracteres](../wes/subscribing-to-events.md)de consulta para determinados eventos, [consulte](/previous-versions//aa385231(v=vs.85)) Seleção de eventos e Assinatura de Eventos .

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
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> <dt>

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

