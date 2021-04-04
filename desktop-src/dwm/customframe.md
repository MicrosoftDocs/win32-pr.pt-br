---
title: Quadro de janela personalizado usando DWM
description: Este tópico demonstra como usar as APIs de Gerenciador de Janelas da Área de Trabalho (DWM) para criar quadros de janela personalizados para seu aplicativo.
ms.assetid: 7f7dc902-40d3-44e9-adc2-05a39c634eb3
keywords:
- Gerenciador de Janelas da Área de Trabalho (DWM), quadros de janela personalizados
- DWM (Gerenciador de Janelas da Área de Trabalho), quadros de janela personalizados
- quadros de janela personalizados
- removendo quadros padrão
- estendendo quadros de cliente
- Gerenciador de Janelas da Área de Trabalho (DWM), estendendo quadros de cliente
- DWM (Gerenciador de Janelas da Área de Trabalho), estendendo quadros de cliente
- Gerenciador de Janelas da Área de Trabalho (DWM), removendo quadros padrão
- DWM (Gerenciador de Janelas da Área de Trabalho), removendo quadros padrão
- Gerenciador de Janelas da Área de Trabalho (DWM), desenho em quadros estendidos
- DWM (Gerenciador de Janelas da Área de Trabalho), desenho em quadros estendidos
- desenho em quadros estendidos
- testes de clique
- Gerenciador de Janelas da Área de Trabalho (DWM), teste de clique
- DWM (Gerenciador de Janelas da Área de Trabalho), teste de clique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a27a9b71dd2dd91cb000a352ef039de2a71cd9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008333"
---
# <a name="custom-window-frame-using-dwm"></a><span data-ttu-id="8bac2-118">Quadro de janela personalizado usando DWM</span><span class="sxs-lookup"><span data-stu-id="8bac2-118">Custom Window Frame Using DWM</span></span>

<span data-ttu-id="8bac2-119">Este tópico demonstra como usar as APIs de Gerenciador de Janelas da Área de Trabalho (DWM) para criar quadros de janela personalizados para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8bac2-119">This topic demonstrates how to use the Desktop Window Manager (DWM) APIs to create custom window frames for your application.</span></span>

