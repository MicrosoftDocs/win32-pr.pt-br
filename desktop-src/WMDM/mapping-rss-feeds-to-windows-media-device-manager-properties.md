---
title: Mapeando RSS feeds para propriedades do Windows Media Gerenciador de Dispositivos
description: Mapeando RSS feeds para propriedades do Windows Media Gerenciador de Dispositivos
ms.assetid: 354c98ab-1392-476f-a650-75b948dc971a
keywords:
- Windows Media Gerenciador de Dispositivos, RSS feeds
- Gerenciador de Dispositivos, RSS feeds
- Guia de programação, RSS feeds
- aplicativos de desktop, RSS feeds
- Criando aplicativos de Gerenciador de Dispositivos de mídia do Windows, RSS feeds
- RSS feeds
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a81d52b4099d77542963d2e87ae5b7dc26b034
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822346"
---
# <a name="mapping-rss-feeds-to-windows-media-device-manager-properties"></a><span data-ttu-id="38dec-109">Mapeando RSS feeds para propriedades do Windows Media Gerenciador de Dispositivos</span><span class="sxs-lookup"><span data-stu-id="38dec-109">Mapping RSS Feeds to Windows Media Device Manager Properties</span></span>

<span data-ttu-id="38dec-110">O Windows Media Player 11 fornece um recurso de agregador RSS que permite que os usuários armazenem conteúdo obtido de podcasts em seus computadores.</span><span class="sxs-lookup"><span data-stu-id="38dec-110">Windows Media Player 11 provides an RSS aggregator feature that enables users to store content obtained from podcasts on their computers.</span></span> <span data-ttu-id="38dec-111">Este tópico descreve os elementos XML encontrados em um RSS feed.</span><span class="sxs-lookup"><span data-stu-id="38dec-111">This topic describes the XML elements found in an RSS feed.</span></span> <span data-ttu-id="38dec-112">Além disso, ele mapeia esses elementos RSS para as propriedades do Windows Media Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="38dec-112">In addition, it maps these RSS elements to Windows Media Device Manager properties.</span></span>

<span data-ttu-id="38dec-113">Os elementos em um RSS feed têm a seguinte hierarquia e atributos:</span><span class="sxs-lookup"><span data-stu-id="38dec-113">The elements in an RSS feed have the following hierarchy and attributes:</span></span>


```C++
<channel>
    <title />
    <link />
    <description />
    <language />
    <copyright />
    <managingEditor />
    <webMaster />
    <pubDate />
    <lastBuildDate />
    <category />
    <generator />
    <docs />
    <cloud />
    <ttl />

    <image>
        <url />
        <title />
        <link />
        <width />
        <height />
        <description />
    </image>

    <rating />

    <textInput>
        <title />
        <description />
        <name />
        <link />
    </textInput>

    <skipHours />
    <skipDays />

    <item>
        <title />
        <link />
        <description />
        <author />
        <category domain = " "/>
        <comments />
        <enclousure url = " " length = " " type = " "/>
        <guid isPermaLink = " "/>
        <pubDate />
        <source url = " " />
    </item>
</channel>
```



