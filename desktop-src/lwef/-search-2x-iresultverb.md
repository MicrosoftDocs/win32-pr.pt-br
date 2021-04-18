---
title: Interface IResultVerb (WdsSharedIDL. h)
description: Expõe as propriedades de verbo.
ms.assetid: 8cc8408e-0117-4344-ad26-0c4a5d09a935
keywords:
- Recursos do ambiente Windows herdado da interface IResultVerb
- Recursos do ambiente Windows herdado da interface IResultVerb, descritos
topic_type:
- apiref
api_name:
- IResultVerb
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d922b9e9b3eb93697ed7daf2688001b031db0c92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105781601"
---
# <a name="iresultverb-interface"></a><span data-ttu-id="2f8e0-105">Interface IResultVerb</span><span class="sxs-lookup"><span data-stu-id="2f8e0-105">IResultVerb interface</span></span>

> [!NOTE]
> <span data-ttu-id="2f8e0-106">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2f8e0-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="2f8e0-107">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="2f8e0-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="2f8e0-108">Expõe as propriedades de verbo.</span><span class="sxs-lookup"><span data-stu-id="2f8e0-108">Exposes verb properties.</span></span>

## <a name="members"></a><span data-ttu-id="2f8e0-109">Membros</span><span class="sxs-lookup"><span data-stu-id="2f8e0-109">Members</span></span>

<span data-ttu-id="2f8e0-110">A interface **IResultVerb** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2f8e0-110">The **IResultVerb** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2f8e0-111">**IResultVerb** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2f8e0-111">**IResultVerb** also has these types of members:</span></span>

-   [<span data-ttu-id="2f8e0-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2f8e0-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2f8e0-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2f8e0-113">Properties</span></span>

<span data-ttu-id="2f8e0-114">A interface **IResultVerb** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2f8e0-114">The **IResultVerb** interface has these properties.</span></span>



| <span data-ttu-id="2f8e0-115">Propriedade</span><span class="sxs-lookup"><span data-stu-id="2f8e0-115">Property</span></span>                                                             | <span data-ttu-id="2f8e0-116">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="2f8e0-116">Access type</span></span>           | <span data-ttu-id="2f8e0-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="2f8e0-117">Description</span></span>                                                                                                       |
|:---------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f8e0-118">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="2f8e0-118">**DisplayName**</span></span>](-search-2x-iresultverb-displayname.md)<br/> | <span data-ttu-id="2f8e0-119">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2f8e0-119">Read-only</span></span><br/>  | <span data-ttu-id="2f8e0-120">Essa propriedade retorna um ponteiro para o nome de exibição localizado para o verbo.</span><span class="sxs-lookup"><span data-stu-id="2f8e0-120">This property returns a pointer to the localized display name for the verb.</span></span> <br/>                           |
| [<span data-ttu-id="2f8e0-121">**DoIt**</span><span class="sxs-lookup"><span data-stu-id="2f8e0-121">**DoIt**</span></span>](-search-2x-iresultverb-doit.md)<br/>               | <span data-ttu-id="2f8e0-122">Somente gravação</span><span class="sxs-lookup"><span data-stu-id="2f8e0-122">Write-only</span></span><br/> | <span data-ttu-id="2f8e0-123">Executa o verbo.</span><span class="sxs-lookup"><span data-stu-id="2f8e0-123">Executes the verb.</span></span> <br/>                                                                                    |
| [<span data-ttu-id="2f8e0-124">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="2f8e0-124">**Enabled**</span></span>](-search-2x-iresultverb-enabled.md)<br/>         | <span data-ttu-id="2f8e0-125">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2f8e0-125">Read-only</span></span><br/>  | <span data-ttu-id="2f8e0-126">Essa propriedade retornará TRUE se o verbo estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="2f8e0-126">This property returns TRUE if the verb is enabled.</span></span> <br/>                                                    |
| [<span data-ttu-id="2f8e0-127">**Texto**</span><span class="sxs-lookup"><span data-stu-id="2f8e0-127">**HelpText**</span></span>](-search-2x-iresultverb-helptext.md)<br/>       | <span data-ttu-id="2f8e0-128">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2f8e0-128">Read-only</span></span><br/>  | <span data-ttu-id="2f8e0-129">Essa propriedade retorna um ponteiro para a cadeia de caracteres de ajuda localizada para o verbo.</span><span class="sxs-lookup"><span data-stu-id="2f8e0-129">This property returns a pointer to the localized help string for the verb.</span></span> <br/>                            |
| [<span data-ttu-id="2f8e0-130">**ícone**</span><span class="sxs-lookup"><span data-stu-id="2f8e0-130">**Icon**</span></span>](-search-2x-iresultverb-icon.md)<br/>               | <span data-ttu-id="2f8e0-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2f8e0-131">Read-only</span></span><br/>  | <span data-ttu-id="2f8e0-132">Essa propriedade retorna um ponteiro para o identificador do ícone opcional associado ao verbo.</span><span class="sxs-lookup"><span data-stu-id="2f8e0-132">This property returns a pointer to handle of the optional icon associated with the verb.</span></span> <br/>              |
| [<span data-ttu-id="2f8e0-133">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2f8e0-133">**Name**</span></span>](-search-2x-iresultverb-name.md)<br/>               | <span data-ttu-id="2f8e0-134">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2f8e0-134">Read-only</span></span><br/>  | <span data-ttu-id="2f8e0-135">Essa propriedade retorna um ponteiro para o nome cononical do verbo, como Print, Open e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="2f8e0-135">This property returns a pointer to the cononical name for the verb such as print, open, and so forth.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="2f8e0-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f8e0-136">Remarks</span></span>

<span data-ttu-id="2f8e0-137">Esses métodos expõem propriedades e ações aplicáveis a verbos.</span><span class="sxs-lookup"><span data-stu-id="2f8e0-137">These methods expose properties and actions applicable to verbs.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f8e0-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f8e0-138">Requirements</span></span>



| <span data-ttu-id="2f8e0-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f8e0-139">Requirement</span></span> | <span data-ttu-id="2f8e0-140">Valor</span><span class="sxs-lookup"><span data-stu-id="2f8e0-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f8e0-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f8e0-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2f8e0-142">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="2f8e0-142">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2f8e0-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f8e0-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2f8e0-144">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="2f8e0-144">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2f8e0-145">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="2f8e0-145">Redistributable</span></span><br/>          | <span data-ttu-id="2f8e0-146">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="2f8e0-146">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="2f8e0-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2f8e0-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f8e0-148"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f8e0-148"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

