---
title: Rotinas de verificação
description: Esta seção descreve as rotinas de verificação que o verificador de acessibilidade da interface do usuário pode executar para testar a implementação de acessibilidade de um aplicativo.
ms.assetid: 0ff38f83-5741-4c0e-a070-a8385f95eba3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78eea821a4c918078c6390e33fa7046de1452f76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292243"
---
# <a name="verification-routines"></a><span data-ttu-id="bd2f1-103">Rotinas de verificação</span><span class="sxs-lookup"><span data-stu-id="bd2f1-103">Verification Routines</span></span>

<span data-ttu-id="bd2f1-104">Esta seção descreve as rotinas de verificação que o verificador de acessibilidade da interface do usuário pode executar para testar a implementação de acessibilidade de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-104">This section describes the verification routines that UI Accessibility Checker can run to test an application's accessibility implementation.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bd2f1-105">Categoria</span><span class="sxs-lookup"><span data-stu-id="bd2f1-105">Category</span></span></th>
<th><span data-ttu-id="bd2f1-106">Rotina</span><span class="sxs-lookup"><span data-stu-id="bd2f1-106">Routine</span></span></th>
<th><span data-ttu-id="bd2f1-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="bd2f1-107">Description</span></span></th>
</tr><span data-ttu-id="bd2f1-108">
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><strong>Consistência</strong>$ {remove} $</span><span class="sxs-lookup"><span data-stu-id="bd2f1-108">
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><strong>Consistency</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="bd2f1-109"><strong>ScreenReader</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-109"><strong>ScreenReader</strong></span></span></td>
<td><span data-ttu-id="bd2f1-110">Compila todos os elementos visíveis no destino de verificação e os exibe em um controle ListView na ordem em que um leitor de tela padrão os anuncia para um usuário.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-110">Compiles all visible elements in the verification target and displays them in a ListView control in the order that a standard screen reader announces them to a user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd2f1-111"><strong>UiaScreenReader</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-111"><strong>UiaScreenReader</strong></span></span></td>
<td><span data-ttu-id="bd2f1-112">O mesmo que <strong>ScreenReader</strong>, mas para implementações UIA.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-112">Same as <strong>ScreenReader</strong>, but for UIA implementations.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="bd2f1-113"><strong>Navegação</strong>$ {remove} $</span><span class="sxs-lookup"><span data-stu-id="bd2f1-113"><strong>Navigation</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="bd2f1-114"><strong>CheckTreeDepth</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-114"><strong>CheckTreeDepth</strong></span></span></td>
<td><span data-ttu-id="bd2f1-115">Envia caracteres de tabulação (ou Shift + Tab) como entrada para o destino de verificação para confirmar se a interface do usuário do destino não é excessivamente complexa ou inacessível usando a navegação de teclado padrão.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-115">Sends Tab (or Shift+Tab) characters as input to the verification target to confirm that the target's UI isn't overly complex or inaccessible using standard keyboard navigation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd2f1-116"><strong>CheckTabbingUia</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-116"><strong>CheckTabbingUia</strong></span></span></td>
<td><span data-ttu-id="bd2f1-117">Envia caracteres de tabulação (ou Shift + Tab) como entrada para o destino de verificação para confirmar se todos os elementos que podem ser focados na interface do usuário são acessíveis de maneira ordenada e lógica usando a navegação de teclado padrão.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-117">Sends Tab (or Shift+Tab) characters as input to the verification target to confirm that all focusable elements in the UI are reachable in an orderly, logical fashion using standard keyboard navigation.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="5"><span data-ttu-id="bd2f1-118"><strong>Propriedades</strong>$ {remove} $</span><span class="sxs-lookup"><span data-stu-id="bd2f1-118"><strong>Properties</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="bd2f1-119"><strong>CheckRole</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-119"><strong>CheckRole</strong></span></span></td>
<td><span data-ttu-id="bd2f1-120">Confirma que cada elemento focado na interface do usuário relata uma função de MSAA lógica válida e que o controle tem um valor conforme exigido por essa função.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-120">Confirms that each focusable element in the UI reports a valid, logical MSAA role, and that the control has a value as required by that role.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd2f1-121"><strong>CheckState</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-121"><strong>CheckState</strong></span></span></td>
<td><span data-ttu-id="bd2f1-122">Confirma que cada elemento focado na interface do usuário relata um estado de MSAA lógico válido.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-122">Confirms that each focusable element in the UI reports a valid, logical MSAA state.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="bd2f1-123"><strong>CHECKNAME</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-123"><strong>CheckName</strong></span></span></td>
<td><span data-ttu-id="bd2f1-124">Confirma que cada elemento focado na interface do usuário relata um nome de MSAA lógico válido.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-124">Confirms that each focusable element in the UI reports a valid, logical MSAA name.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="bd2f1-125"><strong>CheckAccessKeys</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-125"><strong>CheckAccessKeys</strong></span></span></td>
<td><span data-ttu-id="bd2f1-126">Confirma que as chaves de acesso atribuídas a elementos no destino de verificação são exclusivas dentro do destino de verificação.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-126">Confirms that access keys that are assigned to elements in the verification target are unique within the verification target.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="bd2f1-127"><strong>CheckBoundingRect</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-127"><strong>CheckBoundingRect</strong></span></span></td>
<td><span data-ttu-id="bd2f1-128">Confirma que cada elemento focado na interface do usuário tem um retângulo delimitador que pode ser usado como um destino para teste de clique.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-128">Confirms that each focusable element in the UI has a bounding rectangle that can be used as a target for hit testing.</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="bd2f1-129"><strong>Árvore</strong>$ {remove} $</span><span class="sxs-lookup"><span data-stu-id="bd2f1-129"><strong>Tree</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="bd2f1-130"><strong>CheckParentChild</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-130"><strong>CheckParentChild</strong></span></span></td>
<td><span data-ttu-id="bd2f1-131">As relações pai e filho na árvore de elementos são consistentes e previsíveis.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-131">Parent and child relationships in the element tree are consistent and predictable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd2f1-132"><strong>CheckOrphanChildren</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-132"><strong>CheckOrphanChildren</strong></span></span></td>
<td><span data-ttu-id="bd2f1-133">Confirma que cada elemento focado na interface do usuário relata um pai de MSAA válido.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-133">Confirms that each focusable element in the UI reports a valid MSAA parent.</span></span></td>

