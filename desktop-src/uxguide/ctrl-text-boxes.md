---
title: Caixas de texto
description: Com uma caixa de texto, os usuários podem exibir, inserir ou editar um texto ou valor numérico.
ms.assetid: fb8ed262-1451-496d-a3f4-a29af39763bb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 2b5257e9772465f26815abb0f6ecbe0ff357ba4b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104506321"
---
# <a name="text-boxes"></a><span data-ttu-id="0323c-103">Caixas de texto</span><span class="sxs-lookup"><span data-stu-id="0323c-103">Text Boxes</span></span>

> [!NOTE]
> <span data-ttu-id="0323c-104">Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="0323c-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="0323c-105">Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="0323c-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="0323c-106">Com uma caixa de texto, os usuários podem exibir, inserir ou editar um texto ou valor numérico.</span><span class="sxs-lookup"><span data-stu-id="0323c-106">With a text box, users can display, enter, or edit a text or numeric value.</span></span>

![<span data-ttu-id="0323c-107">captura de tela de uma caixa de texto e rótulo típicos</span><span class="sxs-lookup"><span data-stu-id="0323c-107">screen shot of a typical text box and label</span></span> ](images/ctrl-text-boxes-image1.png)

<span data-ttu-id="0323c-108">Uma caixa de texto típica.</span><span class="sxs-lookup"><span data-stu-id="0323c-108">A typical text box.</span></span>

> [!Note]  
> <span data-ttu-id="0323c-109">As diretrizes relacionadas ao [layout](vis-layout.md), às [fontes](vis-fonts.md)e aos [balões](ctrl-balloons.md) são apresentadas em artigos separados.</span><span class="sxs-lookup"><span data-stu-id="0323c-109">Guidelines related to [layout](vis-layout.md), [fonts](vis-fonts.md), and [balloons](ctrl-balloons.md) are presented in separate articles.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="0323c-110">Esse é o controle correto?</span><span class="sxs-lookup"><span data-stu-id="0323c-110">Is this the right control?</span></span>

<span data-ttu-id="0323c-111">Para decidir, considere estas perguntas:</span><span class="sxs-lookup"><span data-stu-id="0323c-111">To decide, consider these questions:</span></span>

