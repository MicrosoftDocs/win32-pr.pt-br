---
title: Tipo complexo XmlTypeListType
description: Define uma lista de tipos de saída que o serviço usa para determinar como renderizar um tipo de dados de entrada.
ms.assetid: d90b32cc-a0b5-44d1-8083-781aa5e10783
keywords:
- Log de eventos do tipo complexo XmlTypeListType
topic_type:
- apiref
api_name:
- XmlTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 388161572ec9c84ed46d5b40987df5fb8d1ed077
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295807"
---
# <a name="xmltypelisttype-complex-type"></a>Tipo complexo XmlTypeListType

Define uma lista de tipos de saída que o serviço usa para determinar como renderizar um tipo de dados de entrada.

``` syntax
<xs:complexType name="XmlTypeListType">
    <xs:sequence>
        <xs:element name="xmlType"
            minOccurs="0"
            maxOccurs="unbounded"
        >
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
                            type="CSymbolType"
                            use="required"
                         />
                    </xs:extension>
                </xs:complexContent>
            </xs:complexType>
        </xs:element>
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                | Type | Descrição                      |
|------------------------------------------------------------------------|------|----------------------------------|
| [**xmlType**](eventmanifestschema-xmltype-xmltypelisttype-element.md) |      | Define um tipo XML. <br/> |



## <a name="attributes"></a>Atributos



| Nome   | Tipo                                                              | Descrição                                                                                                                                                                                                                                                |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name   | **QName**                                                         | O nome do tipo de saída.<br/>                                                                                                                                                                                                                    |
| símbolo | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | O símbolo a ser usado para referenciar o tipo de saída em seu aplicativo. O [**compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md) usa o símbolo para criar uma constante para o tipo de saída no arquivo de cabeçalho que o compilador gera.<br/> |
| value  | string                                                            | Um valor inteiro que identifica exclusivamente o tipo de saída na lista de tipos de saída que você define.<br/>                                                                                                                                          |



## <a name="remarks"></a>Comentários

O \\ arquivo de inclusão \\Winmeta.xml, que está incluído na SDK do Windows, contém uma lista de tipos de saída predefinidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