<span data-ttu-id="38dec-114">A tabela a seguir lista os elementos de canal em um RSS feed e as propriedades correspondentes do Windows Media Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="38dec-114">The following table lists the channel elements in an RSS feed and the corresponding Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="38dec-115">Elemento Channel</span><span class="sxs-lookup"><span data-stu-id="38dec-115">Channel element</span></span> | <span data-ttu-id="38dec-116">Status</span><span class="sxs-lookup"><span data-stu-id="38dec-116">Status</span></span>         | <span data-ttu-id="38dec-117">Propriedade Gerenciador de Dispositivos de mídia do Windows correspondente</span><span class="sxs-lookup"><span data-stu-id="38dec-117">Corresponding Windows Media Device Manager property</span></span>   |
|-----------------|----------------|-------------------------------------------------------|
| <span data-ttu-id="38dec-118">category</span><span class="sxs-lookup"><span data-stu-id="38dec-118">category</span></span>        | <span data-ttu-id="38dec-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="38dec-119">Optional</span></span>       | [<span data-ttu-id="38dec-120">g \_ wszWMDMGenre</span><span class="sxs-lookup"><span data-stu-id="38dec-120">g\_wszWMDMGenre</span></span>](metadata-constants.md)             |
| <span data-ttu-id="38dec-121">nuvem</span><span class="sxs-lookup"><span data-stu-id="38dec-121">cloud</span></span>           | <span data-ttu-id="38dec-122">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="38dec-122">Not applicable</span></span> | <span data-ttu-id="38dec-123">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="38dec-123">Not applicable</span></span>                                        |
| <span data-ttu-id="38dec-124">direitos autorais</span><span class="sxs-lookup"><span data-stu-id="38dec-124">copyright</span></span>       | <span data-ttu-id="38dec-125">Opcional</span><span class="sxs-lookup"><span data-stu-id="38dec-125">Optional</span></span>       | [<span data-ttu-id="38dec-126">g \_ wszWMDMProviderCopyright</span><span class="sxs-lookup"><span data-stu-id="38dec-126">g\_wszWMDMProviderCopyright</span></span>](metadata-constants.md) |
| <span data-ttu-id="38dec-127">descrição</span><span class="sxs-lookup"><span data-stu-id="38dec-127">description</span></span>     | <span data-ttu-id="38dec-128">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="38dec-128">Required</span></span>       | [<span data-ttu-id="38dec-129">g \_ wszWMDMDescription</span><span class="sxs-lookup"><span data-stu-id="38dec-129">g\_wszWMDMDescription</span></span>](metadata-constants.md)       |
| <span data-ttu-id="38dec-130">docs</span><span class="sxs-lookup"><span data-stu-id="38dec-130">docs</span></span>            | <span data-ttu-id="38dec-131">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="38dec-131">Not applicable</span></span> | <span data-ttu-id="38dec-132">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="38dec-132">Not applicable</span></span>                                        |
| <span data-ttu-id="38dec-133">gerador</span><span class="sxs-lookup"><span data-stu-id="38dec-133">generator</span></span>       | <span data-ttu-id="38dec-134">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="38dec-134">Not applicable</span></span> | <span data-ttu-id="38dec-135">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="38dec-135">Not applicable</span></span>                                        |
| <span data-ttu-id="38dec-136">Linguagem</span><span class="sxs-lookup"><span data-stu-id="38dec-136">language</span></span>        | <span data-ttu-id="38dec-137">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="38dec-137">Not applicable</span></span> | <span data-ttu-id="38dec-138">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="38dec-138">Not applicable</span></span>                                        |
| <span data-ttu-id="38dec-139">lastBuildDate</span><span class="sxs-lookup"><span data-stu-id="38dec-139">lastBuildDate</span></span>   | <span data-ttu-id="38dec-140">Opcional</span><span class="sxs-lookup"><span data-stu-id="38dec-140">Optional</span></span>       | [<span data-ttu-id="38dec-141">g \_ wszWMDMLastModifiedDate</span><span class="sxs-lookup"><span data-stu-id="38dec-141">g\_wszWMDMLastModifiedDate</span></span>](metadata-constants.md)  |
| <span data-ttu-id="38dec-142">link</span><span class="sxs-lookup"><span data-stu-id="38dec-142">link</span></span>            | <span data-ttu-id="38dec-143">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="38dec-143">Required</span></span>       | [<span data-ttu-id="38dec-144">g \_ wszWMDMDestinationURL</span><span class="sxs-lookup"><span data-stu-id="38dec-144">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)    |
| <span data-ttu-id="38dec-145">managingEditor</span><span class="sxs-lookup"><span data-stu-id="38dec-145">managingEditor</span></span>  | <span data-ttu-id="38dec-146">Opcional</span><span class="sxs-lookup"><span data-stu-id="38dec-146">Optional</span></span>       | [<span data-ttu-id="38dec-147">g \_ wszWMDMEditor</span><span class="sxs-lookup"><span data-stu-id="38dec-147">g\_wszWMDMEditor</span></span>](metadata-constants.md)            |
| <span data-ttu-id="38dec-148">pubDate</span><span class="sxs-lookup"><span data-stu-id="38dec-148">pubDate</span></span>         | <span data-ttu-id="38dec-149">Opcional</span><span class="sxs-lookup"><span data-stu-id="38dec-149">Optional</span></span>       | [<span data-ttu-id="38dec-150">g \_ wszWMDMYear</span><span class="sxs-lookup"><span data-stu-id="38dec-150">g\_wszWMDMYear</span></span>](metadata-constants.md)              |
| <span data-ttu-id="38dec-151">classificação</span><span class="sxs-lookup"><span data-stu-id="38dec-151">rating</span></span>          | <span data-ttu-id="38dec-152">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="38dec-152">Not applicable</span></span> | <span data-ttu-id="38dec-153">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="38dec-153">Not applicable</span></span>                                        |
| <span data-ttu-id="38dec-154">skipDays</span><span class="sxs-lookup"><span data-stu-id="38dec-154">skipDays</span></span>        | <span data-ttu-id="38dec-155">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="38dec-155">Not applicable</span></span> | <span data-ttu-id="38dec-156">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="38dec-156">Not applicable</span></span>                                        |
| <span data-ttu-id="38dec-157">skipHours</span><span class="sxs-lookup"><span data-stu-id="38dec-157">skipHours</span></span>       | <span data-ttu-id="38dec-158">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="38dec-158">Not applicable</span></span> | <span data-ttu-id="38dec-159">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="38dec-159">Not applicable</span></span>                                        |
| <span data-ttu-id="38dec-160">textInput</span><span class="sxs-lookup"><span data-stu-id="38dec-160">textInput</span></span>       | <span data-ttu-id="38dec-161">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="38dec-161">Not applicable</span></span> | <span data-ttu-id="38dec-162">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="38dec-162">Not applicable</span></span>                                        |
| <span data-ttu-id="38dec-163">título</span><span class="sxs-lookup"><span data-stu-id="38dec-163">title</span></span>           | <span data-ttu-id="38dec-164">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="38dec-164">Required</span></span>       | [<span data-ttu-id="38dec-165">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="38dec-165">g\_wszWMDMTitle</span></span>](metadata-constants.md)             |
| <span data-ttu-id="38dec-166">ttl</span><span class="sxs-lookup"><span data-stu-id="38dec-166">ttl</span></span>             | <span data-ttu-id="38dec-167">Opcional</span><span class="sxs-lookup"><span data-stu-id="38dec-167">Optional</span></span>       | [<span data-ttu-id="38dec-168">g \_ wszWMDMTimeToLive</span><span class="sxs-lookup"><span data-stu-id="38dec-168">g\_wszWMDMTimeToLive</span></span>](metadata-constants.md)        |
| <span data-ttu-id="38dec-169">webMaster</span><span class="sxs-lookup"><span data-stu-id="38dec-169">webMaster</span></span>       | <span data-ttu-id="38dec-170">Opcional</span><span class="sxs-lookup"><span data-stu-id="38dec-170">Optional</span></span>       | [<span data-ttu-id="38dec-171">g \_ wszWMDMWebMaster</span><span class="sxs-lookup"><span data-stu-id="38dec-171">g\_wszWMDMWebMaster</span></span>](metadata-constants.md)         |



 

