---
title: Propriedade IWMPNetwork encodedFrameRate
description: A propriedade encodedFrameRate obtém a taxa de quadros de vídeo especificada pelo autor do conteúdo.
ms.assetid: 4faf5675-5bf3-485d-802f-a1f900ddae63
keywords:
- Propriedade encodedFrameRate Windows Media Player
- A propriedade encodedFrameRate Windows Media Player , interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player , propriedade encodedFrameRate
topic_type:
- apiref
api_name:
- IWMPNetwork.encodedFrameRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33f8a08572f65e1e44027ed25d84acfe7d917f92bf4bb63d5d9b8cca1e1201d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000006"
---
# <a name="iwmpnetworkencodedframerate-property"></a>Propriedade IWMPNetwork::encodedFrameRate

A **propriedade encodedFrameRate** obtém a taxa de quadros de vídeo especificada pelo autor do conteúdo.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 encodedFrameRate {get; set;}
```


```VB

Public ReadOnly Property encodedFrameRate As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System.Int32 que** é a taxa de quadros codificada em quadros por segundo (fps).

> [!Note]  
> Embora a propriedade **encodedFrameRate** mede a taxa de quadros codificada em quadros por segundo, a propriedade **frameRate** mede a taxa de quadros atual em quadros por centenas de segundos.

 

## <a name="examples"></a>Exemplos

O exemplo de código a seguir **usa encodedFrameRate** para exibir a taxa de quadros especificada quando o arquivo foi codificado. As informações são exibidas em um rótulo, em resposta ao **Evento PlayStateChange.** O **objeto AxWMPLib.AxWindowsMediaPlayer** é representado pela variável chamada player.


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the encodedFrameRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.encodedFrameRate != 0)
            {
                encodedFrameRateLabel.Text = "Current Encoded Frame Rate: " + player.network.encodedFrameRate + " K bits/second";
            }
            break;

        default:
            break;
    }
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Display the encodedFrameRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.encodedFrameRate <> 0) Then

                encodedFrameRateLabel.Text = &quot;Current Encoded Frame Rate: &quot; + player.network.encodedFrameRate + &quot; K bits/second&quot;

            End If

    End Select

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

[**Interface IWMPNetwork (VB e C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.frameRate (VB e C#)**](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)
</dt> </dl>

 

 





