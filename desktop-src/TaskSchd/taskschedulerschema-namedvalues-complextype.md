---
title: Tipo complexo namedValues
description: Define um par nome-valor no qual o nome está associado ao valor .
ms.assetid: 07c512fd-3eab-4238-8d75-83827a958a1e
keywords:
- tipo complexo namedValues Agendador de Tarefas
topic_type:
- apiref
api_name:
- namedValues
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d54e7c33d0b7ab2e5be3c4de6f3f648398a7e65670c0379f5621ae9e8a8bd46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513932"
---
# <a name="namedvalues-complex-type"></a>Tipo complexo namedValues

Define um par nome-valor no qual o nome está associado ao valor .

``` syntax
<xs:complexType name="namedValues">
    <xs:sequence>
        <xs:element name="Value"
            type="namedValue"
            minOccurs="1"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                        | Type                                                | Descrição                                                                         |
|----------------------------------------------------------------|-----------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Valor**](taskschedulerschema-value-namedvalues-element.md) | [**namedValue**](schema-namedvalue-complextype.md) | Especifica o valor associado a um nome em um par nome-valor.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





