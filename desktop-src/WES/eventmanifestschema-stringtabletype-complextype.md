---
title: Tipo complexo StringTableType
description: Define uma lista de cadeias de caracteres localizadas que você pode referenciar em seu manifesto. | Tipo complexo StringTableType
ms.assetid: 47a59ff7-aaf6-4200-805b-0a8b5f57f101
keywords:
- Log de eventos do tipo complexo StringTableType
topic_type:
- apiref
api_name:
- StringTableType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9964c51524f7401afdfdd8a2da10cf43326bcae
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105763401"
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
| [**string**](eventmanifestschema-string-stringtabletype-element.md) |      | Define uma cadeia de caracteres localizada.<br/> |



## <a name="attributes"></a>Atributos



| Nome       | Tipo   | Descrição                                                                                                              |
|------------|--------|--------------------------------------------------------------------------------------------------------------------------|
| id         | string | Um identificador que identifica exclusivamente a cadeia de caracteres na tabela de cadeias de caracteres. Por exemplo, "Printer. Connection".<br/> |
| StringType | string | Não usado.<br/>                                                                                                     |
| value      | string | A cadeia de caracteres localizada.<br/>                                                                                         |



## <a name="remarks"></a>Comentários

Você pode fazer referência às cadeias de caracteres de qualquer tipo de manifesto que contenha o atributo Message. Para fazer referência a uma cadeia de caracteres com um StringType de "String" e uma ID de "Printer. Connection", use $ (String. Printer. Connection) como o valor do atributo Message.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





