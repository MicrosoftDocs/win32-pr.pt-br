---
title: list.csv
description: list.csv
ms.assetid: 020b213c-826c-430c-8ce7-92b819581de8
keywords:
- Armazenamentos online do Windows Media Player, list.csv
- lojas online, list.csv
- Digite 1 lojas online, list.csv
- list.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f41ed237c5f4a185f01feace8f09b4615e4922b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104084342"
---
# <a name="listcsv"></a><span data-ttu-id="ddf0e-107">list.csv</span><span class="sxs-lookup"><span data-stu-id="ddf0e-107">list.csv</span></span>

<span data-ttu-id="ddf0e-108">Esse arquivo contém uma entrada para cada uma das listas que o catálogo contém.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-108">This file contains an entry for each of the lists the catalog contains.</span></span> <span data-ttu-id="ddf0e-109">As listas podem ser listas de faixas, álbuns, artistas, gêneros, subgêneros ou feeds de rádio; ou podem ser listas de outras listas.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-109">Lists can be lists of tracks, albums, artists, genres, subgenres, or radio feeds; or they can be lists of other lists.</span></span> <span data-ttu-id="ddf0e-110">Cada entrada de lista é uma linha composta pelos campos delimitados por tabulação descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-110">Each list entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="ddf0e-111">Os campos devem aparecer na ordem listada.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-111">Fields must appear in the order listed.</span></span>

