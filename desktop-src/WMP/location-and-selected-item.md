---
title: Local e item selecionado
description: Local e item selecionado
ms.assetid: 9556e01f-1f75-4089-9e62-b41a9aa53e93
keywords:
- Lojas online do Windows Media Player, locais
- lojas online, locais
- tipos 1 lojas online, locais
- Lojas online do Windows Media Player, locais de biblioteca
- lojas online, locais de biblioteca
- Digite 1 lojas online, locais de biblioteca
- Lojas online do Windows Media Player, itens selecionados
- lojas online, itens selecionados
- Digite 1 lojas online, itens selecionados
- Biblioteca do Windows Media Player, locais
- Biblioteca do Windows Media Player, itens selecionados
- biblioteca, locais
- biblioteca, itens selecionados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d665b11e7509e369224d3e85db30dddb4a988a14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159726"
---
# <a name="location-and-selected-item"></a><span data-ttu-id="9b5cf-116">Local e item selecionado</span><span class="sxs-lookup"><span data-stu-id="9b5cf-116">Location and Selected Item</span></span>

<span data-ttu-id="9b5cf-117">O Windows Media Player usa os cinco itens a seguir para caracterizar sua exibição atual do conteúdo da loja online:</span><span class="sxs-lookup"><span data-stu-id="9b5cf-117">Windows Media Player uses the following five items to characterize its current view of online store content:</span></span>

-   <span data-ttu-id="9b5cf-118">task</span><span class="sxs-lookup"><span data-stu-id="9b5cf-118">task</span></span>
-   <span data-ttu-id="9b5cf-119">tipo de local da biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b5cf-119">library location type</span></span>
-   <span data-ttu-id="9b5cf-120">ID do local da biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b5cf-120">library location ID</span></span>
-   <span data-ttu-id="9b5cf-121">tipo de item selecionado</span><span class="sxs-lookup"><span data-stu-id="9b5cf-121">selected item type</span></span>
-   <span data-ttu-id="9b5cf-122">ID do item selecionado</span><span class="sxs-lookup"><span data-stu-id="9b5cf-122">selected item ID</span></span>

<span data-ttu-id="9b5cf-123">Normalmente, você pode considerar o modo de exibição no Windows Media Player como um contêiner de itens.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-123">Typically, you can think of the view in Windows Media Player as a container of items.</span></span> <span data-ttu-id="9b5cf-124">O contêiner tem um tipo e um item tem um tipo.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-124">The container has a type, and an item has a type.</span></span> <span data-ttu-id="9b5cf-125">Todos os itens em um contêiner têm o mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-125">All the items in a container have the same type.</span></span> <span data-ttu-id="9b5cf-126">Tipos de localização e tipos de item são especificados pelas [constantes de local de biblioteca](library-location-constants.md).</span><span class="sxs-lookup"><span data-stu-id="9b5cf-126">Location types and item types are both specified by the [library location constants](library-location-constants.md).</span></span> <span data-ttu-id="9b5cf-127">Por exemplo, se a exibição atual estiver mostrando um álbum individual, o tipo de local da biblioteca será CPAlbumID e, como um álbum conterá faixas, o tipo de item selecionado será CPTrackID.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-127">For example, if the current view is showing an individual album, the library location type is CPAlbumID, and, because an album contains tracks, the selected item type is CPTrackID.</span></span>

<span data-ttu-id="9b5cf-128">A tabela a seguir mostra os tipos de local e item para vários contêineres.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-128">The following table shows the location and item types for several containers.</span></span>



