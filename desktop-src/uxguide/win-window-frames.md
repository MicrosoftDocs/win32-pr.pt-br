---
title: Quadros de janela
description: A maioria dos programas deve usar quadros de janela padrão. Aplicativos de imersão podem ter um modo de tela inteira que oculta o quadro da janela. Considere o uso estratégico de vidro para uma aparência mais simples, mais leve e coesa.
ms.assetid: 6613e07a-2466-4283-88a9-02f2a3fea079
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 40aa58ab48c032519f55afa7c269be6452956912
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104569141"
---
# <a name="window-frames"></a><span data-ttu-id="23c4c-105">Quadros de janela</span><span class="sxs-lookup"><span data-stu-id="23c4c-105">Window Frames</span></span>

> [!NOTE]
> <span data-ttu-id="23c4c-106">Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="23c4c-106">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="23c4c-107">Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="23c4c-107">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="23c4c-108">A maioria dos programas deve usar quadros de janela padrão.</span><span class="sxs-lookup"><span data-stu-id="23c4c-108">Most programs should use standard window frames.</span></span> <span data-ttu-id="23c4c-109">Aplicativos de imersão podem ter um modo de tela inteira que oculta o quadro da janela.</span><span class="sxs-lookup"><span data-stu-id="23c4c-109">Immersive applications can have a full screen mode that hides the window frame.</span></span> <span data-ttu-id="23c4c-110">Considere o uso estratégico de vidro para uma aparência mais simples, mais leve e coesa.</span><span class="sxs-lookup"><span data-stu-id="23c4c-110">Consider using glass strategically for a simpler, lighter, more cohesive look.</span></span>

<span data-ttu-id="23c4c-111">Com um quadro de janela, os usuários podem manipular uma janela e exibir o título e o ícone para identificar seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="23c4c-111">With a window frame, users can manipulate a window and view the title and icon to identify its contents.</span></span>

![<span data-ttu-id="23c4c-112">captura de tela do quadro da janela ao contrário da janela do bloco de notas</span><span class="sxs-lookup"><span data-stu-id="23c4c-112">screen shot of window frame around notepad window</span></span> ](images/win-window-frames-image1.png)

<span data-ttu-id="23c4c-113">Um quadro de janela típico.</span><span class="sxs-lookup"><span data-stu-id="23c4c-113">A typical window frame.</span></span>

<span data-ttu-id="23c4c-114">**Observação:** As diretrizes relacionadas ao [Gerenciamento de janelas](win-window-mgt.md) e à [identidade visual](exper-branding.md) são apresentadas em artigos separados.</span><span class="sxs-lookup"><span data-stu-id="23c4c-114">**Note:** Guidelines related to [window management](win-window-mgt.md) and [branding](exper-branding.md) are presented in separate articles.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="23c4c-115">Conceitos de design</span><span class="sxs-lookup"><span data-stu-id="23c4c-115">Design concepts</span></span>

### <a name="glass-window-frames"></a><span data-ttu-id="23c4c-116">Quadros de janela de vidro</span><span class="sxs-lookup"><span data-stu-id="23c4c-116">Glass window frames</span></span>

<span data-ttu-id="23c4c-117">Os quadros de janela de vidro são um novo aspecto surpreendente da estética do Microsoft Windows, objetivando ser atraentes e leves.</span><span class="sxs-lookup"><span data-stu-id="23c4c-117">The glass window frames are a striking new aspect of the Microsoft Windows aesthetic, aiming to be both attractive and lightweight.</span></span> <span data-ttu-id="23c4c-118">Esses quadros translúcidas fornecem ao Windows uma aparência aberta e menos invasiva, ajudando os usuários a se concentrarem no conteúdo e na funcionalidade, e não na interface em torno dela.</span><span class="sxs-lookup"><span data-stu-id="23c4c-118">These translucent frames give windows an open, less intrusive appearance, helping users focus on content and functionality rather than the interface surrounding it.</span></span>

![<span data-ttu-id="23c4c-119">captura de tela do quadro de vidro em volta da calculadora</span><span class="sxs-lookup"><span data-stu-id="23c4c-119">screen shot of glass frame around calculator</span></span> ](images/win-window-frames-image2.png)

