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
ms.openlocfilehash: 5ad87b79175b0cecdec17ad081340fa0be2b90b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921736"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Instrumentação**](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype)
</dt> </dl>

 

