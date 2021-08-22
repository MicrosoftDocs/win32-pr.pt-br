---
title: Propriedade EventTrigger.ValueQueries
description: Para scripts, obtém ou define uma coleção de consultas XPath nomeadas. Cada consulta na coleção é aplicada ao ÚLTIMO XML de evento correspondente que é retornado da consulta de assinatura especificada na propriedade Subscription.
ms.assetid: 9ff92b66-f63c-4736-b086-df7dd8cd2b10
keywords:
- Propriedade ValueQueries Agendador de Tarefas
- Propriedade ValueQueries Agendador de Tarefas objeto , EventTrigger
- Objeto EventTrigger Agendador de Tarefas propriedade , ValueQueries
topic_type:
- apiref
api_name:
- EventTrigger.ValueQueries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f8fd28cd616af56a9b51ecf4e709df5f07674c6d1f307320128645364f3bfc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253876"
---
# <a name="eventtriggervaluequeries-property"></a>Propriedade EventTrigger.ValueQueries

Para scripts, obtém ou define uma coleção de consultas XPath nomeadas. Cada consulta na coleção é aplicada ao ÚLTIMO XML de evento correspondente que é retornado da consulta de assinatura especificada na [**propriedade**](eventtrigger-subscription.md) Subscription.

## <a name="syntax"></a>Sintaxe


```VB
EventTrigger.ValueQueries As String
```



## <a name="property-value"></a>Valor da propriedade

Uma coleção de pares nome-valor. Cada par nome-valor na coleção define um nome exclusivo para um valor da propriedade do evento que dispara o gatilho de evento. O valor da propriedade do evento é definido como uma consulta de evento XPath. Para obter mais informações sobre consultas de evento XPath, consulte [Seleção de eventos](/previous-versions//aa385231(v=vs.85)).

## <a name="remarks"></a>Comentários

O nome da consulta pode ser usado como uma variável nas seguintes propriedades de ação:

-   [**ShowMessageAction.MessageBody**](showmessageaction-messagebody.md)
-   [**ShowMessageAction.Title**](showmessageaction-title.md)
-   [**ExecAction.Arguments**](execaction-arguments.md)
-   [**ExecAction.WorkingDirectory**](execaction-workingdirectory.md)
-   [**EmailAction.Server**](emailaction-server.md)
-   [**EmailAction.Subject**](emailaction-subject.md)
-   [**EmailAction.To**](emailaction-to.md)
-   [**EmailAction.Cc**](emailaction-cc.md)
-   [**EmailAction.Bcc**](emailaction-bcc.md)
-   [**EmailAction.ReplyTo**](emailaction-replyto.md)
-   [**EmailAction.From**](emailaction-from.md)
-   [**EmailAction.Body**](emailaction-body.md)
-   [**ComHandlerAction.Data**](comhandleraction-data.md)

As cadeias de caracteres de exemplo de código a seguir mostram dois pares de valores de nome que podem ser usados em uma coleção nome-valor. Os valores retornados pelas consultas XPath podem substituir variáveis na propriedade de uma ação. Os valores são referenciados por nome, com `$(user)` e , na propriedade de `$(machine)` ação. Por exemplo, se as variáveis e são usadas na cadeia de `$(user)` `$(machine)` [**caracteres ShowMessageAction.MessageBody,**](showmessageaction-messagebody.md) o valor das consultas XPath substituirá as variáveis na cadeia de caracteres.

``` syntax
name: user
value: Event/UserData/SubjectUserName

name: machine
value: Event/UserData/MachineName
```

Para obter mais informações sobre como escrever uma cadeia de [caracteres](../wes/subscribing-to-events.md)de consulta para determinados eventos, [consulte](/previous-versions//aa385231(v=vs.85)) Seleção de eventos e Assinatura de Eventos .

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

 

