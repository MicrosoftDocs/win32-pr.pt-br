---
title: Verificação de automação da interface do usuário Visual
description: Verificação de automação da interface do usuário Visual (verificação de UIA Visual) é um Windows \ 32; Driver de GUI para a biblioteca de teste UIA projetada para teste manual da automação da interface do usuário.
ms.assetid: 8AEB083E-785E-4F15-B708-2098A9A41B4E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96e224a52d243427af86c6cd27a3add3be03d9b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636992"
---
# <a name="visual-ui-automation-verify"></a><span data-ttu-id="4cc9a-103">Verificação de automação da interface do usuário Visual</span><span class="sxs-lookup"><span data-stu-id="4cc9a-103">Visual UI Automation Verify</span></span>

<span data-ttu-id="4cc9a-104">A verificação de automação da interface do usuário Visual (verificação do Visual UIA) é um driver de GUI do Windows para a biblioteca de teste UIA, projetada para teste manual da automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-104">Visual UI Automation Verify (Visual UIA Verify) is a Windows GUI driver for the UIA Test Library that is designed for manual testing of UI automation.</span></span> <span data-ttu-id="4cc9a-105">Ele fornece uma interface para a funcionalidade de biblioteca de teste UIA que elimina a sobrecarga de codificação de uma ferramenta de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-105">It provides an interface to UIA Test Library functionality that eliminates the coding overhead of a command-line tool.</span></span>

