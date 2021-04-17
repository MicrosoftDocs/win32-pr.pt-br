---
title: Propriedade IWMPNetwork receptionQuality
description: A propriedade receptionQuality Obtém a porcentagem de pacotes que não são perdidos nos últimos 30 segundos.
ms.assetid: 103e6b8f-e029-4f53-93ac-b516896a7594
keywords:
- Propriedade receptionQuality Windows Media Player
- Propriedade receptionQuality Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, Propriedade receptionQuality
topic_type:
- apiref
api_name:
- IWMPNetwork.receptionQuality
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3703ffa29183937874c40053bd3c7ae3c85d75d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764092"
---
# <a name="iwmpnetworkreceptionquality-property"></a>Propriedade IWMPNetwork:: receptionQuality

A propriedade **receptionQuality** Obtém a porcentagem de pacotes que não são perdidos nos últimos 30 segundos.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 receptionQuality {get; set;}
```


```VB

Public ReadOnly Property receptionQuality As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System. Int32** que é a qualidade da recepção.

## <a name="remarks"></a>Comentários

O número de pacotes recebidos, perdidos e recuperados durante o streaming é monitorado uma vez a cada segundo. A propriedade **receptionQuality** Obtém a porcentagem de pacotes que não foram perdidos durante os últimos 30 segundos.

Toda vez que a reprodução é interrompida e reiniciada, essa propriedade é redefinida como zero. O valor não será redefinido se a reprodução for pausada.

Essa propriedade obtém informações válidas somente durante o tempo de execução quando a URL para reprodução é definida usando a propriedade **AxWindowsMediaPlayer. URL** .

## <a name="examples"></a>Exemplos

O exemplo a seguir usa **receptionQuality** para exibir a porcentagem de pacotes recebidos em um rótulo, em resposta ao evento **PlayStateChange** . O exemplo usa um temporizador com um intervalo de 1 segundo para atualizar a exibição. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Test whether content is playing. 
    if (e.newState == 3)
    {
        // Start the timer. Update the display every 10 seconds.
        timer.Interval = 10000;
        timer.Start();
    }
    else
    {
        // Not playing; stop the timer.
        timer.Stop();
    }
}

private void UpdateReceptionQuality(object sender, EventArgs e)
{
    receptionQualityLabel.Text = ("Packets recovered: " + player.network.receptionQuality.ToString() + "%");
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Test whether packets may be arriving.
    Select Case e.newState

    &#39; If WMPPlayState is Stopped, Paused, ScanForward, ScanReverse, Waiting, MediaEnded
    &#39; or Transitioning then stop the timer. 
        Case 1
        Case 2
        Case 4
        Case 5
        Case 7
        Case 8
        Case 9
            timer.Stop()

        &#39; If WMPPlayState is Playing or Buffering then set the timer interval and start the timer.
        Case Else
            timer.Interval = 1000
            timer.Start()

    End Select

End Sub

Public Sub UpdateReceptionQuality(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    receptionQualityLabel.Text = (&quot;Packets recovered: &quot; + player.network.receptionQuality.ToString() + &quot;%&quot;)

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

 

 





