---
title: Usando o controle do Windows Media Player com Microsoft Visual Studio
description: Usando o controle do Windows Media Player com Microsoft Visual Studio
ms.assetid: e007876e-f215-4976-8a70-018fedc0e67d
keywords:
- Windows Media Player, incorporando controle ActiveX
- Modelo de objeto do Windows Media Player, inserindo controle ActiveX
- modelo de objeto, inserindo controle ActiveX
- Windows Media Player Mobile, inserindo controle ActiveX
- Controle ActiveX do Windows Media Player, incorporando
- Controle ActiveX móvel do Windows Media Player, incorporando
- Controle ActiveX, incorporando
- Windows Media Player,. NET Framework
- Modelo de objeto do Windows Media Player,. NET Framework
- modelo de objeto,. NET Framework
- Windows Media Player Mobile, .NET Framework
- Controle ActiveX do Windows Media Player, .NET Framework
- Controle ActiveX móvel do Windows Media Player, .NET Framework
- Controle ActiveX, .NET Framework
- Controle ActiveX do Windows Media Player, Visual Studio
- Controle ActiveX móvel do Windows Media Player, Visual Studio
- Controle ActiveX, Visual Studio
- .NET Framework, incorporação de programa do Visual Studio
- incorporando, programas do Visual Studio
- Visual Studio, incorporação de programa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b01fecd6acdfd5ccc9a7d823740ef3915bf9c6
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2019
ms.locfileid: "104006221"
---
# <a name="using-the-windows-media-player-control-with-microsoft-visual-studio"></a><span data-ttu-id="bb1bb-123">Usando o controle do Windows Media Player com Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bb1bb-123">Using the Windows Media Player Control with Microsoft Visual Studio</span></span>

<span data-ttu-id="bb1bb-124">Você pode adicionar o controle ActiveX do Windows Media Player 9 Series ou posterior a um aplicativo .NET Framework por meio da caixa de ferramentas no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="bb1bb-124">You can add the Windows Media Player 9 Series or later ActiveX control to a .NET Framework application through the Toolbox in Visual Studio.</span></span>

## <a name="adding-the-windows-media-player-control"></a><span data-ttu-id="bb1bb-125">Adicionando o controle do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="bb1bb-125">Adding the Windows Media Player Control</span></span>

<span data-ttu-id="bb1bb-126">Antes de criar um novo projeto, verifique se a versão mais recente do Windows Media Player e o SDK do Windows Media Player estão instalados no computador.</span><span class="sxs-lookup"><span data-stu-id="bb1bb-126">Before creating a new project, make sure that the latest version of Windows Media Player and the Windows Media Player SDK is installed on your computer.</span></span>

<span data-ttu-id="bb1bb-127">Inicie o Visual Studio e crie um novo projeto.</span><span class="sxs-lookup"><span data-stu-id="bb1bb-127">Start Visual Studio, then create a new project.</span></span>

<span data-ttu-id="bb1bb-128">No Visual Studio, abra a caixa de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="bb1bb-128">In Visual Studio, open the Toolbox.</span></span>

<span data-ttu-id="bb1bb-129">Se o Windows Media Player não aparecer na parte **componentes** da caixa de ferramentas, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="bb1bb-129">If Windows Media Player does not appear in the **Components** portion of the Toolbox, do the following:</span></span>

1.  <span data-ttu-id="bb1bb-130">Clique com o botão direito do mouse na caixa de ferramentas e selecione **escolher itens**.</span><span class="sxs-lookup"><span data-stu-id="bb1bb-130">Right-click within the Toolbox, and then select **Choose Items**.</span></span> <span data-ttu-id="bb1bb-131">Isso abre a caixa de diálogo Personalizar caixas de **ferramentas** .</span><span class="sxs-lookup"><span data-stu-id="bb1bb-131">This opens the **Customize Toolbox** dialog box.</span></span>
2.  <span data-ttu-id="bb1bb-132">Na guia **componentes com** , selecione Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="bb1bb-132">On the **COM Components** tab, select Windows Media Player.</span></span>

    <span data-ttu-id="bb1bb-133">Se o Windows Media Player não aparecer na lista, clique em **procurar** e abra Wmp.dll, que deve estar na pasta system32 do Windows \\ .</span><span class="sxs-lookup"><span data-stu-id="bb1bb-133">If Windows Media Player does not appear in the list, click **Browse**, and then open Wmp.dll, which should be in the Windows\\System32 folder.</span></span>

