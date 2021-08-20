---
title: Método MediaCollection.getPlaylistByQuery
description: O método getPlaylistByQuery recupera um objeto Playlist que contém objetos media que corresponderem às condições de consulta.
ms.assetid: 3487d442-a5bb-4519-ac45-d0138516305e
keywords:
- Método getPlaylistByQuery Windows Media Player
- Método getPlaylistByQuery Windows Media Player classe , MediaCollection
- Classe MediaCollection Windows Media Player , método getPlaylistByQuery
topic_type:
- apiref
api_name:
- MediaCollection.getPlaylistByQuery
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47f64f054fe59865fb8d213d343696c86d83a5f8698d498c854660f76dc9085f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118837139"
---
# <a name="mediacollectiongetplaylistbyquery-method"></a>Método MediaCollection.getPlaylistByQuery

O **método getPlaylistByQuery** recupera um objeto **Playlist** que contém objetos **media** que corresponderem às condições de consulta.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = MediaCollection.getPlaylistByQuery(
  query,
  mediaType,
  sortAttribute,
  sortAscending
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*consulta* \[ Em\]
</dt> <dd>

**Objeto de** consulta que define as condições usadas para criar a playlist.

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

**Booliana**, true indicando que a playlist deve ser classificação em ordem crescente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um **objeto Playlist.**

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

 

 