<span data-ttu-id="38dec-172">A tabela a seguir lista os elementos de imagem em um RSS feed e as propriedades WMDM correspondentes.</span><span class="sxs-lookup"><span data-stu-id="38dec-172">The following table lists the image elements in an RSS feed and the corresponding WMDM properties.</span></span>



| <span data-ttu-id="38dec-173">Elemento Image</span><span class="sxs-lookup"><span data-stu-id="38dec-173">Image element</span></span> | <span data-ttu-id="38dec-174">Status</span><span class="sxs-lookup"><span data-stu-id="38dec-174">Status</span></span>   | <span data-ttu-id="38dec-175">Propriedade Gerenciador de Dispositivos de mídia do Windows correspondente</span><span class="sxs-lookup"><span data-stu-id="38dec-175">Corresponding Windows Media Device Manager property</span></span> |
|---------------|----------|-----------------------------------------------------|
| <span data-ttu-id="38dec-176">descrição</span><span class="sxs-lookup"><span data-stu-id="38dec-176">description</span></span>   | <span data-ttu-id="38dec-177">Opcional</span><span class="sxs-lookup"><span data-stu-id="38dec-177">Optional</span></span> | [<span data-ttu-id="38dec-178">g \_ wszWMDMDescription</span><span class="sxs-lookup"><span data-stu-id="38dec-178">g\_wszWMDMDescription</span></span>](metadata-constants.md)     |
| <span data-ttu-id="38dec-179">altura</span><span class="sxs-lookup"><span data-stu-id="38dec-179">height</span></span>        | <span data-ttu-id="38dec-180">Opcional</span><span class="sxs-lookup"><span data-stu-id="38dec-180">Optional</span></span> | [<span data-ttu-id="38dec-181">g \_ wszWMDMHeight</span><span class="sxs-lookup"><span data-stu-id="38dec-181">g\_wszWMDMHeight</span></span>](metadata-constants.md)          |
| <span data-ttu-id="38dec-182">link</span><span class="sxs-lookup"><span data-stu-id="38dec-182">link</span></span>          | <span data-ttu-id="38dec-183">Opcional</span><span class="sxs-lookup"><span data-stu-id="38dec-183">Optional</span></span> | [<span data-ttu-id="38dec-184">g \_ wszWMDMDestinationURL</span><span class="sxs-lookup"><span data-stu-id="38dec-184">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)  |
| <span data-ttu-id="38dec-185">título</span><span class="sxs-lookup"><span data-stu-id="38dec-185">title</span></span>         | <span data-ttu-id="38dec-186">Opcional</span><span class="sxs-lookup"><span data-stu-id="38dec-186">Optional</span></span> | [<span data-ttu-id="38dec-187">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="38dec-187">g\_wszWMDMTitle</span></span>](metadata-constants.md)           |
| <span data-ttu-id="38dec-188">url</span><span class="sxs-lookup"><span data-stu-id="38dec-188">url</span></span>           | <span data-ttu-id="38dec-189">Opcional</span><span class="sxs-lookup"><span data-stu-id="38dec-189">Optional</span></span> | [<span data-ttu-id="38dec-190">g \_ wszWMDMSourceURL</span><span class="sxs-lookup"><span data-stu-id="38dec-190">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)       |
| <span data-ttu-id="38dec-191">width</span><span class="sxs-lookup"><span data-stu-id="38dec-191">width</span></span>         | <span data-ttu-id="38dec-192">Opcional</span><span class="sxs-lookup"><span data-stu-id="38dec-192">Optional</span></span> | [<span data-ttu-id="38dec-193">g \_ wszWMDMWidth</span><span class="sxs-lookup"><span data-stu-id="38dec-193">g\_wszWMDMWidth</span></span>](metadata-constants.md)           |



 

