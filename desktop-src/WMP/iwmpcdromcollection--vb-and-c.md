---
title: Interface IWMPCdromCollection (VB e C) (WMP. h)
description: Fornece uma maneira de organizar e acessar uma coleção de unidades de CD ou DVD. A interface IWMPCdromCollection expõe a propriedade a seguir.
ms.assetid: 60874603-d9c8-4ed1-a92a-bd069bd0c253
keywords:
- IWMPCdromCollection (VB e C) interface do Windows Media Player
- IWMPCdromCollection (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPCdromCollection (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d3fbc9c053c186b6d542e201f7bee5d2331b649
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788155"
---
# <a name="iwmpcdromcollection-vb-and-c-interface"></a><span data-ttu-id="c39f9-105">Interface IWMPCdromCollection (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="c39f9-105">IWMPCdromCollection (VB and C#) interface</span></span>

<span data-ttu-id="c39f9-106">Fornece uma maneira de organizar e acessar uma coleção de unidades de CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="c39f9-106">Provides a way to organize and access a collection of CD or DVD drives.</span></span>

<span data-ttu-id="c39f9-107">A interface **IWMPCdromCollection** expõe a propriedade a seguir.</span><span class="sxs-lookup"><span data-stu-id="c39f9-107">The **IWMPCdromCollection** interface exposes the following property.</span></span>

## <a name="members"></a><span data-ttu-id="c39f9-108">Membros</span><span class="sxs-lookup"><span data-stu-id="c39f9-108">Members</span></span>

<span data-ttu-id="c39f9-109">A interface **IWMPCdromCollection (VB e C#)** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c39f9-109">The **IWMPCdromCollection (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="c39f9-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="c39f9-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="c39f9-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c39f9-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c39f9-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="c39f9-112">Methods</span></span>

<span data-ttu-id="c39f9-113">A interface **IWMPCdromCollection (VB e C#)** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c39f9-113">The **IWMPCdromCollection (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="c39f9-114">Método</span><span class="sxs-lookup"><span data-stu-id="c39f9-114">Method</span></span>                                                                                                     | <span data-ttu-id="c39f9-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="c39f9-115">Description</span></span>                                                                              |
|:-----------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="c39f9-116">**getByDriveSpecifier**</span><span class="sxs-lookup"><span data-stu-id="c39f9-116">**getByDriveSpecifier**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-getbydrivespecifier--vb-and-c.md) | <span data-ttu-id="c39f9-117">Retorna uma interface **IWMPCdrom** associada a uma letra de unidade específica.</span><span class="sxs-lookup"><span data-stu-id="c39f9-117">Returns an **IWMPCdrom** interface associated with a particular drive letter.</span></span><br/> |
| [<span data-ttu-id="c39f9-118">**Item**</span><span class="sxs-lookup"><span data-stu-id="c39f9-118">**Item**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-item--vb-and-c.md)                               | <span data-ttu-id="c39f9-119">Retorna uma interface **IWMPCdrom** no índice fornecido.</span><span class="sxs-lookup"><span data-stu-id="c39f9-119">Returns an **IWMPCdrom** interface at the given index.</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="c39f9-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c39f9-120">Properties</span></span>

<span data-ttu-id="c39f9-121">A interface **IWMPCdromCollection (VB e C#)** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c39f9-121">The **IWMPCdromCollection (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="c39f9-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c39f9-122">Property</span></span>                                                                                  | <span data-ttu-id="c39f9-123">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="c39f9-123">Access type</span></span>          | <span data-ttu-id="c39f9-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="c39f9-124">Description</span></span>                                                              |
|:------------------------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="c39f9-125">**count**</span><span class="sxs-lookup"><span data-stu-id="c39f9-125">**count**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)<br/> | <span data-ttu-id="c39f9-126">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c39f9-126">Read-only</span></span><br/> | <span data-ttu-id="c39f9-127">Obtém o número de unidades de CD e DVD disponíveis no sistema.</span><span class="sxs-lookup"><span data-stu-id="c39f9-127">Gets the number of available CD and DVD drives on the system.</span></span><br/> |



 

<span data-ttu-id="c39f9-128">Obtenha uma interface **IWMPCdromCollection** usando a propriedade a seguir.</span><span class="sxs-lookup"><span data-stu-id="c39f9-128">Get an **IWMPCdromCollection** interface by using the following property.</span></span>



| <span data-ttu-id="c39f9-129">Objeto</span><span class="sxs-lookup"><span data-stu-id="c39f9-129">Object</span></span>                                                                   | <span data-ttu-id="c39f9-130">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c39f9-130">Property</span></span>                                                                           |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="c39f9-131">Objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="c39f9-131">AxWindowsMediaPlayer Object</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="c39f9-132">**cdromCollection**</span><span class="sxs-lookup"><span data-stu-id="c39f9-132">**cdromCollection**</span></span>](axwmplib-axwindowsmediaplayer-cdromcollection--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="c39f9-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c39f9-133">Requirements</span></span>



| <span data-ttu-id="c39f9-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c39f9-134">Requirement</span></span> | <span data-ttu-id="c39f9-135">Valor</span><span class="sxs-lookup"><span data-stu-id="c39f9-135">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c39f9-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c39f9-136">Header</span></span><br/> | <dl> <span data-ttu-id="c39f9-137"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="c39f9-137"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c39f9-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="c39f9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c39f9-139">**Interfaces para Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="c39f9-139">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="c39f9-140">**Interface IWMPCdrom (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c39f9-140">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> </dl>

 

 





