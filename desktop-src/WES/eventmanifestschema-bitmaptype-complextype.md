---
title: Tipo complexo de BitMaptype
description: Define uma lista de mapeamentos de nome/valor entre valores de bits e valores de cadeia de caracteres.
ms.assetid: 65dc6a48-878c-415c-872c-41dc27691b7f
keywords:
- EventLog do tipo complexo de BitMaptype
topic_type:
- apiref
api_name:
- BitMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef3a48b102b9ab36ef492fcd38c4bb8b2560d5fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455979"
---
# <a name="bitmaptype-complex-type"></a>Tipo complexo de BitMaptype

Define uma lista de mapeamentos de nome/valor entre valores de bits e valores de cadeia de caracteres.

``` syntax
<xs:complexType name="BitMapType">
    <xs:sequence>
        <xs:element name="map"
            type="BitMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                   | Type                                                                       | Descrição                                                            |
|-----------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**mapeada**](eventmanifestschema-map-bitmaptype-element.md) | [**BitMapValueType**](eventmanifestschema-bitmapvaluetype-complextype.md) | Define o mapeamento entre um valor de bit e um valor de cadeia de caracteres.<br/> |



## <a name="attributes"></a>Atributos



| Nome   | Tipo                                                              | Descrição                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name   | string                                                            | O nome do bitmap.<br/>                                                                                                                                                                                                                                                                                  |
| símbolo | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | O símbolo a ser usado para fazer referência aos mapeamentos em seu aplicativo. O [**compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md) usa o símbolo para criar uma constante para o mapa no arquivo de cabeçalho que o compilador gera. Se você não especificar um símbolo, o compilador gerará um para você.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





