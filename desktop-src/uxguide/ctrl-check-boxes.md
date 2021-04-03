---
title: Caixas de seleção
description: Com uma caixa de seleção, os usuários tomarão uma decisão entre duas opções claramente opostas.
ms.assetid: 7c39987d-807b-41c1-9788-65c3d468b976
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 7a175893b2dfab2999ce37e3f00395d881f03973
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103930062"
---
# <a name="check-boxes"></a><span data-ttu-id="413f0-103">Caixas de seleção</span><span class="sxs-lookup"><span data-stu-id="413f0-103">Check Boxes</span></span>

> [!NOTE]
> <span data-ttu-id="413f0-104">Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="413f0-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="413f0-105">Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="413f0-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="413f0-106">Com uma caixa de seleção, os usuários tomarão uma decisão entre duas opções claramente opostas.</span><span class="sxs-lookup"><span data-stu-id="413f0-106">With a check box, users make a decision between two clearly opposite choices.</span></span> <span data-ttu-id="413f0-107">O rótulo da caixa de seleção indica o estado selecionado, enquanto o significado do estado limpo deve ser o oposto não ambíguo do estado selecionado.</span><span class="sxs-lookup"><span data-stu-id="413f0-107">The check box label indicates the selected state, whereas the meaning of the cleared state must be the unambiguous opposite of the selected state.</span></span> <span data-ttu-id="413f0-108">Consequentemente, as **caixas de seleção devem ser usadas apenas para ativar ou desativar uma opção ou para selecionar ou desmarcar um item.**</span><span class="sxs-lookup"><span data-stu-id="413f0-108">Consequently, **check boxes should be used only to toggle an option on or off or to select or deselect an item.**</span></span>

![<span data-ttu-id="413f0-109">captura de tela de uma das quatro caixas de seleção selecionadas</span><span class="sxs-lookup"><span data-stu-id="413f0-109">screen shot of one of four check boxes selected</span></span> ](images/ctrl-check-boxes-image1.png)

<span data-ttu-id="413f0-110">Um grupo típico de caixas de seleção.</span><span class="sxs-lookup"><span data-stu-id="413f0-110">A typical group of check boxes.</span></span>

> [!Note]  
> <span data-ttu-id="413f0-111">As diretrizes relacionadas ao [layout](vis-layout.md) são apresentadas em um artigo separado.</span><span class="sxs-lookup"><span data-stu-id="413f0-111">Guidelines related to [layout](vis-layout.md) are presented in a separate article.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="413f0-112">Esse é o controle correto?</span><span class="sxs-lookup"><span data-stu-id="413f0-112">Is this the right control?</span></span>

<span data-ttu-id="413f0-113">Para decidir, considere estas perguntas:</span><span class="sxs-lookup"><span data-stu-id="413f0-113">To decide, consider these questions:</span></span>

