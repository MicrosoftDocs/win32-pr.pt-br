---
title: Interface IWMPCdrom (VB e C) (WMP. h)
description: Fornece uma maneira de acessar um CD ou DVD em sua unidade. A interface IWMPCdrom expõe as propriedades a seguir.
ms.assetid: 2748e64b-b9b7-489a-a6b5-21154aabd312
keywords:
- IWMPCdrom (VB e C) interface do Windows Media Player
- IWMPCdrom (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPCdrom (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 036411c96b278023d87c37ad48f81e986b9dadcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782986"
---
# <a name="iwmpcdrom-vb-and-c-interface"></a><span data-ttu-id="57982-105">Interface IWMPCdrom (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="57982-105">IWMPCdrom (VB and C#) interface</span></span>

<span data-ttu-id="57982-106">Fornece uma maneira de acessar um CD ou DVD em sua unidade.</span><span class="sxs-lookup"><span data-stu-id="57982-106">Provides a way to access a CD or DVD in its drive.</span></span>

<span data-ttu-id="57982-107">A interface **IWMPCdrom** expõe as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="57982-107">The **IWMPCdrom** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="57982-108">Membros</span><span class="sxs-lookup"><span data-stu-id="57982-108">Members</span></span>

<span data-ttu-id="57982-109">A interface **IWMPCdrom (VB e C#)** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="57982-109">The **IWMPCdrom (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="57982-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="57982-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="57982-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="57982-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="57982-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="57982-112">Methods</span></span>

<span data-ttu-id="57982-113">A interface **IWMPCdrom (VB e C#)** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="57982-113">The **IWMPCdrom (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="57982-114">Método</span><span class="sxs-lookup"><span data-stu-id="57982-114">Method</span></span>                                                     | <span data-ttu-id="57982-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="57982-115">Description</span></span>                                     |
|:-----------------------------------------------------------|:------------------------------------------------|
| [<span data-ttu-id="57982-116">**ejeção**</span><span class="sxs-lookup"><span data-stu-id="57982-116">**eject**</span></span>](wmplibiwmpcdrom-iwmpcdrom-eject--vb-and-c.md) | <span data-ttu-id="57982-117">Ejeta o CD ou DVD da unidade.</span><span class="sxs-lookup"><span data-stu-id="57982-117">Ejects the CD or DVD from the drive.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="57982-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="57982-118">Properties</span></span>

<span data-ttu-id="57982-119">A interface **IWMPCdrom (VB e C#)** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="57982-119">The **IWMPCdrom (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="57982-120">Propriedade</span><span class="sxs-lookup"><span data-stu-id="57982-120">Property</span></span>                                                                                | <span data-ttu-id="57982-121">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="57982-121">Access type</span></span>          | <span data-ttu-id="57982-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="57982-122">Description</span></span>                                                                                                                                  |
|:----------------------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57982-123">**driveSpecifier**</span><span class="sxs-lookup"><span data-stu-id="57982-123">**driveSpecifier**</span></span>](wmplibiwmpcdrom-iwmpcdrom-drivespecifier--vb-and-c.md)<br/> | <span data-ttu-id="57982-124">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57982-124">Read-only</span></span><br/> | <span data-ttu-id="57982-125">Obtém a letra da unidade de CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="57982-125">Gets the CD or DVD drive letter.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="57982-126">**7.1**</span><span class="sxs-lookup"><span data-stu-id="57982-126">**Playlist**</span></span>](wmplibiwmpcdrom-iwmpcdrom-playlist--vb-and-c.md)<br/>             | <span data-ttu-id="57982-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57982-127">Read-only</span></span><br/> | <span data-ttu-id="57982-128">Obtém uma interface [**IWMPPlaylist**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) que representa as faixas em um CD ou as entradas de título no nível raiz de um DVD.</span><span class="sxs-lookup"><span data-stu-id="57982-128">Gets an [**IWMPPlaylist**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) interface representing the tracks on a CD or the root-level title entries for a DVD.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="57982-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57982-129">Requirements</span></span>



| <span data-ttu-id="57982-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="57982-130">Requirement</span></span> | <span data-ttu-id="57982-131">Valor</span><span class="sxs-lookup"><span data-stu-id="57982-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="57982-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="57982-132">Header</span></span><br/> | <dl> <span data-ttu-id="57982-133"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="57982-133"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57982-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="57982-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57982-135">**Interfaces para Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="57982-135">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="57982-136">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="57982-136">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





