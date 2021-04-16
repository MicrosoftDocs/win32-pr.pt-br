---
title: Estrutura de CD3DX12_SUBRESOURCE_RANGE_UINT64 (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura UINT64 de intervalo de subrecursos do D3D12 \_ \_ .
ms.assetid: 607A60ED-98D2-4A77-9A7A-6B54342EA101
keywords:
- Estrutura de CD3DX12_SUBRESOURCE_RANGE_UINT64
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2aea83d993c0c7b58ded8d0b92374d1dcbacdcc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105808257"
---
# <a name="cd3dx12_subresource_range_uint64-structure"></a><span data-ttu-id="0af0f-104">\_ \_ Estrutura UINT64 do intervalo de subrecursos do CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="0af0f-104">CD3DX12\_SUBRESOURCE\_RANGE\_UINT64 structure</span></span>

<span data-ttu-id="0af0f-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ UINT64 de \_ intervalo \_ de subrecursos do D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) .</span><span class="sxs-lookup"><span data-stu-id="0af0f-105">A helper structure to enable easy initialization of a [**D3D12\_SUBRESOURCE\_RANGE\_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="0af0f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0af0f-106">Syntax</span></span>


```C++
struct CD3DX12_SUBRESOURCE_RANGE_UINT64  : public D3D12_SUBRESOURCE_RANGE_UINT64{
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64();
  CD3DX12_SUBRESOURCE_RANGE_UINT64 explicit CD3DX12_SUBRESOURCE_RANGE_UINT64(const D3D12_SUBRESOURCE_RANGE_UINT64 &o);
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64(UINT subresource, const D3D12_RANGE_UINT64& range);
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64(UINT subresource, UINT64 begin, UINT64 end);
                                   operator const D3D12_SUBRESOURCE_RANGE_UINT64&() const;
};
```



## <a name="members"></a><span data-ttu-id="0af0f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="0af0f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0af0f-108">**CD3DX12 \_ \_ do intervalo de subrecurso \_ UINT64 ()**</span><span class="sxs-lookup"><span data-stu-id="0af0f-108">**CD3DX12\_SUBRESOURCE\_RANGE\_UINT64()**</span></span>
</dt> <dd>

<span data-ttu-id="0af0f-109">Cria uma nova instância não inicializada de um CD3DX12 do \_ intervalo de subrecurso \_ \_ UINT64.</span><span class="sxs-lookup"><span data-stu-id="0af0f-109">Creates a new, uninitialized, instance of a CD3DX12\_SUBRESOURCE\_RANGE\_UINT64.</span></span>

</dd> <dt>

<span data-ttu-id="0af0f-110">**\_intervalo de SUBRECURSO CD3DX12 explícito \_ \_ UINT64 (const D3D12 \_ intervalo de subrecurso \_ \_ UInt64 &o)**</span><span class="sxs-lookup"><span data-stu-id="0af0f-110">**explicit CD3DX12\_SUBRESOURCE\_RANGE\_UINT64(const D3D12\_SUBRESOURCE\_RANGE\_UINT64 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="0af0f-111">Cria uma nova instância de um CD3DX12 do \_ intervalo de subrecurso \_ \_ UINT64, inicializada com valores copiados de uma estrutura UInt64 do [**\_ \_ intervalo \_ de subrecurso do D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) .</span><span class="sxs-lookup"><span data-stu-id="0af0f-111">Creates a new instance of a CD3DX12\_SUBRESOURCE\_RANGE\_UINT64, initialized with values copied from a [**D3D12\_SUBRESOURCE\_RANGE\_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0af0f-112">**CD3DX12 \_ do intervalo de subrecurso \_ \_ UInt64 (subrecurso uint, D3D12 do \_ intervalo de& const \_ UINT64)**</span><span class="sxs-lookup"><span data-stu-id="0af0f-112">**CD3DX12\_SUBRESOURCE\_RANGE\_UINT64(UINT subresource, const D3D12\_RANGE\_UINT64& range)**</span></span>
</dt> <dd>

<span data-ttu-id="0af0f-113">Cria uma nova instância de um estêncil de profundidade de CD3DX12 \_ \_ \_ DESC1, inicializada com os valores passados na lista de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0af0f-113">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.</span></span>

</dd> <dt>

<span data-ttu-id="0af0f-114">**CD3DX12 \_ do intervalo de subrecurso \_ \_ UINT64 (subrecurso uint, UINT64 Begin, UInt64 end)**</span><span class="sxs-lookup"><span data-stu-id="0af0f-114">**CD3DX12\_SUBRESOURCE\_RANGE\_UINT64(UINT subresource, UINT64 begin, UINT64 end)**</span></span>
</dt> <dd>

<span data-ttu-id="0af0f-115">Cria uma nova instância de um estêncil de profundidade de CD3DX12 \_ \_ \_ DESC1, inicializada com os valores passados na lista de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0af0f-115">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.</span></span>

</dd> <dt>

<span data-ttu-id="0af0f-116">**D3D12 const \_ \_ de subconjunto de subrecurso \_ UINT64& () const**</span><span class="sxs-lookup"><span data-stu-id="0af0f-116">**operator const D3D12\_SUBRESOURCE\_RANGE\_UINT64&() const**</span></span>
</dt> <dd>

<span data-ttu-id="0af0f-117">Conversão implícita em uma \_ estrutura UINT64 do intervalo de SUBrecursos do D3D12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0af0f-117">Implicit conversion to a D3D12\_SUBRESOURCE\_RANGE\_UINT64 structure.</span></span> <span data-ttu-id="0af0f-118">Como \_ o intervalo de SUBrecursos do D3D12 \_ \_ UInt64 é o tipo subjacente do \_ intervalo de subrecursos do CD3DX12 \_ \_ UInt64, o objeto é simplesmente retornado como um estêncil const D3D12 \_ Depth \_ \_ DESC1 referência a si mesmo.</span><span class="sxs-lookup"><span data-stu-id="0af0f-118">Because D3D12\_SUBRESOURCE\_RANGE\_UINT64 is the underlying type of CD3DX12\_SUBRESOURCE\_RANGE\_UINT64, the object is simply returned as a const D3D12\_DEPTH\_STENCIL\_DESC1 reference to itself.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0af0f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0af0f-119">Requirements</span></span>



| <span data-ttu-id="0af0f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0af0f-120">Requirement</span></span> | <span data-ttu-id="0af0f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="0af0f-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0af0f-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0af0f-122">Header</span></span><br/> | <dl> <span data-ttu-id="0af0f-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="0af0f-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0af0f-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="0af0f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0af0f-125">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="0af0f-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="0af0f-126">**D3D12 do \_ intervalo de subrecurso \_ \_ UINT64**</span><span class="sxs-lookup"><span data-stu-id="0af0f-126">**D3D12\_SUBRESOURCE\_RANGE\_UINT64**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64)
</dt> </dl>

 

 





