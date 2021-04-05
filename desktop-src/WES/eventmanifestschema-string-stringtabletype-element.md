---
title: Elemento String (StringTableType)
description: Define uma cadeia de caracteres localizada.
ms.assetid: 845476a9-bcf4-4821-824c-06c9a9f64649
keywords:
- elemento string EventLog
topic_type:
- apiref
api_name:
- string
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c46fc43366d6472e8047b529d847eefd5369c263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918636"
---
# <a name="string-stringtabletype-element"></a>Elemento String (StringTableType)

Define uma cadeia de caracteres localizada.

``` syntax
<xs:element name="string">
    <xs:complexType>
        <xs:attribute name="id"
            type="string"
            use="required"
         />
        <xs:attribute name="value"
            type="string"
            use="required"
         />
        <xs:attribute name="stringType"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

O elemento **String** é definido pelo tipo complexo [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) .

## <a name="attributes"></a>Atributos



| Nome       | Tipo   | Descrição                                                                           |
|------------|--------|---------------------------------------------------------------------------------------|
| id         | string | Um identificador que identifica exclusivamente a cadeia de caracteres na tabela de cadeias de caracteres.<br/> |
| StringType | string | Não usado.<br/>                                                                  |
| value      | string | A cadeia de caracteres localizada.<br/>                                                      |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Elemento pai**
</dt> <dt>

[**stringTable (corlocalizatype)**](eventmanifestschema-stringtable-localizationtype-element.md)
</dt> </dl>

 

 





