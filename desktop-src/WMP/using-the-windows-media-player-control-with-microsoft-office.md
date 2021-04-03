---
title: Usando o controle do Windows Media Player com Microsoft Office
description: Usando o controle do Windows Media Player com Microsoft Office
ms.assetid: bc7b2623-8e6d-4af6-b4d0-8087c0159273
keywords:
- Windows Media Player, incorporando controle ActiveX
- Modelo de objeto do Windows Media Player, inserindo controle ActiveX
- modelo de objeto, inserindo controle ActiveX
- Windows Media Player Mobile, inserindo controle ActiveX
- Controle ActiveX do Windows Media Player, incorporando
- Controle ActiveX móvel do Windows Media Player, incorporando
- Controle ActiveX, incorporando
- Windows Media Player, Office
- Modelo de objeto do Windows Media Player, Office
- modelo de objeto, Office
- Windows Media Player Mobile, Office
- Controle ActiveX do Windows Media Player, Office
- Controle ActiveX móvel do Windows Media Player, Office
- Controle ActiveX, Office
- Inserção de documentos do Office
- inserindo, documentos do Office
- Controle ActiveX do Windows Media Player, Excel
- Controle ActiveX móvel do Windows Media Player, Excel
- Controle ActiveX, Excel
- incorporação, planilhas do Excel
- Inserção de planilha do Excel
- Controle ActiveX do Windows Media Player, PowerPoint
- Controle ActiveX móvel do Windows Media Player, PowerPoint
- Controle ActiveX, PowerPoint
- inserindo, apresentações de slides do PowerPoint
- Inserção de apresentação de slides do PowerPoint
- Controle ActiveX do Windows Media Player, Word
- Controle ActiveX móvel do Windows Media Player, Word
- Controle ActiveX, Word
- Inserção de documento do Word
- inserindo, documentos do Word
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2504b46b4fb409dede108c41b43014c3aaeae5ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916332"
---
# <a name="using-the-windows-media-player-control-with-microsoft-office"></a><span data-ttu-id="87336-134">Usando o controle do Windows Media Player com Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="87336-134">Using the Windows Media Player Control with Microsoft Office</span></span>

<span data-ttu-id="87336-135">Esta seção descreve como inserir o controle ActiveX do Windows Media Player 9 Series ou posterior em vários documentos criados usando o Microsoft Office XP.</span><span class="sxs-lookup"><span data-stu-id="87336-135">This section describes how to embed the Windows Media Player 9 Series or later ActiveX control in various documents created using Microsoft Office XP.</span></span>

<span data-ttu-id="87336-136">No Microsoft Word, Excel e PowerPoint®, você insere o controle selecionando **objeto** no menu **Inserir** e, em seguida, escolhendo **Windows Media Player** na lista de tipos de objetos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="87336-136">In Microsoft Word, Excel, and PowerPoint®, you embed the control by selecting **Object** from the **Insert** menu, then choosing **Windows Media Player** from the list of available object types.</span></span> <span data-ttu-id="87336-137">O controle do Windows Media Player aparece no documento no local atual.</span><span class="sxs-lookup"><span data-stu-id="87336-137">The Windows Media Player control appears in the document at the current location.</span></span> <span data-ttu-id="87336-138">Você pode selecionar **Formatar controle** ( **Formatar objeto** no Excel) no menu de atalho do controle para ajustar o layout, o estilo de disposição do texto e outras opções de formato.</span><span class="sxs-lookup"><span data-stu-id="87336-138">You can then select **Format Control** ( **Format Object** in Excel) from the shortcut menu for the control to adjust the layout, text wrapping style, and other format options.</span></span> <span data-ttu-id="87336-139">No Word e no Excel, você deve estar no modo de design para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="87336-139">In Word and Excel, you must be in design mode to do this.</span></span>

<span data-ttu-id="87336-140">Depois de posicionar e formatar o controle, você poderá configurá-lo usando a caixa de diálogo de **Propriedades** , que pode ser acessada na **Toolbox Control** ou no menu de atalho no modo de design para Word e Excel.</span><span class="sxs-lookup"><span data-stu-id="87336-140">Once you have positioned and formatted the control, you can configure it using the **Properties** dialog box, which is accessible from the **Control Toolbox** or from the shortcut menu in design mode for Word and Excel.</span></span> <span data-ttu-id="87336-141">Aqui você pode especificar as propriedades básicas de controle do Player, como o nome do controle, a URL de um arquivo de mídia digital e o modo de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="87336-141">Here you can specify basic Player control properties such as the control name, the URL of a digital media file, and the user interface mode.</span></span> <span data-ttu-id="87336-142">A definição da propriedade **UIMODE** como "None" oculta tudo no controle, exceto a janela de vídeo ou visualização, permitindo que você adicione seus próprios botões e escreva o código de script usando Visual Basic for Applications (VBA) para manipular os cliques de botão e os eventos de controle do jogador.</span><span class="sxs-lookup"><span data-stu-id="87336-142">Setting the **uiMode** property to "none" hides everything in the control except the video or visualization window, allowing you to add your own buttons and write script code using Visual Basic for Applications (VBA) to handle the button clicks and Player control events.</span></span>

