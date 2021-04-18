---
title: Estrutura de CD3DX12_TILE_REGION_SIZE (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de tamanho de região de bloco do D3D12 \_ \_ .
ms.assetid: 07D2D8DE-C35C-48EE-8E9E-36545B60C594
keywords:
- Estrutura de CD3DX12_TILE_REGION_SIZE
topic_type:
- apiref
api_name:
- CD3DX12_TILE_REGION_SIZE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f64046f2a7efa32af8b43adbcf7349f43b6ec3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105810852"
---
# <a name="cd3dx12_tile_region_size-structure"></a><span data-ttu-id="d03d3-104">\_Estrutura de \_ tamanho da região de bloco do CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="d03d3-104">CD3DX12\_TILE\_REGION\_SIZE structure</span></span>

<span data-ttu-id="d03d3-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**tamanho de região de bloco do D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) .</span><span class="sxs-lookup"><span data-stu-id="d03d3-105">A helper structure to enable easy initialization of a [**D3D12\_TILE\_REGION\_SIZE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="d03d3-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d03d3-106">Syntax</span></span>


```C++
struct CD3DX12_TILE_REGION_SIZE  : public D3D12_TILE_REGION_SIZE{
   CD3DX12_TILE_REGION_SIZE();
   explicit CD3DX12_TILE_REGION_SIZE(const D3D12_TILE_REGION_SIZE &o);
   CD3DX12_TILE_REGION_SIZE(UINT numTiles, BOOL useBox, UINT width, UINT16 height, UINT16 depth);
   operator const D3D12_TILE_REGION_SIZE&() const;
};
```



## <a name="members"></a><span data-ttu-id="d03d3-107">Membros</span><span class="sxs-lookup"><span data-stu-id="d03d3-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d03d3-108">**\_Tamanho da \_ região do bloco CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="d03d3-108">**CD3DX12\_TILE\_REGION\_SIZE()**</span></span>
</dt> <dd>

<span data-ttu-id="d03d3-109">Cria uma nova instância, não inicializada, de um \_ tamanho de região de bloco CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d03d3-109">Creates a new, uninitialized, instance of a CD3DX12\_TILE\_REGION\_SIZE.</span></span>

</dd> <dt>

<span data-ttu-id="d03d3-110">**\_ \_ tamanho de região de bloco CD3DX12 explícito \_ (const D3D12 \_ tamanho da região do bloco \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="d03d3-110">**explicit CD3DX12\_TILE\_REGION\_SIZE(const D3D12\_TILE\_REGION\_SIZE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="d03d3-111">Cria uma nova instância de um \_ tamanho de região de bloco CD3DX12 \_ \_ , inicializada com o conteúdo de outra estrutura de tamanho de [**\_ região de bloco \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) .</span><span class="sxs-lookup"><span data-stu-id="d03d3-111">Creates a new instance of a CD3DX12\_TILE\_REGION\_SIZE, initialized with the contents of another [**D3D12\_TILE\_REGION\_SIZE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d03d3-112">**\_Tamanho da \_ região de bloco CD3DX12 \_ (UINT NumTiles, bool useBox, largura de uint, altura de UInt16, profundidade de UInt16)**</span><span class="sxs-lookup"><span data-stu-id="d03d3-112">**CD3DX12\_TILE\_REGION\_SIZE(UINT numTiles, BOOL useBox, UINT width, UINT16 height, UINT16 depth)**</span></span>
</dt> <dd>

<span data-ttu-id="d03d3-113">Cria uma nova instância de um \_ tamanho de região de bloco CD3DX12 \_ \_ , inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="d03d3-113">Creates a new instance of a CD3DX12\_TILE\_REGION\_SIZE, initializing the following parameters:</span></span>

<span data-ttu-id="d03d3-114">NumTiles UINT</span><span class="sxs-lookup"><span data-stu-id="d03d3-114">UINT numTiles</span></span>

<span data-ttu-id="d03d3-115">UseBox BOOL</span><span class="sxs-lookup"><span data-stu-id="d03d3-115">BOOL useBox</span></span>

<span data-ttu-id="d03d3-116">Largura de UINT</span><span class="sxs-lookup"><span data-stu-id="d03d3-116">UINT width</span></span>

<span data-ttu-id="d03d3-117">Altura de UINT16</span><span class="sxs-lookup"><span data-stu-id="d03d3-117">UINT16 height</span></span>

<span data-ttu-id="d03d3-118">Profundidade de UINT16</span><span class="sxs-lookup"><span data-stu-id="d03d3-118">UINT16 depth</span></span>

</dd> <dt>

<span data-ttu-id="d03d3-119">**const D3D12 \_ tamanho da \_ região \_ de bloco do operador& () constante**</span><span class="sxs-lookup"><span data-stu-id="d03d3-119">**operator const D3D12\_TILE\_REGION\_SIZE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="d03d3-120">Define o & operador de passagem por referência para o tipo de estrutura pai.</span><span class="sxs-lookup"><span data-stu-id="d03d3-120">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d03d3-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d03d3-121">Requirements</span></span>



| <span data-ttu-id="d03d3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d03d3-122">Requirement</span></span> | <span data-ttu-id="d03d3-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d03d3-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d03d3-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d03d3-124">Header</span></span><br/> | <dl> <span data-ttu-id="d03d3-125"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="d03d3-125"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d03d3-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d03d3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d03d3-127">**\_Tamanho da \_ região do bloco D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="d03d3-127">**D3D12\_TILE\_REGION\_SIZE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size)
</dt> <dt>

[<span data-ttu-id="d03d3-128">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="d03d3-128">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





