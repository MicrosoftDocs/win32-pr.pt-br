---
title: Interface IPropertyFilterCollection (WdsSharedIDL. h)
description: Expõe as propriedades da coleção retornada com base na consulta enviada.
ms.assetid: 9ed4217f-54b0-4d69-bf44-2547320a9681
keywords:
- Recursos do ambiente Windows herdado da interface IPropertyFilterCollection
- Recursos do ambiente Windows herdado da interface IPropertyFilterCollection, descritos
topic_type:
- apiref
api_name:
- IPropertyFilterCollection
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9be9fe01bacf24c852b49538beae16b4ecbc97b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295819"
---
# <a name="ipropertyfiltercollection-interface"></a><span data-ttu-id="b7622-105">Interface IPropertyFilterCollection</span><span class="sxs-lookup"><span data-stu-id="b7622-105">IPropertyFilterCollection interface</span></span>

> [!NOTE]
> <span data-ttu-id="b7622-106">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b7622-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="b7622-107">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="b7622-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="b7622-108">Expõe as propriedades da coleção retornada com base na consulta enviada.</span><span class="sxs-lookup"><span data-stu-id="b7622-108">Exposes properties of the returned collection based on the query submitted.</span></span>

## <a name="members"></a><span data-ttu-id="b7622-109">Membros</span><span class="sxs-lookup"><span data-stu-id="b7622-109">Members</span></span>

<span data-ttu-id="b7622-110">A interface **IPropertyFilterCollection** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b7622-110">The **IPropertyFilterCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b7622-111">**IPropertyFilterCollection** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b7622-111">**IPropertyFilterCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="b7622-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b7622-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b7622-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b7622-113">Properties</span></span>

<span data-ttu-id="b7622-114">A interface **IPropertyFilterCollection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b7622-114">The **IPropertyFilterCollection** interface has these properties.</span></span>



| <span data-ttu-id="b7622-115">Propriedade</span><span class="sxs-lookup"><span data-stu-id="b7622-115">Property</span></span>                                                                         | <span data-ttu-id="b7622-116">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="b7622-116">Access type</span></span>           | <span data-ttu-id="b7622-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7622-117">Description</span></span>                                                  |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="b7622-118">**Item**</span><span class="sxs-lookup"><span data-stu-id="b7622-118">**AddItem**</span></span>](-search-2x-ipropertyfiltercollection-additem.md)<br/>       | <span data-ttu-id="b7622-119">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b7622-119">Read-only</span></span><br/>  | <span data-ttu-id="b7622-120">Adiciona um novo filtro à coleção.</span><span class="sxs-lookup"><span data-stu-id="b7622-120">Adds a new filter to the collection.</span></span> <br/>             |
| [<span data-ttu-id="b7622-121">**formatação**</span><span class="sxs-lookup"><span data-stu-id="b7622-121">**clear**</span></span>](-search-2x-ipropertyfiltercollection-clear.md)<br/>           | <span data-ttu-id="b7622-122">Somente gravação</span><span class="sxs-lookup"><span data-stu-id="b7622-122">Write-only</span></span><br/> | <span data-ttu-id="b7622-123">Limpa a coleção.</span><span class="sxs-lookup"><span data-stu-id="b7622-123">Clears the collection.</span></span> <br/>                           |
| [<span data-ttu-id="b7622-124">**Contar**</span><span class="sxs-lookup"><span data-stu-id="b7622-124">**Count**</span></span>](-search-2x-ipropertyfiltercollection-count.md)<br/>           | <span data-ttu-id="b7622-125">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b7622-125">Read-only</span></span><br/>  | <span data-ttu-id="b7622-126">Número de filtros na coleção.</span><span class="sxs-lookup"><span data-stu-id="b7622-126">Number of filters in the collection.</span></span> <br/>             |
| [<span data-ttu-id="b7622-127">**GetITem**</span><span class="sxs-lookup"><span data-stu-id="b7622-127">**GetITem**</span></span>](-search-2x-ipropertyfiltercollection-getitem.md)<br/>       | <span data-ttu-id="b7622-128">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b7622-128">Read/write</span></span><br/> | <span data-ttu-id="b7622-129">Retorna um filtro específico dentro da coleção.</span><span class="sxs-lookup"><span data-stu-id="b7622-129">Returns a specific filter within the collection.</span></span> <br/> |
| [<span data-ttu-id="b7622-130">**RemoveItem**</span><span class="sxs-lookup"><span data-stu-id="b7622-130">**RemoveItem**</span></span>](-search-2x-ipropertyfiltercollection-removeitem.md)<br/> | <span data-ttu-id="b7622-131">Somente gravação</span><span class="sxs-lookup"><span data-stu-id="b7622-131">Write-only</span></span><br/> | <span data-ttu-id="b7622-132">Remove um filtro específico para a coleção.</span><span class="sxs-lookup"><span data-stu-id="b7622-132">Removes a specific filter to the collection.</span></span> <br/>     |



 

## <a name="remarks"></a><span data-ttu-id="b7622-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7622-133">Remarks</span></span>

<span data-ttu-id="b7622-134">Essas propriedades são usadas para filtrar a coleção retornada pela consulta.</span><span class="sxs-lookup"><span data-stu-id="b7622-134">These properties are used to filter collection returned by the query.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7622-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7622-135">Requirements</span></span>



| <span data-ttu-id="b7622-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7622-136">Requirement</span></span> | <span data-ttu-id="b7622-137">Valor</span><span class="sxs-lookup"><span data-stu-id="b7622-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7622-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7622-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b7622-139">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="b7622-139">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b7622-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7622-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b7622-141">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="b7622-141">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b7622-142">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="b7622-142">Redistributable</span></span><br/>          | <span data-ttu-id="b7622-143">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="b7622-143">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="b7622-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b7622-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7622-145"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7622-145"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

