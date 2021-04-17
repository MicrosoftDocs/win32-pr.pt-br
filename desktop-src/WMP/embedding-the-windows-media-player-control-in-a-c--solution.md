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
# <a name="embedding-the-windows-media-player-control-in-a-c-solution"></a><span data-ttu-id="d51d2-119">Inserindo o controle do Windows Media Player em uma solução C#</span><span class="sxs-lookup"><span data-stu-id="d51d2-119">Embedding the Windows Media Player Control in a C# Solution</span></span>

<span data-ttu-id="d51d2-120">Para usar a funcionalidade do Windows Media Player em um aplicativo C#, primeiro adicione o componente a um formulário, conforme descrito em [usando o controle do Windows Media Player com Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)</span><span class="sxs-lookup"><span data-stu-id="d51d2-120">To use the functionality of Windows Media Player in a C# application, first add the component to a form as described in [Using the Windows Media Player Control with Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)</span></span>

<span data-ttu-id="d51d2-121">As seções a seguir descrevem como criar um aplicativo que reproduz vídeo e usa botões de reprodução e parada personalizados.</span><span class="sxs-lookup"><span data-stu-id="d51d2-121">The following sections describe how to create an application that plays video and uses custom play and stop buttons.</span></span>

## <a name="add-the-video-window"></a><span data-ttu-id="d51d2-122">Adicionar a janela de vídeo</span><span class="sxs-lookup"><span data-stu-id="d51d2-122">Add the Video Window</span></span>

<span data-ttu-id="d51d2-123">Adicione o controle ActiveX do Windows Media Player a um formulário.</span><span class="sxs-lookup"><span data-stu-id="d51d2-123">Add the Windows Media Player ActiveX control to a form.</span></span> <span data-ttu-id="d51d2-124">Redimensione o controle e coloque-o onde você deseja que a janela de vídeo apareça.</span><span class="sxs-lookup"><span data-stu-id="d51d2-124">Resize the control, and then place it where you want the video window to appear.</span></span>

<span data-ttu-id="d51d2-125">Selecione o controle do Windows Media Player e, em seguida, altere a propriedade **UIMODE** para "None".</span><span class="sxs-lookup"><span data-stu-id="d51d2-125">Select the Windows Media Player control, then change the **uiMode** property to "none".</span></span> <span data-ttu-id="d51d2-126">Essa configuração oculta os controles da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="d51d2-126">This setting hides the UI controls.</span></span> <span data-ttu-id="d51d2-127">Quando o usuário reproduzir um vídeo, ele será exibido na janela.</span><span class="sxs-lookup"><span data-stu-id="d51d2-127">When the user plays a video, it will appear in the window.</span></span> <span data-ttu-id="d51d2-128">Para conteúdo somente de áudio, uma visualização será exibida.</span><span class="sxs-lookup"><span data-stu-id="d51d2-128">For audio-only content, a visualization will appear.</span></span>

## <a name="add-two-buttons-and-adjust-the-form"></a><span data-ttu-id="d51d2-129">Adicionar dois botões e ajustar o formulário</span><span class="sxs-lookup"><span data-stu-id="d51d2-129">Add Two Buttons and Adjust the Form</span></span>

<span data-ttu-id="d51d2-130">Agora, adicione dois botões ao formulário.</span><span class="sxs-lookup"><span data-stu-id="d51d2-130">Now, add two buttons to the form.</span></span> <span data-ttu-id="d51d2-131">Selecione o primeiro botão e altere a propriedade **texto** para "reproduzir".</span><span class="sxs-lookup"><span data-stu-id="d51d2-131">Select the first button and change the **Text** property to "Play".</span></span> <span data-ttu-id="d51d2-132">Selecione o segundo botão e altere sua propriedade **Text** para "Stop".</span><span class="sxs-lookup"><span data-stu-id="d51d2-132">Select the second button and change its **Text** property to "Stop".</span></span>

## <a name="add-the-play-code"></a><span data-ttu-id="d51d2-133">Adicionar o código de reprodução</span><span class="sxs-lookup"><span data-stu-id="d51d2-133">Add the Play Code</span></span>

<span data-ttu-id="d51d2-134">Clique duas vezes no botão **reproduzir** para revelar a janela de código.</span><span class="sxs-lookup"><span data-stu-id="d51d2-134">Double-click the **Play** button to reveal the Code window.</span></span> <span data-ttu-id="d51d2-135">No C#, o código a seguir será exibido:</span><span class="sxs-lookup"><span data-stu-id="d51d2-135">In C#, the following code will be displayed:</span></span>


```CSharp
private void button1_Click(object sender, System.EventArgs e)
{

}

```



<span data-ttu-id="d51d2-136">Adicione essa linha entre as duas chaves:</span><span class="sxs-lookup"><span data-stu-id="d51d2-136">Add this line between the two curly braces:</span></span>


```CSharp
axWindowsMediaPlayer1.URL = @"c:\mediafile.wmv";

```



<span data-ttu-id="d51d2-137">No exemplo de código anterior, "axWindowsMediaPlayer1" é o nome padrão do controle do Windows Media Player e "c: \\ mediafile. wmv" é um espaço reservado para o nome do item de mídia que você deseja reproduzir.</span><span class="sxs-lookup"><span data-stu-id="d51d2-137">In the preceding code example, "axWindowsMediaPlayer1" is the default name of the Windows Media Player control, and "c:\\mediafile.wmv" is a placeholder for the name of the media item you want to play.</span></span> <span data-ttu-id="d51d2-138">Qualquer caminho de arquivo válido pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="d51d2-138">Any valid file path can be used.</span></span> <span data-ttu-id="d51d2-139">O símbolo @ instrui o compilador a não interpretar barras invertidas como caracteres de escape.</span><span class="sxs-lookup"><span data-stu-id="d51d2-139">The @ symbol instructs the compiler to not interpret backslashes as escape characters.</span></span>

