---
title: Estrutura de CD3DX12_DESCRIPTOR_RANGE (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de intervalo do descritor D3D12 \_ .
ms.assetid: F066ECA5-5E52-4483-B773-B43C5F12809B
keywords:
- Estrutura de CD3DX12_DESCRIPTOR_RANGE
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b511af1766daaefa7f92d33b71841b3a69c99927
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105752152"
---
# <a name="cd3dx12_descriptor_range-structure"></a><span data-ttu-id="4b12e-104">\_Estrutura do intervalo do descritor CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="4b12e-104">CD3DX12\_DESCRIPTOR\_RANGE structure</span></span>

<span data-ttu-id="4b12e-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ intervalo do descritor D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) .</span><span class="sxs-lookup"><span data-stu-id="4b12e-105">A helper structure to enable easy initialization of a [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b12e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b12e-106">Syntax</span></span>


```C++
struct CD3DX12_DESCRIPTOR_RANGE  : public D3D12_DESCRIPTOR_RANGE{
       CD3DX12_DESCRIPTOR_RANGE();
       explicit CD3DX12_DESCRIPTOR_RANGE(const D3D12_DESCRIPTOR_RANGE &o);
       CD3DX12_DESCRIPTOR_RANGE(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a><span data-ttu-id="4b12e-107">Membros</span><span class="sxs-lookup"><span data-stu-id="4b12e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4b12e-108">**\_ \_ Intervalo do descritor de CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="4b12e-108">**CD3DX12\_DESCRIPTOR\_RANGE()**</span></span>
</dt> <dd>

<span data-ttu-id="4b12e-109">Cria uma nova instância, não inicializada, de um \_ intervalo de descritor D3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="4b12e-109">Creates a new, uninitialized, instance of a D3DX12\_DESCRIPTOR\_RANGE.</span></span>

</dd> <dt>

<span data-ttu-id="4b12e-110">**\_intervalo de descritor de CD3DX12 explícito \_ ( \_ intervalo de descritores const D3D12 \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="4b12e-110">**explicit CD3DX12\_DESCRIPTOR\_RANGE(const D3D12\_DESCRIPTOR\_RANGE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="4b12e-111">Cria uma nova instância de um \_ intervalo de descritor D3DX12 \_ , inicializada com o conteúdo de outra estrutura de [**\_ \_ intervalo do descritor D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) .</span><span class="sxs-lookup"><span data-stu-id="4b12e-111">Creates a new instance of a D3DX12\_DESCRIPTOR\_RANGE, initialized with the contents of another [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4b12e-112">**\_ \_ Intervalo de descritores de CD3DX12 (D3D12 de intervalo de \_ descritor de \_ \_ tipo RangeType, uint NUMDESCRIPTORS, uint baseShaderRegister, UINT RegisterSpace = 0, uint offsetInDescriptorsFromTableStart = D3D12 de \_ deslocamento de intervalo de descritor \_ \_ \_ append)**</span><span class="sxs-lookup"><span data-stu-id="4b12e-112">**CD3DX12\_DESCRIPTOR\_RANGE(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="4b12e-113">Cria uma nova instância de um \_ intervalo de descritor D3DX12 \_ , inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="4b12e-113">Creates a new instance of a D3DX12\_DESCRIPTOR\_RANGE, initializing the following parameters:</span></span>

<span data-ttu-id="4b12e-114">[**D3D12 \_ \_ \_ Tipo de intervalo do descritor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) RangeType</span><span class="sxs-lookup"><span data-stu-id="4b12e-114">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="4b12e-115">NumDescriptors UINT</span><span class="sxs-lookup"><span data-stu-id="4b12e-115">UINT numDescriptors</span></span>

<span data-ttu-id="4b12e-116">BaseShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="4b12e-116">UINT baseShaderRegister</span></span>

<span data-ttu-id="4b12e-117">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="4b12e-117">UINT registerSpace = 0</span></span>

<span data-ttu-id="4b12e-118">UINT offsetInDescriptorsFromTableStart = \_ deslocamento de intervalo de descritor de D3D12 \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="4b12e-118">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="4b12e-119">**Init embutido (D3D12 \_ de intervalo do descritor de \_ \_ tipo RangeType, UINT NumDescriptors, UINT BaseShaderRegister, uint registerSpace = 0, uint offsetInDescriptorsFromTableStart = D3D12 de \_ deslocamento de intervalo de descritor de \_ \_ \_ anexo)**</span><span class="sxs-lookup"><span data-stu-id="4b12e-119">**inline Init(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="4b12e-120">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="4b12e-120">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="4b12e-121">[**D3D12 \_ \_ \_ Tipo de intervalo do descritor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) RangeType</span><span class="sxs-lookup"><span data-stu-id="4b12e-121">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="4b12e-122">NumDescriptors UINT</span><span class="sxs-lookup"><span data-stu-id="4b12e-122">UINT numDescriptors</span></span>

<span data-ttu-id="4b12e-123">BaseShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="4b12e-123">UINT baseShaderRegister</span></span>

<span data-ttu-id="4b12e-124">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="4b12e-124">UINT registerSpace = 0</span></span>

<span data-ttu-id="4b12e-125">UINT offsetInDescriptorsFromTableStart = \_ deslocamento de intervalo de descritor de D3D12 \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="4b12e-125">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="4b12e-126">**Inicialização embutida estática ( \_ intervalo do descritor de D3D12 \_ &intervalo, D3D12 do \_ descritor de tipo RangeType \_ \_ , uint NUMDESCRIPTORS, uint baseShaderRegister, UINT RegisterSpace = 0, uint offsetInDescriptorsFromTableStart = D3D12 do \_ intervalo de descritor de descrição \_ \_ \_ acrescentar)**</span><span class="sxs-lookup"><span data-stu-id="4b12e-126">**static inline Init(D3D12\_DESCRIPTOR\_RANGE &range, D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="4b12e-127">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="4b12e-127">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="4b12e-128">[**D3D12 \_ Intervalo \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) de &do intervalo do descritor</span><span class="sxs-lookup"><span data-stu-id="4b12e-128">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) &range</span></span>

<span data-ttu-id="4b12e-129">[**D3D12 \_ \_ \_ Tipo de intervalo do descritor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) RangeType</span><span class="sxs-lookup"><span data-stu-id="4b12e-129">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="4b12e-130">NumDescriptors UINT</span><span class="sxs-lookup"><span data-stu-id="4b12e-130">UINT numDescriptors</span></span>

<span data-ttu-id="4b12e-131">BaseShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="4b12e-131">UINT baseShaderRegister</span></span>

<span data-ttu-id="4b12e-132">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="4b12e-132">UINT registerSpace = 0</span></span>

<span data-ttu-id="4b12e-133">UINT offsetInDescriptorsFromTableStart = \_ deslocamento de intervalo de descritor de D3D12 \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="4b12e-133">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4b12e-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b12e-134">Requirements</span></span>



| <span data-ttu-id="4b12e-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b12e-135">Requirement</span></span> | <span data-ttu-id="4b12e-136">Valor</span><span class="sxs-lookup"><span data-stu-id="4b12e-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4b12e-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4b12e-137">Header</span></span><br/> | <dl> <span data-ttu-id="4b12e-138"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b12e-138"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b12e-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b12e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b12e-140">**\_Intervalo do descritor de D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="4b12e-140">**D3D12\_DESCRIPTOR\_RANGE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)
</dt> <dt>

[<span data-ttu-id="4b12e-141">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="4b12e-141">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





