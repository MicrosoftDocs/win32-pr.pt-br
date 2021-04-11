---
title: Inserindo o controle do Windows Media Player em uma solução Visual Basic .NET
description: Inserindo o controle do Windows Media Player em uma solução Visual Basic .NET
ms.assetid: e6428b42-5d8b-48ef-9f7a-c90a4625b745
keywords:
- Windows Media Player, incorporando controle ActiveX
- Modelo de objeto do Windows Media Player, inserindo controle ActiveX
- modelo de objeto, inserindo controle ActiveX
- Windows Media Player Mobile, inserindo controle ActiveX
- Controle ActiveX do Windows Media Player, incorporando
- Controle ActiveX móvel do Windows Media Player, incorporando
- Controle ActiveX, incorporando
- Windows Media Player, Visual Basic .NET
- Modelo de objeto do Windows Media Player, Visual Basic .NET
- modelo de objeto, Visual Basic .NET
- Windows Media Player Mobile, Visual Basic .NET
- Controle ActiveX do Windows Media Player, Visual Basic .NET
- Controle ActiveX móvel do Windows Media Player, Visual Basic .NET
- Controle ActiveX, Visual Basic .NET
- inserindo, Visual Basicndo programas .NET
- Incorporação de programa .NET Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d578b456a5064f1846ead7f074f178753dbc7c97
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2019
ms.locfileid: "104292909"
---
# <a name="embedding-the-windows-media-player-control-in-a-visual-basic-net-solution"></a>Inserindo o controle do Windows Media Player em uma solução Visual Basic .NET

Para usar a funcionalidade do Windows Media Player 9 Series ou posterior em um aplicativo Visual Basic .NET, primeiro adicione o componente a um formulário, conforme descrito em [usando o controle do Windows Media Player com Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)

Esta seção descreve como criar um aplicativo que reproduz vídeo e tem botões de reprodução e parada personalizados.

## <a name="add-the-video-window"></a>Adicionar a janela de vídeo

Adicione o controle do Windows Media Player a um formulário. Redimensione o controle e coloque-o onde você deseja que a janela de vídeo apareça.

Selecione o controle do Windows Media Player e, em seguida, altere a propriedade **UIMODE** para "None". Essa configuração oculta os controles da interface do usuário. Quando o usuário reproduzir um vídeo, ele será exibido na janela. Para conteúdo somente de áudio, uma visualização será exibida.

## <a name="add-two-buttons-and-adjust-the-form"></a>Adicionar dois botões e ajustar o formulário

Agora, adicione dois botões ao formulário. Selecione o primeiro botão e altere a propriedade **texto** para "reproduzir". Selecione o segundo botão e altere sua propriedade **Text** para "Stop".

## <a name="add-the-play-code"></a>Adicionar o código de reprodução

Clique duas vezes no botão **reproduzir** para revelar a janela de código. O código a seguir é exibido:


```VB
Private Sub Button1_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub
```



Adicione esta linha à sub-rotina:


```VB
AxWindowsMediaPlayer1.URL = "c:\mediafile.wmv"
```



No exemplo de código anterior, "axWindowsMediaPlayer1" é o nome padrão do controle do Windows Media Player e "c: \\ mediafile. wmv" é um espaço reservado para o nome da mídia que você deseja reproduzir.

Se você tiver adicionado o conteúdo de mídia digital do SDK do Windows Media Player à biblioteca no Windows Media Player, você poderá usar esse código:


```VB
axWindowsMediaPlayer1.currentPlaylist = _
    axWindowsMediaPlayer1.mediaCollection.getByName("mediafile")

```



Como a propriedade **AutoStart** é true por padrão, o Windows Media Player começará a ser reproduzido quando você definir a propriedade **currentPlaylist** ou **URL** .

## <a name="add-the-stop-code"></a>Adicionar o código de parada

Clique duas vezes no botão **parar** para revelar a janela de código. O código a seguir é exibido:


```VB
Private Sub Button2_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub

```



Adicione esta linha à sub-rotina:


```VB
AxWindowsMediaPlayer1.Ctlcontrols.stop()

```



> [!Note]  
> O wrapper de código gerenciado para o controle do Windows Media Player expõe o objeto **Controls** como **Ctlcontrols** para evitar a colisão com a propriedade **Controls** herdada de **System. Windows. Forms. Control**.

 

## <a name="add-error-handling"></a>Adicionar tratamento de erros

O controle do Windows Media Player não gera uma exceção quando encontra um erro como uma URL inválida. Em vez disso, o controle sinaliza um evento. Seu aplicativo deve lidar com eventos de erro enviados pelo Player.

Para criar um manipulador de eventos, abra a janela de código para sua classe de formulário. Na lista suspensa na parte superior da janela, selecione o controle do Windows Media Player. Uma lista de eventos é exibida na lista suspensa à direita. Nessa lista, selecione [**MediaError**](axwmplib-axwindowsmediaplayer-mediaerror.md). O código a seguir é exibido:


```VB
Private Sub AxWindowsMediaPlayer1_MediaError(ByVal sender As Object, _
    ByVal e As _WMPOCXEvents_MediaErrorEvent) Handles AxWindowsMediaPlayer1.MediaError

End Sub

```



O código a seguir pode ser inserido na sub-rotina para fornecer o mínimo de recursos de manipulação de erros. Observe que as informações sobre o erro podem ser recuperadas do argumento **\_ WMPOCXEvents \_ MediaErrorEvent** .


```VB
Try
    ' If the file is corrupt or missing, show the 
    ' hexadecimal error code and URL.
    Dim errSource As WMPLib.IWMPMedia2 = e.pMediaObject
    Dim errorItem As WMPLib.IWMPErrorItem = errSource.Error
    MessageBox.Show("Media error " + errorItem.errorCode.ToString("X") _
                    + " in " + errSource.sourceURL)
Catch ex As InvalidCastException
    ' In case pMediaObject is not an IWMPMedia item.
    MessageBox.Show("Player error.")
End Try

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Inserindo o controle do Windows Media Player em uma solução .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