3.  <span data-ttu-id="bb1bb-134">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="bb1bb-134">Click **OK**.</span></span> <span data-ttu-id="bb1bb-135">O controle do Windows Media Player será colocado na guia atual da caixa de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="bb1bb-135">The Windows Media Player control will be placed on the current Toolbox tab.</span></span>

<span data-ttu-id="bb1bb-136">Agora você pode selecionar o Windows Media Player na caixa de ferramentas e adicioná-lo a um formulário.</span><span class="sxs-lookup"><span data-stu-id="bb1bb-136">You can now select Windows Media Player in the Toolbox and add it to a form.</span></span>

<span data-ttu-id="bb1bb-137">O Visual Studio dá ao controle do Windows Media Player um nome padrão, como "axWindowsMediaPlayer1".</span><span class="sxs-lookup"><span data-stu-id="bb1bb-137">Visual Studio gives the Windows Media Player control a default name such as "axWindowsMediaPlayer1".</span></span> <span data-ttu-id="bb1bb-138">Talvez você queira alterar o nome para algo mais facilmente lembrado, como "Player".</span><span class="sxs-lookup"><span data-stu-id="bb1bb-138">You may want to change the name to something more easily remembered, such as "Player".</span></span>

<span data-ttu-id="bb1bb-139">Adicionar o controle do Windows Media Player da caixa de ferramentas também adiciona referências a duas bibliotecas criadas pelo Visual Studio, AxWMPLib e WMPLib.</span><span class="sxs-lookup"><span data-stu-id="bb1bb-139">Adding the Windows Media Player control from the Toolbox also adds references to two libraries created by Visual Studio, AxWMPLib and WMPLib.</span></span> <span data-ttu-id="bb1bb-140">Você pode encontrá-los na Gerenciador de Soluções em **referências**.</span><span class="sxs-lookup"><span data-stu-id="bb1bb-140">You can find them in the Solution Explorer under **References**.</span></span>

<span data-ttu-id="bb1bb-141">Para facilitar o uso dos objetos no namespace do Player, você deve incluir o namespace nas diretivas using ou Imports de seus arquivos, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="bb1bb-141">To make using the objects in the Player namespace easier, you should include the namespace in the using or imports directives of your files, as follows:</span></span>


```Csharp
using WMPLib;
```




```VB
imports WMPLib

```



<span data-ttu-id="bb1bb-142">A diretiva garante que você possa consultar objetos do **Player** sem qualificar totalmente seus nomes.</span><span class="sxs-lookup"><span data-stu-id="bb1bb-142">The directive ensures that you can refer to **Player** objects without fully qualifying their names.</span></span>

> [!Note]  
> <span data-ttu-id="bb1bb-143">O controle do Windows Media Player é um objeto **AxWindowsMediaPlayer** do namespace **AxWMPLib** .</span><span class="sxs-lookup"><span data-stu-id="bb1bb-143">The Windows Media Player control is an **AxWindowsMediaPlayer** object from the **AxWMPLib** namespace.</span></span> <span data-ttu-id="bb1bb-144">No entanto, a classe **AxWindowsMediaPlayer** usa tipos de dados, interfaces e outros elementos do namespace **WMPLib** .</span><span class="sxs-lookup"><span data-stu-id="bb1bb-144">However, the **AxWindowsMediaPlayer** class uses data types, interfaces, and other elements from the **WMPLib** namespace.</span></span>

 

## <a name="configuring-visibility-of-the-control"></a><span data-ttu-id="bb1bb-145">Configurando a visibilidade do controle</span><span class="sxs-lookup"><span data-stu-id="bb1bb-145">Configuring Visibility of the Control</span></span>

<span data-ttu-id="bb1bb-146">Quando você adiciona o controle do Windows Media Player pela primeira vez a um formulário, ele ficará visível.</span><span class="sxs-lookup"><span data-stu-id="bb1bb-146">When you first add the Windows Media Player control to a form, it will be visible.</span></span> <span data-ttu-id="bb1bb-147">Se você não quiser usar a imagem visível do Player em seu aplicativo, oculte o player padrão definindo qualquer uma das seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="bb1bb-147">If you do not want to use the visible image of the Player in your application, hide the default Player by setting any one of the following properties:</span></span>



