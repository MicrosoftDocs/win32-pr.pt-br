---
title: Método MediaCollection.getStringCollectionByQuery
description: O método getStringCollectionByQuery recupera um objeto StringCollection que contém todas as cadeias de caracteres que corresponderem às condições de consulta.
ms.assetid: 17442151-7eb1-4256-ac5f-142b11645216
keywords:
- Método getStringCollectionByQuery Windows Media Player
- Método getStringCollectionByQuery Windows Media Player classe , MediaCollection
- Classe MediaCollection Windows Media Player método , getStringCollectionByQuery
topic_type:
- apiref
api_name:
- MediaCollection.getStringCollectionByQuery
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d9e8f2eae2ce52a566d4db6b8298187df1d4d444432e99dda22d3cacc0ed3ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390106"
---
# <a name="mediacollectiongetstringcollectionbyquery-method"></a>Método MediaCollection.getStringCollectionByQuery

O **método getStringCollectionByQuery** recupera um objeto **StringCollection** que contém todas as cadeias de caracteres que corresponderem às condições de consulta.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = MediaCollection.getStringCollectionByQuery(
  attribute,
  query,
  mediaType,
  sortAttribute,
  sortAscending
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*atributo* \[ Em\]
</dt> <dd>

**Cadeia de** caracteres que contém o nome do atributo.

</dd> <dt>

*consulta* \[ Em\]
</dt> <dd>

**Objeto de** consulta.

</dd> <dt>

*mediaType* \[ Em\]
</dt> <dd>

**Cadeia de** caracteres que contém o tipo de mídia. Deve conter um dos seguintes valores: "audio", "video", "photo", "playlist" ou "other".

</dd> <dt>

*sortAttribute* \[ Em\]
</dt> <dd>

**Cadeia de** caracteres que contém o nome do atributo usado para classificação. Uma cadeia de caracteres vazia ("") significa que nenhuma classificação é aplicada.

</dd> <dt>

*sortAscending* \[ Em\]
</dt> <dd>

**Boolean**, true indicando que **StringCollection** deve ser classificação em ordem crescente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um **objeto StringCollection.**

## <a name="remarks"></a>Comentários

Consultas compostas que **usam Consulta não** são sensíveis a minúsculas.

Quando a consulta composta especificada pelo parâmetro *de* consulta contém uma condição criada no atributo **MediaType,** essa condição é ignorada. O valor do parâmetro *mediaType* é sempre usado. Por exemplo, se a consulta composta contiver a condição "MediaType Equals audio" e o valor do parâmetro *mediaType* for "video", a playlist resultante conterá apenas itens de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Atributo MediaType**](mediatype-attribute.md)
</dt> <dt>

[**Objeto Query**](query-object.md)
</dt> </dl>

 

 