<span data-ttu-id="d51d2-140">Se você tiver adicionado o conteúdo de mídia digital do SDK do Windows Media Player à biblioteca no Windows Media Player, você poderá usar esse código:</span><span class="sxs-lookup"><span data-stu-id="d51d2-140">If you have added the digital media content from the Windows Media Player SDK to the library in Windows Media Player, you can use this code instead:</span></span>


```CSharp
axWindowsMediaPlayer1.currentPlaylist = axWindowsMediaPlayer1.mediaCollection.getByName("mediafile");

```



<span data-ttu-id="d51d2-141">Como a propriedade **AutoStart** é true por padrão, o Windows Media Player começará a ser reproduzido quando você definir a propriedade **currentPlaylist** ou **URL** .</span><span class="sxs-lookup"><span data-stu-id="d51d2-141">Because the **autoStart** property is true by default, Windows Media Player will start playing when you set the **currentPlaylist** or **URL** property.</span></span>

## <a name="add-the-stop-code"></a><span data-ttu-id="d51d2-142">Adicionar o código de parada</span><span class="sxs-lookup"><span data-stu-id="d51d2-142">Add the Stop Code</span></span>

<span data-ttu-id="d51d2-143">Clique duas vezes no botão **parar** para revelar a janela de código.</span><span class="sxs-lookup"><span data-stu-id="d51d2-143">Double-click the **Stop** button to reveal the Code window.</span></span> <span data-ttu-id="d51d2-144">No C#, o código a seguir será exibido:</span><span class="sxs-lookup"><span data-stu-id="d51d2-144">In C#, the following code will be displayed:</span></span>


```CSharp
private void button2_Click(object sender, System.EventArgs e)
{

}

```



<span data-ttu-id="d51d2-145">Adicione essa linha entre as duas chaves:</span><span class="sxs-lookup"><span data-stu-id="d51d2-145">Add this line between the two curly braces:</span></span>


```CSharp
axWindowsMediaPlayer1.Ctlcontrols.stop();

```



> [!Note]  
> <span data-ttu-id="d51d2-146">O wrapper de código gerenciado para o controle do Windows Media Player expõe o objeto **Controls** como **Ctlcontrols** para evitar a colisão com a propriedade **Controls** herdada de **System. Windows. Forms. Control**.</span><span class="sxs-lookup"><span data-stu-id="d51d2-146">The managed-code wrapper for the Windows Media Player control exposes the **Controls** object as **Ctlcontrols** to avoid collision with the **Controls** property inherited from **System.Windows.Forms.Control**.</span></span>

 

## <a name="add-error-handling"></a><span data-ttu-id="d51d2-147">Adicionar tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="d51d2-147">Add Error-handling</span></span>

<span data-ttu-id="d51d2-148">O controle do Windows Media Player não gera uma exceção quando encontra um erro como uma URL inválida.</span><span class="sxs-lookup"><span data-stu-id="d51d2-148">The Windows Media Player control does not raise an exception when it encounters an error such as an invalid URL.</span></span> <span data-ttu-id="d51d2-149">Em vez disso, ele sinaliza um evento.</span><span class="sxs-lookup"><span data-stu-id="d51d2-149">Instead, it signals an event.</span></span> <span data-ttu-id="d51d2-150">Seu aplicativo deve lidar com eventos de erro enviados pelo Player.</span><span class="sxs-lookup"><span data-stu-id="d51d2-150">Your application should handle error events sent by the Player.</span></span>

<span data-ttu-id="d51d2-151">Para criar um manipulador de eventos, primeiro abra o janela Propriedades para o controle do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d51d2-151">To create an event handler, first open the Properties window for the Windows Media Player control.</span></span> <span data-ttu-id="d51d2-152">Na lista de eventos, clique duas vezes em **MediaError**.</span><span class="sxs-lookup"><span data-stu-id="d51d2-152">In the list of events, double-click **MediaError**.</span></span> <span data-ttu-id="d51d2-153">O código a seguir é exibido:</span><span class="sxs-lookup"><span data-stu-id="d51d2-153">The following code is displayed:</span></span>


```CSharp
private void Player_MediaError(object sender, _WMPOCXEvents_MediaErrorEvent e)
{
}

```



<span data-ttu-id="d51d2-154">O código a seguir pode ser inserido no método para fornecer o mínimo de recursos de manipulação de erros.</span><span class="sxs-lookup"><span data-stu-id="d51d2-154">The following code could be inserted in the method to provide minimal error-handling capability.</span></span> <span data-ttu-id="d51d2-155">Observe que as informações sobre o erro podem ser recuperadas do argumento **\_ WMPOCXEvents \_ MediaErrorEvent** .</span><span class="sxs-lookup"><span data-stu-id="d51d2-155">Note that information about the error can be retrieved from the **\_WMPOCXEvents\_MediaErrorEvent** argument.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d51d2-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d51d2-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d51d2-157">**Inserindo o controle do Windows Media Player em uma solução .NET Framework**</span><span class="sxs-lookup"><span data-stu-id="d51d2-157">**Embedding the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