<span data-ttu-id="23c4c-120">Quadros de janela de vidro.</span><span class="sxs-lookup"><span data-stu-id="23c4c-120">Glass window frames.</span></span>

<span data-ttu-id="23c4c-121">Você pode usar o vidro estrategicamente em pequenas regiões dentro de uma janela que toca o quadro da janela.</span><span class="sxs-lookup"><span data-stu-id="23c4c-121">You can use glass strategically in small regions within a window that touch the window frame.</span></span> <span data-ttu-id="23c4c-122">Essas regiões parecem ser parte do quadro da janela, embora tecnicamente elas façam parte da área do cliente da janela.</span><span class="sxs-lookup"><span data-stu-id="23c4c-122">Such regions appear to be part of the window frame, even though technically they are part of the window's client area.</span></span>

![<span data-ttu-id="23c4c-123">captura de tela da janela com borda translúcida</span><span class="sxs-lookup"><span data-stu-id="23c4c-123">screen shot of window with translucent edge</span></span> ](images/win-window-frames-image3.png)

<span data-ttu-id="23c4c-124">Neste exemplo, o vidro é usado na área do cliente para deixá-lo parecer com parte do quadro.</span><span class="sxs-lookup"><span data-stu-id="23c4c-124">In this example, glass is used in the client area to make it look like part of the frame.</span></span>

### <a name="hidden-frames"></a><span data-ttu-id="23c4c-125">Quadros ocultos</span><span class="sxs-lookup"><span data-stu-id="23c4c-125">Hidden frames</span></span>

<span data-ttu-id="23c4c-126">Às vezes, o melhor quadro de janela não é nenhum quadro.</span><span class="sxs-lookup"><span data-stu-id="23c4c-126">Sometimes the best window frame is no frame at all.</span></span> <span data-ttu-id="23c4c-127">Esse é geralmente o caso para a [janela principal](glossary.md) de aplicativos de [tela inteira](glossary.md) de imersão que não são usados em conjunto com outros programas, como media players, jogos e aplicativos de quiosque.</span><span class="sxs-lookup"><span data-stu-id="23c4c-127">This is often the case for the [primary window](glossary.md) of immersive [full screen](glossary.md) applications that aren't used in conjunction with other programs, such as media players, games, and kiosk applications.</span></span>

<span data-ttu-id="23c4c-128">Os visualizadores de conteúdo geralmente se beneficiam da opção de mostrar o conteúdo em tela inteira.</span><span class="sxs-lookup"><span data-stu-id="23c4c-128">Content viewers often benefit from having the option to show content full screen.</span></span> <span data-ttu-id="23c4c-129">Os exemplos incluem o Windows Internet Explorer, a Galeria de fotos do Windows Live, o Windows Movie Maker HD, o Microsoft PowerPoint e o Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="23c4c-129">Examples include Windows Internet Explorer , Windows Live Photo Gallery, Windows Movie Maker HD, Microsoft PowerPoint , and Microsoft Word.</span></span>

![<span data-ttu-id="23c4c-130">captura de tela do player de mídia no modo de exibição de tela inteira</span><span class="sxs-lookup"><span data-stu-id="23c4c-130">screen shot of media player in full-screen view</span></span> ](images/win-window-frames-image4.png)

<span data-ttu-id="23c4c-131">Neste exemplo, o Windows Media Player pode exibir seu conteúdo em tela inteira.</span><span class="sxs-lookup"><span data-stu-id="23c4c-131">In this example, Windows Media Player can display its content full screen.</span></span>

### <a name="custom-frames"></a><span data-ttu-id="23c4c-132">Quadros personalizados</span><span class="sxs-lookup"><span data-stu-id="23c4c-132">Custom frames</span></span>

