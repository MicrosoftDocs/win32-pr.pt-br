---
title: Elemento resources (Localizatype)
description: Define um grupo de tabelas de cadeia que contém as cadeias de caracteres localizadas que você referencia em seu manifesto.
ms.assetid: b984894a-0ae8-49be-af93-3acdcce53ee9
keywords:
- Log de elementos de recursos
topic_type:
- apiref
api_name:
- resources
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55bdfe504da08c754c18b790e282eba6787c3ee3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105789598"
---
# <a name="resources-localizationtype-element"></a>Elemento resources (Localizatype)

Define um grupo de tabelas de cadeia que contém as cadeias de caracteres localizadas que você referencia em seu manifesto.

``` syntax
<xs:element name="resources">
    <xs:complexType>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="stringTable"
                type="StringTableType"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                namespace="##other"
             />
        </xs:choice>
        <xs:attribute name="culture"
            type="string"
            default="##fallback"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

O elemento **Resources** é definido pelo tipo complexo de [**corlocalizatype**](eventmanifestschema-localizationtype-complextype.md) .

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                  | Type                                                                       | Descrição                                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**stringTable**](eventmanifestschema-stringtable-resources-element.md) | [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) | Define uma lista de cadeias de caracteres localizadas que você pode referenciar em seu manifesto.<br/> |



## <a name="attributes"></a>Atributos



| Nome    | Tipo   | Descrição                                                                                                                                            |
|---------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| culture | string | Um nome de idioma que identifica a cultura das cadeias de caracteres localizadas na tabela de cadeias. Por exemplo, "en-US" para inglês (Estados Unidos).<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Elemento pai**
</dt> <dt>

[**localização (instrumentationManifest)**](eventmanifestschema-localization-instrumentationmanifest-element.md)
</dt> </dl>

 

 





