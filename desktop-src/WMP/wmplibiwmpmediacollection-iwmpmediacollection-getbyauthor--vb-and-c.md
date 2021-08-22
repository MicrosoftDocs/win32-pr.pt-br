---
title: Método getByAuthor IWMPMediaCollection
description: O método getByAuthor retorna uma interface IWMPPlaylist que fornece acesso aos itens de mídia pelo autor especificado.
ms.assetid: eb3793f6-bad1-4c80-991e-c6d0093ae57f
keywords:
- Método getByAuthor Windows Media Player
- Método getByAuthor Windows Media Player interface , IWMPMediaCollection
- Interface IWMPMediaCollection Windows Media Player , método getByAuthor
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAuthor
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829232e6cd9fb64fec1d209991c3734ad435b4b69d0d7b66b135ab9cca1fe4a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053604"
---
# <a name="iwmpmediacollectiongetbyauthor-method"></a>Método IWMPMediaCollection::getByAuthor

O `getByAuthor` método retorna uma interface **IWMPPlaylist** que fornece acesso aos itens de mídia pelo autor especificado.

## <a name="syntax"></a>Sintaxe


```CSharp
public IWMPPlaylist getByAuthor(
  System.String bstrAuthor
);
```


```VB

Public Function getByAuthor( _
  ByVal bstrAuthor As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAuthor
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrAuthor* \[ Em\]
</dt> <dd>

O **System.String** que é o nome do autor.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Uma interface **WMPLib.IWMPPlaylist** para os itens de mídia recuperados.

## <a name="remarks"></a>Comentários

Antes de chamar esse método, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

Há duas maneiras de recuperar uma interface **IWMPMediaCollection** e o comportamento do método depende de qual dessas duas maneiras `getByAuthor` você usa. Se você recuperar a interface chamando [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), o método retornará todos os itens `getByAuthor` de mídia na biblioteca. No entanto, se você recuperar a interface chamando [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), o método retornará apenas os itens de áudio na biblioteca que têm o atributo e o valor `getByAuthor` especificados.

## <a name="examples"></a>Exemplos

O exemplo a seguir `getByAuthor` usa para criar uma playlist de itens de mídia quando o usuário clica em um botão. A playlist contém itens correspondentes ao nome do autor especificado pelo usuário em uma caixa de texto. O **objeto AxWMPLib.AxWindowsMediaPlayer** é representado pela variável chamada player.


```CSharp
private void playAuthor_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the author's name from the text box. 
    string author = getAuthor.Text;

    // Create the playlist using getByAuthor. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAuthor(author);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playAuthor_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playAuthor.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the author&#39;s name from the text box. 
    Dim author As String = getAuthor.Text

    &#39; Create the playlist using getByAuthor. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAuthor(author)

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

 

 





