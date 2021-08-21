---
title: Evento Player. PlaylistCollectionPlaylistRemoved
description: O evento PlaylistCollectionPlaylistRemoved ocorre quando uma playlist é removida da coleção de playlist. | Evento Player. PlaylistCollectionPlaylistRemoved
ms.assetid: 2405be98-b4c2-4b4e-bea6-0c48a3e26f18
keywords:
- Windows Media Player de eventos PlaylistCollectionPlaylistRemoved
- Windows Media Player de eventos PlaylistCollectionPlaylistRemoved, classe Player
- classe de jogador Windows Media Player, evento PlaylistCollectionPlaylistRemoved
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 456f7598b9e1f1d2c2a6e76e58a0b06142980835c3c6d71d9ab10c2230ac386f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118337969"
---
# <a name="playerplaylistcollectionplaylistremoved-event"></a>Evento Player. PlaylistCollectionPlaylistRemoved

O evento **PlaylistCollectionPlaylistRemoved** ocorre quando uma playlist é removida da coleção de playlist.

## <a name="syntax"></a>Sintaxe


```JScript
Player.PlaylistCollectionPlaylistRemoved(
  bstrPlaylistName
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrPlaylistName* 
</dt> <dd>

**Cadeia de caracteres** que especifica o nome da lista de reprodução que foi removida.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

o valor dos parâmetros de evento é especificado por Windows Media Player e pode ser acessado ou passado para um método em um arquivo de JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

**Windows Media Player 10 Mobile:** Não há suporte para esse evento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> <dt>

[**Playlistcollection. getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





