---
title: Tipo complexo namedValues
description: Define um par de nome-valor no qual o nome está associado ao valor.
ms.assetid: 07c512fd-3eab-4238-8d75-83827a958a1e
keywords:
- Agendador de Tarefas tipo complexo namedValues
topic_type:
- apiref
api_name:
- namedValues
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f18c9fddab58f33ffc724a3e8df7bd65583cb88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644815"
---
# <a name="namedvalues-complex-type"></a>Tipo complexo namedValues

Define um par de nome-valor no qual o nome está associado ao valor.

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
| [**Valor**](taskschedulerschema-value-namedvalues-element.md) | [**nome do chamado**](schema-namedvalue-complextype.md) | Especifica o valor que está associado a um nome em um par de nome-valor.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





