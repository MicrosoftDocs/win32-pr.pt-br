---
title: Tipo complexo InputTypeListType
description: Define uma lista de tipos de entrada.
ms.assetid: e6bba894-7c17-411e-92e5-9276728a5e4b
keywords:
- Log de eventos do tipo complexo InputTypeListType
topic_type:
- apiref
api_name:
- InputTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e68b4077bfb08b69a31f18d81aa55d0b5ac54f78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086341"
---
# <a name="inputtypelisttype-complex-type"></a>Tipo complexo InputTypeListType

Define uma lista de tipos de entrada.

``` syntax
<xs:complexType name="InputTypeListType">
    <xs:sequence>
        <xs:element name="inType"
            type="InputType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                | Type                                                           | Descrição                       |
|------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------|
| [**intipo**](eventmanifestschema-intype-inputtypelisttype-element.md) | [**InputType**](eventmanifestschema-inputtype-complextype.md) | Define um tipo de entrada.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





