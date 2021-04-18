---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_DS (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever um sombreador de domínio como um único objeto adequado para uma descrição de fluxo.
ms.assetid: 42F8B7C1-B754-4B07-BF04-DBF450A942E6
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_DS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbae1d75894e1fb8ffaa5bf95a45cc1eb3b2d9f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105748887"
---
# <a name="cd3dx12_pipeline_state_stream_ds-structure"></a><span data-ttu-id="35e55-104">\_ \_ \_ Estrutura DS do fluxo de estado do pipeline do CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="35e55-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_DS structure</span></span>

<span data-ttu-id="35e55-105">Uma estrutura auxiliar usada para descrever um sombreador de domínio como um único objeto adequado para uma descrição de fluxo.</span><span class="sxs-lookup"><span data-stu-id="35e55-105">A helper structure used to describe a domain shader as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="35e55-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35e55-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DS {
                                   CD3DX12_PIPELINE_STATE_STREAM_DS;
                                   CD3DX12_PIPELINE_STATE_STREAM_DS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a><span data-ttu-id="35e55-107">Membros</span><span class="sxs-lookup"><span data-stu-id="35e55-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="35e55-108">**Fluxo de estado do pipeline do CD3DX12 \_ \_ \_ \_ DS**</span><span class="sxs-lookup"><span data-stu-id="35e55-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DS**</span></span>
</dt> <dd>

<span data-ttu-id="35e55-109">Cria uma nova instância, não inicializada, de um fluxo de estado de pipeline do CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="35e55-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DS.</span></span>

</dd> <dt>

<span data-ttu-id="35e55-110">**\_ \_ \_ Fluxo \_ de estado do pipeline do CD3DX12 DS (D3D12 do \_ código de bytes do sombreador do \_ am&**</span><span class="sxs-lookup"><span data-stu-id="35e55-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DS(D3D12\_SHADER\_BYTECODE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="35e55-111">Cria uma nova instância de um fluxo de estado do pipeline do CD3DX12 \_ \_ \_ \_ , inicializada com um tipo de subobjeto do tipo de subobjeto do perfil do D3D12 e dados de subobjeto **\_ \_ \_ \_ \_ DS** e SubObject copiados de *i*, uma estrutura de [**código de \_ \_ bytes do sombreador D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="35e55-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DS** and subobject data copied from *i*, a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="35e55-112">**Operator = (D3D12 do \_ código de bytes do sombreador de \_ Radio& i)**</span><span class="sxs-lookup"><span data-stu-id="35e55-112">**operator=(D3D12\_SHADER\_BYTECODE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="35e55-113">Operador de atribuição de cópia.</span><span class="sxs-lookup"><span data-stu-id="35e55-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="35e55-114">**\_ \_ constante de código de bytes do sombreador D3D12 do operador ()**</span><span class="sxs-lookup"><span data-stu-id="35e55-114">**operator D3D12\_SHADER\_BYTECODE() const**</span></span>
</dt> <dd>

<span data-ttu-id="35e55-115">Conversão implícita em uma estrutura de [**\_ código de \_ bytes do sombreador D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="35e55-115">Implicit conversion to a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35e55-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="35e55-116">Remarks</span></span>

<span data-ttu-id="35e55-117">\_ \_ \_ O fluxo de estado \_ do pipeline do CD3DX12 DS é uma especialização de typedef do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="35e55-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_DS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DS>
    CD3DX12_PIPELINE_STATE_STREAM_DS;
          
```



## <a name="requirements"></a><span data-ttu-id="35e55-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35e55-118">Requirements</span></span>



| <span data-ttu-id="35e55-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="35e55-119">Requirement</span></span> | <span data-ttu-id="35e55-120">Valor</span><span class="sxs-lookup"><span data-stu-id="35e55-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="35e55-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="35e55-121">Header</span></span><br/> | <dl> <span data-ttu-id="35e55-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="35e55-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35e55-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="35e55-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35e55-124">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="35e55-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="35e55-125">**Subobjeto de fluxo do estado do \_ pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="35e55-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="35e55-126">**\_Tipo de \_ subobjeto de estado de pipeline D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="35e55-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

