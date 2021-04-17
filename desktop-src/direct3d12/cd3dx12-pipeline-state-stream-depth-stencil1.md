---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever uma descrição de estêncil de profundidade como um único objeto adequado para uma descrição de fluxo. | Estrutura de CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 (D3dx12. h)
ms.assetid: 7D3554D9-610D-43B5-94F0-68167E966A86
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee95e9e37ad1dfced119848c76f071564aaa9435
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105748668"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil1-structure"></a><span data-ttu-id="b9598-105">\_ \_ \_ \_ Estrutura STENCIL1 de profundidade de fluxo do CD3DX12 pipeline \_</span><span class="sxs-lookup"><span data-stu-id="b9598-105">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1 structure</span></span>

<span data-ttu-id="b9598-106">Uma estrutura auxiliar usada para descrever uma descrição de estêncil de profundidade como um único objeto adequado para uma descrição de fluxo.</span><span class="sxs-lookup"><span data-stu-id="b9598-106">A helper structure used to describe a depth stencil description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9598-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9598-107">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 {
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1(CD3DX12_DEPTH_STENCIL_DESC1 const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 operator=(CD3DX12_DEPTH_STENCIL_DESC1 const& i);
                                               operator CD3DX12_DEPTH_STENCIL_DESC1() const;
};
```



## <a name="members"></a><span data-ttu-id="b9598-108">Membros</span><span class="sxs-lookup"><span data-stu-id="b9598-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b9598-109">**\_STENCIL1 de \_ profundidade de fluxo de estado de pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b9598-109">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1**</span></span>
</dt> <dd>

<span data-ttu-id="b9598-110">Cria uma instância nova e não inicializada de uma STENCIL1 de \_ profundidade de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b9598-110">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1.</span></span>

</dd> <dt>

<span data-ttu-id="b9598-111">**CD3DX12 \_ \_ \_ \_ de camada de estado \_ de pipeline de STENCIL1 ( \_ estêncil de profundidade CD3DX12 \_ \_ DESC1 const &i)**</span><span class="sxs-lookup"><span data-stu-id="b9598-111">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1(CD3DX12\_DEPTH\_STENCIL\_DESC1 const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="b9598-112">Cria uma nova instância de uma STENCIL1 de profundidade de fluxo de estado de pipeline do CD3DX12 \_ \_ \_ \_ \_ , inicializada com um tipo de subobjeto de subobjeto de **perfil de D3D12 do estado de \_ pipeline \_ \_ \_ \_ \_ STENCIL1** e dados de subobjeto copiados de *i*, uma estrutura [**CD3DX12 de \_ \_ estêncil \_ de profundidade**](cd3dx12-depth-stencil-desc1.md) DESC1.</span><span class="sxs-lookup"><span data-stu-id="b9598-112">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL1** and subobject data copied from *i*, a [**CD3DX12\_DEPTH\_STENCIL\_DESC1**](cd3dx12-depth-stencil-desc1.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b9598-113">**Operator = (estêncil de profundidade de CD3DX12 \_ \_ \_ DESC1 const& i)**</span><span class="sxs-lookup"><span data-stu-id="b9598-113">**operator=(CD3DX12\_DEPTH\_STENCIL\_DESC1 const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="b9598-114">Operador de atribuição de cópia.</span><span class="sxs-lookup"><span data-stu-id="b9598-114">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="b9598-115">**\_ \_ \_ const de estêncil de profundidade de CD3DX12 de operador DESC1 ()**</span><span class="sxs-lookup"><span data-stu-id="b9598-115">**operator CD3DX12\_DEPTH\_STENCIL\_DESC1() const**</span></span>
</dt> <dd>

<span data-ttu-id="b9598-116">Conversão implícita em uma [**estrutura \_ \_ \_ DESC1 de estêncil de profundidade de CD3DX12**](cd3dx12-depth-stencil-desc1.md) .</span><span class="sxs-lookup"><span data-stu-id="b9598-116">Implicit conversion to a [**CD3DX12\_DEPTH\_STENCIL\_DESC1**](cd3dx12-depth-stencil-desc1.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9598-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9598-117">Remarks</span></span>

<span data-ttu-id="b9598-118">\_O CD3DX12 \_ pipeline \_ \_ de extensão \_ de fluxo STENCIL1 é uma especialização de TYPEDEF do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b9598-118">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1 is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC1, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL1, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
          
```



## <a name="requirements"></a><span data-ttu-id="b9598-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9598-119">Requirements</span></span>



| <span data-ttu-id="b9598-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9598-120">Requirement</span></span> | <span data-ttu-id="b9598-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b9598-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b9598-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b9598-122">Header</span></span><br/> | <dl> <span data-ttu-id="b9598-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9598-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9598-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9598-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9598-125">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="b9598-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="b9598-126">**Subobjeto de fluxo do estado do \_ pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b9598-126">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="b9598-127">**\_Tipo de \_ subobjeto de estado de pipeline D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b9598-127">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

