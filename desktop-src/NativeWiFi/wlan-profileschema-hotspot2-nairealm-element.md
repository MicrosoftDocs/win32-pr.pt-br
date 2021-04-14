---
description: Uma lista de identificadores de territórios da NAI (identificador de acesso à rede).
ms.assetid: e77802ee-4017-4f04-ae71-5d6d0de8fcf3
title: Elemento NAIRealm (Hotspot2)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NAIRealm
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a7c8fcf85bd23c13f0e7501d59c3db62c2bf82f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502235"
---
# <a name="nairealm-hotspot2-element"></a>Elemento NAIRealm (Hotspot2)

Uma lista de identificadores de territórios da NAI (identificador de acesso à rede). As entradas nessa lista geralmente são do formulário `user@domain` . A lista de territórios da NAI é o método preferencial para identificar a maioria dos operadores não móveis, como MSOs, operadores de conexão e locais públicos.

``` syntax
<xs:element name="NAIRealm"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                maxOccurs="256"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:minLength
                            value="1"
                         />
                        <xs:maxLength
                            value="255"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

O elemento é definido pelo elemento [**Hotspot2**](wlan-profileschema-hotspot2-element.md) .

## <a name="child-elements"></a>Elementos filho



| Elemento | Type | Descrição                                                   |
|---------|------|---------------------------------------------------------------|
| name    |      | Um único identificador de realm. Geralmente do formulário `user@domain` . |



 

 



