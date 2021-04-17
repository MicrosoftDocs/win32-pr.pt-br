---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever o valor de recorte da faixa de buffer de índice como um único objeto adequado para uma descrição de fluxo.
ms.assetid: AF8F0919-4601-4A95-832A-5E1DA0304939
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c14924828c924b3bbbca3bb1a5f822437ec4c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105747720"
---
# <a name="cd3dx12_pipeline_state_stream_ib_strip_cut_value-structure"></a><span data-ttu-id="2c9a4-104">\_Estrutura do \_ \_ valor de \_ \_ \_ recorte de \_ faixa do CD3DX12 de fluxo do Stream IB</span><span class="sxs-lookup"><span data-stu-id="2c9a4-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE structure</span></span>

<span data-ttu-id="2c9a4-105">Uma estrutura auxiliar usada para descrever o valor de recorte da faixa de buffer de índice como um único objeto adequado para uma descrição de fluxo.</span><span class="sxs-lookup"><span data-stu-id="2c9a4-105">A helper structure used to describe the index buffer strip cut value as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c9a4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c9a4-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE {
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE operator=(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const& i);
                                                   operator D3D12_INDEX_BUFFER_STRIP_CUT_VALUE() const;
};
```



## <a name="members"></a><span data-ttu-id="2c9a4-107">Membros</span><span class="sxs-lookup"><span data-stu-id="2c9a4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2c9a4-108">**\_Valor de \_ \_ \_ \_ \_ recorte de faixa \_ do Stream IB do CD3DX12 pipeline**</span><span class="sxs-lookup"><span data-stu-id="2c9a4-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE**</span></span>
</dt> <dd>

<span data-ttu-id="2c9a4-109">Cria uma instância nova e não inicializada de um valor de \_ \_ \_ \_ \_ \_ recorte de faixa \_ de CD3DX12 do fluxo de estado de pipeline.</span><span class="sxs-lookup"><span data-stu-id="2c9a4-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE.</span></span>

</dd> <dt>

<span data-ttu-id="2c9a4-110">**CD3DX12 \_ pipeline \_ State \_ Stream \_ IB \_ faixa \_ \_ Value (D3D12 \_ index buffer de índice de \_ \_ \_ recorte de \_ valor const &i)**</span><span class="sxs-lookup"><span data-stu-id="2c9a4-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE(D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="2c9a4-111">Cria uma nova instância de um fluxo de estado de pipeline do CD3DX12 \_ \_ Stream de \_ \_ \_ recorte de faixa \_ \_ , inicializado com um tipo de subobjeto do  **tipo de \_ \_ \_ subobjeto do estado \_ \_ \_ \_ \_ do pipeline de D3D12** e dados de subobjeto recortados da faixa de [**\_ buffer de índice \_ \_ \_ \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) .</span><span class="sxs-lookup"><span data-stu-id="2c9a4-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_IB\_STRIP\_CUT\_VALUE** and subobject data copied from *i*, a [**D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2c9a4-112">**Operator = (D3D12 de \_ buffer de índice de distribuição de valor de \_ \_ \_ recorte \_ constante& i)**</span><span class="sxs-lookup"><span data-stu-id="2c9a4-112">**operator=(D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="2c9a4-113">Operador de atribuição de cópia.</span><span class="sxs-lookup"><span data-stu-id="2c9a4-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="2c9a4-114">**\_ \_ \_ \_ valor de recorte de faixa \_ do buffer de índice do operador D3D12 () const**</span><span class="sxs-lookup"><span data-stu-id="2c9a4-114">**operator D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE() const**</span></span>
</dt> <dd>

<span data-ttu-id="2c9a4-115">Conversão implícita em uma [**\_ faixa de \_ \_ \_ \_ valor de recorte de buffer de índice D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) .</span><span class="sxs-lookup"><span data-stu-id="2c9a4-115">Implicit conversion to a [**D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c9a4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c9a4-116">Remarks</span></span>

<span data-ttu-id="2c9a4-117">\_ \_ \_ \_ \_ \_ O valor de recorte do Stream IB strip do CD3DX12 pipeline \_ é uma especialização de typedef do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2c9a4-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INDEX_BUFFER_STRIP_CUT_VALUE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_IB_STRIP_CUT_VALUE>
    CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
          
```



## <a name="requirements"></a><span data-ttu-id="2c9a4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c9a4-118">Requirements</span></span>



| <span data-ttu-id="2c9a4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c9a4-119">Requirement</span></span> | <span data-ttu-id="2c9a4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2c9a4-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2c9a4-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2c9a4-121">Header</span></span><br/> | <dl> <span data-ttu-id="2c9a4-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c9a4-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c9a4-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c9a4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c9a4-124">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="2c9a4-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="2c9a4-125">**Subobjeto de fluxo do estado do \_ pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2c9a4-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="2c9a4-126">**\_Tipo de \_ subobjeto de estado de pipeline D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2c9a4-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

