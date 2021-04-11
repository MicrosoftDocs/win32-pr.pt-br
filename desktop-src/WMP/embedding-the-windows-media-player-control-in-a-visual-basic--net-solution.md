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
# <a name="embedding-the-windows-media-player-control-in-a-visual-basic-net-solution"></a><span data-ttu-id="6a014-119">Inserindo o controle do Windows Media Player em uma solução Visual Basic .NET</span><span class="sxs-lookup"><span data-stu-id="6a014-119">Embedding the Windows Media Player Control in a Visual Basic .NET Solution</span></span>

<span data-ttu-id="6a014-120">Para usar a funcionalidade do Windows Media Player 9 Series ou posterior em um aplicativo Visual Basic .NET, primeiro adicione o componente a um formulário, conforme descrito em [usando o controle do Windows Media Player com Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)</span><span class="sxs-lookup"><span data-stu-id="6a014-120">To use the functionality of Windows Media Player 9 Series or later in a Visual Basic .NET application, first add the component to a form as described in [Using the Windows Media Player Control with Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)</span></span>

<span data-ttu-id="6a014-121">Esta seção descreve como criar um aplicativo que reproduz vídeo e tem botões de reprodução e parada personalizados.</span><span class="sxs-lookup"><span data-stu-id="6a014-121">This section describes how to create an application that plays video and has custom play and stop buttons.</span></span>

## <a name="add-the-video-window"></a><span data-ttu-id="6a014-122">Adicionar a janela de vídeo</span><span class="sxs-lookup"><span data-stu-id="6a014-122">Add the Video Window</span></span>

<span data-ttu-id="6a014-123">Adicione o controle do Windows Media Player a um formulário.</span><span class="sxs-lookup"><span data-stu-id="6a014-123">Add the Windows Media Player control to a form.</span></span> <span data-ttu-id="6a014-124">Redimensione o controle e coloque-o onde você deseja que a janela de vídeo apareça.</span><span class="sxs-lookup"><span data-stu-id="6a014-124">Resize the control, and then place it where you want the video window to appear.</span></span>

<span data-ttu-id="6a014-125">Selecione o controle do Windows Media Player e, em seguida, altere a propriedade **UIMODE** para "None".</span><span class="sxs-lookup"><span data-stu-id="6a014-125">Select the Windows Media Player control, then change the **uiMode** property to "none".</span></span> <span data-ttu-id="6a014-126">Essa configuração oculta os controles da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="6a014-126">This setting hides the UI controls.</span></span> <span data-ttu-id="6a014-127">Quando o usuário reproduzir um vídeo, ele será exibido na janela.</span><span class="sxs-lookup"><span data-stu-id="6a014-127">When the user plays a video, it will appear in the window.</span></span> <span data-ttu-id="6a014-128">Para conteúdo somente de áudio, uma visualização será exibida.</span><span class="sxs-lookup"><span data-stu-id="6a014-128">For audio-only content, a visualization will appear.</span></span>

## <a name="add-two-buttons-and-adjust-the-form"></a><span data-ttu-id="6a014-129">Adicionar dois botões e ajustar o formulário</span><span class="sxs-lookup"><span data-stu-id="6a014-129">Add Two Buttons and Adjust the Form</span></span>

<span data-ttu-id="6a014-130">Agora, adicione dois botões ao formulário.</span><span class="sxs-lookup"><span data-stu-id="6a014-130">Now add two buttons to the form.</span></span> <span data-ttu-id="6a014-131">Selecione o primeiro botão e altere a propriedade **texto** para "reproduzir".</span><span class="sxs-lookup"><span data-stu-id="6a014-131">Select the first button and change the **Text** property to "Play".</span></span> <span data-ttu-id="6a014-132">Selecione o segundo botão e altere sua propriedade **Text** para "Stop".</span><span class="sxs-lookup"><span data-stu-id="6a014-132">Select the second button and change its **Text** property to "Stop".</span></span>

## <a name="add-the-play-code"></a><span data-ttu-id="6a014-133">Adicionar o código de reprodução</span><span class="sxs-lookup"><span data-stu-id="6a014-133">Add the Play Code</span></span>

<span data-ttu-id="6a014-134">Clique duas vezes no botão **reproduzir** para revelar a janela de código.</span><span class="sxs-lookup"><span data-stu-id="6a014-134">Double-click the **Play** button to reveal the Code window.</span></span> <span data-ttu-id="6a014-135">O código a seguir é exibido:</span><span class="sxs-lookup"><span data-stu-id="6a014-135">The following code is displayed:</span></span>


```VB
Private Sub Button1_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub
```



<span data-ttu-id="6a014-136">Adicione esta linha à sub-rotina:</span><span class="sxs-lookup"><span data-stu-id="6a014-136">Add this line to the subroutine:</span></span>


```VB
AxWindowsMediaPlayer1.URL = "c:\mediafile.wmv"
```



<span data-ttu-id="6a014-137">No exemplo de código anterior, "axWindowsMediaPlayer1" é o nome padrão do controle do Windows Media Player e "c: \\ mediafile. wmv" é um espaço reservado para o nome da mídia que você deseja reproduzir.</span><span class="sxs-lookup"><span data-stu-id="6a014-137">In the preceding code example, "axWindowsMediaPlayer1" is the default name of the Windows Media Player control and "c:\\mediafile.wmv" is a placeholder for the name of the media you want to play.</span></span>