</tr>
<tr class="even">
<td rowspan="6"><span data-ttu-id="bd2f1-134"><strong>Propriedades UIA</strong>$ {remove} $</span><span class="sxs-lookup"><span data-stu-id="bd2f1-134"><strong>UIA Properties</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="bd2f1-135"><strong>CheckNameUIA</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-135"><strong>CheckNameUIA</strong></span></span></td>
<td><span data-ttu-id="bd2f1-136">Confirma que cada elemento focado na interface do usuário relata um nome de UIA lógico válido.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-136">Confirms that each focusable element in the UI reports a valid, logical UIA name.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd2f1-137"><strong>CheckTreeDepthUIA</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-137"><strong>CheckTreeDepthUIA</strong></span></span></td>
<td><span data-ttu-id="bd2f1-138">Envia caracteres de tabulação (ou Shift + Tab) como entrada para o destino de verificação para confirmar que os elementos UIA na interface do usuário de destino não são excessivamente complexos ou inacessíveis usando a navegação de teclado padrão.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-138">Sends Tab (or Shift+Tab) characters as input to the verification target to confirm that to UIA elements in the target's UI aren't overly complex or inaccessible using standard keyboard navigation.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="bd2f1-139"><strong>CheckStateUIA</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-139"><strong>CheckStateUIA</strong></span></span></td>
<td><span data-ttu-id="bd2f1-140">Confirma que cada elemento focado na interface do usuário relata um estado de UIA lógico válido.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-140">Confirms that each focusable element in the UI reports a valid, logical UIA state.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="bd2f1-141"><strong>CheckAccessKeysUIA</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-141"><strong>CheckAccessKeysUIA</strong></span></span></td>
<td><span data-ttu-id="bd2f1-142">Confirma que os elementos irmãos não têm a mesma chave de acesso e/ou acelerador.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-142">Confirms that sibling elements do not have the same access and/or accelerator key.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="bd2f1-143"><strong>CheckBoundingRectUIA</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-143"><strong>CheckBoundingRectUIA</strong></span></span></td>
<td><span data-ttu-id="bd2f1-144">Confirma que cada elemento UIA com foco na interface do usuário tem um retângulo delimitador que pode ser usado como um destino para teste de clique.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-144">Confirms that each focusable UIA element in the UI has a bounding rectangle that can be used as a target for hit testing.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="bd2f1-145"><strong>CheckControlTypeUIA</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-145"><strong>CheckControlTypeUIA</strong></span></span></td>
<td><span data-ttu-id="bd2f1-146">Confirma que cada elemento focado na interface do usuário relata um tipo de controle UIA lógico válido.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-146">Confirms that each focusable element in the UI reports a valid, logical UIA control type.</span></span></td>