<span data-ttu-id="ddf0e-112">A coluna Format na tabela a seguir descreve a maneira como cada campo de texto Unicode é formatado.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-112">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="ddf0e-113">Ele não se refere ao tipo de dados do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-113">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="ddf0e-114">Por exemplo, se Integer for indicado na coluna Format, significa que o campo contém uma cadeia de caracteres Unicode que representa um valor integral, em vez de um inteiro real.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-114">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ddf0e-115">Campo</span><span class="sxs-lookup"><span data-stu-id="ddf0e-115">Field</span></span></th>
<th><span data-ttu-id="ddf0e-116">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ddf0e-116">Required</span></span></th>
<th><span data-ttu-id="ddf0e-117">Formatar</span><span class="sxs-lookup"><span data-stu-id="ddf0e-117">Format</span></span></th>
<th><span data-ttu-id="ddf0e-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="ddf0e-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ddf0e-119">ListID</span><span class="sxs-lookup"><span data-stu-id="ddf0e-119">ListID</span></span></td>
<td><span data-ttu-id="ddf0e-120">Sim</span><span class="sxs-lookup"><span data-stu-id="ddf0e-120">Yes</span></span></td>
<td><span data-ttu-id="ddf0e-121">Inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-121">Non-negative integer.</span></span></td>
<td><span data-ttu-id="ddf0e-122">Identificador de lista, exclusivo dentro de list.csv.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-122">List identifier, unique within list.csv.</span></span> <span data-ttu-id="ddf0e-123">Deve ser não negativo e menor que 2 ^ 32. <strong>Exibindo um nó de lista no controle de exibição de árvore:</strong> Se ListId for 0, 1, 2, 3, 4, 5, 6 ou 7, a lista será exibida como um nó personalizado no nó de nível superior da loja online no controle de exibição de árvore do Player.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-123">Must be non-negative and less than 2^32.<strong>Displaying a list node in tree view control:</strong> If the ListID is 0, 1, 2, 3, 4, 5, 6, or 7, the list will appear as a custom node under your online store's top-level node in the Player's tree view control.</span></span> <span data-ttu-id="ddf0e-124">Os nós personalizados aparecem antes dos nós padrão no nó de nível superior da loja online e são posicionados em ordem crescente por lista de classificação.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-124">Custom nodes appear before the standard nodes under the online store's top-level node, and they are positioned in ascending order by ListID.</span></span> <span data-ttu-id="ddf0e-125">Por exemplo, se houver três nós personalizados, com ListIDs de 1, 3 e 5, eles serão exibidos primeiro, segundo e terceiro sob o nó de nível superior da loja online.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-125">For example, if there are three custom nodes, with ListIDs of 1, 3, and 5, they will be displayed first, second, and third under the online store's top level node.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddf0e-126">ListTitle</span><span class="sxs-lookup"><span data-stu-id="ddf0e-126">ListTitle</span></span></td>
<td><span data-ttu-id="ddf0e-127">Não</span><span class="sxs-lookup"><span data-stu-id="ddf0e-127">No</span></span></td>
<td><span data-ttu-id="ddf0e-128">Cadeia de caracteres Unicode. Exemplo: dez principais ocorrências</span><span class="sxs-lookup"><span data-stu-id="ddf0e-128">Unicode string.Example: Top Ten Hits</span></span><br/></td>
<td><span data-ttu-id="ddf0e-129">Título da lista.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-129">List title.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddf0e-130">ListSubtitle</span><span class="sxs-lookup"><span data-stu-id="ddf0e-130">ListSubtitle</span></span></td>
<td><span data-ttu-id="ddf0e-131">Não</span><span class="sxs-lookup"><span data-stu-id="ddf0e-131">No</span></span></td>
<td><span data-ttu-id="ddf0e-132">Cadeia de caracteres Unicode</span><span class="sxs-lookup"><span data-stu-id="ddf0e-132">Unicode string</span></span></td>
<td><span data-ttu-id="ddf0e-133">Listar título alternativo, exibido na segunda linha da exibição de bloco.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-133">List alternate title, displayed in the second line of the Tile view.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddf0e-134">ListDescription</span><span class="sxs-lookup"><span data-stu-id="ddf0e-134">ListDescription</span></span></td>
<td><span data-ttu-id="ddf0e-135">Sim</span><span class="sxs-lookup"><span data-stu-id="ddf0e-135">Yes</span></span></td>
<td><span data-ttu-id="ddf0e-136">Cadeia de caracteres Unicode</span><span class="sxs-lookup"><span data-stu-id="ddf0e-136">Unicode string</span></span></td>
<td><span data-ttu-id="ddf0e-137">Listar texto de exibição amigável (exibido em páginas de propriedades).</span><span class="sxs-lookup"><span data-stu-id="ddf0e-137">List friendly display text (displayed in property pages).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddf0e-138">Linked_ItemType</span><span class="sxs-lookup"><span data-stu-id="ddf0e-138">Linked_ItemType</span></span></td>
<td><span data-ttu-id="ddf0e-139">Sim</span><span class="sxs-lookup"><span data-stu-id="ddf0e-139">Yes</span></span></td>
<td><span data-ttu-id="ddf0e-140">Cadeia de caracteres Unicode. Formato: [T | P | A | L | G | S | D</span><span class="sxs-lookup"><span data-stu-id="ddf0e-140">Unicode string.Format: [T|P|A|L|G|S|R]</span></span><br/> <span data-ttu-id="ddf0e-141">Exemplo: T</span><span class="sxs-lookup"><span data-stu-id="ddf0e-141">Example: T</span></span><br/></td>
<td><span data-ttu-id="ddf0e-142">Indica o tipo dos itens vinculados.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-142">Indicates the type of the linked items.</span></span>
<ul>
<li><span data-ttu-id="ddf0e-143">T = faixa</span><span class="sxs-lookup"><span data-stu-id="ddf0e-143">T= Track</span></span></li>
<li><span data-ttu-id="ddf0e-144">P = executor</span><span class="sxs-lookup"><span data-stu-id="ddf0e-144">P = Performer</span></span></li>
<li><span data-ttu-id="ddf0e-145">A = álbum</span><span class="sxs-lookup"><span data-stu-id="ddf0e-145">A = Album</span></span></li>
<li><span data-ttu-id="ddf0e-146">L = lista</span><span class="sxs-lookup"><span data-stu-id="ddf0e-146">L = List</span></span></li>
<li><span data-ttu-id="ddf0e-147">G = gênero</span><span class="sxs-lookup"><span data-stu-id="ddf0e-147">G = Genre</span></span></li>
<li><span data-ttu-id="ddf0e-148">S = subgênero</span><span class="sxs-lookup"><span data-stu-id="ddf0e-148">S = Subgenre</span></span></li>
<li><span data-ttu-id="ddf0e-149">R = rádio</span><span class="sxs-lookup"><span data-stu-id="ddf0e-149">R = Radio</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddf0e-150">ListPrice</span><span class="sxs-lookup"><span data-stu-id="ddf0e-150">ListPrice</span></span></td>
<td><span data-ttu-id="ddf0e-151">Sim</span><span class="sxs-lookup"><span data-stu-id="ddf0e-151">Yes</span></span></td>
<td><span data-ttu-id="ddf0e-152">Cadeia de caracteres Unicode. Exemplo: $9.99</span><span class="sxs-lookup"><span data-stu-id="ddf0e-152">Unicode string.Example: $9.99</span></span><br/></td>
<td><span data-ttu-id="ddf0e-153">Preço da lista.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-153">Price of the list.</span></span> <span data-ttu-id="ddf0e-154">O símbolo de moeda deve ser incluído. Um zero significa que a lista é gratuita.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-154">The currency symbol should be included.A zero means the list is free.</span></span> <span data-ttu-id="ddf0e-155">Nenhum valor significa que o preço é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-155">No value means the price is unknown.</span></span> <span data-ttu-id="ddf0e-156">Um hífen significa que a lista não pode ser comprada.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-156">A hyphen means the list cannot be purchased.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddf0e-157">Popularidade</span><span class="sxs-lookup"><span data-stu-id="ddf0e-157">Popularity</span></span></td>
<td><span data-ttu-id="ddf0e-158">Sim</span><span class="sxs-lookup"><span data-stu-id="ddf0e-158">Yes</span></span></td>
<td><span data-ttu-id="ddf0e-159">Valor inteiro ou Decimal. Exemplo: 1259,3</span><span class="sxs-lookup"><span data-stu-id="ddf0e-159">Integer or decimal value.Example: 1259.3</span></span><br/></td>
<td><span data-ttu-id="ddf0e-160">Indica a classificação de popularidade quando essa lista aparece em outras listas.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-160">Indicates the popularity ranking when this list appears in other lists.</span></span> <span data-ttu-id="ddf0e-161">Pode ser zero se não for aplicável..</span><span class="sxs-lookup"><span data-stu-id="ddf0e-161">Can be zero if not applicable..</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddf0e-162">IsRecentlyAdded</span><span class="sxs-lookup"><span data-stu-id="ddf0e-162">IsRecentlyAdded</span></span></td>
<td><span data-ttu-id="ddf0e-163">Sim</span><span class="sxs-lookup"><span data-stu-id="ddf0e-163">Yes</span></span></td>
<td><span data-ttu-id="ddf0e-164">Booliano. formato: [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="ddf0e-164">Boolean.Format: [0|1]</span></span><br/> <span data-ttu-id="ddf0e-165">Exemplo: 0</span><span class="sxs-lookup"><span data-stu-id="ddf0e-165">Example: 0</span></span><br/></td>
<td><span data-ttu-id="ddf0e-166">Indica se a lista foi adicionada recentemente.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-166">Indicates whether the list was recently added.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddf0e-167">Isfeatured</span><span class="sxs-lookup"><span data-stu-id="ddf0e-167">IsFeatured</span></span></td>
<td><span data-ttu-id="ddf0e-168">Sim</span><span class="sxs-lookup"><span data-stu-id="ddf0e-168">Yes</span></span></td>
<td><span data-ttu-id="ddf0e-169">Booliano. formato: [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="ddf0e-169">Boolean.Format: [0|1]</span></span><br/> <span data-ttu-id="ddf0e-170">Exemplo: 0</span><span class="sxs-lookup"><span data-stu-id="ddf0e-170">Example: 0</span></span><br/></td>
<td><span data-ttu-id="ddf0e-171">Indica se a lista está em destaque.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-171">Indicates whether the list is featured.</span></span> <span data-ttu-id="ddf0e-172">Pode ser usado para determinar a ordem de classificação.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-172">Can be used in determining sort order.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddf0e-173">EditorialGlyph</span><span class="sxs-lookup"><span data-stu-id="ddf0e-173">EditorialGlyph</span></span></td>
<td><span data-ttu-id="ddf0e-174">Sim</span><span class="sxs-lookup"><span data-stu-id="ddf0e-174">Yes</span></span></td>
<td><span data-ttu-id="ddf0e-175">Inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-175">Non-negative integer.</span></span> <span data-ttu-id="ddf0e-176">Deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-176">Should be 0.</span></span></td>
<td><span data-ttu-id="ddf0e-177">Não usado nesta versão.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-177">Not used in this release.</span></span> <span data-ttu-id="ddf0e-178">Deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-178">Should be 0.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddf0e-179">ViewType</span><span class="sxs-lookup"><span data-stu-id="ddf0e-179">ViewType</span></span></td>
<td><span data-ttu-id="ddf0e-180">Sim</span><span class="sxs-lookup"><span data-stu-id="ddf0e-180">Yes</span></span></td>
<td><span data-ttu-id="ddf0e-181">Cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-181">Unicode string.</span></span> <span data-ttu-id="ddf0e-182">Formato: [I | T | R | L | O] exemplo: T</span><span class="sxs-lookup"><span data-stu-id="ddf0e-182">Format: [I|T|R|L|O]Example: T</span></span><br/></td>
<td><span data-ttu-id="ddf0e-183">Indica o tipo de exibição a ser usado para a lista.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-183">Indicates the view type to use for the list.</span></span>
<ul>
<li><span data-ttu-id="ddf0e-184">I = ícone</span><span class="sxs-lookup"><span data-stu-id="ddf0e-184">I = Icon</span></span></li>
<li><span data-ttu-id="ddf0e-185">T = bloco</span><span class="sxs-lookup"><span data-stu-id="ddf0e-185">T = Tile</span></span></li>
<li><span data-ttu-id="ddf0e-186">R = relatório</span><span class="sxs-lookup"><span data-stu-id="ddf0e-186">R = Report</span></span></li>
<li><span data-ttu-id="ddf0e-187">L = lista</span><span class="sxs-lookup"><span data-stu-id="ddf0e-187">L = List</span></span></li>
<li><span data-ttu-id="ddf0e-188">O = lista ordenada</span><span class="sxs-lookup"><span data-stu-id="ddf0e-188">O = Ordered List</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddf0e-189">ViewImageSize</span><span class="sxs-lookup"><span data-stu-id="ddf0e-189">ViewImageSize</span></span></td>
<td><span data-ttu-id="ddf0e-190">Sim</span><span class="sxs-lookup"><span data-stu-id="ddf0e-190">Yes</span></span></td>
<td><span data-ttu-id="ddf0e-191">Inteiro não negativo. Exemplo: 180</span><span class="sxs-lookup"><span data-stu-id="ddf0e-191">Non-negative integer.Example: 180</span></span><br/></td>
<td><span data-ttu-id="ddf0e-192">O tamanho no qual a imagem da lista é exibida.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-192">The size at which the list image is displayed.</span></span> <span data-ttu-id="ddf0e-193">Se for 0, o tamanho será determinado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-193">If 0, size is determined automatically.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddf0e-194">GroupBy</span><span class="sxs-lookup"><span data-stu-id="ddf0e-194">GroupBy</span></span></td>
<td><span data-ttu-id="ddf0e-195">Sim</span><span class="sxs-lookup"><span data-stu-id="ddf0e-195">Yes</span></span></td>
<td><span data-ttu-id="ddf0e-196">Cadeia de caracteres Unicode. Formato: [-| P | A | C | R | 3D</span><span class="sxs-lookup"><span data-stu-id="ddf0e-196">Unicode string.Format: [-|P|A|C|R|D]</span></span><br/> <span data-ttu-id="ddf0e-197">Exemplo: P</span><span class="sxs-lookup"><span data-stu-id="ddf0e-197">Example: P</span></span><br/></td>
<td><span data-ttu-id="ddf0e-198">Indica qual campo é usado para agrupar os itens na lista.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-198">Indicates what field is used to group the items in the list.</span></span>
<ul>
<li><span data-ttu-id="ddf0e-199">- = Automático</span><span class="sxs-lookup"><span data-stu-id="ddf0e-199">- = Automatic</span></span></li>
<li><span data-ttu-id="ddf0e-200">P = executor</span><span class="sxs-lookup"><span data-stu-id="ddf0e-200">P = Performer</span></span></li>
<li><span data-ttu-id="ddf0e-201">A = álbum</span><span class="sxs-lookup"><span data-stu-id="ddf0e-201">A = Album</span></span></li>
<li><span data-ttu-id="ddf0e-202">C = Composer</span><span class="sxs-lookup"><span data-stu-id="ddf0e-202">C = Composer</span></span></li>
<li><span data-ttu-id="ddf0e-203">R = classificação</span><span class="sxs-lookup"><span data-stu-id="ddf0e-203">R = Rating</span></span></li>
<li><span data-ttu-id="ddf0e-204">D = data</span><span class="sxs-lookup"><span data-stu-id="ddf0e-204">D = Date</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddf0e-205">ListItemsAreDynamic</span><span class="sxs-lookup"><span data-stu-id="ddf0e-205">ListItemsAreDynamic</span></span></td>
<td><span data-ttu-id="ddf0e-206">Sim</span><span class="sxs-lookup"><span data-stu-id="ddf0e-206">Yes</span></span></td>
<td><span data-ttu-id="ddf0e-207">Booliano.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-207">Boolean.</span></span> <span data-ttu-id="ddf0e-208">Pode ser 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-208">Can be 0 or 1.</span></span></td>
<td><span data-ttu-id="ddf0e-209">Indica se a lista é gerada dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-209">Indicates whether the list is generated dynamically.</span></span> <span data-ttu-id="ddf0e-210">Listas dinâmicas não têm itens em listitem.csv.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-210">Dynamic lists do not have items in listitem.csv.</span></span> <span data-ttu-id="ddf0e-211">Se uma lista for marcada como dinâmica, seus itens serão fornecidos por <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner:: GetListContents</a></span><span class="sxs-lookup"><span data-stu-id="ddf0e-211">If a list is marked as dynamic, its items are provided by <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner::GetListContents</a></span></span></td>
</tr>
</tbody>
</table>



 

 

 





