---
title: Elemento ValueQueries (eventTriggertype)
description: Contém uma sequência de elementos que cada um contém um nome e um valor de consulta XPath.
ms.assetid: 4b57568c-81b6-43fd-9194-9817c4817197
keywords:
- Agendador de Tarefas do elemento ValueQueries
topic_type:
- apiref
api_name:
- ValueQueries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4448693c1c1ab19b2ea13050cc9ab817bdc25e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918141"
---
# <a name="valuequeries-eventtriggertype-element"></a>Elemento ValueQueries (eventTriggertype)

Contém uma sequência de elementos que cada um contém um nome e um valor de consulta XPath. As consultas são aplicadas a um evento retornado da assinatura de evento especificada no elemento [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) . O nome do valor de consulta XPath pode ser usado como uma variável na seção de ação de uma tarefa.

``` syntax
<xs:element name="ValueQueries"
    type="namedValues"
    minOccurs="0"
 />
```

O elemento **ValueQueries** é definido pelo tipo complexo [**eventtriggertype**](taskschedulerschema-eventtriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                      | Derivado de                                                                 | Descrição                                                                   |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger (The Trigger)**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**eventTriggertype**](taskschedulerschema-eventtriggertype-complextype.md) | Especifica um gatilho que inicia uma tarefa quando ocorre um evento do sistema.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte a [**Propriedade ValueQueries de IEventTrigger**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries).

Para desenvolvimento de script, consulte [**EventTrigger. ValueQueries**](eventtrigger-valuequeries.md).

## <a name="examples"></a>Exemplos

Para obter um exemplo completo do XML para uma tarefa que especifica um gatilho de evento usando esse elemento, consulte [exemplo de gatilho de evento (XML)](/previous-versions//aa446889(v=vs.85)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

