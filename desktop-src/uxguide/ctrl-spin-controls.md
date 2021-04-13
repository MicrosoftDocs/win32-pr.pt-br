---
title: Controles de rotação
description: Com um controle de rotação, os usuários podem clicar nos botões de seta para alterar incrementalmente o valor dentro de sua caixa de texto numérica associada.
ms.assetid: 5f791fb9-1354-41b9-a9de-ddab35302d50
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 54ce622983e52d65fa58ef05aca783ff67ebce66
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104297869"
---
# <a name="spin-controls"></a><span data-ttu-id="c9251-103">Controles de rotação</span><span class="sxs-lookup"><span data-stu-id="c9251-103">Spin Controls</span></span>

> [!NOTE]
> <span data-ttu-id="c9251-104">Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="c9251-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="c9251-105">Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="c9251-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="c9251-106">Com um controle de rotação, os usuários podem clicar nos botões de seta para alterar incrementalmente o valor dentro de sua [caixa de texto numérica](ctrl-text-boxes.md)associada.</span><span class="sxs-lookup"><span data-stu-id="c9251-106">With a spin control, users can click arrow buttons to change incrementally the value within its associated [numeric text box](ctrl-text-boxes.md).</span></span> <span data-ttu-id="c9251-107">O termo caixa de rotação refere-se à combinação de uma caixa de texto e seu controle de rotação associado.</span><span class="sxs-lookup"><span data-stu-id="c9251-107">The term spin box refers to the combination of a text box and its associated spin control.</span></span>

![<span data-ttu-id="c9251-108">captura de tela do controle de rotação e caixa de texto</span><span class="sxs-lookup"><span data-stu-id="c9251-108">screen shot of spin control and text box</span></span> ](images/ctrl-spin-controls-image1.png)

<span data-ttu-id="c9251-109">Uma caixa de rotação típica.</span><span class="sxs-lookup"><span data-stu-id="c9251-109">A typical spin box.</span></span>

<span data-ttu-id="c9251-110">Os usuários geralmente preferem controles de rotação porque podem fazer alterações sem mover suas mãos do mouse.</span><span class="sxs-lookup"><span data-stu-id="c9251-110">Users often prefer spin controls because they can make changes without moving their hands from the mouse.</span></span> <span data-ttu-id="c9251-111">Quando o controle de rotação é emparelhado com uma caixa de texto, os usuários podem digitar ou colar a entrada diretamente na caixa de texto, portanto, o uso do controle de rotação é opcional.</span><span class="sxs-lookup"><span data-stu-id="c9251-111">When the spin control is paired with a text box, users can type or paste input directly in the text box, so use of the spin control is optional.</span></span>

<span data-ttu-id="c9251-112">Enquanto os controles de rotação são usados para entrada numérica, a entrada não precisa ser um número inteiro puro.</span><span class="sxs-lookup"><span data-stu-id="c9251-112">While spin controls are used for numeric input, the input doesn't have to be a pure whole number.</span></span> <span data-ttu-id="c9251-113">A entrada pode ser de números decimais e pode ter sinais negativos, delimitadores (como dois-pontos ou hifens) e modificadores de unidade.</span><span class="sxs-lookup"><span data-stu-id="c9251-113">The input can be decimal numbers and it can have negative signs, delimiters (such as colons or hyphens), and unit modifiers.</span></span>

> [!Note]  
> <span data-ttu-id="c9251-114">As diretrizes relacionadas às [caixas de texto](ctrl-text-boxes.md) e ao [layout](vis-layout.md) são apresentadas em artigos separados.</span><span class="sxs-lookup"><span data-stu-id="c9251-114">Guidelines related to [text boxes](ctrl-text-boxes.md) and [layout](vis-layout.md) are presented in separate articles.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="c9251-115">Esse é o controle correto?</span><span class="sxs-lookup"><span data-stu-id="c9251-115">Is this the right control?</span></span>

<span data-ttu-id="c9251-116">Para decidir, considere estas perguntas:</span><span class="sxs-lookup"><span data-stu-id="c9251-116">To decide, consider these questions:</span></span>

