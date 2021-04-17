---
title: Estrutura de CD3DX12_HEAP_DESC (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura desc de heap D3D12 \_ .
ms.assetid: 38E0BA60-2BB0-4AC1-870A-10AB16E4C6E6
keywords:
- Estrutura de CD3DX12_HEAP_DESC
topic_type:
- apiref
api_name:
- CD3DX12_HEAP_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5b2537d2571355f26c46f03aed3489fb2b6069
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762334"
---
# <a name="cd3dx12_heap_desc-structure"></a><span data-ttu-id="5f40d-104">\_Estrutura desc de heap CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="5f40d-104">CD3DX12\_HEAP\_DESC structure</span></span>

<span data-ttu-id="5f40d-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ \_ desc de heap D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) .</span><span class="sxs-lookup"><span data-stu-id="5f40d-105">A helper structure to enable easy initialization of a [**D3D12\_HEAP\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f40d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f40d-106">Syntax</span></span>


```C++
struct CD3DX12_HEAP_DESC  : public D3D12_HEAP_DESC{
   CD3DX12_HEAP_DESC();
   explicit CD3DX12_HEAP_DESC(const D3D12_HEAP_DESC &o);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_HEAP_PROPERTIES properties, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_HEAP_TYPE type, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_HEAP_PROPERTIES properties, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_HEAP_TYPE type, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   operator const D3D12_HEAP_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="5f40d-107">Membros</span><span class="sxs-lookup"><span data-stu-id="5f40d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5f40d-108">**CD3DX12 \_ \_ de heap DESC ()**</span><span class="sxs-lookup"><span data-stu-id="5f40d-108">**CD3DX12\_HEAP\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="5f40d-109">Cria uma nova instância, não inicializada, de um CD3DX12 de \_ heap \_ desc.</span><span class="sxs-lookup"><span data-stu-id="5f40d-109">Creates a new, uninitialized, instance of a CD3DX12\_HEAP\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="5f40d-110">**heap CD3DX12 \_ explícito \_ DESC (const D3D12 \_ heap \_ desc &o)**</span><span class="sxs-lookup"><span data-stu-id="5f40d-110">**explicit CD3DX12\_HEAP\_DESC(const D3D12\_HEAP\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="5f40d-111">Cria uma nova instância de um \_ heap CD3DX12 \_ DESC, inicializada com o conteúdo de outra estrutura [**\_ \_ desc de heap D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) .</span><span class="sxs-lookup"><span data-stu-id="5f40d-111">Creates a new instance of a CD3DX12\_HEAP\_DESC, initialized with the contents of another [**D3D12\_HEAP\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5f40d-112">**CD3DX12 \_ heap \_ DESC (tamanho UInt64, propriedades de heap de D3D12 \_ \_ , alinhamento de UINT64 = 0, D3D12 sinalizadores de \_ heap sinalizadores \_ = D3D12 \_ heap \_ Flag \_ nenhum)**</span><span class="sxs-lookup"><span data-stu-id="5f40d-112">**CD3DX12\_HEAP\_DESC(UINT64 size, D3D12\_HEAP\_PROPERTIES properties, UINT64 alignment = 0, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="5f40d-113">Cria uma nova instância de um \_ heap CD3DX12 \_ DESC, inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="5f40d-113">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="5f40d-114">Tamanho de UINT64</span><span class="sxs-lookup"><span data-stu-id="5f40d-114">UINT64 size</span></span>

<span data-ttu-id="5f40d-115">[**D3D12 \_ Propriedades de \_ Propriedades do heap**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)</span><span class="sxs-lookup"><span data-stu-id="5f40d-115">[**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) properties</span></span>

<span data-ttu-id="5f40d-116">opt Alinhamento de UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="5f40d-116">(opt) UINT64 alignment = 0</span></span>

<span data-ttu-id="5f40d-117">opt [**D3D12 \_ Sinalizadores de \_ sinalizadores de heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = sinalizador de heap D3D12 \_ \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="5f40d-117">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="5f40d-118">**CD3DX12 \_ heap \_ DESC (tamanho UInt64, \_ \_ tipo de heap D3D12, alinhamento de UInt64 = 0, sinalizadores de \_ sinalizadores de heap D3D12 \_ = sinalizador de heap de D3D12 \_ \_ \_ nenhum)**</span><span class="sxs-lookup"><span data-stu-id="5f40d-118">**CD3DX12\_HEAP\_DESC(UINT64 size, D3D12\_HEAP\_TYPE type, UINT64 alignment = 0, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="5f40d-119">Cria uma nova instância de um \_ heap CD3DX12 \_ DESC, inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="5f40d-119">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="5f40d-120">Tamanho de UINT64</span><span class="sxs-lookup"><span data-stu-id="5f40d-120">UINT64 size</span></span>

<span data-ttu-id="5f40d-121">[**D3D12 \_ Tipo de \_ tipo de heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)</span><span class="sxs-lookup"><span data-stu-id="5f40d-121">[**D3D12\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) type</span></span>

<span data-ttu-id="5f40d-122">opt Alinhamento de UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="5f40d-122">(opt) UINT64 alignment = 0</span></span>

<span data-ttu-id="5f40d-123">opt [**D3D12 \_ Sinalizadores de \_ sinalizadores de heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = sinalizador de heap D3D12 \_ \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="5f40d-123">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="5f40d-124">**CD3DX12 \_ heap \_ DESC (tamanho de UInt64, \_ propriedade de página de CPU D3D12 \_ \_ cpuPageProperty, D3D12 de \_ \_ pool de memória memoryPoolPreference, alinhamento de UINT64 = 0, sinalizadores de \_ sinalizadores de heap D3D12 \_ = sinalizador de heap D3D12 \_ \_ \_ nenhum)**</span><span class="sxs-lookup"><span data-stu-id="5f40d-124">**CD3DX12\_HEAP\_DESC(UINT64 size, D3D12\_CPU\_PAGE\_PROPERTY cpuPageProperty, D3D12\_MEMORY\_POOL memoryPoolPreference, UINT64 alignment = 0, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="5f40d-125">Cria uma nova instância de um \_ heap CD3DX12 \_ DESC, inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="5f40d-125">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="5f40d-126">Tamanho de UINT64</span><span class="sxs-lookup"><span data-stu-id="5f40d-126">UINT64 size</span></span>

<span data-ttu-id="5f40d-127">[**D3D12 \_ \_ \_ Propriedade da página da CPU**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span><span class="sxs-lookup"><span data-stu-id="5f40d-127">[**D3D12\_CPU\_PAGE\_PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span></span>

<span data-ttu-id="5f40d-128">[**D3D12 \_ MemoryPoolPreference do \_ pool de memória**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool)</span><span class="sxs-lookup"><span data-stu-id="5f40d-128">[**D3D12\_MEMORY\_POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference</span></span>

<span data-ttu-id="5f40d-129">opt Alinhamento de UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="5f40d-129">(opt) UINT64 alignment = 0</span></span>

<span data-ttu-id="5f40d-130">opt [**D3D12 \_ Sinalizadores de \_ sinalizadores de heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = sinalizador de heap D3D12 \_ \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="5f40d-130">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="5f40d-131">**CD3DX12 \_ heap \_ DESC (const D3D12 \_ \_ informações de alocação de recursos \_& resAllocInfo, D3D12 \_ heap propriedades propriedades \_ , sinalizadores de heap de D3D12 \_ \_ flags = D3D12 \_ sinalizador de heap \_ \_ nenhum)**</span><span class="sxs-lookup"><span data-stu-id="5f40d-131">**CD3DX12\_HEAP\_DESC(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_HEAP\_PROPERTIES properties, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="5f40d-132">Cria uma nova instância de um \_ heap CD3DX12 \_ DESC, inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="5f40d-132">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="5f40d-133">[**D3D12 \_ \_ \_ Informações de alocação de recursos**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span><span class="sxs-lookup"><span data-stu-id="5f40d-133">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="5f40d-134">[**D3D12 \_ Propriedades de \_ Propriedades do heap**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)</span><span class="sxs-lookup"><span data-stu-id="5f40d-134">[**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) properties</span></span>

<span data-ttu-id="5f40d-135">opt [**D3D12 \_ Sinalizadores de \_ sinalizadores de heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = sinalizador de heap D3D12 \_ \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="5f40d-135">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="5f40d-136">**CD3DX12 \_ heap \_ DESC (const D3D12 \_ \_ informações de alocação de recursos \_& resAllocInfo, D3D12 \_ \_ tipo de heap, \_ sinalizadores de heap D3D12 \_ flags = \_ sinalizador de heap D3D12 \_ \_ nenhum)**</span><span class="sxs-lookup"><span data-stu-id="5f40d-136">**CD3DX12\_HEAP\_DESC(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_HEAP\_TYPE type, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="5f40d-137">Cria uma nova instância de um \_ heap CD3DX12 \_ DESC, inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="5f40d-137">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="5f40d-138">[**D3D12 \_ \_ \_ Informações de alocação de recursos**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span><span class="sxs-lookup"><span data-stu-id="5f40d-138">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="5f40d-139">[**D3D12 \_ Tipo de \_ tipo de heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)</span><span class="sxs-lookup"><span data-stu-id="5f40d-139">[**D3D12\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) type</span></span>

<span data-ttu-id="5f40d-140">opt [**D3D12 \_ Sinalizadores de \_ sinalizadores de heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = sinalizador de heap D3D12 \_ \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="5f40d-140">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="5f40d-141">**CD3DX12 \_ heap \_ DESC (const D3D12 \_ \_ informações de alocação de recursos \_& resAllocInfo, D3D12 \_ CPU \_ Page \_ Property CPUPAGEPROPERTY, D3D12 \_ \_ pool de memória memoryPoolPreference, D3D12 \_ heap \_ flags flags = D3D12 \_ \_ sinalizador heap \_ None)**</span><span class="sxs-lookup"><span data-stu-id="5f40d-141">**CD3DX12\_HEAP\_DESC(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_CPU\_PAGE\_PROPERTY cpuPageProperty, D3D12\_MEMORY\_POOL memoryPoolPreference, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="5f40d-142">Cria uma nova instância de um \_ heap CD3DX12 \_ DESC, inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="5f40d-142">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="5f40d-143">[**D3D12 \_ \_ \_ Informações de alocação de recursos**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span><span class="sxs-lookup"><span data-stu-id="5f40d-143">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="5f40d-144">[**D3D12 \_ \_ \_ Propriedade da página da CPU**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span><span class="sxs-lookup"><span data-stu-id="5f40d-144">[**D3D12\_CPU\_PAGE\_PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span></span>

<span data-ttu-id="5f40d-145">[**D3D12 \_ MemoryPoolPreference do \_ pool de memória**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool)</span><span class="sxs-lookup"><span data-stu-id="5f40d-145">[**D3D12\_MEMORY\_POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference</span></span>

<span data-ttu-id="5f40d-146">opt [**D3D12 \_ Sinalizadores de \_ sinalizadores de heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = sinalizador de heap D3D12 \_ \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="5f40d-146">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="5f40d-147">**const do operador const D3D12 \_ \_ de HEAP desc& () constante**</span><span class="sxs-lookup"><span data-stu-id="5f40d-147">**operator const D3D12\_HEAP\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="5f40d-148">Define o & operador de passagem por referência para o tipo de \_ estrutura desc de heap CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="5f40d-148">Defines the & pass-by-reference operator for the CD3DX12\_HEAP\_DESC structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f40d-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f40d-149">Requirements</span></span>



| <span data-ttu-id="5f40d-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f40d-150">Requirement</span></span> | <span data-ttu-id="5f40d-151">Valor</span><span class="sxs-lookup"><span data-stu-id="5f40d-151">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5f40d-152">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f40d-152">Header</span></span><br/> | <dl> <span data-ttu-id="5f40d-153"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f40d-153"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f40d-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f40d-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f40d-155">**D3D12 de \_ heap \_ desc**</span><span class="sxs-lookup"><span data-stu-id="5f40d-155">**D3D12\_HEAP\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc)
</dt> <dt>

[<span data-ttu-id="5f40d-156">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="5f40d-156">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





