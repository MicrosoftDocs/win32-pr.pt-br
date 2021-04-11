---
description: Constantes usadas para definir a prioridade de um recurso em setanteriority.
ms.assetid: 98886349-883f-41c3-870b-e4a639977760
title: D3D9_RESOURCE_PRIORITY (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3D9_RESOURCE_PRIORITY_MINIMUM
- D3D9_RESOURCE_PRIORITY_LOW
- D3D9_RESOURCE_PRIORITY_NORMAL
- D3D9_RESOURCE_PRIORITY_HIGH
- D3D9_RESOURCE_PRIORITY_MAXIMUM
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1ae5a54c7645db63b1023c3571f8181f4ee2daec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172953"
---
# <a name="d3d9_resource_priority"></a><span data-ttu-id="505bb-103">\_Prioridade do recurso d3d9 \_</span><span class="sxs-lookup"><span data-stu-id="505bb-103">D3D9\_RESOURCE\_PRIORITY</span></span>

<span data-ttu-id="505bb-104">Constantes usadas para definir a prioridade de um recurso em [**Setanteriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority).</span><span class="sxs-lookup"><span data-stu-id="505bb-104">Constants used to set the priority of a resource in [**SetPriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority).</span></span>



| <span data-ttu-id="505bb-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="505bb-105">Constant/value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="505bb-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="505bb-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3D9_RESOURCE_PRIORITY_MINIMUM"></span><span id="d3d9_resource_priority_minimum"></span><dl> <span data-ttu-id="505bb-107"><dt>**D3d9 \_ 0x28000000 \_ \_ mínimo de prioridade de recurso**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="505bb-107"><dt>**D3D9\_RESOURCE\_PRIORITY\_MINIMUM**</dt> <dt>0x28000000</dt></span></span> </dl> | <span data-ttu-id="505bb-108">O recurso tem a menor prioridade possível.</span><span class="sxs-lookup"><span data-stu-id="505bb-108">The resource has the lowest priority possible.</span></span> <span data-ttu-id="505bb-109">Essa constante marca o recurso como não usado e para remoção.</span><span class="sxs-lookup"><span data-stu-id="505bb-109">This constant marks the resource as unused and for eviction.</span></span> <span data-ttu-id="505bb-110">O recurso deve ser removido assim que outro recurso exigir o espaço de memória que o recurso ocupa.</span><span class="sxs-lookup"><span data-stu-id="505bb-110">The resource should be evicted as soon as another resource requires the memory space that the resource occupies.</span></span><br/>                                                                                                                                                                                                              |
| <span id="D3D9_RESOURCE_PRIORITY_LOW"></span><span id="d3d9_resource_priority_low"></span><dl> <span data-ttu-id="505bb-111"><dt>**D3d9 \_ Prioridade de recurso \_ \_ baixa**</dt> <dt>0x50000000</dt></span><span class="sxs-lookup"><span data-stu-id="505bb-111"><dt>**D3D9\_RESOURCE\_PRIORITY\_LOW**</dt> <dt>0x50000000</dt></span></span> </dl>             | <span data-ttu-id="505bb-112">O recurso está agendado com baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="505bb-112">The resource is scheduled with low priority.</span></span> <span data-ttu-id="505bb-113">O posicionamento do recurso não é crítico e o sistema operacional executa o mínimo de trabalho para encontrar um local para o recurso.</span><span class="sxs-lookup"><span data-stu-id="505bb-113">The placement of the resource is not critical, and the operating system performs minimal work to find a location for the resource.</span></span> <span data-ttu-id="505bb-114">Marcar um recurso como prioridade baixa permite que outros recursos mais críticos ocupem a memória mais rápida.</span><span class="sxs-lookup"><span data-stu-id="505bb-114">Marking a resource as low priority allows other more critical resources to occupy the faster memory.</span></span><br/>                                                                                                                                                      |
| <span id="D3D9_RESOURCE_PRIORITY_NORMAL"></span><span id="d3d9_resource_priority_normal"></span><dl> <span data-ttu-id="505bb-115"><dt>**D3d9 \_ 0x78000000 \_ \_ normal de prioridade de recurso**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="505bb-115"><dt>**D3D9\_RESOURCE\_PRIORITY\_NORMAL**</dt> <dt>0x78000000</dt></span></span> </dl>    | <span data-ttu-id="505bb-116">O recurso está agendado com prioridade normal.</span><span class="sxs-lookup"><span data-stu-id="505bb-116">The resource is scheduled with normal priority.</span></span> <span data-ttu-id="505bb-117">O posicionamento do recurso é importante para o desempenho, mas não é crítico.</span><span class="sxs-lookup"><span data-stu-id="505bb-117">The placement of the resource is important for performance, but it is not critical.</span></span> <span data-ttu-id="505bb-118">O sistema operacional deve tentar posicionar o recurso que está marcado como normal no local preferido do recurso, em vez de um recurso de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="505bb-118">The operating system should try to place the resource that is marked as normal in the resource's preferred location instead of a low-priority resource.</span></span> <span data-ttu-id="505bb-119">Normalmente, as texturas são marcadas como normais.</span><span class="sxs-lookup"><span data-stu-id="505bb-119">Typically, textures are marked as normal.</span></span><br/>                                                                                                     |
| <span id="D3D9_RESOURCE_PRIORITY_HIGH"></span><span id="d3d9_resource_priority_high"></span><dl> <span data-ttu-id="505bb-120"><dt>**D3d9 \_ Prioridade de recurso \_ \_ alta**</dt> <dt>0xA0000000</dt></span><span class="sxs-lookup"><span data-stu-id="505bb-120"><dt>**D3D9\_RESOURCE\_PRIORITY\_HIGH**</dt> <dt>0xa0000000</dt></span></span> </dl>          | <span data-ttu-id="505bb-121">O recurso está agendado com alta prioridade.</span><span class="sxs-lookup"><span data-stu-id="505bb-121">The resource is scheduled with high priority.</span></span> <span data-ttu-id="505bb-122">O posicionamento do recurso é crítico para o desempenho.</span><span class="sxs-lookup"><span data-stu-id="505bb-122">The placement of the resource is critical for performance.</span></span> <span data-ttu-id="505bb-123">O sistema operacional sempre tenta posicionar o recurso que está marcado como alto no local preferido do recurso, em vez de um recurso de baixa prioridade ou de prioridade normal.</span><span class="sxs-lookup"><span data-stu-id="505bb-123">The operating system always tries to place the resource that is marked as high in the resource's preferred location instead of a low-priority or normal-priority resource.</span></span> <span data-ttu-id="505bb-124">Normalmente, os destinos de renderização são marcados como altos.</span><span class="sxs-lookup"><span data-stu-id="505bb-124">Typically, render targets are marked as high.</span></span><br/>                                                                                                         |
| <span id="D3D9_RESOURCE_PRIORITY_MAXIMUM"></span><span id="d3d9_resource_priority_maximum"></span><dl> <span data-ttu-id="505bb-125"><dt>**D3d9 \_ 0xc8000000 \_ \_ máxima de prioridade de recurso**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="505bb-125"><dt>**D3D9\_RESOURCE\_PRIORITY\_MAXIMUM**</dt> <dt>0xc8000000</dt></span></span> </dl> | <span data-ttu-id="505bb-126">O recurso tem a prioridade máxima possível.</span><span class="sxs-lookup"><span data-stu-id="505bb-126">The resource has the maximum priority possible.</span></span> <span data-ttu-id="505bb-127">Essa constante marca a prioridade do recurso como fixado flexível.</span><span class="sxs-lookup"><span data-stu-id="505bb-127">This constant marks the priority of the resource as soft-pinned.</span></span> <span data-ttu-id="505bb-128">Um recurso fixo por software será removido da memória somente se não houver nenhuma outra maneira de resolver o requisito de memória de um buffer de DMA.</span><span class="sxs-lookup"><span data-stu-id="505bb-128">A soft-pinned resource is evicted from memory only if there is no other way of resolving the memory requirement of a DMA buffer.</span></span> <span data-ttu-id="505bb-129">O sistema operacional tenta dividir um buffer de DMA para seu tamanho mínimo e remover todos os outros recursos que não estão fixados e não são fixados antes de remover um recurso fixado por software.</span><span class="sxs-lookup"><span data-stu-id="505bb-129">The operating system attempts to split a DMA buffer to its minimum size and evict all other resources that are not pinned and not soft-pinned before it evicts a soft-pinned resource.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="505bb-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="505bb-130">Remarks</span></span>

<span data-ttu-id="505bb-131">Valores diferentes de **\_ prioridade de recurso d3d9 \_ \_ mínimo** e máximo de **\_ prioridade de recurso \_ \_ d3d9** são tratados como dicas pelo Agendador.</span><span class="sxs-lookup"><span data-stu-id="505bb-131">Values other than **D3D9\_RESOURCE\_PRIORITY\_MINIMUM** and **D3D9\_RESOURCE\_PRIORITY\_MAXIMUM** are treated as hints by the scheduler.</span></span>

<span data-ttu-id="505bb-132">Você pode usar níveis de prioridade diferentes dos valores definidos anteriormente neste tópico.</span><span class="sxs-lookup"><span data-stu-id="505bb-132">You can use priority levels other than the values defined earlier in this topic.</span></span> <span data-ttu-id="505bb-133">Por exemplo, marcar um recurso com um nível de prioridade de 0x78000001 indica que a prioridade do recurso está um pouco acima do normal.</span><span class="sxs-lookup"><span data-stu-id="505bb-133">For example, marking a resource with a priority level of 0x78000001 indicates that the resource priority is slightly above normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="505bb-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="505bb-134">Requirements</span></span>



| <span data-ttu-id="505bb-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="505bb-135">Requirement</span></span> | <span data-ttu-id="505bb-136">Valor</span><span class="sxs-lookup"><span data-stu-id="505bb-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="505bb-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="505bb-137">Header</span></span><br/> | <dl> <span data-ttu-id="505bb-138"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="505bb-138"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="505bb-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="505bb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="505bb-140">Constantes do Direct3D</span><span class="sxs-lookup"><span data-stu-id="505bb-140">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