<span data-ttu-id="87336-143">Na caixa de diálogo **Propriedades** básicas, você também pode acessar a caixa de diálogo Propriedades de controle mais sofisticadas do **Windows Media Player** clicando duas vezes na linha "(personalizado)" ou clicando no botão de reticências ("...") depois de selecionar essa linha.</span><span class="sxs-lookup"><span data-stu-id="87336-143">From the basic **Properties** dialog box, you can also access the more sophisticated **Windows Media Player Control Properties** dialog box by double-clicking the "(Custom)" row or by clicking the ellipsis ("...") button after selecting that row.</span></span> <span data-ttu-id="87336-144">Nessa caixa de diálogo, você pode modificar todas as propriedades de controle do Player disponíveis.</span><span class="sxs-lookup"><span data-stu-id="87336-144">From this dialog box, you can modify all available Player control properties.</span></span>

> [!Note]  
> <span data-ttu-id="87336-145">Você deve ter cuidado para não tomar ações em manipuladores de eventos de controle do Player que resultarão no controle que está sendo destruído.</span><span class="sxs-lookup"><span data-stu-id="87336-145">You must be careful not to take actions in Player control event handlers that will result in the control being destroyed.</span></span> <span data-ttu-id="87336-146">Por exemplo, se você inserir o controle do Windows Media Player em um slide em uma apresentação do PowerPoint, não chame o **próximo** método do PowerPoint do evento **openStateChange** do Player ou de qualquer outro evento.</span><span class="sxs-lookup"><span data-stu-id="87336-146">For example, if you embed the Windows Media Player control on a slide in a PowerPoint presentation, do not call the PowerPoint **Next** method from the Player **openStateChange** event or any other event.</span></span>

 

> [!Note]  
> <span data-ttu-id="87336-147">Além disso, você não deve definir a propriedade **Player. URL** de um manipulador de eventos de controle de jogador.</span><span class="sxs-lookup"><span data-stu-id="87336-147">In addition, you should not set the **Player.URL** property from a Player control event handler.</span></span>

 

<span data-ttu-id="87336-148">No FrontPage, adicione o controle do Windows Media Player a uma página da Web selecionando **componente da Internet** no menu **Inserir** .</span><span class="sxs-lookup"><span data-stu-id="87336-148">In FrontPage, add the Windows Media Player control to a webpage by selecting **Web Component** from the **Insert** menu.</span></span> <span data-ttu-id="87336-149">Na caixa de diálogo **Inserir componente da Web** , selecione **controles avançados** na lista **tipo de componente** e, em seguida, selecione **controle ActiveX** na lista de opções de controle.</span><span class="sxs-lookup"><span data-stu-id="87336-149">In the **Insert Web Component** dialog box, select **Advanced Controls** from the **Component type** list, then select **ActiveX Control** from the list of control choices.</span></span> <span data-ttu-id="87336-150">Na próxima janela da caixa de diálogo, selecione **Windows Media Player**.</span><span class="sxs-lookup"><span data-stu-id="87336-150">In the next window of the dialog box, select **Windows Media Player**.</span></span> <span data-ttu-id="87336-151">Se não estiver listado, clique em **Personalizar** e marque a caixa de seleção **Windows Media Player** na lista **controle** .</span><span class="sxs-lookup"><span data-stu-id="87336-151">If it is not listed, click **Customize** and select the **Windows Media Player** check box in the **Control** list.</span></span>

<span data-ttu-id="87336-152">Depois que o controle do Windows Media Player é inserido, você pode posicioná-lo e redimensioná-lo e modificar suas propriedades selecionando **Propriedades do controle ActiveX** no menu de atalho do controle.</span><span class="sxs-lookup"><span data-stu-id="87336-152">After the Windows Media Player control is embedded, you can position and resize it, and modify its properties by selecting **ActiveX Control Properties** from the shortcut menu for the control.</span></span> <span data-ttu-id="87336-153">Na exibição HTML, os valores de propriedade que você especifica aparecem no elemento OBJECT que representa o controle do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="87336-153">In the HTML view, the property values that you specify appear in the OBJECT element representing the Windows Media Player control.</span></span> <span data-ttu-id="87336-154">O nome do objeto aparece como o atributo de ID e as propriedades de controle aparecem como marcas PARAM.</span><span class="sxs-lookup"><span data-stu-id="87336-154">The object name appears as the ID attribute, and the control properties appear as PARAM tags.</span></span> <span data-ttu-id="87336-155">O nome do objeto fornece acesso ao modelo de objeto de controle do Windows Media Player, que você pode programar usando o Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="87336-155">The object name gives you access to the Windows Media Player control object model, which you can program using Microsoft JScript.</span></span> <span data-ttu-id="87336-156">Para obter mais informações, consulte [usando o controle do Windows Media Player em uma página da Web](using-the-windows-media-player-control-in-a-web-page.md).</span><span class="sxs-lookup"><span data-stu-id="87336-156">For more information, see [Using the Windows Media Player Control in a Web Page](using-the-windows-media-player-control-in-a-web-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="87336-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87336-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87336-158">**Guia de controle do Player**</span><span class="sxs-lookup"><span data-stu-id="87336-158">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




