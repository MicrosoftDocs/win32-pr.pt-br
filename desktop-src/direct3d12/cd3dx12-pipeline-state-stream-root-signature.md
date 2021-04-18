---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever a assinatura raiz como um único objeto adequado para uma descrição de fluxo.
ms.assetid: 351A78DC-9BDE-43B4-9A72-D65EE15CA441
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a97402fa267693de23ed2085b3d41973dc409e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105785022"
---
# <a name="cd3dx12_pipeline_state_stream_root_signature-structure"></a><span data-ttu-id="784be-104">\_Estrutura de \_ \_ \_ assinatura raiz do fluxo de estado do pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="784be-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE structure</span></span>

<span data-ttu-id="784be-105">Uma estrutura auxiliar usada para descrever a assinatura raiz como um único objeto adequado para uma descrição de fluxo.</span><span class="sxs-lookup"><span data-stu-id="784be-105">A helper structure used to describe the root signature as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="784be-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="784be-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE {
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE(ID3D12RootSignature* const &i);
  CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE operator=(ID3D12RootSignature* const& i);
                                               operator ID3D12RootSignature*() const;
};
```



## <a name="members"></a><span data-ttu-id="784be-107">Membros</span><span class="sxs-lookup"><span data-stu-id="784be-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="784be-108">**\_ \_ \_ Assinatura raiz do fluxo de estado \_ do pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="784be-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE**</span></span>
</dt> <dd>

<span data-ttu-id="784be-109">Cria uma nova instância, não inicializada, de uma \_ assinatura raiz do fluxo de estado do pipeline CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="784be-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE.</span></span>

</dd> <dt>

<span data-ttu-id="784be-110">**\_ \_ \_ \_ Assinatura raiz do fluxo de estado do pipeline CD3DX12 \_ (ID3D12RootSignature \* const &i)**</span><span class="sxs-lookup"><span data-stu-id="784be-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE(ID3D12RootSignature\* const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="784be-111">Cria uma nova instância de uma \_ assinatura raiz do fluxo de estado do pipeline do CD3DX12 \_ \_ \_ \_ , inicializada com um tipo de subobjeto de **\_ \_ \_ \_ \_ \_ assinatura raiz do tipo** de subobjeto do estado do pipeline D3D12 e dados de subobjeto copiados de *i*, uma estrutura [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) .</span><span class="sxs-lookup"><span data-stu-id="784be-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_ROOT\_SIGNATURE** and subobject data copied from *i*, a [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) structure.</span></span>

</dd> <dt>

<span data-ttu-id="784be-112">**Operator = (ID3D12RootSignature \* const& i)**</span><span class="sxs-lookup"><span data-stu-id="784be-112">**operator=(ID3D12RootSignature\* const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="784be-113">Operador de atribuição de cópia.</span><span class="sxs-lookup"><span data-stu-id="784be-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="784be-114">**constante ID3D12RootSignature \* () de operador**</span><span class="sxs-lookup"><span data-stu-id="784be-114">**operator ID3D12RootSignature\*() const**</span></span>
</dt> <dd>

<span data-ttu-id="784be-115">Conversão implícita em um ponteiro de estrutura [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) .</span><span class="sxs-lookup"><span data-stu-id="784be-115">Implicit conversion to a [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) structure pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="784be-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="784be-116">Remarks</span></span>

<span data-ttu-id="784be-117">\_ \_ \_ \_ \_ A assinatura raiz do fluxo de estado do pipeline CD3DX12 é uma especialização de TYPEDEF do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="784be-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<ID3D12RootSignature*, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_ROOT_SIGNATURE>
    CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
          
```



## <a name="requirements"></a><span data-ttu-id="784be-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="784be-118">Requirements</span></span>



| <span data-ttu-id="784be-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="784be-119">Requirement</span></span> | <span data-ttu-id="784be-120">Valor</span><span class="sxs-lookup"><span data-stu-id="784be-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="784be-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="784be-121">Header</span></span><br/> | <dl> <span data-ttu-id="784be-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="784be-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="784be-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="784be-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="784be-124">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="784be-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="784be-125">**Subobjeto de fluxo do estado do \_ pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="784be-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="784be-126">**\_Tipo de \_ subobjeto de estado de pipeline D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="784be-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

