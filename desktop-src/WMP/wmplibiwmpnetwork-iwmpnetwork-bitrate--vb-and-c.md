---
title: Propriedade de taxa de bits IWMPNetwork
description: A propriedade de taxa de bits Obtém a taxa de bit atual sendo recebida.
ms.assetid: f7dda557-3954-45ed-9eac-6d27109e2dfa
keywords:
- Propriedade de taxa de bits Windows Media Player
- Propriedade de taxa de bits Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, propriedade de taxa de bits
topic_type:
- apiref
api_name:
- IWMPNetwork.bitRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64039eb960a928f5268643e18d1a01b9034d5d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797574"
---
# <a name="iwmpnetworkbitrate-property"></a>Propriedade IWMPNetwork:: taxa de bits

A propriedade de **taxa** de bits Obtém a taxa de bit atual sendo recebida.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 bitRate {get; set;}
```


```VB

Public ReadOnly Property bitRate As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System. Int32** que é a taxa de bits.

## <a name="remarks"></a>Comentários

O valor dessa propriedade é uma combinação das taxas de bits de fluxos de áudio e vídeo.

## <a name="examples"></a>Exemplos

O exemplo a seguir **usa taxa de bits para** exibir a taxa do bit de mídia atual. As informações são exibidas em um rótulo em resposta ao evento **PlayStateChange** . O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the bitRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.bitRate != 0)
            {
                bitRateLabel.Text = "Current Bit Rate: " + player.network.bitRate + " K bits/second";
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

    &#39; Display the bitRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.bitRate <> 0) Then

                bitRateLabel.Text = &quot;Current Bit Rate: &quot; + player.network.bitRate + &quot; K bits/second&quot;

            End If

    End Select

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

[**Interface IWMPNetwork (VB e C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





