---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever um PSO armazenado em cache como um único objeto adequado para uma descrição de fluxo.
ms.assetid: 86CDC60A-275D-4B71-BE6D-C863C72E9C05
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78ddb223dfd2baa7bc6bee1b5a36950fc47d65d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781623"
---
# <a name="cd3dx12_pipeline_state_stream_cached_pso-structure"></a><span data-ttu-id="3c0cb-104">\_ \_ \_ \_ Estrutura PSO em cache do fluxo de estado do pipeline \_ do CD3DX12</span><span class="sxs-lookup"><span data-stu-id="3c0cb-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO structure</span></span>

<span data-ttu-id="3c0cb-105">Uma estrutura auxiliar usada para descrever um PSO armazenado em cache como um único objeto adequado para uma descrição de fluxo.</span><span class="sxs-lookup"><span data-stu-id="3c0cb-105">A helper structure used to describe a cached PSO as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c0cb-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3c0cb-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO {
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO(D3D12_CACHED_PIPELINE_STATE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO operator=(D3D12_CACHED_PIPELINE_STATE const& i);
                                           operator D3D12_CACHED_PIPELINE_STATE() const;
};
```



## <a name="members"></a><span data-ttu-id="3c0cb-107">Membros</span><span class="sxs-lookup"><span data-stu-id="3c0cb-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3c0cb-108">**PSO do fluxo de estado do pipeline do CD3DX12 \_ \_ \_ \_ em cache \_**</span><span class="sxs-lookup"><span data-stu-id="3c0cb-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO**</span></span>
</dt> <dd>

<span data-ttu-id="3c0cb-109">Cria uma nova instância, não inicializada, de um CD3DX12 de \_ fluxo de estado de pipeline do \_ \_ \_ codecache \_ .</span><span class="sxs-lookup"><span data-stu-id="3c0cb-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO.</span></span>

</dd> <dt>

<span data-ttu-id="3c0cb-110">**CD3DX12 \_ \_ \_ \_ do fluxo de estado do pipeline \_ do D3D12 do PSO cache do estado de \_ pipeline em cache \_ \_ constante &i)**</span><span class="sxs-lookup"><span data-stu-id="3c0cb-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO(D3D12\_CACHED\_PIPELINE\_STATE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="3c0cb-111">Cria uma nova instância de um CD3DX12 de \_ fluxo de estado de pipeline do \_ \_ \_ \_ D3D12, inicializada com um tipo de subobjeto do tipo de subobjeto do estado do pipeline do codeD3D12 **\_ \_ \_ \_ \_ armazenado em cache do \_ PSO** e dos dados de subobjetos copiados de *i*, uma estrutura de [**\_ \_ \_ estado de pipeline em cache em**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) .</span><span class="sxs-lookup"><span data-stu-id="3c0cb-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_CACHED\_PSO** and subobject data copied from *i*, a [**D3D12\_CACHED\_PIPELINE\_STATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3c0cb-112">**Operator = (D3D12 de \_ estado de pipeline em cache \_ \_ const& i)**</span><span class="sxs-lookup"><span data-stu-id="3c0cb-112">**operator=(D3D12\_CACHED\_PIPELINE\_STATE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="3c0cb-113">Operador de atribuição de cópia.</span><span class="sxs-lookup"><span data-stu-id="3c0cb-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="3c0cb-114">**operador D3D12 \_ \_ de estado de pipeline armazenado em cache \_ () const**</span><span class="sxs-lookup"><span data-stu-id="3c0cb-114">**operator D3D12\_CACHED\_PIPELINE\_STATE() const**</span></span>
</dt> <dd>

<span data-ttu-id="3c0cb-115">Conversão implícita em uma estrutura de [**\_ \_ \_ estado de pipeline em cache D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) .</span><span class="sxs-lookup"><span data-stu-id="3c0cb-115">Implicit conversion to a [**D3D12\_CACHED\_PIPELINE\_STATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c0cb-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c0cb-116">Remarks</span></span>

<span data-ttu-id="3c0cb-117">\_O CD3DX12 \_ do \_ fluxo \_ de estado \_ de pipeline do CD3DX12 de um controle de perfil é uma especialização de TYPEDEF do modelo de [**\_ \_ \_ \_ subobjeto de fluxo do estado do pipeline**](cd3dx12-pipeline-state-stream-subobject.md) e é definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="3c0cb-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_CACHED_PIPELINE_STATE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_CACHED_PSO>
    CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
          
```



## <a name="requirements"></a><span data-ttu-id="3c0cb-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c0cb-118">Requirements</span></span>



| <span data-ttu-id="3c0cb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c0cb-119">Requirement</span></span> | <span data-ttu-id="3c0cb-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3c0cb-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3c0cb-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3c0cb-121">Header</span></span><br/> | <dl> <span data-ttu-id="3c0cb-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c0cb-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c0cb-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c0cb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c0cb-124">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="3c0cb-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="3c0cb-125">**Subobjeto de fluxo do estado do \_ pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3c0cb-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="3c0cb-126">**\_Tipo de \_ subobjeto de estado de pipeline D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3c0cb-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

