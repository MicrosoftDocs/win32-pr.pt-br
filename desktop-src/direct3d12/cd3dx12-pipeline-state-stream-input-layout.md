---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever um layout de entrada como um único objeto adequado para uma descrição de fluxo.
ms.assetid: CEAD9FA6-4FB0-492E-9E81-8C4900A1FBC5
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ba382552d700ddddee02cdc1343936e6bcf6837
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105749550"
---
# <a name="cd3dx12_pipeline_state_stream_input_layout-structure"></a><span data-ttu-id="08394-104">\_Estrutura de \_ \_ layout de entrada de fluxo de estado de \_ pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="08394-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT structure</span></span>

<span data-ttu-id="08394-105">Uma estrutura auxiliar usada para descrever um layout de entrada como um único objeto adequado para uma descrição de fluxo.</span><span class="sxs-lookup"><span data-stu-id="08394-105">A helper structure used to describe an input layout as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="08394-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08394-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT {
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT(D3D12_INPUT_LAYOUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT operator=(D3D12_INPUT_LAYOUT_DESC const& i);
                                             operator D3D12_INPUT_LAYOUT_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="08394-107">Membros</span><span class="sxs-lookup"><span data-stu-id="08394-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="08394-108">**\_Layout de \_ entrada de fluxo de estado de pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="08394-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT**</span></span>
</dt> <dd>

<span data-ttu-id="08394-109">Cria uma nova instância, não inicializada, de um \_ layout de entrada de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="08394-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT.</span></span>

</dd> <dt>

<span data-ttu-id="08394-110">**\_ \_ \_ \_ \_ Layout de entrada de fluxo de estado de pipeline CD3DX12 (D3D12 de \_ layout de entrada \_ \_ desc const &i)**</span><span class="sxs-lookup"><span data-stu-id="08394-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT(D3D12\_INPUT\_LAYOUT\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="08394-111">Cria uma nova instância de um \_ layout de entrada de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ , inicializada com um tipo de subobjeto do tipo de subobjeto de **estado de pipeline D3D12 \_ \_ \_ \_ \_ \_ layout de entrada** e dados de subobjeto copiados de *i*, uma estrutura [**\_ \_ \_ desc de layout de entrada D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) .</span><span class="sxs-lookup"><span data-stu-id="08394-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_INPUT\_LAYOUT** and subobject data copied from *i*, a [**D3D12\_INPUT\_LAYOUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="08394-112">**Operator = (D3D12 \_ Input \_ layout \_ desc const& i)**</span><span class="sxs-lookup"><span data-stu-id="08394-112">**operator=(D3D12\_INPUT\_LAYOUT\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="08394-113">Operador de atribuição de cópia.</span><span class="sxs-lookup"><span data-stu-id="08394-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="08394-114">**D3D12 \_ \_ \_ de layout de entrada do operador DESC () const**</span><span class="sxs-lookup"><span data-stu-id="08394-114">**operator D3D12\_INPUT\_LAYOUT\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="08394-115">Conversão implícita em uma [**estrutura \_ \_ \_ desc de layout de entrada D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) .</span><span class="sxs-lookup"><span data-stu-id="08394-115">Implicit conversion to a [**D3D12\_INPUT\_LAYOUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08394-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="08394-116">Remarks</span></span>

<span data-ttu-id="08394-117">\_ \_ \_ \_ \_ O layout de entrada do fluxo de estado do pipeline CD3DX12 é uma especialização de TYPEDEF do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="08394-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INPUT_LAYOUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_INPUT_LAYOUT>
    CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
          
```



## <a name="requirements"></a><span data-ttu-id="08394-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08394-118">Requirements</span></span>



| <span data-ttu-id="08394-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="08394-119">Requirement</span></span> | <span data-ttu-id="08394-120">Valor</span><span class="sxs-lookup"><span data-stu-id="08394-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="08394-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="08394-121">Header</span></span><br/> | <dl> <span data-ttu-id="08394-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="08394-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08394-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="08394-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08394-124">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="08394-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="08394-125">**Subobjeto de fluxo do estado do \_ pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="08394-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="08394-126">**\_Tipo de \_ subobjeto de estado de pipeline D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="08394-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