| <span data-ttu-id="9b5cf-129">Descrição do contêiner</span><span class="sxs-lookup"><span data-stu-id="9b5cf-129">Description of container</span></span>                              | <span data-ttu-id="9b5cf-130">Tipo de local da biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b5cf-130">Library location type</span></span> | <span data-ttu-id="9b5cf-131">Tipo de item selecionado</span><span class="sxs-lookup"><span data-stu-id="9b5cf-131">Selected item type</span></span> |
|-------------------------------------------------------|-----------------------|--------------------|
| <span data-ttu-id="9b5cf-132">Um álbum que é um contêiner de faixas</span><span class="sxs-lookup"><span data-stu-id="9b5cf-132">An album that is a container of tracks</span></span>                | <span data-ttu-id="9b5cf-133">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="9b5cf-133">CPAlbumID</span></span>             | <span data-ttu-id="9b5cf-134">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="9b5cf-134">CPTrackID</span></span>          |
| <span data-ttu-id="9b5cf-135">Uma lista que é um contêiner de faixas</span><span class="sxs-lookup"><span data-stu-id="9b5cf-135">A list that is a container of tracks</span></span>                  | <span data-ttu-id="9b5cf-136">CPListID</span><span class="sxs-lookup"><span data-stu-id="9b5cf-136">CPListID</span></span>              | <span data-ttu-id="9b5cf-137">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="9b5cf-137">CPTrackID</span></span>          |
| <span data-ttu-id="9b5cf-138">Uma lista que é um contêiner de álbuns</span><span class="sxs-lookup"><span data-stu-id="9b5cf-138">A list that is a container of albums</span></span>                  | <span data-ttu-id="9b5cf-139">CPListID</span><span class="sxs-lookup"><span data-stu-id="9b5cf-139">CPListID</span></span>              | <span data-ttu-id="9b5cf-140">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="9b5cf-140">CPAlbumID</span></span>          |
| <span data-ttu-id="9b5cf-141">Uma estação de rádio que é um contêiner de listas</span><span class="sxs-lookup"><span data-stu-id="9b5cf-141">A radio station that is a container of lists</span></span>          | <span data-ttu-id="9b5cf-142">CPRadioID</span><span class="sxs-lookup"><span data-stu-id="9b5cf-142">CPRadioID</span></span>             | <span data-ttu-id="9b5cf-143">CPListID</span><span class="sxs-lookup"><span data-stu-id="9b5cf-143">CPListID</span></span>           |
| <span data-ttu-id="9b5cf-144">O conjunto de todos os álbuns, que é um contêiner de álbuns</span><span class="sxs-lookup"><span data-stu-id="9b5cf-144">The set of all albums, which is a container of albums</span></span> | <span data-ttu-id="9b5cf-145">AllCPAlbumIDs</span><span class="sxs-lookup"><span data-stu-id="9b5cf-145">AllCPAlbumIDs</span></span>         | <span data-ttu-id="9b5cf-146">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="9b5cf-146">CPAlbumID</span></span>          |
| <span data-ttu-id="9b5cf-147">O conjunto de todos os gêneros, que é um contêiner de gêneros</span><span class="sxs-lookup"><span data-stu-id="9b5cf-147">The set of all genres, which is a container of genres</span></span> | <span data-ttu-id="9b5cf-148">AllCPGenreIDs</span><span class="sxs-lookup"><span data-stu-id="9b5cf-148">AllCPGenreIDs</span></span>         | <span data-ttu-id="9b5cf-149">CPGenreID</span><span class="sxs-lookup"><span data-stu-id="9b5cf-149">CPGenreID</span></span>          |



 

<span data-ttu-id="9b5cf-150">As guias no Windows Media Player representam tarefas diferentes.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-150">The tabs in Windows Media Player represent different tasks.</span></span> <span data-ttu-id="9b5cf-151">O Player exibe o conteúdo da loja online em três painéis de tarefas diferentes: **biblioteca**, **gravação** e **sincronização**. O painel de tarefas biblioteca também é chamado de painel de tarefas **procurar** .</span><span class="sxs-lookup"><span data-stu-id="9b5cf-151">The Player displays online store content in three different task panes: **Library**, **Burn**, and **Sync**. The Library task pane is also called the **Browse** task pane.</span></span> <span data-ttu-id="9b5cf-152">Às vezes, um painel de tarefas é chamado de *recurso*, por isso você pode ver termos como o recurso de *gravação* e o *recurso de sincronização* nesta documentação.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-152">Sometimes, a task pane is called a *feature*, so you might see terms like *Burn feature* and *Sync feature* in this documentation.</span></span>

<span data-ttu-id="9b5cf-153">Os exemplos a seguir mostram como o Windows Media Player usa as cinco partes de informações (tarefa, tipo de local da biblioteca, ID do local da biblioteca, tipo de item selecionado, ID do item selecionado) para caracterizar exibições diferentes.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-153">The following examples show how Windows Media Player uses the five pieces of information (task, library location type, library location ID, selected item type, selected Item ID) to characterize different views.</span></span>

<span data-ttu-id="9b5cf-154">No painel de tarefas **gravar** , o player está exibindo um álbum como um contêiner de faixas.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-154">In the **Burn** task pane, the Player is displaying an album as a container of tracks.</span></span> <span data-ttu-id="9b5cf-155">O álbum tem uma ID de 250.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-155">The album has an ID of 250.</span></span> <span data-ttu-id="9b5cf-156">Na exibição, o item selecionado é a faixa que tem uma ID de 800.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-156">In the view, the selected item is the track that has an ID of 800.</span></span> <span data-ttu-id="9b5cf-157">Observe que 800 é a ID da faixa no catálogo da loja online, não o número do controle no álbum.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-157">Note that 800 is the ID of the track in the online store's catalog, not the number of the track on the album.</span></span>



