---
title: Inserindo o controle do Windows Media Player em uma solução C
description: Inserindo o controle do Windows Media Player em uma solução C \
ms.assetid: 0889cfd8-ed1f-4d0c-aff8-bff2f55ffccb
keywords:
- Windows Media Player, incorporando controle ActiveX
- Modelo de objeto do Windows Media Player, inserindo controle ActiveX
- modelo de objeto, inserindo controle ActiveX
- Windows Media Player Mobile, inserindo controle ActiveX
- Controle ActiveX do Windows Media Player, incorporando
- Controle ActiveX móvel do Windows Media Player, incorporando
- Controle ActiveX, incorporando
- Windows Media Player, C
- Modelo de objeto do Windows Media Player, C
- modelo de objeto, C
- Windows Media Player Mobile, C
- Controle ActiveX do Windows Media Player, C
- Controle ActiveX móvel do Windows Media Player, C
- Controle ActiveX, C
- incorporando, programas C
- Inserção de programa C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c950bed9812cea0aa6ce28995fd6998bb8417ac
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2019
ms.locfileid: "105811110"
---
# <a name="embedding-the-windows-media-player-control-in-a-c-solution"></a>Inserindo o controle do Windows Media Player em uma solução C#

Para usar a funcionalidade do Windows Media Player em um aplicativo C#, primeiro adicione o componente a um formulário, conforme descrito em [usando o controle do Windows Media Player com Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)

As seções a seguir descrevem como criar um aplicativo que reproduz vídeo e usa botões de reprodução e parada personalizados.

## <a name="add-the-video-window"></a>Adicionar a janela de vídeo

Adicione o controle ActiveX do Windows Media Player a um formulário. Redimensione o controle e coloque-o onde você deseja que a janela de vídeo apareça.

Selecione o controle do Windows Media Player e, em seguida, altere a propriedade **UIMODE** para "None". Essa configuração oculta os controles da interface do usuário. Quando o usuário reproduzir um vídeo, ele será exibido na janela. Para conteúdo somente de áudio, uma visualização será exibida.

## <a name="add-two-buttons-and-adjust-the-form"></a>Adicionar dois botões e ajustar o formulário

Agora, adicione dois botões ao formulário. Selecione o primeiro botão e altere a propriedade **texto** para "reproduzir". Selecione o segundo botão e altere sua propriedade **Text** para "Stop".

## <a name="add-the-play-code"></a>Adicionar o código de reprodução

Clique duas vezes no botão **reproduzir** para revelar a janela de código. No C#, o código a seguir será exibido:


```CSharp
private void button1_Click(object sender, System.EventArgs e)
{

}

```



Adicione essa linha entre as duas chaves:


```CSharp
axWindowsMediaPlayer1.URL = @"c:\mediafile.wmv";

```



No exemplo de código anterior, "axWindowsMediaPlayer1" é o nome padrão do controle do Windows Media Player e "c: \\ mediafile. wmv" é um espaço reservado para o nome do item de mídia que você deseja reproduzir. Qualquer caminho de arquivo válido pode ser usado. O símbolo @ instrui o compilador a não interpretar barras invertidas como caracteres de escape.

Se você tiver adicionado o conteúdo de mídia digital do SDK do Windows Media Player à biblioteca no Windows Media Player, você poderá usar esse código:


```CSharp
axWindowsMediaPlayer1.currentPlaylist = axWindowsMediaPlayer1.mediaCollection.getByName("mediafile");

```



Como a propriedade **AutoStart** é true por padrão, o Windows Media Player começará a ser reproduzido quando você definir a propriedade **currentPlaylist** ou **URL** .

## <a name="add-the-stop-code"></a>Adicionar o código de parada

Clique duas vezes no botão **parar** para revelar a janela de código. No C#, o código a seguir será exibido:


```CSharp
private void button2_Click(object sender, System.EventArgs e)
{

}

```



Adicione essa linha entre as duas chaves:


```CSharp
axWindowsMediaPlayer1.Ctlcontrols.stop();

```



> [!Note]  
> O wrapper de código gerenciado para o controle do Windows Media Player expõe o objeto **Controls** como **Ctlcontrols** para evitar a colisão com a propriedade **Controls** herdada de **System. Windows. Forms. Control**.

 

## <a name="add-error-handling"></a>Adicionar tratamento de erros

O controle do Windows Media Player não gera uma exceção quando encontra um erro como uma URL inválida. Em vez disso, ele sinaliza um evento. Seu aplicativo deve lidar com eventos de erro enviados pelo Player.

Para criar um manipulador de eventos, primeiro abra o janela Propriedades para o controle do Windows Media Player. Na lista de eventos, clique duas vezes em **MediaError**. O código a seguir é exibido:


```CSharp
private void Player_MediaError(object sender, _WMPOCXEvents_MediaErrorEvent e)
{
}

```



O código a seguir pode ser inserido no método para fornecer o mínimo de recursos de manipulação de erros. Observe que as informações sobre o erro podem ser recuperadas do argumento **\_ WMPOCXEvents \_ MediaErrorEvent** .


```CSharp
try
// If the Player encounters a corrupt or missing file, 
// show the hexadecimal error code and URL.
{
    IWMPMedia2 errSource = e.pMediaObject as IWMPMedia2;
    IWMPErrorItem errorItem = errSource.Error;
    MessageBox.Show("Error " + errorItem.errorCode.ToString("X") 
                    + " in " + errSource.sourceURL);
}
catch(InvalidCastException)
// In case pMediaObject is not an IWMPMedia item.
{
    MessageBox.Show("Error.");
} 

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Inserindo o controle do Windows Media Player em uma solução .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




