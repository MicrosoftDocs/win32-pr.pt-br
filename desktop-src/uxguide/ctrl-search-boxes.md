---
title: Caixas de pesquisa
description: Com uma caixa de pesquisa, os usuários podem localizar rapidamente objetos ou texto específicos em um grande conjunto de dados filtrando ou realçando correspondências.
ms.assetid: e2d77b36-e001-403c-9b66-2d136c394a24
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: e9d1fca8fdb96b17098cee79fd5b62ecd7ab7531
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103930070"
---
# <a name="search-boxes"></a><span data-ttu-id="9a00d-103">Caixas de pesquisa</span><span class="sxs-lookup"><span data-stu-id="9a00d-103">Search Boxes</span></span>

> [!NOTE]
> <span data-ttu-id="9a00d-104">Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="9a00d-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="9a00d-105">Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="9a00d-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="9a00d-106">Com uma caixa de pesquisa, os usuários podem localizar rapidamente objetos ou texto específicos em um grande conjunto de dados filtrando ou realçando correspondências.</span><span class="sxs-lookup"><span data-stu-id="9a00d-106">With a Search box, users can quickly locate specific objects or text within a large set of data by filtering or highlighting matches.</span></span> <span data-ttu-id="9a00d-107">Não há nenhum controle de pesquisa padrão, mas você deve se esforçar para tornar os recursos de pesquisa do programa consistentes com os do Windows.</span><span class="sxs-lookup"><span data-stu-id="9a00d-107">There is no standard search control, but you should strive to make your program's search features consistent with those of Windows.</span></span>

<span data-ttu-id="9a00d-108">Há dois tipos de pesquisas:</span><span class="sxs-lookup"><span data-stu-id="9a00d-108">There are two types of searches:</span></span>

-   <span data-ttu-id="9a00d-109">**Pesquisa instantânea**, onde os resultados são exibidos imediatamente conforme o usuário digita.</span><span class="sxs-lookup"><span data-stu-id="9a00d-109">**Instant search**, where the results are displayed immediately as the user types.</span></span> <span data-ttu-id="9a00d-110">Nenhum botão precisa ser clicado, portanto, o símbolo de pesquisa de lupa é mostrado como um gráfico, não um botão.</span><span class="sxs-lookup"><span data-stu-id="9a00d-110">No button needs to be clicked, so the magnifying glass search symbol is shown as a graphic, not a button.</span></span>

    ![Captura de tela que mostra uma caixa de pesquisa instantânea com um texto explicativo "prompt" apontando na caixa de pesquisa e um texto explicativo "símbolo de pesquisa" apontando para o gráfico de lupa.](images/ctrl-search-boxes-image1.png)

    <span data-ttu-id="9a00d-112">Uma caixa de pesquisa típica usando A pesquisa instantânea.</span><span class="sxs-lookup"><span data-stu-id="9a00d-112">A typical Search box using Instant search.</span></span> <span data-ttu-id="9a00d-113">A pesquisa é executada automaticamente em cada pressionamento de tecla.</span><span class="sxs-lookup"><span data-stu-id="9a00d-113">Search is automatically executed on every keystroke.</span></span>

-   <span data-ttu-id="9a00d-114">**Pesquisa regular**, em que uma pesquisa é executada quando o usuário clica no botão de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9a00d-114">**Regular search**, where a search is performed when the user clicks the search button.</span></span> <span data-ttu-id="9a00d-115">O símbolo de pesquisa de lupa é mostrado em um botão.</span><span class="sxs-lookup"><span data-stu-id="9a00d-115">The magnifying glass search symbol is shown on a button.</span></span>

    ![<span data-ttu-id="9a00d-116">captura de tela de uma caixa de pesquisa normal</span><span class="sxs-lookup"><span data-stu-id="9a00d-116">screen shot of a regular search box</span></span> ](images/ctrl-search-boxes-image2.png)

    <span data-ttu-id="9a00d-117">Uma caixa de pesquisa típica usando A pesquisa regular.</span><span class="sxs-lookup"><span data-stu-id="9a00d-117">A typical Search box using regular search.</span></span> <span data-ttu-id="9a00d-118">Os usuários clicam em um botão para executar a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9a00d-118">Users click a button to perform the search.</span></span>

    <span data-ttu-id="9a00d-119">Você pode fornecer um ou ambos os tipos de opções de pesquisa para seus usuários.</span><span class="sxs-lookup"><span data-stu-id="9a00d-119">You can provide either or both kinds of search options for your users.</span></span>