<span data-ttu-id="38dec-194">A tabela a seguir lista os elementos de item em um RSS feed e as propriedades correspondentes do Windows Media Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="38dec-194">The following table lists the item elements in an RSS feed and the corresponding Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="38dec-195">Elemento Item</span><span class="sxs-lookup"><span data-stu-id="38dec-195">Item element</span></span> | <span data-ttu-id="38dec-196">Atributo</span><span class="sxs-lookup"><span data-stu-id="38dec-196">Attribute</span></span>   | <span data-ttu-id="38dec-197">Status</span><span class="sxs-lookup"><span data-stu-id="38dec-197">Status</span></span>         | <span data-ttu-id="38dec-198">Propriedade Gerenciador de Dispositivos de mídia do Windows correspondente</span><span class="sxs-lookup"><span data-stu-id="38dec-198">Corresponding Windows Media Device Manager property</span></span>            |
|--------------|-------------|----------------|----------------------------------------------------------------|
| <span data-ttu-id="38dec-199">autor</span><span class="sxs-lookup"><span data-stu-id="38dec-199">author</span></span>       |             | <span data-ttu-id="38dec-200">Opcional</span><span class="sxs-lookup"><span data-stu-id="38dec-200">Optional</span></span>       | [<span data-ttu-id="38dec-201">g \_ wszWMDMAuthor</span><span class="sxs-lookup"><span data-stu-id="38dec-201">g\_wszWMDMAuthor</span></span>](metadata-constants.md)                     |
| <span data-ttu-id="38dec-202">category</span><span class="sxs-lookup"><span data-stu-id="38dec-202">category</span></span>     |             | <span data-ttu-id="38dec-203">Opcional</span><span class="sxs-lookup"><span data-stu-id="38dec-203">Optional</span></span>       | [<span data-ttu-id="38dec-204">g \_ wszWMDMGenre</span><span class="sxs-lookup"><span data-stu-id="38dec-204">g\_wszWMDMGenre</span></span>](metadata-constants.md)                      |
|              | <span data-ttu-id="38dec-205">domínio</span><span class="sxs-lookup"><span data-stu-id="38dec-205">domain</span></span>      | <span data-ttu-id="38dec-206">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="38dec-206">Not applicable</span></span> | <span data-ttu-id="38dec-207">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="38dec-207">Not applicable</span></span>                                                 |
| <span data-ttu-id="38dec-208">descrição</span><span class="sxs-lookup"><span data-stu-id="38dec-208">description</span></span>  |             | <span data-ttu-id="38dec-209">Opcional</span><span class="sxs-lookup"><span data-stu-id="38dec-209">Optional</span></span>       | [<span data-ttu-id="38dec-210">g \_ wszWMDMDescription</span><span class="sxs-lookup"><span data-stu-id="38dec-210">g\_wszWMDMDescription</span></span>](metadata-constants.md)                |
| <span data-ttu-id="38dec-211">SPE</span><span class="sxs-lookup"><span data-stu-id="38dec-211">enclosure</span></span>    |             | <span data-ttu-id="38dec-212">Opcional</span><span class="sxs-lookup"><span data-stu-id="38dec-212">Optional</span></span>       | <span data-ttu-id="38dec-213">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="38dec-213">Not applicable</span></span>                                                 |
|              | <span data-ttu-id="38dec-214">comprimento</span><span class="sxs-lookup"><span data-stu-id="38dec-214">length</span></span>      | <span data-ttu-id="38dec-215">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="38dec-215">Required</span></span>       | [<span data-ttu-id="38dec-216">g \_ wszWMDMFileSize</span><span class="sxs-lookup"><span data-stu-id="38dec-216">g\_wszWMDMFileSize</span></span>](metadata-constants.md)                   |
|              | <span data-ttu-id="38dec-217">type</span><span class="sxs-lookup"><span data-stu-id="38dec-217">type</span></span>        | <span data-ttu-id="38dec-218">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="38dec-218">Required</span></span>       | <span data-ttu-id="38dec-219">(O tipo MIME deve ser mapeado para o tipo de conteúdo da propriedade.)</span><span class="sxs-lookup"><span data-stu-id="38dec-219">(The MIME type should be mapped to the property content type.)</span></span> |
|              | <span data-ttu-id="38dec-220">url</span><span class="sxs-lookup"><span data-stu-id="38dec-220">url</span></span>         | <span data-ttu-id="38dec-221">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="38dec-221">Required</span></span>       | [<span data-ttu-id="38dec-222">g \_ wszWMDMSourceURL</span><span class="sxs-lookup"><span data-stu-id="38dec-222">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)                  |
| <span data-ttu-id="38dec-223">guid</span><span class="sxs-lookup"><span data-stu-id="38dec-223">guid</span></span>         |             | <span data-ttu-id="38dec-224">Opcional</span><span class="sxs-lookup"><span data-stu-id="38dec-224">Optional</span></span>       | [<span data-ttu-id="38dec-225">g \_ wszWMDMediaGuid</span><span class="sxs-lookup"><span data-stu-id="38dec-225">g\_wszWMDMediaGuid</span></span>](metadata-constants.md)                   |
|              | <span data-ttu-id="38dec-226">IsLink permanente</span><span class="sxs-lookup"><span data-stu-id="38dec-226">isPermaLink</span></span> | <span data-ttu-id="38dec-227">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="38dec-227">Not applicable</span></span> | <span data-ttu-id="38dec-228">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="38dec-228">Not applicable</span></span>                                                 |
| <span data-ttu-id="38dec-229">link</span><span class="sxs-lookup"><span data-stu-id="38dec-229">link</span></span>         |             | <span data-ttu-id="38dec-230">Opcional</span><span class="sxs-lookup"><span data-stu-id="38dec-230">Optional</span></span>       | [<span data-ttu-id="38dec-231">g \_ wszWMDMDestinationURL</span><span class="sxs-lookup"><span data-stu-id="38dec-231">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)             |
| <span data-ttu-id="38dec-232">pubDate</span><span class="sxs-lookup"><span data-stu-id="38dec-232">pubDate</span></span>      |             | <span data-ttu-id="38dec-233">Opcional</span><span class="sxs-lookup"><span data-stu-id="38dec-233">Optional</span></span>       | [<span data-ttu-id="38dec-234">g \_ wszWMDMYear</span><span class="sxs-lookup"><span data-stu-id="38dec-234">g\_wszWMDMYear</span></span>](metadata-constants.md)                       |
| <span data-ttu-id="38dec-235">source</span><span class="sxs-lookup"><span data-stu-id="38dec-235">source</span></span>       |             | <span data-ttu-id="38dec-236">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="38dec-236">Not applicable</span></span> | <span data-ttu-id="38dec-237">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="38dec-237">Not applicable</span></span>                                                 |
| <span data-ttu-id="38dec-238">título</span><span class="sxs-lookup"><span data-stu-id="38dec-238">title</span></span>        |             | <span data-ttu-id="38dec-239">Opcional</span><span class="sxs-lookup"><span data-stu-id="38dec-239">Optional</span></span>       | [<span data-ttu-id="38dec-240">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="38dec-240">g\_wszWMDMTitle</span></span>](metadata-constants.md)                      |



 

