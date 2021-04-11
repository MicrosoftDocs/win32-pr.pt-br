---
title: Criando o controle do Windows Media Player programaticamente
description: Criando o controle do Windows Media Player programaticamente
ms.assetid: 9a4856ce-6a44-47fb-b863-59ce4deb0597
keywords:
- Windows Media Player, criando controle ActiveX programaticamente
- Modelo de objeto do Windows Media Player, criando controle ActiveX programaticamente
- modelo de objeto, criando controle ActiveX programaticamente
- Windows Media Player Mobile, criando controle ActiveX programaticamente
- Controle ActiveX do Windows Media Player, criando programaticamente
- Controle ActiveX móvel do Windows Media Player, criando programaticamente
- Controle ActiveX, criando programaticamente
- Criando o controle ActiveX programaticamente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222c207b33dcc13a5392f79dad267d6ee82a677c
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2019
ms.locfileid: "104292907"
---
# <a name="creating-the-windows-media-player-control-programmatically"></a>Criando o controle do Windows Media Player programaticamente

Quando você adiciona o controle do Windows Media Player a um formulário da caixa de ferramentas, um objeto da classe **AxWMPLib. AxWindowsMediaPlayer** é criado. Essa classe wrapper fornece ao Player toda a funcionalidade de um controle ActiveX, incluindo o acesso às propriedades da interface do usuário, como **local** e **tamanho**.

Se você não precisar das propriedades expostas por **AxWindowsMediaPlayer**, ou se seu aplicativo não tiver uma interface gráfica do usuário, você poderá criar um controle de jogador programaticamente. Nesse caso, você cria um objeto da classe **WMPLib. WindowsMediaPlayer** .

> [!Note]  
> Como o objeto **WindowsMediaPlayer** não é encapsulado como um controle ActiveX, ele não tem nenhuma propriedade herdada de **System. Windows. Forms. Control**. Como resultado, a propriedade **Controls** não é renomeada como **CtlControls**, pois está em **AxWindowsMediaPlayer**.

 

Para criar o controle do Windows Media Player programaticamente, você deve primeiro adicionar uma referência a wmp.dll, que é encontrado na \\ \\ pasta system32 do Windows. A adição dessa referência cria WMPLib.dll na pasta do projeto e uma referência a WMPLib aparece em Gerenciador de Soluções.

O código de exemplo a seguir, parte de uma classe Form1, mostra como criar um objeto de **jogador** e reproduzir um arquivo. Quando a reprodução terminar, ou se o arquivo não puder ser reproduzido, o formulário será fechado.


```VB
Dim WithEvents Player As WMPLib.WindowsMediaPlayer

Private Sub PlayFile(ByVal url As String)
    Player = New WMPLib.WindowsMediaPlayer
    Player.URL = url
    Player.controls.play()
End Sub

Private Sub Form1_Load(ByVal sender As Object, ByVal e As System.EventArgs) _
                       Handles MyBase.Load
    ' TODO  Insert a valid path in the line below.
    PlayFile("c:\media\myaudio.wma")
End Sub

Private Sub Player_MediaError(ByVal pMediaObject As Object) _
                              Handles Player.MediaError
    MessageBox.Show("Cannot play media file.")
    Me.Close()
End Sub

Private Sub Player_PlayStateChange(ByVal NewState As Integer) _
                                   Handles Player.PlayStateChange
    If NewState = WMPLib.WMPPlayState.wmppsStopped Then
        Me.Close()
    End If
End Sub

```




```CSharp
WMPLib.WindowsMediaPlayer Player;

private void PlayFile(String url)
{
    Player = new WMPLib.WindowsMediaPlayer();
    Player.PlayStateChange += 
        new WMPLib._WMPOCXEvents_PlayStateChangeEventHandler(Player_PlayStateChange);
    Player.MediaError += 
        new WMPLib._WMPOCXEvents_MediaErrorEventHandler(Player_MediaError);
    Player.URL = url;
    Player.controls.play();
}

private void Form1_Load(object sender, System.EventArgs e)
{
    // TODO  Insert a valid path in the line below.
    PlayFile(@"c:\myaudio.wma");
}

private void Player_PlayStateChange(int NewState)
{
    if ((WMPLib.WMPPlayState)NewState == WMPLib.WMPPlayState.wmppsStopped)
    {
        this.Close();
    }
}

private void Player_MediaError(object pMediaObject)
{
    MessageBox.Show("Cannot play media file.");
    this.Close();
}


```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Inserindo o controle do Windows Media Player em uma solução .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




