---
title: Evento Player. MediaCollectionMediaRemoved
description: O evento MediaCollectionMediaRemoved ocorre quando um item de mídia é removido da biblioteca local. | Evento Player. MediaCollectionMediaRemoved
ms.assetid: a1df6faf-38dc-4f5f-8f8a-953c91ea026c
keywords:
- Evento MediaCollectionMediaRemoved do Windows Media Player
- Evento MediaCollectionMediaRemoved Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento MediaCollectionMediaRemoved
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
ms.openlocfilehash: 72af5fe4c5e90effeb34745ea71e3edb457da357
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763331"
---
# <a name="playermediacollectionmediaremoved-event"></a>Evento Player. MediaCollectionMediaRemoved

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

O objeto de **mídia** que foi removido.

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

[**Objeto mediacollection**](mediacollection-object.md)
</dt> <dt>

[**Objeto de jogador**](player-object.md)
</dt> <dt>

[**Player. mediacollection**](player-mediacollection.md)
</dt> </dl>

 

 





