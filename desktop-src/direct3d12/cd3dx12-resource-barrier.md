---
title: Estrutura de CD3DX12_RESOURCE_BARRIER (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de barreira de recursos D3D12 \_ .
ms.assetid: 89E0F38C-8802-46E6-9583-95C5D853CD99
keywords:
- Estrutura de CD3DX12_RESOURCE_BARRIER
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_BARRIER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eaa9b19a8bc7dcebba5982313bb362dbcee6157
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105788612"
---
# <a name="cd3dx12_resource_barrier-structure"></a><span data-ttu-id="ca5f8-104">Estrutura de barreira de \_ recursos CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="ca5f8-104">CD3DX12\_RESOURCE\_BARRIER structure</span></span>

<span data-ttu-id="ca5f8-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ barreira de recursos D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier) .</span><span class="sxs-lookup"><span data-stu-id="ca5f8-105">A helper structure to enable easy initialization of a [**D3D12\_RESOURCE\_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca5f8-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca5f8-106">Syntax</span></span>


```C++
struct CD3DX12_RESOURCE_BARRIER  : public D3D12_RESOURCE_BARRIER{
                           CD3DX12_RESOURCE_BARRIER();
                           explicit CD3DX12_RESOURCE_BARRIER(const D3D12_RESOURCE_BARRIER &o);
  CD3DX12_RESOURCE_BARRIER static inline Transition(ID3D12Resource* pResource, D3D12_RESOURCE_STATES stateBefore, D3D12_RESOURCE_STATES stateAfter, UINT subresource = D3D12_RESOURCE_BARRIER_ALL_SUBRESOURCES, D3D12_RESOURCE_BARRIER_FLAGS flags = D3D12_RESOURCE_BARRIER_FLAG_NONE);
  CD3DX12_RESOURCE_BARRIER static inline Aliasing(ID3D12Resource* pResourceBefore, ID3D12Resource* pResourceAfter);
  CD3DX12_RESOURCE_BARRIER static inline UAV(ID3D12Resource* pResource);
                           operator const D3D12_RESOURCE_BARRIER&() const;
};
```



## <a name="members"></a><span data-ttu-id="ca5f8-107">Membros</span><span class="sxs-lookup"><span data-stu-id="ca5f8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ca5f8-108">**\_ \_ Barreira de recurso CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="ca5f8-108">**CD3DX12\_RESOURCE\_BARRIER()**</span></span>
</dt> <dd>

<span data-ttu-id="ca5f8-109">Cria uma nova instância, não inicializada, de uma \_ barreira de recurso CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="ca5f8-109">Creates a new, uninitialized, instance of a CD3DX12\_RESOURCE\_BARRIER.</span></span>

</dd> <dt>

<span data-ttu-id="ca5f8-110">**\_ \_ barreira de recurso de CD3DX12 explícita ( \_ barreira de recurso D3D12 const \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="ca5f8-110">**explicit CD3DX12\_RESOURCE\_BARRIER(const D3D12\_RESOURCE\_BARRIER &o)**</span></span>
</dt> <dd>

<span data-ttu-id="ca5f8-111">Cria uma nova instância de uma \_ barreira de recurso CD3DX12 \_ , inicializada com o conteúdo de outra [**\_ \_ barreira de recurso D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier).</span><span class="sxs-lookup"><span data-stu-id="ca5f8-111">Creates a new instance of a CD3DX12\_RESOURCE\_BARRIER, initialized with the contents of another [**D3D12\_RESOURCE\_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier).</span></span>

</dd> <dt>

<span data-ttu-id="ca5f8-112">**Transição embutida estática (ID3D12Resource de \* origem, D3D12 de \_ recursos do \_ stateBefore, D3D12 de \_ Estados de recursos \_ stateAfter, subresource uint = D3D12 \_ barreira de recursos \_ \_ todos os \_ subrecursos, D3D12 sinalizadores de \_ barreira de recurso \_ \_ sinalizadores = D3D12 \_ sinalizador de barreira de recurso \_ \_ \_ nenhum)**</span><span class="sxs-lookup"><span data-stu-id="ca5f8-112">**static inline Transition(ID3D12Resource\* pResource, D3D12\_RESOURCE\_STATES stateBefore, D3D12\_RESOURCE\_STATES stateAfter, UINT subresource = D3D12\_RESOURCE\_BARRIER\_ALL\_SUBRESOURCES, D3D12\_RESOURCE\_BARRIER\_FLAGS flags = D3D12\_RESOURCE\_BARRIER\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="ca5f8-113">Transições entre os Estados de recursos, usando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="ca5f8-113">Transitions between resource states, using the following parameters:</span></span>

<span data-ttu-id="ca5f8-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* origem</span><span class="sxs-lookup"><span data-stu-id="ca5f8-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResource</span></span>

<span data-ttu-id="ca5f8-115">[**D3D12 \_ StateBefore de \_ Estados de recursos**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)</span><span class="sxs-lookup"><span data-stu-id="ca5f8-115">[**D3D12\_RESOURCE\_STATES**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateBefore</span></span>

<span data-ttu-id="ca5f8-116">[**D3D12 \_ StateAfter de \_ Estados de recursos**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)</span><span class="sxs-lookup"><span data-stu-id="ca5f8-116">[**D3D12\_RESOURCE\_STATES**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateAfter</span></span>

<span data-ttu-id="ca5f8-117">opt Subrecurso UINT = [ **D3D12 de \_ recurso para \_ \_ todos os \_ subrecursos**](constants.md)</span><span class="sxs-lookup"><span data-stu-id="ca5f8-117">(opt) UINT subresource = [**D3D12\_RESOURCE\_BARRIER\_ALL\_SUBRESOURCES**](constants.md)</span></span>

<span data-ttu-id="ca5f8-118">opt [**D3D12 \_ Sinalizadores \_ \_ sinalizadores de barreira de recurso**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags) = sinalizador de barreira de recurso D3D12 \_ \_ \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="ca5f8-118">(opt) [**D3D12\_RESOURCE\_BARRIER\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags) flags = D3D12\_RESOURCE\_BARRIER\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="ca5f8-119">**Alias embutido estático (ID3D12Resource \* pResourceBefore, ID3D12Resource \* pResourceAfter)**</span><span class="sxs-lookup"><span data-stu-id="ca5f8-119">**static inline Aliasing(ID3D12Resource\* pResourceBefore, ID3D12Resource\* pResourceAfter)**</span></span>
</dt> <dd>

<span data-ttu-id="ca5f8-120">Cria aliases para o recurso antes e depois da transição de barreira.</span><span class="sxs-lookup"><span data-stu-id="ca5f8-120">Creates aliases for the resource before and after the barrier transition.</span></span> <span data-ttu-id="ca5f8-121">Parâmetros:</span><span class="sxs-lookup"><span data-stu-id="ca5f8-121">Parameters:</span></span>

<span data-ttu-id="ca5f8-122">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResourceBefore</span><span class="sxs-lookup"><span data-stu-id="ca5f8-122">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResourceBefore</span></span>

<span data-ttu-id="ca5f8-123">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResourceAfter</span><span class="sxs-lookup"><span data-stu-id="ca5f8-123">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResourceAfter</span></span>

</dd> <dt>

<span data-ttu-id="ca5f8-124">**UAV embutido estático ( \* PreSource ID3D12Resource)**</span><span class="sxs-lookup"><span data-stu-id="ca5f8-124">**static inline UAV(ID3D12Resource\* pResource)**</span></span>
</dt> <dd>

<span data-ttu-id="ca5f8-125">Cria um UAV (modo de exibição de acesso não ordenado) para o recurso.</span><span class="sxs-lookup"><span data-stu-id="ca5f8-125">Creates an unordered-access-view (UAV) for the resource.</span></span> <span data-ttu-id="ca5f8-126">Parâmetros:</span><span class="sxs-lookup"><span data-stu-id="ca5f8-126">Parameters:</span></span>

<span data-ttu-id="ca5f8-127">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* origem</span><span class="sxs-lookup"><span data-stu-id="ca5f8-127">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResource</span></span>

</dd> <dt>

<span data-ttu-id="ca5f8-128">**\_const do operador D3D12 \_ de barreira de recurso constante& () constante**</span><span class="sxs-lookup"><span data-stu-id="ca5f8-128">**operator const D3D12\_RESOURCE\_BARRIER&() const**</span></span>
</dt> <dd>

<span data-ttu-id="ca5f8-129">Define o & operador de passagem por referência para o tipo de estrutura pai.</span><span class="sxs-lookup"><span data-stu-id="ca5f8-129">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca5f8-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca5f8-130">Requirements</span></span>



| <span data-ttu-id="ca5f8-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca5f8-131">Requirement</span></span> | <span data-ttu-id="ca5f8-132">Valor</span><span class="sxs-lookup"><span data-stu-id="ca5f8-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ca5f8-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ca5f8-133">Header</span></span><br/> | <dl> <span data-ttu-id="ca5f8-134"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca5f8-134"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca5f8-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca5f8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca5f8-136">**\_Barreira de recurso D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="ca5f8-136">**D3D12\_RESOURCE\_BARRIER**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)
</dt> <dt>

[<span data-ttu-id="ca5f8-137">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="ca5f8-137">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





