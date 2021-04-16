---
title: Comportamento de fallback de fontes HTML
description: Comportamento de fallback de fontes HTML
ms.assetid: 5BDFBD58-0B34-4A58-BFAF-B8BB1DD569DB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc7da95c46190fd348dda72edc8283ee6438b00
ms.sourcegitcommit: 80bac5863880f1bd4c1c3e06db27c5d8fb5232b4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "105773012"
---
# <a name="html-font-fallback-behavior"></a><span data-ttu-id="14e25-103">Comportamento de fallback de fontes HTML</span><span class="sxs-lookup"><span data-stu-id="14e25-103">HTML font fallback behavior</span></span>

## <a name="platform"></a><span data-ttu-id="14e25-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="14e25-104">Platform</span></span>

<span data-ttu-id="14e25-105">Clientes-\* \* Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="14e25-105">Clients -\*\* Windows 8.1</span></span>  
<span data-ttu-id="14e25-106">**Servidores-** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="14e25-106">**Servers -** Windows Server 2012 R2</span></span>  


## <a name="description"></a><span data-ttu-id="14e25-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="14e25-107">Description</span></span>

<span data-ttu-id="14e25-108">A Microsoft está atualizando a lógica para fontes de interface do usuário para vários idiomas em aplicativos da Windows Store usando HTML.</span><span class="sxs-lookup"><span data-stu-id="14e25-108">Microsoft is updating the logic for UI fonts for several languages in Windows Store apps using HTML.</span></span> <span data-ttu-id="14e25-109">Em vez de usar uma única fonte para todos os idiomas, a fonte da interface do usuário agora será determinada de acordo com a linguagem.</span><span class="sxs-lookup"><span data-stu-id="14e25-109">Rather than using a single font for all languages, the UI font will now be determined on a per language basis.</span></span> <span data-ttu-id="14e25-110">Por exemplo, as fontes de interface do usuário para japonês agora serão a interface do usuário do Meiryo em aplicativos que usam HTML.</span><span class="sxs-lookup"><span data-stu-id="14e25-110">For example, UI fonts for Japanese will now be Meiryo UI in apps that use HTML.</span></span>

## <a name="manifestation"></a><span data-ttu-id="14e25-111">Manifestação</span><span class="sxs-lookup"><span data-stu-id="14e25-111">Manifestation</span></span>

<span data-ttu-id="14e25-112">Os aplicativos que dependem de uma fonte antiga podem parecer diferentes; Embora a aparência do seu aplicativo seja aprimorada em geral graças a fontes mais legíveis, pode haver um problema com layouts que dependem de tamanhos de conteúdo de pixel perfeito.</span><span class="sxs-lookup"><span data-stu-id="14e25-112">Apps that depended on an old font may look different; while your app appearance will be improved overall thanks to more readable fonts, there could be an issue with layouts that depend on pixel-perfect content sizes.</span></span> <span data-ttu-id="14e25-113">Por exemplo, algumas linhas de conteúdo podem ser maiores do que antes, causando quebras de linha inesperadas e/ou redimensionamento de elementos de contêiner.</span><span class="sxs-lookup"><span data-stu-id="14e25-113">For example, some lines of content may be bigger than they were previously, causing unexpected line breaks and/or resizing of container elements.</span></span> <span data-ttu-id="14e25-114">No entanto, na prática, não notamos nenhum problema com nenhum aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="14e25-114">However, in practice we haven’t noticed any issues with any existing apps.</span></span>

## <a name="solution"></a><span data-ttu-id="14e25-115">Solução</span><span class="sxs-lookup"><span data-stu-id="14e25-115">Solution</span></span>

<span data-ttu-id="14e25-116">Os aplicativos afetados podem mitigar esse comportamento especificando uma determinada fonte por meio de CSS (por exemplo, "font-family: interface do usuário Meiryo") em vez de depender das fontes padrão antigas.</span><span class="sxs-lookup"><span data-stu-id="14e25-116">Affected apps can mitigate this behavior by specifying a given font via CSS (for example, “font-family: Meiryo UI”) instead of relying on the old default fonts.</span></span> <span data-ttu-id="14e25-117">A tabela a seguir fornece a fonte da interface do usuário para cada um dos nomes de script.</span><span class="sxs-lookup"><span data-stu-id="14e25-117">The following table provides the UI font for each of the script names.</span></span>