<span data-ttu-id="23c4c-133">A maioria dos aplicativos do Windows deve usar os quadros de janela padrão.</span><span class="sxs-lookup"><span data-stu-id="23c4c-133">Most Windows applications should use the standard window frames.</span></span> <span data-ttu-id="23c4c-134">No entanto, para aplicativos de imersão, tela inteira e autônoma, como jogos e aplicativos de quiosque, pode ser apropriado usar quadros personalizados para qualquer janela que não seja mostrada em tela inteira.</span><span class="sxs-lookup"><span data-stu-id="23c4c-134">However, for immersive, full screen, stand-alone applications like games and kiosk applications, it may be appropriate to use custom frames for any windows that aren't shown full screen.</span></span> <span data-ttu-id="23c4c-135">A motivação de usar quadros personalizados deve ser oferecer a experiência geral uma sensação única, não apenas para [identidade visual](exper-branding.md).</span><span class="sxs-lookup"><span data-stu-id="23c4c-135">The motivation to use custom frames should be to give the overall experience a unique feel, not just for [branding](exper-branding.md).</span></span>

![<span data-ttu-id="23c4c-136">ilustração de quebra-cabeça e quadro de imagem embaralhada</span><span class="sxs-lookup"><span data-stu-id="23c4c-136">illustration of scrambled picture puzzle and frame</span></span> ](images/win-window-frames-image5.png)

<span data-ttu-id="23c4c-137">Os quadros personalizados são apropriados para aplicativos de imersão, tela inteira e autônomos, como jogos.</span><span class="sxs-lookup"><span data-stu-id="23c4c-137">Custom frames are appropriate for immersive, full screen, stand-alone applications such as games.</span></span>

## <a name="guidelines"></a><span data-ttu-id="23c4c-138">Diretrizes</span><span class="sxs-lookup"><span data-stu-id="23c4c-138">Guidelines</span></span>

### <a name="window-frames"></a><span data-ttu-id="23c4c-139">Quadros de janela</span><span class="sxs-lookup"><span data-stu-id="23c4c-139">Window frames</span></span>

