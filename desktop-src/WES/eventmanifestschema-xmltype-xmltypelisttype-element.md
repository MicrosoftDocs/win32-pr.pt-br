---
title: Elemento xmlType (XmlTypeListType)
description: Define um tipo XML.
ms.assetid: 4443963f-f47a-4371-87d8-58f508ba15d6
keywords:
- EventLog do elemento xmlType
topic_type:
- apiref
api_name:
- xmlType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5aa37214c5efc0dee9e788ad10ed2f437e3df19f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811370"
---
# <a name="xmltype-xmltypelisttype-element"></a>Elemento xmlType (XmlTypeListType)

Define um tipo XML.

``` syntax
<xs:element name="xmlType">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="XmlType"
            >
                <xs:attribute name="name"
                    type="QName"
                    use="required"
                 />
                <xs:attribute name="value"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="symbol"
                    type="string"
                    use="required"
                 />
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

O elemento **xmlType** é definido pelo tipo complexo [**XmlTypeListType**](eventmanifestschema-xmltypelisttype-complextype.md) .

## <a name="attributes"></a>Atributos



| Nome   | Tipo      | Descrição                                                                                                                                                                                                                                                |
|--------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name   | **QName** | O nome do tipo de saída.<br/>                                                                                                                                                                                                                    |
| símbolo | string    | O símbolo a ser usado para referenciar o tipo de saída em seu aplicativo. O [**compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md) usa o símbolo para criar uma constante para o tipo de saída no arquivo de cabeçalho que o compilador gera.<br/> |
| value  | string    | Um valor inteiro que identifica exclusivamente o tipo de saída na lista de tipos de saída que você define.<br/>                                                                                                                                          |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Elemento pai**
</dt> <dt>

[**xmltypes (TypeListType)**](eventmanifestschema-xmltypes-typelisttype-element.md)
</dt> </dl>

 

 