## <a name="is-this-the-right-control"></a><span data-ttu-id="9a00d-120">Esse é o controle correto?</span><span class="sxs-lookup"><span data-stu-id="9a00d-120">Is this the right control?</span></span>

<span data-ttu-id="9a00d-121">Para decidir, considere estas perguntas:</span><span class="sxs-lookup"><span data-stu-id="9a00d-121">To decide, consider these questions:</span></span>

-   <span data-ttu-id="9a00d-122">**Os objetos específicos são difíceis de encontrar?**</span><span class="sxs-lookup"><span data-stu-id="9a00d-122">**Are specific objects difficult to find?**</span></span> <span data-ttu-id="9a00d-123">Isso pode ocorrer quando:</span><span class="sxs-lookup"><span data-stu-id="9a00d-123">This can happen when:</span></span>
    -   <span data-ttu-id="9a00d-124">Há muitos objetos.</span><span class="sxs-lookup"><span data-stu-id="9a00d-124">There are many objects.</span></span>
    -   <span data-ttu-id="9a00d-125">Os objetos não estão localizados em um único local.</span><span class="sxs-lookup"><span data-stu-id="9a00d-125">The objects aren't located in a single location.</span></span> <span data-ttu-id="9a00d-126">A pesquisa é especialmente útil para localizar objetos em árvores.</span><span class="sxs-lookup"><span data-stu-id="9a00d-126">Search is especially useful for finding objects in trees.</span></span>
    -   <span data-ttu-id="9a00d-127">Os dados de pesquisa são difíceis de localizar (por exemplo, metadados).</span><span class="sxs-lookup"><span data-stu-id="9a00d-127">The search data is difficult to find (for example, metadata).</span></span>
-   <span data-ttu-id="9a00d-128">**Os usuários precisam localizar texto específico em documentos?**</span><span class="sxs-lookup"><span data-stu-id="9a00d-128">**Do users need to find specific text within documents?**</span></span>
-   <span data-ttu-id="9a00d-129">**Seu recurso retorna resultados de pesquisa relevantes dentro de cinco segundos?**</span><span class="sxs-lookup"><span data-stu-id="9a00d-129">**Does your feature return relevant search results within five seconds?**</span></span> <span data-ttu-id="9a00d-130">Caso contrário, você pode fornecer um recurso de pesquisa, mas usar um design alternativo que fornece comentários visíveis para acomodar pesquisas de execução longa, como uma caixa de diálogo de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9a00d-130">If not, you can provide a search feature, but use an alternative design that gives visible feedback to accommodate long-running searches, such as a search dialog box.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="9a00d-131">Conceitos de design</span><span class="sxs-lookup"><span data-stu-id="9a00d-131">Design concepts</span></span>

<span data-ttu-id="9a00d-132">A pesquisa é uma primeira etapa crucial em muitos cenários: os usuários devem encontrar objetos antes de poderem usá-los.</span><span class="sxs-lookup"><span data-stu-id="9a00d-132">Searching is a crucial first step in many scenarios: Users must find objects before they can use them.</span></span> <span data-ttu-id="9a00d-133">Os usuários estão economizando mais e mais objetos em discos rígidos cada vez maiores, mas procurar objetos não é bem dimensionável.</span><span class="sxs-lookup"><span data-stu-id="9a00d-133">Users are saving more and more objects on increasingly larger hard disks, but browsing for objects doesn't scale well.</span></span> <span data-ttu-id="9a00d-134">A pesquisa deve ser uma parte simples, consistente e confiável da experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="9a00d-134">Search must be a simple, consistent, reliable part of the user experience.</span></span>

<span data-ttu-id="9a00d-135">Caixas de pesquisa no Windows:</span><span class="sxs-lookup"><span data-stu-id="9a00d-135">Search boxes in Windows:</span></span>