<span data-ttu-id="38dec-241">Exemplo</span><span class="sxs-lookup"><span data-stu-id="38dec-241">Example</span></span>

<span data-ttu-id="38dec-242">O exemplo a seguir mostra um RSS feed completo para um podcast fictício fornecido pelo CEO de uma empresa de publicação.</span><span class="sxs-lookup"><span data-stu-id="38dec-242">The following example shows a complete RSS feed for a fictitious podcast supplied by the CEO of a publishing company.</span></span>


```C++
<channel>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing.com/podcasting</link>
    <description>Lucerne Publishing CEO Peter Bankov takes a look at the latest trends in online publications.</description>
    <language>en-us</language>
    <copyright>2006 Lucerne Publishing LP, LLLP. All Rights Reserved.</copyright>
    <managingEditor>someone@example.com</managingEditor>
    <webMaster>someone@example.com</webMaster>
    <pubDate>Fri, 9 June 2006 14:00:28 EDT</pubDate>
    <lastBuildDate Fri, 9 June 2006 14:00:28 EDT />
    <category>News</category>
    <generator>Podcaster version 1.0</generator>
    <docs>https://www.lucernepublishing.com/tech/rss</docs>
    <cloud />
    <ttl>240</ttl>
    <rating />
    <textInput />
    <skipHours />
    <skipDays />

<image>
     <url>https://www.lucernepublishing.com/images/logo.gif</url>
     <title>Lucerne Publishing</title>
     <link>https://www.lucernepublishing.com/community/podcasts</link>
     <width>300</width>
     <height>300</height>
     <description>Lucerne Logo</description>
</image>

<item>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</link>
    <description>Online publications are rapidly changing. A publishing house CEO examines the trends of the past five years and their implications.</description>
    <author>Lucerne</author>
    <category>News</category>
    <comments />
    <enclosure url="https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3" length="10329011" type="audio/mpeg" />
    <guid>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</guid>
    <pubDate>Thur, 1 June 2006 14:00:28 EDT</pubDate>
    <source />
</item>

</channel>
```



<span data-ttu-id="38dec-243">Mapeamento de elementos de canal RSS para os valores de Propriedade do Windows Media Gerenciador de Dispositivos</span><span class="sxs-lookup"><span data-stu-id="38dec-243">Mapping of RSS Channel Elements to Windows Media Device Manager Property Values</span></span>