-   [<span data-ttu-id="8bac2-120">Introdução</span><span class="sxs-lookup"><span data-stu-id="8bac2-120">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="8bac2-121">Estendendo o quadro do cliente</span><span class="sxs-lookup"><span data-stu-id="8bac2-121">Extending the Client Frame</span></span>](#extending-the-client-frame)
-   [<span data-ttu-id="8bac2-122">Removendo o quadro padrão</span><span class="sxs-lookup"><span data-stu-id="8bac2-122">Removing the Standard Frame</span></span>](#removing-the-standard-frame)
-   [<span data-ttu-id="8bac2-123">Desenho na janela do quadro estendido</span><span class="sxs-lookup"><span data-stu-id="8bac2-123">Drawing in the Extended Frame Window</span></span>](#drawing-in-the-extended-frame-window)
-   [<span data-ttu-id="8bac2-124">Habilitando o teste de clique para o quadro personalizado</span><span class="sxs-lookup"><span data-stu-id="8bac2-124">Enabling Hit Testing for the Custom Frame</span></span>](#enabling-hit-testing-for-the-custom-frame)
-   [<span data-ttu-id="8bac2-125">Apêndice A: procedimento de janela de exemplo</span><span class="sxs-lookup"><span data-stu-id="8bac2-125">Appendix A: Sample Window Procedure</span></span>](#appendix-a-sample-window-procedure)
-   [<span data-ttu-id="8bac2-126">Apêndice B: pintando o título da legenda</span><span class="sxs-lookup"><span data-stu-id="8bac2-126">Appendix B: Painting the Caption Title</span></span>](#appendix-b-painting-the-caption-title)
-   [<span data-ttu-id="8bac2-127">Apêndice C: função HitTestNCA</span><span class="sxs-lookup"><span data-stu-id="8bac2-127">Appendix C: HitTestNCA Function</span></span>](#appendix-c-hittestnca-function)
-   [<span data-ttu-id="8bac2-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8bac2-128">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="8bac2-129">Introdução</span><span class="sxs-lookup"><span data-stu-id="8bac2-129">Introduction</span></span>

<span data-ttu-id="8bac2-130">No Windows Vista e posterior, a aparência das áreas que não são de cliente das janelas de aplicativos (a barra de título, o ícone, a borda da janela e os botões de legenda) é controlada pelo DWM.</span><span class="sxs-lookup"><span data-stu-id="8bac2-130">In Windows Vista and later, the appearance of the non-client areas of application windows (the title bar, icon, window border, and caption buttons) is controlled by the DWM.</span></span> <span data-ttu-id="8bac2-131">Usando as APIs DWM, você pode alterar a maneira como o DWM renderiza o quadro de uma janela.</span><span class="sxs-lookup"><span data-stu-id="8bac2-131">Using the DWM APIs, you can change the way the DWM renders a window's frame.</span></span>

<span data-ttu-id="8bac2-132">Um recurso das APIs do DWM é a capacidade de estender o quadro do aplicativo para a área do cliente.</span><span class="sxs-lookup"><span data-stu-id="8bac2-132">One feature of the DWM APIs is the ability to extend the application frame into the client area.</span></span> <span data-ttu-id="8bac2-133">Isso permite que você integre um elemento de interface do usuário do cliente — como uma barra de ferramentas — ao quadro, dando à interface do usuário um lugar mais proeminente na interface do usuário do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8bac2-133">This enables you to integrate a client UI element—such as a toolbar—into the frame, giving the UI controls a more prominent place in the application UI.</span></span> <span data-ttu-id="8bac2-134">Por exemplo, o Windows Internet Explorer 7 no Windows Vista integra a barra de navegação no quadro da janela, estendendo a parte superior do quadro, conforme mostrado na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8bac2-134">For example, Windows Internet Explorer 7 on Windows Vista integrates the navigation bar into the window frame by extending the top of the frame as shown in the following screen shot.</span></span>

![barra de navegação integrada ao quadro da janela.](images/ie7-extendedborder-boxed.png)

<span data-ttu-id="8bac2-136">A capacidade de estender o quadro da janela também permite que você crie quadros personalizados mantendo a aparência da janela.</span><span class="sxs-lookup"><span data-stu-id="8bac2-136">The ability to extend the window frame also enables you to create custom frames while maintaining the window's look and feel.</span></span> <span data-ttu-id="8bac2-137">Por exemplo, Microsoft Office o Word 2007 desenha o botão do Office e a barra de ferramentas de acesso rápido dentro do quadro personalizado, fornecendo os botões de legenda padrão de minimizar, maximizar e fechar, conforme mostrado na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8bac2-137">For example, Microsoft Office Word 2007 draws the Office button and the Quick Access toolbar inside the custom frame while providing the standard Minimize, Maximize, and Close caption buttons, as shown in the following screen shot.</span></span>

![botão do Office e barra de ferramentas de acesso rápido no Word 2007](images/word2007-customborder-boxed.png)

## <a name="extending-the-client-frame"></a><span data-ttu-id="8bac2-139">Estendendo o quadro do cliente</span><span class="sxs-lookup"><span data-stu-id="8bac2-139">Extending the Client Frame</span></span>

<span data-ttu-id="8bac2-140">A funcionalidade para estender o quadro para a área do cliente é exposta pela função [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) .</span><span class="sxs-lookup"><span data-stu-id="8bac2-140">The functionality to extend the frame into the client area is exposed by the [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) function.</span></span> <span data-ttu-id="8bac2-141">Para estender o quadro, passe o identificador da janela de destino junto com os valores de margem inserida para **DwmExtendFrameIntoClientArea**.</span><span class="sxs-lookup"><span data-stu-id="8bac2-141">To extend the frame, pass the handle of the target window together with the margin inset values to **DwmExtendFrameIntoClientArea**.</span></span> <span data-ttu-id="8bac2-142">Os valores de margem interna determinam a distância para estender o quadro nos quatro lados da janela.</span><span class="sxs-lookup"><span data-stu-id="8bac2-142">The margin inset values determine how far to extend the frame on the four sides of the window.</span></span>

<span data-ttu-id="8bac2-143">O código a seguir demonstra o uso de [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) para estender o quadro.</span><span class="sxs-lookup"><span data-stu-id="8bac2-143">The following code demonstrates the use of [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) to extend the frame.</span></span>


```
// Handle the window activation.
if (message == WM_ACTIVATE)
{
    // Extend the frame into the client area.
    MARGINS margins;

    margins.cxLeftWidth = LEFTEXTENDWIDTH;      // 8
    margins.cxRightWidth = RIGHTEXTENDWIDTH;    // 8
    margins.cyBottomHeight = BOTTOMEXTENDWIDTH; // 20
    margins.cyTopHeight = TOPEXTENDWIDTH;       // 27

    hr = DwmExtendFrameIntoClientArea(hWnd, &margins);

    if (!SUCCEEDED(hr))
    {
        // Handle the error.
    }

    fCallDWP = true;
    lRet = 0;
}
```



<span data-ttu-id="8bac2-144">Observe que a extensão de quadro é feita na mensagem de [**\_ ativação do WM**](/windows/desktop/inputdev/wm-activate) em vez da mensagem de [**\_ criação do WM**](/windows/desktop/winmsg/wm-create) .</span><span class="sxs-lookup"><span data-stu-id="8bac2-144">Note that the frame extension is done within the [**WM\_ACTIVATE**](/windows/desktop/inputdev/wm-activate) message rather than the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message.</span></span> <span data-ttu-id="8bac2-145">Isso garante que a extensão de quadro seja manipulada corretamente quando a janela estiver em seu tamanho padrão e quando for maximizada.</span><span class="sxs-lookup"><span data-stu-id="8bac2-145">This ensures that frame extension is handled properly when the window is at its default size and when it is maximized.</span></span>

<span data-ttu-id="8bac2-146">A imagem a seguir mostra um quadro de janela padrão (à esquerda) e o mesmo quadro de janela estendido (à direita).</span><span class="sxs-lookup"><span data-stu-id="8bac2-146">The following image shows a standard window frame (on the left) and the same window frame extended (on the right).</span></span> <span data-ttu-id="8bac2-147">O quadro é estendido usando o exemplo de código anterior e a tela de fundo padrão Microsoft Visual Studio [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) / [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) (janela de cores \_ + 1).</span><span class="sxs-lookup"><span data-stu-id="8bac2-147">The frame is extended using the previous code example and the default Microsoft Visual Studio [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)/[**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) background (COLOR\_WINDOW +1).</span></span>

![captura de tela de um padrão (à esquerda) e quadro estendido (à direita) com plano de fundo branco](images/white-sidebyside.png)

<span data-ttu-id="8bac2-149">A diferença visual entre essas duas janelas é muito sutil.</span><span class="sxs-lookup"><span data-stu-id="8bac2-149">The visual difference between these two windows is very subtle.</span></span> <span data-ttu-id="8bac2-150">A única diferença entre os dois é que a borda da linha preta fina da região do cliente na janela à esquerda está ausente na janela à direita.</span><span class="sxs-lookup"><span data-stu-id="8bac2-150">The only difference between the two is that the thin black line border of the client region in the window on the left is missing from the window on the right.</span></span> <span data-ttu-id="8bac2-151">O motivo para essa falta de borda é que ela é incorporada ao quadro estendido, mas o restante da área do cliente não é.</span><span class="sxs-lookup"><span data-stu-id="8bac2-151">The reason for this missing border is that it is incorporated into the extended frame, but the rest of the client area is not.</span></span> <span data-ttu-id="8bac2-152">Para que os quadros estendidos fiquem visíveis, as regiões subjacentes a cada um dos lados do quadro estendido devem ter dados de pixel com um valor alfa de 0.</span><span class="sxs-lookup"><span data-stu-id="8bac2-152">For the extended frames to be visible, the regions underlying each of the extended frame's sides must have pixel data with an alpha value of 0.</span></span> <span data-ttu-id="8bac2-153">A borda preta em torno da região do cliente tem dados de pixel em que todos os valores de cor (vermelho, verde, azul e alfa) são definidos como 0.</span><span class="sxs-lookup"><span data-stu-id="8bac2-153">The black border around the client region has pixel data in which all color values (red, green, blue, and alpha) are set to 0.</span></span> <span data-ttu-id="8bac2-154">O restante do plano de fundo não tem o valor alfa definido como 0, portanto, o restante do quadro estendido não está visível.</span><span class="sxs-lookup"><span data-stu-id="8bac2-154">The rest of the background does not have the alpha value set to 0, so the rest of the extended frame is not visible.</span></span>

<span data-ttu-id="8bac2-155">A maneira mais fácil de garantir que os quadros estendidos fiquem visíveis é pintar toda a região do cliente em preto.</span><span class="sxs-lookup"><span data-stu-id="8bac2-155">The easiest way to ensure that the extended frames are visible is to paint the entire client region black.</span></span> <span data-ttu-id="8bac2-156">Para fazer isso, inicialize o membro *hbrBackground* da sua estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) ou [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) para o identificador do pincel preto de estoque \_ .</span><span class="sxs-lookup"><span data-stu-id="8bac2-156">To accomplish this, initialize the *hbrBackground* member of your [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) or [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) structure to the handle of the stock BLACK\_BRUSH.</span></span> <span data-ttu-id="8bac2-157">A imagem a seguir mostra o mesmo quadro padrão (à esquerda) e o quadro estendido (à direita) mostrado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="8bac2-157">The following image shows the same standard frame (left) and extended frame (right) shown previously.</span></span> <span data-ttu-id="8bac2-158">Dessa vez, no entanto, *hbrBackground* é definido como o \_ identificador de pincel preto obtido da função [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) .</span><span class="sxs-lookup"><span data-stu-id="8bac2-158">This time, however, *hbrBackground* is set to the BLACK\_BRUSH handle obtained from the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) function.</span></span>

![captura de tela de um padrão (à esquerda) e quadro estendido (à direita) com plano de fundo preto](images/standard-extended-sidebyside.png)

## <a name="removing-the-standard-frame"></a><span data-ttu-id="8bac2-160">Removendo o quadro padrão</span><span class="sxs-lookup"><span data-stu-id="8bac2-160">Removing the Standard Frame</span></span>

<span data-ttu-id="8bac2-161">Depois de estender o quadro do aplicativo e tornar-o visível, você pode remover o quadro padrão.</span><span class="sxs-lookup"><span data-stu-id="8bac2-161">After you have extended the frame of your application and made it visible, you can remove the standard frame.</span></span> <span data-ttu-id="8bac2-162">A remoção do quadro padrão permite que você controle a largura de cada lado do quadro em vez de simplesmente estender o quadro padrão.</span><span class="sxs-lookup"><span data-stu-id="8bac2-162">Removing the standard frame enables you to control the width of each side of the frame rather than simply extending the standard frame.</span></span>

<span data-ttu-id="8bac2-163">Para remover o quadro de janela padrão, você deve manipular a mensagem do [**WM \_ NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) , especificamente quando seu valor *wParam* é **true** e o valor de retorno é 0.</span><span class="sxs-lookup"><span data-stu-id="8bac2-163">To remove the standard window frame, you must handle the [**WM\_NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) message, specifically when its *wParam* value is **TRUE** and the return value is 0.</span></span> <span data-ttu-id="8bac2-164">Ao fazer isso, seu aplicativo usa a região da janela inteira como a área do cliente, removendo o quadro padrão.</span><span class="sxs-lookup"><span data-stu-id="8bac2-164">By doing so, your application uses the entire window region as the client area, removing the standard frame.</span></span>

<span data-ttu-id="8bac2-165">Os resultados da manipulação da mensagem do [**WM \_ NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) não são visíveis até que a região do cliente precise ser redimensionada.</span><span class="sxs-lookup"><span data-stu-id="8bac2-165">The results of handling the [**WM\_NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) message are not visible until the client region needs to be resized.</span></span> <span data-ttu-id="8bac2-166">Até esse momento, a exibição inicial da janela é exibida com o quadro padrão e as bordas estendidas.</span><span class="sxs-lookup"><span data-stu-id="8bac2-166">Until that time, the initial view of the window appears with the standard frame and extended borders.</span></span> <span data-ttu-id="8bac2-167">Para resolver isso, você deve redimensionar a janela ou executar uma ação que inicia uma mensagem do **WM \_ NCCALCSIZE** no momento da criação da janela.</span><span class="sxs-lookup"><span data-stu-id="8bac2-167">To overcome this, you must either resize your window or perform an action that initiates a **WM\_NCCALCSIZE** message at the time of window creation.</span></span> <span data-ttu-id="8bac2-168">Isso pode ser feito usando a função [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para mover sua janela e redimensioná-la.</span><span class="sxs-lookup"><span data-stu-id="8bac2-168">This can be accomplished by using the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function to move your window and resize it.</span></span> <span data-ttu-id="8bac2-169">O código a seguir demonstra uma chamada para **SetWindowPos** que força uma mensagem **\_ NCCALCSIZE do WM** a ser enviada usando os atributos de retângulo da janela atual e o \_ sinalizador framechanged do SWP.</span><span class="sxs-lookup"><span data-stu-id="8bac2-169">The following code demonstrates a call to **SetWindowPos** that forces a **WM\_NCCALCSIZE** message to be sent using the current window rectangle attributes and the SWP\_FRAMECHANGED flag.</span></span>


```
// Handle window creation.
if (message == WM_CREATE)
{
    RECT rcClient;
    GetWindowRect(hWnd, &rcClient);

    // Inform the application of the frame change.
    SetWindowPos(hWnd, 
                 NULL, 
                 rcClient.left, rcClient.top,
                 RECTWIDTH(rcClient), RECTHEIGHT(rcClient),
                 SWP_FRAMECHANGED);

    fCallDWP = true;
    lRet = 0;
}
```



<span data-ttu-id="8bac2-170">A imagem a seguir mostra o quadro padrão (à esquerda) e o quadro recentemente estendido sem o quadro padrão (direita).</span><span class="sxs-lookup"><span data-stu-id="8bac2-170">The following image shows the standard frame (left) and the newly extended frame without the standard frame (right).</span></span>

![captura de tela de um quadro padrão (à esquerda) e quadro personalizado (à direita)](images/standard-custom-sidebyside.png)

## <a name="drawing-in-the-extended-frame-window"></a><span data-ttu-id="8bac2-172">Desenho na janela do quadro estendido</span><span class="sxs-lookup"><span data-stu-id="8bac2-172">Drawing in the Extended Frame Window</span></span>

<span data-ttu-id="8bac2-173">Ao remover o quadro padrão, você perde o desenho automático do ícone e do título do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8bac2-173">By removing the standard frame, you lose the automatic drawing of the application icon and title.</span></span> <span data-ttu-id="8bac2-174">Para adicioná-los de volta ao seu aplicativo, você mesmo deve desenhá-los.</span><span class="sxs-lookup"><span data-stu-id="8bac2-174">To add these back to your application, you must draw them yourself.</span></span> <span data-ttu-id="8bac2-175">Para fazer isso, primeiro examine a alteração que ocorreu na sua área de cliente.</span><span class="sxs-lookup"><span data-stu-id="8bac2-175">To do this, first look at the change that has occurred to your client area.</span></span>

<span data-ttu-id="8bac2-176">Com a remoção do quadro padrão, sua área de cliente agora consiste em toda a janela, incluindo o quadro estendido.</span><span class="sxs-lookup"><span data-stu-id="8bac2-176">With the removal of the standard frame, your client area now consists of the entire window, including the extended frame.</span></span> <span data-ttu-id="8bac2-177">Isso inclui a região onde os botões de legenda são desenhados.</span><span class="sxs-lookup"><span data-stu-id="8bac2-177">This includes the region where the caption buttons are drawn.</span></span> <span data-ttu-id="8bac2-178">Na seguinte comparação lado a lado, a área do cliente para o quadro padrão e o quadro estendido personalizado é realçado em vermelho.</span><span class="sxs-lookup"><span data-stu-id="8bac2-178">In the following side-by-side comparison, the client area for both the standard frame and the custom extended frame is highlighted in red.</span></span> <span data-ttu-id="8bac2-179">A área do cliente para a janela de quadro padrão (esquerda) é a região preta.</span><span class="sxs-lookup"><span data-stu-id="8bac2-179">The client area for the standard frame window (left) is the black region.</span></span> <span data-ttu-id="8bac2-180">Na janela do quadro estendido (à direita), a área do cliente é a janela inteira.</span><span class="sxs-lookup"><span data-stu-id="8bac2-180">On the extended frame window (right), the client area is the entire window.</span></span>

![captura de tela de áreas de cliente em vermelho realçadas em quadro padrão e personalizado](images/clientarea-sidebyside.png)

<span data-ttu-id="8bac2-182">Como a janela inteira é a área do cliente, você pode simplesmente desenhar o que deseja no quadro estendido.</span><span class="sxs-lookup"><span data-stu-id="8bac2-182">Because the entire window is your client area, you can simply draw what you want in the extended frame.</span></span> <span data-ttu-id="8bac2-183">Para adicionar um título ao seu aplicativo, basta desenhar o texto na região apropriada.</span><span class="sxs-lookup"><span data-stu-id="8bac2-183">To add a title to your application, just draw text in the appropriate region.</span></span> <span data-ttu-id="8bac2-184">A imagem a seguir mostra o texto com tema desenhado no quadro de legenda personalizada.</span><span class="sxs-lookup"><span data-stu-id="8bac2-184">The following image shows themed text drawn on the custom caption frame.</span></span> <span data-ttu-id="8bac2-185">O título é desenhado usando a função [**DrawThemeTextEx**](/windows/win32/api/uxtheme/nf-uxtheme-drawthemetextex) .</span><span class="sxs-lookup"><span data-stu-id="8bac2-185">The title is drawn using the [**DrawThemeTextEx**](/windows/win32/api/uxtheme/nf-uxtheme-drawthemetextex) function.</span></span> <span data-ttu-id="8bac2-186">Para exibir o código que pinta o título, consulte [o apêndice B: pintando o título da legenda](#appendix-b-painting-the-caption-title).</span><span class="sxs-lookup"><span data-stu-id="8bac2-186">To view the code that paints the title, see [Appendix B: Painting the Caption Title](#appendix-b-painting-the-caption-title).</span></span>

![captura de tela de um quadro personalizado com título](images/custom-caption-title.png)

> [!Note]  
> <span data-ttu-id="8bac2-188">Ao desenhar em seu quadro personalizado, tenha cuidado ao colocar os controles da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="8bac2-188">When drawing in your custom frame, be careful when placing UI controls.</span></span> <span data-ttu-id="8bac2-189">Como a janela inteira é sua região de cliente, você deve ajustar o posicionamento do controle de interface do usuário para cada largura de quadro se não quiser que eles apareçam no quadro estendido ou no mesmo.</span><span class="sxs-lookup"><span data-stu-id="8bac2-189">Because the entire window is your client region, you must adjust your UI control placement for each frame width if you do not want them to appear on or in the extended frame.</span></span>

 

## <a name="enabling-hit-testing-for-the-custom-frame"></a><span data-ttu-id="8bac2-190">Habilitando o teste de clique para o quadro personalizado</span><span class="sxs-lookup"><span data-stu-id="8bac2-190">Enabling Hit Testing for the Custom Frame</span></span>

<span data-ttu-id="8bac2-191">Um efeito colateral de remover o quadro padrão é a perda do comportamento padrão de redimensionamento e movimentação.</span><span class="sxs-lookup"><span data-stu-id="8bac2-191">A side effect of removing the standard frame is the loss of the default resizing and moving behavior.</span></span> <span data-ttu-id="8bac2-192">Para que seu aplicativo eMule corretamente o comportamento de janela padrão, você precisará implementar a lógica para lidar com o teste de clique de botão de legenda e o redimensionamento/movimentação de quadros.</span><span class="sxs-lookup"><span data-stu-id="8bac2-192">For your application to properly emulate standard window behavior, you will need to implement logic to handle caption button hit testing and frame resizing/moving.</span></span>

<span data-ttu-id="8bac2-193">Para teste de clique de botão de legenda, o DWM fornece a função [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) .</span><span class="sxs-lookup"><span data-stu-id="8bac2-193">For caption button hit testing, DWM provides the [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) function.</span></span> <span data-ttu-id="8bac2-194">Para testar corretamente os botões de legenda em cenários de quadro personalizados, as mensagens devem primeiro ser passadas para **DwmDefWindowProc** para manipulação.</span><span class="sxs-lookup"><span data-stu-id="8bac2-194">To properly hit test the caption buttons in custom frame scenarios, messages should first be passed to **DwmDefWindowProc** for handling.</span></span> <span data-ttu-id="8bac2-195">**DwmDefWindowProc** retornará **true** se uma mensagem for manipulada e **false** se não for.</span><span class="sxs-lookup"><span data-stu-id="8bac2-195">**DwmDefWindowProc** returns **TRUE** if a message is handled and **FALSE** if it is not.</span></span> <span data-ttu-id="8bac2-196">Se a mensagem não for tratada pelo **DwmDefWindowProc**, seu aplicativo deverá lidar com a própria mensagem ou passar a mensagem para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="8bac2-196">If the message is not handled by **DwmDefWindowProc**, your application should handle the message itself or pass the message onto [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="8bac2-197">Para redimensionamento e movimentação de quadros, seu aplicativo deve fornecer a lógica de teste de cliques e manipular mensagens de teste de clique de quadro.</span><span class="sxs-lookup"><span data-stu-id="8bac2-197">For frame resizing and moving, your application must provide the hit testing logic and handle frame hit test messages.</span></span> <span data-ttu-id="8bac2-198">As mensagens de teste de quadro de quadros são enviadas para você por meio da mensagem do [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) , mesmo que seu aplicativo crie um quadro personalizado sem o quadro padrão.</span><span class="sxs-lookup"><span data-stu-id="8bac2-198">Frame hit test messages are sent to you through the [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) message, even if your application creates a custom frame without the standard frame.</span></span> <span data-ttu-id="8bac2-199">O código a seguir demonstra como tratar a mensagem do **WM \_ NCHITTEST** quando o [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) não a trata.</span><span class="sxs-lookup"><span data-stu-id="8bac2-199">The following code demonstrates handling the **WM\_NCHITTEST** message when [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) does not handle it.</span></span> <span data-ttu-id="8bac2-200">Para ver o código da função chamada `HitTestNCA` , consulte o [Apêndice C: HitTestNCA function](#appendix-c-hittestnca-function).</span><span class="sxs-lookup"><span data-stu-id="8bac2-200">To see the code of the called `HitTestNCA` function, see [Appendix C: HitTestNCA Function](#appendix-c-hittestnca-function).</span></span>


```
// Handle hit testing in the NCA if not handled by DwmDefWindowProc.
if ((message == WM_NCHITTEST) && (lRet == 0))
{
    lRet = HitTestNCA(hWnd, wParam, lParam);

    if (lRet != HTNOWHERE)
    {
        fCallDWP = false;
    }
}
```



## <a name="appendix-a-sample-window-procedure"></a><span data-ttu-id="8bac2-201">Apêndice A: procedimento de janela de exemplo</span><span class="sxs-lookup"><span data-stu-id="8bac2-201">Appendix A: Sample Window Procedure</span></span>

<span data-ttu-id="8bac2-202">O exemplo de código a seguir demonstra um procedimento de janela e suas funções de trabalho de suporte usadas para criar um aplicativo de quadro personalizado.</span><span class="sxs-lookup"><span data-stu-id="8bac2-202">The following code sample demonstrates a window procedure and its supporting worker functions used to create a custom frame application.</span></span>


```
//
//  Main WinProc.
//
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    bool fCallDWP = true;
    BOOL fDwmEnabled = FALSE;
    LRESULT lRet = 0;
    HRESULT hr = S_OK;

    // Winproc worker for custom frame issues.
    hr = DwmIsCompositionEnabled(&fDwmEnabled);
    if (SUCCEEDED(hr))
    {
        lRet = CustomCaptionProc(hWnd, message, wParam, lParam, &fCallDWP);
    }

    // Winproc worker for the rest of the application.
    if (fCallDWP)
    {
        lRet = AppWinProc(hWnd, message, wParam, lParam);
    }
    return lRet;
}

//
// Message handler for handling the custom caption messages.
//
LRESULT CustomCaptionProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam, bool* pfCallDWP)
{
    LRESULT lRet = 0;
    HRESULT hr = S_OK;
    bool fCallDWP = true; // Pass on to DefWindowProc?

    fCallDWP = !DwmDefWindowProc(hWnd, message, wParam, lParam, &lRet);

    // Handle window creation.
    if (message == WM_CREATE)
    {
        RECT rcClient;
        GetWindowRect(hWnd, &rcClient);

        // Inform application of the frame change.
        SetWindowPos(hWnd, 
                     NULL, 
                     rcClient.left, rcClient.top,
                     RECTWIDTH(rcClient), RECTHEIGHT(rcClient),
                     SWP_FRAMECHANGED);

        fCallDWP = true;
        lRet = 0;
    }

    // Handle window activation.
    if (message == WM_ACTIVATE)
    {
        // Extend the frame into the client area.
        MARGINS margins;

        margins.cxLeftWidth = LEFTEXTENDWIDTH;      // 8
        margins.cxRightWidth = RIGHTEXTENDWIDTH;    // 8
        margins.cyBottomHeight = BOTTOMEXTENDWIDTH; // 20
        margins.cyTopHeight = TOPEXTENDWIDTH;       // 27

        hr = DwmExtendFrameIntoClientArea(hWnd, &margins);

        if (!SUCCEEDED(hr))
        {
            // Handle error.
        }

        fCallDWP = true;
        lRet = 0;
    }

    if (message == WM_PAINT)
    {
        HDC hdc;
        {
            PAINTSTRUCT ps;
            hdc = BeginPaint(hWnd, &ps);
            PaintCustomCaption(hWnd, hdc);
            EndPaint(hWnd, &ps);
        }

        fCallDWP = true;
        lRet = 0;
    }

    // Handle the non-client size message.
    if ((message == WM_NCCALCSIZE) && (wParam == TRUE))
    {
        // Calculate new NCCALCSIZE_PARAMS based on custom NCA inset.
        NCCALCSIZE_PARAMS *pncsp = reinterpret_cast<NCCALCSIZE_PARAMS*>(lParam);

        pncsp->rgrc[0].left   = pncsp->rgrc[0].left   + 0;
        pncsp->rgrc[0].top    = pncsp->rgrc[0].top    + 0;
        pncsp->rgrc[0].right  = pncsp->rgrc[0].right  - 0;
        pncsp->rgrc[0].bottom = pncsp->rgrc[0].bottom - 0;

        lRet = 0;
        
        // No need to pass the message on to the DefWindowProc.
        fCallDWP = false;
    }

    // Handle hit testing in the NCA if not handled by DwmDefWindowProc.
    if ((message == WM_NCHITTEST) && (lRet == 0))
    {
        lRet = HitTestNCA(hWnd, wParam, lParam);

        if (lRet != HTNOWHERE)
        {
            fCallDWP = false;
        }
    }

    *pfCallDWP = fCallDWP;

    return lRet;
}

//
// Message handler for the application.
//
LRESULT AppWinProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;
    HRESULT hr; 
    LRESULT result = 0;

    switch (message)
    {
        case WM_CREATE:
            {}
            break;
        case WM_COMMAND:
            wmId    = LOWORD(wParam);
            wmEvent = HIWORD(wParam);

            // Parse the menu selections:
            switch (wmId)
            {
                default:
                    return DefWindowProc(hWnd, message, wParam, lParam);
            }
            break;
        case WM_PAINT:
            {
                hdc = BeginPaint(hWnd, &ps);
                PaintCustomCaption(hWnd, hdc);
                
                // Add any drawing code here...
    
                EndPaint(hWnd, &ps);
            }
            break;
        case WM_DESTROY:
            PostQuitMessage(0);
            break;
        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



## <a name="appendix-b-painting-the-caption-title"></a><span data-ttu-id="8bac2-203">Apêndice B: pintando o título da legenda</span><span class="sxs-lookup"><span data-stu-id="8bac2-203">Appendix B: Painting the Caption Title</span></span>

<span data-ttu-id="8bac2-204">O código a seguir demonstra como pintar um título de legenda no quadro estendido.</span><span class="sxs-lookup"><span data-stu-id="8bac2-204">The following code demonstrates how to paint a caption title on the extended frame.</span></span> <span data-ttu-id="8bac2-205">Essa função deve ser chamada de dentro das chamadas [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) e [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) .</span><span class="sxs-lookup"><span data-stu-id="8bac2-205">This function must be called from within the [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) and [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) calls.</span></span>


```
// Paint the title on the custom frame.
void PaintCustomCaption(HWND hWnd, HDC hdc)
{
    RECT rcClient;
    GetClientRect(hWnd, &rcClient);

    HTHEME hTheme = OpenThemeData(NULL, L"CompositedWindow::Window");
    if (hTheme)
    {
        HDC hdcPaint = CreateCompatibleDC(hdc);
        if (hdcPaint)
        {
            int cx = RECTWIDTH(rcClient);
            int cy = RECTHEIGHT(rcClient);

            // Define the BITMAPINFO structure used to draw text.
            // Note that biHeight is negative. This is done because
            // DrawThemeTextEx() needs the bitmap to be in top-to-bottom
            // order.
            BITMAPINFO dib = { 0 };
            dib.bmiHeader.biSize            = sizeof(BITMAPINFOHEADER);
            dib.bmiHeader.biWidth           = cx;
            dib.bmiHeader.biHeight          = -cy;
            dib.bmiHeader.biPlanes          = 1;
            dib.bmiHeader.biBitCount        = BIT_COUNT;
            dib.bmiHeader.biCompression     = BI_RGB;

            HBITMAP hbm = CreateDIBSection(hdc, &dib, DIB_RGB_COLORS, NULL, NULL, 0);
            if (hbm)
            {
                HBITMAP hbmOld = (HBITMAP)SelectObject(hdcPaint, hbm);

                // Setup the theme drawing options.
                DTTOPTS DttOpts = {sizeof(DTTOPTS)};
                DttOpts.dwFlags = DTT_COMPOSITED | DTT_GLOWSIZE;
                DttOpts.iGlowSize = 15;

                // Select a font.
                LOGFONT lgFont;
                HFONT hFontOld = NULL;
                if (SUCCEEDED(GetThemeSysFont(hTheme, TMT_CAPTIONFONT, &lgFont)))
                {
                    HFONT hFont = CreateFontIndirect(&lgFont);
                    hFontOld = (HFONT) SelectObject(hdcPaint, hFont);
                }

                // Draw the title.
                RECT rcPaint = rcClient;
                rcPaint.top += 8;
                rcPaint.right -= 125;
                rcPaint.left += 8;
                rcPaint.bottom = 50;
                DrawThemeTextEx(hTheme, 
                                hdcPaint, 
                                0, 0, 
                                szTitle, 
                                -1, 
                                DT_LEFT | DT_WORD_ELLIPSIS, 
                                &rcPaint, 
                                &DttOpts);

                // Blit text to the frame.
                BitBlt(hdc, 0, 0, cx, cy, hdcPaint, 0, 0, SRCCOPY);

                SelectObject(hdcPaint, hbmOld);
                if (hFontOld)
                {
                    SelectObject(hdcPaint, hFontOld);
                }
                DeleteObject(hbm);
            }
            DeleteDC(hdcPaint);
        }
        CloseThemeData(hTheme);
    }
}
```



## <a name="appendix-c-hittestnca-function"></a><span data-ttu-id="8bac2-206">Apêndice C: função HitTestNCA</span><span class="sxs-lookup"><span data-stu-id="8bac2-206">Appendix C: HitTestNCA Function</span></span>

<span data-ttu-id="8bac2-207">O código a seguir mostra a `HitTestNCA` função usada [para habilitar o teste de clique para o quadro personalizado](#enabling-hit-testing-for-the-custom-frame).</span><span class="sxs-lookup"><span data-stu-id="8bac2-207">The following code shows the `HitTestNCA` function used in [Enabling Hit Testing for the Custom Frame](#enabling-hit-testing-for-the-custom-frame).</span></span> <span data-ttu-id="8bac2-208">Essa função manipula a lógica de teste de cliques para o [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) quando o [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) não manipula a mensagem.</span><span class="sxs-lookup"><span data-stu-id="8bac2-208">This function handles the hit testing logic for the [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) when [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) does not handle the message.</span></span>


```
// Hit test the frame for resizing and moving.
LRESULT HitTestNCA(HWND hWnd, WPARAM wParam, LPARAM lParam)
{
    // Get the point coordinates for the hit test.
    POINT ptMouse = { GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam)};

    // Get the window rectangle.
    RECT rcWindow;
    GetWindowRect(hWnd, &rcWindow);

    // Get the frame rectangle, adjusted for the style without a caption.
    RECT rcFrame = { 0 };
    AdjustWindowRectEx(&rcFrame, WS_OVERLAPPEDWINDOW & ~WS_CAPTION, FALSE, NULL);

    // Determine if the hit test is for resizing. Default middle (1,1).
    USHORT uRow = 1;
    USHORT uCol = 1;
    bool fOnResizeBorder = false;

    // Determine if the point is at the top or bottom of the window.
    if (ptMouse.y >= rcWindow.top && ptMouse.y < rcWindow.top + TOPEXTENDWIDTH)
    {
        fOnResizeBorder = (ptMouse.y < (rcWindow.top - rcFrame.top));
        uRow = 0;
    }
    else if (ptMouse.y < rcWindow.bottom && ptMouse.y >= rcWindow.bottom - BOTTOMEXTENDWIDTH)
    {
        uRow = 2;
    }

    // Determine if the point is at the left or right of the window.
    if (ptMouse.x >= rcWindow.left && ptMouse.x < rcWindow.left + LEFTEXTENDWIDTH)
    {
        uCol = 0; // left side
    }
    else if (ptMouse.x < rcWindow.right && ptMouse.x >= rcWindow.right - RIGHTEXTENDWIDTH)
    {
        uCol = 2; // right side
    }

    // Hit test (HTTOPLEFT, ... HTBOTTOMRIGHT)
    LRESULT hitTests[3][3] = 
    {
        { HTTOPLEFT,    fOnResizeBorder ? HTTOP : HTCAPTION,    HTTOPRIGHT },
        { HTLEFT,       HTNOWHERE,     HTRIGHT },
        { HTBOTTOMLEFT, HTBOTTOM, HTBOTTOMRIGHT },
    };

    return hitTests[uRow][uCol];
}
```



## <a name="related-topics"></a><span data-ttu-id="8bac2-209">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8bac2-209">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bac2-210">Visão geral do Gerenciador de Janelas da Área de Trabalho</span><span class="sxs-lookup"><span data-stu-id="8bac2-210">Desktop Window Manager Overview</span></span>](dwm-overview.md)
</dt> </dl>

 

 