| <span data-ttu-id="9b5cf-158">Item</span><span class="sxs-lookup"><span data-stu-id="9b5cf-158">Item</span></span>                  | <span data-ttu-id="9b5cf-159">Valor</span><span class="sxs-lookup"><span data-stu-id="9b5cf-159">Value</span></span>     |
|-----------------------|-----------|
| <span data-ttu-id="9b5cf-160">task</span><span class="sxs-lookup"><span data-stu-id="9b5cf-160">task</span></span>                  | <span data-ttu-id="9b5cf-161">Queima</span><span class="sxs-lookup"><span data-stu-id="9b5cf-161">Burn</span></span>      |
| <span data-ttu-id="9b5cf-162">tipo de local da biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b5cf-162">library location type</span></span> | <span data-ttu-id="9b5cf-163">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="9b5cf-163">CPAlbumID</span></span> |
| <span data-ttu-id="9b5cf-164">ID do local da biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b5cf-164">library location ID</span></span>   | <span data-ttu-id="9b5cf-165">250</span><span class="sxs-lookup"><span data-stu-id="9b5cf-165">250</span></span>       |
| <span data-ttu-id="9b5cf-166">tipo de item selecionado</span><span class="sxs-lookup"><span data-stu-id="9b5cf-166">selected item type</span></span>    | <span data-ttu-id="9b5cf-167">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="9b5cf-167">CPTrackID</span></span> |
| <span data-ttu-id="9b5cf-168">ID do item selecionado</span><span class="sxs-lookup"><span data-stu-id="9b5cf-168">selected item ID</span></span>      | <span data-ttu-id="9b5cf-169">800</span><span class="sxs-lookup"><span data-stu-id="9b5cf-169">800</span></span>       |



 

<span data-ttu-id="9b5cf-170">No painel de tarefas **sincronizar** , o player está exibindo o conjunto de todos os álbuns, que é um contêiner de álbuns.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-170">In the **Sync** task pane, the Player is displaying the set of all albums, which is a container of albums.</span></span> <span data-ttu-id="9b5cf-171">Na exibição, o item selecionado é o álbum que tem uma ID de 300.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-171">In the view, the selected item is the album that has an ID of 300.</span></span> <span data-ttu-id="9b5cf-172">Observe que a ID do local da biblioteca não é aplicável a esta exibição.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-172">Note that the library location ID is not applicable to this view.</span></span>



| <span data-ttu-id="9b5cf-173">Item</span><span class="sxs-lookup"><span data-stu-id="9b5cf-173">Item</span></span>                  | <span data-ttu-id="9b5cf-174">Valor</span><span class="sxs-lookup"><span data-stu-id="9b5cf-174">Value</span></span>         |
|-----------------------|---------------|
| <span data-ttu-id="9b5cf-175">task</span><span class="sxs-lookup"><span data-stu-id="9b5cf-175">task</span></span>                  | <span data-ttu-id="9b5cf-176">Sincronizar</span><span class="sxs-lookup"><span data-stu-id="9b5cf-176">Sync</span></span>          |
| <span data-ttu-id="9b5cf-177">tipo de local da biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b5cf-177">library location type</span></span> | <span data-ttu-id="9b5cf-178">AllCPAlbumIDs</span><span class="sxs-lookup"><span data-stu-id="9b5cf-178">AllCPAlbumIDs</span></span> |
| <span data-ttu-id="9b5cf-179">ID do local da biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b5cf-179">library location ID</span></span>   | <span data-ttu-id="9b5cf-180">N/D</span><span class="sxs-lookup"><span data-stu-id="9b5cf-180">N/A</span></span>           |
| <span data-ttu-id="9b5cf-181">tipo de item selecionado</span><span class="sxs-lookup"><span data-stu-id="9b5cf-181">selected item type</span></span>    | <span data-ttu-id="9b5cf-182">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="9b5cf-182">CPAlbumID</span></span>     |
| <span data-ttu-id="9b5cf-183">ID do item selecionado</span><span class="sxs-lookup"><span data-stu-id="9b5cf-183">selected item ID</span></span>      | <span data-ttu-id="9b5cf-184">300</span><span class="sxs-lookup"><span data-stu-id="9b5cf-184">300</span></span>           |



 

<span data-ttu-id="9b5cf-185">No controle de exibição em árvore, o nó raiz do repositório online é selecionado.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-185">In the tree-view control, the root node for the online store is selected.</span></span> <span data-ttu-id="9b5cf-186">Nesse caso, não há nenhum contêiner e, consequentemente, não há itens.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-186">In this case, there is no container, and consequently, there are no items.</span></span> <span data-ttu-id="9b5cf-187">O painel de tarefas da **biblioteca** inteira está exibindo uma página de descoberta.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-187">The entire **Library** task pane is displaying a discovery page.</span></span>



