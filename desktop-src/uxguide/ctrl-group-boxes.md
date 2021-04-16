---
title: Caixas de grupo
description: Uma caixa de grupo é um quadro retangular rotulado que circunda um conjunto de controles relacionados. Uma caixa de grupo é uma maneira de mostrar as relações visualmente; Além de, possivelmente, fornecer uma chave de acesso para um grupo de controles, ele não fornece nenhuma funcionalidade.
ms.assetid: 5b5ffb36-3ed1-44cd-af87-5cddf46c56a6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 67f930383f2d4412d30027971c6cab2bd3edcccd
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104564128"
---
# <a name="group-boxes"></a><span data-ttu-id="c462e-104">Caixas de grupo</span><span class="sxs-lookup"><span data-stu-id="c462e-104">Group Boxes</span></span>

> [!NOTE]
> <span data-ttu-id="c462e-105">Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="c462e-105">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="c462e-106">Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="c462e-106">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="c462e-107">Uma caixa de grupo é um quadro retangular rotulado que circunda um conjunto de controles relacionados.</span><span class="sxs-lookup"><span data-stu-id="c462e-107">A group box is a labeled rectangular frame that surrounds a set of related controls.</span></span> <span data-ttu-id="c462e-108">Uma caixa de grupo é uma maneira de mostrar as relações visualmente; Além de, possivelmente, fornecer uma chave de acesso para um grupo de controles, ele não fornece nenhuma funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="c462e-108">A group box is a way to show relationships visually; aside from possibly providing an access key for a group of controls, it provides no functionality.</span></span>

![<span data-ttu-id="c462e-109">captura de tela da caixa de grupo contendo caixas de seleção</span><span class="sxs-lookup"><span data-stu-id="c462e-109">screen shot of group box containing check boxes</span></span> ](images/ctrl-group-boxes-image1.png)

<span data-ttu-id="c462e-110">Uma caixa de grupo típica.</span><span class="sxs-lookup"><span data-stu-id="c462e-110">A typical group box.</span></span>

> [!Note]  
> <span data-ttu-id="c462e-111">As diretrizes relacionadas ao [layout](vis-layout.md) são apresentadas em um artigo separado.</span><span class="sxs-lookup"><span data-stu-id="c462e-111">Guidelines related to [layout](vis-layout.md) are presented in a separate article.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="c462e-112">Esse é o controle correto?</span><span class="sxs-lookup"><span data-stu-id="c462e-112">Is this the right control?</span></span>

<span data-ttu-id="c462e-113">Embora as caixas de grupo sejam um forte meio de indicar relações, a utilização delas adiciona resíduos visuais e reduz consideravelmente o espaço disponível em uma superfície.</span><span class="sxs-lookup"><span data-stu-id="c462e-113">While group boxes are a strong visual means of indicating relationships, overusing them adds visual clutter and greatly reduces the space available on a surface.</span></span> <span data-ttu-id="c462e-114">Elas são visualmente pesadas e devem ser usadas com moderação – apenas quando não há uma solução melhor.</span><span class="sxs-lookup"><span data-stu-id="c462e-114">They are visually heavy and should be used sparingly—only when there isn't a better solution.</span></span>

<span data-ttu-id="c462e-115">Uma tendência de design no Windows é uma aparência mais simples e mais limpa, eliminando linhas desnecessárias.</span><span class="sxs-lookup"><span data-stu-id="c462e-115">A design trend in Windows is a simpler, cleaner appearance by eliminating unnecessary lines.</span></span>

<span data-ttu-id="c462e-116">Para decidir se uma caixa de grupo é necessária, considere estas perguntas:</span><span class="sxs-lookup"><span data-stu-id="c462e-116">To decide whether a group box is necessary, consider these questions:</span></span>

-   <span data-ttu-id="c462e-117">**Há mais de um controle no grupo?**</span><span class="sxs-lookup"><span data-stu-id="c462e-117">**Is there more than one control in the group?**</span></span> <span data-ttu-id="c462e-118">Caso contrário, use um rótulo de texto sem formatação em vez disso.</span><span class="sxs-lookup"><span data-stu-id="c462e-118">If not, use a plain text label instead.</span></span> <span data-ttu-id="c462e-119">Uma exceção rara é usar uma caixa de grupo com um único controle para manter a consistência com outras caixas de grupo na mesma superfície.</span><span class="sxs-lookup"><span data-stu-id="c462e-119">A rare exception is to use a group box with a single control to maintain consistency with other group boxes on the same surface.</span></span>