| <span data-ttu-id="bb1bb-148">Propriedade</span><span class="sxs-lookup"><span data-stu-id="bb1bb-148">Property</span></span>        | <span data-ttu-id="bb1bb-149">Valor</span><span class="sxs-lookup"><span data-stu-id="bb1bb-149">Value</span></span>                                                 |
|-----------------|-------------------------------------------------------|
| <span data-ttu-id="bb1bb-150">**uiMode**</span><span class="sxs-lookup"><span data-stu-id="bb1bb-150">**uiMode**</span></span>      | <span data-ttu-id="bb1bb-151">"invisível" (consulte [Player. UIMODE](player-uimode.md).)</span><span class="sxs-lookup"><span data-stu-id="bb1bb-151">"invisible" (See [Player.uiMode](player-uimode.md).)</span></span> |
| <span data-ttu-id="bb1bb-152">**Visível**</span><span class="sxs-lookup"><span data-stu-id="bb1bb-152">**Visible**</span></span>     | <span data-ttu-id="bb1bb-153">"false"</span><span class="sxs-lookup"><span data-stu-id="bb1bb-153">"false"</span></span>                                               |
| <span data-ttu-id="bb1bb-154">**Tamanho. largura**</span><span class="sxs-lookup"><span data-stu-id="bb1bb-154">**Size.Width**</span></span>  | <span data-ttu-id="bb1bb-155">0</span><span class="sxs-lookup"><span data-stu-id="bb1bb-155">0</span></span>                                                     |
| <span data-ttu-id="bb1bb-156">**Tamanho. altura**</span><span class="sxs-lookup"><span data-stu-id="bb1bb-156">**Size.Height**</span></span> | <span data-ttu-id="bb1bb-157">0</span><span class="sxs-lookup"><span data-stu-id="bb1bb-157">0</span></span>                                                     |



 

<span data-ttu-id="bb1bb-158">Você pode definir essas propriedades no código ou na janela **Propriedades** quando o controle do Windows Media Player é selecionado no designer de formulário.</span><span class="sxs-lookup"><span data-stu-id="bb1bb-158">You can set these properties either in code or in the **Properties** window when the Windows Media Player control is selected in the form designer.</span></span>

## <a name="object-model-compatibility-of-the-control"></a><span data-ttu-id="bb1bb-159">Compatibilidade do modelo de objeto do controle</span><span class="sxs-lookup"><span data-stu-id="bb1bb-159">Object Model Compatibility of the Control</span></span>

<span data-ttu-id="bb1bb-160">O modelo de objeto para o controle do Windows Media Player é basicamente o mesmo na .NET Framework como em código e script não gerenciados.</span><span class="sxs-lookup"><span data-stu-id="bb1bb-160">The object model for the Windows Media Player control is basically the same in the .NET Framework as in unmanaged code and script.</span></span> <span data-ttu-id="bb1bb-161">No entanto, há diferenças em como os elementos são expostos:</span><span class="sxs-lookup"><span data-stu-id="bb1bb-161">However, there are differences in how elements are exposed:</span></span>