| <span data-ttu-id="9b5cf-188">Item</span><span class="sxs-lookup"><span data-stu-id="9b5cf-188">Item</span></span>                  | <span data-ttu-id="9b5cf-189">Valor</span><span class="sxs-lookup"><span data-stu-id="9b5cf-189">Value</span></span>           |
|-----------------------|-----------------|
| <span data-ttu-id="9b5cf-190">task</span><span class="sxs-lookup"><span data-stu-id="9b5cf-190">task</span></span>                  | <span data-ttu-id="9b5cf-191">Procurar</span><span class="sxs-lookup"><span data-stu-id="9b5cf-191">Browse</span></span>          |
| <span data-ttu-id="9b5cf-192">tipo de local da biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b5cf-192">library location type</span></span> | <span data-ttu-id="9b5cf-193">RootLocation</span><span class="sxs-lookup"><span data-stu-id="9b5cf-193">RootLocation</span></span>    |
| <span data-ttu-id="9b5cf-194">ID do local da biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b5cf-194">library location ID</span></span>   | <span data-ttu-id="9b5cf-195">N/D</span><span class="sxs-lookup"><span data-stu-id="9b5cf-195">N/A</span></span>             |
| <span data-ttu-id="9b5cf-196">tipo de item selecionado</span><span class="sxs-lookup"><span data-stu-id="9b5cf-196">selected item type</span></span>    | <span data-ttu-id="9b5cf-197">UnknownLocation</span><span class="sxs-lookup"><span data-stu-id="9b5cf-197">UnknownLocation</span></span> |
| <span data-ttu-id="9b5cf-198">ID do item selecionado</span><span class="sxs-lookup"><span data-stu-id="9b5cf-198">selected item ID</span></span>      | <span data-ttu-id="9b5cf-199">N/D</span><span class="sxs-lookup"><span data-stu-id="9b5cf-199">N/A</span></span>             |



 

<span data-ttu-id="9b5cf-200">No painel de tarefas **sincronizar** , o player está exibindo o ano 2002 como um contêiner de faixas.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-200">In the **Sync** task pane, the Player is displaying the year 2002 as a container of tracks.</span></span> <span data-ttu-id="9b5cf-201">Na exibição, o item selecionado é a faixa que tem uma ID de 450.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-201">In the view, the selected item is the track that has an ID of 450.</span></span>



| <span data-ttu-id="9b5cf-202">Item</span><span class="sxs-lookup"><span data-stu-id="9b5cf-202">Item</span></span>                  | <span data-ttu-id="9b5cf-203">Valor</span><span class="sxs-lookup"><span data-stu-id="9b5cf-203">Value</span></span>           |
|-----------------------|-----------------|
| <span data-ttu-id="9b5cf-204">task</span><span class="sxs-lookup"><span data-stu-id="9b5cf-204">task</span></span>                  | <span data-ttu-id="9b5cf-205">Sincronizar</span><span class="sxs-lookup"><span data-stu-id="9b5cf-205">Sync</span></span>            |
| <span data-ttu-id="9b5cf-206">tipo de local da biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b5cf-206">library location type</span></span> | <span data-ttu-id="9b5cf-207">ReleaseDateYear</span><span class="sxs-lookup"><span data-stu-id="9b5cf-207">ReleaseDateYear</span></span> |
| <span data-ttu-id="9b5cf-208">ID do local da biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b5cf-208">library location ID</span></span>   | <span data-ttu-id="9b5cf-209">2002</span><span class="sxs-lookup"><span data-stu-id="9b5cf-209">2002</span></span>            |
| <span data-ttu-id="9b5cf-210">tipo de item selecionado</span><span class="sxs-lookup"><span data-stu-id="9b5cf-210">selected item type</span></span>    | <span data-ttu-id="9b5cf-211">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="9b5cf-211">CPTrackID</span></span>       |
| <span data-ttu-id="9b5cf-212">ID do item selecionado</span><span class="sxs-lookup"><span data-stu-id="9b5cf-212">selected item ID</span></span>      | <span data-ttu-id="9b5cf-213">450</span><span class="sxs-lookup"><span data-stu-id="9b5cf-213">450</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="9b5cf-214">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9b5cf-214">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b5cf-215">**Sobre o tipo 1 lojas online**</span><span class="sxs-lookup"><span data-stu-id="9b5cf-215">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="9b5cf-216">**Páginas de descoberta**</span><span class="sxs-lookup"><span data-stu-id="9b5cf-216">**Discovery Pages**</span></span>](discovery-pages.md)
</dt> </dl>

 

 




