---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever os formatos de destino de renderização como um único objeto adequado para uma descrição de fluxo.
ms.assetid: 8C5C2279-7985-41B6-87EA-ABB0007DAFD4
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a64f051ba56edf176c87bbc99551cd974fc3a43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105797546"
---
# <a name="cd3dx12_pipeline_state_stream_render_target_formats-structure"></a><span data-ttu-id="fbcb9-104">\_Estrutura de \_ \_ formatos de \_ destino de renderização de fluxo de \_ estado de pipeline \_ CD3DX12</span><span class="sxs-lookup"><span data-stu-id="fbcb9-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS structure</span></span>

<span data-ttu-id="fbcb9-105">Uma estrutura auxiliar usada para descrever os formatos de destino de renderização como um único objeto adequado para uma descrição de fluxo.</span><span class="sxs-lookup"><span data-stu-id="fbcb9-105">A helper structure used to describe the render target formats as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbcb9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fbcb9-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS {
                                                      CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
                                                      CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS(D3D12_RT_FORMAT_ARRAY const &i);
  CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS operator=(D3D12_RT_FORMAT_ARRAY const& i);
                                                      operator D3D12_RT_FORMAT_ARRAY() const;
};
```



## <a name="members"></a><span data-ttu-id="fbcb9-107">Membros</span><span class="sxs-lookup"><span data-stu-id="fbcb9-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="fbcb9-108">**\_Formatos de \_ \_ destino de renderização de fluxo de estado \_ de \_ pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="fbcb9-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS**</span></span>
</dt> <dd>

<span data-ttu-id="fbcb9-109">Cria uma nova instância, não inicializada, de um fluxo de estado do pipeline do CD3DX12 \_ formatos de \_ destino de \_ \_ renderização \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="fbcb9-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS.</span></span>

</dd> <dt>

<span data-ttu-id="fbcb9-110">**\_ \_ \_ \_ \_ \_ Formatos de destino de renderização de fluxo de estado de pipeline CD3DX12 ( \_ matriz de formato D3D12 RT \_ \_ &i)**</span><span class="sxs-lookup"><span data-stu-id="fbcb9-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS(D3D12\_RT\_FORMAT\_ARRAY const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="fbcb9-111">Cria uma nova instância de um \_ fluxo de estado do pipeline CD3DX12 \_ \_ \_ \_ \_ formatos de destino, inicializados com um tipo de subobjeto do **tipo de \_ subobjeto do estado do pipeline D3D12 \_ \_ \_ \_ renderizar os \_ \_ formatos de destino** e os dados de subobjeto copiados de *i*, uma estrutura de [**\_ \_ \_ matriz de formato D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .</span><span class="sxs-lookup"><span data-stu-id="fbcb9-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_RENDER\_TARGET\_FORMATS** and subobject data copied from *i*, a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fbcb9-112">**Operator = ( \_ matriz de formato D3D12 RT \_ \_ const& i)**</span><span class="sxs-lookup"><span data-stu-id="fbcb9-112">**operator=(D3D12\_RT\_FORMAT\_ARRAY const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="fbcb9-113">Operador de atribuição de cópia.</span><span class="sxs-lookup"><span data-stu-id="fbcb9-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="fbcb9-114">**\_ \_ matriz de formato D3D12 RT \_ do operador () const**</span><span class="sxs-lookup"><span data-stu-id="fbcb9-114">**operator D3D12\_RT\_FORMAT\_ARRAY() const**</span></span>
</dt> <dd>

<span data-ttu-id="fbcb9-115">Conversão implícita em uma estrutura de [**\_ matriz de \_ formato \_ D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .</span><span class="sxs-lookup"><span data-stu-id="fbcb9-115">Implicit conversion to a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fbcb9-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbcb9-116">Remarks</span></span>

<span data-ttu-id="fbcb9-117">\_ \_ \_ \_ \_ \_ Os formatos de destino de renderização de fluxo de estado de pipeline CD3DX12 é uma especialização de typedef do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="fbcb9-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_RT_FORMAT_ARRAY, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RENDER_TARGET_FORMATS>
    CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
          
```



## <a name="requirements"></a><span data-ttu-id="fbcb9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbcb9-118">Requirements</span></span>



| <span data-ttu-id="fbcb9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbcb9-119">Requirement</span></span> | <span data-ttu-id="fbcb9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="fbcb9-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fbcb9-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fbcb9-121">Header</span></span><br/> | <dl> <span data-ttu-id="fbcb9-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbcb9-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbcb9-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbcb9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbcb9-124">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="fbcb9-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="fbcb9-125">**Subobjeto de fluxo do estado do \_ pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fbcb9-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="fbcb9-126">**\_Tipo de \_ subobjeto de estado de pipeline D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fbcb9-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

