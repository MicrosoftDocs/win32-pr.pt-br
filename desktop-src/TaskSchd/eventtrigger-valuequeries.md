---
title: Propriedade EventTrigger. ValueQueries
description: Para scripts, Obtém ou define uma coleção de consultas XPath nomeadas. Cada consulta na coleção é aplicada ao último XML de evento de correspondência que é retornado da consulta de assinatura especificada na propriedade de assinatura.
ms.assetid: 9ff92b66-f63c-4736-b086-df7dd8cd2b10
keywords:
- Agendador de Tarefas da propriedade ValueQueries
- Propriedade ValueQueries Agendador de Tarefas, objeto EventTrigger
- Objeto EventTrigger Agendador de Tarefas, Propriedade ValueQueries
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
ms.openlocfilehash: fd2061f9d910e67855cc0dcb6d64248067fcb9e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499618"
---
# <a name="eventtriggervaluequeries-property"></a>Propriedade EventTrigger. ValueQueries

Para scripts, Obtém ou define uma coleção de consultas XPath nomeadas. Cada consulta na coleção é aplicada ao último XML de evento de correspondência que é retornado da consulta de assinatura especificada na propriedade de [**assinatura**](eventtrigger-subscription.md) .

## <a name="syntax"></a>Syntax


```VB
EventTrigger.ValueQueries As String
```



## <a name="property-value"></a>Valor da propriedade

Uma coleção de pares nome-valor. Cada par de nome-valor na coleção define um nome exclusivo para um valor de Propriedade do evento que dispara o gatilho de evento. O valor da Propriedade do evento é definido como uma consulta de evento XPath. Para obter mais informações sobre consultas de eventos XPath, consulte [seleção de eventos](/previous-versions//aa385231(v=vs.85)).

## <a name="remarks"></a>Comentários

O nome da consulta pode ser usado como uma variável nas seguintes propriedades de ação:

-   [**MessageBody.**](showmessageaction-messagebody.md)
-   [**Nome da mensagem. title**](showmessageaction-title.md)
-   [**Argumentos execaction.**](execaction-arguments.md)
-   [**Execaction. WorkingDirectory**](execaction-workingdirectory.md)
-   [**Emailaction. Server**](emailaction-server.md)
-   [**Emailaction. Subject**](emailaction-subject.md)
-   [**EmailAction.To**](emailaction-to.md)
-   [**EmailAction.Cc**](emailaction-cc.md)
-   [**Emailaction. Bcc**](emailaction-bcc.md)
-   [**Emailaction. ReplyTo**](emailaction-replyto.md)
-   [**Emailaction. from**](emailaction-from.md)
-   [**Emailaction. Body**](emailaction-body.md)
-   [**Comhandleaction. Data**](comhandleraction-data.md)

As cadeias de caracteres de exemplo de código a seguir mostram dois pares de valor de nome que podem ser usados em uma coleção de nome-valor. Os valores retornados pelas consultas XPath podem substituir variáveis na propriedade de uma ação. Os valores são referenciados pelo nome, com `$(user)` e `$(machine)` , na propriedade Action. Por exemplo, se as `$(user)` `$(machine)` variáveis e forem usadas na cadeia de caracteres [**. MessageBody**](showmessageaction-messagebody.md) , o valor das consultas XPath substituirá as variáveis na cadeia de caracteres.

``` syntax
name: user
value: Event/UserData/SubjectUserName

name: machine
value: Event/UserData/MachineName
```

Para obter mais informações sobre como gravar uma cadeia de caracteres de consulta para determinados eventos, consulte [seleção de eventos](/previous-versions//aa385231(v=vs.85)) e [assinatura de eventos](../wes/subscribing-to-events.md).

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

 

