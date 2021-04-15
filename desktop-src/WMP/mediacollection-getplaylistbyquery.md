---
title: Método mediacollection. getPlaylistByQuery
description: O método getPlaylistByQuery recupera um objeto playlist contendo objetos de mídia que correspondem às condições de consulta.
ms.assetid: 3487d442-a5bb-4519-ac45-d0138516305e
keywords:
- método getPlaylistByQuery Windows Media Player
- método getPlaylistByQuery Windows Media Player, classe Mediacollection
- Classe mediacollection Windows Media Player, método getPlaylistByQuery
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
ms.openlocfilehash: 50b57d4303ba8784f912db9570faacb26d01677d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761436"
---
# <a name="mediacollectiongetplaylistbyquery-method"></a>Método mediacollection. getPlaylistByQuery

O método **getPlaylistByQuery** recupera um objeto **playlist** contendo objetos de **mídia** que correspondem às condições de consulta.

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

*consulta* \[ do no\]
</dt> <dd>

Objeto de **consulta** que define as condições usadas para criar a lista de reprodução.

</dd> <dt>

*MediaType* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que contém o tipo de mídia. Deve conter um dos seguintes valores: "áudio", "vídeo", "foto", "playlist" ou "outros".

</dd> <dt>

*tipo de classificação* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que contém o nome do atributo usado para classificação. Uma cadeia de caracteres vazia ("") significa que nenhuma classificação é aplicada.

</dd> <dt>

*sortAscending* \[ no\]
</dt> <dd>

**Booliano**, verdadeiro indicando que a lista de reprodução deve ser classificada em ordem crescente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um objeto **playlist** .

## <a name="remarks"></a>Comentários

Consultas compostas usando a **consulta** não diferenciam maiúsculas de minúsculas.

Quando a consulta composta especificada pelo parâmetro de *consulta* contém uma condição criada no atributo **MediaType** , essa condição é ignorada. O valor do parâmetro *MediaType* é sempre usado. Por exemplo, se a consulta composta contiver a condição "MediaType igual a áudio" e o valor do parâmetro *MediaType* for "vídeo", a lista de reprodução resultante conterá apenas itens de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto mediacollection**](mediacollection-object.md)
</dt> <dt>

[**Atributo MediaType**](mediatype-attribute.md)
</dt> <dt>

[**Objeto de consulta**](query-object.md)
</dt> </dl>

 

 





