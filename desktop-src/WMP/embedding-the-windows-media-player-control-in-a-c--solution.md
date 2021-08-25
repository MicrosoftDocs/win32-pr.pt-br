---
title: inserindo o controle de Windows Media Player em uma solução C
description: inserindo o controle de Windows Media Player em uma solução C \
ms.assetid: 0889cfd8-ed1f-4d0c-aff8-bff2f55ffccb
keywords:
- Windows Media Player, inserindo controle de ActiveX
- modelo de objeto Windows Media Player, inserindo ActiveX controle
- modelo de objeto, inserindo ActiveX controle
- Windows Media Player controle de ActiveX móvel, incorporando
- Windows Media Player controle de ActiveX, inserindo
- Windows Media Player controle de ActiveX móvel, incorporando
- controle de ActiveX, inserindo
- Windows Media Player, C
- modelo de objeto Windows Media Player, C
- modelo de objeto, C
- Windows Media Player Móvel, C
- Windows Media Player controle de ActiveX, C
- Windows Media Player controle de ActiveX móvel, C
- controle de ActiveX, C
- incorporando, programas C
- Inserção de programa C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a067a407fccdd78d71d9e60bc00d1eae6950e3fdaf204f886c5e96edf372eb07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901976"
---
# <a name="embedding-the-windows-media-player-control-in-a-c-solution"></a>inserindo o controle de Windows Media Player em uma solução C#

para usar a funcionalidade de Windows Media Player em um aplicativo C#, primeiro adicione o componente a um formulário, conforme descrito em [usando o controle de Windows Media Player com Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)

As seções a seguir descrevem como criar um aplicativo que reproduz vídeo e usa botões de reprodução e parada personalizados.

## <a name="add-the-video-window"></a>Adicionar a janela de vídeo

adicione o controle de ActiveX de Windows Media Player a um formulário. Redimensione o controle e coloque-o onde você deseja que a janela de vídeo apareça.

selecione o controle de Windows Media Player e, em seguida, altere a propriedade **uiMode** para "none". Essa configuração oculta os controles da interface do usuário. Quando o usuário reproduzir um vídeo, ele será exibido na janela. Para conteúdo somente de áudio, uma visualização será exibida.

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



no exemplo de código anterior, "axWindowsMediaPlayer1" é o nome padrão do controle de Windows Media Player e "c: \\ mediafile. wmv" é um espaço reservado para o nome do item de mídia que você deseja reproduzir. Qualquer caminho de arquivo válido pode ser usado. O símbolo @ instrui o compilador a não interpretar barras invertidas como caracteres de escape.

se você tiver adicionado o conteúdo de mídia digital do SDK do Windows Media Player à biblioteca no Windows Media Player, você poderá usar esse código:


```CSharp
axWindowsMediaPlayer1.currentPlaylist = axWindowsMediaPlayer1.mediaCollection.getByName("mediafile");

```



como a propriedade **autostart** é true por padrão, Windows Media Player começará a ser reproduzida quando você definir a propriedade **currentPlaylist** ou **URL** .

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
> o wrapper de código gerenciado para o controle de Windows Media Player expõe o objeto **Controls** como **Ctlcontrols** para evitar a colisão com a propriedade **controls** herdada de **System. Windows. Forms. Control**.

 

## <a name="add-error-handling"></a>Adicionar tratamento de erros

o controle de Windows Media Player não gera uma exceção quando encontra um erro como uma URL inválida. Em vez disso, ele sinaliza um evento. Seu aplicativo deve lidar com eventos de erro enviados pelo Player.

para criar um manipulador de eventos, primeiro abra o janela Propriedades para o controle de Windows Media Player. Na lista de eventos, clique duas vezes em **MediaError**. O código a seguir é exibido:


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

[**inserindo o controle de Windows Media Player em uma solução de .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




