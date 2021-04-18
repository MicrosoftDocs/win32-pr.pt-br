---
title: Evento Player. PlaylistCollectionPlaylistAdded
description: O evento PlaylistCollectionPlaylistAdded ocorre quando uma playlist é adicionada à coleção de playlist. | Evento Player. PlaylistCollectionPlaylistAdded
ms.assetid: 07acb5e6-d832-4f0b-a6bb-2b7ba27c368d
keywords:
- Evento PlaylistCollectionPlaylistAdded do Windows Media Player
- Evento PlaylistCollectionPlaylistAdded Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento PlaylistCollectionPlaylistAdded
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
ms.openlocfilehash: 6e6a229aff95d29ae93433dab538521d88c50c1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784548"
---
# <a name="playerplaylistcollectionplaylistadded-event"></a>Evento Player. PlaylistCollectionPlaylistAdded

O evento **PlaylistCollectionPlaylistAdded** ocorre quando uma playlist é adicionada à coleção de playlist.

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

**Cadeia de caracteres** que especifica o nome da lista de reprodução que foi adicionada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

O nome da lista de reprodução que foi adicionado pode ser usado para recuperar o objeto de **playlist** correspondente usando a *playlistcollection*. método **getByName** .

O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

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

 

 





