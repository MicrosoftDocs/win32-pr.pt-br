---
title: Interface IResultsViewer (WdsSharedIDL. h)
description: Expõe métodos e propriedades para a exibição de resultados.
ms.assetid: 4d476511-d65c-4417-8073-337cfbae621d
keywords:
- Recursos do ambiente Windows herdado da interface IResultsViewer
- Recursos do ambiente Windows herdado da interface IResultsViewer, descritos
topic_type:
- apiref
api_name:
- IResultsViewer
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18702812394f6e7fedd626062aa8c0116cab8427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499490"
---
# <a name="iresultsviewer-interface"></a><span data-ttu-id="cdc42-105">Interface IResultsViewer</span><span class="sxs-lookup"><span data-stu-id="cdc42-105">IResultsViewer interface</span></span>

> [!NOTE]
> <span data-ttu-id="cdc42-106">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cdc42-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="cdc42-107">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="cdc42-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="cdc42-108">Expõe métodos e propriedades para a exibição de resultados.</span><span class="sxs-lookup"><span data-stu-id="cdc42-108">Exposes methods and properties for the results view.</span></span>

## <a name="members"></a><span data-ttu-id="cdc42-109">Membros</span><span class="sxs-lookup"><span data-stu-id="cdc42-109">Members</span></span>

<span data-ttu-id="cdc42-110">A interface **IResultsViewer** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="cdc42-110">The **IResultsViewer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cdc42-111">**IResultsViewer** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cdc42-111">**IResultsViewer** also has these types of members:</span></span>

