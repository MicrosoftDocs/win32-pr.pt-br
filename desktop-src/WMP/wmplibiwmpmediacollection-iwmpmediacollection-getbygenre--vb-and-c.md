---
title: Método getByGenre de IWMPMediaCollection
description: O método getByGenre retorna uma interface IWMPPlaylist que fornece acesso a itens de mídia do gênero especificado.
ms.assetid: 0681e5a2-b56d-4c33-95ce-d9ef3cd5473d
keywords:
- Método getByGenre Windows Media Player
- Método getByGenre Windows Media Player interface , IWMPMediaCollection
- Interface IWMPMediaCollection Windows Media Player método , getByGenre
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
ms.openlocfilehash: d72f20182f2bfb3bef0d4de2907165a571009072d234add3b8f89ae2db859c7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053594"
---
# <a name="iwmpmediacollectiongetbygenre-method"></a>Método IWMPMediaCollection::getByGenre

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

*bstrGenre* \[ Em\]
</dt> <dd>

O **System.String** que é o nome do gênero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Uma interface **WMPLib.IWMPPlaylist** para os itens de mídia recuperados.

## <a name="remarks"></a>Comentários

Antes de chamar esse método, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

Há duas maneiras de recuperar uma interface **IWMPMediaCollection** e o comportamento do método depende de qual dessas duas maneiras `getByGenre` você usa. Se você recuperar a interface chamando [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), o método retornará todos os itens `getByGenre` de mídia na biblioteca. No entanto, se você recuperar a interface chamando [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), o método retornará apenas os itens de áudio na biblioteca que têm o atributo e o valor `getByGenre` especificados.

## <a name="examples"></a>Exemplos

O exemplo a seguir `getByGenre` usa para recuperar uma playlist de itens de mídia quando o usuário clica em um botão. A playlist contém itens com o gênero especificado pelo usuário em uma caixa de texto. O **objeto AxWMPLib.AxWindowsMediaPlayer** é representado pela variável chamada player.


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
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





