---
title: Evento de erro do objeto AxWindowsMediaPlayer
description: O evento Error ocorre quando o controle Windows Media Player tem uma condição de erro.
ms.assetid: d28c18a9-c650-4169-989b-8727b7a5a831
keywords:
- Evento de erro do objeto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- Error Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a146f58276ab433fa11b4c5b212af43a92511328e22f70b93d0a45779f4eaa24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582154"
---
# <a name="error-event-of-the-axwindowsmediaplayer-object"></a>Evento de erro do objeto AxWindowsMediaPlayer

O evento Error ocorre quando o controle Windows Media Player tem uma condição de erro.

``` syntax
[C#]
private void player_ErrorEvent(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_ErrorEvent(  
  sender As Object,  
  e As System.EventArgs
) Handles player.ErrorEvent
```

## <a name="event-data"></a>Dados de evento

Esse evento não contém dados.

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um manipulador de eventos para o evento Error para exibir o texto de descrição do primeiro erro na fila de erros. O objeto AxWMPLib.AxWindowsMediaPlayer é representado pela variável chamada player.


```CSharp
// Add a delegate for the Error event.
player.ErrorEvent += new EventHandler(player_ErrorEvent);

private void player_ErrorEvent(object sender, System.EventArgs e)
{
    // Get the description of the first error. 
    string errDesc = player.Error.get_Item(0).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc);
}
```


```VB

Public Sub player_ErrorEvent(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the description of the first error. 
    Dim errDesc As String = player.Error.Item(0).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc)

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

[**IWMPError.Item (VB e C#)**](iwmperror-item--vb-and-c.md)
</dt> <dt>

[**IWMPErrorItem.errorDescription (VB e C#)**](wmplibiwmperroritem-iwmperroritem-errordescription--vb-and-c.md)
</dt> </dl>

 

 





