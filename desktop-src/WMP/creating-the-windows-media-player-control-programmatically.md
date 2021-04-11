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
# <a name="creating-the-windows-media-player-control-programmatically"></a><span data-ttu-id="f691b-111">Criando o controle do Windows Media Player programaticamente</span><span class="sxs-lookup"><span data-stu-id="f691b-111">Creating the Windows Media Player Control Programmatically</span></span>

<span data-ttu-id="f691b-112">Quando você adiciona o controle do Windows Media Player a um formulário da caixa de ferramentas, um objeto da classe **AxWMPLib. AxWindowsMediaPlayer** é criado.</span><span class="sxs-lookup"><span data-stu-id="f691b-112">When you add the Windows Media Player control to a form from the Toolbox, an object of the class **AxWMPLib.AxWindowsMediaPlayer** is created.</span></span> <span data-ttu-id="f691b-113">Essa classe wrapper fornece ao Player toda a funcionalidade de um controle ActiveX, incluindo o acesso às propriedades da interface do usuário, como **local** e **tamanho**.</span><span class="sxs-lookup"><span data-stu-id="f691b-113">This wrapper class gives the Player all the functionality of an ActiveX control, including access to UI properties such as **Location** and **Size**.</span></span>

<span data-ttu-id="f691b-114">Se você não precisar das propriedades expostas por **AxWindowsMediaPlayer**, ou se seu aplicativo não tiver uma interface gráfica do usuário, você poderá criar um controle de jogador programaticamente.</span><span class="sxs-lookup"><span data-stu-id="f691b-114">If you do not require the properties exposed by **AxWindowsMediaPlayer**, or if your application does not have a graphical user interface, you can create a Player control programmatically.</span></span> <span data-ttu-id="f691b-115">Nesse caso, você cria um objeto da classe **WMPLib. WindowsMediaPlayer** .</span><span class="sxs-lookup"><span data-stu-id="f691b-115">In this case, you create an object of the **WMPLib.WindowsMediaPlayer** class.</span></span>

> [!Note]  
> <span data-ttu-id="f691b-116">Como o objeto **WindowsMediaPlayer** não é encapsulado como um controle ActiveX, ele não tem nenhuma propriedade herdada de **System. Windows. Forms. Control**.</span><span class="sxs-lookup"><span data-stu-id="f691b-116">Because the **WindowsMediaPlayer** object is not wrapped as an ActiveX control, it does not have any properties inherited from **System.Windows.Forms.Control**.</span></span> <span data-ttu-id="f691b-117">Como resultado, a propriedade **Controls** não é renomeada como **CtlControls**, pois está em **AxWindowsMediaPlayer**.</span><span class="sxs-lookup"><span data-stu-id="f691b-117">As a result, the **Controls** property is not renamed to **CtlControls**, as it is in **AxWindowsMediaPlayer**.</span></span>

 

<span data-ttu-id="f691b-118">Para criar o controle do Windows Media Player programaticamente, você deve primeiro adicionar uma referência a wmp.dll, que é encontrado na \\ \\ pasta system32 do Windows.</span><span class="sxs-lookup"><span data-stu-id="f691b-118">To create the Windows Media Player control programmatically, you must first add a reference to wmp.dll, which is found in the \\Windows\\system32 folder.</span></span> <span data-ttu-id="f691b-119">A adição dessa referência cria WMPLib.dll na pasta do projeto e uma referência a WMPLib aparece em Gerenciador de Soluções.</span><span class="sxs-lookup"><span data-stu-id="f691b-119">Adding this reference creates WMPLib.dll in your project folder, and a reference to WMPLib appears in Solution Explorer.</span></span>

<span data-ttu-id="f691b-120">O código de exemplo a seguir, parte de uma classe Form1, mostra como criar um objeto de **jogador** e reproduzir um arquivo.</span><span class="sxs-lookup"><span data-stu-id="f691b-120">The following example code, part of a Form1 class, shows how to create a **Player** object and play a file.</span></span> <span data-ttu-id="f691b-121">Quando a reprodução terminar, ou se o arquivo não puder ser reproduzido, o formulário será fechado.</span><span class="sxs-lookup"><span data-stu-id="f691b-121">When playback ends, or if the file cannot be played, the form is closed.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="f691b-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f691b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f691b-123">**Inserindo o controle do Windows Media Player em uma solução .NET Framework**</span><span class="sxs-lookup"><span data-stu-id="f691b-123">**Embedding the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




