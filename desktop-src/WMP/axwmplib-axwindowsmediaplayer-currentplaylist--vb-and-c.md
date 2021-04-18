---
title: Propriedade AxWindowsMediaPlayer. currentPlaylist
description: A propriedade currentPlaylist Obtém ou define a interface IWMPPlaylist atual que fornece uma maneira fácil de organizar e manipular itens de mídia em uma lista.
ms.assetid: d5a9f126-a628-499c-a012-8a47c6c987ef
keywords:
- Propriedade currentPlaylist Windows Media Player
- Propriedade currentPlaylist Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer do Windows Media Player, Propriedade currentPlaylist
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0f5b91a2e65b81fd1f13da0bad5f77c5ea1415
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783633"
---
# <a name="axwindowsmediaplayercurrentplaylist-property"></a>Propriedade AxWindowsMediaPlayer. currentPlaylist

A propriedade currentPlaylist Obtém ou define a interface **IWMPPlaylist** atual que fornece uma maneira fácil de organizar e manipular itens de mídia em uma lista.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylist currentPlaylist {get; set;}
```


```VB

Public Property currentPlaylist As IWMPPlaylist
```





## <a name="property-value"></a>Valor da propriedade

A interface WMPLib. IWMPPlaylist que fornece acesso à playlist atual.

## <a name="remarks"></a>Comentários

Se a propriedade IWMPSettings. AutoStart (também acessada via AxWindowsMediaPlayer. Settings.**AutoStart**) é true, a reprodução é iniciada automaticamente sempre que você definir **currentPlaylist**.

Essa propriedade usa uma interface IWMPPlaylist, que pode ser adquirida de várias maneiras, como ao obter o valor do *IWMPPlaylistArray*. **Item** ou *IWMPPlaylistCollection*. Propriedades **newPlaylist** . Para carregar um item da **playlist** usando um nome de arquivo, defina a propriedade URL ou use AxWindowsMediaPlayer. **newPlaylist**.

## <a name="examples"></a>Exemplos

O exemplo a seguir recupera a primeira lista de reprodução na biblioteca e usa a propriedade currentPlaylist para definir a lista de reprodução recuperada como a playlist atual e exibir seu nome. O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.


```CSharp
// Get an interface to the first playlist from the library. 
WMPLib.IWMPPlaylist firstPlaylist = player.playlistCollection.getAll().Item(0);

// Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist;

// Display the name of the current playlist.
currentPlaylistLabel.Text = ("Found first playlist. Name = " + player.currentPlaylist.name);
```


```VB

' Get an interface to the first playlist from the library. 
Dim firstPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getAll().Item(0)

&#39; Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist

&#39; Display the name of the current playlist.
currentPlaylistLabel.Text = (&quot;Found first playlist. Name = &quot; + player.currentPlaylist.name)
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. newPlaylist (VB e C#)**](axwmplib-axwindowsmediaplayer-newplaylist.md)
</dt> <dt>

[**AxWindowsMediaPlayer. Settings (VB e C#)**](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistArray. Item (VB e C#)**](wmplibiwmpplaylistarray-iwmpplaylistarray-item--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. newPlaylist (VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. AutoStart (VB e C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





