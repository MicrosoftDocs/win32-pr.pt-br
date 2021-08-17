---
title: Elemento string (StringTableType)
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
ms.openlocfilehash: 82eae0fa7007790995617b2c26bc5aff2bca720fb689b9ac468ef551d3400e05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136168"
---
# <a name="string-stringtabletype-element"></a>Elemento string (StringTableType)

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

O **elemento string** é definido pelo tipo complexo [**StringTableType.**](eventmanifestschema-stringtabletype-complextype.md)

## <a name="attributes"></a>Atributos



| Nome       | Tipo   | Descrição                                                                           |
|------------|--------|---------------------------------------------------------------------------------------|
| id         | string | Um identificador que identifica exclusivamente a cadeia de caracteres dentro da tabela de cadeia de caracteres.<br/> |
| Stringtype | string | Não usado.<br/>                                                                  |
| value      | string | A cadeia de caracteres localizada.<br/>                                                      |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Elemento pai**
</dt> <dt>

[**stringTable (LocalizationType)**](eventmanifestschema-stringtable-localizationtype-element.md)
</dt> </dl>

 

 