-   <span data-ttu-id="9a00d-136">Fazem parte de todas as janelas do Explorer, para que sejam fáceis de localizar e reconhecer.</span><span class="sxs-lookup"><span data-stu-id="9a00d-136">Are part of all Explorer windows, so they are easy to find and recognize.</span></span>
-   <span data-ttu-id="9a00d-137">Ter aparência e comportamento consistentes.</span><span class="sxs-lookup"><span data-stu-id="9a00d-137">Have consistent appearance and behavior.</span></span>
-   <span data-ttu-id="9a00d-138">São eficientes e rápidos, oferecendo resultados instantâneos no modo de pesquisa instantânea.</span><span class="sxs-lookup"><span data-stu-id="9a00d-138">Are efficient and fast, giving instant results in Instant search mode.</span></span>

<span data-ttu-id="9a00d-139">Uma caixa de pesquisa é usada no Windows nestes locais:</span><span class="sxs-lookup"><span data-stu-id="9a00d-139">A Search box is used in Windows in these places:</span></span>

-   <span data-ttu-id="9a00d-140">Exploradores</span><span class="sxs-lookup"><span data-stu-id="9a00d-140">Explorers</span></span>
-   <span data-ttu-id="9a00d-141">Experiências (Microsoft Windows Media Player, Galeria de fotos do Windows, Windows Internet Explorer)</span><span class="sxs-lookup"><span data-stu-id="9a00d-141">Experiences (Microsoft Windows Media Player, Windows Photo Gallery, Windows Internet Explorer)</span></span>
-   <span data-ttu-id="9a00d-142">Menu iniciar (para localizar programas e arquivos recentes)</span><span class="sxs-lookup"><span data-stu-id="9a00d-142">Start menu (to find programs and recent files)</span></span>
-   <span data-ttu-id="9a00d-143">Home page do painel de controle (para localizar itens e tarefas do painel de controle)</span><span class="sxs-lookup"><span data-stu-id="9a00d-143">Control Panel home page (to find control panel items and tasks)</span></span>
-   <span data-ttu-id="9a00d-144">Ajuda (para encontrar tópicos relevantes da ajuda)</span><span class="sxs-lookup"><span data-stu-id="9a00d-144">Help (to find relevant Help topics)</span></span>

### <a name="look-and-feel"></a><span data-ttu-id="9a00d-145">Aparência</span><span class="sxs-lookup"><span data-stu-id="9a00d-145">Look and feel</span></span>

<span data-ttu-id="9a00d-146">A sensação de pesquisa no Windows é significativamente aprimorada com o suporte à pesquisa instantânea.</span><span class="sxs-lookup"><span data-stu-id="9a00d-146">The feel of Search in Windows is significantly enhanced by supporting Instant search.</span></span> <span data-ttu-id="9a00d-147">Ter resultados instantâneos faz com que o Windows se sinta mais poderoso e direto.</span><span class="sxs-lookup"><span data-stu-id="9a00d-147">Having instant results makes Windows feel more powerful and direct.</span></span>

<span data-ttu-id="9a00d-148">No Windows Explorer e no Windows do aplicativo, a pesquisa está localizada no canto superior direito se for um ponto de entrada suplementar.</span><span class="sxs-lookup"><span data-stu-id="9a00d-148">In Windows Explorer and application windows, Search is located in the upper-right corner if it is a supplemental entry point.</span></span> <span data-ttu-id="9a00d-149">Nesse caso, os usuários procuram um mecanismo de pesquisa quando não localizam o que estão procurando na janela.</span><span class="sxs-lookup"><span data-stu-id="9a00d-149">In this case, users look for a search mechanism when they don't find what they are looking for in the window.</span></span> <span data-ttu-id="9a00d-150">No entanto, se a pesquisa for o ponto de entrada primário, ela será centralizada na parte superior da janela.</span><span class="sxs-lookup"><span data-stu-id="9a00d-150">However, if Search is the primary entry point, it is centered at the top of the window.</span></span>

