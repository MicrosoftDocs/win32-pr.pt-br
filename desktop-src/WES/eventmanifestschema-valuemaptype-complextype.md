---
title: Tipo complexo ValueMapType
description: Define uma lista de mapeamentos de nome/valor entre valores inteiros e valores de cadeia de caracteres.
ms.assetid: 754578bf-d3c6-4467-af39-af56d5a11dce
keywords:
- Log de eventos do tipo complexo ValueMapType
topic_type:
- apiref
api_name:
- ValueMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c05452197fb71ca436fea4854346efa90f53ce6b3396e66af7e9b7ccb6615200
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120384"
---
# <a name="valuemaptype-complex-type"></a>Tipo complexo ValueMapType

Define uma lista de mapeamentos de nome/valor entre valores inteiros e valores de cadeia de caracteres.

``` syntax
<xs:complexType name="ValueMapType">
    <xs:sequence>
        <xs:element name="map"
            type="ValueMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                     | Type                                                                           | Descrição                                                                 |
|-------------------------------------------------------------|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [**mapeada**](eventmanifestschema-map-valuemaptype-element.md) | [**ValueMapValueType**](eventmanifestschema-valuemapvaluetype-complextype.md) | Define o mapeamento entre um valor inteiro e um valor de cadeia de caracteres.<br/> |



## <a name="attributes"></a>Atributos



| Nome   | Tipo                                                              | Descrição                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name   | string                                                            | O nome do mapa de valor. Use o nome em um elemento de dados para fazer referência aos mapeamentos.<br/>                                                                                                                                                                                                                     |
| símbolo | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | O símbolo a ser usado para fazer referência aos mapeamentos em seu aplicativo. O [**compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md) usa o símbolo para criar uma constante para o mapa no arquivo de cabeçalho que o compilador gera. Se você não especificar um símbolo, o compilador gerará um para você.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 





