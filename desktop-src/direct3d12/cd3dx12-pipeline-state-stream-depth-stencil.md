---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever uma descrição de estêncil de profundidade como um único objeto adequado para uma descrição de fluxo. | Estrutura de CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL (D3dx12. h)
ms.assetid: 4FB54EA5-FCC6-4B64-A747-27DFE4C1D2DC
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb24779aeff950bd213ce18774f55493777df9c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105757181"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil-structure"></a><span data-ttu-id="f5759-105">\_Estrutura de \_ \_ estêncil de profundidade do fluxo de estado do \_ pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="f5759-105">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL structure</span></span>

<span data-ttu-id="f5759-106">Uma estrutura auxiliar usada para descrever uma descrição de estêncil de profundidade como um único objeto adequado para uma descrição de fluxo.</span><span class="sxs-lookup"><span data-stu-id="f5759-106">A helper structure used to describe a depth stencil description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5759-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5759-107">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL {
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL(CD3DX12_DEPTH_STENCIL_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL operator=(CD3DX12_DEPTH_STENCIL_DESC const& i);
                                              operator CD3DX12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="f5759-108">Membros</span><span class="sxs-lookup"><span data-stu-id="f5759-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f5759-109">**\_Estêncil de \_ profundidade do fluxo de estado do pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f5759-109">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL**</span></span>
</dt> <dd>

<span data-ttu-id="f5759-110">Cria uma nova instância, não inicializada, de um \_ estêncil de profundidade de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f5759-110">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL.</span></span>

</dd> <dt>

<span data-ttu-id="f5759-111">**\_ \_ \_ \_ \_ Estêncil de profundidade de fluxo de estado de pipeline CD3DX12 ( \_ estêncil de profundidade CD3DX12 \_ \_ desc const &i)**</span><span class="sxs-lookup"><span data-stu-id="f5759-111">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL(CD3DX12\_DEPTH\_STENCIL\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="f5759-112">Cria uma nova instância de um estêncil de profundidade do fluxo de estado do pipeline do CD3DX12 \_ \_ \_ \_ \_ , inicializado com um tipo de subobjeto do subobjeto do **estado do pipeline D3D12 de \_ \_ \_ \_ \_ \_ estêncil** de profundidade e dados de subobjeto copiados de *i*, uma estrutura [**desc de \_ estêncil de profundidade \_ \_ CD3DX12**](cd3dx12-depth-stencil-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="f5759-112">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL** and subobject data copied from *i*, a [**CD3DX12\_DEPTH\_STENCIL\_DESC**](cd3dx12-depth-stencil-desc.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f5759-113">**Operator = ( \_ estêncil de profundidade CD3DX12 \_ \_ desc const& i)**</span><span class="sxs-lookup"><span data-stu-id="f5759-113">**operator=(CD3DX12\_DEPTH\_STENCIL\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="f5759-114">Operador de atribuição de cópia.</span><span class="sxs-lookup"><span data-stu-id="f5759-114">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="f5759-115">**\_ \_ \_ const do estêncil de profundidade do CD3DX12 do operador DESC ()**</span><span class="sxs-lookup"><span data-stu-id="f5759-115">**operator CD3DX12\_DEPTH\_STENCIL\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="f5759-116">Conversão implícita em uma [**estrutura \_ \_ \_ desc de estêncil de profundidade de CD3DX12**](cd3dx12-depth-stencil-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="f5759-116">Implicit conversion to a [**CD3DX12\_DEPTH\_STENCIL\_DESC**](cd3dx12-depth-stencil-desc.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5759-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5759-117">Remarks</span></span>

<span data-ttu-id="f5759-118">\_ \_ \_ \_ \_ O estêncil de profundidade do fluxo de estado do pipeline CD3DX12 é uma especialização de TYPEDEF do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="f5759-118">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
          
```



## <a name="requirements"></a><span data-ttu-id="f5759-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5759-119">Requirements</span></span>



| <span data-ttu-id="f5759-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5759-120">Requirement</span></span> | <span data-ttu-id="f5759-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f5759-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f5759-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f5759-122">Header</span></span><br/> | <dl> <span data-ttu-id="f5759-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5759-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5759-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5759-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5759-125">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="f5759-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="f5759-126">**Subobjeto de fluxo do estado do \_ pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f5759-126">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="f5759-127">**\_Tipo de \_ subobjeto de estado de pipeline D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f5759-127">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