<span data-ttu-id="38dec-244">A tabela a seguir descreve como os valores nos elementos do canal RSS no exemplo anterior são mapeados para as propriedades específicas do Windows Media Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="38dec-244">The following table describes how the values in the RSS Channel elements in the previous example map to particular Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="38dec-245">Propriedade Gerenciador de Dispositivos do Windows Media</span><span class="sxs-lookup"><span data-stu-id="38dec-245">Windows Media Device Manager property</span></span>                    | <span data-ttu-id="38dec-246">Valor</span><span class="sxs-lookup"><span data-stu-id="38dec-246">Value</span></span>                                                                                         |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="38dec-247">g \_ wszWMDMAuthorDate</span><span class="sxs-lookup"><span data-stu-id="38dec-247">g\_wszWMDMAuthorDate</span></span>](metadata-constants.md)           | <span data-ttu-id="38dec-248">Sexta-feira, 9 de junho de 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="38dec-248">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="38dec-249">g \_ wszWMDMDESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="38dec-249">g\_wszWMDMDESCRIPTION</span></span>](metadata-constants.md)          | <span data-ttu-id="38dec-250">A Lucerne Publishing CEO Peter Bankov analisa as tendências mais recentes em publicações online.</span><span class="sxs-lookup"><span data-stu-id="38dec-250">Lucerne Publishing CEO Peter Bankov takes a look at the latest trends in online publications.</span></span> |
| [<span data-ttu-id="38dec-251">\_URL g wszWMDMDESTINATION \_</span><span class="sxs-lookup"><span data-stu-id="38dec-251">g\_wszWMDMDESTINATION\_URL</span></span>](metadata-constants.md)     | https://www.lucernepublishing/services/podcasting                                              |
| [<span data-ttu-id="38dec-252">g \_ wszWMDMEDITOR</span><span class="sxs-lookup"><span data-stu-id="38dec-252">g\_wszWMDMEDITOR</span></span>](metadata-constants.md)               | someone@example.com                                                                           |
| [<span data-ttu-id="38dec-253">g \_ wszWMDMFileCreationDate</span><span class="sxs-lookup"><span data-stu-id="38dec-253">g\_wszWMDMFileCreationDate</span></span>](metadata-constants.md)     | <span data-ttu-id="38dec-254">Sexta-feira, 9 de junho de 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="38dec-254">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="38dec-255">g \_ wszWMDMFileName</span><span class="sxs-lookup"><span data-stu-id="38dec-255">g\_wszWMDMFileName</span></span>](metadata-constants.md)             | <span data-ttu-id="38dec-256">A publicação digital</span><span class="sxs-lookup"><span data-stu-id="38dec-256">The Digital Publication</span></span>                                                                       |
| [<span data-ttu-id="38dec-257">g \_ wszWMDMFileSize</span><span class="sxs-lookup"><span data-stu-id="38dec-257">g\_wszWMDMFileSize</span></span>](metadata-constants.md)             | <span data-ttu-id="38dec-258">13.790</span><span class="sxs-lookup"><span data-stu-id="38dec-258">13,790</span></span>                                                                                        |
| [<span data-ttu-id="38dec-259">g \_ wszWMDMFormatCode</span><span class="sxs-lookup"><span data-stu-id="38dec-259">g\_wszWMDMFormatCode</span></span>](metadata-constants.md)           | <span data-ttu-id="38dec-260">conversão de mídia do WMDM \_ FORMATCODE \_ \_</span><span class="sxs-lookup"><span data-stu-id="38dec-260">WMDM\_FORMATCODE\_MEDIA\_CAST</span></span>                                                                 |
| [<span data-ttu-id="38dec-261">g \_ wszWMDMGENRE</span><span class="sxs-lookup"><span data-stu-id="38dec-261">g\_wszWMDMGENRE</span></span>](metadata-constants.md)                | <span data-ttu-id="38dec-262">Notícias</span><span class="sxs-lookup"><span data-stu-id="38dec-262">News</span></span>                                                                                          |
| [<span data-ttu-id="38dec-263">Data de modificação de g \_ wszWMDMLAST \_ \_</span><span class="sxs-lookup"><span data-stu-id="38dec-263">g\_wszWMDMLAST\_MODIFIED\_DATE</span></span>](metadata-constants.md) | <span data-ttu-id="38dec-264">Sexta-feira, 9 de junho de 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="38dec-264">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="38dec-265">g \_ wszWMDMLastModifiedDate</span><span class="sxs-lookup"><span data-stu-id="38dec-265">g\_wszWMDMLastModifiedDate</span></span>](metadata-constants.md)     | <span data-ttu-id="38dec-266">Sexta-feira, 9 de junho de 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="38dec-266">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="38dec-267">g \_ wszWMDMProviderCopyright</span><span class="sxs-lookup"><span data-stu-id="38dec-267">g\_wszWMDMProviderCopyright</span></span>](metadata-constants.md)    | <span data-ttu-id="38dec-268">2006 Lucerne Publishing LP, LLLP.</span><span class="sxs-lookup"><span data-stu-id="38dec-268">2006 Lucerne Publishing LP, LLLP.</span></span> <span data-ttu-id="38dec-269">Todos os direitos reservados.</span><span class="sxs-lookup"><span data-stu-id="38dec-269">All Rights Reserved.</span></span>                                        |
| [<span data-ttu-id="38dec-270">g \_ wszWMDMTimeToLive</span><span class="sxs-lookup"><span data-stu-id="38dec-270">g\_wszWMDMTimeToLive</span></span>](metadata-constants.md)           | <span data-ttu-id="38dec-271">240</span><span class="sxs-lookup"><span data-stu-id="38dec-271">240</span></span>                                                                                           |
| [<span data-ttu-id="38dec-272">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="38dec-272">g\_wszWMDMTitle</span></span>](metadata-constants.md)                | <span data-ttu-id="38dec-273">A publicação digital</span><span class="sxs-lookup"><span data-stu-id="38dec-273">The Digital Publication</span></span>                                                                       |
| [<span data-ttu-id="38dec-274">g \_ wszWMDMWEBMASTER</span><span class="sxs-lookup"><span data-stu-id="38dec-274">g\_wszWMDMWEBMASTER</span></span>](metadata-constants.md)            | someone@example.com                                                                           |
| [<span data-ttu-id="38dec-275">g \_ wszWMDMYear</span><span class="sxs-lookup"><span data-stu-id="38dec-275">g\_wszWMDMYear</span></span>](metadata-constants.md)                 | <span data-ttu-id="38dec-276">Sexta-feira, 9 de junho de 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="38dec-276">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |



 

