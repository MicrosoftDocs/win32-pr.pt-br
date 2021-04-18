---
title: Estrutura de CD3DX12_RANGE (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de intervalo D3D12.
ms.assetid: 5D5192BF-D14C-487B-A214-F8428E82AF0E
keywords:
- Estrutura de CD3DX12_RANGE
topic_type:
- apiref
api_name:
- CD3DX12_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b6b92cd24a981d48252f5ad457f7ac0320e2d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105785175"
---
# <a name="cd3dx12_range-structure"></a><span data-ttu-id="d25d4-104">Estrutura do intervalo de CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="d25d4-104">CD3DX12\_RANGE structure</span></span>

<span data-ttu-id="d25d4-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ intervalo D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) .</span><span class="sxs-lookup"><span data-stu-id="d25d4-105">A helper structure to enable easy initialization of a [**D3D12\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="d25d4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d25d4-106">Syntax</span></span>


```C++
struct CD3DX12_RANGE  : public D3D12_RANGE{
   CD3DX12_RANGE();
   explicit CD3DX12_RANGE(const D3D12_RANGE &o);
   CD3DX12_RANGE(SIZE_T begin, SIZE_T end);
   operator const D3D12_RANGE&() const;
};
```



## <a name="members"></a><span data-ttu-id="d25d4-107">Membros</span><span class="sxs-lookup"><span data-stu-id="d25d4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d25d4-108">**\_Intervalo de CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="d25d4-108">**CD3DX12\_RANGE()**</span></span>
</dt> <dd>

<span data-ttu-id="d25d4-109">Cria uma instância nova e não inicializada de um intervalo de CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="d25d4-109">Creates a new, uninitialized, instance of a CD3DX12\_RANGE.</span></span>

</dd> <dt>

<span data-ttu-id="d25d4-110">**intervalo CD3DX12 explícito \_ (const D3D12 \_ intervalo &o)**</span><span class="sxs-lookup"><span data-stu-id="d25d4-110">**explicit CD3DX12\_RANGE(const D3D12\_RANGE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="d25d4-111">Cria uma nova instância de um \_ intervalo CD3DX12, inicializada com o conteúdo de outra estrutura de [**\_ intervalo D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) .</span><span class="sxs-lookup"><span data-stu-id="d25d4-111">Creates a new instance of a CD3DX12\_RANGE, initialized with the contents of another [**D3D12\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d25d4-112">**\_Intervalo de CD3DX12 ( \_ início de tamanho t, tamanho \_ t end)**</span><span class="sxs-lookup"><span data-stu-id="d25d4-112">**CD3DX12\_RANGE(SIZE\_T begin, SIZE\_T end)**</span></span>
</dt> <dd>

<span data-ttu-id="d25d4-113">Cria uma nova instância de um intervalo de CD3DX12 \_ , inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="d25d4-113">Creates a new instance of a CD3DX12\_RANGE, initializing the following parameters:</span></span>

<span data-ttu-id="d25d4-114">Início de T de tamanho \_</span><span class="sxs-lookup"><span data-stu-id="d25d4-114">SIZE\_T begin</span></span>

<span data-ttu-id="d25d4-115">Fim de T de tamanho \_</span><span class="sxs-lookup"><span data-stu-id="d25d4-115">SIZE\_T end</span></span>

</dd> <dt>

<span data-ttu-id="d25d4-116">**\_const de D3D12 de& intervalo constante de operador**</span><span class="sxs-lookup"><span data-stu-id="d25d4-116">**operator const D3D12\_RANGE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="d25d4-117">Define o & operador de passagem por referência para o tipo de estrutura pai.</span><span class="sxs-lookup"><span data-stu-id="d25d4-117">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d25d4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d25d4-118">Requirements</span></span>



| <span data-ttu-id="d25d4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d25d4-119">Requirement</span></span> | <span data-ttu-id="d25d4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d25d4-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d25d4-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d25d4-121">Header</span></span><br/> | <dl> <span data-ttu-id="d25d4-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="d25d4-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d25d4-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="d25d4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d25d4-124">**Intervalo de D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="d25d4-124">**D3D12\_RANGE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)
</dt> <dt>

[<span data-ttu-id="d25d4-125">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="d25d4-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





