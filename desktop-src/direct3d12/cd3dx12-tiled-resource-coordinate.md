---
title: Estrutura de CD3DX12_TILED_RESOURCE_COORDINATE (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ \_ estrutura de coordenada de recursos lado-a-D3D12 \_ .
ms.assetid: B337ED04-E2C6-4B89-80F1-92C0854A6AF2
keywords:
- Estrutura de CD3DX12_TILED_RESOURCE_COORDINATE
topic_type:
- apiref
api_name:
- CD3DX12_TILED_RESOURCE_COORDINATE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 281afeab8d1172e9cae749512612129dd001161b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761522"
---
# <a name="cd3dx12_tiled_resource_coordinate-structure"></a><span data-ttu-id="29d89-104">\_Estrutura de \_ coordenada de recursos lado-a-CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="29d89-104">CD3DX12\_TILED\_RESOURCE\_COORDINATE structure</span></span>

<span data-ttu-id="29d89-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ \_ coordenada de recursos lado**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) -a-D3D12.</span><span class="sxs-lookup"><span data-stu-id="29d89-105">A helper structure to enable easy initialization of a [**D3D12\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="29d89-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29d89-106">Syntax</span></span>


```C++
struct CD3DX12_TILED_RESOURCE_COORDINATE  : public D3D12_TILED_RESOURCE_COORDINATE{
   CD3DX12_TILED_RESOURCE_COORDINATE();
   explicit CD3DX12_TILED_RESOURCE_COORDINATE(const D3D12_TILED_RESOURCE_COORDINATE &o);
   CD3DX12_TILED_RESOURCE_COORDINATE(UINT x, UINT y, UINT z, UINT subresource);
   operator const D3D12_TILED_RESOURCE_COORDINATE&() const;
};
```



## <a name="members"></a><span data-ttu-id="29d89-107">Membros</span><span class="sxs-lookup"><span data-stu-id="29d89-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="29d89-108">**\_ \_ \_ Coordenada de recurso do lado do CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="29d89-108">**CD3DX12\_TILED\_RESOURCE\_COORDINATE()**</span></span>
</dt> <dd>

<span data-ttu-id="29d89-109">Cria uma nova instância, não inicializada, de uma \_ coordenada de recurso de lado CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="29d89-109">Creates a new, uninitialized, instance of a CD3DX12\_TILED\_RESOURCE\_COORDINATE.</span></span>

</dd> <dt>

<span data-ttu-id="29d89-110">**\_ \_ \_ coordenada de recurso CD3DX12 de lado explícito (constante D3D12 de recurso em ladrilho de const \_ \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="29d89-110">**explicit CD3DX12\_TILED\_RESOURCE\_COORDINATE(const D3D12\_TILED\_RESOURCE\_COORDINATE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="29d89-111">Cria uma nova instância de uma \_ coordenada de recurso do lado do CD3DX12 \_ \_ , inicializada com o conteúdo de outra estrutura de [**\_ \_ \_ coordenada de recurso de lado D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) .</span><span class="sxs-lookup"><span data-stu-id="29d89-111">Creates a new instance of a CD3DX12\_TILED\_RESOURCE\_COORDINATE, initialized with the contents of another [**D3D12\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) structure.</span></span>

</dd> <dt>

<span data-ttu-id="29d89-112">**\_ \_ \_ Coordenada de recurso do lado do CD3DX12 (UINT x, UINT y, uintstate z, uint preresource)**</span><span class="sxs-lookup"><span data-stu-id="29d89-112">**CD3DX12\_TILED\_RESOURCE\_COORDINATE(UINT x, UINT y, UINT z, UINT subresource)**</span></span>
</dt> <dd>

<span data-ttu-id="29d89-113">Cria uma nova instância de uma \_ coordenada de recurso do lado do CD3DX12 \_ \_ , inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="29d89-113">Creates a new instance of a CD3DX12\_TILED\_RESOURCE\_COORDINATE, initializing the following parameters:</span></span>

<span data-ttu-id="29d89-114">X UINT</span><span class="sxs-lookup"><span data-stu-id="29d89-114">UINT x</span></span>

<span data-ttu-id="29d89-115">Y UINT</span><span class="sxs-lookup"><span data-stu-id="29d89-115">UINT y</span></span>

<span data-ttu-id="29d89-116">Z UINT</span><span class="sxs-lookup"><span data-stu-id="29d89-116">UINT z</span></span>

<span data-ttu-id="29d89-117">Subrecurso UINT</span><span class="sxs-lookup"><span data-stu-id="29d89-117">UINT subresource</span></span>

</dd> <dt>

<span data-ttu-id="29d89-118">**constante \_ \_ de recurso const D3D12 \_ de coordenadas de recursos de lado& () const**</span><span class="sxs-lookup"><span data-stu-id="29d89-118">**operator const D3D12\_TILED\_RESOURCE\_COORDINATE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="29d89-119">Define o & operador de passagem por referência para o tipo de estrutura pai.</span><span class="sxs-lookup"><span data-stu-id="29d89-119">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="29d89-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29d89-120">Requirements</span></span>



| <span data-ttu-id="29d89-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="29d89-121">Requirement</span></span> | <span data-ttu-id="29d89-122">Valor</span><span class="sxs-lookup"><span data-stu-id="29d89-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="29d89-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="29d89-123">Header</span></span><br/> | <dl> <span data-ttu-id="29d89-124"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="29d89-124"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29d89-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="29d89-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29d89-126">**\_ \_ Coordenada de recurso de lado D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="29d89-126">**D3D12\_TILED\_RESOURCE\_COORDINATE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate)
</dt> <dt>

[<span data-ttu-id="29d89-127">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="29d89-127">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





