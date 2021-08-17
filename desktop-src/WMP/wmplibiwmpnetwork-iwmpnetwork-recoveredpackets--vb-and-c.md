---
title: Propriedade IWMPNetwork recoveredPackets
description: A propriedade recoveredPackets obtém o número de pacotes recuperados.
ms.assetid: 90fcefcd-2bd7-4fb5-8337-36bec5d44e60
keywords:
- propriedade recoveredPackets Windows Media Player
- propriedade recoveredPackets Windows Media Player , interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player , propriedade recoveredPackets
topic_type:
- apiref
api_name:
- IWMPNetwork.recoveredPackets
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7665fad35e87b32b4e5cf20875e7b0f59c5e7fb8915fa7595fd625a04303835c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956076"
---
# <a name="iwmpnetworkrecoveredpackets-property"></a>Propriedade IWMPNetwork::recoveredPackets

A **propriedade recoveredPackets** obtém o número de pacotes recuperados.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 recoveredPackets {get; set;}
```


```VB

Public ReadOnly Property recoveredPackets As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System.Int32** que é o número de pacotes recuperados.

## <a name="remarks"></a>Comentários

Cada vez que a reprodução é interrompida e reiniciada, essa propriedade é redefinida como zero. O valor não será redefinido se a reprodução estiver em pausa.

Essa propriedade obtém informações válidas somente durante o tempo de reprodução quando a URL para reprodução é definida usando **a propriedade AxWindowsMediaPlayer.URL.** O valor será zero ao usar o protocolo HTTP, que é sem perda.

## <a name="examples"></a>Exemplos

O exemplo a seguir **usa recoveredPackets** para exibir o número de pacotes recuperados em um rótulo, em resposta ao Evento **PlayStateChange.** O exemplo usa um temporizador com um intervalo de 1 segundo para atualizar a exibição. O **objeto AxWMPLib.AxWindowsMediaPlayer** é representado pela variável chamada player.


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

private void UpdateRecoveredPackets(object sender, EventArgs e)
{
    recoveredPacketsLabel.Text = ("Packets recovered: " + player.network.recoveredPackets.ToString());
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

Public Sub UpdateRecoveredPackets(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    recoveredPacketsLabel.Text = (&quot;Packets recovered: &quot; + player.network.recoveredPackets.ToString())

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

[**AxWindowsMediaPlayer.URL (VB e C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Interface IWMPNetwork (VB e C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





