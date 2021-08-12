---
title: Evento Player.MediaCollectionMediaRemoved
description: O evento MediaCollectionMediaRemoved ocorre quando um item de mídia é removido da biblioteca local. | Evento Player.MediaCollectionMediaRemoved
ms.assetid: a1df6faf-38dc-4f5f-8f8a-953c91ea026c
keywords:
- Evento MediaCollectionMediaRemoved Windows Media Player
- Evento MediaCollectionMediaRemoved Windows Media Player , classe Player
- Classe player Windows Media Player evento , MediaCollectionMediaRemoved
topic_type:
- apiref
api_name:
- Player.MediaCollectionMediaRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 009432040deace140dd3cf4d7d7da1246c0a38dbd9fc0da028832af137cefa83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572846"
---
# <a name="playermediacollectionmediaremoved-event"></a>Evento Player.MediaCollectionMediaRemoved

O evento MediaCollectionMediaRemoved ocorre quando um item de mídia é removido da biblioteca local.

## <a name="syntax"></a>Sintaxe


```JScript
Player.MediaCollectionMediaRemoved(
  pdispMedia
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pdispMedia* 
</dt> <dd>

**Objeto de** mídia que foi removido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse evento ocorre apenas para a biblioteca local.

**Windows Media Player 10 Mobile:** Não há suporte para esse evento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Player.mediaCollection**](player-mediacollection.md)
</dt> </dl>

 

 