-   <span data-ttu-id="0323c-112">**É prático enumerar todos os valores válidos com eficiência?**</span><span class="sxs-lookup"><span data-stu-id="0323c-112">**Is it practical to enumerate all the valid values efficiently?**</span></span> <span data-ttu-id="0323c-113">Nesse caso, considere uma [lista de seleção única](ctrl-list-boxes.md), [exibição de lista](ctrl-list-views.md), [lista suspensa](/windows/desktop/uxguide/ctrl-drop), lista suspensa editável ou [controle deslizante](ctrl-sliders.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="0323c-113">If so, consider a [single-selection list](ctrl-list-boxes.md), [list view](ctrl-list-views.md), [drop-down list](/windows/desktop/uxguide/ctrl-drop), editable drop-down list, or [slider](ctrl-sliders.md) instead.</span></span>
-   <span data-ttu-id="0323c-114">**Os dados válidos são completamente irrestrito? Ou os dados válidos são restritos apenas por formato (comprimento ou tipos de caracteres restritos)?**</span><span class="sxs-lookup"><span data-stu-id="0323c-114">**Is the valid data completely unconstrained? Or is the valid data constrained only by format (constrained length or character types)?**</span></span> <span data-ttu-id="0323c-115">Nesse caso, use uma caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="0323c-115">If so, use a text box.</span></span>
-   <span data-ttu-id="0323c-116">**O valor representa um tipo de dados que tem um controle comum especializado?**</span><span class="sxs-lookup"><span data-stu-id="0323c-116">**Does the value represent a data type that has a specialized common control?**</span></span> <span data-ttu-id="0323c-117">Os exemplos incluem data, hora ou endereço IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="0323c-117">Examples include date, time, or IPv4 or IPv6 address.</span></span> <span data-ttu-id="0323c-118">Nesse caso, use o controle apropriado, como um controle de data, em vez de uma caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="0323c-118">If so, use the appropriate control, such as a date control rather than a text box.</span></span>
-   <span data-ttu-id="0323c-119">Se os dados forem numéricos:</span><span class="sxs-lookup"><span data-stu-id="0323c-119">If the data is numeric:</span></span>
    -   <span data-ttu-id="0323c-120">**Os usuários percebem a configuração como uma quantidade relativa?**</span><span class="sxs-lookup"><span data-stu-id="0323c-120">**Do users perceive the setting as a relative quantity?**</span></span> <span data-ttu-id="0323c-121">Se sim, use um controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="0323c-121">If so, use a slider.</span></span>
    -   <span data-ttu-id="0323c-122">**O usuário se beneficiaria com um feedback instantâneo sobre o efeito das alterações de configuração?**</span><span class="sxs-lookup"><span data-stu-id="0323c-122">**Would the user benefit from instant feedback on the effect of setting changes?**</span></span> <span data-ttu-id="0323c-123">Nesse caso, use um controle deslizante, possivelmente junto com uma caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="0323c-123">If so, use a slider, possibly along with a text box.</span></span> <span data-ttu-id="0323c-124">Por exemplo, os usuários podem escolher facilmente uma cor usando um controle deslizante, pois eles podem ver imediatamente o efeito das alterações nos valores de matiz, saturação ou luminosidade.</span><span class="sxs-lookup"><span data-stu-id="0323c-124">For example, users can easily choose a color using a slider because they can immediately see the effect of changes to hue, saturation, or luminosity values.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="0323c-125">Conceitos de design</span><span class="sxs-lookup"><span data-stu-id="0323c-125">Design concepts</span></span>

<span data-ttu-id="0323c-126">Embora as caixas de texto tenham o benefício de ser muito flexível, elas têm a desvantagem de ter restrições mínimas.</span><span class="sxs-lookup"><span data-stu-id="0323c-126">While text boxes have the benefit of being very flexible, they have the drawback of having minimal constraints.</span></span> <span data-ttu-id="0323c-127">As únicas restrições em uma caixa de texto editável são:</span><span class="sxs-lookup"><span data-stu-id="0323c-127">The only constraints on an editable text box are:</span></span>

-   <span data-ttu-id="0323c-128">Opcionalmente, você pode definir o número máximo de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0323c-128">You can optionally set the maximum number of characters.</span></span>
-   <span data-ttu-id="0323c-129">Opcionalmente, você pode restringir a entrada para caracteres numéricos (0 9).</span><span class="sxs-lookup"><span data-stu-id="0323c-129">You can optionally restrict input to numeric characters (0   9) only.</span></span>
-   <span data-ttu-id="0323c-130">Se você usar um [controle de rotação](ctrl-spin-controls.md), poderá limitar as opções de controle de giro a valores válidos.</span><span class="sxs-lookup"><span data-stu-id="0323c-130">If you use a [spin control](ctrl-spin-controls.md), you can limit spin control choices to valid values.</span></span>

<span data-ttu-id="0323c-131">Além da sua duração e da presença opcional de um controle de rotação, as caixas de texto não têm nenhuma pista visual que sugira os valores válidos ou seu formato.</span><span class="sxs-lookup"><span data-stu-id="0323c-131">Aside from their length and the optional presence of a spin control, text boxes don't have any visual clues that suggest the valid values or their format.</span></span> <span data-ttu-id="0323c-132">Isso significa depender dos rótulos para transmitir essas informações aos usuários.</span><span class="sxs-lookup"><span data-stu-id="0323c-132">This means relying on labels to convey this information to users.</span></span> <span data-ttu-id="0323c-133">Se os usuários digitarem texto que não seja válido, você deverá manipular o erro com uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="0323c-133">If users enter text that's not valid, you must handle the error with an error message.</span></span>

<span data-ttu-id="0323c-134">Como regra geral, **você deve usar o controle mais restrito que pode**.</span><span class="sxs-lookup"><span data-stu-id="0323c-134">As a general rule, **you should use the most constrained control that you can**.</span></span> <span data-ttu-id="0323c-135">Use controles irrestrito como caixas de texto como último recurso.</span><span class="sxs-lookup"><span data-stu-id="0323c-135">Use unconstrained controls like text boxes as a last resort.</span></span> <span data-ttu-id="0323c-136">Dito isso, quando você estiver considerando restrições, tenha em mente as necessidades de usuários globais.</span><span class="sxs-lookup"><span data-stu-id="0323c-136">That said, when you are considering constraints, bear in mind the needs of global users.</span></span> <span data-ttu-id="0323c-137">Por exemplo, um controle que é restrito a Estados Unidos CEPs não é globalizado, mas uma caixa de texto irrestrita que aceita qualquer formato de código postal é.</span><span class="sxs-lookup"><span data-stu-id="0323c-137">For example, a control that is constrained to United States ZIP Codes isn't globalized, but an unconstrained text box that accepts any postal code format is.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="0323c-138">Padrões de uso</span><span class="sxs-lookup"><span data-stu-id="0323c-138">Usage patterns</span></span>

<span data-ttu-id="0323c-139">Uma caixa de texto é um controle flexível com vários usos possíveis.</span><span class="sxs-lookup"><span data-stu-id="0323c-139">A text box is a flexible control with several possible uses.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0323c-140"><strong>Entrada de dados</strong></span><span class="sxs-lookup"><span data-stu-id="0323c-140"><strong>Data input</strong></span></span><br/> <span data-ttu-id="0323c-141">Uma caixa de texto de linha única e irrestrita usada para inserir ou editar cadeias de caracteres curtas.</span><span class="sxs-lookup"><span data-stu-id="0323c-141">A single-line, unconstrained text box used to enter or edit short strings.</span></span><br/></td>
<td><img src="images/ctrl-text-boxes-image2.png" alt="Screen shot of a text box with Display name label " /><br/> <span data-ttu-id="0323c-142">Uma caixa de texto de linha única e irrestrita.</span><span class="sxs-lookup"><span data-stu-id="0323c-142">A single-line, unconstrained text box.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0323c-143"><strong>Entrada de dados formatados</strong></span><span class="sxs-lookup"><span data-stu-id="0323c-143"><strong>Formatted data input</strong></span></span><br/> <span data-ttu-id="0323c-144">Um conjunto de caixas de texto de linha simples, com tamanho fixo e curto usado para inserir dados com um formato específico.</span><span class="sxs-lookup"><span data-stu-id="0323c-144">A set of short, fixed-sized, single-line text boxes used to enter data with a specific format.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image3.png" alt="Screen shot of a Product key text box " /><br/> <span data-ttu-id="0323c-145">Uma caixa de texto usada para entrada de dados formatados.</span><span class="sxs-lookup"><span data-stu-id="0323c-145">A text box used for formatted data input.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="0323c-146">O recurso de <a href="glossary.md">saída automática</a> avança automaticamente o foco de entrada de uma caixa de texto para a próxima.</span><span class="sxs-lookup"><span data-stu-id="0323c-146">The <a href="glossary.md">auto-exit</a> feature automatically advances the input focus from one text box to the next.</span></span> <span data-ttu-id="0323c-147">Uma desvantagem dessa abordagem é que os dados não podem ser copiados ou colados como uma única unidade.</span><span class="sxs-lookup"><span data-stu-id="0323c-147">One disadvantage to this approach is that the data can't be copied or pasted as a single unit.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0323c-148"><strong>Entrada de dados assistida</strong></span><span class="sxs-lookup"><span data-stu-id="0323c-148"><strong>Assisted data input</strong></span></span><br/> <span data-ttu-id="0323c-149">Uma caixa de texto de linha única e irrestrita usada para inserir ou editar cadeias de caracteres, combinadas com um botão de comando que ajuda os usuários a selecionar valores válidos.</span><span class="sxs-lookup"><span data-stu-id="0323c-149">A single-line, unconstrained text box used to enter or edit strings, combined with a command button that helps users select valid values.</span></span><br/></td>
<td><img src="images/ctrl-text-boxes-image4.png" alt="Screen shot of text box with Browse button" /><br/> <span data-ttu-id="0323c-150">Neste exemplo, o comando procurar ajuda os usuários a selecionar valores válidos.</span><span class="sxs-lookup"><span data-stu-id="0323c-150">In this example, the Browse command helps users select valid values.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0323c-151"><strong>Entrada textual</strong></span><span class="sxs-lookup"><span data-stu-id="0323c-151"><strong>Textual input</strong></span></span><br/> <span data-ttu-id="0323c-152">Uma caixa de texto de várias linhas e irrestrita usada para inserir ou editar cadeias de caracteres longas.</span><span class="sxs-lookup"><span data-stu-id="0323c-152">A multi-line, unconstrained text box used to enter or edit long strings.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image5.png" alt="Screen shot of an Address text box " /><br/> <span data-ttu-id="0323c-153">Uma caixa de texto de várias linhas e irrestrita.</span><span class="sxs-lookup"><span data-stu-id="0323c-153">A multi-line, unconstrained text box.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0323c-154"><strong>Entrada numérica</strong></span><span class="sxs-lookup"><span data-stu-id="0323c-154"><strong>Numeric input</strong></span></span><br/> <span data-ttu-id="0323c-155">Uma caixa de texto de linha única, somente numérica, usada para inserir ou editar números, com um <a href="ctrl-spin-controls.md">controle de rotação</a> opcional para facilitar a entrada baseada no mouse.</span><span class="sxs-lookup"><span data-stu-id="0323c-155">A single-line, numeric-only text box used to enter or edit numbers, with an optional <a href="ctrl-spin-controls.md">spin control</a> to facilitate mouse-based input.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image6.png" alt="Screen shot of a text box for entering a wait time " /><br/> <span data-ttu-id="0323c-156">Uma caixa de texto usada para entrada numérica.</span><span class="sxs-lookup"><span data-stu-id="0323c-156">A text box used for numeric input.</span></span><br/> <span data-ttu-id="0323c-157">A combinação de uma caixa de texto e seu controle de rotação associado é chamada de <a href="ctrl-spin-controls.md">caixa de rotação</a>.</span><span class="sxs-lookup"><span data-stu-id="0323c-157">The combination of a text box and its associated spin control is called a <a href="ctrl-spin-controls.md">spin box</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0323c-158"><strong>Senha e PIN de entrada</strong></span><span class="sxs-lookup"><span data-stu-id="0323c-158"><strong>Password and PIN input</strong></span></span><br/> <span data-ttu-id="0323c-159">Uma caixa de texto de linha única e irrestrita usada para inserir senhas e PINs com segurança.</span><span class="sxs-lookup"><span data-stu-id="0323c-159">A single-line, unconstrained text box used to enter passwords and PINs securely.</span></span><br/></td>
<td><img src="images/ctrl-text-boxes-image7.png" alt="Screen shot of a Password text box " /><br/> <span data-ttu-id="0323c-160">Uma caixa de texto usada para inserir senhas.</span><span class="sxs-lookup"><span data-stu-id="0323c-160">A text box used to enter passwords.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0323c-161"><strong>Saída de dados</strong></span><span class="sxs-lookup"><span data-stu-id="0323c-161"><strong>Data output</strong></span></span><br/> <span data-ttu-id="0323c-162">Uma caixa de texto de linha única, somente leitura, sempre exibida sem uma borda, usada para exibir cadeias de caracteres curtas.</span><span class="sxs-lookup"><span data-stu-id="0323c-162">A single-line, read-only text box, always displayed without a border, used to display short strings.</span></span> <br/></td>
<td><span data-ttu-id="0323c-163">Diferentemente do texto estático, os dados exibidos usando uma caixa de texto podem ser rolados (útil se os dados forem mais largos do que o controle), selecionados e copiados.</span><span class="sxs-lookup"><span data-stu-id="0323c-163">Unlike static text, data displayed using a text box can be scrolled (useful if the data is wider than the control), selected, and copied.</span></span><br/> <img src="images/ctrl-text-boxes-image8.png" alt="Screen shot of a text box showing path to a folder " /><br/> <span data-ttu-id="0323c-164">Uma caixa de texto somente leitura de linha única usada para exibir dados.</span><span class="sxs-lookup"><span data-stu-id="0323c-164">A single-line, read-only text box used to display data.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0323c-165"><strong>Saída textual</strong></span><span class="sxs-lookup"><span data-stu-id="0323c-165"><strong>Textual output</strong></span></span><br/> <span data-ttu-id="0323c-166">Uma caixa de texto somente leitura de várias linhas usada para exibir cadeias de caracteres longas.</span><span class="sxs-lookup"><span data-stu-id="0323c-166">A multi-line, read-only text box used to display long strings.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image9.png" alt="Screen shot of a Privacy information text box " /><br/> <span data-ttu-id="0323c-167">Uma caixa de texto somente leitura usada para exibir dados.</span><span class="sxs-lookup"><span data-stu-id="0323c-167">A read-only text box used to display data.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a><span data-ttu-id="0323c-168">Diretrizes</span><span class="sxs-lookup"><span data-stu-id="0323c-168">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="0323c-169">Geral</span><span class="sxs-lookup"><span data-stu-id="0323c-169">General</span></span>

-   <span data-ttu-id="0323c-170">**Ao desabilitar uma caixa de texto, também desabilite quaisquer rótulos associados, rótulos de instrução, controles de rotação e botões de comando.**</span><span class="sxs-lookup"><span data-stu-id="0323c-170">**When disabling a text box, also disable any associated labels, instruction labels, spin controls, and command buttons.**</span></span>
-   <span data-ttu-id="0323c-171">**Use o preenchimento automático para ajudar os usuários a inserir dados que provavelmente serão usados repetidamente**.</span><span class="sxs-lookup"><span data-stu-id="0323c-171">**Use auto-complete to help users enter data that is likely to be used repeatedly**.</span></span> <span data-ttu-id="0323c-172">Os exemplos incluem nomes de usuário, endereços e nomes de arquivo.</span><span class="sxs-lookup"><span data-stu-id="0323c-172">Examples include user names, addresses, and file names.</span></span> <span data-ttu-id="0323c-173">No entanto, não use o preenchimento automático para caixas de texto que possam conter informações confidenciais, como senhas, PINs, números de cartão de crédito ou informações médicas.</span><span class="sxs-lookup"><span data-stu-id="0323c-173">However, don't use auto-complete for text boxes that may contain sensitive information, such as passwords, PINs, credit card numbers, or medical information.</span></span>
-   <span data-ttu-id="0323c-174">**Não faça os usuários rolarem desnecessariamente.**</span><span class="sxs-lookup"><span data-stu-id="0323c-174">**Don't make users scroll unnecessarily.**</span></span> <span data-ttu-id="0323c-175">Se você espera que os dados sejam maiores do que a caixa de texto e você pode rapidamente tornar a caixa de texto maior sem prejudicar o layout, dimensione a caixa para eliminar a necessidade de rolagem.</span><span class="sxs-lookup"><span data-stu-id="0323c-175">If you expect data to be larger than the text box and you can readily make the text box larger without harming the layout, size the box to eliminate the need for scrolling.</span></span>

    <span data-ttu-id="0323c-176">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="0323c-176">**Incorrect:**</span></span>

    ![<span data-ttu-id="0323c-177">captura de tela de uma caixa de texto de nome do computador</span><span class="sxs-lookup"><span data-stu-id="0323c-177">screen shot of a computer name text box</span></span> ](images/ctrl-text-boxes-image10.png)

    <span data-ttu-id="0323c-178">Neste exemplo, a caixa de texto deve se tornar muito mais demorada para lidar com seus dados.</span><span class="sxs-lookup"><span data-stu-id="0323c-178">In this example, the text box should be made much longer to handle its data.</span></span>

-   <span data-ttu-id="0323c-179">Barras de rolagem:</span><span class="sxs-lookup"><span data-stu-id="0323c-179">Scroll bars:</span></span>
    -   <span data-ttu-id="0323c-180">**Não coloque barras de rolagem horizontais em caixas de texto de várias linhas.**</span><span class="sxs-lookup"><span data-stu-id="0323c-180">**Don't put horizontal scroll bars on multi-line text boxes.**</span></span> <span data-ttu-id="0323c-181">Em vez disso, use a rolagem vertical e a quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="0323c-181">Use vertical scrolling and line wrapping instead.</span></span>
    -   <span data-ttu-id="0323c-182">**Não coloque nenhuma barra de rolagem em caixas de texto de linha única.**</span><span class="sxs-lookup"><span data-stu-id="0323c-182">**Don't put any scroll bars on single-line text boxes.**</span></span>
-   <span data-ttu-id="0323c-183">**Para entrada numérica, você pode usar um controle de rotação.**</span><span class="sxs-lookup"><span data-stu-id="0323c-183">**For numeric input, you may use a spin control.**</span></span> <span data-ttu-id="0323c-184">Para entrada textual, use uma lista suspensa ou lista suspensa editável em vez disso.</span><span class="sxs-lookup"><span data-stu-id="0323c-184">For textual input, use a drop-down list or editable drop-down list instead.</span></span>
-   <span data-ttu-id="0323c-185">**Não use o recurso de saída automática, exceto para entrada de dados formatados.**</span><span class="sxs-lookup"><span data-stu-id="0323c-185">**Don't use the auto-exit feature except for formatted data input.**</span></span> <span data-ttu-id="0323c-186">A mudança automática de foco pode surpreender os usuários.</span><span class="sxs-lookup"><span data-stu-id="0323c-186">The automatic shift of focus can surprise users.</span></span>

### <a name="editable-text-boxes"></a><span data-ttu-id="0323c-187">Caixas de texto editáveis</span><span class="sxs-lookup"><span data-stu-id="0323c-187">Editable text boxes</span></span>

-   <span data-ttu-id="0323c-188">**Limite o tamanho do texto de entrada quando possível.**</span><span class="sxs-lookup"><span data-stu-id="0323c-188">**Limit the length of the input text when you can.**</span></span> <span data-ttu-id="0323c-189">Por exemplo, se a entrada válida for um número entre 0 e 999, use uma caixa de texto numérica que esteja limitada a três caracteres.</span><span class="sxs-lookup"><span data-stu-id="0323c-189">For example, if the valid input is a number between 0 and 999, use a numeric text box that is limited to three characters.</span></span> <span data-ttu-id="0323c-190">Todas as partes de caixas de texto que usam entrada de dados formatados devem ter um tamanho curto e fixo.</span><span class="sxs-lookup"><span data-stu-id="0323c-190">All parts of text boxes that use formatted data input must have a short, fixed length.</span></span>
-   <span data-ttu-id="0323c-191">**Seja flexível com formatos de dados.**</span><span class="sxs-lookup"><span data-stu-id="0323c-191">**Be flexible with data formats.**</span></span> <span data-ttu-id="0323c-192">Se for provável que os usuários insiram texto usando uma ampla variedade de formatos, tente lidar com todos os mais comuns.</span><span class="sxs-lookup"><span data-stu-id="0323c-192">If users are likely to enter text using a wide variety of formats, try to handle all the most common ones.</span></span> <span data-ttu-id="0323c-193">Por exemplo, muitos nomes, números e identificadores podem ser inseridos com espaços e pontuação opcionais, e a capitalização geralmente não importa.</span><span class="sxs-lookup"><span data-stu-id="0323c-193">For example, many names, numbers, and identifiers can be entered with optional spaces and punctuation, and the capitalization often doesn't matter.</span></span>
-   <span data-ttu-id="0323c-194">Se você não puder lidar com os formatos prováveis, exija um formato específico usando a entrada de dados formatados ou indique os formatos válidos no rótulo.</span><span class="sxs-lookup"><span data-stu-id="0323c-194">If you can't handle the likely formats, require a specific format by using formatted data input or indicate the valid formats in the label.</span></span>

    <span data-ttu-id="0323c-195">**Aceitável:**</span><span class="sxs-lookup"><span data-stu-id="0323c-195">**Acceptable:**</span></span>

    ![<span data-ttu-id="0323c-196">captura de tela de uma caixa de texto para entrada numérica</span><span class="sxs-lookup"><span data-stu-id="0323c-196">screen shot of a text box for numeric input</span></span> ](images/ctrl-text-boxes-image11.png)

    <span data-ttu-id="0323c-197">Neste exemplo, uma caixa de texto requer entrada em um formato específico.</span><span class="sxs-lookup"><span data-stu-id="0323c-197">In this example, a text box requires input in a specific format.</span></span>

    <span data-ttu-id="0323c-198">**Melhor:**</span><span class="sxs-lookup"><span data-stu-id="0323c-198">**Better:**</span></span>

    ![<span data-ttu-id="0323c-199">captura de tela da caixa de texto de entrada de dados formatados</span><span class="sxs-lookup"><span data-stu-id="0323c-199">screen shot of formatted data input text box</span></span> ](images/ctrl-text-boxes-image12.png)

    <span data-ttu-id="0323c-200">Neste exemplo, o padrão de entrada de dados formatados é usado para exigir um formato específico.</span><span class="sxs-lookup"><span data-stu-id="0323c-200">In this example, the formatted data input pattern is used to require a specific format.</span></span>

    <span data-ttu-id="0323c-201">**Recomendá**</span><span class="sxs-lookup"><span data-stu-id="0323c-201">**Best:**</span></span>

    ![<span data-ttu-id="0323c-202">captura de tela de uma caixa de texto irrestrita</span><span class="sxs-lookup"><span data-stu-id="0323c-202">screen shot of an unconstrained text box</span></span> ](images/ctrl-text-boxes-image13.png)

    <span data-ttu-id="0323c-203">Neste exemplo, uma caixa de texto lida com todos os formatos prováveis.</span><span class="sxs-lookup"><span data-stu-id="0323c-203">In this example, a text box handles all likely formats.</span></span>

-   <span data-ttu-id="0323c-204">Considere a flexibilidade de formato ao escolher o comprimento máximo de entrada.</span><span class="sxs-lookup"><span data-stu-id="0323c-204">Consider format flexibility when choosing the maximum input length.</span></span> <span data-ttu-id="0323c-205">Por exemplo, um número de cartão de crédito válido pode usar até 19 caracteres, portanto, limitar o comprimento a algo mais curto dificultaria a inserção de números usando os formatos mais longos.</span><span class="sxs-lookup"><span data-stu-id="0323c-205">For example, a valid credit card number can use up to 19 characters so limiting the length to anything shorter would make it difficult to enter numbers using the longer formats.</span></span>
-   <span data-ttu-id="0323c-206">**Não use o padrão de entrada de dados formatado se for mais provável que os usuários colem dados longos e complexos.**</span><span class="sxs-lookup"><span data-stu-id="0323c-206">**Don't use the formatted data input pattern if users are more likely to paste in long, complex data.**</span></span> <span data-ttu-id="0323c-207">Em vez disso, Reserve o padrão de entrada de dados formatado para situações em que os usuários têm mais probabilidade de digitar os dados.</span><span class="sxs-lookup"><span data-stu-id="0323c-207">Rather, reserve the formatted data input pattern for situations where users are more likely to type the data.</span></span>

    ![<span data-ttu-id="0323c-208">captura de tela de uma caixa de texto com rótulo: endereço IPv6</span><span class="sxs-lookup"><span data-stu-id="0323c-208">screen shot of a text box with label: ipv6 address</span></span> ](images/ctrl-text-boxes-image14.png)

    <span data-ttu-id="0323c-209">Neste exemplo, o padrão de entrada de dados formatado não é usado, para que os usuários possam colar os endereços IPv6.</span><span class="sxs-lookup"><span data-stu-id="0323c-209">In this example, the formatted data input pattern isn't used, so that users can to paste IPv6 addresses.</span></span>

-   <span data-ttu-id="0323c-210">**Se for mais provável que os usuários reinsiram o valor inteiro, selecione todo o texto no foco de entrada.**</span><span class="sxs-lookup"><span data-stu-id="0323c-210">**If users are more likely going to reenter the entire value, select all the text on input focus.**</span></span> <span data-ttu-id="0323c-211">Se for mais provável que os usuários editem, coloque o cursor no final do texto.</span><span class="sxs-lookup"><span data-stu-id="0323c-211">If users are more likely to edit, place the caret at the end of the text.</span></span>

    ![<span data-ttu-id="0323c-212">captura de tela de uma caixa de texto de senha</span><span class="sxs-lookup"><span data-stu-id="0323c-212">screen shot of a password text box</span></span> ](images/ctrl-text-boxes-image15.png)

    <span data-ttu-id="0323c-213">Neste exemplo, é mais provável que os usuários substituam de editar, portanto, o valor inteiro é selecionado no foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="0323c-213">In this example, users are more likely to replace than edit, so the entire value is selected on input focus.</span></span>

    ![<span data-ttu-id="0323c-214">captura de tela de uma caixa de texto para inserir palavras-chave</span><span class="sxs-lookup"><span data-stu-id="0323c-214">screen shot of a text box for entering keywords</span></span> ](images/ctrl-text-boxes-image16.png)

    <span data-ttu-id="0323c-215">Neste exemplo, é mais provável que os usuários adicionem palavras-chave do que substituir o texto, portanto, o cursor é colocado no final do texto.</span><span class="sxs-lookup"><span data-stu-id="0323c-215">In this example, users are more likely to add keywords than replace the text, so the caret is placed at the end of the text.</span></span>

-   <span data-ttu-id="0323c-216">**Sempre use uma caixa de texto de várias linhas se os caracteres de nova linha forem de entrada válida.**</span><span class="sxs-lookup"><span data-stu-id="0323c-216">**Always use a multi-line text box if new-line characters are valid input.**</span></span>
-   <span data-ttu-id="0323c-217">**Quando a caixa de texto for para um arquivo ou caminho, sempre forneça um botão procurar.**</span><span class="sxs-lookup"><span data-stu-id="0323c-217">**When the text box is for a file or path, always provide a Browse button.**</span></span>

### <a name="numeric-text-boxes"></a><span data-ttu-id="0323c-218">Caixas de texto numéricas</span><span class="sxs-lookup"><span data-stu-id="0323c-218">Numeric text boxes</span></span>

-   <span data-ttu-id="0323c-219">**Escolha a unidade mais conveniente e etiquete as unidades.**</span><span class="sxs-lookup"><span data-stu-id="0323c-219">**Choose the most convenient unit and label the units.**</span></span> <span data-ttu-id="0323c-220">Por exemplo, considere usar milliliters em vez de litros (ou vice-versa), percentuais em vez de valores diretos (ou vice-versa) e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="0323c-220">For example, consider using milliliters instead of liters (or vice versa), percentages instead of direct values (or vice versa), and so on.</span></span>

    <span data-ttu-id="0323c-221">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="0323c-221">**Correct:**</span></span>

    ![<span data-ttu-id="0323c-222">captura de tela da caixa de texto com litros como unidade</span><span class="sxs-lookup"><span data-stu-id="0323c-222">screen shot of text box with liters as unit</span></span> ](images/ctrl-text-boxes-image17.png)

    <span data-ttu-id="0323c-223">Neste exemplo, a unidade é rotulada, mas requer que os usuários insiram números decimais.</span><span class="sxs-lookup"><span data-stu-id="0323c-223">In this example, the unit is labeled, but it requires users to enter decimal numbers.</span></span>

    <span data-ttu-id="0323c-224">**Melhor:**</span><span class="sxs-lookup"><span data-stu-id="0323c-224">**Better:**</span></span>

    ![<span data-ttu-id="0323c-225">captura de tela da caixa de texto com milliliters como unidade</span><span class="sxs-lookup"><span data-stu-id="0323c-225">screen shot of text box with milliliters as unit</span></span> ](images/ctrl-text-boxes-image18.png)

    <span data-ttu-id="0323c-226">Neste exemplo, a caixa de texto usa uma unidade mais conveniente.</span><span class="sxs-lookup"><span data-stu-id="0323c-226">In this example, the text box uses a more convenient unit.</span></span>

-   <span data-ttu-id="0323c-227">**Use um controle de rotação sempre que for útil.**</span><span class="sxs-lookup"><span data-stu-id="0323c-227">**Use a spin control whenever it is helpful.**</span></span> <span data-ttu-id="0323c-228">No entanto, às vezes, os controles de rotação não são práticos, como quando os usuários precisam inserir muitos números grandes.</span><span class="sxs-lookup"><span data-stu-id="0323c-228">However, sometimes spin controls aren't practical, such as when users need to enter many large numbers.</span></span> <span data-ttu-id="0323c-229">Use controles de rotação quando:</span><span class="sxs-lookup"><span data-stu-id="0323c-229">Use spin controls when:</span></span>
    -   <span data-ttu-id="0323c-230">A entrada provavelmente será um número pequeno, normalmente em 100.</span><span class="sxs-lookup"><span data-stu-id="0323c-230">The input is likely to be a small number, typically under 100.</span></span>
    -   <span data-ttu-id="0323c-231">É provável que os usuários façam uma pequena alteração em um número existente.</span><span class="sxs-lookup"><span data-stu-id="0323c-231">Users are likely to make a small change to an existing number.</span></span>
    -   <span data-ttu-id="0323c-232">É mais provável que os usuários estejam usando o mouse do que o teclado.</span><span class="sxs-lookup"><span data-stu-id="0323c-232">Users are more likely to be using the mouse than the keyboard.</span></span>
-   <span data-ttu-id="0323c-233">**Alinhar texto numérico à direita sempre que:**</span><span class="sxs-lookup"><span data-stu-id="0323c-233">**Right-align numeric text whenever:**</span></span>

    -   <span data-ttu-id="0323c-234">Há mais de uma caixa de texto numérica.</span><span class="sxs-lookup"><span data-stu-id="0323c-234">There is more than one numeric text box.</span></span>
    -   <span data-ttu-id="0323c-235">As caixas de texto são alinhadas verticalmente.</span><span class="sxs-lookup"><span data-stu-id="0323c-235">The text boxes are vertically aligned.</span></span>
    -   <span data-ttu-id="0323c-236">É provável que os usuários adicionem ou comparem os valores.</span><span class="sxs-lookup"><span data-stu-id="0323c-236">Users are likely to add or compare the values.</span></span>

    <span data-ttu-id="0323c-237">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="0323c-237">**Correct:**</span></span>

    ![<span data-ttu-id="0323c-238">captura de tela de caixas de texto de despesas (Hotel, etc.)</span><span class="sxs-lookup"><span data-stu-id="0323c-238">screen shot of expenses text boxes (hotel, etc.)</span></span> ](images/ctrl-text-boxes-image19.png)

    <span data-ttu-id="0323c-239">Neste exemplo, o texto numérico é alinhado à direita para facilitar a comparação de valores.</span><span class="sxs-lookup"><span data-stu-id="0323c-239">In this example, the numeric text is right-aligned to make it easy to compare values.</span></span>

    <span data-ttu-id="0323c-240">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="0323c-240">**Incorrect:**</span></span>

    ![<span data-ttu-id="0323c-241">captura de tela de caixas de texto para valores RGB</span><span class="sxs-lookup"><span data-stu-id="0323c-241">screen shot of text boxes for rgb values</span></span> ](images/ctrl-text-boxes-image20.png)

    <span data-ttu-id="0323c-242">Neste exemplo, o texto numérico está alinhado à esquerda incorretamente.</span><span class="sxs-lookup"><span data-stu-id="0323c-242">In this example, the numeric text is incorrectly left-aligned.</span></span>

-   <span data-ttu-id="0323c-243">**Sempre alinhar valores monetários à direita.**</span><span class="sxs-lookup"><span data-stu-id="0323c-243">**Always right-align monetary values.**</span></span>
-   <span data-ttu-id="0323c-244">**Não atribua significados especiais a valores numéricos específicos**, mesmo se esses significados especiais forem usados internamente pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0323c-244">**Don't assign special meanings to specific numeric values**, even if those special meanings are used internally by your application.</span></span> <span data-ttu-id="0323c-245">Em vez disso, use caixas de seleção ou botões de opção para uma seleção de usuário explícita.</span><span class="sxs-lookup"><span data-stu-id="0323c-245">Instead, use check boxes or radio buttons for an explicit user selection.</span></span>

    <span data-ttu-id="0323c-246">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="0323c-246">**Incorrect:**</span></span>

    ![<span data-ttu-id="0323c-247">captura de tela do rótulo: use-1 para desabilitar o cache</span><span class="sxs-lookup"><span data-stu-id="0323c-247">screen shot of label: use -1 to disable caching</span></span> ](images/ctrl-text-boxes-image21.png)

    <span data-ttu-id="0323c-248">Neste exemplo, o valor-1 tem um significado especial.</span><span class="sxs-lookup"><span data-stu-id="0323c-248">In this example, the value -1 has a special meaning.</span></span>

    <span data-ttu-id="0323c-249">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="0323c-249">**Correct:**</span></span>

    ![<span data-ttu-id="0323c-250">captura de tela do rótulo da caixa de seleção: Caching</span><span class="sxs-lookup"><span data-stu-id="0323c-250">screen shot of check box label: caching</span></span> ](images/ctrl-text-boxes-image22.png)

    <span data-ttu-id="0323c-251">Neste exemplo, uma caixa de seleção torna a opção Explicit.</span><span class="sxs-lookup"><span data-stu-id="0323c-251">In this example, a check box makes the option explicit.</span></span>

### <a name="password-and-pin-input"></a><span data-ttu-id="0323c-252">Senha e PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="0323c-252">Password and PIN input</span></span>

-   <span data-ttu-id="0323c-253">**Sempre use o controle comum de senha em vez de criar o seu próprio.**</span><span class="sxs-lookup"><span data-stu-id="0323c-253">**Always use the password common control instead of creating your own.**</span></span> <span data-ttu-id="0323c-254">Senhas e PINs exigem tratamento especial para serem manipulados com segurança.</span><span class="sxs-lookup"><span data-stu-id="0323c-254">Passwords and PINs require special treatment to be handled securely.</span></span>

<span data-ttu-id="0323c-255">Para obter mais diretrizes e exemplos, consulte [balões](ctrl-balloons.md).</span><span class="sxs-lookup"><span data-stu-id="0323c-255">For more guidelines and examples, see [Balloons](ctrl-balloons.md).</span></span>

### <a name="textual-output"></a><span data-ttu-id="0323c-256">Saída textual</span><span class="sxs-lookup"><span data-stu-id="0323c-256">Textual output</span></span>

-   <span data-ttu-id="0323c-257">**Considere o uso da cor do sistema de plano de fundo branco para texto grande somente leitura de várias linhas.**</span><span class="sxs-lookup"><span data-stu-id="0323c-257">**Consider using the white background system color for large, multi-line read-only text.**</span></span> <span data-ttu-id="0323c-258">Um plano de fundo branco torna o texto mais fácil de ler.</span><span class="sxs-lookup"><span data-stu-id="0323c-258">A white background makes the text easier to read.</span></span> <span data-ttu-id="0323c-259">Muitos textos em um plano de fundo cinza desencorajam a leitura.</span><span class="sxs-lookup"><span data-stu-id="0323c-259">Lots of text on a gray background discourages reading.</span></span>

<span data-ttu-id="0323c-260">Para obter mais informações sobre cores de plano de fundo, consulte [fontes](vis-fonts.md).</span><span class="sxs-lookup"><span data-stu-id="0323c-260">For more information on background colors, see [Fonts](vis-fonts.md).</span></span>

### <a name="data-output"></a><span data-ttu-id="0323c-261">Saída de dados</span><span class="sxs-lookup"><span data-stu-id="0323c-261">Data output</span></span>

-   <span data-ttu-id="0323c-262">**Não use uma borda para caixas de texto somente leitura de linha única.**</span><span class="sxs-lookup"><span data-stu-id="0323c-262">**Don't use a border for single-line, read-only text boxes.**</span></span> <span data-ttu-id="0323c-263">A borda é uma pista visual de que o texto é editável.</span><span class="sxs-lookup"><span data-stu-id="0323c-263">The border is a visual clue that the text is editable.</span></span>
-   <span data-ttu-id="0323c-264">**Não desabilite caixas de texto somente leitura de linha única.**</span><span class="sxs-lookup"><span data-stu-id="0323c-264">**Don't disable single-line, read-only text boxes.**</span></span> <span data-ttu-id="0323c-265">Isso impede que os usuários selecionem e copiem o texto para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="0323c-265">This prevents users from selecting and copying the text to the clipboard.</span></span> <span data-ttu-id="0323c-266">Ele também impede que os usuários rolem os dados se excederem o tamanho de seus limites.</span><span class="sxs-lookup"><span data-stu-id="0323c-266">It also prevents users from scrolling the data if it exceeds the size of its boundaries.</span></span>
-   <span data-ttu-id="0323c-267">**Não defina uma parada de tabulação na caixa de texto somente leitura de linha única, a menos que o usuário provavelmente precise rolar ou copiar o texto.**</span><span class="sxs-lookup"><span data-stu-id="0323c-267">**Don't set a tab stop on single-line, read-only text box unless the user is likely to need to scroll or copy the text.**</span></span>

## <a name="input-validation-and-error-handling"></a><span data-ttu-id="0323c-268">Validação de entrada e tratamento de erro</span><span class="sxs-lookup"><span data-stu-id="0323c-268">Input validation and error handling</span></span>

<span data-ttu-id="0323c-269">Como as caixas de texto geralmente não são restritas para aceitar apenas uma entrada válida, talvez seja necessário validar a entrada e lidar com quaisquer problemas.</span><span class="sxs-lookup"><span data-stu-id="0323c-269">Because text boxes are usually not constrained to accept only valid input, you may need to validate the input and handle any problems.</span></span> <span data-ttu-id="0323c-270">Valide os vários tipos de problemas de entrada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="0323c-270">Validate the various types of input problems as follows:</span></span>

-   <span data-ttu-id="0323c-271">Se o usuário inserir um caractere que não é válido, ignore o caractere e exiba um [balão de problema de entrada](ctrl-balloons.md) que explique os caracteres válidos.</span><span class="sxs-lookup"><span data-stu-id="0323c-271">If the user enters a character that isn't valid, ignore the character and display an [input problem balloon](ctrl-balloons.md) that explains the valid characters.</span></span>

    ![captura de tela da caixa de texto da chave do produto](images/ctrl-text-boxes-image23.png)

    <span data-ttu-id="0323c-273">Neste exemplo, um balão relata um caractere de entrada incorreto.</span><span class="sxs-lookup"><span data-stu-id="0323c-273">In this example, a balloon reports an incorrect input character.</span></span>

-   <span data-ttu-id="0323c-274">Se os dados de entrada tiverem um valor ou formato que não é válido, exiba um balão de problema de entrada quando a caixa de texto perder o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="0323c-274">If the input data has a value or format that isn't valid, display an input problem balloon when the text box loses input focus.</span></span>
-   <span data-ttu-id="0323c-275">Se os dados de entrada estiverem inconsistentes com outros controles na janela, forneça uma mensagem de erro quando a entrada inteira for concluída, por exemplo, quando os usuários clicarem em OK para uma caixa de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="0323c-275">If the input data is inconsistent with other controls on the window, give an error message when the entire input is complete, such as when users click OK for a modal dialog box.</span></span>

<span data-ttu-id="0323c-276">**Não limpe dados de entrada inválidos, a menos que os usuários não possam corrigir erros facilmente.**</span><span class="sxs-lookup"><span data-stu-id="0323c-276">**Don't clear invalid input data unless users aren't able to correct errors easily.**</span></span> <span data-ttu-id="0323c-277">Isso permite que os usuários corrijam os erros sem começar de novo.</span><span class="sxs-lookup"><span data-stu-id="0323c-277">Doing so allows users to correct mistakes without starting over.</span></span> <span data-ttu-id="0323c-278">Por exemplo, você deve limpar senhas e PINs incorretos, pois os usuários não podem corrigi-los facilmente.</span><span class="sxs-lookup"><span data-stu-id="0323c-278">For example, you should clear incorrect passwords and PINs because users can't correct them easily.</span></span>

<span data-ttu-id="0323c-279">Para obter mais diretrizes e exemplos, consulte [mensagens de erro](mess-error.md) e [balões](ctrl-balloons.md).</span><span class="sxs-lookup"><span data-stu-id="0323c-279">For more guidelines and examples, see [Error Messages](mess-error.md) and [Balloons](ctrl-balloons.md).</span></span>

## <a name="prompts"></a><span data-ttu-id="0323c-280">Solicitações</span><span class="sxs-lookup"><span data-stu-id="0323c-280">Prompts</span></span>

<span data-ttu-id="0323c-281">Um prompt é um rótulo ou uma instrução curta colocada dentro de uma caixa de texto como seu valor padrão.</span><span class="sxs-lookup"><span data-stu-id="0323c-281">A prompt is a label or short instruction placed inside a text box as its default value.</span></span> <span data-ttu-id="0323c-282">Ao contrário do texto estático, os prompts desaparecem da tela quando os usuários digitam algo na caixa de texto ou recebem o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="0323c-282">Unlike static text, prompts disappear from the screen once users type something into the text box or it gets input focus.</span></span>

![<span data-ttu-id="0323c-283">captura de tela da caixa de texto de aviso com o rótulo: Pesquisar</span><span class="sxs-lookup"><span data-stu-id="0323c-283">screen shot of prompt text box with label: search</span></span> ](images/ctrl-text-boxes-image24.png)

<span data-ttu-id="0323c-284">Um prompt típico.</span><span class="sxs-lookup"><span data-stu-id="0323c-284">A typical prompt.</span></span>

<span data-ttu-id="0323c-285">Use um prompt quando:</span><span class="sxs-lookup"><span data-stu-id="0323c-285">Use a prompt when:</span></span>

-   <span data-ttu-id="0323c-286">O espaço na tela é um tanto que usar um rótulo ou instrução é indesejável, como em uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="0323c-286">Screen space is at such a premium that using a label or instruction is undesirable, such as on a toolbar.</span></span>
-   <span data-ttu-id="0323c-287">O prompt destina-se principalmente à identificação da finalidade da caixa de texto de forma compactada.</span><span class="sxs-lookup"><span data-stu-id="0323c-287">The prompt is primarily for identifying the purpose of the text box in a compact way.</span></span> <span data-ttu-id="0323c-288">Elas não devem ser informações cruciais que o usuário precisa ver ao usar a caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="0323c-288">It must not be crucial information that the user needs to see while using the text box.</span></span>

<span data-ttu-id="0323c-289">Não use prompts apenas para direcionar os usuários para digitar algo ou clicar em botões.</span><span class="sxs-lookup"><span data-stu-id="0323c-289">Don't use prompts just to direct users to type something or to click buttons.</span></span> <span data-ttu-id="0323c-290">Por exemplo, não escreva o texto do prompt que diga inserir um nome de arquivo e, em seguida, clique em enviar.</span><span class="sxs-lookup"><span data-stu-id="0323c-290">For example, don't write prompt text that says Enter a filename and then click Send.</span></span>

<span data-ttu-id="0323c-291">Ao usar prompts:</span><span class="sxs-lookup"><span data-stu-id="0323c-291">When using prompts:</span></span>

-   <span data-ttu-id="0323c-292">Desenhe o texto do prompt em cinza itálico e o texto de entrada real em preto normal.</span><span class="sxs-lookup"><span data-stu-id="0323c-292">Draw the prompt text in italic gray and the actual input text in normal black.</span></span> <span data-ttu-id="0323c-293">O texto do prompt não deve ser confundido com texto real.</span><span class="sxs-lookup"><span data-stu-id="0323c-293">The prompt text must not be confused with real text.</span></span>
-   <span data-ttu-id="0323c-294">Mantenha o texto do prompt conciso.</span><span class="sxs-lookup"><span data-stu-id="0323c-294">Keep the prompt text concise.</span></span> <span data-ttu-id="0323c-295">Você pode usar fragmentos em vez de frases completas.</span><span class="sxs-lookup"><span data-stu-id="0323c-295">You can use fragments instead of full sentences.</span></span>
-   <span data-ttu-id="0323c-296">Use a capitalização com estilo de frase.</span><span class="sxs-lookup"><span data-stu-id="0323c-296">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="0323c-297">Não use pontuação final ou reticências.</span><span class="sxs-lookup"><span data-stu-id="0323c-297">Don't use ending punctuation or ellipsis.</span></span>
-   <span data-ttu-id="0323c-298">O texto do prompt não deve ser editável e deve desaparecer quando os usuários clicarem na guia ou na caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="0323c-298">The prompt text should not be editable and should disappear once users click in or tab into the text box.</span></span>
    -   <span data-ttu-id="0323c-299">**Exceção:** Se a caixa de texto tiver o foco de entrada padrão, o prompt será exibido e desaparece quando o usuário começa a digitar.</span><span class="sxs-lookup"><span data-stu-id="0323c-299">**Exception:** If the text box has default input focus, the prompt is displayed, and it disappears once the user starts typing.</span></span>
-   <span data-ttu-id="0323c-300">O texto do prompt será restaurado se a caixa de texto ainda estiver vazia quando perder o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="0323c-300">The prompt text is restored if the text box is still empty when it loses input focus.</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="0323c-301">Dimensionamento e espaçamento recomendados</span><span class="sxs-lookup"><span data-stu-id="0323c-301">Recommended sizing and spacing</span></span>

![<span data-ttu-id="0323c-302">Figura de caixas de texto de uma linha e de duas linhas</span><span class="sxs-lookup"><span data-stu-id="0323c-302">figure of one-line and two-line text boxes</span></span> ](images/ctrl-text-boxes-image25.png)

<span data-ttu-id="0323c-303">Dimensionamento e espaçamento recomendados para caixas de texto.</span><span class="sxs-lookup"><span data-stu-id="0323c-303">Recommended sizing and spacing for text boxes.</span></span>

<span data-ttu-id="0323c-304">A largura de uma caixa de texto é uma pista visual do tamanho de entrada esperado.</span><span class="sxs-lookup"><span data-stu-id="0323c-304">The width of a text box is a visual clue of the expected input size.</span></span> <span data-ttu-id="0323c-305">Ao dimensionar caixas de texto:</span><span class="sxs-lookup"><span data-stu-id="0323c-305">When sizing text boxes:</span></span>

-   <span data-ttu-id="0323c-306">**Escolha uma largura apropriada para os dados válidos mais longos.**</span><span class="sxs-lookup"><span data-stu-id="0323c-306">**Choose a width appropriate for the longest valid data.**</span></span> <span data-ttu-id="0323c-307">Na maioria das situações, os usuários não precisam rolar a cadeia de caracteres mais longa provável que eles inserirão ou exibirão.</span><span class="sxs-lookup"><span data-stu-id="0323c-307">In most situations, users shouldn't have to scroll the longest likely string they'll enter or view.</span></span>
-   <span data-ttu-id="0323c-308">**Inclua mais 30%** (até 200 por cento para texto mais curto) para qualquer texto (mas não números) que serão localizados.</span><span class="sxs-lookup"><span data-stu-id="0323c-308">**Include an additional 30 percent** (up to 200 percent for shorter text) for any text (but not numbers) that will be localized.</span></span>
-   <span data-ttu-id="0323c-309">**Se a entrada esperada não tiver um tamanho específico, escolha uma largura consistente com as outras caixas de texto ou controles na janela.**</span><span class="sxs-lookup"><span data-stu-id="0323c-309">**If the expected input has no particular size, choose a width that is consistent with the other text boxes or controls on the window.**</span></span>
-   <span data-ttu-id="0323c-310">**Dimensione as caixas de texto de várias linhas para exibir um número integral de linhas de texto.**</span><span class="sxs-lookup"><span data-stu-id="0323c-310">**Size multi-line text boxes to display an integral number of lines of text.**</span></span>

## <a name="labels"></a><span data-ttu-id="0323c-311">Rótulos</span><span class="sxs-lookup"><span data-stu-id="0323c-311">Labels</span></span>

### <a name="text-box-labels"></a><span data-ttu-id="0323c-312">Rótulos da caixa de texto</span><span class="sxs-lookup"><span data-stu-id="0323c-312">Text box labels</span></span>

-   <span data-ttu-id="0323c-313">Todas as caixas de texto precisam de rótulos.</span><span class="sxs-lookup"><span data-stu-id="0323c-313">All text boxes need labels.</span></span> <span data-ttu-id="0323c-314">Grave o rótulo como uma palavra ou frase, não como uma frase, terminando com dois-pontos e usando [texto estático](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="0323c-314">Write the label as a word or phrase, not as a sentence, ending with a colon, and using [static text](glossary.md).</span></span>

    <span data-ttu-id="0323c-315">**Exceção**</span><span class="sxs-lookup"><span data-stu-id="0323c-315">**Exceptions:**</span></span>

    -   <span data-ttu-id="0323c-316">Caixas de texto com prompts localizados onde o espaço está em uma parte Premium.</span><span class="sxs-lookup"><span data-stu-id="0323c-316">Text boxes with prompts located where space is at a premium.</span></span>
    -   <span data-ttu-id="0323c-317">Para rotulagem, um grupo de caixas de texto usado para **entrada de dados formatados** deve ser tratado como uma única caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="0323c-317">For labeling, a group of text boxes used for **formatted data input** should be treated as a single text box.</span></span>
    -   <span data-ttu-id="0323c-318">Se uma caixa de texto for subordinada a um botão de opção ou caixa de seleção e for introduzida por seu rótulo que termina com dois-pontos, não coloque um rótulo adicional na caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="0323c-318">If a text box is subordinate to a radio button or check box, and is introduced by its label ending with a colon, don't put an additional label on the text box.</span></span>
    -   <span data-ttu-id="0323c-319">**Omita os rótulos de controle que redefinem a instrução principal.**</span><span class="sxs-lookup"><span data-stu-id="0323c-319">**Omit control labels that restate the main instruction.**</span></span> <span data-ttu-id="0323c-320">Nesse caso, a instrução principal leva os dois-pontos (a menos que seja uma pergunta) e a chave de acesso.</span><span class="sxs-lookup"><span data-stu-id="0323c-320">In this case, the main instruction takes the colon (unless it's a question) and access key.</span></span>

        <span data-ttu-id="0323c-321">**Aceitável:**</span><span class="sxs-lookup"><span data-stu-id="0323c-321">**Acceptable:**</span></span>

        ![captura de tela da caixa de texto com o rótulo redundante](images/ctrl-text-boxes-image26.png)

        <span data-ttu-id="0323c-323">Neste exemplo, o rótulo da caixa de texto é apenas uma recondição da instrução principal.</span><span class="sxs-lookup"><span data-stu-id="0323c-323">In this example, the text box label is just a restatement of the main instruction.</span></span>

        <span data-ttu-id="0323c-324">**Melhor:**</span><span class="sxs-lookup"><span data-stu-id="0323c-324">**Better:**</span></span>

        ![<span data-ttu-id="0323c-325">captura de tela da caixa de texto com a instrução Main somente</span><span class="sxs-lookup"><span data-stu-id="0323c-325">screen shot of text box with main instruction only</span></span> ](images/ctrl-text-boxes-image27.png)

        <span data-ttu-id="0323c-326">Neste exemplo, o rótulo redundante é removido e, portanto, a instrução Main usa a tecla de acesso e os dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="0323c-326">In this example, the redundant label is removed, so the main instruction takes the colon and access key.</span></span>

-   <span data-ttu-id="0323c-327">Atribua uma chave de acesso exclusiva.</span><span class="sxs-lookup"><span data-stu-id="0323c-327">Assign a unique access key.</span></span> <span data-ttu-id="0323c-328">Para obter diretrizes de atribuição de chave de acesso, consulte [teclado](inter-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="0323c-328">For access key assignment guidelines, see [Keyboard](inter-keyboard.md).</span></span>
-   <span data-ttu-id="0323c-329">Use a capitalização com estilo de frase.</span><span class="sxs-lookup"><span data-stu-id="0323c-329">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="0323c-330">Posicione o rótulo à esquerda ou acima da caixa de texto e alinhe o rótulo à borda esquerda da caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="0323c-330">Position the label either to the left of or above the text box, and align the label with the left edge of the text box.</span></span> <span data-ttu-id="0323c-331">Se o rótulo estiver à esquerda, alinhe verticalmente o texto do rótulo com o texto da caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="0323c-331">If the label is on the left, vertically align the label text with the text box text.</span></span>

    <span data-ttu-id="0323c-332">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="0323c-332">**Correct:**</span></span>

    ![<span data-ttu-id="0323c-333">captura de tela do rótulo alinhado à esquerda acima da caixa de texto</span><span class="sxs-lookup"><span data-stu-id="0323c-333">screen shot of left-aligned label above text box</span></span> ](images/ctrl-text-boxes-image28.png)

    ![<span data-ttu-id="0323c-334">captura de tela do rótulo alinhado por texto à esquerda da caixa de texto</span><span class="sxs-lookup"><span data-stu-id="0323c-334">screen shot of text-aligned label left of text box</span></span> ](images/ctrl-text-boxes-image29.png)

    <span data-ttu-id="0323c-335">Nesses exemplos, o rótulo na parte superior alinha com a borda esquerda da caixa de texto e o rótulo à esquerda é alinhado com o texto na caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="0323c-335">In these examples, the label on top aligns with the left edge of the text box, and the label on the left aligns with the text in the text box.</span></span>

    <span data-ttu-id="0323c-336">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="0323c-336">**Incorrect:**</span></span>

    ![<span data-ttu-id="0323c-337">captura de tela de rótulo alinhado por texto acima da caixa de texto</span><span class="sxs-lookup"><span data-stu-id="0323c-337">screen shot of text-aligned label above text box</span></span> ](images/ctrl-text-boxes-image30.png)

    ![<span data-ttu-id="0323c-338">captura de tela do rótulo alinhado na parte superior esquerda da caixa de texto</span><span class="sxs-lookup"><span data-stu-id="0323c-338">screen shot of top-aligned label left of text box</span></span> ](images/ctrl-text-boxes-image31.png)

    <span data-ttu-id="0323c-339">Nesses exemplos incorretos, o rótulo na parte superior alinha com o texto na caixa de texto e o rótulo à esquerda é alinhado com a parte superior da caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="0323c-339">In these incorrect examples, the label on top aligns with the text in the text box, and the label on the left aligns with the top of the text box.</span></span>

-   <span data-ttu-id="0323c-340">Você pode especificar unidades (por exemplo, segundos ou conexões) entre parênteses após o rótulo.</span><span class="sxs-lookup"><span data-stu-id="0323c-340">You may specify units (for example, seconds or connections) in parentheses after the label.</span></span>
-   <span data-ttu-id="0323c-341">Se uma caixa de texto aceitar um número máximo de caracteres arbitrariamente pequeno, você poderá indicar a entrada máxima no rótulo.</span><span class="sxs-lookup"><span data-stu-id="0323c-341">If a text box accepts an arbitrarily small maximum number of characters, you can state the maximum input in the label.</span></span> <span data-ttu-id="0323c-342">A largura da caixa de texto também deve sugerir o tamanho máximo.</span><span class="sxs-lookup"><span data-stu-id="0323c-342">The text box width should also suggest the maximum size.</span></span>

    ![<span data-ttu-id="0323c-343">captura de tela da caixa de texto de senha</span><span class="sxs-lookup"><span data-stu-id="0323c-343">screen shot of password text box</span></span> ](images/ctrl-text-boxes-image32.png)

    <span data-ttu-id="0323c-344">Neste exemplo, o rótulo fornece o número máximo de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0323c-344">In this example, the label gives the maximum number of characters.</span></span>

-   <span data-ttu-id="0323c-345">Não faça com que o conteúdo da caixa de texto (ou seu rótulo de unidade) faça parte de uma frase, pois isso não é localizável.</span><span class="sxs-lookup"><span data-stu-id="0323c-345">Don't make the content of the text box (or its units label) part of a sentence, because this is not localizable.</span></span>
-   <span data-ttu-id="0323c-346">Se a caixa de texto puder ser usada para inserir vários itens, deixe claro como separar os itens no rótulo.</span><span class="sxs-lookup"><span data-stu-id="0323c-346">If the text box can be used to enter several items, make it clear how to separate the items in the label.</span></span>

    ![<span data-ttu-id="0323c-347">captura de tela de nomes separados por rótulo com ponto e vírgula</span><span class="sxs-lookup"><span data-stu-id="0323c-347">screen shot of label separate names with semicolon</span></span> ](images/ctrl-text-boxes-image33.png)

    <span data-ttu-id="0323c-348">Neste exemplo, o separador de item é fornecido no rótulo.</span><span class="sxs-lookup"><span data-stu-id="0323c-348">In this example, the item separator is given in the label.</span></span>

-   <span data-ttu-id="0323c-349">Para obter diretrizes sobre como indicar a entrada necessária, consulte entrada necessária nas [caixas de diálogo](win-dialog-box.md).</span><span class="sxs-lookup"><span data-stu-id="0323c-349">For guidelines on indicating required input, see Required input in [Dialog Boxes](win-dialog-box.md).</span></span>

### <a name="instruction-labels"></a><span data-ttu-id="0323c-350">Rótulos de instrução</span><span class="sxs-lookup"><span data-stu-id="0323c-350">Instruction labels</span></span>

-   <span data-ttu-id="0323c-351">Se você precisar adicionar texto de instrução sobre uma caixa de texto, adicione-a acima do rótulo.</span><span class="sxs-lookup"><span data-stu-id="0323c-351">If you need to add instructional text about a text box, add it above the label.</span></span> <span data-ttu-id="0323c-352">Use frases completas com pontuação final.</span><span class="sxs-lookup"><span data-stu-id="0323c-352">Use complete sentences with ending punctuation.</span></span>
-   <span data-ttu-id="0323c-353">Use a capitalização com estilo de frase.</span><span class="sxs-lookup"><span data-stu-id="0323c-353">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="0323c-354">Informações adicionais que são úteis, mas não necessárias, devem ser mantidas curtas.</span><span class="sxs-lookup"><span data-stu-id="0323c-354">Additional information that is helpful but not necessary should be kept short.</span></span> <span data-ttu-id="0323c-355">Coloque essas informações entre parênteses entre o rótulo e os dois-pontos ou sem parênteses abaixo da caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="0323c-355">Place this information either in parentheses between the label and colon, or without parentheses below the text box.</span></span>

    ![<span data-ttu-id="0323c-356">captura de tela de informações adicionadas abaixo da caixa de texto</span><span class="sxs-lookup"><span data-stu-id="0323c-356">screen shot of added information below text box</span></span> ](images/ctrl-text-boxes-image34.png)

    <span data-ttu-id="0323c-357">Neste exemplo, informações adicionais são colocadas abaixo da caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="0323c-357">In this example, additional information is placed below the text box.</span></span>

### <a name="prompt-labels"></a><span data-ttu-id="0323c-358">Rótulos de prompt</span><span class="sxs-lookup"><span data-stu-id="0323c-358">Prompt labels</span></span>

-   <span data-ttu-id="0323c-359">Mantenha o texto do prompt conciso.</span><span class="sxs-lookup"><span data-stu-id="0323c-359">Keep the prompt text concise.</span></span> <span data-ttu-id="0323c-360">Você pode usar fragmentos em vez de frases completas.</span><span class="sxs-lookup"><span data-stu-id="0323c-360">You can use fragments instead of full sentences.</span></span>
-   <span data-ttu-id="0323c-361">Use a capitalização com estilo de frase.</span><span class="sxs-lookup"><span data-stu-id="0323c-361">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="0323c-362">Não use pontuação final ou reticências.</span><span class="sxs-lookup"><span data-stu-id="0323c-362">Don't use ending punctuation or ellipsis.</span></span>
-   <span data-ttu-id="0323c-363">Se o prompt instrui os usuários a inserir informações que serão acionadas por um botão ao lado da caixa de texto, basta posicionar o botão ao lado da caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="0323c-363">If the prompt directs users to enter information that will be acted upon by a button next to the text box, simply place the button next to the text box.</span></span> <span data-ttu-id="0323c-364">Não use o prompt para direcionar os usuários a clicar no botão (por exemplo, não escreva o texto do prompt que diz, arraste um arquivo e clique em enviar).</span><span class="sxs-lookup"><span data-stu-id="0323c-364">Don't use the prompt to direct users to click the button (for example, don't write prompt text that says, Drag a file and then click Send).</span></span>

## <a name="documentation"></a><span data-ttu-id="0323c-365">Documentação</span><span class="sxs-lookup"><span data-stu-id="0323c-365">Documentation</span></span>

<span data-ttu-id="0323c-366">Ao fazer referência a caixas de texto:</span><span class="sxs-lookup"><span data-stu-id="0323c-366">When referring to text boxes:</span></span>

-   <span data-ttu-id="0323c-367">Use tipo para se referir a interações do usuário que exigem digitação ou colagem; caso contrário, use Enter se os usuários puderem colocar informações na caixa de texto usando outros meios, como selecionar o valor de uma lista ou usar um botão de procura.</span><span class="sxs-lookup"><span data-stu-id="0323c-367">Use type to refer to user interactions that require typing or pasting; otherwise use enter if users can put information into the text box using other means, such as selecting the value from a list or using a Browse button.</span></span>
-   <span data-ttu-id="0323c-368">Use Selecionar para se referir a uma entrada em uma caixa de texto somente leitura.</span><span class="sxs-lookup"><span data-stu-id="0323c-368">Use select to refer to an entry in a read-only text box.</span></span>
-   <span data-ttu-id="0323c-369">Use o texto exato do rótulo, incluindo sua capitalização e inclua a caixa palavra.</span><span class="sxs-lookup"><span data-stu-id="0323c-369">Use the exact label text, including its capitalization, and include the word box.</span></span> <span data-ttu-id="0323c-370">Não inclua a tecla de acesso sublinhado ou dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="0323c-370">Don't include the access key underscore or colon.</span></span> <span data-ttu-id="0323c-371">Não faça referência a uma caixa de texto como uma caixa de texto ou um campo.</span><span class="sxs-lookup"><span data-stu-id="0323c-371">Don't refer to a text box as a text box or a field.</span></span>
-   <span data-ttu-id="0323c-372">Quando possível, formate o rótulo usando texto em negrito.</span><span class="sxs-lookup"><span data-stu-id="0323c-372">When possible, format the label using bold text.</span></span> <span data-ttu-id="0323c-373">Caso contrário, coloque o rótulo entre aspas somente se necessário para evitar confusão.</span><span class="sxs-lookup"><span data-stu-id="0323c-373">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>

    <span data-ttu-id="0323c-374">Exemplo: digite sua senha na caixa **senha** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="0323c-374">Example: Type your password into the **Password** box, and then click **OK**.</span></span>

-   <span data-ttu-id="0323c-375">Se a caixa de texto exigir um formato específico, documente apenas o formato aceitável mais comumente usado.</span><span class="sxs-lookup"><span data-stu-id="0323c-375">If the text box requires a specific format, document only the most commonly used acceptable format.</span></span> <span data-ttu-id="0323c-376">Permita que os usuários descubram outros formatos por conta própria.</span><span class="sxs-lookup"><span data-stu-id="0323c-376">Let users discover any other formats on their own.</span></span> <span data-ttu-id="0323c-377">Você deseja ser flexível com formatos de dados, mas fazer isso não deve resultar em documentação complexa.</span><span class="sxs-lookup"><span data-stu-id="0323c-377">You want to be flexible with data formats, but doing so should not result in complex documentation.</span></span>

    <span data-ttu-id="0323c-378">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="0323c-378">**Correct:**</span></span>

    <span data-ttu-id="0323c-379">Insira o número de série da parte usando o formato 1234-56-7890.</span><span class="sxs-lookup"><span data-stu-id="0323c-379">Enter the part's serial number using the 1234-56-7890 format.</span></span>

    <span data-ttu-id="0323c-380">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="0323c-380">**Incorrect:**</span></span>

    <span data-ttu-id="0323c-381">Insira o número de série da parte usando qualquer um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="0323c-381">Enter the part's serial number using any of the following formats:</span></span>

    <span data-ttu-id="0323c-382">1234567890</span><span class="sxs-lookup"><span data-stu-id="0323c-382">1234567890</span></span>

    <span data-ttu-id="0323c-383">1234-56-7890</span><span class="sxs-lookup"><span data-stu-id="0323c-383">1234-56-7890</span></span>

    <span data-ttu-id="0323c-384">1234 56 7890</span><span class="sxs-lookup"><span data-stu-id="0323c-384">1234 56 7890</span></span>

