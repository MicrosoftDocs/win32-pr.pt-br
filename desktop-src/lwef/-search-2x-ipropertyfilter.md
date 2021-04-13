---
title: Interface IPropertyFilter (WdsSharedIDL. h)
description: Expõe as propriedades usadas para filtrar a consulta.
ms.assetid: 3760c413-931c-44f2-adaf-eb17df4015c3
keywords:
- Recursos do ambiente Windows herdado da interface IPropertyFilter
- Recursos do ambiente Windows herdado da interface IPropertyFilter, descritos
topic_type:
- apiref
api_name:
- IPropertyFilter
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4358ca7e111fd68beb68391ba7f08a9b8095d7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499552"
---
# <a name="ipropertyfilter-interface"></a><span data-ttu-id="39181-105">Interface IPropertyFilter</span><span class="sxs-lookup"><span data-stu-id="39181-105">IPropertyFilter interface</span></span>

> [!NOTE]
> <span data-ttu-id="39181-106">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="39181-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="39181-107">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="39181-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="39181-108">Expõe as propriedades usadas para filtrar a consulta.</span><span class="sxs-lookup"><span data-stu-id="39181-108">Exposes properties used to filter the query.</span></span>

## <a name="members"></a><span data-ttu-id="39181-109">Membros</span><span class="sxs-lookup"><span data-stu-id="39181-109">Members</span></span>

<span data-ttu-id="39181-110">A interface **IPropertyFilter** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="39181-110">The **IPropertyFilter** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="39181-111">**IPropertyFilter** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="39181-111">**IPropertyFilter** also has these types of members:</span></span>

-   [<span data-ttu-id="39181-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="39181-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="39181-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="39181-113">Properties</span></span>

<span data-ttu-id="39181-114">A interface **IPropertyFilter** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="39181-114">The **IPropertyFilter** interface has these properties.</span></span>



| <span data-ttu-id="39181-115">Propriedade</span><span class="sxs-lookup"><span data-stu-id="39181-115">Property</span></span>                                                                                      | <span data-ttu-id="39181-116">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="39181-116">Access type</span></span>           | <span data-ttu-id="39181-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="39181-117">Description</span></span>                                                   |
|:----------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="39181-118">**IPropertyFilter::IndexColumn**</span><span class="sxs-lookup"><span data-stu-id="39181-118">**IPropertyFilter::IndexColumn**</span></span>](-search-2x-ipropertyfilter-indexcolumn.md)<br/>     | <span data-ttu-id="39181-119">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="39181-119">Read/write</span></span><br/> | <span data-ttu-id="39181-120">Nome da coluna indexada da propriedade pela qual filtrar.</span><span class="sxs-lookup"><span data-stu-id="39181-120">Indexed column name of the property to filter by.</span></span> <br/> |
| [<span data-ttu-id="39181-121">**IPropertyFilter::LogicOperator**</span><span class="sxs-lookup"><span data-stu-id="39181-121">**IPropertyFilter::LogicOperator**</span></span>](-search-2x-ipropertyfilter-logicoperator.md)<br/> | <span data-ttu-id="39181-122">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="39181-122">Read/write</span></span><br/> | <span data-ttu-id="39181-123">Operador lógico a ser usado ao aplicar o filtro.</span><span class="sxs-lookup"><span data-stu-id="39181-123">Logic Operator to use when applying filter.</span></span> <br/>       |
| [<span data-ttu-id="39181-124">**IPropertyFilter::NestingDepth**</span><span class="sxs-lookup"><span data-stu-id="39181-124">**IPropertyFilter::NestingDepth**</span></span>](-search-2x-ipropertyfilter-nestingdepth.md)<br/>   | <span data-ttu-id="39181-125">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="39181-125">Read/write</span></span><br/> | <span data-ttu-id="39181-126">Profundidade de filtros em um conjunto aninhado de parênteses.</span><span class="sxs-lookup"><span data-stu-id="39181-126">Filters depth within a nested set of parentheses.</span></span> <br/> |
| [<span data-ttu-id="39181-127">**IPropertyFilter:: texto**</span><span class="sxs-lookup"><span data-stu-id="39181-127">**IPropertyFilter::Text**</span></span>](-search-2x-ipropertyfilter-text.md)<br/>                   | <span data-ttu-id="39181-128">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="39181-128">Read/write</span></span><br/> | <span data-ttu-id="39181-129">Texto do filtro.</span><span class="sxs-lookup"><span data-stu-id="39181-129">Text of the filter.</span></span> <br/>                               |
| [<span data-ttu-id="39181-130">**IPropertyFilter:: UID**</span><span class="sxs-lookup"><span data-stu-id="39181-130">**IPropertyFilter::UID**</span></span>](-search-2x-ipropertyfilter-uid.md)<br/>                     | <span data-ttu-id="39181-131">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="39181-131">Read/write</span></span><br/> | <span data-ttu-id="39181-132">UID da propriedade pela qual filtrar.</span><span class="sxs-lookup"><span data-stu-id="39181-132">UID fo the property to filter by.</span></span> <br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="39181-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="39181-133">Remarks</span></span>

<span data-ttu-id="39181-134">Essas propriedades são usadas para filtrar a consulta.</span><span class="sxs-lookup"><span data-stu-id="39181-134">These properties are used to filter the query.</span></span>

## <a name="requirements"></a><span data-ttu-id="39181-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39181-135">Requirements</span></span>



| <span data-ttu-id="39181-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="39181-136">Requirement</span></span> | <span data-ttu-id="39181-137">Valor</span><span class="sxs-lookup"><span data-stu-id="39181-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="39181-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39181-138">Minimum supported client</span></span><br/> | <span data-ttu-id="39181-139">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="39181-139">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="39181-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39181-140">Minimum supported server</span></span><br/> | <span data-ttu-id="39181-141">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="39181-141">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="39181-142">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="39181-142">Redistributable</span></span><br/>          | <span data-ttu-id="39181-143">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="39181-143">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="39181-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="39181-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="39181-145"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="39181-145"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

