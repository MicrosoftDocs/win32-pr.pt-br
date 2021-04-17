---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever uma máscara de exemplo como um único objeto adequado para uma descrição de fluxo.
ms.assetid: 20116DA1-F56D-42CA-A846-42509FAF88C1
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 868a498bec1bbf8c4f55f320765272d04cbdd81c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105790495"
---
# <a name="cd3dx12_pipeline_state_stream_sample_mask-structure"></a><span data-ttu-id="8e724-104">\_Estrutura da \_ \_ máscara de exemplo do fluxo de estado do \_ pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="8e724-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK structure</span></span>

<span data-ttu-id="8e724-105">Uma estrutura auxiliar usada para descrever uma máscara de exemplo como um único objeto adequado para uma descrição de fluxo.</span><span class="sxs-lookup"><span data-stu-id="8e724-105">A helper structure used to describe a sample mask as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e724-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e724-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK {
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK;
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK(UINT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK operator=(UINT const& i);
                                            operator UINT() const;
};
```



## <a name="members"></a><span data-ttu-id="8e724-107">Membros</span><span class="sxs-lookup"><span data-stu-id="8e724-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8e724-108">**\_Máscara de \_ exemplo de fluxo de estado de pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8e724-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK**</span></span>
</dt> <dd>

<span data-ttu-id="8e724-109">Cria uma nova instância, não inicializada, de uma \_ máscara de exemplo de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8e724-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK.</span></span>

</dd> <dt>

<span data-ttu-id="8e724-110">**\_ \_ \_ \_ \_ Máscara de exemplo de fluxo de estado de PIPELINE CD3DX12 (UINT const &i)**</span><span class="sxs-lookup"><span data-stu-id="8e724-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK(UINT const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="8e724-111">Cria uma nova instância de uma \_ máscara de exemplo de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ , inicializada com um tipo de subobjeto de tipo de subobjeto de **estado de pipeline D3D12 \_ \_ \_ \_ \_ \_ máscara de exemplo** e dados de subobjeto copiados de *i*, uma máscara de exemplo **uint** .</span><span class="sxs-lookup"><span data-stu-id="8e724-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_SAMPLE\_MASK** and subobject data copied from *i*, a **UINT** sample mask.</span></span>

</dd> <dt>

<span data-ttu-id="8e724-112">**Operator = (UINT const& i)**</span><span class="sxs-lookup"><span data-stu-id="8e724-112">**operator=(UINT const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="8e724-113">Operador de atribuição de cópia.</span><span class="sxs-lookup"><span data-stu-id="8e724-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="8e724-114">**constante de operador UINT ()**</span><span class="sxs-lookup"><span data-stu-id="8e724-114">**operator UINT() const**</span></span>
</dt> <dd>

<span data-ttu-id="8e724-115">Conversão implícita em uma máscara de exemplo **uint** .</span><span class="sxs-lookup"><span data-stu-id="8e724-115">Implicit conversion to a **UINT** sample mask.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e724-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e724-116">Remarks</span></span>

<span data-ttu-id="8e724-117">\_ \_ \_ \_ \_ A máscara de exemplo de fluxo de estado do pipeline CD3DX12 é uma especialização de TYPEDEF do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="8e724-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<UINT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_SAMPLE_MASK>
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK;
          
```



## <a name="requirements"></a><span data-ttu-id="8e724-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e724-118">Requirements</span></span>



| <span data-ttu-id="8e724-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e724-119">Requirement</span></span> | <span data-ttu-id="8e724-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8e724-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8e724-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8e724-121">Header</span></span><br/> | <dl> <span data-ttu-id="8e724-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e724-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e724-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e724-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e724-124">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="8e724-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="8e724-125">**Subobjeto de fluxo do estado do \_ pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8e724-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="8e724-126">**\_Tipo de \_ subobjeto de estado de pipeline D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8e724-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

