---
title: Estrutura de CD3DX12_SUBRESOURCE_TILING (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de subrecurso do D3D12 \_ .
ms.assetid: 102E5E25-300B-40F2-A953-E40AD7EE61AD
keywords:
- Estrutura de CD3DX12_SUBRESOURCE_TILING
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_TILING
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07677c8a8367f58016a0236cf0b5558b852bef01
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764208"
---
# <a name="cd3dx12_subresource_tiling-structure"></a><span data-ttu-id="844d7-104">\_Estrutura de SUBrecurso do CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="844d7-104">CD3DX12\_SUBRESOURCE\_TILING structure</span></span>

<span data-ttu-id="844d7-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ subrecurso do D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) .</span><span class="sxs-lookup"><span data-stu-id="844d7-105">A helper structure to enable easy initialization of a [**D3D12\_SUBRESOURCE\_TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="844d7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="844d7-106">Syntax</span></span>


```C++
struct CD3DX12_SUBRESOURCE_TILING  : public D3D12_SUBRESOURCE_TILING{
   CD3DX12_SUBRESOURCE_TILING();
   explicit CD3DX12_SUBRESOURCE_TILING(const D3D12_SUBRESOURCE_TILING &o);
   CD3DX12_SUBRESOURCE_TILING(UINT widthInTiles, UINT16 heightInTiles, UINT16 depthInTiles, UINT startTileIndexInOverallResource);
   operator const D3D12_SUBRESOURCE_TILING&() const;
};
```



## <a name="members"></a><span data-ttu-id="844d7-107">Membros</span><span class="sxs-lookup"><span data-stu-id="844d7-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="844d7-108">**SubCD3DX12 \_ de subrecurso \_ ()**</span><span class="sxs-lookup"><span data-stu-id="844d7-108">**CD3DX12\_SUBRESOURCE\_TILING()**</span></span>
</dt> <dd>

<span data-ttu-id="844d7-109">Cria uma nova instância, não inicializada, de um \_ subrecurso do CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="844d7-109">Creates a new, uninitialized, instance of a CD3DX12\_SUBRESOURCE\_TILING.</span></span>

</dd> <dt>

<span data-ttu-id="844d7-110">**subdivisão \_ de SUBRECURSO CD3DX12 explícito \_ (const D3D12 \_ subrecurso do \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="844d7-110">**explicit CD3DX12\_SUBRESOURCE\_TILING(const D3D12\_SUBRESOURCE\_TILING &o)**</span></span>
</dt> <dd>

<span data-ttu-id="844d7-111">Cria uma nova instância de um subCD3DX12 de \_ subrecurso \_ , inicializado com o conteúdo de outra estrutura de [**\_ subrecurso \_ do D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) .</span><span class="sxs-lookup"><span data-stu-id="844d7-111">Creates a new instance of a CD3DX12\_SUBRESOURCE\_TILING, initialized with the contents of another [**D3D12\_SUBRESOURCE\_TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) structure.</span></span>

</dd> <dt>

<span data-ttu-id="844d7-112">**SubCD3DX12 \_ de subrecurso \_ (UINT WIDTHINTILES, UInt16 HEIGHTINTILES, UInt16 DEPTHINTILES, uint startTileIndexInOverallResource)**</span><span class="sxs-lookup"><span data-stu-id="844d7-112">**CD3DX12\_SUBRESOURCE\_TILING(UINT widthInTiles, UINT16 heightInTiles, UINT16 depthInTiles, UINT startTileIndexInOverallResource)**</span></span>
</dt> <dd>

<span data-ttu-id="844d7-113">Cria uma nova instância de um subCD3DX12 de \_ subrecurso \_ , inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="844d7-113">Creates a new instance of a CD3DX12\_SUBRESOURCE\_TILING, initializing the following parameters:</span></span>

<span data-ttu-id="844d7-114">WidthInTiles UINT</span><span class="sxs-lookup"><span data-stu-id="844d7-114">UINT widthInTiles</span></span>

<span data-ttu-id="844d7-115">UINT16 heightInTiles</span><span class="sxs-lookup"><span data-stu-id="844d7-115">UINT16 heightInTiles</span></span>

<span data-ttu-id="844d7-116">UINT16 depthInTiles</span><span class="sxs-lookup"><span data-stu-id="844d7-116">UINT16 depthInTiles</span></span>

<span data-ttu-id="844d7-117">StartTileIndexInOverallResource UINT</span><span class="sxs-lookup"><span data-stu-id="844d7-117">UINT startTileIndexInOverallResource</span></span>

</dd> <dt>

<span data-ttu-id="844d7-118">**\_ \_ const de D3D12 de sub& recurso do operador const**</span><span class="sxs-lookup"><span data-stu-id="844d7-118">**operator const D3D12\_SUBRESOURCE\_TILING&() const**</span></span>
</dt> <dd>

<span data-ttu-id="844d7-119">Define o & operador de passagem por referência para o tipo de estrutura pai.</span><span class="sxs-lookup"><span data-stu-id="844d7-119">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="844d7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="844d7-120">Requirements</span></span>



| <span data-ttu-id="844d7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="844d7-121">Requirement</span></span> | <span data-ttu-id="844d7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="844d7-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="844d7-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="844d7-123">Header</span></span><br/> | <dl> <span data-ttu-id="844d7-124"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="844d7-124"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="844d7-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="844d7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="844d7-126">**SubD3D12 de \_ SUBrecurso \_**</span><span class="sxs-lookup"><span data-stu-id="844d7-126">**D3D12\_SUBRESOURCE\_TILING**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling)
</dt> <dt>

[<span data-ttu-id="844d7-127">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="844d7-127">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





