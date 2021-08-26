---
title: Propriedade IWMPNetwork frameRate
description: A propriedade frameRate obtém a taxa de quadros de vídeo atual.
ms.assetid: 800ecf3d-3b2c-48f9-8fc4-c7c32757749a
keywords:
- Propriedade frameRate Windows Media Player
- propriedade frameRate Windows Media Player , interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player , propriedade frameRate
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
ms.openlocfilehash: 3169cc21eee2317da45db3cb3ca9ceffffa01c85479312defe63cda1fa09796f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956156"
---
# <a name="iwmpnetworkframerate-property"></a>Propriedade IWMPNetwork::frameRate

A **propriedade frameRate** obtém a taxa de quadros de vídeo atual.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 frameRate {get; set;}
```


```VB

Public ReadOnly Property frameRate As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System.Int32 que** é a taxa de quadros atual em quadros por centenas de segundos.

> [!Note]  
> Embora a propriedade **encodedFrameRate** mede a taxa de quadros codificada em quadros por segundo, a propriedade **frameRate** mede a taxa de quadros atual em quadros por centenas de segundos. Consulte Observações.

 

## <a name="remarks"></a>Comentários

O valor atual da taxa de quadros é retornado em quadros por centenas de segundos. Por exemplo, um valor de 2998 indica 29,98 quadros por segundo (fps).

## <a name="examples"></a>Exemplos

O exemplo de código a seguir **usa frameRate** para exibir a taxa de quadros especificada quando o arquivo foi codificado. As informações são exibidas em um rótulo em resposta ao **Evento PlayStateChange.** O **objeto AxWMPLib.AxWindowsMediaPlayer** é representado pela variável chamada player.


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
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPNetwork (VB e C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.encodedFrameRate (VB e C#)**](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)
</dt> </dl>

 

 





