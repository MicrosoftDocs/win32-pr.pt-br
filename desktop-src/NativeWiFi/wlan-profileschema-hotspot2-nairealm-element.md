---
description: Uma lista de identificadores de Realm do NAI (Identificador de Acesso à Rede).
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
ms.openlocfilehash: 084ee3ce04a560ce50c3ab0391f808bc09aed1bb90da6a34b86755b9b64ae772
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684206"
---
# <a name="nairealm-hotspot2-element"></a>Elemento NAIRealm (Hotspot2)

Uma lista de identificadores de Realm do NAI (Identificador de Acesso à Rede). As entradas nesta lista geralmente são do formato `user@domain` . A lista Realm da NAI é o método preferencial para identificar a maioria dos operadores não móveis, como MSOs, operadores de linha de transmissão e locais públicos.

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

O elemento é definido pelo [**elemento Hotspot2.**](wlan-profileschema-hotspot2-element.md)

## <a name="child-elements"></a>Elementos filho



| Elemento | Type | Descrição                                                   |
|---------|------|---------------------------------------------------------------|
| name    |      | Um único identificador de realm. Geralmente do formato `user@domain` . |



 

 



