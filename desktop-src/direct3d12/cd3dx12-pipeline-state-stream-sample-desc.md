---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever uma descrição de exemplo como um único objeto adequado para uma descrição de fluxo.
ms.assetid: D84C5373-AC0F-430A-97A1-6125611869B2
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fea786dc0429da28f9c26f0203b06059aff1c17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813484"
---
# <a name="cd3dx12_pipeline_state_stream_sample_desc-structure"></a><span data-ttu-id="c9cc2-104">\_ \_ \_ \_ Estrutura desc de amostra de fluxo de estado de pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="c9cc2-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC structure</span></span>

<span data-ttu-id="c9cc2-105">Uma estrutura auxiliar usada para descrever uma descrição de exemplo como um único objeto adequado para uma descrição de fluxo.</span><span class="sxs-lookup"><span data-stu-id="c9cc2-105">A helper structure used to describe a sample description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9cc2-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9cc2-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC {
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC(DXGI_SAMPLE_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC operator=(DXGI_SAMPLE_DESC const& i);
                                            operator DXGI_SAMPLE_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="c9cc2-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c9cc2-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c9cc2-108">**\_Exemplo de fluxo de estado do pipeline CD3DX12 \_ \_ \_ \_ desc**</span><span class="sxs-lookup"><span data-stu-id="c9cc2-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC**</span></span>
</dt> <dd>

<span data-ttu-id="c9cc2-109">Cria uma nova instância, não inicializada, de um \_ exemplo de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ desc.</span><span class="sxs-lookup"><span data-stu-id="c9cc2-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="c9cc2-110">**\_ \_ \_ \_ Exemplo de fluxo de estado \_ do pipeline CD3DX12 DESC (exemplo de dxgi \_ \_ desc const &i)**</span><span class="sxs-lookup"><span data-stu-id="c9cc2-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC(DXGI\_SAMPLE\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="c9cc2-111">Cria uma nova instância de um \_ exemplo de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ DESC, inicializada com um tipo de subobjeto de tipo de subobjeto de **estado de pipeline D3D12 amostra de dados \_ \_ \_ \_ \_ \_ desc** e subobjeto copiado de *i*, uma estrutura [**\_ \_ desc de amostra de dxgi**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) .</span><span class="sxs-lookup"><span data-stu-id="c9cc2-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_SAMPLE\_DESC** and subobject data copied from *i*, a [**DXGI\_SAMPLE\_DESC**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c9cc2-112">**Operator = ( \_ exemplo \_ DESC constante& i)**</span><span class="sxs-lookup"><span data-stu-id="c9cc2-112">**operator=(DXGI\_SAMPLE\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="c9cc2-113">Operador de atribuição de cópia.</span><span class="sxs-lookup"><span data-stu-id="c9cc2-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="c9cc2-114">**\_ \_ const do exemplo de dxgi do operador DESC ()**</span><span class="sxs-lookup"><span data-stu-id="c9cc2-114">**operator DXGI\_SAMPLE\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="c9cc2-115">Conversão implícita em uma [**estrutura \_ \_ desc de amostra de dxgi**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) .</span><span class="sxs-lookup"><span data-stu-id="c9cc2-115">Implicit conversion to a [**DXGI\_SAMPLE\_DESC**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9cc2-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9cc2-116">Remarks</span></span>

<span data-ttu-id="c9cc2-117">\_ \_ \_ \_ Exemplo de fluxo de estado \_ de pipeline CD3DX12 DESC é uma especialização de TYPEDEF do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c9cc2-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_SAMPLE_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_SAMPLE_DESC>
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
          
```



## <a name="requirements"></a><span data-ttu-id="c9cc2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9cc2-118">Requirements</span></span>



| <span data-ttu-id="c9cc2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9cc2-119">Requirement</span></span> | <span data-ttu-id="c9cc2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c9cc2-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c9cc2-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c9cc2-121">Header</span></span><br/> | <dl> <span data-ttu-id="c9cc2-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9cc2-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9cc2-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9cc2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9cc2-124">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="c9cc2-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="c9cc2-125">**Subobjeto de fluxo do estado do \_ pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c9cc2-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="c9cc2-126">**\_Tipo de \_ subobjeto de estado de pipeline D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c9cc2-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

