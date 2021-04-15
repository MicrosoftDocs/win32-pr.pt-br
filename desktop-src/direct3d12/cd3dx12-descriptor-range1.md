---
title: Estrutura de CD3DX12_DESCRIPTOR_RANGE1 (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura RANGE1 do descritor D3D12 \_ .
ms.assetid: 9D073158-5907-4D1C-8D75-72B304277DAD
keywords:
- Estrutura de CD3DX12_DESCRIPTOR_RANGE1
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6386d8094d573fba9cd3af44b0148215ee621e2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105747458"
---
# <a name="cd3dx12_descriptor_range1-structure"></a><span data-ttu-id="37eb2-104">\_Estrutura RANGE1 do descritor CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="37eb2-104">CD3DX12\_DESCRIPTOR\_RANGE1 structure</span></span>

<span data-ttu-id="37eb2-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ \_ RANGE1 do descritor D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) .</span><span class="sxs-lookup"><span data-stu-id="37eb2-105">A helper structure to enable easy initialization of a [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="37eb2-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37eb2-106">Syntax</span></span>


```C++
struct CD3DX12_DESCRIPTOR_RANGE1  : public D3D12_DESCRIPTOR_RANGE1{
       CD3DX12_DESCRIPTOR_RANGE1();
       explicit CD3DX12_DESCRIPTOR_RANGE1(const D3D12_DESCRIPTOR_RANGE1 &o);
       CD3DX12_DESCRIPTOR_RANGE1(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE1 &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a><span data-ttu-id="37eb2-107">Membros</span><span class="sxs-lookup"><span data-stu-id="37eb2-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="37eb2-108">**CD3DX12 \_ DESCRIPTOR \_ RANGE1 ()**</span><span class="sxs-lookup"><span data-stu-id="37eb2-108">**CD3DX12\_DESCRIPTOR\_RANGE1()**</span></span>
</dt> <dd>

<span data-ttu-id="37eb2-109">Cria uma nova instância, não inicializada, de um \_ descritor CD3DX12 \_ RANGE1.</span><span class="sxs-lookup"><span data-stu-id="37eb2-109">Creates a new, uninitialized, instance of a CD3DX12\_DESCRIPTOR\_RANGE1.</span></span>

</dd> <dt>

<span data-ttu-id="37eb2-110">**\_descritor CD3DX12 explícito \_ RANGE1 (const D3D12 \_ Descriptor \_ RANGE1 &o)**</span><span class="sxs-lookup"><span data-stu-id="37eb2-110">**explicit CD3DX12\_DESCRIPTOR\_RANGE1(const D3D12\_DESCRIPTOR\_RANGE1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="37eb2-111">Cria uma nova instância de um \_ descritor CD3DX12 \_ RANGE1, inicializada com o conteúdo de outra estrutura [**\_ \_ RANGE1 do descritor D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) .</span><span class="sxs-lookup"><span data-stu-id="37eb2-111">Creates a new instance of a CD3DX12\_DESCRIPTOR\_RANGE1, initialized with the contents of another [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="37eb2-112">**CD3DX12 \_ Descriptor \_ RANGE1 (D3D12 \_ descritor de intervalo de tipo RangeType \_ \_ , uint NUMDESCRIPTORS, uint baseShaderRegister, uint registerSpace = 0, D3D12 \_ descritor \_ sinalizadores de intervalo sinalizadores \_ flags = D3D12 \_ \_ sinalizador de intervalo de descritor \_ \_ nenhum, uint offsetInDescriptorsFromTableStart = D3D12 \_ descritor de intervalo de descrição \_ \_ \_ acrescentar)**</span><span class="sxs-lookup"><span data-stu-id="37eb2-112">**CD3DX12\_DESCRIPTOR\_RANGE1(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12\_DESCRIPTOR\_RANGE\_FLAGS flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="37eb2-113">Cria uma nova instância de um \_ descritor CD3DX12 \_ RANGE1, inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="37eb2-113">Creates a new instance of a CD3DX12\_DESCRIPTOR\_RANGE1, initializing the following parameters:</span></span>

<span data-ttu-id="37eb2-114">[**D3D12 \_ \_ \_ Tipo de intervalo do descritor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) RangeType</span><span class="sxs-lookup"><span data-stu-id="37eb2-114">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="37eb2-115">NumDescriptors UINT</span><span class="sxs-lookup"><span data-stu-id="37eb2-115">UINT numDescriptors</span></span>

<span data-ttu-id="37eb2-116">BaseShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="37eb2-116">UINT baseShaderRegister</span></span>

<span data-ttu-id="37eb2-117">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="37eb2-117">UINT registerSpace = 0</span></span>

<span data-ttu-id="37eb2-118">[**D3D12 \_ Sinalizadores \_ de \_ intervalo de descritores**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = \_ sinalizador de intervalo de descritor D3D12 \_ \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="37eb2-118">[**D3D12\_DESCRIPTOR\_RANGE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE</span></span>

<span data-ttu-id="37eb2-119">UINT offsetInDescriptorsFromTableStart = \_ deslocamento de intervalo de descritor de D3D12 \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="37eb2-119">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="37eb2-120">**Init embutido (D3D12 \_ de intervalo de descritor de \_ \_ tipo RangeType, UINT NumDescriptors, UINT BaseShaderRegister, uint registerSpace = 0, D3D12 \_ descritor \_ sinalizadores de intervalo sinalizadores \_ flags = D3D12 \_ descritor de intervalo de descrição \_ \_ \_ nenhum, uint offsetInDescriptorsFromTableStart = D3D12 \_ descritor de intervalo de descrição \_ \_ \_ acrescentar)**</span><span class="sxs-lookup"><span data-stu-id="37eb2-120">**inline Init(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12\_DESCRIPTOR\_RANGE\_FLAGS flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="37eb2-121">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="37eb2-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="37eb2-122">[**D3D12 \_ \_ \_ Tipo de intervalo do descritor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) RangeType</span><span class="sxs-lookup"><span data-stu-id="37eb2-122">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="37eb2-123">NumDescriptors UINT</span><span class="sxs-lookup"><span data-stu-id="37eb2-123">UINT numDescriptors</span></span>

<span data-ttu-id="37eb2-124">BaseShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="37eb2-124">UINT baseShaderRegister</span></span>

<span data-ttu-id="37eb2-125">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="37eb2-125">UINT registerSpace = 0</span></span>

<span data-ttu-id="37eb2-126">[**D3D12 \_ Sinalizadores \_ de \_ intervalo de descritores**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = \_ sinalizador de intervalo de descritor D3D12 \_ \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="37eb2-126">[**D3D12\_DESCRIPTOR\_RANGE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE</span></span>

<span data-ttu-id="37eb2-127">UINT offsetInDescriptorsFromTableStart = \_ deslocamento de intervalo de descritor de D3D12 \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="37eb2-127">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="37eb2-128">**Inicialização embutida estática ( \_ descritor de D3D12 \_ RANGE1 &intervalo, D3D12 descritor de intervalo de \_ \_ \_ tipo RangeType, uint NUMDESCRIPTORS, uint baseShaderRegister, uint registerSpace = 0, D3D12 \_ descritor \_ sinalizadores de intervalo sinalizadores \_ = D3D12 \_ descritor de \_ intervalo \_ Flag \_ nenhum, uint offsetInDescriptorsFromTableStart = D3D12 \_ descritor de intervalo de descrição de \_ \_ deslocamento \_**</span><span class="sxs-lookup"><span data-stu-id="37eb2-128">**static inline Init(D3D12\_DESCRIPTOR\_RANGE1 &range, D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12\_DESCRIPTOR\_RANGE\_FLAGS flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="37eb2-129">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="37eb2-129">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="37eb2-130">[**D3D12 \_ Intervalo \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) de &de RANGE1 do descritor</span><span class="sxs-lookup"><span data-stu-id="37eb2-130">[**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) &range</span></span>

<span data-ttu-id="37eb2-131">[**D3D12 \_ \_ \_ Tipo de intervalo do descritor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) RangeType</span><span class="sxs-lookup"><span data-stu-id="37eb2-131">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="37eb2-132">NumDescriptors UINT</span><span class="sxs-lookup"><span data-stu-id="37eb2-132">UINT numDescriptors</span></span>

<span data-ttu-id="37eb2-133">BaseShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="37eb2-133">UINT baseShaderRegister</span></span>

<span data-ttu-id="37eb2-134">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="37eb2-134">UINT registerSpace = 0</span></span>

<span data-ttu-id="37eb2-135">[**D3D12 \_ Sinalizadores \_ de \_ intervalo de descritores**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = \_ sinalizador de intervalo de descritor D3D12 \_ \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="37eb2-135">[**D3D12\_DESCRIPTOR\_RANGE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE</span></span>

<span data-ttu-id="37eb2-136">UINT offsetInDescriptorsFromTableStart = \_ deslocamento de intervalo de descritor de D3D12 \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="37eb2-136">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37eb2-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37eb2-137">Requirements</span></span>



| <span data-ttu-id="37eb2-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="37eb2-138">Requirement</span></span> | <span data-ttu-id="37eb2-139">Valor</span><span class="sxs-lookup"><span data-stu-id="37eb2-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="37eb2-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="37eb2-140">Header</span></span><br/> | <dl> <span data-ttu-id="37eb2-141"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="37eb2-141"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37eb2-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="37eb2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37eb2-143">**D3D12 \_ descritor \_ RANGE1**</span><span class="sxs-lookup"><span data-stu-id="37eb2-143">**D3D12\_DESCRIPTOR\_RANGE1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
</dt> <dt>

[<span data-ttu-id="37eb2-144">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="37eb2-144">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





