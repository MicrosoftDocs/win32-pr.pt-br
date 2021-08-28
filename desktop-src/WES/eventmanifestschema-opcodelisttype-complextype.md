---
title: Tipo complexo OpcodeListType
description: Define uma lista de opcodes que são usados para identificar as operações de um componente do aplicativo.
ms.assetid: 0cbca036-b32e-4fc4-96ee-1dd5bee019bf
keywords:
- Tipo complexo OpcodeListType EventLog
topic_type:
- apiref
api_name:
- OpcodeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c44a2c2fa38957f302dfe3861a89f57dbe51d44ca737268a8988f8c138be8b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767296"
---
# <a name="opcodelisttype-complex-type"></a>Tipo complexo OpcodeListType

Define uma lista de opcodes que são usados para identificar as operações de um componente do aplicativo.

``` syntax
<xs:complexType name="OpcodeListType">
    <xs:sequence>
        <xs:element name="opcode"
            type="OpcodeType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                             | Type                                                             | Descrição                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Opcode**](eventmanifestschema-opcode-opcodelisttype-element.md) | [**Opcodetype**](eventmanifestschema-opcodetype-complextype.md) | Define uma operação dentro de um componente do aplicativo.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





