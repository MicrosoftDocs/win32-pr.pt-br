---
title: Propriedade durationstring de IWMPMedia
description: A propriedade durationstring Obtém uma cadeia de caracteres que indica a duração do item de mídia atual no formato HH MM SS.
ms.assetid: de33c737-d73e-41f0-9c1b-944279194738
keywords:
- Propriedade durationstring Windows Media Player
- Propriedade durationstring Windows Media Player, interface IWMPMedia
- Interface IWMPMedia Windows Media Player, Propriedade durationstring
topic_type:
- apiref
api_name:
- IWMPMedia.durationString
- IWMPMedia.get_durationString
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e6bc732388036aa9e79aeedd988de94fa263bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753386"
---
# <a name="iwmpmediadurationstring-property"></a>IWMPMedia: Propriedade urationString de:d

A propriedade **durationstring** Obtém uma cadeia de caracteres que indica a duração do item de mídia atual no formato hh: mm: SS.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.String durationString {get;}
```


```VB

Public ReadOnly Property durationString As System.String
```





## <a name="property-value"></a>Valor da propriedade

Um **System. String** que é a duração.

## <a name="remarks"></a>Comentários

Se essa propriedade for usada com um item de mídia diferente daquele especificado em AxWindowsMediaPlayer. currentMedia, ele não poderá conter um valor válido. Se o item de mídia tiver menos de uma hora, a parte de horas do valor de retorno será omitida.

Antes de usar essa propriedade, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir usa **durationstring** para exibir a duração do item de mídia atual como texto formatado em um rótulo. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
// Create an event handler for the OpenStateChange event.
private void player_OpenStateChange(object sender, AxWMPLib._WMPOCXEvents_OpenStateChangeEvent e)
{
    // Test whether the current media item is open.
    if (e.newState == (int)WMPLib.WMPOpenState.wmposMediaOpen)
    {
         // Display the formatted duration string in the label.
         mediaDuration.Text = player.currentMedia.durationString;
    }
}
```


```VB

' Create an event handler for the OpenStateChange event.
Public Sub player_OpenStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_OpenStateChangeEvent) Handles player.OpenStateChange

    &#39; Test whether the current media item is open.
    If (e.newState = 13) Then

        &#39; Display the formatted duration string in the label.
        mediaDuration.Text = player.currentMedia.durationString

    End If

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

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. Duration (VB e C#)**](wmplibiwmpmedia-iwmpmedia-duration--vb-and-c.md)
</dt> </dl>

 

 





