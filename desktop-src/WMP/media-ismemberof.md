---
title: Método Media. isMemberOf
description: O método isMemberOf retorna um valor que indica se o item de mídia é um membro da playlist especificada.
ms.assetid: e620741f-6807-4a61-ba9b-f45426d6e33e
keywords:
- método isMemberOf Windows Media Player
- método isMemberOf Windows Media Player, classe de mídia
- Classe de mídia Windows Media Player, método isMemberOf
topic_type:
- apiref
api_name:
- Media.isMemberOf
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41555bd5910ddb3151468a458c5becbf247ea484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813476"
---
# <a name="mediaismemberof-method"></a>Método Media. isMemberOf

O método **isMemberOf** retorna um valor que indica se o item de mídia é um membro da playlist especificada.

## <a name="syntax"></a>Sintaxe


```JScript
bRetVal = Media.isMemberOf(
  playlist
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lista de reprodução* \[ no\]
</dt> <dd>

Objeto de **playlist** que pode conter o item de mídia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um **valor booleano**.

## <a name="remarks"></a>Comentários

Esse método não pode verificar as listas de reprodução recuperadas por meio do objeto **mediacollection** . Para testar se um item de mídia é membro de uma lista de reprodução nomeada específica, recupere a lista de reprodução com o *Player*. *playlistcollection*. **getByName**(*nome*). **Item**(0). Esse método também pode ser usado com playlists de CD e listas de reprodução de metarquivo.

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa *mídia*. **isMemberOf** para testar se o item de mídia atual é membro da playlist chamada playlist de exemplo. Se não for, o item de mídia atual será anexado à playlist de exemplo. O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Store the playlist object named Sample Playlist.
var sPlaylist = Player.playlistcollection.getbyname("Sample Playlist").item(0);

// Test whether the current media item is a member of Sample Playlist.
 var answer = ((Player.currentMedia.isMemberOf(sPlaylist))?"Yes":"No");

// If the current media item is not a member of Sample Playlist,
// append the current media item to the playlist.
if (answer == "No"){
   sPlaylist.appendItem(Player.currentMedia);
}

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Objeto playlist**](playlist-object.md)
</dt> <dt>

[**Objeto playlistcollection**](playlistcollection-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





