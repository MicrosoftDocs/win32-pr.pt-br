---
title: Tipo complexo de corlocalizatype
description: Define um grupo de recursos localizados que você referencia em seu manifesto. | Tipo complexo de corlocalizatype
ms.assetid: fecab4e0-7136-4b13-8c24-bebbad0812e6
keywords:
- LogType tipo complexo EventLog
topic_type:
- apiref
api_name:
- LocalizationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cbb6911ea606ea30d8e656f20b4c566d4f6d0e08
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105800192"
---
# <a name="localizationtype-complex-type"></a>Tipo complexo de corlocalizatype

Define um grupo de recursos localizados que você referencia em seu manifesto.

``` syntax
<xs:complexType name="LocalizationType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="resources">
            <xs:complexType>
                <xs:choice
                    minOccurs="0"
                    maxOccurs="unbounded"
                >
                    <xs:element name="stringTable"
                        type="StringTableType"
                     />
                </xs:choice>
                <xs:attribute name="culture"
                    type="string"
                    use="required"
                 />
                <xs:anyAttribute
                    processContents="lax"
                    namespace="##other"
                 />
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            namespace="##other"
         />
    </xs:choice>
    <xs:attribute name="fallbackCulture"
        type="string"
        default="en-us"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                         | Type                                                                       | Description                                                                                                         |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**os**](eventmanifestschema-resources-localizationtype-element.md)     |                                                                            | Define um grupo de tabelas de cadeia que contém as cadeias de caracteres localizadas que você referencia em seu manifesto.<br/> |
| [**stringTable**](eventmanifestschema-stringtable-localizationtype-element.md) | [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) | Define uma lista de cadeias de caracteres localizadas que você pode referenciar em seu manifesto.<br/>                             |



## <a name="attributes"></a>Atributos



| Nome            | Tipo   | Description                                                                                                                                            |
|-----------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| culture         | string | Um nome de idioma que identifica a cultura das cadeias de caracteres localizadas na tabela de cadeias. Por exemplo, "en-US" para inglês (Estados Unidos).<br/> |
| fallbackCulture | string | Não usado.<br/>                                                                                                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





