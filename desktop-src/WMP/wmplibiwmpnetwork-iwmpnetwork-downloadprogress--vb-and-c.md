---
title: Propriedade IWMPNetwork downloadProgress
description: A propriedade downloadProgress Obtém a porcentagem de download concluído.
ms.assetid: 40568c81-5bb5-45d9-b654-31072608663d
keywords:
- Propriedade downloadProgress Windows Media Player
- Propriedade downloadProgress Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, Propriedade downloadProgress
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
ms.openlocfilehash: 4b10b767845ac951e1364e15c7f6f1d729882e0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781407"
---
# <a name="iwmpnetworkdownloadprogress-property"></a>IWMPNetwork: Propriedade ownloadProgress de:d

A propriedade **downloadProgress** Obtém a porcentagem de download concluído.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 downloadProgress {get; set;}
```


```VB

Public ReadOnly Property downloadProgress As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System. Int32** que é o progresso do download expresso como uma porcentagem.

## <a name="remarks"></a>Comentários

Quando o controle do Windows Media Player está conectado a um arquivo de mídia digital que pode ser reproduzido e baixado ao mesmo tempo, a propriedade **downloadProgress** Obtém a porcentagem do arquivo total que foi baixado. Atualmente, esse recurso tem suporte apenas para arquivos de mídia digital baixados de servidores Web. Um arquivo de qualquer um dos seguintes formatos pode ser baixado e reproduzido simultaneamente:

-   Advanced Systems Format (ASF)
-   Áudio do Windows Media (WMA)
-   Vídeo do Windows Media (WMV)
-   MP3
-   FUNCIONALIDADES
-   WAV

Além disso, alguns arquivos AVI podem ser baixados e reproduzidos simultaneamente.

Use o **AxWindowsMediaPlayer. \_ WMPOCXEvents \_ BufferingEvent** para determinar quando o buffer é iniciado ou interrompido.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir usa **downloadProgress** para exibir a porcentagem de download concluído. As informações são exibidas em um rótulo, em resposta ao evento de **buffer** . O exemplo usa um temporizador com um intervalo de 1 segundo para atualizar a exibição. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


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
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Evento AxWindowsMediaPlayer. buffering (VB e C#)**](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[**Interface IWMPNetwork (VB e C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





