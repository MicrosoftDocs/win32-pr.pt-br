---
title: Ordem de Precedência
description: Ordem de Precedência
ms.assetid: 3865ea8a-2489-4714-9a05-d1082589841f
keywords:
- Metaarquivos do Windows Media, ordem de precedência
- Metaarquivos do Windows Media, precedência
- metaarquivos, ordem de precedência
- metaarquivos, precedência
- Windows Media, metaarquivos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9161d1e43f61ae1b1a7231c640e33c4c6ec6527f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005171"
---
# <a name="order-of-precedence"></a><span data-ttu-id="c0e45-108">Ordem de Precedência</span><span class="sxs-lookup"><span data-stu-id="c0e45-108">Order of Precedence</span></span>

<span data-ttu-id="c0e45-109">Nem todos os atributos de elemento de metarquivo são criados como iguais.</span><span class="sxs-lookup"><span data-stu-id="c0e45-109">Not all metafile element attributes are created equal.</span></span> <span data-ttu-id="c0e45-110">Alguns atributos de elemento de metarquivo substituem outros atributos de elemento.</span><span class="sxs-lookup"><span data-stu-id="c0e45-110">Some metafile element attributes override other element attributes.</span></span> <span data-ttu-id="c0e45-111">Atributos de elemento podem ser substituídos por atributos de elemento semelhantes, dependendo da posição e da ordem.</span><span class="sxs-lookup"><span data-stu-id="c0e45-111">Element attributes can be overridden by similar element attributes depending on position and order.</span></span> <span data-ttu-id="c0e45-112">Todos os atributos de uma playlist de metarquivo substituem aqueles contidos em um arquivo de mídia do Windows referenciado.</span><span class="sxs-lookup"><span data-stu-id="c0e45-112">Any attributes of a metafile playlist override those contained in a referenced Windows Media file.</span></span> <span data-ttu-id="c0e45-113">Um atributo que substitui outro tem precedência mais alta.</span><span class="sxs-lookup"><span data-stu-id="c0e45-113">An attribute that overrides another has higher precedence.</span></span>

<span data-ttu-id="c0e45-114">A hierarquia, precedência mais alta para a mais baixa, é mostrada na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c0e45-114">The hierarchy, highest precedence to lowest, is shown in the following table.</span></span> <span data-ttu-id="c0e45-115">O item de precedência mais alta nunca é substituído.</span><span class="sxs-lookup"><span data-stu-id="c0e45-115">The highest precedence item is never overridden.</span></span>



| <span data-ttu-id="c0e45-116">Escopo</span><span class="sxs-lookup"><span data-stu-id="c0e45-116">Scope</span></span>                    | <span data-ttu-id="c0e45-117">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="c0e45-117">Hierarchy</span></span>                                   |
|--------------------------|---------------------------------------------|
| <span data-ttu-id="c0e45-118">"Conteúdo DRM assinado"</span><span class="sxs-lookup"><span data-stu-id="c0e45-118">"Signed DRM content"</span></span>     | <span data-ttu-id="c0e45-119">Nunca substituído.</span><span class="sxs-lookup"><span data-stu-id="c0e45-119">Never overridden.</span></span>                           |
| <span data-ttu-id="c0e45-120">Escopo do elemento **ref**</span><span class="sxs-lookup"><span data-stu-id="c0e45-120">**REF** element scope</span></span>    | <span data-ttu-id="c0e45-121">Substituído apenas por conteúdo DRM assinado.</span><span class="sxs-lookup"><span data-stu-id="c0e45-121">Only overridden by signed DRM content.</span></span>      |
| <span data-ttu-id="c0e45-122">Escopo do elemento de **entrada**</span><span class="sxs-lookup"><span data-stu-id="c0e45-122">**ENTRY** element scope</span></span>  | <span data-ttu-id="c0e45-123">Substitui os elementos das categorias abaixo.</span><span class="sxs-lookup"><span data-stu-id="c0e45-123">Overrides elements of the categories below.</span></span> |
| <span data-ttu-id="c0e45-124">Escopo **ASX**</span><span class="sxs-lookup"><span data-stu-id="c0e45-124">**ASX** scope</span></span>            | <span data-ttu-id="c0e45-125">Substitui elementos do arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="c0e45-125">Overrides media file elements.</span></span>              |
| <span data-ttu-id="c0e45-126">Escopo do arquivo de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="c0e45-126">Windows Media file scope</span></span> | <span data-ttu-id="c0e45-127">Substituído por todos os itens acima.</span><span class="sxs-lookup"><span data-stu-id="c0e45-127">Overridden by all of the above.</span></span>             |



 

