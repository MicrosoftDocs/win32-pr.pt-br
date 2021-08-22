---
title: Propriedade AxWindowsMediaPlayer. currentMedia
description: A propriedade currentMedia Obtém ou define a interface IWMPMedia que corresponde ao item de mídia atual.
ms.assetid: 814ccb1d-713d-4b91-b225-d2199a7c9b6b
keywords:
- Windows Media Player da propriedade currentMedia
- propriedade currentMedia Windows Media Player, classe AxWindowsMediaPlayer
- classe AxWindowsMediaPlayer Windows Media Player, propriedade currentMedia
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027949872b2ff988fcfcad5a8464d9a48ed69d3389ddbca0ad4f91b2d9e3c8d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098836"
---
# <a name="axwindowsmediaplayercurrentmedia-property"></a>Propriedade AxWindowsMediaPlayer. currentMedia

A propriedade currentMedia Obtém ou define a interface IWMPMedia que corresponde ao item de mídia atual.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPMedia currentMedia {get; set;}
```


```VB

Public Property currentMedia As IWMPMedia
```





## <a name="property-value"></a>Valor da propriedade

A interface WMPLib. IWMPMedia que fornece acesso ao item de mídia atual.

## <a name="remarks"></a>Comentários

Se AxWindowsMediaPlayer. Settings. a propriedade **AutoStart** é true, a reprodução é iniciada automaticamente sempre que você definir **currentMedia**.

Você pode recuperar uma interface IWMPMedia para um determinado item de mídia por meio da propriedade IWMPPlaylist. Item (o método IWMPPlaylist. get \_ item em C#). Para carregar um item de mídia usando um nome de arquivo, defina a propriedade URL ou use newMedia.

## <a name="examples"></a>Exemplos

O exemplo a seguir recupera o primeiro item de mídia na biblioteca e usa a propriedade currentMedia para definir o item de mídia recuperado como o item de mídia atual e exibir seu nome. O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.


```CSharp
// Get an interface to the first media item in the library. 
WMPLib.IWMPMedia3 firstMedia = (WMPLib.IWMPMedia3)player.mediaCollection.getAll().get_Item(0);

// Make the retrieved media item the current media item.
player.currentMedia = firstMedia;

// Display the name of the current media item.
currentMediaLabel.Text = ("Found first media item. Name = " + player.currentMedia.name);
```


```VB

' Get an interface to the first media item in the library. 
Dim firstMedia As WMPLib.IWMPMedia3 = player.mediaCollection.getAll().Item(0)

&#39; Make the retrieved media item the current media item.
player.currentMedia = firstMedia

&#39; Display the name of the current media item.
currentMediaLabel.Text = (&quot;Found first media item. Name = &quot; + player.currentMedia.name)
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

[**AxWindowsMediaPlayer. newMedia (VB e C#)**](axwmplib-axwindowsmediaplayer-newmedia.md)
</dt> <dt>

[**AxWindowsMediaPlayer. URL (VB e C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. Item (VB e C#)**](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. AutoStart (VB e C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





