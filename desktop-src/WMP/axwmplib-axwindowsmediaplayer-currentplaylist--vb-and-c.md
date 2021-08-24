---
title: Propriedade AxWindowsMediaPlayer.currentPlaylist
description: A propriedade currentPlaylist obtém ou define a interface IWMPPlaylist atual que fornece uma maneira fácil de organizar e manipular itens de mídia em uma lista.
ms.assetid: d5a9f126-a628-499c-a012-8a47c6c987ef
keywords:
- propriedade currentPlaylist Windows Media Player
- propriedade currentPlaylist Windows Media Player , classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player , propriedade currentPlaylist
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
ms.openlocfilehash: f976084773a333e40c0a278878e9a35ed913e5911ec732c0dccfe6525e5f45a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765256"
---
# <a name="axwindowsmediaplayercurrentplaylist-property"></a>Propriedade AxWindowsMediaPlayer.currentPlaylist

A propriedade currentPlaylist obtém ou define a interface **IWMPPlaylist** atual que fornece uma maneira fácil de organizar e manipular itens de mídia em uma lista.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylist currentPlaylist {get; set;}
```


```VB

Public Property currentPlaylist As IWMPPlaylist
```





## <a name="property-value"></a>Valor da propriedade

A interface WMPLib.IWMPPlaylist que fornece acesso à playlist atual.

## <a name="remarks"></a>Comentários

Se a propriedade IWMPSettings.autoStart (também acessada por meio de AxWindowsMediaPlayer.settings).**autoStart**) é true, a reprodução começa automaticamente sempre que você definir **currentPlaylist**.

Essa propriedade aceita uma interface IWMPPlaylist, que pode ser adquirida de várias maneiras, como ao obter o valor de *IWMPPlaylistArray.* **Item** ou *IWMPPlaylistCollection.* **propriedades newPlaylist.** Para carregar um **item de** playlist usando um nome de arquivo, de definir a propriedade URL ou usar AxWindowsMediaPlayer. **newPlaylist**.

## <a name="examples"></a>Exemplos

O exemplo a seguir recupera a primeira playlist na biblioteca e usa a propriedade currentPlaylist para definir a playlist recuperada como a playlist atual e exibir seu nome. O objeto AxWMPLib.AxWindowsMediaPlayer é representado pela variável chamada player.


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
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.newPlaylist (VB e C#)**](axwmplib-axwindowsmediaplayer-newplaylist.md)
</dt> <dt>

[**AxWindowsMediaPlayer.settings (VB e C#)**](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistArray.Item (VB e C#)**](wmplibiwmpplaylistarray-iwmpplaylistarray-item--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection.newPlaylist (VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.autoStart (VB e C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