<span data-ttu-id="9a00d-151">O botão Pesquisar está visualmente conectado a uma caixa de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9a00d-151">The Search button is visually connected to a Search box.</span></span> <span data-ttu-id="9a00d-152">Para minimizar o espaço, um [prompt](ctrl-text-boxes.md) opcional é usado dentro de uma caixa de pesquisa em vez de um rótulo.</span><span class="sxs-lookup"><span data-stu-id="9a00d-152">To minimize space, an optional [prompt](ctrl-text-boxes.md) is used inside a Search box instead of a label.</span></span> <span data-ttu-id="9a00d-153">O prompt pode ser uma instrução (por exemplo, digite para Pesquisar) ou indicar o escopo da pesquisa (por exemplo, procurar imagens).</span><span class="sxs-lookup"><span data-stu-id="9a00d-153">The prompt may be an instruction (for example, Type to search) or indicate the scope of the search (for example, Search for pictures).</span></span>

![<span data-ttu-id="9a00d-154">captura de tela de uma caixa de pesquisa instantânea</span><span class="sxs-lookup"><span data-stu-id="9a00d-154">screen shot of an instant search box</span></span> ](images/ctrl-search-boxes-image3.png)

<span data-ttu-id="9a00d-155">Sem rótulos e botões separados, a pesquisa instantânea no Windows tem uma aparência leve.</span><span class="sxs-lookup"><span data-stu-id="9a00d-155">Without labels and separate buttons, Instant search in Windows has a lightweight look.</span></span>

<span data-ttu-id="9a00d-156">Executar uma pesquisa bem-sucedida cria uma página virtual dos resultados da pesquisa e o adiciona à pilha voltar e à barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="9a00d-156">Performing a successful search creates a virtual page of the search results and adds it to the Back stack and Address bar.</span></span> <span data-ttu-id="9a00d-157">Os usuários têm várias maneiras de restaurar a página original e desmarcar uma caixa de pesquisa, incluindo clicar em voltar, clicar na página original na barra de endereços, pressionar ESC ou limpar a caixa de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9a00d-157">Users have several ways to restore the original page and clear a Search box, including clicking Back, clicking the original page in the Address bar, pressing Esc, or clearing the Search box.</span></span>

<span data-ttu-id="9a00d-158">Os usuários também podem simplesmente desmarcar a caixa de pesquisa sem restaurar uma página anterior de resultados.</span><span class="sxs-lookup"><span data-stu-id="9a00d-158">Users can also simply clear the Search box without restoring a previous page of results.</span></span> <span data-ttu-id="9a00d-159">No modo de pesquisa instantânea, um botão Limpar é exibido depois que o usuário começa a digitar; um "x" substitui o símbolo de pesquisa de lupa.</span><span class="sxs-lookup"><span data-stu-id="9a00d-159">In Instant search mode, a clear button appears after the user starts typing; an "x" replaces the magnifying glass search symbol.</span></span> <span data-ttu-id="9a00d-160">Ao focalizar, o "x" Obtém uma aparência de botão e pode ser clicado.</span><span class="sxs-lookup"><span data-stu-id="9a00d-160">On hover, the "x" gets a button look and can be clicked.</span></span>

![<span data-ttu-id="9a00d-161">captura de tela de uma caixa de pesquisa com um ícone ' x '</span><span class="sxs-lookup"><span data-stu-id="9a00d-161">screen shot of a search box with an 'x' icon</span></span> ](images/ctrl-search-boxes-image4.png)

<span data-ttu-id="9a00d-162">O usuário pode desmarcar a caixa de pesquisa clicando em "x" na extremidade direita do controle.</span><span class="sxs-lookup"><span data-stu-id="9a00d-162">The user can clear the Search box by clicking "x" at the right end of the control.</span></span>

<span data-ttu-id="9a00d-163">No modo de pesquisa normal, o botão Limpar é opcional.</span><span class="sxs-lookup"><span data-stu-id="9a00d-163">In regular search mode, the clear button is optional.</span></span> <span data-ttu-id="9a00d-164">Os usuários podem achar útil, por exemplo, se uma pesquisa estiver demorando muito tempo para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="9a00d-164">Users may find it useful, for example, if a search is taking a long time to complete.</span></span> <span data-ttu-id="9a00d-165">Os usuários podem clicar no "x" para interromper a pesquisa em andamento.</span><span class="sxs-lookup"><span data-stu-id="9a00d-165">Users can click the "x" to stop the search in progress.</span></span> <span data-ttu-id="9a00d-166">Se uma pesquisa já tiver sido concluída, os usuários poderão clicar no "x" para desmarcar a caixa de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9a00d-166">If a search has already completed, users can click the "x" to clear the Search box.</span></span>