<span data-ttu-id="6a014-138">Se você tiver adicionado o conteúdo de mídia digital do SDK do Windows Media Player à biblioteca no Windows Media Player, você poderá usar esse código:</span><span class="sxs-lookup"><span data-stu-id="6a014-138">If you have added the digital media content from the Windows Media Player SDK to the library in Windows Media Player, you can use this code instead:</span></span>


```VB
axWindowsMediaPlayer1.currentPlaylist = _
    axWindowsMediaPlayer1.mediaCollection.getByName("mediafile")

```



<span data-ttu-id="6a014-139">Como a propriedade **AutoStart** é true por padrão, o Windows Media Player começará a ser reproduzido quando você definir a propriedade **currentPlaylist** ou **URL** .</span><span class="sxs-lookup"><span data-stu-id="6a014-139">Because the **autoStart** property is true by default, Windows Media Player will start playing when you set the **currentPlaylist** or **URL** property.</span></span>

## <a name="add-the-stop-code"></a><span data-ttu-id="6a014-140">Adicionar o código de parada</span><span class="sxs-lookup"><span data-stu-id="6a014-140">Add the Stop Code</span></span>

<span data-ttu-id="6a014-141">Clique duas vezes no botão **parar** para revelar a janela de código.</span><span class="sxs-lookup"><span data-stu-id="6a014-141">Double-click the **Stop** button to reveal the Code window.</span></span> <span data-ttu-id="6a014-142">O código a seguir é exibido:</span><span class="sxs-lookup"><span data-stu-id="6a014-142">The following code is displayed:</span></span>


```VB
Private Sub Button2_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub

```



<span data-ttu-id="6a014-143">Adicione esta linha à sub-rotina:</span><span class="sxs-lookup"><span data-stu-id="6a014-143">Add this line to the subroutine:</span></span>


```VB
AxWindowsMediaPlayer1.Ctlcontrols.stop()

```



> [!Note]  
> <span data-ttu-id="6a014-144">O wrapper de código gerenciado para o controle do Windows Media Player expõe o objeto **Controls** como **Ctlcontrols** para evitar a colisão com a propriedade **Controls** herdada de **System. Windows. Forms. Control**.</span><span class="sxs-lookup"><span data-stu-id="6a014-144">The managed-code wrapper for the Windows Media Player control exposes the **Controls** object as **Ctlcontrols** to avoid collision with the **Controls** property inherited from **System.Windows.Forms.Control**.</span></span>

 

## <a name="add-error-handling"></a><span data-ttu-id="6a014-145">Adicionar tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="6a014-145">Add Error-handling</span></span>

<span data-ttu-id="6a014-146">O controle do Windows Media Player não gera uma exceção quando encontra um erro como uma URL inválida.</span><span class="sxs-lookup"><span data-stu-id="6a014-146">The Windows Media Player control does not raise an exception when it encounters an error such as an invalid URL.</span></span> <span data-ttu-id="6a014-147">Em vez disso, o controle sinaliza um evento.</span><span class="sxs-lookup"><span data-stu-id="6a014-147">Instead, the control signals an event.</span></span> <span data-ttu-id="6a014-148">Seu aplicativo deve lidar com eventos de erro enviados pelo Player.</span><span class="sxs-lookup"><span data-stu-id="6a014-148">Your application should handle error events sent by the Player.</span></span>

<span data-ttu-id="6a014-149">Para criar um manipulador de eventos, abra a janela de código para sua classe de formulário.</span><span class="sxs-lookup"><span data-stu-id="6a014-149">To create an event handler, open the code window for your form class.</span></span> <span data-ttu-id="6a014-150">Na lista suspensa na parte superior da janela, selecione o controle do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6a014-150">From the drop-down list at the top of the window, select the Windows Media Player control.</span></span> <span data-ttu-id="6a014-151">Uma lista de eventos é exibida na lista suspensa à direita.</span><span class="sxs-lookup"><span data-stu-id="6a014-151">A list of events appears in the drop-down list to the right.</span></span> <span data-ttu-id="6a014-152">Nessa lista, selecione [**MediaError**](axwmplib-axwindowsmediaplayer-mediaerror.md).</span><span class="sxs-lookup"><span data-stu-id="6a014-152">From that list, select [**MediaError**](axwmplib-axwindowsmediaplayer-mediaerror.md).</span></span> <span data-ttu-id="6a014-153">O código a seguir é exibido:</span><span class="sxs-lookup"><span data-stu-id="6a014-153">The following code is displayed:</span></span>


```VB
Private Sub AxWindowsMediaPlayer1_MediaError(ByVal sender As Object, _
    ByVal e As _WMPOCXEvents_MediaErrorEvent) Handles AxWindowsMediaPlayer1.MediaError

End Sub

```



<span data-ttu-id="6a014-154">O código a seguir pode ser inserido na sub-rotina para fornecer o mínimo de recursos de manipulação de erros.</span><span class="sxs-lookup"><span data-stu-id="6a014-154">The following code could be inserted in the subroutine to provide minimal error-handling capability.</span></span> <span data-ttu-id="6a014-155">Observe que as informações sobre o erro podem ser recuperadas do argumento **\_ WMPOCXEvents \_ MediaErrorEvent** .</span><span class="sxs-lookup"><span data-stu-id="6a014-155">Note that information about the error can be retrieved from the **\_WMPOCXEvents\_MediaErrorEvent** argument.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6a014-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6a014-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a014-157">**Inserindo o controle do Windows Media Player em uma solução .NET Framework**</span><span class="sxs-lookup"><span data-stu-id="6a014-157">**Embedding the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




