---
title: Propriedade IWMPNetwork downloadProgress
description: A propriedade downloadProgress obtém o percentual de download concluído.
ms.assetid: 40568c81-5bb5-45d9-b654-31072608663d
keywords:
- propriedade downloadProgress Windows Media Player
- propriedade downloadProgress Windows Media Player , interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player , propriedade downloadProgress
topic_type:
- apiref
api_name:
- IWMPNetwork.downloadProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96c2b47895d595a570191d9aa66b90b1cdc53392f8f111d64307074e5689f2ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331966"
---
# <a name="iwmpnetworkdownloadprogress-property"></a>Propriedade IWMPNetwork::d ownloadProgress

A **propriedade downloadProgress** obtém o percentual de download concluído.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 downloadProgress {get; set;}
```


```VB

Public ReadOnly Property downloadProgress As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System.Int32 que** é o progresso do download expresso como um percentual.

## <a name="remarks"></a>Comentários

Quando o controle Windows Media Player está conectado a um arquivo de mídia digital que pode ser reproduzido e baixado ao mesmo tempo, a propriedade **downloadProgress** obtém a porcentagem do arquivo total que foi baixado. Atualmente, esse recurso tem suporte apenas para arquivos de mídia digital baixados de servidores Web. Um arquivo de qualquer um dos seguintes formatos pode ser baixado e interpretado simultaneamente:

-   Advanced Systems Format (ASF)
-   Áudio do Windows Media (WMA)
-   Vídeo do Windows Media (WMV)
-   MP3
-   Mpeg
-   WAV

Além disso, alguns arquivos AVI podem ser baixados e tocados simultaneamente.

Use **o AxWindowsMediaPlayer. \_ WMPOCXEvents \_ BufferingEvent para** determinar quando o buffer é iniciado ou interrompido.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir **usa downloadProgress** para exibir o percentual de download concluído. As informações são exibidas em um rótulo, em resposta ao **Evento de Buffer.** O exemplo usa um temporizador com um intervalo de 1 segundo para atualizar a exibição. O **objeto AxWMPLib.AxWindowsMediaPlayer** é representado pela variável chamada player.


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Determine whether buffering has started or stopped.
    if (e.start == true)
    {
        // Set the timer interval at one second (1000 miliseconds).
        timer.Interval = 1000;
        
        // Start the timer.
        timer.Start();
    }
    else
    {
        // Buffering is complete. Stop the timer.
        timer.Stop();
    }
}

// Update the download progress in a timer event handler.
private void UpdateDownloadProgress(object sender, EventArgs e)
{
    downloadProgressLabel.Text = ("Download progress: " + player.network.downloadProgress + " percent complete");
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

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

&#39; Update the download progress in a timer event handler.
Public Sub UpdateDownloadProgress(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    downloadProgressLabel.Text = (&quot;Download progress: &quot; + player.network.downloadProgress + &quot; percent complete&quot;)

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

[**Evento AxWindowsMediaPlayer.Buffering (VB e C#)**](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[**Interface IWMPNetwork (VB e C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