## <a name="guidelines"></a><span data-ttu-id="9a00d-167">Diretrizes</span><span class="sxs-lookup"><span data-stu-id="9a00d-167">Guidelines</span></span>

### <a name="location"></a><span data-ttu-id="9a00d-168">Local</span><span class="sxs-lookup"><span data-stu-id="9a00d-168">Location</span></span>

-   <span data-ttu-id="9a00d-169">Para janelas de aplicativos, localize Pesquisar no canto superior direito.</span><span class="sxs-lookup"><span data-stu-id="9a00d-169">For application windows, locate Search in the upper-right corner.</span></span>
-   <span data-ttu-id="9a00d-170">Para janelas pop-up, localize Pesquisar onde quer que seja mais sensato e conveniente.</span><span class="sxs-lookup"><span data-stu-id="9a00d-170">For popup windows, locate Search wherever is most sensible and convenient.</span></span>
-   <span data-ttu-id="9a00d-171">**Exceção:** Se a pesquisa for geralmente a primeira coisa que os usuários fazem em uma janela (o ponto de entrada primário), centralize-o na parte superior da janela.</span><span class="sxs-lookup"><span data-stu-id="9a00d-171">**Exception:** If Search is usually the first thing users do in a window (the primary entry point), center it at the top of the window.</span></span>

### <a name="look"></a><span data-ttu-id="9a00d-172">Consulte</span><span class="sxs-lookup"><span data-stu-id="9a00d-172">Look</span></span>

-   <span data-ttu-id="9a00d-173">Use os gráficos do botão de pesquisa padrão.</span><span class="sxs-lookup"><span data-stu-id="9a00d-173">Use the standard search button graphics.</span></span> <span data-ttu-id="9a00d-174">Há três versões:</span><span class="sxs-lookup"><span data-stu-id="9a00d-174">There are three versions:</span></span>
    -   <span data-ttu-id="9a00d-175">**Somente símbolo de pesquisa de lupa (sem botão ao focalizar).**</span><span class="sxs-lookup"><span data-stu-id="9a00d-175">**Magnifying glass search symbol only (no button on hover).**</span></span> <span data-ttu-id="9a00d-176">Use para pesquisa instantânea.</span><span class="sxs-lookup"><span data-stu-id="9a00d-176">Use for Instant search.</span></span>
    -   <span data-ttu-id="9a00d-177">**Símbolo de pesquisa de lupa com botão.**</span><span class="sxs-lookup"><span data-stu-id="9a00d-177">**Magnifying glass search symbol with button.**</span></span> <span data-ttu-id="9a00d-178">Use quando o botão precisa ser clicado para iniciar a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9a00d-178">Use when button needs to be clicked to start the search.</span></span>
    -   <span data-ttu-id="9a00d-179">**Símbolo de pesquisa de lupa com botão e seta suspensa.**</span><span class="sxs-lookup"><span data-stu-id="9a00d-179">**Magnifying glass search symbol with button and drop-down arrow.**</span></span> <span data-ttu-id="9a00d-180">Adicione uma seta suspensa quando os usuários puderem alterar o escopo ou quando outras configurações estiverem disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9a00d-180">Add a drop-down arrow when users can change the scope or when other settings are available.</span></span>
        -   <span data-ttu-id="9a00d-181">Para pesquisa instantânea, use uma seta suspensa somente e mostre um botão ao focalizar.</span><span class="sxs-lookup"><span data-stu-id="9a00d-181">For Instant search, use a drop-down arrow only, and show a button on hover.</span></span>
        -   <span data-ttu-id="9a00d-182">Para pesquisa regular, mostre a seta suspensa em um botão.</span><span class="sxs-lookup"><span data-stu-id="9a00d-182">For regular search, show the drop-down arrow on a button.</span></span>

