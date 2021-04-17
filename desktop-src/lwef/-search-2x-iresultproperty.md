---
title: Interface IResultProperty (WdsSharedIDL. h)
description: Expõe as propriedades de resultado.
ms.assetid: 58d8c516-47c6-4cae-b46c-5127baf3054d
keywords:
- Recursos do ambiente Windows herdado da interface IResultProperty
- Recursos do ambiente Windows herdado da interface IResultProperty, descritos
topic_type:
- apiref
api_name:
- IResultProperty
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 716c0b3998171731dea5f976afc266fe81b2c613
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760993"
---
# <a name="iresultproperty-interface"></a><span data-ttu-id="c2ac7-105">Interface IResultProperty</span><span class="sxs-lookup"><span data-stu-id="c2ac7-105">IResultProperty interface</span></span>

> [!NOTE]
> <span data-ttu-id="c2ac7-106">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="c2ac7-107">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="c2ac7-108">Expõe as propriedades de resultado.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-108">Exposes result properties.</span></span>

## <a name="members"></a><span data-ttu-id="c2ac7-109">Membros</span><span class="sxs-lookup"><span data-stu-id="c2ac7-109">Members</span></span>

<span data-ttu-id="c2ac7-110">A interface **IResultProperty** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c2ac7-110">The **IResultProperty** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c2ac7-111">**IResultProperty** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c2ac7-111">**IResultProperty** also has these types of members:</span></span>

-   [<span data-ttu-id="c2ac7-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="c2ac7-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="c2ac7-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c2ac7-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c2ac7-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="c2ac7-114">Methods</span></span>

<span data-ttu-id="c2ac7-115">A interface **IResultProperty** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-115">The **IResultProperty** interface has these methods.</span></span>



| <span data-ttu-id="c2ac7-116">Método</span><span class="sxs-lookup"><span data-stu-id="c2ac7-116">Method</span></span>                                                    | <span data-ttu-id="c2ac7-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2ac7-117">Description</span></span>                 |
|:----------------------------------------------------------|:----------------------------|
| [<span data-ttu-id="c2ac7-118">**GoBack**</span><span class="sxs-lookup"><span data-stu-id="c2ac7-118">**GoBack**</span></span>](-search-2x-iresultproperty-goback.md)       | <span data-ttu-id="c2ac7-119">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-119">Not implemented.</span></span><br/> |
| [<span data-ttu-id="c2ac7-120">**GoForward**</span><span class="sxs-lookup"><span data-stu-id="c2ac7-120">**GoForward**</span></span>](-search-2x-iresultproperty-goforward.md) | <span data-ttu-id="c2ac7-121">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-121">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c2ac7-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c2ac7-122">Properties</span></span>

<span data-ttu-id="c2ac7-123">A interface **IResultProperty** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-123">The **IResultProperty** interface has these properties.</span></span>



| <span data-ttu-id="c2ac7-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c2ac7-124">Property</span></span>                                                                   | <span data-ttu-id="c2ac7-125">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="c2ac7-125">Access type</span></span>          | <span data-ttu-id="c2ac7-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2ac7-126">Description</span></span>                                           |
|:---------------------------------------------------------------------------|:---------------------|:------------------------------------------------------|
| [<span data-ttu-id="c2ac7-127">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="c2ac7-127">**DataType**</span></span>](-search-2x-iresultproperty-datatype.md)<br/>         | <span data-ttu-id="c2ac7-128">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2ac7-128">Read-only</span></span><br/> | <span data-ttu-id="c2ac7-129">Um tipo de dados de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-129">A properties data type.</span></span> <br/>                   |
| [<span data-ttu-id="c2ac7-130">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="c2ac7-130">**DisplayName**</span></span>](-search-2x-iresultproperty-displayname.md)<br/>   | <span data-ttu-id="c2ac7-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2ac7-131">Read-only</span></span><br/> | <span data-ttu-id="c2ac7-132">Nome de exibição localizado da propriedade.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-132">Localized display name of the property.</span></span> <br/>   |
| [<span data-ttu-id="c2ac7-133">**DisplayState**</span><span class="sxs-lookup"><span data-stu-id="c2ac7-133">**DisplayState**</span></span>](-search-2x-iresultproperty-displaystate.md)<br/> | <span data-ttu-id="c2ac7-134">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2ac7-134">Read-only</span></span><br/> | <span data-ttu-id="c2ac7-135">Visability da propriedade.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-135">Visability of the property.</span></span> <br/>               |
| [<span data-ttu-id="c2ac7-136">**Hint**</span><span class="sxs-lookup"><span data-stu-id="c2ac7-136">**Hint**</span></span>](-search-2x-iresultproperty-hint.md)<br/>                 | <span data-ttu-id="c2ac7-137">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2ac7-137">Read-only</span></span><br/> | <span data-ttu-id="c2ac7-138">Valor especial usado para auxiliar a recuperação de dados.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-138">Special value used to aid data retrieval.</span></span> <br/> |
| [<span data-ttu-id="c2ac7-139">**IndexColumn**</span><span class="sxs-lookup"><span data-stu-id="c2ac7-139">**IndexColumn**</span></span>](-search-2x-iresultproperty-indexcolumn.md)<br/>   | <span data-ttu-id="c2ac7-140">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2ac7-140">Read-only</span></span><br/> | <span data-ttu-id="c2ac7-141">Nome da coluna de propriedades no índice.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-141">Properties column name in the index.</span></span> <br/>      |
| [<span data-ttu-id="c2ac7-142">**UID**</span><span class="sxs-lookup"><span data-stu-id="c2ac7-142">**UID**</span></span>](-search-2x-iresultproperty-uid.md)<br/>                   | <span data-ttu-id="c2ac7-143">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2ac7-143">Read-only</span></span><br/> | <span data-ttu-id="c2ac7-144">Identificador exclusivo da propriedade.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-144">Unique identifier for the property.</span></span> <br/>       |



 

## <a name="remarks"></a><span data-ttu-id="c2ac7-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2ac7-145">Remarks</span></span>

<span data-ttu-id="c2ac7-146">Esses são os itens que retornam propriedades.</span><span class="sxs-lookup"><span data-stu-id="c2ac7-146">These are the items return properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2ac7-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2ac7-147">Requirements</span></span>



| <span data-ttu-id="c2ac7-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2ac7-148">Requirement</span></span> | <span data-ttu-id="c2ac7-149">Valor</span><span class="sxs-lookup"><span data-stu-id="c2ac7-149">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2ac7-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2ac7-150">Minimum supported client</span></span><br/> | <span data-ttu-id="c2ac7-151">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="c2ac7-151">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c2ac7-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2ac7-152">Minimum supported server</span></span><br/> | <span data-ttu-id="c2ac7-153">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="c2ac7-153">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c2ac7-154">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="c2ac7-154">Redistributable</span></span><br/>          | <span data-ttu-id="c2ac7-155">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="c2ac7-155">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="c2ac7-156">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c2ac7-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2ac7-157"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2ac7-157"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

