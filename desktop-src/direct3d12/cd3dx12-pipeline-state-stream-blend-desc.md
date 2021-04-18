---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever uma descrição de Blend como um único objeto adequado para uma descrição de fluxo.
ms.assetid: A629B05D-0A70-4C96-9F66-1508F2667BF6
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d251be9cc1423babc58e1d3c3be87c5345308874
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781434"
---
# <a name="cd3dx12_pipeline_state_stream_blend_desc-structure"></a><span data-ttu-id="e886d-104">\_ \_ \_ \_ Estrutura desc de fluxo de estado do pipeline do \_ CD3DX12</span><span class="sxs-lookup"><span data-stu-id="e886d-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC structure</span></span>

<span data-ttu-id="e886d-105">Uma estrutura auxiliar usada para descrever uma descrição de Blend como um único objeto adequado para uma descrição de fluxo.</span><span class="sxs-lookup"><span data-stu-id="e886d-105">A helper structure used to describe a blend description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="e886d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e886d-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC {
                                           CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
                                           CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC(CD3DX12_BLEND_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC operator=(CD3DX12_BLEND_DESC const& i);
                                           operator CD3DX12_BLEND_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="e886d-107">Membros</span><span class="sxs-lookup"><span data-stu-id="e886d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e886d-108">**\_ \_ \_ Stream \_ Blend de estado \_ do pipeline CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="e886d-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**</span></span>
</dt> <dd>

<span data-ttu-id="e886d-109">Cria uma nova instância, não inicializada, de um \_ fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e886d-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="e886d-110">**\_ \_ \_ Stream \_ Blend do CD3DX12 pipeline \_ de transmissão de perfil (CD3DX12 \_ Blend \_ desc const &i)**</span><span class="sxs-lookup"><span data-stu-id="e886d-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC(CD3DX12\_BLEND\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="e886d-111">Cria uma nova instância de um fluxo de estado de pipeline do CD3DX12 \_ \_ \_ \_ \_ , inicializado com um tipo de subobjeto do subobjeto de **estado do pipeline D3D12 de \_ \_ \_ \_ \_ mistura** e dados de subobjeto copiados de *i*, uma estrutura [**desc de CD3DX12 \_ Blend \_**](cd3dx12-blend-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="e886d-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_BLEND** and subobject data copied from *i*, a [**CD3DX12\_BLEND\_DESC**](cd3dx12-blend-desc.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e886d-112">**Operator = (CD3DX12 \_ Blend \_ DESC const& i)**</span><span class="sxs-lookup"><span data-stu-id="e886d-112">**operator=(CD3DX12\_BLEND\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="e886d-113">Operador de atribuição de cópia.</span><span class="sxs-lookup"><span data-stu-id="e886d-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="e886d-114">**\_constante do operador CD3DX12 Blend \_ () const**</span><span class="sxs-lookup"><span data-stu-id="e886d-114">**operator CD3DX12\_BLEND\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="e886d-115">Conversão implícita em uma [**estrutura \_ \_ Desc do CD3DX12 Blend**](cd3dx12-blend-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="e886d-115">Implicit conversion to a [**CD3DX12\_BLEND\_DESC**](cd3dx12-blend-desc.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e886d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e886d-116">Remarks</span></span>

<span data-ttu-id="e886d-117">\_ \_ \_ O fluxo de estado do pipeline do CD3DX12 \_ do Stream Blend \_ DESC é uma especialização de TYPEDEF do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e886d-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_BLEND_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_BLEND, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
          
```



## <a name="requirements"></a><span data-ttu-id="e886d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e886d-118">Requirements</span></span>



| <span data-ttu-id="e886d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e886d-119">Requirement</span></span> | <span data-ttu-id="e886d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e886d-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e886d-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e886d-121">Header</span></span><br/> | <dl> <span data-ttu-id="e886d-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="e886d-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e886d-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="e886d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e886d-124">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="e886d-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="e886d-125">**Subobjeto de fluxo do estado do \_ pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e886d-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="e886d-126">**\_Tipo de \_ subobjeto de estado de pipeline D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e886d-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

