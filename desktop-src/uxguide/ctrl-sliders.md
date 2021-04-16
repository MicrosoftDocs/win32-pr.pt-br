---
title: Controles deslizantes (conceitos básicos de Design)
description: Com um controle deslizante, os usuários podem escolher um intervalo contínuo de valores.
ms.assetid: dee70fbc-6f18-43c7-9d41-4e97eac41e53
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 7ff9791ab49c338e4c11e014a3e996771571add9
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104567021"
---
# <a name="sliders-design-basics"></a><span data-ttu-id="e38c4-103">Controles deslizantes (conceitos básicos de Design)</span><span class="sxs-lookup"><span data-stu-id="e38c4-103">Sliders (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="e38c4-104">Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="e38c4-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="e38c4-105">Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="e38c4-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="e38c4-106">Com um controle deslizante, os usuários podem escolher um intervalo contínuo de valores.</span><span class="sxs-lookup"><span data-stu-id="e38c4-106">With a slider, users can choose from a continuous range of values.</span></span> <span data-ttu-id="e38c4-107">Um controle deslizante tem uma barra que mostra o intervalo e um indicador que mostra o valor atual.</span><span class="sxs-lookup"><span data-stu-id="e38c4-107">A slider has a bar that shows the range and an indicator that shows the current value.</span></span> <span data-ttu-id="e38c4-108">As marcas de escala opcionais mostram valores.</span><span class="sxs-lookup"><span data-stu-id="e38c4-108">Optional tick marks show values.</span></span>

![<span data-ttu-id="e38c4-109">Figura mostrando barras, controle deslizante e marcas de escala</span><span class="sxs-lookup"><span data-stu-id="e38c4-109">figure showing bar, slider, and tick marks</span></span> ](images/ctrl-sliders-image1.png)

<span data-ttu-id="e38c4-110">Um controle deslizante típico.</span><span class="sxs-lookup"><span data-stu-id="e38c4-110">A typical slider.</span></span>

> [!Note]  
> <span data-ttu-id="e38c4-111">As diretrizes relacionadas ao [layout](vis-layout.md) são apresentadas em um artigo separado.</span><span class="sxs-lookup"><span data-stu-id="e38c4-111">Guidelines related to [layout](vis-layout.md) are presented in a separate article.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="e38c4-112">Esse é o controle correto?</span><span class="sxs-lookup"><span data-stu-id="e38c4-112">Is this the right control?</span></span>

<span data-ttu-id="e38c4-113">Use um controle deslizante quando desejar que os usuários possam **definir valores contíguos definidos (como volume ou brilho) ou um intervalo de valores discretos (como configurações de resolução de tela).**</span><span class="sxs-lookup"><span data-stu-id="e38c4-113">Use a slider when you want your users to be able to **set defined, contiguous values (such as volume or brightness) or a range of discrete values (such as screen resolution settings).**</span></span>

<span data-ttu-id="e38c4-114">Um controle deslizante é uma boa opção quando você sabe que os usuários imaginam o valor como uma quantidade relativa, e não como um valor numérico.</span><span class="sxs-lookup"><span data-stu-id="e38c4-114">A slider is a good choice when you know that users think of the value as a relative quantity, not a numeric value.</span></span> <span data-ttu-id="e38c4-115">Por exemplo, os usuários pensam em definir o volume de áudio como baixo ou médio, e não em definir o valor como 2 ou 5.</span><span class="sxs-lookup"><span data-stu-id="e38c4-115">For example, users think about setting their audio volume to low or medium—not about setting the value to 2 or 5.</span></span>

<span data-ttu-id="e38c4-116">Para decidir, considere estas perguntas:</span><span class="sxs-lookup"><span data-stu-id="e38c4-116">To decide, consider these questions:</span></span>

