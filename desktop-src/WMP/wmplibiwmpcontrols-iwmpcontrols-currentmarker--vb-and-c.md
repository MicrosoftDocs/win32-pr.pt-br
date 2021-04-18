---
title: Propriedade IWMPControls currentMarker
description: A propriedade currentMarker Obtém ou define o número do marcador atual.
ms.assetid: faf8c32a-66de-47ce-aa3d-6699d9f9bdda
keywords:
- Propriedade currentMarker Windows Media Player
- Propriedade currentMarker Windows Media Player, interface IWMPControls
- Interface IWMPControls Windows Media Player, Propriedade currentMarker
topic_type:
- apiref
api_name:
- IWMPControls.currentMarker
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfbcea42594b15b8da08248d38b5d8f72a1de29d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796291"
---
# <a name="iwmpcontrolscurrentmarker-property"></a>Propriedade IWMPControls:: currentMarker

A propriedade **currentMarker** Obtém ou define o número do marcador atual.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 currentMarker {get; set;}
```


```VB

Public Property currentMarker As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System. Int32** que é o número do marcador.

## <a name="remarks"></a>Comentários

A definição de **currentMarker** faz com que a reprodução seja iniciada a partir do marcador especificado. Antes de tentar definir **currentMarker**, determine se um arquivo tem marcadores e quantos deles tem usando **IWMPMedia. markerCount**. Se um arquivo não tiver marcadores, definir **currentMarker** como qualquer coisa, exceto zero, resultará em um erro. A definição de **currentMarker** como um número maior que **markerCount** também resulta em um erro.

A propriedade **currentMarker** sempre retorna o marcador atual ou último, o que significa que a posição real do arquivo pode ser no marcador atual ou antes do próximo marcador. Os marcadores são numerados começando em 1, portanto, se um arquivo tiver marcadores, você poderá definir **currentMarker** como zero para alterar a posição do arquivo para zero.

Até que o item de mídia atual seja definido (usando **AxWindowsMediaPlayer. URL** ou **AxWindowsMediaPlayer. CurrentMedia**), **currentMarker** retornará zero.

## <a name="examples"></a>Exemplos

O exemplo a seguir usa **currentMarker** para iniciar a reprodução de vídeo do marcador que corresponde à propriedade SelectedIndex de uma caixa de listagem que foi preenchida com identificadores de marcador. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
// Fill the list box with the marker identifiers of the current media item.
markers.Items.Add("Begining");
markers.Items.Add("Sunrise");
markers.Items.Add("Car chase");
markers.Items.Add("Happy ending");

// Set the currentMarker to the marker selected from the list box.
private void markers_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    int selectedMarker = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    player.Ctlcontrols.currentMarker = selectedMarker;
}
```


```VB

' Fill the list box with the marker identifiers of the current media item.
markers.Items.Add(&quot;Begining&quot;)
markers.Items.Add(&quot;Sunrise&quot;)
markers.Items.Add(&quot;Car chase&quot;)
markers.Items.Add(&quot;Happy ending&quot;)

&#39; Set the currentMarker to the marker selected from the list box.
Public Sub markers_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles markers.SelectedIndexChanged

    Dim lb As System.Windows.Forms.ListBox = sender
    Dim selectedMarker As Integer = lb.SelectedIndex

    player.Ctlcontrols.currentMarker = selectedMarker

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

[**AxWindowsMediaPlayer. currentMedia (VB e C#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. URL (VB e C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Interface IWMPControls (VB e C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. markerCount (VB e C#)**](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





