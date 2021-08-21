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
ms.openlocfilehash: 119ebe7f09f86aa46d9e80380670309fe8734fa818b48049d5dffc29e6a2ebb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863276"
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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Elemento pai**
</dt> <dt>

[**xmltypes (TypeListType)**](eventmanifestschema-xmltypes-typelisttype-element.md)
</dt> </dl>

 

 





