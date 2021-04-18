---
title: Estrutura de CD3DX12_RECT (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura RECT D3D12.
ms.assetid: FBF01294-1448-4D9A-BA6B-27D5D59C2958
keywords:
- Estrutura de CD3DX12_RECT
topic_type:
- apiref
api_name:
- CD3DX12_RECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6d8c133f14b531433ceb2239377ea85ba212af
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798492"
---
# <a name="cd3dx12_rect-structure"></a><span data-ttu-id="16a8e-104">\_Estrutura CD3DX12 Rect</span><span class="sxs-lookup"><span data-stu-id="16a8e-104">CD3DX12\_RECT structure</span></span>

<span data-ttu-id="16a8e-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ Rect D3D12**](d3d12-rect.md) .</span><span class="sxs-lookup"><span data-stu-id="16a8e-105">A helper structure to enable easy initialization of a [**D3D12\_RECT**](d3d12-rect.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="16a8e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16a8e-106">Syntax</span></span>


```C++
struct CD3DX12_RECT  : public D3D12_RECT{
   CD3DX12_RECT();
   explicit CD3DX12_RECT(const D3D12_RECT& o);
   explicit CD3DX12_RECT(LONG Left, LONG Top, LONG Right, LONG Bottom);
   ~CD3DX12_RECT();
   operator const D3D12_RECT&() const;
};
```



## <a name="members"></a><span data-ttu-id="16a8e-107">Membros</span><span class="sxs-lookup"><span data-stu-id="16a8e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="16a8e-108">**CD3DX12 \_ Rect ()**</span><span class="sxs-lookup"><span data-stu-id="16a8e-108">**CD3DX12\_RECT()**</span></span>
</dt> <dd>

<span data-ttu-id="16a8e-109">Cria uma instância nova e não inicializada de um CD3DX12 \_ Rect.</span><span class="sxs-lookup"><span data-stu-id="16a8e-109">Creates a new, uninitialized, instance of a CD3DX12\_RECT.</span></span>

</dd> <dt>

<span data-ttu-id="16a8e-110">**CD3DX12 \_ Rect explícito (const D3D12 \_ Rect& o)**</span><span class="sxs-lookup"><span data-stu-id="16a8e-110">**explicit CD3DX12\_RECT(const D3D12\_RECT& o)**</span></span>
</dt> <dd>

<span data-ttu-id="16a8e-111">Cria uma nova instância de um CD3DX12 \_ Rect, inicializada com o conteúdo de outra estrutura [**D3D12 \_ Rect**](d3d12-rect.md) .</span><span class="sxs-lookup"><span data-stu-id="16a8e-111">Creates a new instance of a CD3DX12\_RECT, initialized with the contents of another [**D3D12\_RECT**](d3d12-rect.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="16a8e-112">**CD3DX12 \_ Rect explícito (esquerda longa, longa superior, longa direita, longa parte inferior)**</span><span class="sxs-lookup"><span data-stu-id="16a8e-112">**explicit CD3DX12\_RECT(LONG Left, LONG Top, LONG Right, LONG Bottom)**</span></span>
</dt> <dd>

<span data-ttu-id="16a8e-113">Cria uma nova instância de um CD3DX12 \_ Rect, inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="16a8e-113">Creates a new instance of a CD3DX12\_RECT, initializing the following parameters:</span></span>

<span data-ttu-id="16a8e-114">LONGA para a esquerda</span><span class="sxs-lookup"><span data-stu-id="16a8e-114">LONG Left</span></span>

<span data-ttu-id="16a8e-115">Início longo</span><span class="sxs-lookup"><span data-stu-id="16a8e-115">LONG Top</span></span>

<span data-ttu-id="16a8e-116">LONGO direito</span><span class="sxs-lookup"><span data-stu-id="16a8e-116">LONG Right</span></span>

<span data-ttu-id="16a8e-117">Parte inferior longa</span><span class="sxs-lookup"><span data-stu-id="16a8e-117">LONG Bottom</span></span>

</dd> <dt>

<span data-ttu-id="16a8e-118">**~ CD3DX12 \_ Rect ()**</span><span class="sxs-lookup"><span data-stu-id="16a8e-118">**~CD3DX12\_RECT()**</span></span>
</dt> <dd>

<span data-ttu-id="16a8e-119">Destrói uma instância de um CD3DX12 \_ Rect.</span><span class="sxs-lookup"><span data-stu-id="16a8e-119">Destroys an instance of a CD3DX12\_RECT.</span></span>

</dd> <dt>

<span data-ttu-id="16a8e-120">**\_const do operador D3D12 RECT& () constante**</span><span class="sxs-lookup"><span data-stu-id="16a8e-120">**operator const D3D12\_RECT&() const**</span></span>
</dt> <dd>

<span data-ttu-id="16a8e-121">Define o & operador de passagem por referência para o tipo de estrutura pai.</span><span class="sxs-lookup"><span data-stu-id="16a8e-121">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="16a8e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16a8e-122">Requirements</span></span>



| <span data-ttu-id="16a8e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="16a8e-123">Requirement</span></span> | <span data-ttu-id="16a8e-124">Valor</span><span class="sxs-lookup"><span data-stu-id="16a8e-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="16a8e-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16a8e-125">Header</span></span><br/> | <dl> <span data-ttu-id="16a8e-126"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="16a8e-126"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16a8e-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="16a8e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16a8e-128">**D3D12 \_ Rect**</span><span class="sxs-lookup"><span data-stu-id="16a8e-128">**D3D12\_RECT**</span></span>](d3d12-rect.md)
</dt> <dt>

[<span data-ttu-id="16a8e-129">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="16a8e-129">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





