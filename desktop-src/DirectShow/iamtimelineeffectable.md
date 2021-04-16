---
description: A interface IAMTimelineEffectable fornece métodos para adicionar efeitos a um objeto de linha do tempo nos serviços de edição do DirectShow (DES) e para manipular os efeitos em um objeto.
ms.assetid: 70f2da64-e16a-4d4d-9522-042b5fa2855c
title: Interface IAMTimelineEffectable (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bc67483f44515c2ce18825de5b6657d51e2c3826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779537"
---
# <a name="iamtimelineeffectable-interface"></a><span data-ttu-id="16b00-103">Interface IAMTimelineEffectable</span><span class="sxs-lookup"><span data-stu-id="16b00-103">IAMTimelineEffectable interface</span></span>

> [!Note]  
> <span data-ttu-id="16b00-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="16b00-104">\[Deprecated.</span></span> <span data-ttu-id="16b00-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="16b00-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="16b00-106">A `IAMTimelineEffectable` interface fornece métodos para adicionar efeitos a um objeto de linha do tempo nos [serviços de edição do DirectShow](directshow-editing-services.md) (des) e para manipular os efeitos em um objeto.</span><span class="sxs-lookup"><span data-stu-id="16b00-106">The `IAMTimelineEffectable` interface provides methods for adding effects to a timeline object in [DirectShow Editing Services](directshow-editing-services.md) (DES), and for manipulating the effects on an object.</span></span> <span data-ttu-id="16b00-107">Todos os objetos que podem ter efeitos aplicados a eles implementam essa interface; Isso inclui fontes, faixas e composições.</span><span class="sxs-lookup"><span data-stu-id="16b00-107">All objects that can have effects applied to them implement this interface; this includes sources, tracks, and compositions.</span></span>

<span data-ttu-id="16b00-108">Um objeto que implementa essa interface pode ter qualquer número de efeitos.</span><span class="sxs-lookup"><span data-stu-id="16b00-108">An object that implements this interface can have any number of effects.</span></span> <span data-ttu-id="16b00-109">Para cada objeto, o mecanismo de renderização aplica seus efeitos em ordem de prioridade, começando com o nível de prioridade 0.</span><span class="sxs-lookup"><span data-stu-id="16b00-109">For each object, the render engine applies its effects in order of priority, starting with priority level 0.</span></span>

## <a name="members"></a><span data-ttu-id="16b00-110">Membros</span><span class="sxs-lookup"><span data-stu-id="16b00-110">Members</span></span>

<span data-ttu-id="16b00-111">A interface **IAMTimelineEffectable** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="16b00-111">The **IAMTimelineEffectable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="16b00-112">**IAMTimelineEffectable** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="16b00-112">**IAMTimelineEffectable** also has these types of members:</span></span>

-   [<span data-ttu-id="16b00-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="16b00-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="16b00-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="16b00-114">Methods</span></span>

<span data-ttu-id="16b00-115">A interface **IAMTimelineEffectable** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="16b00-115">The **IAMTimelineEffectable** interface has these methods.</span></span>



| <span data-ttu-id="16b00-116">Método</span><span class="sxs-lookup"><span data-stu-id="16b00-116">Method</span></span>                                                                     | <span data-ttu-id="16b00-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="16b00-117">Description</span></span>                                                                   |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="16b00-118">**EffectGetCount**</span><span class="sxs-lookup"><span data-stu-id="16b00-118">**EffectGetCount**</span></span>](iamtimelineeffectable-effectgetcount.md)             | <span data-ttu-id="16b00-119">Recupera o número de efeitos neste objeto.</span><span class="sxs-lookup"><span data-stu-id="16b00-119">Retrieves the number of effects on this object.</span></span><br/>                    |
| [<span data-ttu-id="16b00-120">**EffectInsBefore**</span><span class="sxs-lookup"><span data-stu-id="16b00-120">**EffectInsBefore**</span></span>](iamtimelineeffectable-effectinsbefore.md)           | <span data-ttu-id="16b00-121">Insere um efeito no objeto no nível de prioridade especificado.</span><span class="sxs-lookup"><span data-stu-id="16b00-121">Inserts an effect into the object at the specified priority level.</span></span><br/> |
| [<span data-ttu-id="16b00-122">**EffectSwapPriorities**</span><span class="sxs-lookup"><span data-stu-id="16b00-122">**EffectSwapPriorities**</span></span>](iamtimelineeffectable-effectswappriorities.md) | <span data-ttu-id="16b00-123">Alterna os níveis de prioridade de dois efeitos.</span><span class="sxs-lookup"><span data-stu-id="16b00-123">Switches the priority levels of two effects.</span></span><br/>                       |
| [<span data-ttu-id="16b00-124">**GetEffect**</span><span class="sxs-lookup"><span data-stu-id="16b00-124">**GetEffect**</span></span>](iamtimelineeffectable-geteffect.md)                       | <span data-ttu-id="16b00-125">Recupera o efeito no nível de prioridade especificado.</span><span class="sxs-lookup"><span data-stu-id="16b00-125">Retrieves the effect at the specified priority level.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="16b00-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="16b00-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="16b00-127">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="16b00-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="16b00-128">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="16b00-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="16b00-129">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="16b00-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="16b00-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16b00-130">Requirements</span></span>



| <span data-ttu-id="16b00-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="16b00-131">Requirement</span></span> | <span data-ttu-id="16b00-132">Valor</span><span class="sxs-lookup"><span data-stu-id="16b00-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16b00-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16b00-133">Header</span></span><br/>  | <dl> <span data-ttu-id="16b00-134"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="16b00-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="16b00-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="16b00-135">Library</span></span><br/> | <dl> <span data-ttu-id="16b00-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16b00-136"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