-   <span data-ttu-id="c0e45-128">"Conteúdo DRM assinado"-objeto de assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="c0e45-128">"Signed DRM content" - Digital signature object.</span></span>

    <span data-ttu-id="c0e45-129">Os atributos de conteúdo DRM assinado substituirão todos os outros.</span><span class="sxs-lookup"><span data-stu-id="c0e45-129">Attributes of Signed DRM content will override all others.</span></span> <span data-ttu-id="c0e45-130">Por exemplo, as informações de direitos autorais de "conteúdo DRM assinado" não serão substituídas.</span><span class="sxs-lookup"><span data-stu-id="c0e45-130">For example, the Copyright information of "Signed DRM content" will not be overridden.</span></span> <span data-ttu-id="c0e45-131">Ele será sempre transmitido e apresentado.</span><span class="sxs-lookup"><span data-stu-id="c0e45-131">It will always be streamed and presented.</span></span>

-   <span data-ttu-id="c0e45-132">Escopo do elemento **ref**</span><span class="sxs-lookup"><span data-stu-id="c0e45-132">**REF** element scope</span></span>

    <span data-ttu-id="c0e45-133">Os atributos do elemento **ref** substituirão outros atributos de elemento, mas não o conteúdo DRM assinado.</span><span class="sxs-lookup"><span data-stu-id="c0e45-133">Attributes of the **REF** element will override other element attributes, but not signed DRM content.</span></span>

-   <span data-ttu-id="c0e45-134">Escopo de **entrada**</span><span class="sxs-lookup"><span data-stu-id="c0e45-134">**ENTRY** scope</span></span>

    <span data-ttu-id="c0e45-135">Os atributos do elemento de **entrada** serão substituídos pelo atributo **ref** element, mas substituirão outros atributos Element.</span><span class="sxs-lookup"><span data-stu-id="c0e45-135">Attributes of the **ENTRY** element will be overridden by the **REF** element attribute but will override other element attributes.</span></span> <span data-ttu-id="c0e45-136">Os metadados de **título** do elemento de **entrada** são exibidos em vez das informações de título do arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="c0e45-136">**TITLE** metadata from the **ENTRY** element is displayed instead of the title information from the media file.</span></span>

-   <span data-ttu-id="c0e45-137">Escopo **ASX**</span><span class="sxs-lookup"><span data-stu-id="c0e45-137">**ASX** scope</span></span>

    <span data-ttu-id="c0e45-138">Todas as propriedades que são inseridas no metarquivo substituem aquelas contidas no arquivo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c0e45-138">Any properties that are entered in the metafile override those contained in the Windows Media file.</span></span> <span data-ttu-id="c0e45-139">Atributos do elemento de **entrada** substituem atributos de elemento **ASX** .</span><span class="sxs-lookup"><span data-stu-id="c0e45-139">Attributes of the **ENTRY** element override **ASX** element attributes.</span></span> <span data-ttu-id="c0e45-140">Enquanto o clipe de mídia referenciado do elemento de **entrada** está sendo reproduzido, os metadados do **título** do elemento de **entrada** são exibidos em vez das informações de título do elemento **ASX** .</span><span class="sxs-lookup"><span data-stu-id="c0e45-140">While the **ENTRY** element's referenced media clip is playing, **TITLE** metadata from the **ENTRY** element is displayed instead of title information from the **ASX** element.</span></span>

-   <span data-ttu-id="c0e45-141">Escopo do arquivo de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="c0e45-141">Windows Media file scope</span></span>

    <span data-ttu-id="c0e45-142">Os atributos do arquivo de mídia do Windows são substituídos por qualquer atributo de metarquivo.</span><span class="sxs-lookup"><span data-stu-id="c0e45-142">Attributes of the Windows Media file are overridden by any metafile attributes.</span></span> <span data-ttu-id="c0e45-143">Os metadados do arquivo de mídia são exibidos somente se não houver nenhum metadado definido para esse elemento no metarquivo.</span><span class="sxs-lookup"><span data-stu-id="c0e45-143">Media file metadata is displayed only if there is no metadata defined for that element in the metafile.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0e45-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c0e45-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0e45-145">**Criando listas de reprodução de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="c0e45-145">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="c0e45-146">**Playlists de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="c0e45-146">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="c0e45-147">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="c0e45-147">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="c0e45-148">**Guia de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="c0e45-148">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




