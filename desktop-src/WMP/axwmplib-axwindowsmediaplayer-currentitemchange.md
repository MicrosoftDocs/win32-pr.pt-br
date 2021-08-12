---
title: Evento CurrentItemChange do objeto AxWindowsMediaPlayer
description: O evento CurrentItemChange ocorre quando o valor de IWMPControls.currentItem muda.
ms.assetid: c5eeafd2-405b-4808-97d1-399a2344ca42
keywords:
- Evento CurrentItemChange do objeto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- CurrentItemChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1786fab3e312f95550103cdc6cf4f2558e25e883df9c7be2d6f850a7f8a5ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582552"
---
# <a name="currentitemchange-event-of-the-axwindowsmediaplayer-object"></a>Evento CurrentItemChange do objeto AxWindowsMediaPlayer

O evento CurrentItemChange ocorre quando o valor de IWMPControls. **alterações currentItem.**

``` syntax
[C#]
private void player_CurrentItemChange(
  object sender,
  _WMPOCXEvents_CurrentItemChangeEvent e
)

[Visual Basic]
Private Sub player_CurrentItemChange(  
  sender As Object,
  e As _WMPOCXEvents_CurrentItemChangeEvent
) Handles player.CurrentItemChange
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentItemChangeEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentItemChangeEvent**, que contém a propriedade a seguir relacionada a esse evento.



| Propriedade   | Descrição                                                                                                   |
|------------|---------------------------------------------------------------------------------------------------------------|
| pdispMedia | System.ObjectO novo item de mídia atual. Você pode castiá-lo em uma interface IWMPMedia para acessá-la.<br/> |



 

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra um manipulador de eventos para o evento CurrentItemChange. O objeto AxWMPLib.AxWindowsMediaPlayer é representado pela variável chamada player.


```CSharp
// Add a delegate for the CurrentItemChange event
player.CurrentItemChange += new AxWMPLib._WMPOCXEvents_CurrentItemChangeEventHandler(player_CurrentItemChange);

private void player_CurrentItemChange(object sender, AxWMPLib._WMPOCXEvents_CurrentItemChangeEvent e)
{
    // Display the name of the new media item.
    mediaText.Text = player.currentMedia.name;
}
```


```VB

Public Sub player_CurrentItemChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_CurrentItemChangeEvent) Handles player.CurrentItemChange

    &#39; Display the name of the new media item.
    mediaText.Text = player.currentMedia.name

End Sub
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

[**IWMPControls.currentItem (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





