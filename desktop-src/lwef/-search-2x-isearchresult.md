---
title: Interface ISearchResult (WdsSharedIDL. h)
description: Expõe informações e propriedades referentes ao conjunto de resultados.
ms.assetid: 2f50b9d7-f6fd-481c-a5db-d622a7b02017
keywords:
- Recursos do ambiente Windows herdado da interface ISearchResult
- Recursos do ambiente Windows herdado da interface ISearchResult, descritos
topic_type:
- apiref
api_name:
- ISearchResult
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89387ebe02c87ca6a5c5ac663a67ea060bd78948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644852"
---
# <a name="isearchresult-interface"></a><span data-ttu-id="d10db-105">Interface ISearchResult</span><span class="sxs-lookup"><span data-stu-id="d10db-105">ISearchResult interface</span></span>

> [!NOTE]
> <span data-ttu-id="d10db-106">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d10db-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="d10db-107">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="d10db-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="d10db-108">Expõe informações e propriedades referentes ao conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="d10db-108">Exposes information and properties regarding the result set.</span></span>

## <a name="members"></a><span data-ttu-id="d10db-109">Membros</span><span class="sxs-lookup"><span data-stu-id="d10db-109">Members</span></span>

<span data-ttu-id="d10db-110">A interface **ISearchResult** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d10db-110">The **ISearchResult** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d10db-111">**ISearchResult** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d10db-111">**ISearchResult** also has these types of members:</span></span>

-   [<span data-ttu-id="d10db-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="d10db-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d10db-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="d10db-113">Methods</span></span>

<span data-ttu-id="d10db-114">A interface **ISearchResult** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d10db-114">The **ISearchResult** interface has these methods.</span></span>



| <span data-ttu-id="d10db-115">Método</span><span class="sxs-lookup"><span data-stu-id="d10db-115">Method</span></span>                                                            | <span data-ttu-id="d10db-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d10db-116">Description</span></span>                 |
|:------------------------------------------------------------------|:----------------------------|
| [<span data-ttu-id="d10db-117">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="d10db-117">**Availability**</span></span>](-search-2x-isearchresult-availability.md)     | <span data-ttu-id="d10db-118">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="d10db-118">Not implemented.</span></span><br/> |
| [<span data-ttu-id="d10db-119">**Doverbs**</span><span class="sxs-lookup"><span data-stu-id="d10db-119">**DoVerb**</span></span>](-search-2x-isearchresult-doverb.md)                 | <span data-ttu-id="d10db-120">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="d10db-120">Not implemented.</span></span><br/> |
| [<span data-ttu-id="d10db-121">**GetIcon**</span><span class="sxs-lookup"><span data-stu-id="d10db-121">**GetIcon**</span></span>](-search-2x-isearchresult-geticon.md)               | <span data-ttu-id="d10db-122">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="d10db-122">Not implemented.</span></span><br/> |
| [<span data-ttu-id="d10db-123">**GetThumbnail**</span><span class="sxs-lookup"><span data-stu-id="d10db-123">**GetThumbnail**</span></span>](-search-2x-isearchresult-getthumbnail.md)     | <span data-ttu-id="d10db-124">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="d10db-124">Not implemented.</span></span><br/> |
| [<span data-ttu-id="d10db-125">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="d10db-125">**GetValue**</span></span>](-search-2x-isearchresult-getvalue.md)             | <span data-ttu-id="d10db-126">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="d10db-126">Not implemented.</span></span><br/> |
| [<span data-ttu-id="d10db-127">**Getverbs**</span><span class="sxs-lookup"><span data-stu-id="d10db-127">**GetVerb**</span></span>](-search-2x-isearchresult-getverb.md)               | <span data-ttu-id="d10db-128">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="d10db-128">Not implemented.</span></span><br/> |
| [<span data-ttu-id="d10db-129">**IconCount**</span><span class="sxs-lookup"><span data-stu-id="d10db-129">**IconCount**</span></span>](-search-2x-isearchresult-iconcount.md)           | <span data-ttu-id="d10db-130">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="d10db-130">Not implemented.</span></span><br/> |
| [<span data-ttu-id="d10db-131">**Index**</span><span class="sxs-lookup"><span data-stu-id="d10db-131">**Index**</span></span>](-search-2x-isearchresult-index.md)                   | <span data-ttu-id="d10db-132">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="d10db-132">Not implemented.</span></span><br/> |
| [<span data-ttu-id="d10db-133">**LoadState**</span><span class="sxs-lookup"><span data-stu-id="d10db-133">**LoadState**</span></span>](-search-2x-isearchresult-loadstate.md)           | <span data-ttu-id="d10db-134">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="d10db-134">Not implemented.</span></span><br/> |
| [<span data-ttu-id="d10db-135">**Pré-visualizador**</span><span class="sxs-lookup"><span data-stu-id="d10db-135">**Previewer**</span></span>](-search-2x-isearchresult-previewer.md)           | <span data-ttu-id="d10db-136">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="d10db-136">Not implemented.</span></span><br/> |
| [<span data-ttu-id="d10db-137">**PutValue**</span><span class="sxs-lookup"><span data-stu-id="d10db-137">**PutValue**</span></span>](-search-2x-isearchresult-putvalue.md)             | <span data-ttu-id="d10db-138">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="d10db-138">Not implemented.</span></span><br/> |
| [<span data-ttu-id="d10db-139">**Miniaturastate**</span><span class="sxs-lookup"><span data-stu-id="d10db-139">**ThumbnailState**</span></span>](-search-2x-isearchresult-thumbnailstate.md) | <span data-ttu-id="d10db-140">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="d10db-140">Not implemented.</span></span><br/> |
| [<span data-ttu-id="d10db-141">**Escreva**</span><span class="sxs-lookup"><span data-stu-id="d10db-141">**Type**</span></span>](-search-2x-isearchresult-type.md)                     | <span data-ttu-id="d10db-142">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="d10db-142">Not implemented.</span></span><br/> |
| [<span data-ttu-id="d10db-143">**VerbCount**</span><span class="sxs-lookup"><span data-stu-id="d10db-143">**VerbCount**</span></span>](-search-2x-isearchresult-verbcount.md)           | <span data-ttu-id="d10db-144">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="d10db-144">Not implemented.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d10db-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="d10db-145">Remarks</span></span>

<span data-ttu-id="d10db-146">Esses métodos expõem propriedades e ações aplicáveis ao conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="d10db-146">These methods expose properties and actions applicable to the result set.</span></span>

## <a name="requirements"></a><span data-ttu-id="d10db-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d10db-147">Requirements</span></span>



| <span data-ttu-id="d10db-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="d10db-148">Requirement</span></span> | <span data-ttu-id="d10db-149">Valor</span><span class="sxs-lookup"><span data-stu-id="d10db-149">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d10db-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d10db-150">Minimum supported client</span></span><br/> | <span data-ttu-id="d10db-151">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="d10db-151">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d10db-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d10db-152">Minimum supported server</span></span><br/> | <span data-ttu-id="d10db-153">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="d10db-153">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d10db-154">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="d10db-154">Redistributable</span></span><br/>          | <span data-ttu-id="d10db-155">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="d10db-155">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="d10db-156">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d10db-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="d10db-157"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d10db-157"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

