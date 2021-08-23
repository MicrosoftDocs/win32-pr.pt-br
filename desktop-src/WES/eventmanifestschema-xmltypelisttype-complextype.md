---
title: Tipo complexo XmlTypeListType
description: Define uma lista de tipos de saída que o serviço usa para determinar como renderizar um tipo de dados de entrada.
ms.assetid: d90b32cc-a0b5-44d1-8083-781aa5e10783
keywords:
- Tipo complexo XmlTypeListType EventLog
topic_type:
- apiref
api_name:
- XmlTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e30ca23a0e4ab0168ff7479a5246acfb4b34e3a43bc62886d988d5f54549672b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620316"
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
| [**Xmltype**](eventmanifestschema-xmltype-xmltypelisttype-element.md) |      | Define um tipo XML. <br/> |



## <a name="attributes"></a>Atributos



| Nome   | Tipo                                                              | Descrição                                                                                                                                                                                                                                                |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name   | **QName**                                                         | O nome do tipo de saída.<br/>                                                                                                                                                                                                                    |
| símbolo | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | O símbolo a ser usado para referenciar o tipo de saída em seu aplicativo. O [**compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md) usa o símbolo para criar uma constante para o tipo de saída no arquivo de header que o compilador gera.<br/> |
| value  | string                                                            | Um valor inteiro que identifica exclusivamente o tipo de saída na lista de tipos de saída que você define.<br/>                                                                                                                                          |



## <a name="remarks"></a>Comentários

O arquivoWinmeta.xml, que está incluído no \\ \\ SDK do Windows, contém uma lista de tipos de saída predefinidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





