---
title: Estrutura de CD3DX12_RT_FORMAT_ARRAY (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de matriz de formato D3D12 RT \_ \_ .
ms.assetid: E890DD33-599F-4B20-BD15-2734867788E5
keywords:
- Estrutura de CD3DX12_RT_FORMAT_ARRAY
topic_type:
- apiref
api_name:
- CD3DX12_RT_FORMAT_ARRAY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c05b7ae9e51d2d6b2a43f45dc83bda2074f6b734
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762493"
---
# <a name="cd3dx12_rt_format_array-structure"></a><span data-ttu-id="07864-104">\_Estrutura de \_ matriz de formato CD3DX12 RT \_</span><span class="sxs-lookup"><span data-stu-id="07864-104">CD3DX12\_RT\_FORMAT\_ARRAY structure</span></span>

<span data-ttu-id="07864-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ matriz de \_ formato \_ D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .</span><span class="sxs-lookup"><span data-stu-id="07864-105">A helper structure to enable easy initialization of a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="07864-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07864-106">Syntax</span></span>


```C++
struct CD3DX12_RT_FORMAT_ARRAY  : public D3D12_RT_FORMAT_ARRAY{
  CD3DX12_RT_FORMAT_ARRAY CD3DX12_RT_FORMAT_ARRAY();
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const D3D12_RT_FORMAT_ARRAY& o);
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const DXGI_FORMAT* pFormats, UINT NumFormats);
                          operator const D3D12_RT_FORMAT_ARRAY&() const;
};
```



## <a name="members"></a><span data-ttu-id="07864-107">Membros</span><span class="sxs-lookup"><span data-stu-id="07864-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="07864-108">**\_ \_ Matriz de formato CD3DX12 RT \_ ()**</span><span class="sxs-lookup"><span data-stu-id="07864-108">**CD3DX12\_RT\_FORMAT\_ARRAY()**</span></span>
</dt> <dd>

<span data-ttu-id="07864-109">Cria uma nova instância, não inicializada, de uma \_ matriz de \_ formato CD3DX12 RT \_ .</span><span class="sxs-lookup"><span data-stu-id="07864-109">Creates a new, uninitialized, instance of a CD3DX12\_RT\_FORMAT\_ARRAY.</span></span>

</dd> <dt>

<span data-ttu-id="07864-110">**\_ \_ matriz de formato CD3DX12 RT explícita \_ (matriz de formato const D3D12 \_ RT \_ \_& o)**</span><span class="sxs-lookup"><span data-stu-id="07864-110">**explicit CD3DX12\_RT\_FORMAT\_ARRAY(const D3D12\_RT\_FORMAT\_ARRAY& o)**</span></span>
</dt> <dd>

<span data-ttu-id="07864-111">Cria uma nova instância de uma \_ matriz de formato CD3DX12 RT \_ \_ , inicializada com valores copiados de uma estrutura de [**\_ \_ \_ matriz de formato D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .</span><span class="sxs-lookup"><span data-stu-id="07864-111">Creates a new instance of a CD3DX12\_RT\_FORMAT\_ARRAY, initialized with values copied from a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

</dd> <dt>

<span data-ttu-id="07864-112">**\_ \_ matriz de formato CD3DX12 RT explícita \_ (const dxgi \_ Format \* pFormats, uint NumFormats)**</span><span class="sxs-lookup"><span data-stu-id="07864-112">**explicit CD3DX12\_RT\_FORMAT\_ARRAY(const DXGI\_FORMAT\* pFormats, UINT NumFormats)**</span></span>
</dt> <dd>

<span data-ttu-id="07864-113">Cria uma nova instância de uma \_ matriz de formato CD3DX12 RT \_ \_ , inicializada com os valores passados na lista de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="07864-113">Creates a new instance of a CD3DX12\_RT\_FORMAT\_ARRAY, initialized with the values passed in the parameter list.</span></span> <span data-ttu-id="07864-114">O conteúdo da matriz especificada pelo parâmetro *pFormats* é copiado para a matriz de membros **RTFormats**.</span><span class="sxs-lookup"><span data-stu-id="07864-114">Contents of the array specified by the *pFormats* parameter are copied into the member array **RTFormats**.</span></span> <span data-ttu-id="07864-115">Pressupõe-se que a matriz especificada por *pFormats* tenha o mesmo tamanho que **RTFormats**.</span><span class="sxs-lookup"><span data-stu-id="07864-115">The array specified by *pFormats* is assumed to have the same size as **RTFormats**.</span></span>

</dd> <dt>

<span data-ttu-id="07864-116">**\_ \_ matriz de formato const D3D12 RT do operador \_& () const**</span><span class="sxs-lookup"><span data-stu-id="07864-116">**operator const D3D12\_RT\_FORMAT\_ARRAY&() const**</span></span>
</dt> <dd>

<span data-ttu-id="07864-117">Conversão implícita em uma estrutura de [**\_ matriz de \_ formato \_ D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .</span><span class="sxs-lookup"><span data-stu-id="07864-117">Implicit conversion to a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span> <span data-ttu-id="07864-118">Como a \_ \_ matriz de formato D3D12 RT \_ é o tipo subjacente de \_ DESC1 estêncil de profundidade CD3DX12 \_ \_ , o objeto é simplesmente retornado como uma referência de matriz de formato const D3D12 \_ RT \_ \_ para si mesmo.</span><span class="sxs-lookup"><span data-stu-id="07864-118">Because D3D12\_RT\_FORMAT\_ARRAY is the underlying type of CD3DX12\_DEPTH\_STENCIL\_DESC1, the object is simply returned as a const D3D12\_RT\_FORMAT\_ARRAY reference to itself.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07864-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07864-119">Requirements</span></span>



| <span data-ttu-id="07864-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="07864-120">Requirement</span></span> | <span data-ttu-id="07864-121">Valor</span><span class="sxs-lookup"><span data-stu-id="07864-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="07864-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="07864-122">Header</span></span><br/> | <dl> <span data-ttu-id="07864-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="07864-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07864-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="07864-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07864-125">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="07864-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="07864-126">**\_Matriz de \_ formato D3D12 RT \_**</span><span class="sxs-lookup"><span data-stu-id="07864-126">**D3D12\_RT\_FORMAT\_ARRAY**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





