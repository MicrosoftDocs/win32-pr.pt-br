---
title: Tipo complexo StringTableType
description: Define uma lista de cadeias de caracteres localizadas que você pode referenciar em seu manifesto. | Tipo complexo StringTableType
ms.assetid: 47a59ff7-aaf6-4200-805b-0a8b5f57f101
keywords:
- Tipo complexo StringTableType EventLog
topic_type:
- apiref
api_name:
- StringTableType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5d52f19ca01a926c82fcc1e13cc7191866722ba5e0e6eef81e916e244744783
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342980"
---
# <a name="stringtabletype-complex-type"></a>Tipo complexo StringTableType

Define uma lista de cadeias de caracteres localizadas que você pode referenciar em seu manifesto.

``` syntax
<xs:complexType name="StringTableType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="string">
            <xs:complexType
                mixed="true"
            >
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
    </xs:choice>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                              | Type | Descrição                            |
|----------------------------------------------------------------------|------|----------------------------------------|
| [**String**](eventmanifestschema-string-stringtabletype-element.md) |      | Define uma cadeia de caracteres localizada.<br/> |



## <a name="attributes"></a>Atributos



| Nome       | Tipo   | Descrição                                                                                                              |
|------------|--------|--------------------------------------------------------------------------------------------------------------------------|
| id         | string | Um identificador que identifica exclusivamente a cadeia de caracteres dentro da tabela de cadeia de caracteres. Por exemplo, "Printer.Connection".<br/> |
| Stringtype | string | Não usado.<br/>                                                                                                     |
| value      | string | A cadeia de caracteres localizada.<br/>                                                                                         |



## <a name="remarks"></a>Comentários

Você pode referenciar as cadeias de caracteres de qualquer tipo de manifesto que contenha o atributo de mensagem. Para referenciar uma cadeia de caracteres com um stringType de "string" e uma ID de "Printer.Connection", use $(string. Printer.Connection) como o valor do atributo de mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





