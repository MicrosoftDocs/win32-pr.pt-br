---
title: Interface IResultType (WdsSharedIDL. h)
description: Expõe informações de tipo de propriedade.
ms.assetid: 68abd470-2505-4836-a17f-f1c14157f8e7
keywords:
- Recursos do ambiente Windows herdado da interface IResultType
- Recursos do ambiente Windows herdado da interface IResultType, descritos
topic_type:
- apiref
api_name:
- IResultType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88451739a6ca2eb600838ea137ebc1ddba98f3a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454950"
---
# <a name="iresulttype-interface"></a><span data-ttu-id="fbc3e-105">Interface IResultType</span><span class="sxs-lookup"><span data-stu-id="fbc3e-105">IResultType interface</span></span>

> [!NOTE]
> <span data-ttu-id="fbc3e-106">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fbc3e-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="fbc3e-107">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="fbc3e-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="fbc3e-108">Expõe informações de tipo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="fbc3e-108">Exposes property type information.</span></span>

## <a name="members"></a><span data-ttu-id="fbc3e-109">Membros</span><span class="sxs-lookup"><span data-stu-id="fbc3e-109">Members</span></span>

<span data-ttu-id="fbc3e-110">A interface **IResultType** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="fbc3e-110">The **IResultType** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fbc3e-111">**IResultType** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fbc3e-111">**IResultType** also has these types of members:</span></span>

-   [<span data-ttu-id="fbc3e-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fbc3e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fbc3e-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fbc3e-113">Properties</span></span>

<span data-ttu-id="fbc3e-114">A interface **IResultType** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fbc3e-114">The **IResultType** interface has these properties.</span></span>



| <span data-ttu-id="fbc3e-115">Propriedade</span><span class="sxs-lookup"><span data-stu-id="fbc3e-115">Property</span></span>                                                                 | <span data-ttu-id="fbc3e-116">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="fbc3e-116">Access type</span></span>           | <span data-ttu-id="fbc3e-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="fbc3e-117">Description</span></span>                                                                           |
|:-------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="fbc3e-118">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="fbc3e-118">**DisplayName**</span></span>](-search-2x-iresulttype-displayname.md)<br/>     | <span data-ttu-id="fbc3e-119">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbc3e-119">Read-only</span></span><br/>  | <span data-ttu-id="fbc3e-120">Nome de exibição localizado do tipo:</span><span class="sxs-lookup"><span data-stu-id="fbc3e-120">Localized display name of the type:</span></span><br/>                                        |
| [<span data-ttu-id="fbc3e-121">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="fbc3e-121">**GetProperty**</span></span>](-search-2x-iresulttype-getproperty.md)<br/>     | <span data-ttu-id="fbc3e-122">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fbc3e-122">Read/write</span></span><br/> | <span data-ttu-id="fbc3e-123">Esta propriedade contém informações de propriedade especificadas.</span><span class="sxs-lookup"><span data-stu-id="fbc3e-123">This property contains specified property information.</span></span> <br/>                    |
| [<span data-ttu-id="fbc3e-124">**PreceivedType**</span><span class="sxs-lookup"><span data-stu-id="fbc3e-124">**PreceivedType**</span></span>](-search-2x-iresulttype-preceivedtype.md)<br/> | <span data-ttu-id="fbc3e-125">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbc3e-125">Read-only</span></span><br/>  | <span data-ttu-id="fbc3e-126">Essa propriedade contém a cadeia de caracteres usada para identificar o tipo no índice.</span><span class="sxs-lookup"><span data-stu-id="fbc3e-126">This property contains the string used to identify the type in the index.</span></span> <br/> |
| [<span data-ttu-id="fbc3e-127">**PropertyCount**</span><span class="sxs-lookup"><span data-stu-id="fbc3e-127">**PropertyCount**</span></span>](-search-2x-iresulttype-propertycount.md)<br/> | <span data-ttu-id="fbc3e-128">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbc3e-128">Read-only</span></span><br/>  | <span data-ttu-id="fbc3e-129">Essa propriedade contém o número de propriedades expostas pelo tipo.</span><span class="sxs-lookup"><span data-stu-id="fbc3e-129">This property contains the number of properties exposed by the type.</span></span> <br/>      |
| [<span data-ttu-id="fbc3e-130">**UID**</span><span class="sxs-lookup"><span data-stu-id="fbc3e-130">**UID**</span></span>](-search-2x-iresulttype-uid.md)<br/>                     | <span data-ttu-id="fbc3e-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbc3e-131">Read-only</span></span><br/>  | <span data-ttu-id="fbc3e-132">Essa propriedade contém o identificador exclusivo para o tipo.</span><span class="sxs-lookup"><span data-stu-id="fbc3e-132">This property contains the unique identifier for the type.</span></span> <br/>                |



 

## <a name="remarks"></a><span data-ttu-id="fbc3e-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbc3e-133">Remarks</span></span>

<span data-ttu-id="fbc3e-134">Esses métodos expõem os tipos de informações retornados.</span><span class="sxs-lookup"><span data-stu-id="fbc3e-134">These methods expose the types of information returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbc3e-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbc3e-135">Requirements</span></span>



| <span data-ttu-id="fbc3e-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbc3e-136">Requirement</span></span> | <span data-ttu-id="fbc3e-137">Valor</span><span class="sxs-lookup"><span data-stu-id="fbc3e-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbc3e-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbc3e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="fbc3e-139">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="fbc3e-139">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="fbc3e-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbc3e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="fbc3e-141">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="fbc3e-141">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fbc3e-142">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="fbc3e-142">Redistributable</span></span><br/>          | <span data-ttu-id="fbc3e-143">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="fbc3e-143">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="fbc3e-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fbc3e-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbc3e-145"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbc3e-145"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