-   [<span data-ttu-id="cdc42-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="cdc42-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="cdc42-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cdc42-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cdc42-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="cdc42-114">Methods</span></span>

<span data-ttu-id="cdc42-115">A interface **IResultsViewer** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="cdc42-115">The **IResultsViewer** interface has these methods.</span></span>



| <span data-ttu-id="cdc42-116">Método</span><span class="sxs-lookup"><span data-stu-id="cdc42-116">Method</span></span>                                                   | <span data-ttu-id="cdc42-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="cdc42-117">Description</span></span>                                                                            |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="cdc42-118">**GoBack**</span><span class="sxs-lookup"><span data-stu-id="cdc42-118">**GoBack**</span></span>](-search-2x-iresultsviewer-goback.md)       | <span data-ttu-id="cdc42-119">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="cdc42-119">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="cdc42-120">**GoForward**</span><span class="sxs-lookup"><span data-stu-id="cdc42-120">**GoForward**</span></span>](-search-2x-iresultsviewer-goforward.md) | <span data-ttu-id="cdc42-121">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="cdc42-121">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="cdc42-122">**Atualizar**</span><span class="sxs-lookup"><span data-stu-id="cdc42-122">**Refresh**</span></span>](-search-2x-iresultsviewer-refresh.md)     | <span data-ttu-id="cdc42-123">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="cdc42-123">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="cdc42-124">**Stop**</span><span class="sxs-lookup"><span data-stu-id="cdc42-124">**Stop**</span></span>](-search-2x-iresultsviewer-stop.md)           | <span data-ttu-id="cdc42-125">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="cdc42-125">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="cdc42-126">**Cumulativo**</span><span class="sxs-lookup"><span data-stu-id="cdc42-126">**Update**</span></span>](-search-2x-iresultsviewer-update.md)       | <span data-ttu-id="cdc42-127">Aplica qualquer alteração de consulta e navega a exibição para o novo conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="cdc42-127">Applies any query changes and navigates the view to the new set of results.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="cdc42-128">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cdc42-128">Properties</span></span>

<span data-ttu-id="cdc42-129">A interface **IResultsViewer** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cdc42-129">The **IResultsViewer** interface has these properties.</span></span>



| <span data-ttu-id="cdc42-130">Propriedade</span><span class="sxs-lookup"><span data-stu-id="cdc42-130">Property</span></span>                                                                            | <span data-ttu-id="cdc42-131">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="cdc42-131">Access type</span></span>           | <span data-ttu-id="cdc42-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="cdc42-132">Description</span></span>                                                                                      |
|:------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cdc42-133">**Sumário**</span><span class="sxs-lookup"><span data-stu-id="cdc42-133">**Contents**</span></span>](-search-2x-iresultsviewer-contents.md)<br/>                   | <span data-ttu-id="cdc42-134">Somente gravação</span><span class="sxs-lookup"><span data-stu-id="cdc42-134">Write-only</span></span><br/> | <span data-ttu-id="cdc42-135">Essa propriedade controla o tipo do conteúdo que está sendo exibido no modo de exibição de resultados.</span><span class="sxs-lookup"><span data-stu-id="cdc42-135">This property tracks the type of the content being displayed in the results view.</span></span> <br/>    |
| [<span data-ttu-id="cdc42-136">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="cdc42-136">**DisplayName**</span></span>](-search-2x-iresultsviewer-displayname.md)<br/>             | <span data-ttu-id="cdc42-137">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cdc42-137">Read-only</span></span><br/>  | <span data-ttu-id="cdc42-138">Nome de exibição localizado do tipo.</span><span class="sxs-lookup"><span data-stu-id="cdc42-138">Localized display name of the type.</span></span><br/>                                                   |
| [<span data-ttu-id="cdc42-139">**EnumSelectedItems**</span><span class="sxs-lookup"><span data-stu-id="cdc42-139">**EnumSelectedItems**</span></span>](-search-2x-iresultsviewer-enumselecteditems.md)<br/> | <span data-ttu-id="cdc42-140">Somente gravação</span><span class="sxs-lookup"><span data-stu-id="cdc42-140">Write-only</span></span><br/> | <span data-ttu-id="cdc42-141">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="cdc42-141">Not implemented.</span></span><br/>                                                                      |
| [<span data-ttu-id="cdc42-142">**FilterType**</span><span class="sxs-lookup"><span data-stu-id="cdc42-142">**FilterType**</span></span>](-search-2x-iresultsviewer-filtertype.md)<br/>               | <span data-ttu-id="cdc42-143">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cdc42-143">Read/write</span></span><br/> | <span data-ttu-id="cdc42-144">Essa propriedade definirá ou retornará o nome do tipo preceived para filtrar os resultados por.</span><span class="sxs-lookup"><span data-stu-id="cdc42-144">This property will set or return the name of the preceived type to filter results by.</span></span><br/> |
| [<span data-ttu-id="cdc42-145">**HeaderStyle**</span><span class="sxs-lookup"><span data-stu-id="cdc42-145">**HeaderStyle**</span></span>](-search-2x-iresultsviewer-headerstyle.md)<br/>             | <span data-ttu-id="cdc42-146">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cdc42-146">Read/write</span></span><br/> | <span data-ttu-id="cdc42-147">O estilo do cabeçalho exibido na exibição.</span><span class="sxs-lookup"><span data-stu-id="cdc42-147">The style of header displayed in the view.</span></span><br/>                                            |
| [<span data-ttu-id="cdc42-148">**IsUpdateNeeded**</span><span class="sxs-lookup"><span data-stu-id="cdc42-148">**IsUpdateNeeded**</span></span>](-search-2x-iresultsviewer-isupdateneeded.md)<br/>       | <span data-ttu-id="cdc42-149">Somente gravação</span><span class="sxs-lookup"><span data-stu-id="cdc42-149">Write-only</span></span><br/> | <span data-ttu-id="cdc42-150">Isso retornará TRUE se a consulta views tiver sido modificada e precisar de atualização.</span><span class="sxs-lookup"><span data-stu-id="cdc42-150">This returns TRUE if the views query has been modified and needs updating.</span></span> <br/>           |
| [<span data-ttu-id="cdc42-151">**Repositório de armazenamento**</span><span class="sxs-lookup"><span data-stu-id="cdc42-151">**ItemStore**</span></span>](-search-2x-iresultsviewer-itemstore.md)<br/>                 | <span data-ttu-id="cdc42-152">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cdc42-152">Read/write</span></span><br/> | <span data-ttu-id="cdc42-153">Essa propriedade definirá ou retornará o nome do repositório para filtrar os resultados por.</span><span class="sxs-lookup"><span data-stu-id="cdc42-153">This property will set or return the name of the store to filter results by.</span></span><br/>          |
| [<span data-ttu-id="cdc42-154">**Modo de exibição**</span><span class="sxs-lookup"><span data-stu-id="cdc42-154">**PreviewStyle**</span></span>](-search-2x-iresultsviewer-previewstyle.md)<br/>           | <span data-ttu-id="cdc42-155">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cdc42-155">Read/write</span></span><br/> | <span data-ttu-id="cdc42-156">Controla o modo de exibição do painel de visualização.</span><span class="sxs-lookup"><span data-stu-id="cdc42-156">Controls the preview pane's display mode.</span></span><br/>                                             |
| [<span data-ttu-id="cdc42-157">**PropertyFilters**</span><span class="sxs-lookup"><span data-stu-id="cdc42-157">**PropertyFilters**</span></span>](-search-2x-iresultsviewer-propertyfilters.md)<br/>     | <span data-ttu-id="cdc42-158">Somente gravação</span><span class="sxs-lookup"><span data-stu-id="cdc42-158">Write-only</span></span><br/> | <span data-ttu-id="cdc42-159">Ao chamar a coleção de filtros de propriedade, ele retornará o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cdc42-159">When calling the property filter collection it will return the following:</span></span><br/>             |
| [<span data-ttu-id="cdc42-160">**QueryText**</span><span class="sxs-lookup"><span data-stu-id="cdc42-160">**QueryText**</span></span>](-search-2x-iresultsviewer-querytext.md)<br/>                 | <span data-ttu-id="cdc42-161">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cdc42-161">Read/write</span></span><br/> | <span data-ttu-id="cdc42-162">Obtém ou define o texto da consulta atual.</span><span class="sxs-lookup"><span data-stu-id="cdc42-162">Gets or sets the current query text.</span></span><br/>                                                  |
| [<span data-ttu-id="cdc42-163">**Resultstyle**</span><span class="sxs-lookup"><span data-stu-id="cdc42-163">**ResultsStyle**</span></span>](-search-2x-iresultsviewer-resultsstyle.md)<br/>           | <span data-ttu-id="cdc42-164">Somente gravação</span><span class="sxs-lookup"><span data-stu-id="cdc42-164">Write-only</span></span><br/> | <span data-ttu-id="cdc42-165">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="cdc42-165">Not implemented.</span></span><br/>                                                                      |
| [<span data-ttu-id="cdc42-166">**SortOrderproperty**</span><span class="sxs-lookup"><span data-stu-id="cdc42-166">**SortOrderProperty**</span></span>](-search-2x-iresultsviewer-sortorderproperty.md)<br/> | <span data-ttu-id="cdc42-167">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cdc42-167">Read/write</span></span><br/> | <span data-ttu-id="cdc42-168">Essa propriedade definirá ou retornará a ordem das colunas para classificar os resultados por.</span><span class="sxs-lookup"><span data-stu-id="cdc42-168">This property will set or return the order of columns to sort results by.</span></span> <br/>            |
| [<span data-ttu-id="cdc42-169">**SortProperty**</span><span class="sxs-lookup"><span data-stu-id="cdc42-169">**SortProperty**</span></span>](-search-2x-iresultsviewer-sortproperty.md)<br/>           | <span data-ttu-id="cdc42-170">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cdc42-170">Read/write</span></span><br/> | <span data-ttu-id="cdc42-171">Essa propriedade irá definir ou retornar o IndexColumn da propriedade para classificar os resultados por.</span><span class="sxs-lookup"><span data-stu-id="cdc42-171">This property will set or return the IndexColumn of the property to sort results by.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="cdc42-172">Comentários</span><span class="sxs-lookup"><span data-stu-id="cdc42-172">Remarks</span></span>

<span data-ttu-id="cdc42-173">Esses métodos e propriedades são usados para manipular as informações exibidas.</span><span class="sxs-lookup"><span data-stu-id="cdc42-173">These methods and properties are used to manipulate the information viewed.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdc42-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdc42-174">Requirements</span></span>



| <span data-ttu-id="cdc42-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdc42-175">Requirement</span></span> | <span data-ttu-id="cdc42-176">Valor</span><span class="sxs-lookup"><span data-stu-id="cdc42-176">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdc42-177">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cdc42-177">Minimum supported client</span></span><br/> | <span data-ttu-id="cdc42-178">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="cdc42-178">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="cdc42-179">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cdc42-179">Minimum supported server</span></span><br/> | <span data-ttu-id="cdc42-180">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="cdc42-180">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cdc42-181">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="cdc42-181">Redistributable</span></span><br/>          | <span data-ttu-id="cdc42-182">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="cdc42-182">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="cdc42-183">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cdc42-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdc42-184"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdc42-184"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

