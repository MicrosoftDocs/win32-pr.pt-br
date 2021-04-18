---
title: Estrutura de CD3DX12_RANGE_UINT64 (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura UINT64 do intervalo de D3D12 \_ .
ms.assetid: 789A2C46-B7D4-462E-9C10-69FD63D27491
keywords:
- Estrutura de CD3DX12_RANGE_UINT64
topic_type:
- apiref
api_name:
- CD3DX12_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89c408197afb1254cae922c402939f6f169708d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812245"
---
# <a name="cd3dx12_range_uint64-structure"></a><span data-ttu-id="e9968-104">Estrutura de UINT64 do \_ intervalo de CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="e9968-104">CD3DX12\_RANGE\_UINT64 structure</span></span>

<span data-ttu-id="e9968-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ \_ UINT64 do intervalo de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) .</span><span class="sxs-lookup"><span data-stu-id="e9968-105">A helper structure to enable easy initialization of a [**D3D12\_RANGE\_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9968-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9968-106">Syntax</span></span>


```C++
struct CD3DX12_RANGE_UINT64  : public D3D12_RANGE_UINT64{
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64();
  CD3DX12_RANGE_UINT64 explicit CD3DX12_RANGE_UINT64(const D3D12_RANGE_UINT64 &o);
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64(UINT64 begin, UINT64 end);
                       operator const D3D12_RANGE_UINT64&() const;
};
```



## <a name="members"></a><span data-ttu-id="e9968-107">Membros</span><span class="sxs-lookup"><span data-stu-id="e9968-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e9968-108">**CD3DX12 \_ \_ do intervalo UINT64 ()**</span><span class="sxs-lookup"><span data-stu-id="e9968-108">**CD3DX12\_RANGE\_UINT64()**</span></span>
</dt> <dd>

<span data-ttu-id="e9968-109">Cria uma nova instância, não inicializada, de um CD3DX12 do \_ intervalo \_ UINT64.</span><span class="sxs-lookup"><span data-stu-id="e9968-109">Creates a new, uninitialized, instance of a CD3DX12\_RANGE\_UINT64.</span></span>

</dd> <dt>

<span data-ttu-id="e9968-110">**intervalo CD3DX12 \_ explícito \_ UInt64 (const D3D12 \_ intervalo \_ UInt64 &o)**</span><span class="sxs-lookup"><span data-stu-id="e9968-110">**explicit CD3DX12\_RANGE\_UINT64(const D3D12\_RANGE\_UINT64 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="e9968-111">Cria uma nova instância de um CD3DX12 do \_ intervalo \_ UInt64, inicializada com valores copiados de uma estrutura [**\_ \_ UInt64 do intervalo D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) .</span><span class="sxs-lookup"><span data-stu-id="e9968-111">Creates a new instance of a CD3DX12\_RANGE\_UINT64, initialized with values copied from a [**D3D12\_RANGE\_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e9968-112">**CD3DX12 \_ \_ do intervalo UINT64 (UInt64 Begin, UInt64 end)**</span><span class="sxs-lookup"><span data-stu-id="e9968-112">**CD3DX12\_RANGE\_UINT64(UINT64 begin, UINT64 end)**</span></span>
</dt> <dd>

<span data-ttu-id="e9968-113">Cria uma nova instância de um estêncil de profundidade de CD3DX12 \_ \_ \_ DESC1, inicializada com os valores passados na lista de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e9968-113">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.</span></span>

</dd> <dt>

<span data-ttu-id="e9968-114">**\_const D3D12 do intervalo \_ de variação do operador UINT64& () constante**</span><span class="sxs-lookup"><span data-stu-id="e9968-114">**operator const D3D12\_RANGE\_UINT64&() const**</span></span>
</dt> <dd>

<span data-ttu-id="e9968-115">Conversão implícita em uma \_ estrutura UINT64 do intervalo de D3D12 \_ .</span><span class="sxs-lookup"><span data-stu-id="e9968-115">Implicit conversion to a D3D12\_RANGE\_UINT64 structure.</span></span> <span data-ttu-id="e9968-116">Como \_ o intervalo \_ de D3D12 UInt64 é o tipo subjacente do CD3DX12 \_ Range \_ UInt64, o objeto é simplesmente retornado como uma referência a um intervalo de D3D12 const \_ \_ para si mesmo.</span><span class="sxs-lookup"><span data-stu-id="e9968-116">Because D3D12\_RANGE\_UINT64 is the underlying type of CD3DX12\_RANGE\_UINT64, the object is simply returned as a const D3D12\_RANGE\_UINT64 reference to itself.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9968-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9968-117">Requirements</span></span>



| <span data-ttu-id="e9968-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9968-118">Requirement</span></span> | <span data-ttu-id="e9968-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e9968-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e9968-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e9968-120">Header</span></span><br/> | <dl> <span data-ttu-id="e9968-121"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9968-121"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9968-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9968-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9968-123">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="e9968-123">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="e9968-124">**D3D12 do \_ intervalo \_ UINT64**</span><span class="sxs-lookup"><span data-stu-id="e9968-124">**D3D12\_RANGE\_UINT64**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64)
</dt> </dl>

 

 





