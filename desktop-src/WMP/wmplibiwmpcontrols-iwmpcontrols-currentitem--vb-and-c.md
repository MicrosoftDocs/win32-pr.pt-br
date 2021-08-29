---
title: Propriedade currentItem IWMPControls
description: A propriedade currentItem obtém ou define o item de mídia atual em uma playlist.
ms.assetid: 0a331b1f-95bd-48ea-b951-1ca35cc96865
keywords:
- propriedade currentItem Windows Media Player
- propriedade currentItem Windows Media Player , interface IWMPControls
- Interface IWMPControls Windows Media Player propriedade , currentItem
topic_type:
- apiref
api_name:
- IWMPControls.currentItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d8193dc349524495e021dc048ac4be3673d38ec7da30aa1bb72d94960a0989f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053654"
---
# <a name="iwmpcontrolscurrentitem-property"></a>Propriedade IWMPControls::currentItem

A **propriedade currentItem** obtém ou define o item de mídia atual em uma playlist.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPMedia currentItem {get; set;}
```


```VB

Public Property currentItem As IWMPMedia
```





## <a name="property-value"></a>Valor da propriedade

Uma interface **WMPLib.IWMPMedia** que representa o item de mídia.

## <a name="remarks"></a>Comentários

Essa propriedade funciona apenas com itens na playlist atual. Não **há suporte para a configuração currentItem** na interface de um item de mídia salvo.

## <a name="examples"></a>Exemplos

O exemplo a seguir **usa currentItem** para definir o item de mídia atual do player como um item selecionado em uma caixa de listagem. A caixa de listagem foi preenchida com todos os itens na playlist atual. O **objeto AxWMPLib.AxWindowsMediaPlayer** é representado pela variável chamada player.


```CSharp
private void playItem_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    int selectedItem = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Ensure that the previous media item is stopped.
    player.Ctlcontrols.stop();

    // Set the current item to the item selected from the list box.
    player.Ctlcontrols.currentItem = player.currentPlaylist.get_Item(selectedItem);
    
    // Play the current item.
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playItem_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles playItem.SelectedIndexChanged

    Dim lb As System.Windows.Forms.ListBox = sender
    Dim selectedItem As Integer = lb.SelectedIndex

    &#39; Ensure that the previous media item is stopped.
    player.Ctlcontrols.stop()

    &#39; Set the current item to the item selected from the list box.
    player.Ctlcontrols.currentItem = player.currentPlaylist.Item(selectedItem)

    &#39; Play the current item.
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

[**IWMPControlsInterface (VB e C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPMediaInterface (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection.getByName(VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