-   <span data-ttu-id="e38c4-117">**A configuração parece uma quantidade relativa?**</span><span class="sxs-lookup"><span data-stu-id="e38c4-117">**Does the setting seem like a relative quantity?**</span></span> <span data-ttu-id="e38c4-118">Caso contrário, use [botões de opção](ctrl-radio-buttons.md)ou uma lista [suspensa](/windows/desktop/uxguide/ctrl-drop) ou de [seleção única](ctrl-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="e38c4-118">If not, use [radio buttons](ctrl-radio-buttons.md), or a [drop-down](/windows/desktop/uxguide/ctrl-drop) or [single-selection list](ctrl-list-boxes.md).</span></span>
-   <span data-ttu-id="e38c4-119">**A configuração é um valor numérico exato conhecido?**</span><span class="sxs-lookup"><span data-stu-id="e38c4-119">**Is the setting an exact, known numeric value?**</span></span> <span data-ttu-id="e38c4-120">Nesse caso, use uma [caixa de texto numérica](ctrl-text-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="e38c4-120">If so, use a [numeric text boxes](ctrl-text-boxes.md).</span></span>
-   <span data-ttu-id="e38c4-121">**O usuário se beneficiaria com um feedback instantâneo sobre o efeito das alterações de configuração?**</span><span class="sxs-lookup"><span data-stu-id="e38c4-121">**Would a user benefit from instant feedback on the effect of setting changes?**</span></span> <span data-ttu-id="e38c4-122">Se sim, use um controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="e38c4-122">If so, use a slider.</span></span> <span data-ttu-id="e38c4-123">Por exemplo, os usuários podem escolher uma cor com mais facilidade vendo imediatamente o efeito das alterações nos valores de matiz, saturação ou luminosidade.</span><span class="sxs-lookup"><span data-stu-id="e38c4-123">For example, users can choose a color more easily by immediately seeing the effect of changes to hue, saturation, or luminosity values.</span></span>
-   <span data-ttu-id="e38c4-124">**A configuração tem um intervalo de quatro ou mais valores?**</span><span class="sxs-lookup"><span data-stu-id="e38c4-124">**Does the setting have a range of four or more values?**</span></span> <span data-ttu-id="e38c4-125">Se não parecer, use os botões de opção.</span><span class="sxs-lookup"><span data-stu-id="e38c4-125">If not, use radio buttons.</span></span>
-   <span data-ttu-id="e38c4-126">**O usuário pode alterar o valor?**</span><span class="sxs-lookup"><span data-stu-id="e38c4-126">**Can the user change the value?**</span></span> <span data-ttu-id="e38c4-127">Controles deslizantes são destinados para interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e38c4-127">Sliders are for user interaction.</span></span> <span data-ttu-id="e38c4-128">Se um usuário não puder alterar o valor, use uma [caixa de texto](ctrl-text-boxes.md) somente leitura em vez disso.</span><span class="sxs-lookup"><span data-stu-id="e38c4-128">If a user can't ever change the value, use a read-only [text box](ctrl-text-boxes.md) instead.</span></span>

<span data-ttu-id="e38c4-129">Se um controle deslizante ou uma caixa de texto numérica for possível, use uma caixa de texto numérica se:</span><span class="sxs-lookup"><span data-stu-id="e38c4-129">If a slider or a numeric text box is possible, use a numeric text box if:</span></span>

-   <span data-ttu-id="e38c4-130">O espaço na tela for restrito.</span><span class="sxs-lookup"><span data-stu-id="e38c4-130">Screen space is tight.</span></span>
-   <span data-ttu-id="e38c4-131">É provável que um usuário prefira usar o teclado.</span><span class="sxs-lookup"><span data-stu-id="e38c4-131">A user is likely to prefer using the keyboard.</span></span>

<span data-ttu-id="e38c4-132">Use um controle deslizante se:</span><span class="sxs-lookup"><span data-stu-id="e38c4-132">Use a slider if:</span></span>

-   <span data-ttu-id="e38c4-133">Os usuários forem se beneficiar com um feedback instantâneo.</span><span class="sxs-lookup"><span data-stu-id="e38c4-133">Users will benefit from instant feedback.</span></span>

## <a name="guidelines"></a><span data-ttu-id="e38c4-134">Diretrizes</span><span class="sxs-lookup"><span data-stu-id="e38c4-134">Guidelines</span></span>

-   <span data-ttu-id="e38c4-135">**Use uma orientação natural.**</span><span class="sxs-lookup"><span data-stu-id="e38c4-135">**Use a natural orientation.**</span></span> <span data-ttu-id="e38c4-136">Por exemplo, se o controle deslizante representar um valor real que normalmente é mostrado na vertical (como temperatura), use uma orientação vertical.</span><span class="sxs-lookup"><span data-stu-id="e38c4-136">For example, if the slider represents a real-world value that is normally shown vertically (such as temperature), use a vertical orientation.</span></span>
-   <span data-ttu-id="e38c4-137">**Oriente o controle deslizante para refletir a cultura dos usuários.**</span><span class="sxs-lookup"><span data-stu-id="e38c4-137">**Orient the slider to reflect the culture of your users.**</span></span> <span data-ttu-id="e38c4-138">Por exemplo, as culturas ocidentais são lidas da esquerda para a direita, portanto, para controles deslizantes horizontais, coloque a extremidade inferior do intervalo à esquerda e a extremidade superior à direita.</span><span class="sxs-lookup"><span data-stu-id="e38c4-138">For example, Western cultures read from left to right, so for horizontal sliders, put the low end of the range on the left and the high end on the right.</span></span> <span data-ttu-id="e38c4-139">Para culturas que lêem da direita para a esquerda, faça o oposto.</span><span class="sxs-lookup"><span data-stu-id="e38c4-139">For cultures that read from right to left, do the opposite.</span></span>
-   <span data-ttu-id="e38c4-140">**Dimensione o controle para que um usuário possa definir facilmente o valor desejado.**</span><span class="sxs-lookup"><span data-stu-id="e38c4-140">**Size the control so that a user can easily set the desired value.**</span></span> <span data-ttu-id="e38c4-141">Para configurações com valores distintos, certifique-se de que o usuário pode facilmente selecionar qualquer valor utilizando o mouse.</span><span class="sxs-lookup"><span data-stu-id="e38c4-141">For settings with discrete values, make sure the user can easily select any value using the mouse.</span></span>
-   <span data-ttu-id="e38c4-142">**Considere usar uma escala não linear se o intervalo de valores for grande e os usuários provavelmente selecionarem valores em uma extremidade do intervalo.**</span><span class="sxs-lookup"><span data-stu-id="e38c4-142">**Consider using a non-linear scale if the range of values is large and users will likely select values at one end of the range.**</span></span> <span data-ttu-id="e38c4-143">Por exemplo, o valor de tempo pode ser de 1 minuto, 1 hora, 1 dia ou 1 mês.</span><span class="sxs-lookup"><span data-stu-id="e38c4-143">For example, time value might be 1 minute, 1 hour, 1 day, or 1 month.</span></span>
-   <span data-ttu-id="e38c4-144">**Sempre que for prático, dê comentários imediatos enquanto ou depois que um usuário fizer uma seleção.**</span><span class="sxs-lookup"><span data-stu-id="e38c4-144">**Whenever practical, give immediate feedback while or after a user makes a selection.**</span></span> <span data-ttu-id="e38c4-145">Por exemplo, o controle de volume do Microsoft Windows emite um aviso sonoro para indicar o volume de áudio resultante.</span><span class="sxs-lookup"><span data-stu-id="e38c4-145">For example, the Microsoft Windows volume control beeps to indicate the resulting audio volume.</span></span>
-   <span data-ttu-id="e38c4-146">**Use rótulos para mostrar o intervalo de valores.**</span><span class="sxs-lookup"><span data-stu-id="e38c4-146">**Use labels to show the range of values.**</span></span>

    <span data-ttu-id="e38c4-147">**Exceção:** Se o controle deslizante for verticalmente orientado e o rótulo superior for máximo, alto, mais ou equivalente, você poderá omitir os outros rótulos, pois o significado é claro.</span><span class="sxs-lookup"><span data-stu-id="e38c4-147">**Exception:** If the slider is vertically oriented and the top label is Maximum, High, More, or equivalent, you can omit the other labels since the meaning is clear.</span></span>

    ![<span data-ttu-id="e38c4-148">Figura de um controle deslizante vertical</span><span class="sxs-lookup"><span data-stu-id="e38c4-148">figure of a vertical slider</span></span> ](images/ctrl-sliders-image2.png)

    <span data-ttu-id="e38c4-149">Neste exemplo, a orientação vertical do controle deslizante torna os rótulos de intervalo desnecessários.</span><span class="sxs-lookup"><span data-stu-id="e38c4-149">In this example, the slider's vertical orientation makes the range labels unnecessary.</span></span>

-   <span data-ttu-id="e38c4-150">**Use marcas de escala quando os usuários precisarem saber o valor aproximado da configuração.**</span><span class="sxs-lookup"><span data-stu-id="e38c4-150">**Use tick marks when users need to know the approximate value of the setting.**</span></span>
-   <span data-ttu-id="e38c4-151">**Use marcas de escala e um rótulo de valor quando os usuários precisarem saber o valor exato da configuração que escolherem.**</span><span class="sxs-lookup"><span data-stu-id="e38c4-151">**Use tick marks and a value label when users need to know the exact value of the setting they choose.**</span></span> <span data-ttu-id="e38c4-152">Sempre use um rótulo de valor se um usuário precisar saber as unidades para fazer sentido da configuração.</span><span class="sxs-lookup"><span data-stu-id="e38c4-152">Always use a value label if a user needs to know the units to make sense of the setting.</span></span>

    ![<span data-ttu-id="e38c4-153">figura do controle deslizante mostrando o número de pixels selecionados</span><span class="sxs-lookup"><span data-stu-id="e38c4-153">figure of slider showing number of pixels selected</span></span> ](images/ctrl-sliders-image3.png)

    <span data-ttu-id="e38c4-154">Neste exemplo, um rótulo é usado para indicar claramente o valor selecionado.</span><span class="sxs-lookup"><span data-stu-id="e38c4-154">In this example, a label is used to clearly indicate the selected value.</span></span>

-   <span data-ttu-id="e38c4-155">**Para controles deslizantes orientados horizontalmente, coloque as marcas de escala sob o controle deslizante.**</span><span class="sxs-lookup"><span data-stu-id="e38c4-155">**For horizontally-oriented sliders, place tick marks under the slider.**</span></span> <span data-ttu-id="e38c4-156">Para controles deslizantes orientados verticalmente, coloque as marcas de escala à direita para culturas ocidentais; para culturas que lêem da direita para a esquerda, faça o oposto.</span><span class="sxs-lookup"><span data-stu-id="e38c4-156">For vertically-oriented sliders, place tick marks to the right for Western cultures; for cultures that read from right to left, do the opposite.</span></span>
-   <span data-ttu-id="e38c4-157">**Coloque o rótulo de valor completamente abaixo do controle deslizante para que a relação seja clara.**</span><span class="sxs-lookup"><span data-stu-id="e38c4-157">**Place the value label completely under the slider control so that the relationship is clear.**</span></span>

    <span data-ttu-id="e38c4-158">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="e38c4-158">**Incorrect:**</span></span>

    ![<span data-ttu-id="e38c4-159">Figura de um rótulo que é maior que seu controle deslizante</span><span class="sxs-lookup"><span data-stu-id="e38c4-159">figure of a label that is longer than its slider</span></span> ](images/ctrl-sliders-image4.png)

    <span data-ttu-id="e38c4-160">Neste exemplo, o rótulo de valor não está alinhado sob o controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="e38c4-160">In this example, the value label isn't aligned under the slider.</span></span>

-   <span data-ttu-id="e38c4-161">**Ao desabilitar um controle deslizante, desabilite também todos os rótulos associados.**</span><span class="sxs-lookup"><span data-stu-id="e38c4-161">**When disabling a slider, also disable any associated labels.**</span></span>
-   <span data-ttu-id="e38c4-162">**Não use um controle deslizante e uma caixa de texto numérico para a mesma configuração.**</span><span class="sxs-lookup"><span data-stu-id="e38c4-162">**Don't use both a slider and a numeric text box for the same setting.**</span></span> <span data-ttu-id="e38c4-163">Use apenas o controle mais apropriado.</span><span class="sxs-lookup"><span data-stu-id="e38c4-163">Use only the more appropriate control.</span></span>

    <span data-ttu-id="e38c4-164">**Exceção:** Use ambos os controles quando o usuário precisar de comentários imediatos e a capacidade de definir um valor numérico exato.</span><span class="sxs-lookup"><span data-stu-id="e38c4-164">**Exception:** Use both controls when the user needs both immediate feedback and the ability to set an exact numeric value.</span></span>

-   <span data-ttu-id="e38c4-165">**Não use um controle deslizante como indicador de progresso.**</span><span class="sxs-lookup"><span data-stu-id="e38c4-165">**Don't use a slider as a progress indicator.**</span></span>
-   <span data-ttu-id="e38c4-166">**Não altere o tamanho do indicador do controle deslizante do tamanho padrão.**</span><span class="sxs-lookup"><span data-stu-id="e38c4-166">**Don't change the size of the slider indicator from the default size.**</span></span>

    <span data-ttu-id="e38c4-167">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="e38c4-167">**Incorrect:**</span></span>

    ![<span data-ttu-id="e38c4-168">figura do controle deslizante menor que o padrão</span><span class="sxs-lookup"><span data-stu-id="e38c4-168">figure of slider that is smaller than the default</span></span> ](images/ctrl-sliders-image5.png)

    <span data-ttu-id="e38c4-169">Neste exemplo, um tamanho menor do que o padrão é usado.</span><span class="sxs-lookup"><span data-stu-id="e38c4-169">In this example, a size smaller than the default is used.</span></span>

    <span data-ttu-id="e38c4-170">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="e38c4-170">**Correct:**</span></span>

    ![<span data-ttu-id="e38c4-171">Figura mostrando o controle deslizante padrão</span><span class="sxs-lookup"><span data-stu-id="e38c4-171">figure showing the default slider</span></span> ](images/ctrl-sliders-image6.png)

    <span data-ttu-id="e38c4-172">Neste exemplo, o tamanho padrão é usado.</span><span class="sxs-lookup"><span data-stu-id="e38c4-172">In this example, the default size is used.</span></span>

-   <span data-ttu-id="e38c4-173">**Não rotular todas as marcas de escala.**</span><span class="sxs-lookup"><span data-stu-id="e38c4-173">**Don't label every tick mark.**</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="e38c4-174">Dimensionamento e espaçamento recomendados</span><span class="sxs-lookup"><span data-stu-id="e38c4-174">Recommended sizing and spacing</span></span>

![<span data-ttu-id="e38c4-175">figura do espaçamento e dimensionamento do controle deslizante recomendado</span><span class="sxs-lookup"><span data-stu-id="e38c4-175">figure of recommended slider sizing and spacing</span></span> ](images/ctrl-sliders-image7.png)

<span data-ttu-id="e38c4-176">Dimensionamento e espaçamento recomendados para controles deslizantes.</span><span class="sxs-lookup"><span data-stu-id="e38c4-176">Recommended sizing and spacing for sliders.</span></span>

## <a name="labels"></a><span data-ttu-id="e38c4-177">Rótulos</span><span class="sxs-lookup"><span data-stu-id="e38c4-177">Labels</span></span>

### <a name="slider-labels"></a><span data-ttu-id="e38c4-178">Rótulos de controle deslizante</span><span class="sxs-lookup"><span data-stu-id="e38c4-178">Slider labels</span></span>

-   <span data-ttu-id="e38c4-179">Use um rótulo de texto estático que termine com dois-pontos ou um rótulo de caixa de grupo sem pontuação final.</span><span class="sxs-lookup"><span data-stu-id="e38c4-179">Use a static text label ending with a colon, or a group box label with no ending punctuation.</span></span>
-   <span data-ttu-id="e38c4-180">Atribua uma chave de acesso exclusiva para cada rótulo.</span><span class="sxs-lookup"><span data-stu-id="e38c4-180">Assign a unique access key to each label.</span></span> <span data-ttu-id="e38c4-181">Para obter diretrizes de atribuição, consulte [teclado](inter-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="e38c4-181">For assignment guidelines, see [Keyboard](inter-keyboard.md).</span></span>
-   <span data-ttu-id="e38c4-182">Use a capitalização com estilo de frase.</span><span class="sxs-lookup"><span data-stu-id="e38c4-182">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="e38c4-183">Posicione o rótulo do controle deslizante à esquerda do controle deslizante ou acima e alinhado com a borda esquerda do controle deslizante (ou seu identificador de intervalo esquerdo, se presente).</span><span class="sxs-lookup"><span data-stu-id="e38c4-183">Position the slider label either to the left of the slider, or above and aligned with the left edge of the slider (or its left range identifier, if present).</span></span>

### <a name="range-labels"></a><span data-ttu-id="e38c4-184">Rótulos de intervalo</span><span class="sxs-lookup"><span data-stu-id="e38c4-184">Range labels</span></span>

-   <span data-ttu-id="e38c4-185">Rotule as duas extremidades do intervalo do controle deslizante, a menos que uma orientação vertical torne isso desnecessário.</span><span class="sxs-lookup"><span data-stu-id="e38c4-185">Label the two ends of the slider range, unless a vertical orientation makes this unnecessary.</span></span>
-   <span data-ttu-id="e38c4-186">Use somente o Word, se possível, para cada rótulo.</span><span class="sxs-lookup"><span data-stu-id="e38c4-186">Use only word, if possible, for each label.</span></span>
-   <span data-ttu-id="e38c4-187">Não use pontuação final.</span><span class="sxs-lookup"><span data-stu-id="e38c4-187">Don't use ending punctuation.</span></span>
-   <span data-ttu-id="e38c4-188">Certifique-se de que esses rótulos sejam descritivos e paralelos.</span><span class="sxs-lookup"><span data-stu-id="e38c4-188">Make sure these labels are descriptive and parallel.</span></span> <span data-ttu-id="e38c4-189">Exemplos: Máximo/Mínimo, Mais/Menos, Baixo/Alto (altura), Baixo/Alto (som).</span><span class="sxs-lookup"><span data-stu-id="e38c4-189">Examples: Maximum/Minimum, More/Less, Low/High, Soft/Loud.</span></span>
-   <span data-ttu-id="e38c4-190">Use a capitalização com estilo de frase.</span><span class="sxs-lookup"><span data-stu-id="e38c4-190">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="e38c4-191">Não atribua chaves de acesso.</span><span class="sxs-lookup"><span data-stu-id="e38c4-191">Don't assign access keys.</span></span>

### <a name="value-labels"></a><span data-ttu-id="e38c4-192">Rótulos de valor</span><span class="sxs-lookup"><span data-stu-id="e38c4-192">Value labels</span></span>

-   <span data-ttu-id="e38c4-193">Se você precisar de um rótulo de valor, mostre-o abaixo do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="e38c4-193">If you need a value label, display it below the slider.</span></span>
-   <span data-ttu-id="e38c4-194">Centralize o texto em relação ao controle e inclua as unidades (como pixels).</span><span class="sxs-lookup"><span data-stu-id="e38c4-194">Center the text relative to the control and include the units (such as pixels).</span></span>

    ![<span data-ttu-id="e38c4-195">figura do rótulo centralizado sob o controle deslizante</span><span class="sxs-lookup"><span data-stu-id="e38c4-195">figure of label centered under the slider</span></span> ](images/ctrl-sliders-image8.png)

    <span data-ttu-id="e38c4-196">Neste exemplo, o rótulo do valor é centralizado sob o controle deslizante e inclui as unidades.</span><span class="sxs-lookup"><span data-stu-id="e38c4-196">In this example, the value label is centered under the slider and includes the units.</span></span>

## <a name="documentation"></a><span data-ttu-id="e38c4-197">Documentação</span><span class="sxs-lookup"><span data-stu-id="e38c4-197">Documentation</span></span>

<span data-ttu-id="e38c4-198">Ao fazer referência a controles deslizantes:</span><span class="sxs-lookup"><span data-stu-id="e38c4-198">When referring to sliders:</span></span>

-   <span data-ttu-id="e38c4-199">Use o texto exato do rótulo, incluindo sua capitalização e inclua o controle deslizante de palavra.</span><span class="sxs-lookup"><span data-stu-id="e38c4-199">Use the exact label text, including its capitalization, and include the word slider.</span></span> <span data-ttu-id="e38c4-200">Não inclua a tecla de acesso sublinhado ou dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="e38c4-200">Don't include the access key underscore or colon.</span></span>
-   <span data-ttu-id="e38c4-201">Para descrever a interação do usuário, use mover.</span><span class="sxs-lookup"><span data-stu-id="e38c4-201">To describe user interaction, use move.</span></span>
-   <span data-ttu-id="e38c4-202">Quando possível, formate o rótulo usando texto em negrito.</span><span class="sxs-lookup"><span data-stu-id="e38c4-202">When possible, format the label using bold text.</span></span> <span data-ttu-id="e38c4-203">Caso contrário, coloque o rótulo entre aspas somente se necessário para evitar confusão.</span><span class="sxs-lookup"><span data-stu-id="e38c4-203">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="e38c4-204">Exemplo: para aumentar a resolução da tela, mova o controle deslizante de **resolução da tela** para a direita.</span><span class="sxs-lookup"><span data-stu-id="e38c4-204">Example: To increase your screen resolution, move the **Screen resolution** slider to the right.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e38c4-205">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e38c4-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e38c4-206">Glossário</span><span class="sxs-lookup"><span data-stu-id="e38c4-206">Glossary</span></span>](glossary.md)
</dt> </dl>

 

 