-   [<span data-ttu-id="4cc9a-106">Comandos de menu</span><span class="sxs-lookup"><span data-stu-id="4cc9a-106">Menu Commands</span></span>](#menu-commands)
-   [<span data-ttu-id="4cc9a-107">Painéis funcionais</span><span class="sxs-lookup"><span data-stu-id="4cc9a-107">Functional Panes</span></span>](#functional-panes)
    -   [<span data-ttu-id="4cc9a-108">Painel de árvore de elementos de automação</span><span class="sxs-lookup"><span data-stu-id="4cc9a-108">Automation Elements Tree Pane</span></span>](#automation-elements-tree-pane)
    -   [<span data-ttu-id="4cc9a-109">Painel de testes</span><span class="sxs-lookup"><span data-stu-id="4cc9a-109">Tests Pane</span></span>](#tests-pane)
    -   [<span data-ttu-id="4cc9a-110">Painel de resultados de testes</span><span class="sxs-lookup"><span data-stu-id="4cc9a-110">Test Results Pane</span></span>](#test-results-pane)
    -   [<span data-ttu-id="4cc9a-111">Painel Propriedades</span><span class="sxs-lookup"><span data-stu-id="4cc9a-111">Properties Pane</span></span>](#properties-pane)

<span data-ttu-id="4cc9a-112">A verificação de UIA Visual dá suporte apenas à verificação de UIA de agente XML (WUIALoggerXml.dll) nativamente.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-112">Visual UIA Verify supports only the UIA Verify XML logger (WUIALoggerXml.dll) natively.</span></span> <span data-ttu-id="4cc9a-113">As transformações XML selecionáveis pelo usuário são incorporadas à verificação de UIA Visual para apresentar várias exibições do relatório do agente de log XML no painel de **resultados de teste** .</span><span class="sxs-lookup"><span data-stu-id="4cc9a-113">User-selectable XML transformations are incorporated into Visual UIA Verify to present various views of the XML logger report in the **Test Results** pane.</span></span>

<span data-ttu-id="4cc9a-114">Por padrão, o Visual UIA Verify carrega o provedor do lado do cliente de automação da interface do usuário fornecido com a versão original da automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-114">By default, Visual UIA Verify loads the UI Automation client-side provider that shipped with the original release of UI Automation.</span></span> <span data-ttu-id="4cc9a-115">Você pode optar por não carregar esse provedor adicionando **/NOCLIENTSIDEPROVIDER** na opção de linha de comando de VisualUIVerifyNative.exe.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-115">You can choose not to load this provider by adding **/NOCLIENTSIDEPROVIDER** in the command-line option of VisualUIVerifyNative.exe.</span></span>

<span data-ttu-id="4cc9a-116">A captura de tela a seguir mostra as principais áreas funcionais da interface do usuário do Visual UIA Verify.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-116">The following screen shot shows the main functional areas of the Visual UIA Verify user interface.</span></span>

![principais áreas funcionais da interface do usuário de verificação do Visual UIA](images/visual-uia-verify-ui.png)

## <a name="menu-commands"></a><span data-ttu-id="4cc9a-118">Comandos de menu</span><span class="sxs-lookup"><span data-stu-id="4cc9a-118">Menu Commands</span></span>

<span data-ttu-id="4cc9a-119">A tabela a seguir descreve os comandos no menu verificar do Visual UIA.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-119">The following table describes the commands in the Visual UIA Verify menu.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4cc9a-120">Menu</span><span class="sxs-lookup"><span data-stu-id="4cc9a-120">Menu</span></span></th>
<th><span data-ttu-id="4cc9a-121">Comando</span><span class="sxs-lookup"><span data-stu-id="4cc9a-121">Command</span></span></th>
<th><span data-ttu-id="4cc9a-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="4cc9a-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4cc9a-123"><strong>Arquivo</strong></span><span class="sxs-lookup"><span data-stu-id="4cc9a-123"><strong>File</strong></span></span></td>
<td><span data-ttu-id="4cc9a-124"><strong>Sair</strong></span><span class="sxs-lookup"><span data-stu-id="4cc9a-124"><strong>Exit</strong></span></span></td>
<td><span data-ttu-id="4cc9a-125">Saia da verificação de UIA Visual.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-125">Exit Visual UIA Verify.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4cc9a-126"><strong>Exibir</strong></span><span class="sxs-lookup"><span data-stu-id="4cc9a-126"><strong>View</strong></span></span></td>
<td><span data-ttu-id="4cc9a-127"><strong>Realçar</strong></span><span class="sxs-lookup"><span data-stu-id="4cc9a-127"><strong>Highlighting</strong></span></span></td>
<td><span data-ttu-id="4cc9a-128">Realce o retângulo delimitador do elemento selecionado no painel de <strong>árvore elementos de automação</strong> .</span><span class="sxs-lookup"><span data-stu-id="4cc9a-128">Highlight the bounding rectangle of the selected element in the <strong>Automation Elements Tree</strong> pane.</span></span> <span data-ttu-id="4cc9a-129">As opções a seguir estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-129">The following options are available.</span></span>
<ul>
<li><span data-ttu-id="4cc9a-130"><strong>Rectangle</strong>— uma linha vermelha sólida.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-130"><strong>Rectangle</strong>—A solid red line.</span></span></li>
<li><span data-ttu-id="4cc9a-131"><strong>Retângulo esmaecido</strong>— uma linha vermelha sólida que desaparece depois de alguns segundos.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-131"><strong>Fading Rectangle</strong>—A solid red line that disappears after a few seconds.</span></span></li>
<li><span data-ttu-id="4cc9a-132"><strong>Raios e retângulo</strong>— uma linha vermelha sólida com linhas de realce azul adicionais que radiam de cada canto do retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-132"><strong>Rays and Rectangle</strong>—A solid red line with additional blue highlight lines that radiate from each corner of the bounding rectangle.</span></span></li>
<li><span data-ttu-id="4cc9a-133"><strong>Nenhum</strong>– nenhum realce visível.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-133"><strong>None</strong>—No visible highlight.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="4cc9a-134"><strong>Árvore de elementos de automação</strong>$ {remove} $</span><span class="sxs-lookup"><span data-stu-id="4cc9a-134"><strong>Automation Elements Tree</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="4cc9a-135"><strong>Atualizar elemento selecionado</strong></span><span class="sxs-lookup"><span data-stu-id="4cc9a-135"><strong>Refresh Selected Element</strong></span></span></td>
<td><span data-ttu-id="4cc9a-136">Atualize os filhos do elemento selecionado no painel de <strong>árvore elementos de automação</strong> .</span><span class="sxs-lookup"><span data-stu-id="4cc9a-136">Refresh the children of the selected element in the <strong>Automation Elements Tree</strong> pane.</span></span> <span data-ttu-id="4cc9a-137">A lista de elementos é estática e não é atualizada dinamicamente (automaticamente) se a árvore do elemento for alterada.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-137">The list of elements is static and does not refresh dynamically (automatically) if the element tree changes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4cc9a-138"><strong>Navegação</strong></span><span class="sxs-lookup"><span data-stu-id="4cc9a-138"><strong>Navigation</strong></span></span></td>
<td><span data-ttu-id="4cc9a-139">Navegue pela hierarquia de árvore de elementos para um dos elementos a seguir.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-139">Navigate through the element tree hierarchy to one of the following elements.</span></span>
<ul>
<li><span data-ttu-id="4cc9a-140"><strong>Pai</strong>– vá para o elemento pai.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-140"><strong>Parent</strong>—Go to parent element.</span></span></li>
<li><span data-ttu-id="4cc9a-141"><strong>Primeiro filho</strong>— vá para o primeiro elemento filho.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-141"><strong>First Child</strong>—Go to first child element.</span></span></li>
<li><span data-ttu-id="4cc9a-142"><strong>Próximo irmão</strong>— ir para o primeiro elemento irmão.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-142"><strong>Next Sibling</strong>—Go to first sibling element.</span></span></li>
<li><span data-ttu-id="4cc9a-143"><strong>Irmão anterior</strong>— vá para o elemento irmão anterior.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-143"><strong>Previous Sibling</strong>—Go to previous sibling element.</span></span></li>
<li><span data-ttu-id="4cc9a-144"><strong>Último filho</strong>– vá para o último elemento filho.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-144"><strong>Last Child</strong>—Go to last child element.</span></span></li>
</ul></td>

</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="4cc9a-145"><strong>Mode</strong>$ {remove} $</span><span class="sxs-lookup"><span data-stu-id="4cc9a-145"><strong>Mode</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="4cc9a-146"><strong>Always On superior</strong></span><span class="sxs-lookup"><span data-stu-id="4cc9a-146"><strong>Always On Top</strong></span></span></td>
<td><span data-ttu-id="4cc9a-147">A janela Verificação de UIA Visual permanece na parte superior da ordem z da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-147">The Visual UIA Verify window remains at the top of the desktop z-order.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4cc9a-148"><strong>Modo de foco (use Ctrl)</strong></span><span class="sxs-lookup"><span data-stu-id="4cc9a-148"><strong>Hover Mode (Use Ctrl)</strong></span></span></td>
<td><span data-ttu-id="4cc9a-149">Quando a tecla CTRL é pressionada, o elemento sob o cursor do mouse é identificado como o elemento de interesse.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-149">When the Ctrl key is pressed, the element under the mouse cursor is identified as the element of interest.</span></span> <span data-ttu-id="4cc9a-150">O painel de <strong>árvore elementos de automação</strong> é atualizado e o item correspondente na lista de elementos é realçado.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-150">The <strong>Automation Elements Tree</strong> pane is refreshed and the corresponding item in the element list is highlighted.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="4cc9a-151"><strong>Acompanhamento de foco</strong></span><span class="sxs-lookup"><span data-stu-id="4cc9a-151"><strong>Focus Tracking</strong></span></span></td>
<td><span data-ttu-id="4cc9a-152">À medida que o foco é alterado, o elemento com o foco é identificado como o elemento de interesse.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-152">As the focus changes, the element with the focus is identified as the element of interest.</span></span> <span data-ttu-id="4cc9a-153">O painel de <strong>árvore elementos de automação</strong> é atualizado e o item correspondente na lista de elementos é realçado.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-153">The <strong>Automation Elements Tree</strong> pane is refreshed and the corresponding item in the element list is highlighted.</span></span></td>

</tr>
<tr class="even">
<td rowspan="6"><span data-ttu-id="4cc9a-154"><strong>Testes</strong>$ {remove} $</span><span class="sxs-lookup"><span data-stu-id="4cc9a-154"><strong>Tests</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="4cc9a-155"><strong>Ir para a esquerda</strong></span><span class="sxs-lookup"><span data-stu-id="4cc9a-155"><strong>Go Left</strong></span></span></td>
<td><span data-ttu-id="4cc9a-156">Mova um nó para a esquerda na árvore de <strong>testes</strong> .</span><span class="sxs-lookup"><span data-stu-id="4cc9a-156">Move one node left in the <strong>Tests</strong> tree.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4cc9a-157"><strong>Subir</strong></span><span class="sxs-lookup"><span data-stu-id="4cc9a-157"><strong>Go Up</strong></span></span></td>
<td><span data-ttu-id="4cc9a-158">Mova um nó para cima na árvore de <strong>testes</strong> .</span><span class="sxs-lookup"><span data-stu-id="4cc9a-158">Move one node up in the <strong>Tests</strong> tree.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="4cc9a-159"><strong>Descer</strong></span><span class="sxs-lookup"><span data-stu-id="4cc9a-159"><strong>Go Down</strong></span></span></td>
<td><span data-ttu-id="4cc9a-160">Mova um nó para baixo na árvore de <strong>testes</strong> .</span><span class="sxs-lookup"><span data-stu-id="4cc9a-160">Move one node down in the <strong>Tests</strong> tree.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="4cc9a-161"><strong>Ir para a direita</strong></span><span class="sxs-lookup"><span data-stu-id="4cc9a-161"><strong>Go Right</strong></span></span></td>
<td><span data-ttu-id="4cc9a-162">Mova um nó para a direita na árvore de <strong>testes</strong> .</span><span class="sxs-lookup"><span data-stu-id="4cc9a-162">Move one node right in the <strong>Tests</strong> tree.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="4cc9a-163"><strong>Executar teste (s) selecionados no elemento selecionado</strong></span><span class="sxs-lookup"><span data-stu-id="4cc9a-163"><strong>Run Selected Test(s) On Selected Element</strong></span></span></td>
<td><span data-ttu-id="4cc9a-164">Execute os testes selecionados na árvore de <strong>testes</strong> no elemento selecionado.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-164">Run the selected tests from the <strong>Tests</strong> tree on the selected element.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="4cc9a-165"><strong>Filtrar problemas conhecidos</strong></span><span class="sxs-lookup"><span data-stu-id="4cc9a-165"><strong>Filter Known Problems</strong></span></span></td>
<td><span data-ttu-id="4cc9a-166">Filtre bugs de automação da interface do usuário conhecidos dos resultados do teste.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-166">Filter known UI Automation bugs from the test results.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="4cc9a-167"><strong>Ajuda</strong></span><span class="sxs-lookup"><span data-stu-id="4cc9a-167"><strong>Help</strong></span></span></td>
<td><span data-ttu-id="4cc9a-168"><strong>Sobre a verificação da automação da interface do usuário Visual</strong></span><span class="sxs-lookup"><span data-stu-id="4cc9a-168"><strong>About Visual UI Automation Verify</strong></span></span></td>
<td><span data-ttu-id="4cc9a-169">Exiba a versão do software e as informações de direitos autorais para verificação de UIA Visual.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-169">Display the software version and copyright information for Visual UIA Verify.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="functional-panes"></a><span data-ttu-id="4cc9a-170">Painéis funcionais</span><span class="sxs-lookup"><span data-stu-id="4cc9a-170">Functional Panes</span></span>

<span data-ttu-id="4cc9a-171">Esta seção descreve os painéis funcionais na interface do usuário de verificação do Visual UIA.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-171">This section describes the functional panes in the Visual UIA Verify user interface.</span></span>

-   [<span data-ttu-id="4cc9a-172">Painel de árvore de elementos de automação</span><span class="sxs-lookup"><span data-stu-id="4cc9a-172">Automation Elements Tree Pane</span></span>](#automation-elements-tree-pane)
-   [<span data-ttu-id="4cc9a-173">Painel de testes</span><span class="sxs-lookup"><span data-stu-id="4cc9a-173">Tests Pane</span></span>](#tests-pane)
-   [<span data-ttu-id="4cc9a-174">Painel de resultados de testes</span><span class="sxs-lookup"><span data-stu-id="4cc9a-174">Test Results Pane</span></span>](#test-results-pane)
-   [<span data-ttu-id="4cc9a-175">Painel Propriedades</span><span class="sxs-lookup"><span data-stu-id="4cc9a-175">Properties Pane</span></span>](#properties-pane)

### <a name="automation-elements-tree-pane"></a><span data-ttu-id="4cc9a-176">Painel de árvore de elementos de automação</span><span class="sxs-lookup"><span data-stu-id="4cc9a-176">Automation Elements Tree Pane</span></span>

<span data-ttu-id="4cc9a-177">O painel de **árvore elementos de automação** contém um instantâneo hierárquico dos objetos de elemento de automação que estão disponíveis para teste.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-177">The **Automation Elements Tree** pane contains a hierarchical snapshot of automation element objects that are available for testing.</span></span> <span data-ttu-id="4cc9a-178">O elemento superior na árvore representa a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-178">The top element in the tree represents the desktop.</span></span>

<span data-ttu-id="4cc9a-179">Essa exibição é uma coleção estática que é compilada quando a verificação de UIA Visual é iniciada.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-179">This view is a static collection that is compiled when Visual UIA Verify starts.</span></span> <span data-ttu-id="4cc9a-180">Para atualizar a exibição no nó selecionado, use o comando de menu **Atualizar elemento selecionado** ou o botão da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-180">To refresh the view at the selected node, use the **Refresh Selected Element** menu command or toolbar button.</span></span>

<span data-ttu-id="4cc9a-181">A captura de tela a seguir mostra o painel de **árvore elementos de automação** .</span><span class="sxs-lookup"><span data-stu-id="4cc9a-181">The following screen shot shows the **Automation Elements Tree** pane.</span></span>

![painel de árvore de elementos de automação da verificação de UIA Visual](images/automation-elements-tree-pane.png)

<span data-ttu-id="4cc9a-183">Um nó esmaecido (não disponível) na **árvore elementos de automação** indica que o elemento é um membro da exibição bruta de automação da interface do usuário, mas não atende às condições necessárias para ser considerado um membro da exibição de conteúdo ou da exibição de controle.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-183">A dimmed (unavailable) node in the **Automation Elements Tree** indicates that the element is a member of the UI Automation raw view, but does not meet the conditions necessary to be considered a member of the content view or control view.</span></span> <span data-ttu-id="4cc9a-184">No entanto, o elemento ainda pode ser testado da verificação da automação da interface do usuário visual.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-184">However, the element can still be tested from Visual UI Automation Verify.</span></span> <span data-ttu-id="4cc9a-185">Para obter mais informações, consulte [visão geral da árvore de automação da interface do usuário](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="4cc9a-185">For more information, see the [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>

<span data-ttu-id="4cc9a-186">Os comandos disponíveis na barra de ferramentas da **árvore elementos de automação** incluem:</span><span class="sxs-lookup"><span data-stu-id="4cc9a-186">Commands available from the **Automation Elements Tree** toolbar include:</span></span>

-   <span data-ttu-id="4cc9a-187">**Atualizar**— atualize o nó selecionado e seus filhos.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-187">**Refresh**—Refresh the selected node and its children.</span></span> <span data-ttu-id="4cc9a-188">Esse comando não atualiza toda a árvore de elementos, a menos que o nó raiz esteja selecionado.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-188">This command does not refresh the entire element tree unless the root node is selected.</span></span>
-   <span data-ttu-id="4cc9a-189">**Pai (Ctrl + Shift + F6)**– vá para o pai do nó atual.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-189">**Parent (Ctrl+Shift+F6)**—Go to parent of the current node.</span></span>
-   <span data-ttu-id="4cc9a-190">**Primeiro filho (Ctrl + Shift + F7)**– vá para o primeiro filho do nó atual.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-190">**First Child (Ctrl+Shift+F7)**—Go to first child of the current node..</span></span>
-   <span data-ttu-id="4cc9a-191">**Próximo irmão (Ctrl + Shift + F8)**— vá para próximo filho irmão do nó atual.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-191">**Next Sibling (Ctrl+Shift+F8)**—Go to next sibling child of the current node.</span></span>
-   <span data-ttu-id="4cc9a-192">**Irmão anterior (Ctrl + Shift + F9)**– vá para irmão anterior do nó atual.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-192">**Previous Sibling (Ctrl+Shift+F9)**—Go to previous sibling of the current node.</span></span>
-   <span data-ttu-id="4cc9a-193">**Último filho (Ctrl + Shift + F10)**– vá para o último filho do nó atual.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-193">**Last Child (Ctrl+Shift+F10)**—Go to last child of the current node.</span></span>
-   <span data-ttu-id="4cc9a-194">**Acompanhamento de foco**— ativar ou desativar a seleção de nó com base no controle de foco.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-194">**Focus Tracking**—Toggle node selection on or off based on focus tracking.</span></span>

### <a name="tests-pane"></a><span data-ttu-id="4cc9a-195">Painel de testes</span><span class="sxs-lookup"><span data-stu-id="4cc9a-195">Tests Pane</span></span>

<span data-ttu-id="4cc9a-196">O painel de **testes** contém uma lista de testes de automação de interface do usuário organizados por tipo de teste (**elemento de automação**, **controle** e **padrão**) e prioridade (**verificação de compilação**, **prioridade 0**, **prioridade 1**, **prioridade 2** e **prioridade 3**).</span><span class="sxs-lookup"><span data-stu-id="4cc9a-196">The **Tests** pane contains a list of UI Automation tests organized by test type (**Automation Element**, **Control**, and **Pattern**) and priority (**Build Verification**, **Priority 0**, **Priority 1**, **Priority 2**, and **Priority 3**).</span></span> <span data-ttu-id="4cc9a-197">Essa lista é gerada com base no tipo de controle do elemento selecionado no painel de **árvore elementos de automação** .</span><span class="sxs-lookup"><span data-stu-id="4cc9a-197">This list is generated based on the control type of the selected element in the **Automation Elements Tree** pane.</span></span> <span data-ttu-id="4cc9a-198">Para obter mais informações, consulte [visão geral de tipos de controle de automação da interface do usuário](uiauto-controltypesoverview.md).</span><span class="sxs-lookup"><span data-stu-id="4cc9a-198">For more information, see [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span></span>

<span data-ttu-id="4cc9a-199">A captura de tela a seguir mostra o painel **testes** .</span><span class="sxs-lookup"><span data-stu-id="4cc9a-199">The following screen shot shows the **Tests** pane.</span></span>

![painel de teste](images/test-pane.png)

<span data-ttu-id="4cc9a-201">Os comandos disponíveis na barra de ferramentas **testes** incluem:</span><span class="sxs-lookup"><span data-stu-id="4cc9a-201">Commands available from the **Tests** toolbar include:</span></span>

-   <span data-ttu-id="4cc9a-202">**Mostrar**— especifica os testes de automação da interface do usuário a serem exibidos; ou seja, exiba todos os testes ou apenas testes adequados para o tipo de controle do elemento selecionado na **árvore de elementos de automação** (padrão).</span><span class="sxs-lookup"><span data-stu-id="4cc9a-202">**Show**—Specifies the UI Automation tests to display; that is, display all tests or only tests suited to the control type of the selected element in the **Automation Elements Tree** (default).</span></span>
-   <span data-ttu-id="4cc9a-203">**Tipo**— especifica os tipos de teste a serem exibidos: **elemento de automação**, **padrão** ou **controle**.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-203">**Type**—Specifies the test types to display: **Automation Element**, **Pattern**, or **Control**.</span></span>
-   <span data-ttu-id="4cc9a-204">**Prioridades**— especifica as prioridades de teste a serem exibidas: **verificação de compilação**, **prioridade 0**, **prioridade 1**, **prioridade 2** ou **prioridade 3**.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-204">**Priorities**—Specifies the test priorities to display: **Build Verification**, **Priority 0**, **Priority 1**, **Priority 2**, or **Priority 3**.</span></span>
-   <span data-ttu-id="4cc9a-205">**Ir** para a esquerda — vá para o pai do nó atual.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-205">**Go Left**—Go to the parent of the current node.</span></span>
-   <span data-ttu-id="4cc9a-206">**Subir**– vá para o irmão anterior do nó atual.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-206">**Go Up**—Go to the previous sibling of the current node.</span></span>
-   <span data-ttu-id="4cc9a-207">**Descer**– vá para o próximo irmão do nó atual.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-207">**Go Down**—Go to the next sibling of the current node.</span></span>
-   <span data-ttu-id="4cc9a-208">**Vá** para a direita — vá para o primeiro filho do nó atual.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-208">**Go Right**—Go to the first child of the current node.</span></span>
-   <span data-ttu-id="4cc9a-209">**Executar teste (s) selecionados**– executa os testes no elemento selecionado na árvore de **elementos de automação**.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-209">**Run Selected Test(s)**—Runs the tests on the element selected in the **Automation Elements Tree**.</span></span>

### <a name="test-results-pane"></a><span data-ttu-id="4cc9a-210">Painel de resultados de testes</span><span class="sxs-lookup"><span data-stu-id="4cc9a-210">Test Results Pane</span></span>

<span data-ttu-id="4cc9a-211">O painel de **resultados de teste** contém a funcionalidade de log de verificação de UIA Visual.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-211">The **Test Results** pane contains the Visual UIA Verify logging functionality.</span></span> <span data-ttu-id="4cc9a-212">A captura de tela a seguir mostra o painel **resultados de teste** .</span><span class="sxs-lookup"><span data-stu-id="4cc9a-212">The following screen shot shows the **Test Results** pane.</span></span>

![painel de resultados de teste](images/test-results-pane.png)

<span data-ttu-id="4cc9a-214">Os comandos disponíveis na barra de ferramentas **resultados dos testes** incluem:</span><span class="sxs-lookup"><span data-stu-id="4cc9a-214">Commands available from the **Tests Results** toolbar include:</span></span>

-   <span data-ttu-id="4cc9a-215">**Voltar**— Page Backward no histórico de exibição de relatório.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-215">**Back**—Page backward in report viewing history.</span></span>
-   <span data-ttu-id="4cc9a-216">**Avançar**– avanço de página no histórico de exibição de relatório.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-216">**Forward**—Page forward in report viewing history.</span></span>
-   <span data-ttu-id="4cc9a-217">**Geral**— exibe um resumo dos resultados do teste (**passado**, **com falha** e um **erro inesperado**).</span><span class="sxs-lookup"><span data-stu-id="4cc9a-217">**Overall**—Displays a summary of the test results (**Passed**, **Failed**, and **Unexpected Error**).</span></span> <span data-ttu-id="4cc9a-218">O resultado do teste é vinculado à exibição **todos os resultados** .</span><span class="sxs-lookup"><span data-stu-id="4cc9a-218">The test result is linked to the **All Results** view.</span></span> <span data-ttu-id="4cc9a-219">O comando **geral** exibe uma tabela como a mostrada a seguir.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-219">The **Overall** command displays a table like the following one.</span></span>

    ![tabela de resultados de teste geral](images/overall-test-results.png)

-   <span data-ttu-id="4cc9a-221">**Todos os resultados**— exibe um log detalhado para cada resultado de teste, conforme mostrado nas tabelas a seguir.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-221">**All Results**— Displays a detailed log for each test result, as shown in the following tables.</span></span>

    ![exemplo de detalhes de resultado de log da exibição todos os resultados](images/all-results-log.png)

    <span data-ttu-id="4cc9a-223">O nome do teste na tabela **todos os resultados** está vinculado a uma descrição do caso de teste para o elemento, como na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-223">The test name in the **All Results** table is linked to a test case description for the element, as in the following table.</span></span>

    ![detalhes do caso de teste](images/test-case-detail.png)

-   <span data-ttu-id="4cc9a-225">**Log completo**— exibe uma exibição alternativa do log detalhado para cada resultado de teste, conforme mostrado na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-225">**Full Log**—Displays an alternate view of the detailed log for each test result, as shown in the following screen shot.</span></span>

    ![exibição alternativa de um detalhe de caso de teste](images/alt-view-of-test-case-detail.png)

-   <span data-ttu-id="4cc9a-227">**XML**— EXIBE o XML bruto gerado pelo agente de log XML.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-227">**XML**—Displays the raw XML generated by the XML logger.</span></span>
-   <span data-ttu-id="4cc9a-228">**Localização rápida**— pesquisa de texto simples da exibição atual no painel de **resultados de teste** .</span><span class="sxs-lookup"><span data-stu-id="4cc9a-228">**Quick Find**—Simple text search of the current view in the **Test Results** pane.</span></span>
-   <span data-ttu-id="4cc9a-229">**Abrir em nova janela**— abre a exibição atual em uma nova instância do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-229">**Open in New Window**—Opens the current view in a new instance of Internet Explorer.</span></span>

### <a name="properties-pane"></a><span data-ttu-id="4cc9a-230">Painel Propriedades</span><span class="sxs-lookup"><span data-stu-id="4cc9a-230">Properties Pane</span></span>

<span data-ttu-id="4cc9a-231">O painel **Propriedades** contém uma lista de propriedades de automação da interface do usuário e valores de propriedade organizados por tipo de propriedade: **acessibilidade geral**, **identificação**, **padrões** (padrões de controle), **estado** e **visibilidade**.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-231">The **Properties** pane contains a list of UI Automation properties and property values organized by property type: **General Accessibility**, **Identification**, **Patterns** (control patterns), **State**, and **Visibility**.</span></span> <span data-ttu-id="4cc9a-232">Os valores de propriedade são preenchidos dinamicamente com base no tipo de controle do objeto selecionado no painel de **árvore elementos de automação** .</span><span class="sxs-lookup"><span data-stu-id="4cc9a-232">The property values are dynamically populated based on the control type of the object selected in the **Automation Elements Tree** pane.</span></span> <span data-ttu-id="4cc9a-233">A captura de tela a seguir mostra o painel **Propriedades** .</span><span class="sxs-lookup"><span data-stu-id="4cc9a-233">The following screen shot shows the **Properties** pane.</span></span>

![painel Propriedades](images/properties-pane.png)

<span data-ttu-id="4cc9a-235">Se o controle selecionado oferecer suporte a um padrão de controle específico, a verificação de UIA Visual fornecerá a capacidade de chamar métodos que são suportados por esse padrão de controle.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-235">If the selected control supports a specific control pattern, Visual UIA Verify provides the ability to call methods that are supported by that control pattern.</span></span> <span data-ttu-id="4cc9a-236">Por exemplo, o [tipo de controle Window](uiauto-supportwindowcontroltype.md) dá suporte ao [padrão de controle Window](uiauto-implementingwindow.md), que tem um método [**Close**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-close) que pode ser invocado no painel **Propriedades** , conforme mostrado na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-236">For example, the [Window control type](uiauto-supportwindowcontroltype.md) supports the [Window control pattern](uiauto-implementingwindow.md), which has a [**Close**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-close) method that can be invoked from the **Properties** pane, as shown in the following screen shot.</span></span> <span data-ttu-id="4cc9a-237">Para obter mais informações, consulte [visão geral de tipos de controle de automação da interface do usuário](uiauto-controltypesoverview.md).</span><span class="sxs-lookup"><span data-stu-id="4cc9a-237">For more information, see [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span></span>

![método Close do padrão de controle Window invocado no painel Propriedades](images/close-invoked-from-properties-pane.png)

<span data-ttu-id="4cc9a-239">Os comandos disponíveis na barra de ferramentas **Propriedades** incluem:</span><span class="sxs-lookup"><span data-stu-id="4cc9a-239">Commands available from the **Properties** toolbar include:</span></span>

-   <span data-ttu-id="4cc9a-240">**Atualizar**– atualize a árvore de **Propriedades** .</span><span class="sxs-lookup"><span data-stu-id="4cc9a-240">**Refresh**—Refresh the **Properties** tree.</span></span>
-   <span data-ttu-id="4cc9a-241">**Expandir tudo**– expande todos os nós na árvore de **Propriedades** .</span><span class="sxs-lookup"><span data-stu-id="4cc9a-241">**Expand All**—Expands all nodes in the **Properties** tree.</span></span>

 

 




