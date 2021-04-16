---
title: Tipo complexo headerFieldType
description: Define os elementos que são usados para criar um campo de cabeçalho em uma mensagem de email.
ms.assetid: 66036875-1116-46eb-b2f5-8c8ad8373ab1
keywords:
- Agendador de Tarefas tipo complexo headerFieldType
topic_type:
- apiref
api_name:
- headerFieldType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ddbc0ae22c6baf3fd288cbe2ead19dac506afee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779436"
---
# <a name="headerfieldtype-complex-type"></a>Tipo complexo headerFieldType

Define os elementos que são usados para criar um campo de cabeçalho em uma mensagem de email.

``` syntax
<xs:complexType name="headerFieldType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
         />
        <xs:element name="Value"
            type="string"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                            | Type                                                                    | Descrição                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Nome**](taskschedulerschema-name-headerfieldtype-element.md)   | [**não vazio**](taskschedulerschema-nonemptystring-simpletype.md) | Especifica o nome do campo de cabeçalho em uma mensagem de email.<br/> |
| [**Valor**](taskschedulerschema-value-headerfieldtype-element.md) | **cadeia de caracteres**                                                              | Especifica o valor de um campo de cabeçalho em uma mensagem de email.<br/>  |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





