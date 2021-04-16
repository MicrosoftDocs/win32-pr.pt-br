---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever o formato de estêncil de profundidade como um único objeto adequado para uma descrição de fluxo.
ms.assetid: 512DB46E-D8F0-482B-9174-C786FB91AFD2
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dc7ae2703ac80ac155c04d42624a081723288bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105750119"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil_format-structure"></a><span data-ttu-id="246e0-104">\_Estrutura do \_ \_ formato de \_ estêncil profundidade do fluxo de \_ estado do pipeline \_ CD3DX12</span><span class="sxs-lookup"><span data-stu-id="246e0-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT structure</span></span>

<span data-ttu-id="246e0-105">Uma estrutura auxiliar usada para descrever o formato de estêncil de profundidade como um único objeto adequado para uma descrição de fluxo.</span><span class="sxs-lookup"><span data-stu-id="246e0-105">A helper structure used to describe the depth stencil format as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="246e0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="246e0-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT {
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT(DXGI_FORMAT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT operator=(DXGI_FORMAT const& i);
                                                     operator DXGI_FORMAT() const;
};
```



## <a name="members"></a><span data-ttu-id="246e0-107">Membros</span><span class="sxs-lookup"><span data-stu-id="246e0-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="246e0-108">**\_Formato de \_ \_ estêncil de profundidade do fluxo de estado \_ do \_ pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="246e0-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT**</span></span>
</dt> <dd>

<span data-ttu-id="246e0-109">Cria uma nova instância, não inicializada, de um \_ formato de estêncil de profundidade de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="246e0-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT.</span></span>

</dd> <dt>

<span data-ttu-id="246e0-110">**\_ \_ \_ \_ \_ \_ Formato de estêncil de profundidade de fluxo de estado de PIPELINE CD3DX12 ( \_ formato dxgi const &i)**</span><span class="sxs-lookup"><span data-stu-id="246e0-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT(DXGI\_FORMAT const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="246e0-111">Cria uma nova instância de um \_ formato de estêncil de profundidade de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ \_ , inicializada com um tipo de subobjeto do **\_ \_ \_ \_ \_ \_ \_ formato de estêncil profundidade de tipo** de subobjeto de perfil de D3D12 e dados de subobjeto copiados de *i*, uma enumeração de [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .</span><span class="sxs-lookup"><span data-stu-id="246e0-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL\_FORMAT** and subobject data copied from *i*, a [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="246e0-112">**Operator = ( \_ formato dxgi const& i)**</span><span class="sxs-lookup"><span data-stu-id="246e0-112">**operator=(DXGI\_FORMAT const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="246e0-113">Operador de atribuição de cópia.</span><span class="sxs-lookup"><span data-stu-id="246e0-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="246e0-114">**\_const do formato dxgi do operador ()**</span><span class="sxs-lookup"><span data-stu-id="246e0-114">**operator DXGI\_FORMAT() const**</span></span>
</dt> <dd>

<span data-ttu-id="246e0-115">Conversão implícita em uma enumeração de [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .</span><span class="sxs-lookup"><span data-stu-id="246e0-115">Implicit conversion to a [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="246e0-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="246e0-116">Remarks</span></span>

<span data-ttu-id="246e0-117">\_ \_ \_ \_ \_ \_ O formato de estêncil de profundidade do fluxo de estado do pipeline CD3DX12 é uma especialização de typedef do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="246e0-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_FORMAT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL_FORMAT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
          
```



## <a name="requirements"></a><span data-ttu-id="246e0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="246e0-118">Requirements</span></span>



| <span data-ttu-id="246e0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="246e0-119">Requirement</span></span> | <span data-ttu-id="246e0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="246e0-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="246e0-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="246e0-121">Header</span></span><br/> | <dl> <span data-ttu-id="246e0-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="246e0-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="246e0-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="246e0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="246e0-124">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="246e0-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="246e0-125">**Subobjeto de fluxo do estado do \_ pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="246e0-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="246e0-126">**\_Tipo de \_ subobjeto de estado de pipeline D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="246e0-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

