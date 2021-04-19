---
title: Propriedade IWMPNetwork bufferingCount
description: A propriedade bufferingCount Obtém o número de vezes que o buffer ocorreu durante a reprodução.
ms.assetid: 2e3a2914-fc38-4477-8c4c-15b4a2e424dc
keywords:
- Propriedade bufferingCount Windows Media Player
- Propriedade bufferingCount Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, Propriedade bufferingCount
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4958892dd9784ee72b51adfedbbcdee81817b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770647"
---
# <a name="iwmpnetworkbufferingcount-property"></a>Propriedade IWMPNetwork:: bufferingCount

A propriedade **bufferingCount** Obtém o número de vezes que o buffer ocorreu durante a reprodução.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 bufferingCount {get; set;}
```


```VB

Public ReadOnly Property bufferingCount As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System. Int32** que é a contagem de buffers.

## <a name="remarks"></a>Comentários

Toda vez que a reprodução é interrompida e reiniciada, essa propriedade é redefinida como zero. Ele não será redefinido se a reprodução for pausada.

O armazenamento em buffer se aplica somente ao conteúdo de streaming. Essa propriedade obtém informações válidas somente durante o tempo de execução quando a URL para reprodução é definida usando a propriedade **AxWindowsMediaPlayer. URL** .

## <a name="examples"></a>Exemplos

O exemplo a seguir usa *bufferingCount* para exibir o número de vezes que o buffer ocorre durante a reprodução. As informações são exibidas em um rótulo em resposta ao evento de buffer. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Display the bufferingCount when buffering has started.
    if (e.start == true)
    {
        bufferingCountLabel.Text = ("Buffering count: " + player.network.bufferingCount);
    }  
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

    &#39; Display the bufferingCount when buffering has started.
    If (e.start = True) Then

        bufferingCountLabel.Text = (&quot;Buffering count: &quot; + player.network.bufferingCount)

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

[**AxWindowsMediaPlayer. URL (VB e C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Interface IWMPNetwork (VB e C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





