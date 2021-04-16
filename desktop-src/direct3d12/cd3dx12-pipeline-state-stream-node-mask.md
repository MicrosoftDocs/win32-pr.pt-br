---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever uma máscara de nó como um único objeto adequado para uma descrição de fluxo.
ms.assetid: 5C770D9A-D692-46CF-8D60-EE5EB04998C8
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c364ecd20459d8c20bdd3d30b969cc3b9ae46d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105750183"
---
# <a name="cd3dx12_pipeline_state_stream_node_mask-structure"></a><span data-ttu-id="68cd6-104">\_Estrutura de \_ \_ máscara do \_ nó de fluxo \_ do CD3DX12 pipeline</span><span class="sxs-lookup"><span data-stu-id="68cd6-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK structure</span></span>

<span data-ttu-id="68cd6-105">Uma estrutura auxiliar usada para descrever uma máscara de nó como um único objeto adequado para uma descrição de fluxo.</span><span class="sxs-lookup"><span data-stu-id="68cd6-105">A helper structure used to describe a node mask as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="68cd6-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="68cd6-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK {
                                          CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK;
                                          CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK(UINT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK operator=(UINT const& i);
                                          operator UINT() const;
};
```



## <a name="members"></a><span data-ttu-id="68cd6-107">Membros</span><span class="sxs-lookup"><span data-stu-id="68cd6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="68cd6-108">**\_Máscara de \_ nó de fluxo de estado de pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="68cd6-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK**</span></span>
</dt> <dd>

<span data-ttu-id="68cd6-109">Cria uma nova instância, não inicializada, de uma \_ máscara de nó de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="68cd6-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK.</span></span>

</dd> <dt>

<span data-ttu-id="68cd6-110">**\_ \_ \_ \_ \_ Máscara do nó de fluxo do CD3DX12 pipeline (UINT const &i)**</span><span class="sxs-lookup"><span data-stu-id="68cd6-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK(UINT const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="68cd6-111">Cria uma nova instância de uma \_ máscara de nó de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ , inicializada com um tipo de subobjeto de  tipo de subobjeto de estado de **\_ pipeline \_ \_ \_ \_ \_ D3D12** e dados de subobjetos copiados de i, uma máscara de nó uint.</span><span class="sxs-lookup"><span data-stu-id="68cd6-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_NODE\_MASK** and subobject data copied from *i*, a **UINT** node mask.</span></span>

</dd> <dt>

<span data-ttu-id="68cd6-112">**Operator = (UINT const& i)**</span><span class="sxs-lookup"><span data-stu-id="68cd6-112">**operator=(UINT const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="68cd6-113">Operador de atribuição de cópia.</span><span class="sxs-lookup"><span data-stu-id="68cd6-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="68cd6-114">**constante de operador UINT ()**</span><span class="sxs-lookup"><span data-stu-id="68cd6-114">**operator UINT() const**</span></span>
</dt> <dd>

<span data-ttu-id="68cd6-115">Conversão implícita em uma máscara de nó **uint** .</span><span class="sxs-lookup"><span data-stu-id="68cd6-115">Implicit conversion to a **UINT** node mask.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68cd6-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="68cd6-116">Remarks</span></span>

<span data-ttu-id="68cd6-117">\_ \_ \_ \_ \_ A máscara do nó de fluxo do estado do pipeline CD3DX12 é uma especialização de TYPEDEF do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="68cd6-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<UINT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_NODE_MASK>
    CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK;
          
```



## <a name="requirements"></a><span data-ttu-id="68cd6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68cd6-118">Requirements</span></span>



| <span data-ttu-id="68cd6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="68cd6-119">Requirement</span></span> | <span data-ttu-id="68cd6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="68cd6-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="68cd6-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="68cd6-121">Header</span></span><br/> | <dl> <span data-ttu-id="68cd6-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="68cd6-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68cd6-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="68cd6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68cd6-124">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="68cd6-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="68cd6-125">**Subobjeto de fluxo do estado do \_ pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="68cd6-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="68cd6-126">**\_Tipo de \_ subobjeto de estado de pipeline D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="68cd6-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