<span data-ttu-id="38dec-277">Mapeamento de elementos de imagem RSS para os valores de Propriedade do Windows Media Gerenciador de Dispositivos</span><span class="sxs-lookup"><span data-stu-id="38dec-277">Mapping of RSS Image Elements to Windows Media Device Manager Property Values</span></span>

<span data-ttu-id="38dec-278">A tabela a seguir descreve como os valores nos elementos da imagem RSS no exemplo anterior são mapeados para as propriedades específicas do Windows Media Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="38dec-278">The following table describes how the values in the RSS Image elements in the previous example map to particular Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="38dec-279">Propriedade Gerenciador de Dispositivos do Windows Media</span><span class="sxs-lookup"><span data-stu-id="38dec-279">Windows Media Device Manager property</span></span>                | <span data-ttu-id="38dec-280">Valor</span><span class="sxs-lookup"><span data-stu-id="38dec-280">Value</span></span>                                            |
|------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="38dec-281">g \_ wszWMDMAlbumCoverFormat</span><span class="sxs-lookup"><span data-stu-id="38dec-281">g\_wszWMDMAlbumCoverFormat</span></span>](metadata-constants.md) | <span data-ttu-id="38dec-282">\_GIF de \_ formato de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="38dec-282">WPD\_OBJECT\_FORMAT\_GIF</span></span>                         |
| [<span data-ttu-id="38dec-283">g \_ wszWMDMAlbumCoverSize</span><span class="sxs-lookup"><span data-stu-id="38dec-283">g\_wszWMDMAlbumCoverSize</span></span>](metadata-constants.md)   | <span data-ttu-id="38dec-284">512</span><span class="sxs-lookup"><span data-stu-id="38dec-284">512</span></span>                                              |
| [<span data-ttu-id="38dec-285">g \_ wszWMDMDescription</span><span class="sxs-lookup"><span data-stu-id="38dec-285">g\_wszWMDMDescription</span></span>](metadata-constants.md)      | <span data-ttu-id="38dec-286">Logotipo da Lucerne</span><span class="sxs-lookup"><span data-stu-id="38dec-286">Lucerne Logo</span></span>                                     |
| [<span data-ttu-id="38dec-287">g \_ wszWMDMDestinationURL</span><span class="sxs-lookup"><span data-stu-id="38dec-287">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)   | <span data-ttu-id="38dec-288">www.lucernepublishing.com/community/podcasts</span><span class="sxs-lookup"><span data-stu-id="38dec-288">//www.lucernepublishing.com/community/podcasts</span></span>   |
| [<span data-ttu-id="38dec-289">g \_ wszWMDMHeight</span><span class="sxs-lookup"><span data-stu-id="38dec-289">g\_wszWMDMHeight</span></span>](metadata-constants.md)           | <span data-ttu-id="38dec-290">300</span><span class="sxs-lookup"><span data-stu-id="38dec-290">300</span></span>                                              |
| [<span data-ttu-id="38dec-291">g \_ wszWMDMSourceURL</span><span class="sxs-lookup"><span data-stu-id="38dec-291">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)        | https://www.lucernepublishing.com/images/logo.gif |
| [<span data-ttu-id="38dec-292">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="38dec-292">g\_wszWMDMTitle</span></span>](metadata-constants.md)            | <span data-ttu-id="38dec-293">Publicação na editora</span><span class="sxs-lookup"><span data-stu-id="38dec-293">Lucerne Publishing</span></span>                               |
| [<span data-ttu-id="38dec-294">g \_ wszWMDMWidth</span><span class="sxs-lookup"><span data-stu-id="38dec-294">g\_wszWMDMWidth</span></span>](metadata-constants.md)            | <span data-ttu-id="38dec-295">300</span><span class="sxs-lookup"><span data-stu-id="38dec-295">300</span></span>                                              |



 

<span data-ttu-id="38dec-296">Mapeamento de elementos de item RSS para os valores de Propriedade do Windows Media Gerenciador de Dispositivos</span><span class="sxs-lookup"><span data-stu-id="38dec-296">Mapping of RSS Item Elements to Windows Media Device Manager Property Values</span></span>

