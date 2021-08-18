---
description: Define a seção do manifesto de instrumentação que identifica o provedor e os contadores que eles fornecem.
ms.assetid: c661f1af-ebe8-4f8a-b77e-a2229f45facd
title: Tipo complexo de contadores
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 14630fa4e0e9461e59d377b4defc3edacee8dca9560d1f7eb42acb317ffd1f57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143959"
---
# <a name="counters-complex-type"></a>Tipo complexo de contadores

Define a seção do manifesto de instrumentação que identifica o provedor e os contadores que eles fornecem.

``` syntax
<xs:complexType name="counters">
    <xs:choice
        minOccurs="1"
        maxOccurs="1"
    >
        <xs:element name="provider"
            type="man:provider"
         />
    </xs:choice>
    <xs:attribute name="schemaVersion"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="1.1"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento      | Type                                                               | Descrição                                              |
|--------------|--------------------------------------------------------------------|----------------------------------------------------------|
| **operador** | [**Man: provedor**](performance-counters-provider-complex-type.md) | Identifica um provedor que fornece contadores.<br/> |



## <a name="attributes"></a>Atributos



| Nome          | Tipo | Descrição                                                      |
|---------------|------|------------------------------------------------------------------|
| schemaVersion |      | A versão do esquema usada para gravar o manifesto.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Instrumentação**](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype)
</dt> </dl>

 

