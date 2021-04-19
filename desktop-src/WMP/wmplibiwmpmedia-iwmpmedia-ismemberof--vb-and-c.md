---
title: Método IWMPMedia isMemberOf
description: O método isMemberOf retorna um valor que indica se o item de mídia especificado é um membro da playlist especificada.
ms.assetid: 491e0dd5-38e5-47a5-9c94-f1d27d297f8d
keywords:
- método isMemberOf Windows Media Player
- método isMemberOf Windows Media Player, interface IWMPMedia
- Interface IWMPMedia Windows Media Player, método isMemberOf
topic_type:
- apiref
api_name:
- IWMPMedia.isMemberOf
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f627e9b2f0e1c4b226dda13d280d521ad52df2ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764602"
---
# <a name="iwmpmediaismemberof-method"></a>Método IWMPMedia:: isMemberOf

O método **isMemberOf** retorna um valor que indica se o item de mídia especificado é um membro da playlist especificada.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.Boolean isMemberOf(
  IWMPPlaylist pPlaylist
);
```


```VB

Public Function isMemberOf( _
  ByVal pPlaylist As IWMPPlaylist _
) As System.Boolean
Implements IWMPMedia.isMemberOf
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPlaylist* \[ no\]
</dt> <dd>

Uma interface **WMPLib. IWMPPlaylist** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um valor **System. Boolean** que indica se o item de mídia é um membro da playlist.

## <a name="remarks"></a>Comentários

Esse método não pode verificar as listas de reprodução recuperadas por meio da interface **IWMPMediaCollection** . Para testar se um item de mídia é membro de uma lista de reprodução nomeada específica, recupere a coleção de playlist com a propriedade **AxWindowsMediaPlayer. playlistcollection** . Depois de recuperar a coleção, recupere a lista de reprodução individual chamando o método **IWMPPlaylistCollection. getByName** .

Antes de chamar esse método, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir usa **isMemberOf** para testar se o item de mídia atual é um membro da lista de reprodução chamado todas as músicas. Se não for, o item de mídia atual será anexado à lista de reprodução. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
// Get an interface to the playlist named All Music.
WMPLib.IWMPPlaylist sPlaylist = player.playlistCollection.getByName("All Music").Item(0);

// Test whether the current media item is a member of the All Music playlist.
// If it is not a member, append the current media item to the playlist.
if (player.currentMedia.isMemberOf(sPlaylist) == false)
{
    sPlaylist.appendItem(player.currentMedia);
}
```


```VB

' Get an interface to the playlist named All Music.
Dim sPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;All Music&quot;).Item(0)

&#39; Test whether the current media item is a member of the All Music playlist.
&#39; If it is not a member, then append the current media item to the playlist.
If (player.currentMedia.isMemberOf(sPlaylist) = False) Then

    sPlaylist.appendItem(player.currentMedia)

End If
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AxWindowsMediaPlayer. playlistcollection (VB e C#)**](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. getByName (VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





