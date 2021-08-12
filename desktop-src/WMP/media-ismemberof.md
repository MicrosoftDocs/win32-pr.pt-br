---
title: Método Media. isMemberOf
description: O método isMemberOf retorna um valor que indica se o item de mídia é um membro da playlist especificada.
ms.assetid: e620741f-6807-4a61-ba9b-f45426d6e33e
keywords:
- Windows Media Player do método isMemberOf
- método isMemberOf Windows Media Player, classe Media
- classe de mídia Windows Media Player, método isMemberOf
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
ms.openlocfilehash: ef9fc5eb55a306dad8b9d5de6d6501b615a9156c026c8e0fc12664795a23ab21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574798"
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

o exemplo a seguir JScript usa *mídia*. **isMemberOf** para testar se o item de mídia atual é membro da playlist chamada playlist de exemplo. Se não for, o item de mídia atual será anexado à playlist de exemplo. O objeto de **jogador** foi criado com ID = "Player".


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

[**Configurações. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





