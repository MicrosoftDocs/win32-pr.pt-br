---
title: Elemento Value (namedValues)
description: Contém o valor que está associado a um nome em um par de nome-valor.
ms.assetid: d5582b55-0b9b-4fed-a425-9d15a1a62fb7
keywords:
- Elemento de valor Agendador de Tarefas
topic_type:
- apiref
api_name:
- Value
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2583d7fcaa9a9832e54c405200397e40948204546cb81e89a90ceb6949e218e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610411"
---
# <a name="value-namedvalues-element"></a>Elemento Value (namedValues)

Contém o valor que está associado a um nome em um par de nome-valor.

``` syntax
<xs:element name="Value"
    type="namedValue"
    minOccurs="1"
    maxOccurs="32"
 />
```

O elemento **Value** é definido pelo tipo complexo [**namedValues**](taskschedulerschema-namedvalues-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                              | Derivado de                                                       | Descrição                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ValueQueries (eventTriggertype)**](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [**namedValues**](taskschedulerschema-namedvalues-complextype.md) | Especifica uma coleção de consultas XPath nomeadas. Cada consulta na coleção é aplicada ao último XML de evento de correspondência que é retornado da consulta de assinatura especificada no elemento [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) . O nome da consulta pode ser usado como uma variável na mensagem de uma ação de exmessage.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte [**propriedade Value de ITaskNamedValuePair**](/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluepair-get_value).

Para desenvolvimento de script, consulte [**TaskNamedValuePair. Value**](tasknamedvaluepair-value.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 