-   <span data-ttu-id="c9251-117">**O controle é usado para entrada numérica?**</span><span class="sxs-lookup"><span data-stu-id="c9251-117">**Is the control used for numeric input?**</span></span> <span data-ttu-id="c9251-118">Caso contrário, use outro controle, como uma [lista suspensa](/windows/desktop/uxguide/ctrl-drop) ou [controle deslizante](ctrl-sliders.md), para selecionar um conjunto fixo de valores.</span><span class="sxs-lookup"><span data-stu-id="c9251-118">If not, use another control, such as a [drop-down list](/windows/desktop/uxguide/ctrl-drop) or [slider](ctrl-sliders.md), to select from a fixed set of values.</span></span> <span data-ttu-id="c9251-119">Use barras de rolagem para rolar.</span><span class="sxs-lookup"><span data-stu-id="c9251-119">Use scroll bars for scrolling.</span></span>
-   <span data-ttu-id="c9251-120">**Os usuários acham o valor como uma quantidade relativa, não um valor numérico?**</span><span class="sxs-lookup"><span data-stu-id="c9251-120">**Do users think of the value as a relative quantity, not a numeric value?**</span></span> <span data-ttu-id="c9251-121">Nesse caso, use um controle deslizante em vez disso.</span><span class="sxs-lookup"><span data-stu-id="c9251-121">If so, use a slider instead.</span></span> <span data-ttu-id="c9251-122">Use caixas de rotação somente para valores numéricos exatos e conhecidos.</span><span class="sxs-lookup"><span data-stu-id="c9251-122">Use spin boxes only for exact, known numeric values.</span></span> <span data-ttu-id="c9251-123">Por exemplo, os usuários pensam em definir o volume de áudio como baixo ou médio, e não em definir o valor como 2 ou 5.</span><span class="sxs-lookup"><span data-stu-id="c9251-123">For example, users think about setting their audio volume to low or medium—not about setting the value to 2 or 5.</span></span>
-   <span data-ttu-id="c9251-124">**O controle está emparelhado com uma caixa de texto?**</span><span class="sxs-lookup"><span data-stu-id="c9251-124">**Is the control paired with a text box?**</span></span> <span data-ttu-id="c9251-125">Caso contrário, não use.</span><span class="sxs-lookup"><span data-stu-id="c9251-125">If not, don't use.</span></span> <span data-ttu-id="c9251-126">Controles de rotação não devem ser usados sozinhos ou com outros tipos de controles além de uma caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="c9251-126">Spin controls shouldn't be used alone or with other types of controls besides a text box.</span></span>

    <span data-ttu-id="c9251-127">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="c9251-127">**Incorrect:**</span></span>

    ![<span data-ttu-id="c9251-128">captura de tela do controle de rotação, gráfico, nenhuma caixa de texto</span><span class="sxs-lookup"><span data-stu-id="c9251-128">screen shot of spin control, graphic, no text box</span></span> ](images/ctrl-spin-controls-image2.png)

    <span data-ttu-id="c9251-129">Neste exemplo, um controle de rotação é usado para controlar um gráfico dinâmico.</span><span class="sxs-lookup"><span data-stu-id="c9251-129">In this example, a spin control is used to control a dynamic graphic.</span></span>

-   <span data-ttu-id="c9251-130">**Os intervalos de valores contíguos são válidos?**</span><span class="sxs-lookup"><span data-stu-id="c9251-130">**Are contiguous value ranges valid?**</span></span> <span data-ttu-id="c9251-131">Caso contrário, use uma lista suspensa de valores válidos em vez disso.</span><span class="sxs-lookup"><span data-stu-id="c9251-131">If not, use a drop-down list of valid values instead.</span></span>

    ![<span data-ttu-id="c9251-132">captura de tela da lista suspensa</span><span class="sxs-lookup"><span data-stu-id="c9251-132">screen shot of drop-down list</span></span> ](images/ctrl-spin-controls-image3.png)

    <span data-ttu-id="c9251-133">Neste exemplo, nem todos os números de unidade de disco são válidos, portanto, uma lista suspensa é uma opção melhor.</span><span class="sxs-lookup"><span data-stu-id="c9251-133">In this example, not all disk drive numbers are valid, so a drop-down list is a better choice.</span></span>

-   <span data-ttu-id="c9251-134">**O uso do controle de rotação é prático?**</span><span class="sxs-lookup"><span data-stu-id="c9251-134">**Is using the spin control practical?**</span></span> <span data-ttu-id="c9251-135">O uso de um controle de rotação é prático para:</span><span class="sxs-lookup"><span data-stu-id="c9251-135">Using a spin control is practical for:</span></span>

    -   <span data-ttu-id="c9251-136">Inserindo um pequeno número, normalmente abaixo de 100.</span><span class="sxs-lookup"><span data-stu-id="c9251-136">Entering a small number, typically under 100.</span></span>
    -   <span data-ttu-id="c9251-137">Fazer alterações pequenas em um valor padrão ou existente.</span><span class="sxs-lookup"><span data-stu-id="c9251-137">Making small changes to an existing or default value.</span></span>

    <span data-ttu-id="c9251-138">Embora os controles de rotação possam ser usados para qualquer entrada numérica, eles são ineficientes em situações diferentes desses.</span><span class="sxs-lookup"><span data-stu-id="c9251-138">While spin controls can be used for any numeric input, they are inefficient in situations other than these.</span></span>