<span data-ttu-id="c462e-120">**Incorreto:** ![ captura de tela da caixa de grupo que contém uma caixa de texto ](images/ctrl-group-boxes-image2.png)</span><span class="sxs-lookup"><span data-stu-id="c462e-120">**Incorrect:** ![screen shot of group box containing one text box ](images/ctrl-group-boxes-image2.png)</span></span>

<span data-ttu-id="c462e-121">Neste exemplo, a caixa de grupo tem apenas um único controle.</span><span class="sxs-lookup"><span data-stu-id="c462e-121">In this example, the group box has only a single control.</span></span>

-   <span data-ttu-id="c462e-122">**Os controles estão relacionados? Mostrar a relação adiciona clareza?**</span><span class="sxs-lookup"><span data-stu-id="c462e-122">**Are the controls related? Does showing the relationship add clarity?**</span></span> <span data-ttu-id="c462e-123">Caso contrário, apresente os controles separadamente fora de uma caixa de grupo.</span><span class="sxs-lookup"><span data-stu-id="c462e-123">If not, present the controls separately outside of a group box.</span></span>
-   <span data-ttu-id="c462e-124">**Todos os controles estão dentro do grupo?**</span><span class="sxs-lookup"><span data-stu-id="c462e-124">**Are all the controls inside the group?**</span></span> <span data-ttu-id="c462e-125">Nesse caso, indique a relação na superfície maior, como a caixa de diálogo pai ou a página.</span><span class="sxs-lookup"><span data-stu-id="c462e-125">If so, indicate the relationship on the larger surface, such as the parent dialog box or page.</span></span>

<span data-ttu-id="c462e-126">**Incorreto:** ![ captura de tela da caixa de grupo que contém todos os controles ](images/ctrl-group-boxes-image3.png)</span><span class="sxs-lookup"><span data-stu-id="c462e-126">**Incorrect:** ![screen shot of group box containing all controls ](images/ctrl-group-boxes-image3.png)</span></span>

<span data-ttu-id="c462e-127">Neste exemplo, todos os controles (além dos botões de confirmação) na caixa de diálogo estão dentro da caixa de grupo.</span><span class="sxs-lookup"><span data-stu-id="c462e-127">In this example, all the controls (aside from the commit buttons) in the dialog box are within the group box.</span></span>