<span data-ttu-id="38dec-297">A tabela a seguir descreve como os valores nos elementos de item RSS no exemplo anterior são mapeados para as propriedades específicas do Windows Media Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="38dec-297">The following table describes how the values in the RSS Item elements in the previous example map to particular Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="38dec-298">Propriedade Gerenciador de Dispositivos do Windows Media</span><span class="sxs-lookup"><span data-stu-id="38dec-298">Windows Media Device Manager property</span></span>                | <span data-ttu-id="38dec-299">Valor</span><span class="sxs-lookup"><span data-stu-id="38dec-299">Value</span></span>                                                                                                                               |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="38dec-300">g \_ wszWMDMAuthor</span><span class="sxs-lookup"><span data-stu-id="38dec-300">g\_wszWMDMAuthor</span></span>](metadata-constants.md)           | <span data-ttu-id="38dec-301">Zulu</span><span class="sxs-lookup"><span data-stu-id="38dec-301">Lucerne</span></span>                                                                                                                             |
| [<span data-ttu-id="38dec-302">g \_ wszWMDMAuthorDate</span><span class="sxs-lookup"><span data-stu-id="38dec-302">g\_wszWMDMAuthorDate</span></span>](metadata-constants.md)       | <span data-ttu-id="38dec-303">Qui., 1 de junho de 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="38dec-303">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |
| [<span data-ttu-id="38dec-304">g \_ wszWMDMDescription</span><span class="sxs-lookup"><span data-stu-id="38dec-304">g\_wszWMDMDescription</span></span>](metadata-constants.md)      | <span data-ttu-id="38dec-305">Publicações online estão mudando rapidamente.</span><span class="sxs-lookup"><span data-stu-id="38dec-305">Online publications are rapidly changing.</span></span> <span data-ttu-id="38dec-306">Um CEO da casa de publicação examina as tendências dos últimos cinco anos e suas implicações.</span><span class="sxs-lookup"><span data-stu-id="38dec-306">A publishing house CEO examines the trends of the past five years and their implications.</span></span> |
| [<span data-ttu-id="38dec-307">g \_ wszWMDMDestinationURL</span><span class="sxs-lookup"><span data-stu-id="38dec-307">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)   | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [<span data-ttu-id="38dec-308">g \_ wszWMDMDuration</span><span class="sxs-lookup"><span data-stu-id="38dec-308">g\_wszWMDMDuration</span></span>](metadata-constants.md)         | <span data-ttu-id="38dec-309">120325445</span><span class="sxs-lookup"><span data-stu-id="38dec-309">120325445</span></span>                                                                                                                           |
| [<span data-ttu-id="38dec-310">g \_ wszWMDMFileCreationDate</span><span class="sxs-lookup"><span data-stu-id="38dec-310">g\_wszWMDMFileCreationDate</span></span>](metadata-constants.md) | <span data-ttu-id="38dec-311">Qui., 1 de junho de 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="38dec-311">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |
| [<span data-ttu-id="38dec-312">g \_ wszWMDMFileSize</span><span class="sxs-lookup"><span data-stu-id="38dec-312">g\_wszWMDMFileSize</span></span>](metadata-constants.md)         | <span data-ttu-id="38dec-313">10329011</span><span class="sxs-lookup"><span data-stu-id="38dec-313">10329011</span></span>                                                                                                                            |
| [<span data-ttu-id="38dec-314">g \_ wszWMDMFormatCode</span><span class="sxs-lookup"><span data-stu-id="38dec-314">g\_wszWMDMFormatCode</span></span>](metadata-constants.md)       | <span data-ttu-id="38dec-315">\_FORMATCODE de \_ mp3 do WMDM</span><span class="sxs-lookup"><span data-stu-id="38dec-315">WMDM\_FORMATCODE\_MP3</span></span>                                                                                                               |
| [<span data-ttu-id="38dec-316">g \_ wszWMDMGenre</span><span class="sxs-lookup"><span data-stu-id="38dec-316">g\_wszWMDMGenre</span></span>](metadata-constants.md)            | <span data-ttu-id="38dec-317">Notícias</span><span class="sxs-lookup"><span data-stu-id="38dec-317">News</span></span>                                                                                                                                |
| [<span data-ttu-id="38dec-318">g \_ wszWMDMLastModifiedDate</span><span class="sxs-lookup"><span data-stu-id="38dec-318">g\_wszWMDMLastModifiedDate</span></span>](metadata-constants.md) | <span data-ttu-id="38dec-319">Qui., 1 de junho de 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="38dec-319">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |
| [<span data-ttu-id="38dec-320">g \_ wszWMDMMediaGuid</span><span class="sxs-lookup"><span data-stu-id="38dec-320">g\_wszWMDMMediaGuid</span></span>](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [<span data-ttu-id="38dec-321">g \_ wszWMDMSourceURL</span><span class="sxs-lookup"><span data-stu-id="38dec-321">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [<span data-ttu-id="38dec-322">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="38dec-322">g\_wszWMDMTitle</span></span>](metadata-constants.md)            | <span data-ttu-id="38dec-323">A publicação digital</span><span class="sxs-lookup"><span data-stu-id="38dec-323">The Digital Publication</span></span>                                                                                                             |
| [<span data-ttu-id="38dec-324">g \_ wszWMDMYear</span><span class="sxs-lookup"><span data-stu-id="38dec-324">g\_wszWMDMYear</span></span>](metadata-constants.md)             | <span data-ttu-id="38dec-325">Qui., 1 de junho de 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="38dec-325">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="38dec-326">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="38dec-326">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38dec-327">**Constantes de metadados**</span><span class="sxs-lookup"><span data-stu-id="38dec-327">**Metadata Constants**</span></span>](metadata-constants.md)
</dt> </dl>

 

 




