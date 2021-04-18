---
title: Propriedade Duration IWMPMedia
description: A Propriedade Duration Obtém a duração em segundos do item de mídia atual.
ms.assetid: f8a0bf3e-eeaf-46f5-90c8-d3b11ce4eb39
keywords:
- Propriedade Duration Windows Media Player
- Propriedade Duration Windows Media Player, interface IWMPMedia
- Interface IWMPMedia Windows Media Player, Propriedade Duration
topic_type:
- apiref
api_name:
- IWMPMedia.duration
- IWMPMedia.get_duration
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f796cab042713082ce2066659f62736855e62787
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756666"
---
# <a name="iwmpmediaduration-property"></a>IWMPMedia: Propriedade uração de:d

A propriedade **Duration** Obtém a duração em segundos do item de mídia atual.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.Double duration {get;}
```


```VB

Public ReadOnly Property duration As System.Double
```





## <a name="property-value"></a>Valor da propriedade

Um **sistema. Double** que é a duração em segundos.

## <a name="remarks"></a>Comentários

Se essa propriedade for usada com um item de mídia diferente daquele especificado em AxWindowsMediaPlayer. currentMedia, ele não poderá conter um valor válido.

Para recuperar a duração de arquivos que não estão na biblioteca do usuário, você deve aguardar que o Windows Media Player Abra o arquivo; ou seja, o **OpenState** atual deve ser igual a **MediaOpen**. Você pode verificar isso tratando o **AxWindowsMediaPlayer. \_ Evento WMPOCXEvents \_ OpenStateChange** ou verificando periodicamente o valor de **AxWindowsMediaPlayer. OpenState**.

Para listas de reprodução, a duração de cada item de mídia pode ser recuperada quando o item de mídia individual é aberto, em vez de quando a playlist é aberta.

Antes de usar essa propriedade, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir usa **Duration** para exibir o tempo restante no item de mídia atual em um rótulo. Um temporizador atualiza o texto no rótulo a cada segundo.


```CSharp
// Set the timer to fire an event every second and start the timer.
timer.Interval = 1000;
timer.Start();

// Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
// determine when to start and stop the timer. 

private void TimerEventProcessor(object sender, System.EventArgs e)
{
    // Subtract the current position from the duration of the current media to get
    // the time remaining. Use the Math.floor method to round the result down to the
    // nearest whole number.
    double t = Math.Floor(player.currentMedia.duration - player.Ctlcontrols.currentPosition);

    // Display the time remaining in the current media.
    timeRemaining.Text = ("Seconds remaining: " + t.ToString());        
}
```


```VB

' Set the timer to fire an event every second and start the timer.
Timer.Interval = 1000
Timer.Start()

&#39; Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a Select Case statement to
&#39; determine when to start and stop the timer. 

Public Sub TimerEventProcessor(ByVal sender As Object, ByVal e As System.EventArgs) Handles Timer.Tick

    &#39; Subtract the current position from the duration of the current media to get
    &#39; the time remaining. Use the Math.Floor method to round the result down to the
    &#39; nearest whole number.
    Dim t As Double = Math.Floor(player.currentMedia.duration - player.Ctlcontrols.currentPosition)

    &#39; Display the time remaining in the current media.
    timeRemaining.Text = (&quot;Seconds remaining: &quot; + t.ToString())

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

[**AxWindowsMediaPlayer. currentMedia (VB e C#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. OpenState (VB e C#)**](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> <dt>

[**Evento AxWindowsMediaPlayer. OpenStateChange (VB e C#)**](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. durationstring (VB e C#)**](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)
</dt> </dl>

 

 





