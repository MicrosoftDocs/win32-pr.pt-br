---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever a topologia primitiva como um único objeto adequado para uma descrição de fluxo.
ms.assetid: 7DC73B75-2B8D-4DAB-A0AA-6DF6F4039093
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e597da8ea1ed4a4291142065e8e06f89d2664e03
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781563"
---
# <a name="cd3dx12_pipeline_state_stream_primitive_topology-structure"></a><span data-ttu-id="b849e-104">\_Estrutura de \_ \_ \_ topologia primitiva de fluxo de estado de pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="b849e-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY structure</span></span>

<span data-ttu-id="b849e-105">Uma estrutura auxiliar usada para descrever a topologia primitiva como um único objeto adequado para uma descrição de fluxo.</span><span class="sxs-lookup"><span data-stu-id="b849e-105">A helper structure used to describe the primitive topology as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="b849e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b849e-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY {
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY(D3D12_PRIMITIVE_TOPOLOGY_TYPE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY operator=(D3D12_PRIMITIVE_TOPOLOGY_TYPE const& i);
                                                   operator D3D12_PRIMITIVE_TOPOLOGY_TYPE() const;
};
```



## <a name="members"></a><span data-ttu-id="b849e-107">Membros</span><span class="sxs-lookup"><span data-stu-id="b849e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b849e-108">**\_ \_ \_ Topologia primitiva de fluxo de estado \_ de pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="b849e-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY**</span></span>
</dt> <dd>

<span data-ttu-id="b849e-109">Cria uma nova instância, não inicializada, de uma \_ topologia primitiva de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b849e-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY.</span></span>

</dd> <dt>

<span data-ttu-id="b849e-110">**\_ \_ \_ \_ Topologia primitiva de fluxo de estado de pipeline CD3DX12 \_ ( \_ tipo de topologia primitivo D3D12 \_ \_ const &i)**</span><span class="sxs-lookup"><span data-stu-id="b849e-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY(D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="b849e-111">Cria uma nova instância de uma \_ topologia primitiva de fluxo de estado de pipeline do CD3DX12 \_ \_ \_ \_ , inicializada com um tipo de subobjeto do tipo de subobjeto de **perfil de pipeline D3D12 de \_ \_ \_ \_ \_ \_ topologia primitivo** e dados de subobjeto copiados de *i*, uma estrutura de [**\_ \_ \_ tipo de topologia primitivo D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) .</span><span class="sxs-lookup"><span data-stu-id="b849e-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_PRIMITIVE\_TOPOLOGY** and subobject data copied from *i*, a [**D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b849e-112">**Operator = ( \_ tipo de topologia D3D12 primitivo \_ \_ const& i)**</span><span class="sxs-lookup"><span data-stu-id="b849e-112">**operator=(D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="b849e-113">Operador de atribuição de cópia.</span><span class="sxs-lookup"><span data-stu-id="b849e-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="b849e-114">**\_ \_ \_ const do tipo de topologia primitiva do operador D3D12 ()**</span><span class="sxs-lookup"><span data-stu-id="b849e-114">**operator D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE() const**</span></span>
</dt> <dd>

<span data-ttu-id="b849e-115">Conversão implícita em uma estrutura de [**\_ \_ \_ tipo de topologia primitiva de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) .</span><span class="sxs-lookup"><span data-stu-id="b849e-115">Implicit conversion to a [**D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b849e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b849e-116">Remarks</span></span>

<span data-ttu-id="b849e-117">A \_ \_ \_ \_ topologia primitiva de fluxo \_ de estado do pipeline CD3DX12 é uma especialização de TYPEDEF do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b849e-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PRIMITIVE_TOPOLOGY_TYPE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_PRIMITIVE_TOPOLOGY>
    CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
          
```



## <a name="requirements"></a><span data-ttu-id="b849e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b849e-118">Requirements</span></span>



| <span data-ttu-id="b849e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b849e-119">Requirement</span></span> | <span data-ttu-id="b849e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b849e-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b849e-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b849e-121">Header</span></span><br/> | <dl> <span data-ttu-id="b849e-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b849e-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b849e-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="b849e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b849e-124">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="b849e-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="b849e-125">**Subobjeto de fluxo do estado do \_ pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b849e-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="b849e-126">**\_Tipo de \_ subobjeto de estado de pipeline D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b849e-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