-   <span data-ttu-id="c9251-139">**O controle de rotação é útil?**</span><span class="sxs-lookup"><span data-stu-id="c9251-139">**Is the spin control helpful?**</span></span> <span data-ttu-id="c9251-140">O controle é usado em um contexto em que os usuários provavelmente estão usando o mouse?</span><span class="sxs-lookup"><span data-stu-id="c9251-140">Is the control used in a context where users are likely to be using their mouse?</span></span> <span data-ttu-id="c9251-141">Caso contrário, considere um controle de rotação opcional.</span><span class="sxs-lookup"><span data-stu-id="c9251-141">If not, consider a spin control optional.</span></span>
-   <span data-ttu-id="c9251-142">**As listas suspensas de controles irmãos são:**</span><span class="sxs-lookup"><span data-stu-id="c9251-142">**Are the sibling controls drop-down lists?**</span></span> <span data-ttu-id="c9251-143">Se houver outras listas suspensas, considere usar uma lista suspensa para fins de consistência.</span><span class="sxs-lookup"><span data-stu-id="c9251-143">If there are other drop-down lists, consider using a drop-down list for consistency.</span></span>

    ![<span data-ttu-id="c9251-144">captura de tela da caixa de diálogo com listas suspensas</span><span class="sxs-lookup"><span data-stu-id="c9251-144">screen shot of dialog box with drop-down lists</span></span> ](images/ctrl-spin-controls-image4.png)

    <span data-ttu-id="c9251-145">Neste exemplo, uma caixa de rotação pode ser usada, mas uma lista suspensa é usada para fins de consistência.</span><span class="sxs-lookup"><span data-stu-id="c9251-145">In this example, a spin box could be used, but a drop-down list is used for consistency.</span></span>

-   <span data-ttu-id="c9251-146">**Os usuários de toque ou caneta são um destino principal?**</span><span class="sxs-lookup"><span data-stu-id="c9251-146">**Are touch or pen users a primary target?**</span></span> <span data-ttu-id="c9251-147">Nesse caso, considere usar uma lista suspensa em vez disso.</span><span class="sxs-lookup"><span data-stu-id="c9251-147">If so, consider using a drop-down list instead.</span></span> <span data-ttu-id="c9251-148">Os botões de seta em um controle de rotação são muito pequenos para serem usados com eficiência com toque ou caneta.</span><span class="sxs-lookup"><span data-stu-id="c9251-148">The arrow buttons in a spin control are too small to be used efficiently with touch or a pen.</span></span>

<span data-ttu-id="c9251-149">Se um controle deslizante ou uma caixa de rotação for possível, use uma caixa de rotação se:</span><span class="sxs-lookup"><span data-stu-id="c9251-149">If a slider or a spin box is possible, use a spin box if:</span></span>

-   <span data-ttu-id="c9251-150">O espaço na tela for restrito.</span><span class="sxs-lookup"><span data-stu-id="c9251-150">Screen space is tight.</span></span>
-   <span data-ttu-id="c9251-151">É provável que um usuário prefira usar o teclado.</span><span class="sxs-lookup"><span data-stu-id="c9251-151">A user is likely to prefer using the keyboard.</span></span>

<span data-ttu-id="c9251-152">Use um controle deslizante se:</span><span class="sxs-lookup"><span data-stu-id="c9251-152">Use a slider if:</span></span>

-   <span data-ttu-id="c9251-153">Os usuários forem se beneficiar com um feedback instantâneo.</span><span class="sxs-lookup"><span data-stu-id="c9251-153">Users will benefit from instant feedback.</span></span>

## <a name="guidelines"></a><span data-ttu-id="c9251-154">Diretrizes</span><span class="sxs-lookup"><span data-stu-id="c9251-154">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="c9251-155">Geral</span><span class="sxs-lookup"><span data-stu-id="c9251-155">General</span></span>