-   <span data-ttu-id="413f0-114">**A caixa de seleção é usada para ativar ou desativar uma opção ou para selecionar ou desmarcar um item?**</span><span class="sxs-lookup"><span data-stu-id="413f0-114">**Is the check box used to toggle an option on or off or to select or deselect an item?**</span></span> <span data-ttu-id="413f0-115">Se não, use outro controle.</span><span class="sxs-lookup"><span data-stu-id="413f0-115">If not, use another control.</span></span>
-   <span data-ttu-id="413f0-116">**Os Estados selecionado e limpo são opostos claros e não ambíguos?**</span><span class="sxs-lookup"><span data-stu-id="413f0-116">**Are the selected and cleared states clear and unambiguous opposites?**</span></span> <span data-ttu-id="413f0-117">Caso contrário, use [botões de opção](ctrl-radio-buttons.md) ou uma [lista suspensa](/windows/desktop/uxguide/ctrl-drop) para que você possa rotular os Estados de forma independente.</span><span class="sxs-lookup"><span data-stu-id="413f0-117">If not, use [radio buttons](ctrl-radio-buttons.md) or a [drop-down list](/windows/desktop/uxguide/ctrl-drop) so that you can label the states independently.</span></span>
-   <span data-ttu-id="413f0-118">**Quando usado em um grupo, o grupo consiste em opções independentes, das quais os usuários podem escolher zero ou mais?**</span><span class="sxs-lookup"><span data-stu-id="413f0-118">**When used in a group, does the group comprise independent choices, from which users may choose zero or more?**</span></span> <span data-ttu-id="413f0-119">Caso contrário, considere os controles para as opções dependentes, como botões de opção e [exibições de árvore da caixa de seleção](ctrl-tree-views.md).</span><span class="sxs-lookup"><span data-stu-id="413f0-119">If not, consider controls for dependent choices, such as radio buttons and [check box tree views](ctrl-tree-views.md).</span></span>
-   <span data-ttu-id="413f0-120">**Quando usado em um grupo, o grupo é composto por opções dependentes, das quais os usuários devem escolher um ou mais?**</span><span class="sxs-lookup"><span data-stu-id="413f0-120">**When used in a group, does the group comprise dependent choices, from which users must choose one or more?**</span></span> <span data-ttu-id="413f0-121">Nesse caso, use um grupo de caixas de seleção e manipule o erro quando nenhuma das opções estiver selecionada.</span><span class="sxs-lookup"><span data-stu-id="413f0-121">If so, use a group of check boxes and handle the error when none of the options are selected.</span></span>
-   <span data-ttu-id="413f0-122">**O número de opções em um grupo é de 10 ou menos?**</span><span class="sxs-lookup"><span data-stu-id="413f0-122">**Is the number of options in a group 10 or fewer?**</span></span> <span data-ttu-id="413f0-123">Como o espaço da tela usado é proporcional ao número de opções, mantenha o número de caixas de seleção para 10 ou menos.</span><span class="sxs-lookup"><span data-stu-id="413f0-123">Since the screen space used is proportional to the number of options, keep the number of check boxes to 10 or fewer.</span></span> <span data-ttu-id="413f0-124">Para obter mais de 10 opções, use uma [lista de caixas de seleção](ctrl-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="413f0-124">For more than 10 options, use a [check box list](ctrl-list-boxes.md).</span></span>
-   <span data-ttu-id="413f0-125">**Um botão de opção seria uma opção melhor?**</span><span class="sxs-lookup"><span data-stu-id="413f0-125">**Would a radio button be a better choice?**</span></span> <span data-ttu-id="413f0-126">Onde as caixas de seleção são adequadas apenas para ativar ou desativar uma opção, os botões de opção podem ser usados para opções completamente diferentes.</span><span class="sxs-lookup"><span data-stu-id="413f0-126">Where check boxes are suitable only for turning an option on or off, radio buttons can be used for completely different options.</span></span> <span data-ttu-id="413f0-127">Se ambas as soluções forem possíveis:</span><span class="sxs-lookup"><span data-stu-id="413f0-127">If both solutions are possible:</span></span>
    -   <span data-ttu-id="413f0-128">Use botões de opção se o significado da caixa de seleção desmarcada não for completamente óbvio.</span><span class="sxs-lookup"><span data-stu-id="413f0-128">Use radio buttons if the meaning of the cleared check box isn't completely obvious.</span></span>

        <span data-ttu-id="413f0-129">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="413f0-129">**Incorrect:**</span></span>

        ![<span data-ttu-id="413f0-130">captura de tela de uma caixa de seleção rotulada paisagem</span><span class="sxs-lookup"><span data-stu-id="413f0-130">screen shot of one check box labeled landscape</span></span> ](images/ctrl-check-boxes-image2.png)

        <span data-ttu-id="413f0-131">Neste exemplo, a escolha oposta da paisagem não é clara, portanto, a caixa de seleção não é uma boa opção.</span><span class="sxs-lookup"><span data-stu-id="413f0-131">In this example, the opposite choice from Landscape isn't clear, so the check box isn't a good choice.</span></span>

        <span data-ttu-id="413f0-132">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="413f0-132">**Correct:**</span></span>

        ![<span data-ttu-id="413f0-133">captura de tela de dois botões de opção</span><span class="sxs-lookup"><span data-stu-id="413f0-133">screen shot of two radio buttons</span></span> ](images/ctrl-check-boxes-image3.png)

        <span data-ttu-id="413f0-134">Neste exemplo, as opções não são opostas, portanto, os botões de opção são a melhor opção.</span><span class="sxs-lookup"><span data-stu-id="413f0-134">In this example, the choices are not opposites so radio buttons are the better choice.</span></span>

    -   <span data-ttu-id="413f0-135">Use botões de opção em páginas de assistente para tornar as alternativas desclaradas, mesmo que uma caixa de seleção seja aceitável de outra forma.</span><span class="sxs-lookup"><span data-stu-id="413f0-135">Use radio buttons on wizard pages to make the alternatives clear, even if a check box is otherwise acceptable.</span></span>
    -   <span data-ttu-id="413f0-136">Use botões de opção se você tiver espaço de tela suficiente e as opções forem importantes o suficiente para ser um bom uso desse espaço de tela.</span><span class="sxs-lookup"><span data-stu-id="413f0-136">Use radio buttons if you have enough screen space and the options are important enough to be a good use of that screen space.</span></span> <span data-ttu-id="413f0-137">Caso contrário, use uma caixa de seleção ou uma lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="413f0-137">Otherwise, use a check box or a drop-down list.</span></span>

        <span data-ttu-id="413f0-138">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="413f0-138">**Incorrect:**</span></span>

        ![<span data-ttu-id="413f0-139">captura de tela de botões Mostrar e não mostrar taxa</span><span class="sxs-lookup"><span data-stu-id="413f0-139">screen shot of show and don't show ratio buttons</span></span> ](images/ctrl-check-boxes-image4.png)

        <span data-ttu-id="413f0-140">Neste exemplo, as opções não são importantes o suficiente para usar botões de opção.</span><span class="sxs-lookup"><span data-stu-id="413f0-140">In this example, the options aren't important enough to use radio buttons.</span></span>

        <span data-ttu-id="413f0-141">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="413f0-141">**Correct:**</span></span>

        ![<span data-ttu-id="413f0-142">captura de tela de caixa de seleção com não mostrar mensagem</span><span class="sxs-lookup"><span data-stu-id="413f0-142">screen shot of check box with don't show message</span></span> ](images/ctrl-check-boxes-image5.png)

        <span data-ttu-id="413f0-143">Neste exemplo, uma caixa de seleção é um uso eficiente do espaço da tela para essa opção de periférico.</span><span class="sxs-lookup"><span data-stu-id="413f0-143">In this example, a check box is an efficient use of screen space for this peripheral option.</span></span>

-   <span data-ttu-id="413f0-144">Use uma caixa de seleção se houver outras caixas de seleção na janela.</span><span class="sxs-lookup"><span data-stu-id="413f0-144">Use a check box if there other check boxes on the window.</span></span>
-   <span data-ttu-id="413f0-145">**A opção apresenta uma opção de programa, em vez de dados?**</span><span class="sxs-lookup"><span data-stu-id="413f0-145">**Does the option present a program option, rather than data?**</span></span> <span data-ttu-id="413f0-146">Os valores da opção não devem ser baseados em contexto ou outros dados.</span><span class="sxs-lookup"><span data-stu-id="413f0-146">The option's values shouldn't be based on context or other data.</span></span> <span data-ttu-id="413f0-147">Para dados, use uma lista de caixas de seleção ou uma [lista de seleção múltipla](ctrl-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="413f0-147">For data, use a check box list or [multiple-selection list](ctrl-list-boxes.md).</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="413f0-148">Padrões de uso</span><span class="sxs-lookup"><span data-stu-id="413f0-148">Usage patterns</span></span>

<span data-ttu-id="413f0-149">As caixas de seleção têm vários padrões de uso:</span><span class="sxs-lookup"><span data-stu-id="413f0-149">Check boxes have several usage patterns:</span></span>



|                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="413f0-150">**Uma opção individual** Uma única caixa de seleção é usada para selecionar uma opção individual.</span><span class="sxs-lookup"><span data-stu-id="413f0-150">**An individual choice** A single check box is used to select an individual choice.</span></span> <br/>                                                                                                             | ![<span data-ttu-id="413f0-151">captura de tela de uma caixa de seleção com o rótulo lembrar-me</span><span class="sxs-lookup"><span data-stu-id="413f0-151">screen shot of one check box with remind me label</span></span> ](images/ctrl-check-boxes-image6.png)<br/> <span data-ttu-id="413f0-152">Uma única caixa de seleção é usada para uma escolha individual.</span><span class="sxs-lookup"><span data-stu-id="413f0-152">A single check box is used for an individual choice.</span></span><br/>                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="413f0-153">**Opções independentes (zero ou mais)** Um grupo de caixas de seleção é usado para selecionar de um conjunto de zero ou mais opções.</span><span class="sxs-lookup"><span data-stu-id="413f0-153">**Independent choices (zero or more)** A group of check boxes is used to select from a set of zero or more choices.</span></span><br/>                                                                              | <span data-ttu-id="413f0-154">ao contrário dos controles de seleção única, como [botões de opção](ctrl-radio-buttons.md), os usuários podem selecionar qualquer combinação de opções em um grupo de caixas de seleção.</span><span class="sxs-lookup"><span data-stu-id="413f0-154">unlike single-selection controls such as [radio buttons](ctrl-radio-buttons.md), users can select any combination of options in a group of check boxes.</span></span><br/> <span data-ttu-id="413f0-155">![captura de tela de duas das três caixas de seleção selecionadas ](images/ctrl-check-boxes-image7.png)</span><span class="sxs-lookup"><span data-stu-id="413f0-155">![screen shot of two of three check boxes selected ](images/ctrl-check-boxes-image7.png)</span></span><br/> <span data-ttu-id="413f0-156">Um grupo de caixas de seleção é usado para escolhas independentes.</span><span class="sxs-lookup"><span data-stu-id="413f0-156">A group of check boxes is used for independent choices.</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="413f0-157">**Opções dependentes (um ou mais)** Um grupo de caixas de seleção também pode ser usado para selecionar de um conjunto de uma ou mais opções.</span><span class="sxs-lookup"><span data-stu-id="413f0-157">**Dependent choices (one or more)** A group of check boxes can also be used to select from a set of one or more choices.</span></span><br/>                                                                         | <span data-ttu-id="413f0-158">**talvez seja necessário representar uma seleção de uma ou mais opções dependentes**.</span><span class="sxs-lookup"><span data-stu-id="413f0-158">**you may need to represent a selection of one or more dependent choices**.</span></span> <span data-ttu-id="413f0-159">como o Microsoft? Windows não tem um controle que dá suporte diretamente a esse tipo de entrada, a melhor solução é usar um grupo de caixas de seleção e manipular o erro quando nenhuma das opções estiver selecionada.</span><span class="sxs-lookup"><span data-stu-id="413f0-159">because microsoft?windows doesn't have a control that directly supports this type of input, the best solution is to use a group of check boxes and handle the error when none of the options are selected.</span></span><br/> <span data-ttu-id="413f0-160">![captura de tela de uma das duas caixas de seleção selecionadas ](images/ctrl-check-boxes-image8.png)</span><span class="sxs-lookup"><span data-stu-id="413f0-160">![screen shot of one of two check boxes selected ](images/ctrl-check-boxes-image8.png)</span></span><br/> <span data-ttu-id="413f0-161">Um grupo de caixas de seleção é usado onde pelo menos um protocolo deve ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="413f0-161">A group of check boxes is used where at least one protocol must be selected.</span></span><br/> |
| <span data-ttu-id="413f0-162">**Opção mista** Além dos Estados selecionados e limpos, as caixas de seleção também têm um estado misto para seleção múltipla para indicar que a opção está definida para alguns objetos, mas não todos.</span><span class="sxs-lookup"><span data-stu-id="413f0-162">**Mixed choice** In addition to their selected and cleared states, check boxes also have a mixed state for multiple selection to indicate that the option is set for some, but not all, objects.</span></span><br/> | ![<span data-ttu-id="413f0-163">captura de tela de uma caixa de seleção azul somente leitura sólida</span><span class="sxs-lookup"><span data-stu-id="413f0-163">screen shot of a solid blue read-only check box</span></span> ](images/ctrl-check-boxes-image9.png)<br/> <span data-ttu-id="413f0-164">Uma caixa de seleção de estado misto.</span><span class="sxs-lookup"><span data-stu-id="413f0-164">A mixed-state check box.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="guidelines"></a><span data-ttu-id="413f0-165">Diretrizes</span><span class="sxs-lookup"><span data-stu-id="413f0-165">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="413f0-166">Geral</span><span class="sxs-lookup"><span data-stu-id="413f0-166">General</span></span>

-   <span data-ttu-id="413f0-167">**Caixas de seleção relacionadas ao grupo**.</span><span class="sxs-lookup"><span data-stu-id="413f0-167">**Group related check boxes**.</span></span> <span data-ttu-id="413f0-168">Combine opções relacionadas e separe as opções não relacionadas em grupos de 10 ou menos, usando vários grupos, se necessário.</span><span class="sxs-lookup"><span data-stu-id="413f0-168">Combine related options and separate unrelated options into groups of 10 or fewer, using multiple groups if necessary.</span></span>

    ![<span data-ttu-id="413f0-169">captura de tela das caixas de seleção relacionadas e não relacionadas</span><span class="sxs-lookup"><span data-stu-id="413f0-169">screen shot of related and unrelated check boxes</span></span> ](images/ctrl-check-boxes-image10.png)

    <span data-ttu-id="413f0-170">Um exemplo de grupos de opções relacionadas e independentes.</span><span class="sxs-lookup"><span data-stu-id="413f0-170">An example of groups of related, independent options.</span></span>

-   <span data-ttu-id="413f0-171">**Reconsidere o uso de caixas de grupo para organizar grupos de caixas de seleção** isso geralmente resulta em uma desordem de tela desnecessária.</span><span class="sxs-lookup"><span data-stu-id="413f0-171">**Reconsider using group boxes to organize groups of check boxes** this often results in unnecessary screen clutter.</span></span>
-   <span data-ttu-id="413f0-172">**Listar caixas de seleção em uma ordem lógica**, como agrupar opções altamente relacionadas juntos ou colocar as opções mais comuns primeiro ou seguir alguma outra progressão natural.</span><span class="sxs-lookup"><span data-stu-id="413f0-172">**List check boxes in a logical order**, such as grouping highly related options together or placing most common options first, or following some other natural progression.</span></span> <span data-ttu-id="413f0-173">A ordenação alfabética não é recomendada porque é dependente de idioma e, portanto, não é localizável.</span><span class="sxs-lookup"><span data-stu-id="413f0-173">Alphabetical ordering isn't recommended because it is language dependent, and therefore not localizable.</span></span>
-   <span data-ttu-id="413f0-174">**Alinhar caixas de seleção verticalmente, não horizontalmente**.</span><span class="sxs-lookup"><span data-stu-id="413f0-174">**Align check boxes vertically, not horizontally**.</span></span> <span data-ttu-id="413f0-175">O alinhamento horizontal é mais difícil de ler.</span><span class="sxs-lookup"><span data-stu-id="413f0-175">Horizontal alignment is harder to read.</span></span>

    <span data-ttu-id="413f0-176">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="413f0-176">**Correct:**</span></span>

    ![<span data-ttu-id="413f0-177">captura de tela das caixas de seleção alinhadas verticalmente</span><span class="sxs-lookup"><span data-stu-id="413f0-177">screen shot of check boxes aligned vertically</span></span> ](images/ctrl-check-boxes-image11.png)

    <span data-ttu-id="413f0-178">Neste exemplo, as caixas de seleção estão alinhadas corretamente.</span><span class="sxs-lookup"><span data-stu-id="413f0-178">In this example, the check boxes are correctly aligned.</span></span>

    <span data-ttu-id="413f0-179">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="413f0-179">**Incorrect:**</span></span>

    ![<span data-ttu-id="413f0-180">captura de tela das caixas de seleção alinhadas horizontalmente</span><span class="sxs-lookup"><span data-stu-id="413f0-180">screen shot of check boxes aligned horizontally</span></span> ](images/ctrl-check-boxes-image12.png)

    <span data-ttu-id="413f0-181">Neste exemplo, o alinhamento horizontal é mais difícil de ler.</span><span class="sxs-lookup"><span data-stu-id="413f0-181">In this example, the horizontal alignment is harder to read.</span></span>

-   <span data-ttu-id="413f0-182">**Não use o estado misto para representar um terceiro estado.**</span><span class="sxs-lookup"><span data-stu-id="413f0-182">**Don't use the mixed state to represent a third state.**</span></span> <span data-ttu-id="413f0-183">O estado misto é usado para indicar que uma opção está definida para alguns objetos filho, mas não todos.</span><span class="sxs-lookup"><span data-stu-id="413f0-183">The mixed state is used to indicate that an option is set for some, but not all, child objects.</span></span> <span data-ttu-id="413f0-184">Os usuários não devem ser capazes de definir um estado misto diretamente, em vez disso, o estado misto é uma reflexão dos objetos filho.</span><span class="sxs-lookup"><span data-stu-id="413f0-184">Users shouldn't be able to set a mixed state directly rather the mixed state is a reflection of the child objects.</span></span> <span data-ttu-id="413f0-185">O estado misto não é usado como um terceiro estado para um item individual.</span><span class="sxs-lookup"><span data-stu-id="413f0-185">The mixed state isn't used as a third state for an individual item.</span></span> <span data-ttu-id="413f0-186">Para representar um terceiro estado, use botões de opção ou uma lista suspensa em vez disso.</span><span class="sxs-lookup"><span data-stu-id="413f0-186">To represent a third state, use radio buttons or a drop-down list instead.</span></span>

    <span data-ttu-id="413f0-187">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="413f0-187">**Incorrect:**</span></span>

    ![<span data-ttu-id="413f0-188">captura de tela da caixa de seleção de serviço de tema azul sólido</span><span class="sxs-lookup"><span data-stu-id="413f0-188">screen shot of solid blue theme service check box</span></span> ](images/ctrl-check-boxes-image13.png)

    <span data-ttu-id="413f0-189">Neste exemplo, o estado misto deve indicar que o serviço tema não está instalado.</span><span class="sxs-lookup"><span data-stu-id="413f0-189">In this example, the mixed state is supposed to indicate that the Theme service isn't installed.</span></span>

    <span data-ttu-id="413f0-190">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="413f0-190">**Correct:**</span></span>

    ![<span data-ttu-id="413f0-191">captura de tela da lista suspensa com três opções</span><span class="sxs-lookup"><span data-stu-id="413f0-191">screen shot of drop-down list with three options</span></span> ](images/ctrl-check-boxes-image14.png)

    <span data-ttu-id="413f0-192">Neste exemplo, os usuários podem escolher entre uma lista de três opções claras.</span><span class="sxs-lookup"><span data-stu-id="413f0-192">In this example, users can choose from a list of three clear options.</span></span>

-   <span data-ttu-id="413f0-193">**Clicar em uma caixa de seleção de estado misto deve percorrer todos os Estados mistos selecionados, todos limpos e originais.**</span><span class="sxs-lookup"><span data-stu-id="413f0-193">**Clicking a mixed state check box should cycle through all selected, all cleared, and the original mixed states.**</span></span> <span data-ttu-id="413f0-194">Para Forgiveness, é importante poder restaurar o estado misto original, pois as configurações podem ser complexas ou desconhecidas para o usuário.</span><span class="sxs-lookup"><span data-stu-id="413f0-194">For forgiveness, it's important to be able to restore the original mixed state because the settings might be complex or unknown to the user.</span></span> <span data-ttu-id="413f0-195">Caso contrário, a única maneira de restaurar o estado misto com confiança seria cancelar a tarefa e começar novamente.</span><span class="sxs-lookup"><span data-stu-id="413f0-195">Otherwise, the only way to restore the mixed state with confidence would be to cancel the task and start over.</span></span>
-   <span data-ttu-id="413f0-196">**Não use as caixas de seleção como um indicador de progresso**.</span><span class="sxs-lookup"><span data-stu-id="413f0-196">**Don't use check boxes as a progress indicator**.</span></span> <span data-ttu-id="413f0-197">Em vez disso, use um controle de [indicador de progresso](progress-bars.md) .</span><span class="sxs-lookup"><span data-stu-id="413f0-197">Use a [progress indicator](progress-bars.md) control instead.</span></span>

    <span data-ttu-id="413f0-198">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="413f0-198">**Incorrect:**</span></span>

    ![<span data-ttu-id="413f0-199">captura de tela de quatro caixas de seleção mostrando progresso</span><span class="sxs-lookup"><span data-stu-id="413f0-199">screen shot of four check boxes showing progress</span></span> ](images/ctrl-check-boxes-image15.png)

    <span data-ttu-id="413f0-200">Neste exemplo, as caixas de seleção são usadas incorretamente como um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="413f0-200">In this example, check boxes are used incorrectly as a progress indicator.</span></span>

    <span data-ttu-id="413f0-201">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="413f0-201">**Correct:**</span></span>

    ![<span data-ttu-id="413f0-202">captura de tela de uma barra de progresso parcialmente preenchida</span><span class="sxs-lookup"><span data-stu-id="413f0-202">screen shot of a partially filled progress bar</span></span> ](images/ctrl-check-boxes-image16.png)

    <span data-ttu-id="413f0-203">Exemplo de uma barra de progresso típica.</span><span class="sxs-lookup"><span data-stu-id="413f0-203">Example of a typical progress bar.</span></span>

-   <span data-ttu-id="413f0-204">**Mostrar caixas de seleção desabilitadas usando o estado de seleção correto.**</span><span class="sxs-lookup"><span data-stu-id="413f0-204">**Show disabled check boxes using the correct selection state.**</span></span> <span data-ttu-id="413f0-205">Mesmo que os usuários não possam alterá-los, as caixas de seleção desativadas transmitem informações para que sejam consistentes com os resultados.</span><span class="sxs-lookup"><span data-stu-id="413f0-205">Even though users can't change them, disabled check boxes convey information so they should be consistent with results.</span></span>

    <span data-ttu-id="413f0-206">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="413f0-206">**Incorrect:**</span></span>

    ![<span data-ttu-id="413f0-207">captura de tela de uma das duas caixas de seleção esmaecidas</span><span class="sxs-lookup"><span data-stu-id="413f0-207">screen shot of one of two check boxes dimmed</span></span> ](images/ctrl-check-boxes-image17.png)

    <span data-ttu-id="413f0-208">Neste exemplo, a opção "sempre ler esta seção em voz alta" deve ser desmarcada porque a seção não é lida quando a opção está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="413f0-208">In this example, the "Always read this section aloud" option should be cleared because the section isn't read when the option is disabled.</span></span>

-   <span data-ttu-id="413f0-209">**Não use a seleção de uma caixa de seleção para**:</span><span class="sxs-lookup"><span data-stu-id="413f0-209">**Don't use the selection of a check box to**:</span></span>
    -   <span data-ttu-id="413f0-210">Executar comandos.</span><span class="sxs-lookup"><span data-stu-id="413f0-210">Perform commands.</span></span>
    -   <span data-ttu-id="413f0-211">Exiba outras janelas, como uma caixa de diálogo para coletar mais entradas.</span><span class="sxs-lookup"><span data-stu-id="413f0-211">Display other windows, such as a dialog box to gather more input.</span></span>
    -   <span data-ttu-id="413f0-212">Exibir dinamicamente outros controles relacionados ao controle selecionado (leitores de tela não podem detectar esses eventos).</span><span class="sxs-lookup"><span data-stu-id="413f0-212">Dynamically display other controls related to the selected control (screen readers cannot detect such events).</span></span>

### <a name="dont-show-this-item-again"></a><span data-ttu-id="413f0-213">Não mostrar este</span><span class="sxs-lookup"><span data-stu-id="413f0-213">Don't show this</span></span> <item> <span data-ttu-id="413f0-214">outra</span><span class="sxs-lookup"><span data-stu-id="413f0-214">again</span></span>

-   <span data-ttu-id="413f0-215">**Considere usar uma opção não mostrar esta <item> novamente para permitir que os usuários suprimem uma caixa de diálogo recorrente somente se não houver uma alternativa melhor.**</span><span class="sxs-lookup"><span data-stu-id="413f0-215">**Consider using a Don't show this <item> again option to allow users to suppress a recurring dialog box only if there isn't a better alternative.**</span></span> <span data-ttu-id="413f0-216">Tente determinar com antecedência se os usuários realmente precisam da caixa de diálogo; Se fizerem isso, sempre mostrarão a caixa de diálogo e, se não forem, eliminará a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="413f0-216">Try to determine beforehand if users really need the dialog; if they do, always show the dialog, and if they don't, eliminate the dialog.</span></span>

<span data-ttu-id="413f0-217">Para obter mais diretrizes e exemplos, consulte [caixas de diálogo](win-dialog-box.md).</span><span class="sxs-lookup"><span data-stu-id="413f0-217">For more guidelines and examples, see [Dialog Boxes](win-dialog-box.md).</span></span>

### <a name="subordinate-controls"></a><span data-ttu-id="413f0-218">Controles subordinados</span><span class="sxs-lookup"><span data-stu-id="413f0-218">Subordinate controls</span></span>

-   <span data-ttu-id="413f0-219">Coloque controles subordinados à direita ou abaixo (recuado, libere com o rótulo da caixa de seleção) a caixa de seleção e seu rótulo.</span><span class="sxs-lookup"><span data-stu-id="413f0-219">Place subordinate controls to the right of or below (indented, flush with the check box label) the check box and its label.</span></span> <span data-ttu-id="413f0-220">Termine o rótulo da caixa de seleção com dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="413f0-220">End the check box label with a colon.</span></span>

    ![<span data-ttu-id="413f0-221">captura de tela da caixa de texto abaixo do rótulo da caixa de seleção</span><span class="sxs-lookup"><span data-stu-id="413f0-221">screen shot of text box below check box label</span></span> ](images/ctrl-check-boxes-image18.png)

    <span data-ttu-id="413f0-222">Neste exemplo, a caixa de seleção e seu controle subordinado compartilham o rótulo da caixa de seleção e sua chave de acesso.</span><span class="sxs-lookup"><span data-stu-id="413f0-222">In this example, the check box and its subordinate control share the check box label and its access key.</span></span>

-   <span data-ttu-id="413f0-223">**Deixe caixas de texto editáveis e listas suspensas dependentes habilitadas se compartilharem o rótulo da caixa de seleção.**</span><span class="sxs-lookup"><span data-stu-id="413f0-223">**Leave dependent editable text boxes and drop-down lists enabled if they share the check box's label.**</span></span> <span data-ttu-id="413f0-224">Quando os usuários digitam ou colam qualquer coisa na caixa, selecione a opção correspondente automaticamente.</span><span class="sxs-lookup"><span data-stu-id="413f0-224">When users type or paste anything into the box, select the corresponding option automatically.</span></span> <span data-ttu-id="413f0-225">Fazer isso simplifica a interação.</span><span class="sxs-lookup"><span data-stu-id="413f0-225">Doing so simplifies the interaction.</span></span>

    ![<span data-ttu-id="413f0-226">captura de tela de caixas de texto de cabeçalho e rodapé</span><span class="sxs-lookup"><span data-stu-id="413f0-226">screen shot of header and footer text boxes</span></span> ](images/ctrl-check-boxes-image19.png)

    <span data-ttu-id="413f0-227">Neste exemplo, a inserção de um cabeçalho ou rodapé automaticamente seleciona a opção.</span><span class="sxs-lookup"><span data-stu-id="413f0-227">In this example, entering a header or footer automatically selects the option.</span></span>

-   <span data-ttu-id="413f0-228">Se você aninhar caixas de seleção com botões de opção ou outras caixas de seleção, **Desabilite esses controles subordinados até que a opção de alto nível seja selecionada**.</span><span class="sxs-lookup"><span data-stu-id="413f0-228">If you nest check boxes with radio buttons or other check boxes, **disable these subordinate controls until the high-level option is selected**.</span></span> <span data-ttu-id="413f0-229">Isso evita a confusão sobre o significado dos controles subordinados.</span><span class="sxs-lookup"><span data-stu-id="413f0-229">Doing so avoids confusion about the meaning of the subordinate controls.</span></span>
-   <span data-ttu-id="413f0-230">Torne os controles subordinados a uma caixa de seleção contíguas com a caixa de seleção na ordem de tabulação.</span><span class="sxs-lookup"><span data-stu-id="413f0-230">Make subordinate controls to a check box contiguous with the check box in the tab order.</span></span>
-   <span data-ttu-id="413f0-231">**Se a seleção de uma opção implica selecionar caixas de seleção subordinadas, marque explicitamente as caixas de seleção para tornar a relação clara.**</span><span class="sxs-lookup"><span data-stu-id="413f0-231">**If selecting an option implies selecting subordinate check boxes, explicitly select those check boxes to make the relationship clear.**</span></span>

    <span data-ttu-id="413f0-232">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="413f0-232">**Incorrect:**</span></span>

    ![<span data-ttu-id="413f0-233">captura de tela: botão selecionado, caixas de seleção desmarcadas</span><span class="sxs-lookup"><span data-stu-id="413f0-233">screen shot: selected button, cleared check boxes</span></span> ](images/ctrl-check-boxes-image20.png)

    <span data-ttu-id="413f0-234">Neste exemplo, as caixas de seleção subordinadas não estão selecionadas.</span><span class="sxs-lookup"><span data-stu-id="413f0-234">In this example, the subordinate check boxes aren't selected.</span></span>

    <span data-ttu-id="413f0-235">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="413f0-235">**Correct:**</span></span>

    ![<span data-ttu-id="413f0-236">captura de tela: botão selecionado, caixas de seleção selecionadas</span><span class="sxs-lookup"><span data-stu-id="413f0-236">screen shot: selected button, selected check boxes</span></span> ](images/ctrl-check-boxes-image21.png)

    <span data-ttu-id="413f0-237">Neste exemplo, as caixas de seleção subordinadas são selecionadas, tornando sua relação com a opção selecionada desmarcada.</span><span class="sxs-lookup"><span data-stu-id="413f0-237">In this example, the subordinate check boxes are selected, making their relationship to the selected option clear.</span></span>

-   <span data-ttu-id="413f0-238">**Use as caixas de seleção dependentes se as alternativas adicionarem complexidade desnecessária**.</span><span class="sxs-lookup"><span data-stu-id="413f0-238">**Use dependent check boxes if the alternatives add unnecessary complexity**.</span></span> <span data-ttu-id="413f0-239">Enquanto as caixas de seleção devem ser opções independentes, algumas vezes alternativas como botões de opção adicionam complexidade desnecessária.</span><span class="sxs-lookup"><span data-stu-id="413f0-239">While check boxes should be independent options, sometimes alternatives such as radio buttons add unnecessary complexity.</span></span>

    <span data-ttu-id="413f0-240">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="413f0-240">**Correct:**</span></span>

    ![<span data-ttu-id="413f0-241">captura de tela de botões confusos e caixas de seleção</span><span class="sxs-lookup"><span data-stu-id="413f0-241">screen shot of confusing buttons and check boxes</span></span> ](images/ctrl-check-boxes-image22.png)

    <span data-ttu-id="413f0-242">Neste exemplo, o uso de botões de opção é preciso, mas cria uma complexidade desnecessária.</span><span class="sxs-lookup"><span data-stu-id="413f0-242">In this example, the use of radio buttons is accurate, but creates unnecessary complexity.</span></span>

    <span data-ttu-id="413f0-243">**Melhor:**</span><span class="sxs-lookup"><span data-stu-id="413f0-243">**Better:**</span></span>

    ![<span data-ttu-id="413f0-244">captura de tela apenas de caixas de seleção</span><span class="sxs-lookup"><span data-stu-id="413f0-244">screen shot of check boxes only</span></span> ](images/ctrl-check-boxes-image23.png)

    <span data-ttu-id="413f0-245">Neste exemplo, o uso de caixas de seleção é mais simples e permite que os usuários se concentrem na seleção das opções desejadas em vez de em sua relação complexa.</span><span class="sxs-lookup"><span data-stu-id="413f0-245">In this example, the use of check boxes is simpler and allows users to focus on selecting the desired options instead of on their complex relationship.</span></span>

    <span data-ttu-id="413f0-246">**Importante: aplique essa diretriz somente em circunstâncias extremamente raras**, quando a exibição das dependências adicionar uma complexidade significativa sem aumentar a clareza.</span><span class="sxs-lookup"><span data-stu-id="413f0-246">**Important: Apply this guideline only in extremely rare circumstances**, when showing the dependencies adds significant complexity without adding clarity.</span></span> <span data-ttu-id="413f0-247">No exemplo anterior, é improvável que os usuários tentem escolher sobrescrito e subscrito e, se tiverem feito isso, seria fácil entender que eram opções exclusivas.</span><span class="sxs-lookup"><span data-stu-id="413f0-247">In the previous example, it is unlikely that users would attempt to choose both superscript and subscript, and if they did, it would be easy to understand that they were exclusive options.</span></span>

### <a name="default-values"></a><span data-ttu-id="413f0-248">Valores padrão</span><span class="sxs-lookup"><span data-stu-id="413f0-248">Default values</span></span>

-   <span data-ttu-id="413f0-249">Se uma caixa de seleção for para uma opção de usuário, **defina o mais seguro (para evitar a perda de dados ou acesso ao sistema), o estado mais seguro e privado por padrão.**</span><span class="sxs-lookup"><span data-stu-id="413f0-249">If a check box is for a user option, **set the safest (to prevent loss of data or system access), most secure and private state by default.**</span></span> <span data-ttu-id="413f0-250">Se não houver fatores de segurança e segurança, selecione o valor mais provável ou conveniente.</span><span class="sxs-lookup"><span data-stu-id="413f0-250">If safety and security aren't factors, select the most likely or convenient value.</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="413f0-251">Dimensionamento e espaçamento recomendados</span><span class="sxs-lookup"><span data-stu-id="413f0-251">Recommended sizing and spacing</span></span>

![<span data-ttu-id="413f0-252">figura do espaçamento e dimensionamento da caixa de seleção sugerido</span><span class="sxs-lookup"><span data-stu-id="413f0-252">figure of suggested check box sizing and spacing</span></span> ](images/ctrl-check-boxes-image24.png)

<span data-ttu-id="413f0-253">Dimensionamento e espaçamento recomendados para caixas de seleção.</span><span class="sxs-lookup"><span data-stu-id="413f0-253">Recommended sizing and spacing for check boxes.</span></span>

## <a name="labels"></a><span data-ttu-id="413f0-254">Rótulos</span><span class="sxs-lookup"><span data-stu-id="413f0-254">Labels</span></span>

<span data-ttu-id="413f0-255">**Rótulos da caixa de seleção**</span><span class="sxs-lookup"><span data-stu-id="413f0-255">**Check box labels**</span></span>

-   <span data-ttu-id="413f0-256">Rotular todas as caixas de seleção.</span><span class="sxs-lookup"><span data-stu-id="413f0-256">Label every check box.</span></span>
-   <span data-ttu-id="413f0-257">Atribua uma [chave de acesso](glossary.md) exclusiva para cada rótulo.</span><span class="sxs-lookup"><span data-stu-id="413f0-257">Assign a unique [access key](glossary.md) to each label.</span></span> <span data-ttu-id="413f0-258">Para obter diretrizes, consulte [teclado](inter-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="413f0-258">For guidelines, see [Keyboard](inter-keyboard.md).</span></span>
-   <span data-ttu-id="413f0-259">Use [a capitalização no estilo de frase](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="413f0-259">Use [sentence-style capitalization](glossary.md).</span></span>
-   <span data-ttu-id="413f0-260">Escreva o rótulo como uma frase ou uma frase imperativa e não use pontuação final.</span><span class="sxs-lookup"><span data-stu-id="413f0-260">Write the label as a phrase or an imperative sentence, and use no ending punctuation.</span></span>
    -   <span data-ttu-id="413f0-261">**Exceção:** Se um rótulo da caixa de seleção também rotular um controle subordinado que o segue, termine o rótulo com dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="413f0-261">**Exception:** If a check box label also labels a subordinate control that follows it, end the label with a colon.</span></span>
-   <span data-ttu-id="413f0-262">Escreva o rótulo para que ele descreva o estado selecionado da caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="413f0-262">Write the label so that it describes the selected state of the check box.</span></span>
-   <span data-ttu-id="413f0-263">Para um grupo de caixas de seleção, use frases paralelas e tente manter o comprimento sobre o mesmo para todos os rótulos.</span><span class="sxs-lookup"><span data-stu-id="413f0-263">For a group of check boxes, use parallel phrasing and try to keep the length about the same for all labels.</span></span>
-   <span data-ttu-id="413f0-264">Para um grupo de caixas de seleção, concentre o texto do rótulo nas diferenças entre as opções.</span><span class="sxs-lookup"><span data-stu-id="413f0-264">For a group of check boxes, focus the label text on the differences among the options.</span></span> <span data-ttu-id="413f0-265">Se todas as opções tiverem o mesmo texto introdutório, mova esse texto para o rótulo do grupo.</span><span class="sxs-lookup"><span data-stu-id="413f0-265">If all the options have the same introductory text, move that text to the group label.</span></span>
-   <span data-ttu-id="413f0-266">Use frases positivas.</span><span class="sxs-lookup"><span data-stu-id="413f0-266">Use positive phrasing.</span></span> <span data-ttu-id="413f0-267">Não formule um rótulo para que a seleção de uma caixa de seleção signifique não executar uma ação.</span><span class="sxs-lookup"><span data-stu-id="413f0-267">Don't phrase a label so that selecting a check box means not to perform an action.</span></span>

    -   <span data-ttu-id="413f0-268">**Exceção: não mostrar esta <item>** caixa de seleção novamente.</span><span class="sxs-lookup"><span data-stu-id="413f0-268">**Exception:Don't show this <item> again** check boxes.</span></span>

    <span data-ttu-id="413f0-269">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="413f0-269">**Incorrect:**</span></span>

    ![captura de tela do rótulo negativo ' desligar '](images/ctrl-check-boxes-image25.png)

    <span data-ttu-id="413f0-271">Neste exemplo, a opção não usa frases positivas.</span><span class="sxs-lookup"><span data-stu-id="413f0-271">In this example, the option doesn't use positive phrasing.</span></span>

-   <span data-ttu-id="413f0-272">Descreva apenas a opção com o rótulo.</span><span class="sxs-lookup"><span data-stu-id="413f0-272">Describe just the option with the label.</span></span> <span data-ttu-id="413f0-273">Mantenha os rótulos breves para que seja fácil consultá-los em mensagens e documentação.</span><span class="sxs-lookup"><span data-stu-id="413f0-273">Keep labels brief so it's easy to refer to them in messages and documentation.</span></span> <span data-ttu-id="413f0-274">Se a opção exigir mais explicações, forneça a explicação em um controle de [texto estático](./glossary.md) usando frases completas e pontuação final.</span><span class="sxs-lookup"><span data-stu-id="413f0-274">If the option requires further explanation, provide the explanation in a [static text](./glossary.md) control using complete sentences and ending punctuation.</span></span>

    > [!Note]
    >
    > <span data-ttu-id="413f0-275">Adicionar uma explicação a uma caixa de seleção em um grupo não significa que você precisa fornecer explicações para todas as caixas de seleção no grupo.</span><span class="sxs-lookup"><span data-stu-id="413f0-275">Adding an explanation to one check box in a group doesn't mean that you have to provide explanations for all check boxes in the group.</span></span> <span data-ttu-id="413f0-276">Forneça as informações relevantes no rótulo, se possível, e use explicações somente quando necessário.</span><span class="sxs-lookup"><span data-stu-id="413f0-276">Provide the relevant information in the label if you can, and use explanations only when necessary.</span></span> <span data-ttu-id="413f0-277">Não apenas redeclare o rótulo para fins de consistência.</span><span class="sxs-lookup"><span data-stu-id="413f0-277">Don't merely restate the label for consistency.</span></span>

     

    ![<span data-ttu-id="413f0-278">captura de tela de caixa de seleção, rótulo e descrição</span><span class="sxs-lookup"><span data-stu-id="413f0-278">screen shot of checkbox, label, and description</span></span> ](images/ctrl-check-boxes-image26.png)

    <span data-ttu-id="413f0-279">Neste exemplo, um rótulo de caixa de seleção tem um texto explicativo adicional abaixo dele.</span><span class="sxs-lookup"><span data-stu-id="413f0-279">In this example, a check box label has additional explanatory text beneath it.</span></span>

-   <span data-ttu-id="413f0-280">Se uma opção for altamente recomendável, considere adicionar "(recomendado)" ao rótulo.</span><span class="sxs-lookup"><span data-stu-id="413f0-280">If an option is strongly recommended, consider adding "(recommended)" to the label.</span></span> <span data-ttu-id="413f0-281">Certifique-se de adicionar ao rótulo de controle, não às anotações complementares.</span><span class="sxs-lookup"><span data-stu-id="413f0-281">Be sure to add to the control label, not the supplemental notes.</span></span>
-   <span data-ttu-id="413f0-282">Se você precisar usar rótulos de várias linhas, alinhe a parte superior do rótulo com a caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="413f0-282">If you must use multi-line labels, align the top of the label with the check box.</span></span>
-   <span data-ttu-id="413f0-283">Não use um controle subordinado, os valores que ele contém ou seu rótulo de unidades para criar uma frase ou frase.</span><span class="sxs-lookup"><span data-stu-id="413f0-283">Don't use a subordinate control, the values it contains, or its units label to create a sentence or phrase.</span></span> <span data-ttu-id="413f0-284">Esse tipo de design não é localizável porque a estrutura da frase varia de acordo com a linguagem.</span><span class="sxs-lookup"><span data-stu-id="413f0-284">Such a design isn't localizable because sentence structure varies with language.</span></span>

    <span data-ttu-id="413f0-285">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="413f0-285">**Incorrect:**</span></span>

    ![<span data-ttu-id="413f0-286">captura de tela de rótulo de caixa de seleção com caixa de texto</span><span class="sxs-lookup"><span data-stu-id="413f0-286">screen shot of checkbox label with text box in it</span></span> ](images/ctrl-check-boxes-image27.png)

    <span data-ttu-id="413f0-287">Neste exemplo, a caixa de texto é colocada incorretamente dentro do rótulo da caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="413f0-287">In this example, the text box is incorrectly placed inside the check box label.</span></span>

<span data-ttu-id="413f0-288">**Rótulos de grupo da caixa de seleção**</span><span class="sxs-lookup"><span data-stu-id="413f0-288">**Check box group labels**</span></span>

-   <span data-ttu-id="413f0-289">Use o rótulo de grupo para explicar a finalidade do grupo, não como fazer a seleção.</span><span class="sxs-lookup"><span data-stu-id="413f0-289">Use the group label to explain the purpose of the group, not how to make the selection.</span></span> <span data-ttu-id="413f0-290">Suponha que os usuários saibam como usar as caixas de seleção.</span><span class="sxs-lookup"><span data-stu-id="413f0-290">Assume that users know how to use check boxes.</span></span> <span data-ttu-id="413f0-291">Por exemplo, não diga "Selecione qualquer uma das opções a seguir".</span><span class="sxs-lookup"><span data-stu-id="413f0-291">For example, don't say "Select any of the following choices".</span></span>
-   <span data-ttu-id="413f0-292">Termine cada rótulo com dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="413f0-292">End each label with a colon.</span></span>
-   <span data-ttu-id="413f0-293">Não atribua uma chave de acesso ao rótulo.</span><span class="sxs-lookup"><span data-stu-id="413f0-293">Don't assign an access key to the label.</span></span> <span data-ttu-id="413f0-294">Fazer isso não é necessário e torna mais difícil atribuir as outras chaves de acesso.</span><span class="sxs-lookup"><span data-stu-id="413f0-294">Doing so isn't necessary and it makes the other access keys harder to assign.</span></span>
-   <span data-ttu-id="413f0-295">Para uma seleção de uma ou mais opções dependentes, explique o requisito no rótulo.</span><span class="sxs-lookup"><span data-stu-id="413f0-295">For a selection of one or more dependent choices, explain the requirement on the label.</span></span>

    <span data-ttu-id="413f0-296">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="413f0-296">**Correct:**</span></span>

    ![<span data-ttu-id="413f0-297">captura de tela do rótulo para dois controles: protocolos</span><span class="sxs-lookup"><span data-stu-id="413f0-297">screen shot of label for two controls: protocols</span></span> ](images/ctrl-check-boxes-image28.png)

    <span data-ttu-id="413f0-298">Neste exemplo, os usuários podem imaginar que eles só podem fazer uma seleção.</span><span class="sxs-lookup"><span data-stu-id="413f0-298">In this example, users might think that they can only make one selection.</span></span>

    <span data-ttu-id="413f0-299">**Melhor:**</span><span class="sxs-lookup"><span data-stu-id="413f0-299">**Better:**</span></span>

    ![<span data-ttu-id="413f0-300">captura de tela de rótulo: protocolos selecione um ou mais</span><span class="sxs-lookup"><span data-stu-id="413f0-300">screen shot of label: protocols select one or more</span></span> ](images/ctrl-check-boxes-image29.png)

    <span data-ttu-id="413f0-301">Neste exemplo, é claro que os usuários podem fazer mais de uma seleção.</span><span class="sxs-lookup"><span data-stu-id="413f0-301">In this example, it's clear that users can make more than one selection.</span></span>

## <a name="documentation"></a><span data-ttu-id="413f0-302">Documentação</span><span class="sxs-lookup"><span data-stu-id="413f0-302">Documentation</span></span>

<span data-ttu-id="413f0-303">Ao se referir a caixas de seleção:</span><span class="sxs-lookup"><span data-stu-id="413f0-303">When referring to check boxes:</span></span>

-   <span data-ttu-id="413f0-304">Use o texto exato do rótulo, incluindo sua capitalização, mas não inclua a tecla de acesso sublinhado ou dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="413f0-304">Use the exact label text, including its capitalization, but don't include the access key underscore or colon.</span></span> <span data-ttu-id="413f0-305">Inclua a caixa de seleção Word.</span><span class="sxs-lookup"><span data-stu-id="413f0-305">Include the word check box.</span></span>
-   <span data-ttu-id="413f0-306">Consulte uma caixa de seleção como caixa de seleção, não opção, caixa de seleção ou caixa apenas, porque a caixa sozinha é ambígua para os localizadores.</span><span class="sxs-lookup"><span data-stu-id="413f0-306">Refer to a check box as a check box, not option, checkbox, or just box, because box alone is ambiguous for localizers.</span></span>
-   <span data-ttu-id="413f0-307">Para descrever a interação do usuário, use selecionar e limpar.</span><span class="sxs-lookup"><span data-stu-id="413f0-307">To describe user interaction, use select and clear.</span></span>
-   <span data-ttu-id="413f0-308">Quando possível, formate o rótulo usando texto em negrito.</span><span class="sxs-lookup"><span data-stu-id="413f0-308">When possible, format the label using bold text.</span></span> <span data-ttu-id="413f0-309">Caso contrário, coloque o rótulo entre aspas somente se necessário para evitar confusão.</span><span class="sxs-lookup"><span data-stu-id="413f0-309">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>

    <span data-ttu-id="413f0-310">Exemplo: marque a caixa de seleção **sublinhado** .</span><span class="sxs-lookup"><span data-stu-id="413f0-310">Example: Select the **Underline** check box.</span></span>