| <span data-ttu-id="14e25-118">Nome do script</span><span class="sxs-lookup"><span data-stu-id="14e25-118">Script Name</span></span>        | <span data-ttu-id="14e25-119">Fonte da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="14e25-119">UI Font</span></span>               |
|--------------------|-----------------------|
| <span data-ttu-id="14e25-120">Árabe</span><span class="sxs-lookup"><span data-stu-id="14e25-120">Arabic</span></span>             | <span data-ttu-id="14e25-121">Interface do Usuário Segoe</span><span class="sxs-lookup"><span data-stu-id="14e25-121">Segoe UI</span></span>              |
| <span data-ttu-id="14e25-122">Armênia</span><span class="sxs-lookup"><span data-stu-id="14e25-122">Armenian</span></span>           | <span data-ttu-id="14e25-123">Interface do Usuário Segoe</span><span class="sxs-lookup"><span data-stu-id="14e25-123">Segoe UI</span></span>              |
| <span data-ttu-id="14e25-124">Bengali</span><span class="sxs-lookup"><span data-stu-id="14e25-124">Bengali</span></span>            | <span data-ttu-id="14e25-125">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="14e25-125">Nirmala UI</span></span>            |
| <span data-ttu-id="14e25-126">Bopomofo</span><span class="sxs-lookup"><span data-stu-id="14e25-126">Bopomofo</span></span>           | <span data-ttu-id="14e25-127">Microsoft JhengHei UI</span><span class="sxs-lookup"><span data-stu-id="14e25-127">Microsoft JhengHei UI</span></span> |
| <span data-ttu-id="14e25-128">Braille</span><span class="sxs-lookup"><span data-stu-id="14e25-128">Braille</span></span>            | <span data-ttu-id="14e25-129">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="14e25-129">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="14e25-130">Bugi</span><span class="sxs-lookup"><span data-stu-id="14e25-130">Buginese</span></span>           | <span data-ttu-id="14e25-131">Leelawadee UI</span><span class="sxs-lookup"><span data-stu-id="14e25-131">Leelawadee UI</span></span>         |
| <span data-ttu-id="14e25-132">Silábico canadense</span><span class="sxs-lookup"><span data-stu-id="14e25-132">Canadian Syllabics</span></span> | <span data-ttu-id="14e25-133">Gadugi</span><span class="sxs-lookup"><span data-stu-id="14e25-133">Gadugi</span></span>                |
| <span data-ttu-id="14e25-134">Cherokee</span><span class="sxs-lookup"><span data-stu-id="14e25-134">Cherokee</span></span>           | <span data-ttu-id="14e25-135">Gadugi</span><span class="sxs-lookup"><span data-stu-id="14e25-135">Gadugi</span></span>                |
| <span data-ttu-id="14e25-136">Copta</span><span class="sxs-lookup"><span data-stu-id="14e25-136">Coptic</span></span>             | <span data-ttu-id="14e25-137">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="14e25-137">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="14e25-138">Han (simplificado)</span><span class="sxs-lookup"><span data-stu-id="14e25-138">Han (Simplified)</span></span>   | <span data-ttu-id="14e25-139">Microsoft YaHei UI</span><span class="sxs-lookup"><span data-stu-id="14e25-139">Microsoft YaHei UI</span></span>    |
| <span data-ttu-id="14e25-140">Han (tradicional)</span><span class="sxs-lookup"><span data-stu-id="14e25-140">Han (Traditional)</span></span>  | <span data-ttu-id="14e25-141">Microsoft JhengHei UI</span><span class="sxs-lookup"><span data-stu-id="14e25-141">Microsoft JhengHei UI</span></span> |
| <span data-ttu-id="14e25-142">Cirílico</span><span class="sxs-lookup"><span data-stu-id="14e25-142">Cyrillic</span></span>           | <span data-ttu-id="14e25-143">Interface do Usuário Segoe</span><span class="sxs-lookup"><span data-stu-id="14e25-143">Segoe UI</span></span>              |
| <span data-ttu-id="14e25-144">Devanagari</span><span class="sxs-lookup"><span data-stu-id="14e25-144">Devanagari</span></span>         | <span data-ttu-id="14e25-145">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="14e25-145">Nirmala UI</span></span>            |
| <span data-ttu-id="14e25-146">Deseret</span><span class="sxs-lookup"><span data-stu-id="14e25-146">Deseret</span></span>            | <span data-ttu-id="14e25-147">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="14e25-147">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="14e25-148">Etíope</span><span class="sxs-lookup"><span data-stu-id="14e25-148">Ethiopic</span></span>           | <span data-ttu-id="14e25-149">Ebrima</span><span class="sxs-lookup"><span data-stu-id="14e25-149">Ebrima</span></span>                |
| <span data-ttu-id="14e25-150">Georgiano</span><span class="sxs-lookup"><span data-stu-id="14e25-150">Georgian</span></span>           | <span data-ttu-id="14e25-151">Interface do Usuário Segoe</span><span class="sxs-lookup"><span data-stu-id="14e25-151">Segoe UI</span></span>              |
| <span data-ttu-id="14e25-152">Letra</span><span class="sxs-lookup"><span data-stu-id="14e25-152">Glagolitic</span></span>         | <span data-ttu-id="14e25-153">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="14e25-153">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="14e25-154">Gothic</span><span class="sxs-lookup"><span data-stu-id="14e25-154">Gothic</span></span>             | <span data-ttu-id="14e25-155">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="14e25-155">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="14e25-156">Grego</span><span class="sxs-lookup"><span data-stu-id="14e25-156">Greek</span></span>              | <span data-ttu-id="14e25-157">Interface do Usuário Segoe</span><span class="sxs-lookup"><span data-stu-id="14e25-157">Segoe UI</span></span>              |
| <span data-ttu-id="14e25-158">Guzerate</span><span class="sxs-lookup"><span data-stu-id="14e25-158">Gujarati</span></span>           | <span data-ttu-id="14e25-159">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="14e25-159">Nirmala UI</span></span>            |
| <span data-ttu-id="14e25-160">Gurmukhi</span><span class="sxs-lookup"><span data-stu-id="14e25-160">Gurmukhi</span></span>           | <span data-ttu-id="14e25-161">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="14e25-161">Nirmala UI</span></span>            |
| <span data-ttu-id="14e25-162">Hebraico</span><span class="sxs-lookup"><span data-stu-id="14e25-162">Hebrew</span></span>             | <span data-ttu-id="14e25-163">Interface do Usuário Segoe</span><span class="sxs-lookup"><span data-stu-id="14e25-163">Segoe UI</span></span>              |
| <span data-ttu-id="14e25-164">Itálico antigo</span><span class="sxs-lookup"><span data-stu-id="14e25-164">Old Italic</span></span>         | <span data-ttu-id="14e25-165">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="14e25-165">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="14e25-166">Javanês</span><span class="sxs-lookup"><span data-stu-id="14e25-166">Javanese</span></span>           | <span data-ttu-id="14e25-167">Texto do javanês</span><span class="sxs-lookup"><span data-stu-id="14e25-167">Javanese Text</span></span>         |
| <span data-ttu-id="14e25-168">Japonês</span><span class="sxs-lookup"><span data-stu-id="14e25-168">Japanese</span></span>           | <span data-ttu-id="14e25-169">Interface do usuário do amMeiryo</span><span class="sxs-lookup"><span data-stu-id="14e25-169">Meiryo UI</span></span>             |
| <span data-ttu-id="14e25-170">canarim</span><span class="sxs-lookup"><span data-stu-id="14e25-170">Kannada</span></span>            | <span data-ttu-id="14e25-171">Interface do usuário do amMirmala</span><span class="sxs-lookup"><span data-stu-id="14e25-171">Mirmala UI</span></span>            |
| <span data-ttu-id="14e25-172">Khmer</span><span class="sxs-lookup"><span data-stu-id="14e25-172">Khmer</span></span>              | <span data-ttu-id="14e25-173">Leelawadee UI</span><span class="sxs-lookup"><span data-stu-id="14e25-173">Leelawadee UI</span></span>         |
| <span data-ttu-id="14e25-174">Coreano</span><span class="sxs-lookup"><span data-stu-id="14e25-174">Korean</span></span>             | <span data-ttu-id="14e25-175">Malgun Gothic</span><span class="sxs-lookup"><span data-stu-id="14e25-175">Malgun Gothic</span></span>         |
| <span data-ttu-id="14e25-176">Lao</span><span class="sxs-lookup"><span data-stu-id="14e25-176">Lao</span></span>                | <span data-ttu-id="14e25-177">Leelawadee</span><span class="sxs-lookup"><span data-stu-id="14e25-177">Leelawadee</span></span>            |
| <span data-ttu-id="14e25-178">Latim</span><span class="sxs-lookup"><span data-stu-id="14e25-178">Latin</span></span>              | <span data-ttu-id="14e25-179">Interface do Usuário Segoe</span><span class="sxs-lookup"><span data-stu-id="14e25-179">Segoe UI</span></span>              |
| <span data-ttu-id="14e25-180">Malaiala</span><span class="sxs-lookup"><span data-stu-id="14e25-180">Malayalam</span></span>          | <span data-ttu-id="14e25-181">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="14e25-181">Nirmala UI</span></span>            |
| <span data-ttu-id="14e25-182">Mongol</span><span class="sxs-lookup"><span data-stu-id="14e25-182">Mongolian</span></span>          | <span data-ttu-id="14e25-183">Mongolian Baiti</span><span class="sxs-lookup"><span data-stu-id="14e25-183">Mongolian Baiti</span></span>       |
| <span data-ttu-id="14e25-184">Myanmar</span><span class="sxs-lookup"><span data-stu-id="14e25-184">Myanmar</span></span>            | <span data-ttu-id="14e25-185">Myanmar Text</span><span class="sxs-lookup"><span data-stu-id="14e25-185">Myanmar Text</span></span>          |
| <span data-ttu-id="14e25-186">N' Ko</span><span class="sxs-lookup"><span data-stu-id="14e25-186">N'Ko</span></span>               | <span data-ttu-id="14e25-187">Ebrima</span><span class="sxs-lookup"><span data-stu-id="14e25-187">Ebrima</span></span>                |
| <span data-ttu-id="14e25-188">Ogham</span><span class="sxs-lookup"><span data-stu-id="14e25-188">Ogham</span></span>              | <span data-ttu-id="14e25-189">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="14e25-189">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="14e25-190">Ol Chiki</span><span class="sxs-lookup"><span data-stu-id="14e25-190">Ol Chiki</span></span>           | <span data-ttu-id="14e25-191">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="14e25-191">Nirmala UI</span></span>            |
| <span data-ttu-id="14e25-192">Turco antigo</span><span class="sxs-lookup"><span data-stu-id="14e25-192">Old Turkic</span></span>         | <span data-ttu-id="14e25-193">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="14e25-193">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="14e25-194">Oriya</span><span class="sxs-lookup"><span data-stu-id="14e25-194">Oriya</span></span>              | <span data-ttu-id="14e25-195">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="14e25-195">Nirmala UI</span></span>            |
| <span data-ttu-id="14e25-196">Osmanya</span><span class="sxs-lookup"><span data-stu-id="14e25-196">Osmanya</span></span>            | <span data-ttu-id="14e25-197">Ebrima</span><span class="sxs-lookup"><span data-stu-id="14e25-197">Ebrima</span></span>                |
| <span data-ttu-id="14e25-198">Phags-Pa</span><span class="sxs-lookup"><span data-stu-id="14e25-198">Phags-pa</span></span>           | <span data-ttu-id="14e25-199">Microsoft PhagsPa</span><span class="sxs-lookup"><span data-stu-id="14e25-199">Microsoft PhagsPa</span></span>     |
| <span data-ttu-id="14e25-200">Rúnica</span><span class="sxs-lookup"><span data-stu-id="14e25-200">Runic</span></span>              | <span data-ttu-id="14e25-201">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="14e25-201">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="14e25-202">Sora Sompeng</span><span class="sxs-lookup"><span data-stu-id="14e25-202">Sora Sompeng</span></span>       | <span data-ttu-id="14e25-203">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="14e25-203">Nirmala UI</span></span>            |
| <span data-ttu-id="14e25-204">Sinhala</span><span class="sxs-lookup"><span data-stu-id="14e25-204">Sinhala</span></span>            | <span data-ttu-id="14e25-205">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="14e25-205">Nirmala UI</span></span>            |
| <span data-ttu-id="14e25-206">Siríaco</span><span class="sxs-lookup"><span data-stu-id="14e25-206">Syriac</span></span>             | <span data-ttu-id="14e25-207">Estrangelo Edessa</span><span class="sxs-lookup"><span data-stu-id="14e25-207">Estrangelo Edessa</span></span>     |
| <span data-ttu-id="14e25-208">Tai Le</span><span class="sxs-lookup"><span data-stu-id="14e25-208">Tai Le</span></span>             | <span data-ttu-id="14e25-209">Microsoft Tai Le</span><span class="sxs-lookup"><span data-stu-id="14e25-209">Microsoft Tai Le</span></span>      |
| <span data-ttu-id="14e25-210">Tai Lue Novo</span><span class="sxs-lookup"><span data-stu-id="14e25-210">New Tai Lue</span></span>        | <span data-ttu-id="14e25-211">Microsoft New Tai Lue</span><span class="sxs-lookup"><span data-stu-id="14e25-211">Microsoft New Tai Lue</span></span> |
| <span data-ttu-id="14e25-212">Tâmil</span><span class="sxs-lookup"><span data-stu-id="14e25-212">Tamil</span></span>              | <span data-ttu-id="14e25-213">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="14e25-213">Nirmala UI</span></span>            |
| <span data-ttu-id="14e25-214">Télugo</span><span class="sxs-lookup"><span data-stu-id="14e25-214">Telugu</span></span>             | <span data-ttu-id="14e25-215">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="14e25-215">Nirmala UI</span></span>            |
| <span data-ttu-id="14e25-216">Tifinagh</span><span class="sxs-lookup"><span data-stu-id="14e25-216">Tifinagh</span></span>           | <span data-ttu-id="14e25-217">Ebrima</span><span class="sxs-lookup"><span data-stu-id="14e25-217">Ebrima</span></span>                |
| <span data-ttu-id="14e25-218">Thaana</span><span class="sxs-lookup"><span data-stu-id="14e25-218">Thaana</span></span>             | <span data-ttu-id="14e25-219">MV Boli</span><span class="sxs-lookup"><span data-stu-id="14e25-219">MV Boli</span></span>               |
| <span data-ttu-id="14e25-220">Tailandês</span><span class="sxs-lookup"><span data-stu-id="14e25-220">Thai</span></span>               | <span data-ttu-id="14e25-221">Leelawadee UI</span><span class="sxs-lookup"><span data-stu-id="14e25-221">Leelawadee UI</span></span>         |
| <span data-ttu-id="14e25-222">Tibetano</span><span class="sxs-lookup"><span data-stu-id="14e25-222">Tibetan</span></span>            | <span data-ttu-id="14e25-223">Microsoft Himalaya</span><span class="sxs-lookup"><span data-stu-id="14e25-223">Microsoft Himalaya</span></span>    |
| <span data-ttu-id="14e25-224">Vai</span><span class="sxs-lookup"><span data-stu-id="14e25-224">Vai</span></span>                | <span data-ttu-id="14e25-225">Ebrima</span><span class="sxs-lookup"><span data-stu-id="14e25-225">Ebrima</span></span>                |
| <span data-ttu-id="14e25-226">Yi</span><span class="sxs-lookup"><span data-stu-id="14e25-226">Yi</span></span>                 | <span data-ttu-id="14e25-227">Microsoft Yi Baiti</span><span class="sxs-lookup"><span data-stu-id="14e25-227">Microsoft Yi Baiti</span></span>    |



 

 

 




