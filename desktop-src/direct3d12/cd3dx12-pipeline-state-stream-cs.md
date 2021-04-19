---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_CS (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever um sombreador de computação como um único objeto adequado para uma descrição de fluxo.
ms.assetid: B76B0CB4-FC76-4C5B-84FC-DCFF907BE2F8
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_CS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_CS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5796e0f96ad4e2a87d2a45519321c363078a34b1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763920"
---
# <a name="cd3dx12_pipeline_state_stream_cs-structure"></a><span data-ttu-id="2a1c1-104">\_Estrutura de \_ cs do fluxo de estado do pipeline do \_ CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="2a1c1-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_CS structure</span></span>

<span data-ttu-id="2a1c1-105">Uma estrutura auxiliar usada para descrever um sombreador de computação como um único objeto adequado para uma descrição de fluxo.</span><span class="sxs-lookup"><span data-stu-id="2a1c1-105">A helper structure used to describe a compute shader as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a1c1-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2a1c1-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_CS {
                                   CD3DX12_PIPELINE_STATE_STREAM_CS;
                                   CD3DX12_PIPELINE_STATE_STREAM_CS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_CS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a><span data-ttu-id="2a1c1-107">Membros</span><span class="sxs-lookup"><span data-stu-id="2a1c1-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2a1c1-108">**\_Fluxo de \_ estado do pipeline \_ do CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="2a1c1-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CS**</span></span>
</dt> <dd>

<span data-ttu-id="2a1c1-109">Cria uma instância nova e não inicializada de um fluxo de \_ estado do pipeline do CD3DX12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2a1c1-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_CS.</span></span>

</dd> <dt>

<span data-ttu-id="2a1c1-110">**CD3DX12 \_ pipeline \_ \_ de fluxo \_ de estado cs (D3D12 do \_ código de bytes do sombreador do \_ am&i)**</span><span class="sxs-lookup"><span data-stu-id="2a1c1-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CS(D3D12\_SHADER\_BYTECODE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="2a1c1-111">Cria uma nova instância de um fluxo de estado do pipeline do CD3DX12 \_ \_ \_ \_ , inicializado com um tipo de subobjeto do tipo de subobjeto do **estado do \_ pipeline D3D12 \_ \_ \_ \_ cs** e os dados de subobjeto copiados de *i*, uma estrutura de [**código de \_ \_ bytes do sombreador D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="2a1c1-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_CS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_CS** and subobject data copied from *i*, a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2a1c1-112">**Operator = (D3D12 do \_ código de bytes do sombreador de \_ Radio& i)**</span><span class="sxs-lookup"><span data-stu-id="2a1c1-112">**operator=(D3D12\_SHADER\_BYTECODE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="2a1c1-113">Operador de atribuição de cópia.</span><span class="sxs-lookup"><span data-stu-id="2a1c1-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="2a1c1-114">**\_ \_ constante de código de bytes do sombreador D3D12 do operador ()**</span><span class="sxs-lookup"><span data-stu-id="2a1c1-114">**operator D3D12\_SHADER\_BYTECODE() const**</span></span>
</dt> <dd>

<span data-ttu-id="2a1c1-115">Conversão implícita em uma estrutura de [**\_ código de \_ bytes do sombreador D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="2a1c1-115">Implicit conversion to a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a1c1-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a1c1-116">Remarks</span></span>

<span data-ttu-id="2a1c1-117">\_ \_ \_ O fluxo de estado \_ do pipeline CD3DX12 é uma especialização de typedef do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2a1c1-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_CS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_CS>
    CD3DX12_PIPELINE_STATE_STREAM_CS;
          
```



## <a name="requirements"></a><span data-ttu-id="2a1c1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a1c1-118">Requirements</span></span>



| <span data-ttu-id="2a1c1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a1c1-119">Requirement</span></span> | <span data-ttu-id="2a1c1-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2a1c1-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2a1c1-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2a1c1-121">Header</span></span><br/> | <dl> <span data-ttu-id="2a1c1-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a1c1-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a1c1-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a1c1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a1c1-124">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="2a1c1-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="2a1c1-125">**Subobjeto de fluxo do estado do \_ pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2a1c1-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="2a1c1-126">**\_Tipo de \_ subobjeto de estado de pipeline D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2a1c1-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

