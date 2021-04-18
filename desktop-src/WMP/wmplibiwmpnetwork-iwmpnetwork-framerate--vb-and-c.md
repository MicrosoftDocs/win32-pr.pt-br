---
title: Propriedade de taxa de quadros IWMPNetwork
description: A propriedade de taxa de quadros Obtém a taxa de quadros de vídeo atual.
ms.assetid: 800ecf3d-3b2c-48f9-8fc4-c7c32757749a
keywords:
- Propriedade de taxa de quadros Windows Media Player
- Propriedade de taxa de quadros Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, propriedade de taxa de quadros
topic_type:
- apiref
api_name:
- IWMPNetwork.frameRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c338a116588fa9f1c552feff15f220e08b0f66e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756528"
---
# <a name="iwmpnetworkframerate-property"></a>Propriedade IWMPNetwork:: taxa de quadros

A propriedade de **taxa** de quadros Obtém a taxa de quadros de vídeo atual.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 frameRate {get; set;}
```


```VB

Public ReadOnly Property frameRate As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System. Int32** que é a taxa de quadros atual em quadros por centenas de segundos.

> [!Note]  
> Embora a propriedade **encodedFrameRate** meça a taxa de quadros codificados em quadros por segundo, a propriedade de **taxa** de quadros mede a taxa de quadro atual em quadros por centenas de segundos. Consulte Observações.

 

## <a name="remarks"></a>Comentários

O valor da taxa de quadros atual é retornado em quadros por centenas de segundos. Por exemplo, um valor de 2998 indica 29,98 quadros por segundo (FPS).

## <a name="examples"></a>Exemplos

O exemplo de código a seguir usa taxa de **quadros** para exibir a taxa de quadros especificada quando o arquivo foi codificado. As informações são exibidas em um rótulo em resposta ao evento **PlayStateChange** . O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the frameRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.frameRate != 0)
            {
                frameRateLabel.Text = "Current Frame Rate: " + player.network.frameRate + " K bits/second";
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

    &#39; Display the frameRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.frameRate <> 0) Then

                frameRateLabel.Text = &quot;Current Frame Rate: &quot; + player.network.frameRate + &quot; K bits/second&quot;

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
</dt> <dt>

[**IWMPNetwork. encodedFrameRate (VB e C#)**](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)
</dt> </dl>

 

 