-   <span data-ttu-id="23c4c-140">Use quadros de janela padrão.</span><span class="sxs-lookup"><span data-stu-id="23c4c-140">Use standard window frames.</span></span>
    -   <span data-ttu-id="23c4c-141">**Exceção:** Para dar uma aparência de tela inteira, os aplicativos autônomos são uma sensação única:</span><span class="sxs-lookup"><span data-stu-id="23c4c-141">**Exception:** To give immersive full screen, stand-alone applications a unique feel:</span></span>
        -   <span data-ttu-id="23c4c-142">Considere ocultar o quadro de janela da [janela principal](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="23c4c-142">Consider hiding the window frame of the [primary window](glossary.md).</span></span>
        -   <span data-ttu-id="23c4c-143">Considere o uso de quadros personalizados para a [janela secundária](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="23c4c-143">Consider using custom frames for [secondary window](glossary.md).</span></span>
        -   <span data-ttu-id="23c4c-144">Se um quadro personalizado for apropriado, escolha um design que seja leve e não atraia muita atenção para si mesmo.</span><span class="sxs-lookup"><span data-stu-id="23c4c-144">If a custom frame is appropriate, choose a design that is lightweight and doesn't draw too much attention to itself.</span></span>

            <span data-ttu-id="23c4c-145">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="23c4c-145">**Incorrect:**</span></span>

            ![<span data-ttu-id="23c4c-146">captura de tela de quadro de distração</span><span class="sxs-lookup"><span data-stu-id="23c4c-146">screen shot of distracting frame</span></span> ](images/win-window-frames-image6.png)

            <span data-ttu-id="23c4c-147">Neste exemplo, o quadro personalizado chama muita atenção para si mesmo.</span><span class="sxs-lookup"><span data-stu-id="23c4c-147">In this example, the custom frame draws too much attention to itself.</span></span>
-   <span data-ttu-id="23c4c-148">Não adicione controles a um quadro de janela.</span><span class="sxs-lookup"><span data-stu-id="23c4c-148">Don't add controls to a window frame.</span></span> <span data-ttu-id="23c4c-149">Em vez disso, coloque os controles dentro da janela.</span><span class="sxs-lookup"><span data-stu-id="23c4c-149">Put the controls within the window instead.</span></span>

    <span data-ttu-id="23c4c-150">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="23c4c-150">**Incorrect:**</span></span>

    ![<span data-ttu-id="23c4c-151">captura de tela de controle no quadro da janela</span><span class="sxs-lookup"><span data-stu-id="23c4c-151">screen shot of control in window frame</span></span> ](images/win-window-frames-image7.png)

    <span data-ttu-id="23c4c-152">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="23c4c-152">**Correct:**</span></span>

    ![<span data-ttu-id="23c4c-153">captura de tela de controle na área do cliente</span><span class="sxs-lookup"><span data-stu-id="23c4c-153">screen shot of control in client area</span></span> ](images/win-window-frames-image8.png)

    <span data-ttu-id="23c4c-154">No exemplo correto, o controle está dentro da área do cliente em vez do quadro da janela.</span><span class="sxs-lookup"><span data-stu-id="23c4c-154">In the correct example, the control is within the client area instead of the window frame.</span></span>

### <a name="full-screen-mode"></a><span data-ttu-id="23c4c-155">Modo de tela inteira</span><span class="sxs-lookup"><span data-stu-id="23c4c-155">Full screen mode</span></span>

-   <span data-ttu-id="23c4c-156">Para programas que têm um modo de tela inteira opcional, para habilitar o modo de tela inteira:</span><span class="sxs-lookup"><span data-stu-id="23c4c-156">For programs that have an optional full screen mode, to enable full screen mode:</span></span>
    -   <span data-ttu-id="23c4c-157">Ter um comando de tela inteira modal na barra de menus ou na barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="23c4c-157">Have a modal full screen command in the menu bar or toolbar.</span></span> <span data-ttu-id="23c4c-158">Quando o usuário clicar no comando, mostrará o comando em seu estado selecionado.</span><span class="sxs-lookup"><span data-stu-id="23c4c-158">When the user clicks the command, show the command in its selected state.</span></span>

        ![<span data-ttu-id="23c4c-159">captura de tela de janela com item de menu de tela inteira</span><span class="sxs-lookup"><span data-stu-id="23c4c-159">screen shot of window with full screen menu item</span></span> ](images/win-window-frames-image9.png)

        <span data-ttu-id="23c4c-160">Este exemplo mostra o comando de tela inteira junto com sua tecla de atalho padrão.</span><span class="sxs-lookup"><span data-stu-id="23c4c-160">This example shows the full screen command along with its standard shortcut key.</span></span>

-   <span data-ttu-id="23c4c-161">Use F11 para a tecla de atalho de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="23c4c-161">Use F11 for the full screen shortcut key.</span></span>
-   <span data-ttu-id="23c4c-162">Se houver uma barra de ferramentas e o modo de tela inteira for comumente usado, também terá um botão de barra de ferramentas gráfica com uma dica de ferramenta de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="23c4c-162">If there is a toolbar and full screen mode is commonly used, also have a graphic toolbar button with a Full screen tooltip.</span></span>

    ![<span data-ttu-id="23c4c-163">captura de tela dos botões tela inteira e reverter</span><span class="sxs-lookup"><span data-stu-id="23c4c-163">screen shot of full screen and revert buttons</span></span> ](images/win-window-frames-image10.png)

    <span data-ttu-id="23c4c-164">Exemplos de botões da barra de ferramentas de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="23c4c-164">Examples of full screen toolbar buttons.</span></span>

-   <span data-ttu-id="23c4c-165">Para reverter do modo de tela inteira:</span><span class="sxs-lookup"><span data-stu-id="23c4c-165">To revert back from full screen mode:</span></span>
    -   <span data-ttu-id="23c4c-166">Ter um comando de tela inteira modal na barra de menus ou na barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="23c4c-166">Have a modal full screen command in the menu bar or toolbar.</span></span> <span data-ttu-id="23c4c-167">Quando o usuário clicar no comando, mostrará o comando em seu estado limpo.</span><span class="sxs-lookup"><span data-stu-id="23c4c-167">When the user clicks the command, show the command in its cleared state.</span></span>
    -   <span data-ttu-id="23c4c-168">Use F11 para a tecla de atalho de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="23c4c-168">Use F11 for the full screen shortcut key.</span></span> <span data-ttu-id="23c4c-169">Se ainda não tiver sido atribuído, ESC também poderá ser usado para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="23c4c-169">If not already assigned, Esc can also be used for this purpose.</span></span>

### <a name="glass"></a><span data-ttu-id="23c4c-170">Vidro</span><span class="sxs-lookup"><span data-stu-id="23c4c-170">Glass</span></span>

<span data-ttu-id="23c4c-171">Quadros de janela padrão usam vidro automaticamente no Windows, mas você também pode usar vidro em regiões que tocam o quadro da janela.</span><span class="sxs-lookup"><span data-stu-id="23c4c-171">Standard window frames use glass automatically in Windows, but you can also use glass in regions that touch the window frame.</span></span>

-   <span data-ttu-id="23c4c-172">**Considere usar o vidro estrategicamente em pequenas regiões tocando no quadro da janela sem texto.**</span><span class="sxs-lookup"><span data-stu-id="23c4c-172">**Consider using glass strategically in small regions touching the window frame without text.**</span></span> <span data-ttu-id="23c4c-173">Fazer isso pode dar a um programa uma visão mais simples, mais leve e coesa, fazendo com que a região pareça ser parte do quadro.</span><span class="sxs-lookup"><span data-stu-id="23c4c-173">Doing so can give a program a simpler, lighter, more cohesive look by making the region appear to be part of the frame.</span></span>
-   ![<span data-ttu-id="23c4c-174">captura de tela da janela com borda translúcida</span><span class="sxs-lookup"><span data-stu-id="23c4c-174">screen shot of window with translucent edge</span></span> ](images/win-window-frames-image3.png)
-   <span data-ttu-id="23c4c-175">Neste exemplo, o vidro concentra a atenção do usuário sobre o conteúdo em vez dos controles.</span><span class="sxs-lookup"><span data-stu-id="23c4c-175">In this example, glass focuses the user's attention on the content instead of the controls.</span></span>
-   <span data-ttu-id="23c4c-176">**Não use o vidro em situações em que um plano de fundo de janela simples seria mais atraente ou mais fácil de usar.**</span><span class="sxs-lookup"><span data-stu-id="23c4c-176">**Don't use glass in situations where a plain window background would be more attractive or easier to use.**</span></span>

<span data-ttu-id="23c4c-177">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="23c4c-177">**Correct:**</span></span>

![<span data-ttu-id="23c4c-178">captura de tela de janela com quatro elementos gráficos e rótulo</span><span class="sxs-lookup"><span data-stu-id="23c4c-178">screen shot of window with four graphics and label</span></span> ](images/win-window-frames-image11.png)

<span data-ttu-id="23c4c-179">Neste exemplo, o vidro é usado para dar à janela ALT + TAB uma aparência leve.</span><span class="sxs-lookup"><span data-stu-id="23c4c-179">In this example, glass is used to give the Alt+Tab window a lightweight appearance.</span></span> <span data-ttu-id="23c4c-180">O vidro funciona para esta janela porque ele consiste em gráficos e um único rótulo de texto forte.</span><span class="sxs-lookup"><span data-stu-id="23c4c-180">Glass works for this window because it consists of graphics and a single, strong text label.</span></span>

<span data-ttu-id="23c4c-181">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="23c4c-181">**Incorrect:**</span></span>

![<span data-ttu-id="23c4c-182">captura de tela de janela com doze elementos gráficos</span><span class="sxs-lookup"><span data-stu-id="23c4c-182">screen shot of window with twelve graphics</span></span> ](images/win-window-frames-image12.png)

<span data-ttu-id="23c4c-183">Neste exemplo incorreto, o uso de vidro está me distraindo.</span><span class="sxs-lookup"><span data-stu-id="23c4c-183">In this incorrect example, the use of glass is distracting.</span></span> <span data-ttu-id="23c4c-184">Um plano de fundo de janela simples seria uma opção melhor.</span><span class="sxs-lookup"><span data-stu-id="23c4c-184">A plain window background would be a better choice.</span></span>

 

 