![<span data-ttu-id="9a00d-183">Figura de caixas de pesquisa instantâneas em Estados diferentes</span><span class="sxs-lookup"><span data-stu-id="9a00d-183">figure of instant search boxes in different states</span></span> ](images/ctrl-search-boxes-image5.png)

<span data-ttu-id="9a00d-184">Especificações visuais para pesquisa instantânea.</span><span class="sxs-lookup"><span data-stu-id="9a00d-184">Visual specifications for Instant search.</span></span>

![<span data-ttu-id="9a00d-185">Figura de caixas de pesquisa regulares em Estados diferentes</span><span class="sxs-lookup"><span data-stu-id="9a00d-185">figure of regular search boxes in different states</span></span> ](images/ctrl-search-boxes-image6.png)

<span data-ttu-id="9a00d-186">Especificações visuais para pesquisa regular.</span><span class="sxs-lookup"><span data-stu-id="9a00d-186">Visual specifications for regular search.</span></span>

-   <span data-ttu-id="9a00d-187">Não usar um rótulo; em vez disso, use um prompt opcional.</span><span class="sxs-lookup"><span data-stu-id="9a00d-187">Don't use a label; use an optional prompt instead.</span></span> <span data-ttu-id="9a00d-188">Se os usuários tendem a supor que a pesquisa é uma pesquisa de arquivo genérica, use o prompt para dar o escopo.</span><span class="sxs-lookup"><span data-stu-id="9a00d-188">If users tend to assume that the search is a generic file search, use the prompt to give the scope.</span></span> <span data-ttu-id="9a00d-189">Caso contrário, use o tipo para pesquisar ou uma frase concisa semelhante.</span><span class="sxs-lookup"><span data-stu-id="9a00d-189">Otherwise, use Type to search or a similar, concise phrase.</span></span>

    ![<span data-ttu-id="9a00d-190">captura de tela do prompt ' tipo para pesquisa '</span><span class="sxs-lookup"><span data-stu-id="9a00d-190">screen shot of 'type to search' prompt</span></span> ](images/ctrl-search-boxes-image7.png)

    ![<span data-ttu-id="9a00d-191">captura de tela do prompt ' Pesquisar todos os gadgets '</span><span class="sxs-lookup"><span data-stu-id="9a00d-191">screen shot of 'search all gadgets' prompt</span></span> ](images/ctrl-search-boxes-image8.png)

    <span data-ttu-id="9a00d-192">Nestes exemplos, os prompts de texto breves ajudam os usuários a trabalhar com a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9a00d-192">In these examples, brief textual prompts help users work with Search.</span></span>

### <a name="interaction"></a><span data-ttu-id="9a00d-193">Interação</span><span class="sxs-lookup"><span data-stu-id="9a00d-193">Interaction</span></span>

-   <span data-ttu-id="9a00d-194">**No foco de entrada, selecione automaticamente qualquer texto inserido anteriormente.**</span><span class="sxs-lookup"><span data-stu-id="9a00d-194">**On input focus, automatically select any previously entered text.**</span></span> <span data-ttu-id="9a00d-195">Isso permite que os usuários insiram uma nova pesquisa digitando ou modifiquem a pesquisa anterior posicionando o cursor usando as teclas de direção.</span><span class="sxs-lookup"><span data-stu-id="9a00d-195">Doing so allows users to enter a new search by typing, or to modify the previous search by positioning the caret using the arrow keys.</span></span>

    ![<span data-ttu-id="9a00d-196">captura de tela da caixa de pesquisa com texto realçado</span><span class="sxs-lookup"><span data-stu-id="9a00d-196">screen shot of search box with highlighted text</span></span> ](images/ctrl-search-boxes-image9.png)

    <span data-ttu-id="9a00d-197">Neste exemplo, o texto inserido anteriormente é selecionado no foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="9a00d-197">In this example, previously entered text is selected on input focus.</span></span>

