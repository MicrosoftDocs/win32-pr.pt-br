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
ms.openlocfilehash: dc59103a1a98b0baf1559ead159221ea42288936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756697"
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
| name | [**homem: CSymbolType**](performance-counters-csymboltype-simple-type.md) | O nome da estrutura.<br/>                                                                                                            |
| tipo | [**homem: CSymbolType**](performance-counters-csymboltype-simple-type.md) | Um nome simbólico que identifica a estrutura. A ferramenta [ctrpp](ctrpp.md) cria uma variável de struct com esse nome que você pode usar.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 