</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="bd2f1-147"><strong>Árvore UIA</strong>$ {remove} $</span><span class="sxs-lookup"><span data-stu-id="bd2f1-147"><strong>UIA Tree</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="bd2f1-148"><strong>CheckNavigateUia</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-148"><strong>CheckNavigateUia</strong></span></span></td>
<td><span data-ttu-id="bd2f1-149">Confirma que o UIA TreeWalker pode navegar pelos filhos de um elemento.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-149">Confirms that the UIA TreeWalker can navigate through an element's children.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd2f1-150"><strong>CheckOrphanChildrenUia</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-150"><strong>CheckOrphanChildrenUia</strong></span></span></td>
<td><span data-ttu-id="bd2f1-151">Confirma que cada elemento focado na interface do usuário relata um pai de UIA válido.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-151">Confirms that each focusable element in the UI reports a valid UIA parent.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="bd2f1-152"><strong>CheckSiblingsUia</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-152"><strong>CheckSiblingsUia</strong></span></span></td>
<td><span data-ttu-id="bd2f1-153">Confirma que os elementos irmãos não têm o mesmo nome: pares ControlType, nem o mesmo AutomationId.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-153">Confirms that sibling elements do not have the same Name:ControlType pairs, nor the same AutomationId's.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="bd2f1-154">$ {ROWSPAN9} $<strong>verificações na Web do Aria</strong>$ {remover} $</span><span class="sxs-lookup"><span data-stu-id="bd2f1-154">${ROWSPAN9}$<strong>ARIA Web Verifications</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="bd2f1-155"><strong>CheckARIARole</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-155"><strong>CheckARIARole</strong></span></span></td>
<td><span data-ttu-id="bd2f1-156">Confirma que todos os elementos têm uma função do ARIA válida.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-156">Confirms that all elements have a valid ARIA role.</span></span> <span data-ttu-id="bd2f1-157">A marca HTML associada e a função do ARIA são elementos de informações com funções inválidas sinalizadas como erros.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-157">The associated HTML tag and ARIA role are information elements with invalid roles flagged as errors.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd2f1-158"><strong>CheckLabel</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-158"><strong>CheckLabel</strong></span></span></td>
<td><span data-ttu-id="bd2f1-159">Confirma que cada elemento com entrada, botão, imagem-botão ou função de ponto de referência tem um rótulo.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-159">Confirms each element with input, button, image-button, or landmark role has a label.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="bd2f1-160"><strong>CheckRangeControls</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-160"><strong>CheckRangeControls</strong></span></span></td>
<td><span data-ttu-id="bd2f1-161">Confirma que os controles de intervalo com a função de barra deslizante ou de progresso têm atributos apropriados do ARIA definidos.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-161">Confirms range controls with slider or progress bar role have proper ARIA attributes defined.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="bd2f1-162"><strong>CheckContainerRole</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-162"><strong>CheckContainerRole</strong></span></span></td>
<td><span data-ttu-id="bd2f1-163">Confirma um elemento ou pelo menos um de seus filhos, tem OnKeyDown/OnKeyPress definido.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-163">Confirms an element, or at least one of its children, has onkeydown/onkeypress defined.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="bd2f1-164"><strong>CheckLayoutTable</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-164"><strong>CheckLayoutTable</strong></span></span></td>
<td><span data-ttu-id="bd2f1-165">Confirma que um layout de tabela tem um resumo/th/Aria-DescribedBy incluído.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-165">Confirms a table layout has a summary/th/aria-describedby included.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="bd2f1-166"><strong>CheckGridStructure</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-166"><strong>CheckGridStructure</strong></span></span></td>
<td><span data-ttu-id="bd2f1-167">Confirma que um elemento que não é de tabela com a função de grade tem uma estrutura de grade>linha>gridcell com atributos associados.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-167">Confirms a non-table element with grid role has a structure of grid>row>gridcell with associated attributes.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="bd2f1-168"><strong>CheckDataTable</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-168"><strong>CheckDataTable</strong></span></span></td>
<td><span data-ttu-id="bd2f1-169">Confirma as propriedades das tabelas de dados.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-169">Confirms the properties of data tables.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="bd2f1-170"><strong>CheckActiveDescendants</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-170"><strong>CheckActiveDescendants</strong></span></span></td>
<td><span data-ttu-id="bd2f1-171">Confirma as propriedades dos elementos com um descendente ativo definido.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-171">Confirms the properties of elements with an active descendant defined.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="bd2f1-172"><strong>CheckElementsWithClickHandler</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-172"><strong>CheckElementsWithClickHandler</strong></span></span></td>
<td><span data-ttu-id="bd2f1-173">Confirma o índice de tabulação dos elementos com manipuladores de clique.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-173">Confirms the tab index of elements with click handlers.</span></span></td>

</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="bd2f1-174"><strong>Verificações na Web</strong>$ {remove} $</span><span class="sxs-lookup"><span data-stu-id="bd2f1-174"><strong>Web Verifications</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="bd2f1-175"><strong>CheckHtml (Web)</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-175"><strong>CheckHtml (Web)</strong></span></span></td>
<td><span data-ttu-id="bd2f1-176">Confirma várias características de HTML, como cabeçalhos, nome, quadros e títulos.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-176">Confirms various HTML characteristics such as headers, name, frames, and titles.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd2f1-177"><strong>CHECKNAME (Web)</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-177"><strong>CheckName (Web)</strong></span></span></td>
<td><span data-ttu-id="bd2f1-178">Confirma características de nome, como comprimento, caracteres inválidos e inclusão de função.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-178">Confirms name characteristics such as length, invalid characters, and role inclusion.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="bd2f1-179"><strong>CheckRole (Web)</strong></span><span class="sxs-lookup"><span data-stu-id="bd2f1-179"><strong>CheckRole (Web)</strong></span></span></td>
<td><span data-ttu-id="bd2f1-180">Confirma funções inválidas, funções que devem ter valores e/ou funções não implementadas.</span><span class="sxs-lookup"><span data-stu-id="bd2f1-180">Confirms invalid roles, roles that should have values, and/or roles not implemented.</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="bd2f1-181">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bd2f1-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd2f1-182">UI Accessibility Checker</span><span class="sxs-lookup"><span data-stu-id="bd2f1-182">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




