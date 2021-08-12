---
title: Evento Player.PlaylistCollectionPlaylistAdded
description: O evento PlaylistCollectionPlaylistAdded ocorre quando uma playlist é adicionada à coleção de playlists. | Evento Player.PlaylistCollectionPlaylistAdded
ms.assetid: 07acb5e6-d832-4f0b-a6bb-2b7ba27c368d
keywords:
- Evento PlaylistCollectionPlaylistAdded Windows Media Player
- Evento PlaylistCollectionPlaylistAdded Windows Media Player , classe Player
- Classe player Windows Media Player evento , PlaylistCollectionPlaylistAdded
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e72dcacbb60c141348a295fe086957b1404475e9e3be90433f8bdbe816fc834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572585"
---
# <a name="playerplaylistcollectionplaylistadded-event"></a>Evento Player.PlaylistCollectionPlaylistAdded

O **evento PlaylistCollectionPlaylistAdded** ocorre quando uma playlist é adicionada à coleção de playlists.

## <a name="syntax"></a>Sintaxe


```JScript
Player.PlaylistCollectionPlaylistAdded(
  bstrPlaylistName
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrPlaylistName* 
</dt> <dd>

**Cadeia** de caracteres que especifica o nome da playlist que foi adicionada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

O nome da playlist que foi adicionada pode ser usado para recuperar o objeto **Playlist** correspondente usando *PlaylistCollection*. **Método getByName.**

O valor dos parâmetros de evento é especificado por Windows Media Player e pode ser acessado ou passado para um método em um arquivo JScript importado usando o nome do parâmetro especificado. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

**Windows Media Player 10 Mobile:** Não há suporte para esse evento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





