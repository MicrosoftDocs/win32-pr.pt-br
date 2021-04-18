---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever a descrição da saída do fluxo como um único objeto adequado para uma descrição de fluxo.
ms.assetid: CC7E1E76-CD44-4D70-A5B8-7C2B6210468E
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acc8f7bf059c4eee72b0b22abfc424ee82ffd2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812274"
---
# <a name="cd3dx12_pipeline_state_stream_stream_output-structure"></a><span data-ttu-id="63f61-104">\_Estrutura de \_ \_ saída do fluxo de fluxo do estado do \_ pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="63f61-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT structure</span></span>

<span data-ttu-id="63f61-105">Uma estrutura auxiliar usada para descrever a descrição da saída do fluxo como um único objeto adequado para uma descrição de fluxo.</span><span class="sxs-lookup"><span data-stu-id="63f61-105">A helper structure used to describe the stream output description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="63f61-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63f61-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT {
                                              CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
                                              CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT(D3D12_STREAM_OUTPUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT operator=(D3D12_STREAM_OUTPUT_DESC const& i);
                                              operator D3D12_STREAM_OUTPUT_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="63f61-107">Membros</span><span class="sxs-lookup"><span data-stu-id="63f61-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="63f61-108">**\_Saída de \_ fluxo de fluxo de estado de pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="63f61-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="63f61-109">Cria uma nova instância, não inicializada, de uma \_ saída de fluxo de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="63f61-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT.</span></span>

</dd> <dt>

<span data-ttu-id="63f61-110">**\_ \_ \_ \_ \_ Saída de fluxo de fluxo de estado de pipeline CD3DX12 ( \_ saída de fluxo D3D12 \_ \_ desc const &i)**</span><span class="sxs-lookup"><span data-stu-id="63f61-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT(D3D12\_STREAM\_OUTPUT\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="63f61-111">Cria uma nova instância de uma saída de fluxo de fluxo de estado de pipeline do CD3DX12 \_ \_ \_ \_ \_ , inicializada com um tipo de subobjeto do tipo de subobjeto do estado do  **pipeline D3D12 de \_ \_ \_ \_ \_ \_ saída de fluxo** e dados de subobjeto copiados de i, uma estrutura [**desc de saída do fluxo de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) .</span><span class="sxs-lookup"><span data-stu-id="63f61-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_STREAM\_OUTPUT** and subobject data copied from *i*, a [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="63f61-112">**Operator = (D3D12 \_ de \_ saída de fluxo \_ desc const& i)**</span><span class="sxs-lookup"><span data-stu-id="63f61-112">**operator=(D3D12\_STREAM\_OUTPUT\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="63f61-113">Operador de atribuição de cópia.</span><span class="sxs-lookup"><span data-stu-id="63f61-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="63f61-114">**D3D12 \_ do operador \_ \_ de saída de fluxo DESC () const**</span><span class="sxs-lookup"><span data-stu-id="63f61-114">**operator D3D12\_STREAM\_OUTPUT\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="63f61-115">Conversão implícita em uma [**estrutura \_ \_ \_ desc de saída de fluxo de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) .</span><span class="sxs-lookup"><span data-stu-id="63f61-115">Implicit conversion to a [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63f61-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="63f61-116">Remarks</span></span>

<span data-ttu-id="63f61-117">A \_ \_ \_ \_ \_ saída do fluxo de fluxo do estado do pipeline CD3DX12 é uma especialização de TYPEDEF do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="63f61-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_STREAM_OUTPUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_STREAM_OUTPUT>
    CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
          
```



## <a name="requirements"></a><span data-ttu-id="63f61-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63f61-118">Requirements</span></span>



| <span data-ttu-id="63f61-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="63f61-119">Requirement</span></span> | <span data-ttu-id="63f61-120">Valor</span><span class="sxs-lookup"><span data-stu-id="63f61-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="63f61-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="63f61-121">Header</span></span><br/> | <dl> <span data-ttu-id="63f61-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="63f61-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63f61-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="63f61-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63f61-124">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="63f61-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="63f61-125">**Subobjeto de fluxo do estado do \_ pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="63f61-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="63f61-126">**\_Tipo de \_ subobjeto de estado de pipeline D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="63f61-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