-   <span data-ttu-id="c9251-156">**Use controles de rotação sempre que eles forem práticos e úteis.**</span><span class="sxs-lookup"><span data-stu-id="c9251-156">**Use spin controls whenever they are practical and helpful.**</span></span> <span data-ttu-id="c9251-157">Confira [esse é o controle certo?](#is-this-the-right-control)</span><span class="sxs-lookup"><span data-stu-id="c9251-157">See [Is this the right control?](#is-this-the-right-control)</span></span>

    -   <span data-ttu-id="c9251-158">**Exceção:** Para ser consistente com outras caixas de texto na mesma interface do usuário, use controles de rotação mesmo que nem sempre sejam práticos.</span><span class="sxs-lookup"><span data-stu-id="c9251-158">**Exception:** To be consistent with other text boxes on the same user interface (UI), use spin controls even if they aren't always practical.</span></span>

    <span data-ttu-id="c9251-159">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="c9251-159">**Correct:**</span></span>

    ![<span data-ttu-id="c9251-160">captura de tela dos controles de rotação mês, dia e ano</span><span class="sxs-lookup"><span data-stu-id="c9251-160">screen shot of month, day, year spin controls</span></span> ](images/ctrl-spin-controls-image5.png)

    <span data-ttu-id="c9251-161">Neste exemplo, um controle de rotação é usado com o controle Year para consistência, embora nem sempre seja prático.</span><span class="sxs-lookup"><span data-stu-id="c9251-161">In this example, a spin control is used with the year control for consistency, even though it isn't always practical.</span></span>

    <span data-ttu-id="c9251-162">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="c9251-162">**Incorrect:**</span></span>

    ![<span data-ttu-id="c9251-163">captura de tela do controle de rotação de endereço IP</span><span class="sxs-lookup"><span data-stu-id="c9251-163">screen shot of ip address spin control</span></span> ](images/ctrl-spin-controls-image6.png)

    <span data-ttu-id="c9251-164">Neste exemplo, o controle de rotação é inutilizável.</span><span class="sxs-lookup"><span data-stu-id="c9251-164">In this example, the spin control is unusable.</span></span>

-   <span data-ttu-id="c9251-165">**Sempre faça um controle de rotação do "colega" da caixa de texto.**</span><span class="sxs-lookup"><span data-stu-id="c9251-165">**Always make a spin control the "buddy" of the text box.**</span></span> <span data-ttu-id="c9251-166">Isso coloca o controle de rotação dentro da caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="c9251-166">Doing so places the spin control inside the text box.</span></span>

    <span data-ttu-id="c9251-167">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="c9251-167">**Correct:**</span></span>

    ![<span data-ttu-id="c9251-168">captura de tela do controle de rotação colocado dentro da caixa de texto</span><span class="sxs-lookup"><span data-stu-id="c9251-168">screen shot of spin control placed inside text box</span></span> ](images/ctrl-spin-controls-image7.png)

    <span data-ttu-id="c9251-169">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="c9251-169">**Incorrect:**</span></span>

    ![<span data-ttu-id="c9251-170">captura de tela do controle de rotação colocado fora da caixa de texto</span><span class="sxs-lookup"><span data-stu-id="c9251-170">screen shot of spin control placed outside text box</span></span> ](images/ctrl-spin-controls-image8.png)

    <span data-ttu-id="c9251-171">No exemplo correto, o controle de rotação é colocado dentro de sua caixa de texto associada.</span><span class="sxs-lookup"><span data-stu-id="c9251-171">In the correct example, the spin control is placed inside its associated text box.</span></span>

-   <span data-ttu-id="c9251-172">**Desabilitar um controle de rotação quando sua caixa de texto associada estiver desabilitada.**</span><span class="sxs-lookup"><span data-stu-id="c9251-172">**Disable a spin control when its associated text box is disabled.**</span></span> <span data-ttu-id="c9251-173">O controle de rotação é um método de entrada suplementar — nunca o único método de entrada.</span><span class="sxs-lookup"><span data-stu-id="c9251-173">The spin control is a supplemental input method—never the only input method.</span></span>

### <a name="values"></a><span data-ttu-id="c9251-174">Valores</span><span class="sxs-lookup"><span data-stu-id="c9251-174">Values</span></span>

-   <span data-ttu-id="c9251-175">**Defina o botão superior para aumentar o valor em uma unidade e o botão inferior para diminuir em uma unidade.**</span><span class="sxs-lookup"><span data-stu-id="c9251-175">**Define the top button to increase the value by one unit and the bottom button to decrease by one unit.**</span></span> <span data-ttu-id="c9251-176">Normalmente, a unidade é uma, mas deve ser a menor alteração comum no valor.</span><span class="sxs-lookup"><span data-stu-id="c9251-176">Typically, the unit is one, but it should be the smallest common change in value.</span></span> <span data-ttu-id="c9251-177">Idealmente, o controle de rotação deve abranger todos os valores válidos e deve ser mais conveniente do que digitar o texto.</span><span class="sxs-lookup"><span data-stu-id="c9251-177">Ideally, the spin control should cover all valid values, and it should be more convenient than typing in the text.</span></span>

    ![<span data-ttu-id="c9251-178">captura de tela do controle de rotação ' margens '</span><span class="sxs-lookup"><span data-stu-id="c9251-178">screen shot of 'margins' spin control</span></span> ](images/ctrl-spin-controls-image9.png)

    <span data-ttu-id="c9251-179">Neste exemplo, clicar em um controle de rotação altera os valores por 0,1, que é a menor alteração comum no valor.</span><span class="sxs-lookup"><span data-stu-id="c9251-179">In this example, clicking a spin control changes the values by .1, which is the smallest common change in value.</span></span> <span data-ttu-id="c9251-180">O uso de uma unidade menor abordaria o intervalo de valores válidos, mas tornaria os controles de rotação inutilizáveis.</span><span class="sxs-lookup"><span data-stu-id="c9251-180">Using a smaller unit would cover the range of valid values but make the spin controls unusable.</span></span>

-   <span data-ttu-id="c9251-181">**Use o controle de rotação para limitar a entrada a valores válidos.**</span><span class="sxs-lookup"><span data-stu-id="c9251-181">**Use the spin control to limit input to valid values.**</span></span> <span data-ttu-id="c9251-182">O uso de um controle de rotação nunca deve resultar em um valor incorreto.</span><span class="sxs-lookup"><span data-stu-id="c9251-182">Using a spin control should never result in an incorrect value.</span></span>
-   <span data-ttu-id="c9251-183">**No final de um intervalo de valores válidos, reinicie o intervalo.**</span><span class="sxs-lookup"><span data-stu-id="c9251-183">**At the end of a range of valid values, restart the range.**</span></span> <span data-ttu-id="c9251-184">A metáfora do controle de rotação é que o usuário está girando uma roda de valores, portanto, esse comportamento semelhante a roda.</span><span class="sxs-lookup"><span data-stu-id="c9251-184">The spin control metaphor is that the user is spinning a wheel of values, hence this wheel-like behavior.</span></span>
    -   <span data-ttu-id="c9251-185">**Exceção:** Não reinicie o intervalo se o valor resultante estiver certo de estar incorreto.</span><span class="sxs-lookup"><span data-stu-id="c9251-185">**Exception:** Don't restart the range if the resulting value is certain to be incorrect.</span></span>

        ![<span data-ttu-id="c9251-186">captura de tela do controle de rotação ' número de cópias '</span><span class="sxs-lookup"><span data-stu-id="c9251-186">screen shot of 'number of copies' spin control</span></span> ](images/ctrl-spin-controls-image10.png)

        <span data-ttu-id="c9251-187">Neste exemplo, clicar no botão de seta para baixo não reinicia o intervalo (acessando o valor máximo) porque esse valor está certo para estar incorreto.</span><span class="sxs-lookup"><span data-stu-id="c9251-187">In this example, clicking the down arrow button doesn't restart the range (by going to the maximum value) because that value is certain to be incorrect.</span></span>

-   <span data-ttu-id="c9251-188">**Use texto em vez de valores numéricos especiais.**</span><span class="sxs-lookup"><span data-stu-id="c9251-188">**Use text instead of special numeric values.**</span></span> <span data-ttu-id="c9251-189">Permitir que os usuários girem para esses valores especiais em vez de precisarem conhecê-los e digitá-los.</span><span class="sxs-lookup"><span data-stu-id="c9251-189">Allow users to spin to these special values instead of having to know them and type them in.</span></span>

    ![<span data-ttu-id="c9251-190">captura de tela do controle de rotação ' suspender após (nunca) '</span><span class="sxs-lookup"><span data-stu-id="c9251-190">screen shot of 'sleep after (never)' spin control</span></span> ](images/ctrl-spin-controls-image11.png)

    <span data-ttu-id="c9251-191">Neste exemplo, nunca é um valor especial, mas os usuários podem girar para ele.</span><span class="sxs-lookup"><span data-stu-id="c9251-191">In this example, Never is a special value but users can spin to it.</span></span>

-   <span data-ttu-id="c9251-192">**Se o valor tiver delimitadores, a caixa de texto associada deverá ter vários pontos de foco de entrada.**</span><span class="sxs-lookup"><span data-stu-id="c9251-192">**If the value has delimiters, the associated text box should have multiple input focus points.**</span></span> <span data-ttu-id="c9251-193">Isso permite que os segmentos numéricos sejam manipulados individualmente.</span><span class="sxs-lookup"><span data-stu-id="c9251-193">Doing so allows the numeric segments to be manipulated individually.</span></span>

    ![<span data-ttu-id="c9251-194">captura de tela do controle de rotação de tempo, minutos selecionados</span><span class="sxs-lookup"><span data-stu-id="c9251-194">screen shot of time spin control, minutes selected</span></span> ](images/ctrl-spin-controls-image12.png)

    <span data-ttu-id="c9251-195">Neste exemplo, o controle de rotação afeta os valores de horas, minutos, segundos e A.M./P.M. – o que tiver o foco.</span><span class="sxs-lookup"><span data-stu-id="c9251-195">In this example, the spin control affects the values for hours, minutes, seconds, and A.M./P.M.—whichever has the focus.</span></span>

-   <span data-ttu-id="c9251-196">**Se o valor tiver unidades, use o controle de rotação para alterar essas unidades também.**</span><span class="sxs-lookup"><span data-stu-id="c9251-196">**If the value has units, use the spin control to change those units as well.**</span></span>

    ![<span data-ttu-id="c9251-197">captura de tela do controle de rotação de tempo, ' a.m. '</span><span class="sxs-lookup"><span data-stu-id="c9251-197">screen shot of time spin control, 'a.m.'</span></span> <span data-ttu-id="c9251-198">selecionado</span><span class="sxs-lookup"><span data-stu-id="c9251-198">selected</span></span> ](images/ctrl-spin-controls-image13.png)

    <span data-ttu-id="c9251-199">Neste exemplo, o controle de rotação pode ser usado para alterar as unidades.</span><span class="sxs-lookup"><span data-stu-id="c9251-199">In this example, the spin control can be used to change units.</span></span>

## <a name="labels"></a><span data-ttu-id="c9251-200">Rótulos</span><span class="sxs-lookup"><span data-stu-id="c9251-200">Labels</span></span>

-   <span data-ttu-id="c9251-201">Aplique as diretrizes de [rotulamento da caixa de texto](ctrl-text-boxes.md) para rotular a caixa de texto associada.</span><span class="sxs-lookup"><span data-stu-id="c9251-201">Apply the [text box labeling](ctrl-text-boxes.md) guidelines to label the associated text box.</span></span> <span data-ttu-id="c9251-202">Os controles de rotação nunca são rotulados diretamente.</span><span class="sxs-lookup"><span data-stu-id="c9251-202">Spin controls are never labeled directly.</span></span>

## <a name="documentation"></a><span data-ttu-id="c9251-203">Documentação</span><span class="sxs-lookup"><span data-stu-id="c9251-203">Documentation</span></span>

<span data-ttu-id="c9251-204">Ao fazer referência a controles de rotação:</span><span class="sxs-lookup"><span data-stu-id="c9251-204">When referring to spin controls:</span></span>

-   <span data-ttu-id="c9251-205">Não consulte os controles de rotação na documentação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c9251-205">Don't refer to spin controls in user documentation.</span></span> <span data-ttu-id="c9251-206">Em vez disso, consulte o rótulo da caixa de texto associada.</span><span class="sxs-lookup"><span data-stu-id="c9251-206">Instead, refer to the label of the associated text box.</span></span>
-   <span data-ttu-id="c9251-207">Consulte controles de rotação e caixas de rotação somente em programação e outras documentações técnicas.</span><span class="sxs-lookup"><span data-stu-id="c9251-207">Refer to spin controls and spin boxes only in programming and other technical documentation.</span></span>

<span data-ttu-id="c9251-208">Exemplo: na caixa **Data** , digite ou selecione a parte da data que você deseja alterar.</span><span class="sxs-lookup"><span data-stu-id="c9251-208">Example: In the **Date** box, type or select the part of the date you want to change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9251-209">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9251-209">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9251-210">Glossário</span><span class="sxs-lookup"><span data-stu-id="c9251-210">Glossary</span></span>](glossary.md)
</dt> </dl>

 

 