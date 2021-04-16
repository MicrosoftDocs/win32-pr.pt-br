---
title: Método IWMPMediaCollection getByAlbum
description: O método getByAlbum retorna uma interface IWMPPlaylist que fornece acesso a itens de mídia do álbum especificado.
ms.assetid: 26f004c0-de46-4792-8212-9d4ac749bb21
keywords:
- método getByAlbum Windows Media Player
- método getByAlbum Windows Media Player, interface IWMPMediaCollection
- Interface IWMPMediaCollection Windows Media Player, método getByAlbum
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAlbum
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c455e9bd61038a4d72bb6537d7c62b30a5d0b733
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758264"
---
# <a name="iwmpmediacollectiongetbyalbum-method"></a>Método IWMPMediaCollection:: getByAlbum

O método **getByAlbum** retorna uma interface **IWMPPlaylist** que fornece acesso a itens de mídia do álbum especificado.

## <a name="syntax"></a>Sintaxe


```CSharp
public IWMPPlaylist getByAlbum(
  System.String bstrAlbum
);
```


```VB

Public Function getByAlbum( _
  ByVal bstrAlbum As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAlbum
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrAlbum* \[ no\]
</dt> <dd>

O **System. String** que é o título do álbum.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Uma interface **WMPLib. IWMPPlaylist** para os itens de mídia recuperados.

## <a name="remarks"></a>Comentários

Antes de chamar esse método, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

Há duas maneiras de recuperar uma interface **IWMPMediaCollection** , e o comportamento do método **getByAlbum** depende de quais dessas duas maneiras você usa. Se você recuperar a interface chamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), o método **getByAlbum** retornará todos os itens de mídia na biblioteca. No entanto, se você recuperar a interface chamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), o método **getByAlbum** retornará apenas os itens de áudio na biblioteca que pertencem ao álbum especificado.

## <a name="examples"></a>Exemplos

O exemplo a seguir usa **getByAlbum** para criar uma lista de reprodução de itens de mídia quando o usuário clica em um botão. A lista de reprodução contém itens com o álbum especificado pelo usuário em uma caixa de texto. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
private void playAlbum_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the album title text that the user entered in the text box. 
    string album = getAlbum.Text;

    // Create the playlist using getByAlbum. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAlbum(album);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playAlbum_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playAlbum.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the album title text that the user entered in the text box. 
    Dim album As String = getAlbum.Text

    &#39; Create the playlist using getByAlbum. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAlbum(album)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