-   <span data-ttu-id="bb1bb-162">A maioria dos objetos é exposta sob o nome da interface COM subjacente.</span><span class="sxs-lookup"><span data-stu-id="bb1bb-162">Most objects are exposed under the name of their underlying COM interface.</span></span> <span data-ttu-id="bb1bb-163">Por exemplo, o objeto **playlist** é exposto como **IWMPPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="bb1bb-163">For example, the **Playlist** object is exposed as **IWMPPlaylist**.</span></span>
-   <span data-ttu-id="bb1bb-164">Algumas interfaces têm versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="bb1bb-164">Some interfaces have later versions.</span></span> <span data-ttu-id="bb1bb-165">Por exemplo, **IWMPMedia** recebeu funcionalidade adicional em **IWMPMedia2** e **IWMPMedia3**.</span><span class="sxs-lookup"><span data-stu-id="bb1bb-165">For example, **IWMPMedia** was given additional functionality in **IWMPMedia2** and **IWMPMedia3**.</span></span> <span data-ttu-id="bb1bb-166">Se você declarar um objeto como **IWMPMedia**, normalmente terá acesso à funcionalidade de todas as versões da interface.</span><span class="sxs-lookup"><span data-stu-id="bb1bb-166">If you declare an object as **IWMPMedia**, you usually have access to the functionality of all versions of the interface.</span></span> <span data-ttu-id="bb1bb-167">No entanto, o IntelliSense® não reconhecerá os métodos ou as propriedades das interfaces de versão posteriores, e o Editor Visual Basic .NET não corrigirá automaticamente a capitalização.</span><span class="sxs-lookup"><span data-stu-id="bb1bb-167">However, IntelliSense® will not recognize the methods or properties of the later-version interfaces, and the Visual Basic .NET editor will not automatically correct capitalization.</span></span> <span data-ttu-id="bb1bb-168">Para obter o benefício completo do IntelliSense e de outros recursos do Visual Studio, declare o objeto usando a versão mais recente da interface, como **IWMPMedia3**.</span><span class="sxs-lookup"><span data-stu-id="bb1bb-168">To get the full benefit of IntelliSense and other features of Visual Studio, declare the object by using the latest version of the interface, such as **IWMPMedia3**.</span></span>
-   <span data-ttu-id="bb1bb-169">Não há propriedades indexadas (C#) ou propriedades padrão (Visual Basic .NET).</span><span class="sxs-lookup"><span data-stu-id="bb1bb-169">There are no indexed properties (C#) or default properties (Visual Basic .NET).</span></span> <span data-ttu-id="bb1bb-170">Por exemplo, para recuperar um **playlist. Item**, você deve chamar o método acessador **IWMPlaylist. get \_ Item** em C# ou recuperar a propriedade **IWMPlayist. Item** no Visual Basic .net.</span><span class="sxs-lookup"><span data-stu-id="bb1bb-170">For example, to retrieve a **Playlist.item**, you must call the **IWMPlaylist.get\_Item** accessor method in C# or retrieve the **IWMPlayist.Item** property in Visual Basic .NET.</span></span>
-   <span data-ttu-id="bb1bb-171">Devido a um conflito de nomenclatura entre a propriedade de **controles** do Windows Media Player e a propriedade **Controls** exposta por cada controle, a versão do Player dessa propriedade é chamada de **CtlControls** no contexto do controle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="bb1bb-171">Because of a naming conflict between the Windows Media Player **Controls** property and the **Controls** property exposed by every control, the Player version of this property is called **CtlControls** in the context of the ActiveX control.</span></span> <span data-ttu-id="bb1bb-172">(No entanto, esse não é o caso quando você cria o Player programaticamente, em vez de um controle ActiveX.)</span><span class="sxs-lookup"><span data-stu-id="bb1bb-172">(However, this is not the case when you create the Player programmatically rather than as an ActiveX control.)</span></span>

<span data-ttu-id="bb1bb-173">Use o pesquisador de objetos no Visual Studio para localizar os nomes de API corretos para métodos e objetos nos namespaces **AxWMPLib** e **WMPLib** .</span><span class="sxs-lookup"><span data-stu-id="bb1bb-173">Use the Object Browser in Visual Studio to locate the correct API names for methods and objects in the **AxWMPLib** and **WMPLib** namespaces.</span></span>

## <a name="distributing-your-application"></a><span data-ttu-id="bb1bb-174">Distribuindo o aplicativo</span><span class="sxs-lookup"><span data-stu-id="bb1bb-174">Distributing Your Application</span></span>

<span data-ttu-id="bb1bb-175">Ao distribuir seu aplicativo, certifique-se de instalar AxInterop.WMPLib.dll e Interop.WMPLib.dll na pasta do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bb1bb-175">When you distribute your application, be sure to install AxInterop.WMPLib.dll and Interop.WMPLib.dll in the application folder.</span></span> <span data-ttu-id="bb1bb-176">Você também precisará certificar-se de que a versão necessária do Windows Media Player esteja instalada no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="bb1bb-176">You will also need to make sure that the required Windows Media Player version is installed on the user's computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb1bb-177">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bb1bb-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb1bb-178">**Criando o controle do Windows Media Player programaticamente**</span><span class="sxs-lookup"><span data-stu-id="bb1bb-178">**Creating the Windows Media Player Control Programmatically**</span></span>](creating-the-windows-media-player-control-programmatically.md)
</dt> <dt>

[<span data-ttu-id="bb1bb-179">**Inserindo o controle do Windows Media Player em uma solução C#**</span><span class="sxs-lookup"><span data-stu-id="bb1bb-179">**Embedding the Windows Media Player Control in a C# Solution**</span></span>](embedding-the-windows-media-player-control-in-a-c--solution.md)
</dt> <dt>

[<span data-ttu-id="bb1bb-180">**Inserindo o controle do Windows Media Player em uma solução Visual Basic .NET**</span><span class="sxs-lookup"><span data-stu-id="bb1bb-180">**Embedding the Windows Media Player Control in a Visual Basic .NET Solution**</span></span>](embedding-the-windows-media-player-control-in-a-visual-basic--net-solution.md)
</dt> </dl>

 

 