-   <span data-ttu-id="c462e-128">**Você pode efetivamente comunicar as relações usando apenas o layout?**</span><span class="sxs-lookup"><span data-stu-id="c462e-128">**Can you effectively communicate the relationships using layout alone?**</span></span> <span data-ttu-id="c462e-129">Nesse caso, use o [layout](vis-layout.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="c462e-129">If so, use [layout](vis-layout.md) instead.</span></span> <span data-ttu-id="c462e-130">Você pode colocar controles relacionados ao lado um do outro e colocar o espaçamento adicional entre controles não relacionados.</span><span class="sxs-lookup"><span data-stu-id="c462e-130">You can place related controls next to each other and put extra spacing between unrelated controls.</span></span> <span data-ttu-id="c462e-131">Você também pode usar títulos e recuo para mostrar relações hierárquicas.</span><span class="sxs-lookup"><span data-stu-id="c462e-131">You can also use headings and indenting to show hierarchical relationships.</span></span>

![<span data-ttu-id="c462e-132">Figura de quatro ícones mostrando quatro grupos de tarefas</span><span class="sxs-lookup"><span data-stu-id="c462e-132">figure of four icons showing four groups of tasks</span></span> ](images/ctrl-group-boxes-image4.png)

<span data-ttu-id="c462e-133">Neste exemplo, layout sozinho é usado para mostrar relações de controle.</span><span class="sxs-lookup"><span data-stu-id="c462e-133">In this example, layout alone is used to show control relationships.</span></span>

-   <span data-ttu-id="c462e-134">**Você pode realmente comunicar as relações usando um separador?**</span><span class="sxs-lookup"><span data-stu-id="c462e-134">**Can you effectively communicate the relationships using a separator?**</span></span> <span data-ttu-id="c462e-135">Nesse caso, use um separador.</span><span class="sxs-lookup"><span data-stu-id="c462e-135">If so, use a separator instead.</span></span> <span data-ttu-id="c462e-136">Um separador é uma linha horizontal que unifica os controles abaixo dele.</span><span class="sxs-lookup"><span data-stu-id="c462e-136">A separator is a horizontal line that unifies the controls below it.</span></span> <span data-ttu-id="c462e-137">Os separadores fornecem uma aparência mais simples e limpa.</span><span class="sxs-lookup"><span data-stu-id="c462e-137">Separators provide a simpler, cleaner look.</span></span> <span data-ttu-id="c462e-138">No entanto, ao contrário das caixas de grupo, elas funcionam melhor quando abrangem a largura total da superfície.</span><span class="sxs-lookup"><span data-stu-id="c462e-138">However, unlike group boxes, they work best when they span the full width of the surface.</span></span>
    -   <span data-ttu-id="c462e-139">**Desenvolvedores:** Você pode implementar um separador com um retângulo esboçado com uma altura de um.</span><span class="sxs-lookup"><span data-stu-id="c462e-139">**Developers:** You can implement a separator with an etched rectangle with a height of one.</span></span>

![Captura de tela que mostra os controles de email separados por separadores de retângulo gravados.](images/ctrl-group-boxes-image5.png)

<span data-ttu-id="c462e-141">Neste exemplo, os separadores rotulados são usados para mostrar relações de controle.</span><span class="sxs-lookup"><span data-stu-id="c462e-141">In this example, labeled separators are used to show control relationships.</span></span>

![<span data-ttu-id="c462e-142">captura de tela de controles separados por separadores</span><span class="sxs-lookup"><span data-stu-id="c462e-142">screen shot of controls set apart by separators</span></span> ](images/ctrl-group-boxes-image6.png)

<span data-ttu-id="c462e-143">Neste exemplo, separadores sem rótulo são usados para mostrar relações de controle.</span><span class="sxs-lookup"><span data-stu-id="c462e-143">In this example, unlabeled separators are used to show control relationships.</span></span>

-   <span data-ttu-id="c462e-144">**Você pode realmente comunicar as relações sem texto?**</span><span class="sxs-lookup"><span data-stu-id="c462e-144">**Can you effectively communicate the relationships without text?**</span></span> <span data-ttu-id="c462e-145">Nesse caso, considere o uso de elementos gráficos, como [planos de fundo](vis-graphic.md) ou agregadores.</span><span class="sxs-lookup"><span data-stu-id="c462e-145">If so, consider using graphic elements such as [backgrounds](vis-graphic.md) or aggregators.</span></span>

## <a name="guidelines"></a><span data-ttu-id="c462e-146">Diretrizes</span><span class="sxs-lookup"><span data-stu-id="c462e-146">Guidelines</span></span>

-   <span data-ttu-id="c462e-147">**Não aninhe caixas de grupo.**</span><span class="sxs-lookup"><span data-stu-id="c462e-147">**Don't nest group boxes.**</span></span> <span data-ttu-id="c462e-148">Use layout para mostrar relações dentro de uma caixa de grupo.</span><span class="sxs-lookup"><span data-stu-id="c462e-148">Use layout to show relationships within a group box.</span></span>

<span data-ttu-id="c462e-149">**Incorreto:** ![ captura de tela de uma caixa de grupo dentro de uma caixa de grupo ](images/ctrl-group-boxes-image7.png)</span><span class="sxs-lookup"><span data-stu-id="c462e-149">**Incorrect:** ![screen shot of a group box within a group box ](images/ctrl-group-boxes-image7.png)</span></span>

<span data-ttu-id="c462e-150">Neste exemplo, as caixas de grupo aninhadas resultam em uma desordem Visual desnecessária.</span><span class="sxs-lookup"><span data-stu-id="c462e-150">In this example, the nested group boxes result in unnecessary visual clutter.</span></span>

<span data-ttu-id="c462e-151">**Correto:** ![ captura de tela dos mesmos controles dentro de uma caixa de grupo ](images/ctrl-group-boxes-image8.png)</span><span class="sxs-lookup"><span data-stu-id="c462e-151">**Correct:** ![screen shot of same controls within one group box ](images/ctrl-group-boxes-image8.png)</span></span>

<span data-ttu-id="c462e-152">Neste exemplo, a mesma relação de controle é mostrada usando o layout em vez disso.</span><span class="sxs-lookup"><span data-stu-id="c462e-152">In this example, the same control relationship is shown using layout instead.</span></span>

-   <span data-ttu-id="c462e-153">Não coloque controles em rótulos de caixa de grupo.</span><span class="sxs-lookup"><span data-stu-id="c462e-153">Don't put controls in group box labels.</span></span>
    -   <span data-ttu-id="c462e-154">**Exceção:** Você pode usar uma caixa de seleção como um rótulo de caixa de grupo se todos os controles dentro da caixa estiverem habilitados e desabilitados pela caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="c462e-154">**Exception:** You can use a check box as a group box label if all of the controls inside the box are enabled and disabled by the check box.</span></span>

<span data-ttu-id="c462e-155">**Incorreto:** ![ captura de tela da lista suspensa em um rótulo de caixa de grupo ](images/ctrl-group-boxes-image9.png)</span><span class="sxs-lookup"><span data-stu-id="c462e-155">**Incorrect:** ![screen shot of drop-down list on a group-box label ](images/ctrl-group-boxes-image9.png)</span></span>

<span data-ttu-id="c462e-156">Neste exemplo, uma lista suspensa é colocada incorretamente em uma caixa de grupo.</span><span class="sxs-lookup"><span data-stu-id="c462e-156">In this example, a drop-down list is incorrectly placed on a group box.</span></span> <span data-ttu-id="c462e-157">Este exemplo deve usar [guias](https://msdn.microsoft.com/library/windows/desktop/aa511493.aspx) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="c462e-157">This example should use [tabs](https://msdn.microsoft.com/library/windows/desktop/aa511493.aspx) instead.</span></span>

-   <span data-ttu-id="c462e-158">**Não desabilite caixas de grupo.**</span><span class="sxs-lookup"><span data-stu-id="c462e-158">**Don't disable group boxes.**</span></span> <span data-ttu-id="c462e-159">Para indicar que um grupo de controles não é aplicado no momento, desabilite todos os controles dentro da caixa de grupo, mas não a própria caixa de grupo.</span><span class="sxs-lookup"><span data-stu-id="c462e-159">To indicate that a group of controls doesn't currently apply, disable all the controls within the group box, but not the group box itself.</span></span> <span data-ttu-id="c462e-160">Essa abordagem é mais acessível e pode ser suportada consistentemente por todas as estruturas de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c462e-160">This approach is more accessible and can be supported consistently by all UI frameworks.</span></span>

## <a name="labels"></a><span data-ttu-id="c462e-161">Rótulos</span><span class="sxs-lookup"><span data-stu-id="c462e-161">Labels</span></span>

-   <span data-ttu-id="c462e-162">Rotular todas as caixas de grupo.</span><span class="sxs-lookup"><span data-stu-id="c462e-162">Label all group boxes.</span></span>
-   <span data-ttu-id="c462e-163">Não atribua uma chave de acesso ao rótulo.</span><span class="sxs-lookup"><span data-stu-id="c462e-163">Don't assign an access key to the label.</span></span> <span data-ttu-id="c462e-164">Fazer isso é desnecessário e torna mais difícil atribuir as outras chaves de acesso.</span><span class="sxs-lookup"><span data-stu-id="c462e-164">Doing so is unnecessary and makes the other access keys harder to assign.</span></span> <span data-ttu-id="c462e-165">Em vez disso, atribua chaves de acesso aos controles dentro da caixa de grupo.</span><span class="sxs-lookup"><span data-stu-id="c462e-165">Instead, assign access keys to the controls within the group box.</span></span>
    -   <span data-ttu-id="c462e-166">**Exceção:** Se uma superfície tiver muitos controles, talvez não haja chaves de acesso suficientes disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c462e-166">**Exception:** If a surface has many controls, there may not be enough access keys available.</span></span> <span data-ttu-id="c462e-167">Nesse caso, reduza o número de chaves de acesso atribuindo-as a caixas de grupo em vez dos controles dentro das caixas de grupo.</span><span class="sxs-lookup"><span data-stu-id="c462e-167">If so, reduce the number of access keys by assigning them to group boxes instead of the controls within the group boxes.</span></span>
-   <span data-ttu-id="c462e-168">Use [a capitalização no estilo de frase](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="c462e-168">Use [sentence-style capitalization](glossary.md).</span></span>
-   <span data-ttu-id="c462e-169">Escreva o rótulo usando um substantivo ou uma frase de substantivo, não como uma frase, e não use pontuação final, incluindo dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="c462e-169">Write the label using a noun or a noun phrase, not as a sentence, and use no ending punctuation, including colons.</span></span>
-   <span data-ttu-id="c462e-170">Use frases paralelas para rótulos de caixa de grupo na mesma superfície.</span><span class="sxs-lookup"><span data-stu-id="c462e-170">Use parallel phrasing for group box labels within the same surface.</span></span>
-   <span data-ttu-id="c462e-171">Mantenha os rótulos da caixa de grupo concisos.</span><span class="sxs-lookup"><span data-stu-id="c462e-171">Keep group box labels concise.</span></span> <span data-ttu-id="c462e-172">Não use o texto de instruções como rótulo.</span><span class="sxs-lookup"><span data-stu-id="c462e-172">Don't use instructional text as the label.</span></span> <span data-ttu-id="c462e-173">No entanto, você pode ter texto de instrução dentro da caixa de grupo.</span><span class="sxs-lookup"><span data-stu-id="c462e-173">You can have instructional text within the group box, however.</span></span>
-   <span data-ttu-id="c462e-174">Não repita o rótulo da caixa de grupo nos rótulos de controle dentro da caixa.</span><span class="sxs-lookup"><span data-stu-id="c462e-174">Don't repeat the group box label in control labels within the box.</span></span> <span data-ttu-id="c462e-175">Por exemplo, se a caixa de grupo for rotulada como alinhamento, Rotule os botões de opção esquerda, direita e assim por diante, não alinhamento à esquerda ou alinhamento à direita.</span><span class="sxs-lookup"><span data-stu-id="c462e-175">For example, if the group box is labeled Alignment, label the option buttons Left, Right, and so on, not Left alignment or Right alignment.</span></span>
-   <span data-ttu-id="c462e-176">Não faça referência a caixas de grupo no texto da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c462e-176">Don't refer to group boxes in user interface text.</span></span>

## <a name="documentation"></a><span data-ttu-id="c462e-177">Documentação</span><span class="sxs-lookup"><span data-stu-id="c462e-177">Documentation</span></span>

<span data-ttu-id="c462e-178">Ao fazer referência a caixas de Grupo:</span><span class="sxs-lookup"><span data-stu-id="c462e-178">When referring to group boxes:</span></span>

-   <span data-ttu-id="c462e-179">Consulte as caixas de grupo somente no programador e outras documentações técnicas.</span><span class="sxs-lookup"><span data-stu-id="c462e-179">Refer to group boxes only in programmer and other technical documentation.</span></span> <span data-ttu-id="c462e-180">Para caixa de grupo, use duas palavras em minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c462e-180">For group box, use two lowercase words.</span></span>
-   <span data-ttu-id="c462e-181">Em qualquer outro lugar, é desnecessário incluir o nome da caixa de grupo em um procedimento, a menos que uma caixa de diálogo contenha mais de uma opção com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="c462e-181">Everywhere else, it is unnecessary to include the name of the group box in a procedure unless a dialog box contains more than one option with the same name.</span></span> <span data-ttu-id="c462e-182">Nesses casos, use sob com o nome da caixa de grupo.</span><span class="sxs-lookup"><span data-stu-id="c462e-182">In such cases, use under with the group box name.</span></span>
-   <span data-ttu-id="c462e-183">Quando possível, formate o rótulo usando texto em negrito.</span><span class="sxs-lookup"><span data-stu-id="c462e-183">When possible, format the label using bold text.</span></span> <span data-ttu-id="c462e-184">Caso contrário, coloque o rótulo entre aspas somente se necessário para evitar confusão.</span><span class="sxs-lookup"><span data-stu-id="c462e-184">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="c462e-185">Exemplo: em **efeitos**, selecione **oculto**.</span><span class="sxs-lookup"><span data-stu-id="c462e-185">Example: Under **Effects**, select **Hidden**.</span></span>

 

 