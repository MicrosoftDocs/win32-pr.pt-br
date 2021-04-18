---
title: Método IWMPMediaCollection getByGenre
description: O método getByGenre retorna uma interface IWMPPlaylist que fornece acesso a itens de mídia do gênero especificado.
ms.assetid: 0681e5a2-b56d-4c33-95ce-d9ef3cd5473d
keywords:
- método getByGenre Windows Media Player
- método getByGenre Windows Media Player, interface IWMPMediaCollection
- Interface IWMPMediaCollection Windows Media Player, método getByGenre
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByGenre
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eb6477a4cd212f354f5af3ab7e50fc2a87092cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778664"
---
# <a name="iwmpmediacollectiongetbygenre-method"></a>Método IWMPMediaCollection:: getByGenre

O `getByGenre` método retorna uma interface **IWMPPlaylist** que fornece acesso a itens de mídia do gênero especificado.

## <a name="syntax"></a>Sintaxe


```CSharp
public IWMPPlaylist getByGenre(
  System.String bstrGenre
);
```


```VB

Public Function getByGenre( _
  ByVal bstrGenre As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByGenre
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrGenre* \[ no\]
</dt> <dd>

O **System. String** que é o nome do gênero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Uma interface **WMPLib. IWMPPlaylist** para os itens de mídia recuperados.

## <a name="remarks"></a>Comentários

Antes de chamar esse método, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

Há duas maneiras de se recuperar uma interface **IWMPMediaCollection** , e o comportamento do `getByGenre` método depende de quais dessas duas maneiras você usa. Se você recuperar a interface chamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), o `getByGenre` método retornará todos os itens de mídia na biblioteca. No entanto, se você recuperar a interface chamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), o `getByGenre` método retornará apenas os itens de áudio na biblioteca que têm o atributo e o valor especificados.

## <a name="examples"></a>Exemplos

O exemplo a seguir usa `getByGenre` para recuperar uma lista de reprodução de itens de mídia quando o usuário clica em um botão. A lista de reprodução contém itens com o gênero especificado pelo usuário em uma caixa de texto. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
private void playGenre_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the genre that the user entered in the text box. 
    string genre = getGenre.Text;

    // Create the playlist using getByGenre. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByGenre(genre);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playGenre_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playGenre.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the genre that the user entered in the text box. 
    Dim genre As String = getGenre.Text

    &#39; Create the playlist using getByGenre. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByGenre(genre)

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

 

 