-   <span data-ttu-id="9a00d-198">**Atribua o atalho de teclado para que a caixa de pesquisa seja Ctrl + E.**</span><span class="sxs-lookup"><span data-stu-id="9a00d-198">**Assign the keyboard shortcut for the Search box to be Ctrl+E.**</span></span>

### <a name="functionality"></a><span data-ttu-id="9a00d-199">Funcionalidade</span><span class="sxs-lookup"><span data-stu-id="9a00d-199">Functionality</span></span>

-   <span data-ttu-id="9a00d-200">**Dê suporte à pesquisa instantânea sempre que possível.**</span><span class="sxs-lookup"><span data-stu-id="9a00d-200">**Support Instant search whenever possible.**</span></span> <span data-ttu-id="9a00d-201">Forneça pesquisas regulares e instantâneas se houver cenários em que a pesquisa regular vale o tempo de espera extra.</span><span class="sxs-lookup"><span data-stu-id="9a00d-201">Provide both regular and Instant searches if there are scenarios where regular searching is worth the extra wait time.</span></span>
-   <span data-ttu-id="9a00d-202">Pesquisas regulares devem retornar resultados relevantes em cinco segundos e a pesquisa instantânea deve retornar resultados dentro de dois segundos.</span><span class="sxs-lookup"><span data-stu-id="9a00d-202">Regular searches must return relevant results within five seconds and Instant search must return results within two seconds.</span></span> <span data-ttu-id="9a00d-203">Após esse ponto, a pesquisa pode continuar a preencher resultados menos relevantes ao longo do tempo, desde que o programa seja responsivo e os usuários possam executar outras tarefas.</span><span class="sxs-lookup"><span data-stu-id="9a00d-203">After this point, Search may continue to fill in less relevant results over time as long as the program is responsive and users can perform other tasks.</span></span> <span data-ttu-id="9a00d-204">Talvez seja necessário indexar os dados de pesquisa para garantir essa capacidade de resposta.</span><span class="sxs-lookup"><span data-stu-id="9a00d-204">You may have to index your search data to ensure this responsiveness.</span></span>
-   <span data-ttu-id="9a00d-205">Se você fornecer modos de pesquisa normais e instantâneos, os resultados da pesquisa instantânea deverão ser um subconjunto dos resultados da pesquisa regular.</span><span class="sxs-lookup"><span data-stu-id="9a00d-205">If you provide both regular and Instant search modes, the Instant search results must be a subset of the regular search results.</span></span>
-   <span data-ttu-id="9a00d-206">Toda pesquisa é baseada em prefixo (sem Subcadeia ou pesquisa de sufixo).</span><span class="sxs-lookup"><span data-stu-id="9a00d-206">All searching is prefix-based (no substring or suffix searching).</span></span> <span data-ttu-id="9a00d-207">O uso de caracteres curinga à direita é opcional e não afeta os resultados.</span><span class="sxs-lookup"><span data-stu-id="9a00d-207">The use of trailing wildcard characters is optional and doesn't affect the results.</span></span> <span data-ttu-id="9a00d-208">Se várias palavras forem inseridas, use ou pesquisando.</span><span class="sxs-lookup"><span data-stu-id="9a00d-208">If multiple words are entered, use OR searching.</span></span>
-   <span data-ttu-id="9a00d-209">Uma pesquisa bem-sucedida adiciona uma página virtual com os resultados da pesquisa à pilha voltar e à barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="9a00d-209">A successful search adds a virtual page with the search results to the Back stack and Address bar.</span></span> <span data-ttu-id="9a00d-210">Várias pesquisas resultam em uma única página virtual, portanto, clicar em voltar sempre retorna a página original.</span><span class="sxs-lookup"><span data-stu-id="9a00d-210">Multiple searches result in a single virtual page, so clicking Back always returns the original page.</span></span>
-   <span data-ttu-id="9a00d-211">Se necessário para escala, classifique os resultados da pesquisa por relevância.</span><span class="sxs-lookup"><span data-stu-id="9a00d-211">If necessary for scale, rank the search results by relevance.</span></span>
-   <span data-ttu-id="9a00d-212">Uma pesquisa em branco retorna a página original.</span><span class="sxs-lookup"><span data-stu-id="9a00d-212">A blank search returns the original page.</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="9a00d-213">Dimensionamento e espaçamento recomendados</span><span class="sxs-lookup"><span data-stu-id="9a00d-213">Recommended sizing and spacing</span></span>

