---
title: Tipo complexo MapType
description: Define uma lista de pares de nome/valor.
ms.assetid: 208ae219-8f79-4049-b946-a57b33c97b1b
keywords:
- Log de eventos do tipo complexo MapType
topic_type:
- apiref
api_name:
- MapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4daf6cfe677ab5585ac580e19c868f1bba17de45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644372"
---
# <a name="maptype-complex-type"></a>Tipo complexo MapType

Define uma lista de pares de nome/valor.

``` syntax
<xs:complexType name="MapType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="valueMap"
            type="ValueMapType"
         />
        <xs:element name="bitMap"
            type="BitMapType"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                          | Type                                                                 | Descrição                                                                              |
|------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**bitMap**](eventmanifestschema-bitmap-maptype-element.md)     | [**BitMaptype**](eventmanifestschema-bitmaptype-complextype.md)     | Define uma lista de pares de nome/valor que mapeia valores de bits e valores de cadeia de caracteres.<br/>     |
| [**valueMap**](eventmanifestschema-valuemap-maptype-element.md) | [**ValueMapType**](eventmanifestschema-valuemaptype-complextype.md) | Define uma lista de pares de nome/valor que mapeia valores inteiros e valores de cadeia de caracteres.<br/> |



## <a name="remarks"></a>Comentários

Normalmente, você cria mapas para fornecer valores de cadeia de caracteres enumerados para dados de eventos.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como especificar um mapa de valor e bitmap.


```XML
<maps>
   <valueMap name="MyValueMap">
       <map value="5" message="$(string.value5)"/>
       <map value="45" message="$(string.value45)"/>
   </valueMap>
 
   <bitMap name="MyBitmap">
       <map value="0x8" message="$(string.bit3)/>
       <map value="0x80" message="$(string.bit7)/>
   </bitMap>
</maps>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





