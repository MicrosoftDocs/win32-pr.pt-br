---
description: Define uma estrutura que contém um ou mais valores de contador.
ms.assetid: 3085d490-4ac1-491c-bce0-8af46b16fab9
title: Tipo complexo de struct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 29796a259810cd03739c45338709966bd765f0c1fd9026777f435acb2c5de253
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978846"
---
# <a name="struct-complex-type"></a>Tipo complexo de struct

Define uma estrutura que contém um ou mais valores de contador.

``` syntax
<xs:complexType name="struct">
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="man:CSymbolType"
                use="required"
             />
            <xs:attribute name="type"
                type="man:CSymbolType"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Atributos



| Nome | Tipo                                                                    | Descrição                                                                                                                                      |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| name | [**man:CSymbolType**](performance-counters-csymboltype-simple-type.md) | O nome da estrutura.<br/>                                                                                                            |
| tipo | [**man:CSymbolType**](performance-counters-csymboltype-simple-type.md) | Um nome simbólico que identifica a estrutura. A [ferramenta CTRPP](ctrpp.md) cria uma variável de struct com esse nome que você pode usar.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 




