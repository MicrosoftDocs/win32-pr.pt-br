---
title: Estrutura de CD3DX12_HEAP_PROPERTIES (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de propriedades de heap D3D12 \_ .
ms.assetid: AC759F25-D643-412D-AA83-3A2C040BE64B
keywords:
- Estrutura de CD3DX12_HEAP_PROPERTIES
topic_type:
- apiref
api_name:
- CD3DX12_HEAP_PROPERTIES
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90cc5f5cee6bf70aad064396589aad8a483f2c50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105811461"
---
# <a name="cd3dx12_heap_properties-structure"></a><span data-ttu-id="86d5b-104">Estrutura de propriedades do \_ heap CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="86d5b-104">CD3DX12\_HEAP\_PROPERTIES structure</span></span>

<span data-ttu-id="86d5b-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ Propriedades de heap D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) .</span><span class="sxs-lookup"><span data-stu-id="86d5b-105">A helper structure to enable easy initialization of a [**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="86d5b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="86d5b-106">Syntax</span></span>


```C++
struct CD3DX12_HEAP_PROPERTIES  : public D3D12_HEAP_PROPERTIES{
       CD3DX12_HEAP_PROPERTIES();
       explicit CD3DX12_HEAP_PROPERTIES(const D3D12_HEAP_PROPERTIES &o);
       CD3DX12_HEAP_PROPERTIES(D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, UINT creationNodeMask = 1, UINT nodeMask = 1);
       explicit CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE type, UINT creationNodeMask = 1, UINT nodeMask = 1);
       operator const D3D12_HEAP_PROPERTIES&() const;
  bool inline operator==( const D3D12_HEAP_PROPERTIES& l, const D3D12_HEAP_PROPERTIES& r );
  bool inline operator!=( const D3D12_HEAP_PROPERTIES& l, const D3D12_HEAP_PROPERTIES& r );
};
```



## <a name="members"></a><span data-ttu-id="86d5b-107">Membros</span><span class="sxs-lookup"><span data-stu-id="86d5b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="86d5b-108">**\_ \_ Propriedades de heap CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="86d5b-108">**CD3DX12\_HEAP\_PROPERTIES()**</span></span>
</dt> <dd>

<span data-ttu-id="86d5b-109">Cria uma nova instância, não inicializada, de uma CD3DX12 de \_ heap de \_ Propriedades.</span><span class="sxs-lookup"><span data-stu-id="86d5b-109">Creates a new, uninitialized, instance of a CD3DX12\_HEAP\_PROPERTIES.</span></span>

</dd> <dt>

<span data-ttu-id="86d5b-110">**\_Propriedades de heap CD3DX12 explícitas \_ (const D3D12 \_ heap \_ Propriedades &o)**</span><span class="sxs-lookup"><span data-stu-id="86d5b-110">**explicit CD3DX12\_HEAP\_PROPERTIES(const D3D12\_HEAP\_PROPERTIES &o)**</span></span>
</dt> <dd>

<span data-ttu-id="86d5b-111">Cria uma nova instância de uma CD3DX12 \_ heap \_ Propriedades, inicializada com o conteúdo de outra estrutura de [**\_ \_ Propriedades de heap D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) .</span><span class="sxs-lookup"><span data-stu-id="86d5b-111">Creates a new instance of a CD3DX12\_HEAP\_PROPERTIES, initialized with the contents of another [**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) structure.</span></span>

</dd> <dt>

<span data-ttu-id="86d5b-112">**\_ \_ Propriedades de heap CD3DX12 ( \_ propriedade de página de CPU D3D12 \_ \_ cpuPageProperty, D3D12 \_ \_ pool de memória MEMORYPOOLPREFERENCE, uint creationNodeMask = 1, uint nodeMask = 1)**</span><span class="sxs-lookup"><span data-stu-id="86d5b-112">**CD3DX12\_HEAP\_PROPERTIES(D3D12\_CPU\_PAGE\_PROPERTY cpuPageProperty, D3D12\_MEMORY\_POOL memoryPoolPreference, UINT creationNodeMask = 1, UINT nodeMask = 1)**</span></span>
</dt> <dd>

<span data-ttu-id="86d5b-113">Cria uma nova instância de uma CD3DX12 \_ heap \_ Propriedades, inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="86d5b-113">Creates a new instance of a CD3DX12\_HEAP\_PROPERTIES, initializing the following parameters:</span></span>

<span data-ttu-id="86d5b-114">[**D3D12 \_ \_ \_ Propriedade da página da CPU**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span><span class="sxs-lookup"><span data-stu-id="86d5b-114">[**D3D12\_CPU\_PAGE\_PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span></span>

<span data-ttu-id="86d5b-115">[**D3D12 \_ MemoryPoolPreference do \_ pool de memória**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool)</span><span class="sxs-lookup"><span data-stu-id="86d5b-115">[**D3D12\_MEMORY\_POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference</span></span>

<span data-ttu-id="86d5b-116">opt UINT creationNodeMask = 1</span><span class="sxs-lookup"><span data-stu-id="86d5b-116">(opt) UINT creationNodeMask = 1</span></span>

<span data-ttu-id="86d5b-117">opt UINT nodeMask = 1</span><span class="sxs-lookup"><span data-stu-id="86d5b-117">(opt) UINT nodeMask = 1</span></span>

</dd> <dt>

<span data-ttu-id="86d5b-118">**\_Propriedades de heap CD3DX12 explícitas \_ ( \_ \_ tipo de tipo de heap D3D12, uint CREATIONNODEMASK = 1, uint nodeMask = 1)**</span><span class="sxs-lookup"><span data-stu-id="86d5b-118">**explicit CD3DX12\_HEAP\_PROPERTIES(D3D12\_HEAP\_TYPE type, UINT creationNodeMask = 1, UINT nodeMask = 1)**</span></span>
</dt> <dd>

<span data-ttu-id="86d5b-119">Cria uma nova instância de uma CD3DX12 \_ heap \_ Propriedades, inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="86d5b-119">Creates a new instance of a CD3DX12\_HEAP\_PROPERTIES, initializing the following parameters:</span></span>

<span data-ttu-id="86d5b-120">[**D3D12 \_ Tipo de \_ tipo de heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)</span><span class="sxs-lookup"><span data-stu-id="86d5b-120">[**D3D12\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) type</span></span>

<span data-ttu-id="86d5b-121">opt UINT creationNodeMask = 1</span><span class="sxs-lookup"><span data-stu-id="86d5b-121">(opt) UINT creationNodeMask = 1</span></span>

<span data-ttu-id="86d5b-122">opt UINT nodeMask = 1</span><span class="sxs-lookup"><span data-stu-id="86d5b-122">(opt) UINT nodeMask = 1</span></span>

</dd> <dt>

<span data-ttu-id="86d5b-123">**\_const do operador D3D12 \_ de propriedades de heap& () constante**</span><span class="sxs-lookup"><span data-stu-id="86d5b-123">**operator const D3D12\_HEAP\_PROPERTIES&() const**</span></span>
</dt> <dd>

<span data-ttu-id="86d5b-124">Define o & operador de passagem por referência para o tipo de estrutura pai.</span><span class="sxs-lookup"><span data-stu-id="86d5b-124">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> <dt>

<span data-ttu-id="86d5b-125">**operador embutido = = (const D3D12 \_ heap \_ Propriedades& l, const D3D12 \_ heap \_ Propriedades& r)**</span><span class="sxs-lookup"><span data-stu-id="86d5b-125">**inline operator==( const D3D12\_HEAP\_PROPERTIES& l, const D3D12\_HEAP\_PROPERTIES& r )**</span></span>
</dt> <dd>

<span data-ttu-id="86d5b-126">Testes de igualdade entre as instâncias de \_ Propriedades de heap D3D12 especificadas \_ , com base na igualdade de todos os campos de membro.</span><span class="sxs-lookup"><span data-stu-id="86d5b-126">Tests for equality between the specified D3D12\_HEAP\_PROPERTIES instances, based on equality of all member fields.</span></span>

</dd> <dt>

<span data-ttu-id="86d5b-127">**operador embutido! = (const D3D12 \_ heap \_ Propriedades& l, const D3D12 \_ heap \_ Propriedades& r)**</span><span class="sxs-lookup"><span data-stu-id="86d5b-127">**inline operator!=( const D3D12\_HEAP\_PROPERTIES& l, const D3D12\_HEAP\_PROPERTIES& r )**</span></span>
</dt> <dd>

<span data-ttu-id="86d5b-128">Testa a desigualdade entre as instâncias de propriedades de heap D3D12 especificadas \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="86d5b-128">Tests for inequality between the specified D3D12\_HEAP\_PROPERTIES instances.</span></span> <span data-ttu-id="86d5b-129">Implementado ao tirar o inverso do **operador = =** valor.</span><span class="sxs-lookup"><span data-stu-id="86d5b-129">Implemented by taking the inverse of the **operator==** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="86d5b-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86d5b-130">Requirements</span></span>



| <span data-ttu-id="86d5b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="86d5b-131">Requirement</span></span> | <span data-ttu-id="86d5b-132">Valor</span><span class="sxs-lookup"><span data-stu-id="86d5b-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="86d5b-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="86d5b-133">Header</span></span><br/> | <dl> <span data-ttu-id="86d5b-134"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="86d5b-134"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86d5b-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="86d5b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86d5b-136">**\_Propriedades de heap D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="86d5b-136">**D3D12\_HEAP\_PROPERTIES**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)
</dt> <dt>

[<span data-ttu-id="86d5b-137">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="86d5b-137">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





