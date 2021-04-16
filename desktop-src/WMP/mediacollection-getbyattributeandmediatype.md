---
title: Método mediacollection. getByAttributeAndMediaType
description: O método getByAttributeAndMediaType recupera um objeto playlist contendo objetos de mídia com o tipo de mídia e o atributo especificados.
ms.assetid: 75241b38-ae0e-4216-b405-af9a9c71f5ec
keywords:
- método getByAttributeAndMediaType Windows Media Player
- método getByAttributeAndMediaType Windows Media Player, classe Mediacollection
- Classe mediacollection Windows Media Player, método getByAttributeAndMediaType
topic_type:
- apiref
api_name:
- MediaCollection.getByAttributeAndMediaType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e26abbf2f19d50ec6a10ebbafe12afae8576f34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751123"
---
# <a name="mediacollectiongetbyattributeandmediatype-method"></a>Método mediacollection. getByAttributeAndMediaType

O método **getByAttributeAndMediaType** recupera um objeto **playlist** contendo objetos de **mídia** com o tipo de mídia e o atributo especificados.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = MediaCollection.getByAttributeAndMediaType(
  attribute,
  value,
  mediaType
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*atributo* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que contém o atributo.

</dd> <dt>

*valor* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que contém o valor.

</dd> <dt>

*MediaType* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que contém o tipo de mídia. Deve conter um dos seguintes valores: "áudio", "vídeo", "foto", "playlist" ou "outros".

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um objeto **playlist**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> <dt>

[**Objeto mediacollection**](mediacollection-object.md)
</dt> <dt>

[**Objeto playlist**](playlist-object.md)
</dt> </dl>

 

 