![<span data-ttu-id="9a00d-214">Figura de dimensionamento e espaçamento da caixa de pesquisa instantânea</span><span class="sxs-lookup"><span data-stu-id="9a00d-214">figure of instant search box sizing and spacing</span></span> ](images/ctrl-search-boxes-image10.png)

<span data-ttu-id="9a00d-215">Dimensionamento e espaçamento recomendados para pesquisa instantânea.</span><span class="sxs-lookup"><span data-stu-id="9a00d-215">Recommended sizing and spacing for Instant search.</span></span>

![<span data-ttu-id="9a00d-216">figura do espaçamento e dimensionamento da caixa de pesquisa regular</span><span class="sxs-lookup"><span data-stu-id="9a00d-216">figure of regular search box sizing and spacing</span></span> ](images/ctrl-search-boxes-image11.png)

<span data-ttu-id="9a00d-217">Dimensionamento e espaçamento recomendados para pesquisa regular.</span><span class="sxs-lookup"><span data-stu-id="9a00d-217">Recommended sizing and spacing for regular search.</span></span>

## <a name="text"></a><span data-ttu-id="9a00d-218">Texto</span><span class="sxs-lookup"><span data-stu-id="9a00d-218">Text</span></span>

-   <span data-ttu-id="9a00d-219">Para as palavras do prompt na caixa de pesquisa, faça dele uma instrução (por exemplo, digite para Pesquisar) ou indique o escopo da pesquisa (por exemplo, pesquise imagens).</span><span class="sxs-lookup"><span data-stu-id="9a00d-219">For the wording of the prompt in the Search box, either make it an instruction (for example, Type to search) or indicate the scope of the search (for example, Search for pictures).</span></span>
-   <span data-ttu-id="9a00d-220">O texto do prompt deve ser curto.</span><span class="sxs-lookup"><span data-stu-id="9a00d-220">Prompt text should be brief.</span></span> <span data-ttu-id="9a00d-221">Uma única palavra ou frase curta deve ser suficiente.</span><span class="sxs-lookup"><span data-stu-id="9a00d-221">A single word or short phrase should suffice.</span></span>
-   <span data-ttu-id="9a00d-222">Use a capitalização com estilo de frase.</span><span class="sxs-lookup"><span data-stu-id="9a00d-222">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="9a00d-223">Não use pontuação final ou reticências.</span><span class="sxs-lookup"><span data-stu-id="9a00d-223">Don't use ending punctuation or ellipsis.</span></span>

## <a name="documentation"></a><span data-ttu-id="9a00d-224">Documentação</span><span class="sxs-lookup"><span data-stu-id="9a00d-224">Documentation</span></span>

-   <span data-ttu-id="9a00d-225">Consulte este controle como a caixa de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9a00d-225">Refer to this control as the Search box.</span></span> <span data-ttu-id="9a00d-226">Colocar em maiúscula a letra inicial da primeira palavra; Não coloque em maiúscula a letra inicial da caixa.</span><span class="sxs-lookup"><span data-stu-id="9a00d-226">Capitalize the initial letter of the first word; don't capitalize the initial letter of box.</span></span>
-   <span data-ttu-id="9a00d-227">Consulte os dois tipos de pesquisa como pesquisa instantânea e pesquisa regular.</span><span class="sxs-lookup"><span data-stu-id="9a00d-227">Refer to the two types of search as Instant search and regular search.</span></span> <span data-ttu-id="9a00d-228">Colocar em maiúscula a letra inicial da pesquisa instantânea; Não coloque em maiúscula a letra inicial da pesquisa regular.</span><span class="sxs-lookup"><span data-stu-id="9a00d-228">Capitalize the initial letter of Instant search; don't capitalize the initial letter of regular search.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a00d-229">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9a00d-229">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a00d-230">Glossário</span><span class="sxs-lookup"><span data-stu-id="9a00d-230">Glossary</span></span>](glossary.md)
</dt> </dl>

 

 