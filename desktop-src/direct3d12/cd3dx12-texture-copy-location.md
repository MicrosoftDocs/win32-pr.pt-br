---
title: Estrutura de CD3DX12_TEXTURE_COPY_LOCATION (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de localização de cópia de textura D3D12 \_ \_ .
ms.assetid: 8BA93729-2FFB-4C09-88B0-779049BAF385
keywords:
- Estrutura de CD3DX12_TEXTURE_COPY_LOCATION
topic_type:
- apiref
api_name:
- CD3DX12_TEXTURE_COPY_LOCATION
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5143137f92e38662660588dd89a527f59644126
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105807884"
---
# <a name="cd3dx12_texture_copy_location-structure"></a><span data-ttu-id="e59f1-104">\_Estrutura de \_ localização de cópia de textura CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="e59f1-104">CD3DX12\_TEXTURE\_COPY\_LOCATION structure</span></span>

<span data-ttu-id="e59f1-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ localização de \_ cópia \_ de textura D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) .</span><span class="sxs-lookup"><span data-stu-id="e59f1-105">A helper structure to enable easy initialization of a [**D3D12\_TEXTURE\_COPY\_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e59f1-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e59f1-106">Syntax</span></span>


```C++
struct CD3DX12_TEXTURE_COPY_LOCATION  : public D3D12_TEXTURE_COPY_LOCATION{
   CD3DX12_TEXTURE_COPY_LOCATION();
   explicit CD3DX12_TEXTURE_COPY_LOCATION(const D3D12_TEXTURE_COPY_LOCATION &o);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, D3D12_PLACED_SUBRESOURCE_FOOTPRINT const& Footprint);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, UINT Sub);
};
```



## <a name="members"></a><span data-ttu-id="e59f1-107">Membros</span><span class="sxs-lookup"><span data-stu-id="e59f1-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e59f1-108">**\_ \_ \_ Local de cópia de textura CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="e59f1-108">**CD3DX12\_TEXTURE\_COPY\_LOCATION()**</span></span>
</dt> <dd>

<span data-ttu-id="e59f1-109">Cria uma nova instância não inicializada de um \_ local de cópia de textura CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e59f1-109">Creates a new, uninitialized, instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION.</span></span>

</dd> <dt>

<span data-ttu-id="e59f1-110">**\_ \_ \_ local de cópia de textura de CD3DX12 explícita (localização de cópia de textura D3D12 const \_ \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="e59f1-110">**explicit CD3DX12\_TEXTURE\_COPY\_LOCATION(const D3D12\_TEXTURE\_COPY\_LOCATION &o)**</span></span>
</dt> <dd>

<span data-ttu-id="e59f1-111">Cria uma nova instância de um \_ local de cópia de textura CD3DX12 \_ \_ , inicializada com o conteúdo de outra estrutura de localização de [**\_ cópia de textura \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) .</span><span class="sxs-lookup"><span data-stu-id="e59f1-111">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initialized with the contents of another [**D3D12\_TEXTURE\_COPY\_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e59f1-112">**\_ \_ \_ Local de cópia de textura CD3DX12 (ID3D12Resource \* pRes)**</span><span class="sxs-lookup"><span data-stu-id="e59f1-112">**CD3DX12\_TEXTURE\_COPY\_LOCATION(ID3D12Resource\* pRes)**</span></span>
</dt> <dd>

<span data-ttu-id="e59f1-113">Cria uma nova instância de um \_ local de cópia de textura CD3DX12 \_ \_ , inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="e59f1-113">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initializing the following parameters:</span></span>

<span data-ttu-id="e59f1-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pRes</span><span class="sxs-lookup"><span data-stu-id="e59f1-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pRes</span></span>

</dd> <dt>

<span data-ttu-id="e59f1-115">**\_ \_ \_ Local de cópia de textura do CD3DX12 (ID3D12RESOURCE \* pRes, D3D12 \_ colocou a superfície do \_ subrecurso \_ const& superfície)**</span><span class="sxs-lookup"><span data-stu-id="e59f1-115">**CD3DX12\_TEXTURE\_COPY\_LOCATION(ID3D12Resource\* pRes, D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT const& Footprint)**</span></span>
</dt> <dd>

<span data-ttu-id="e59f1-116">Cria uma nova instância de um \_ local de cópia de textura CD3DX12 \_ \_ , inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="e59f1-116">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initializing the following parameters:</span></span>

<span data-ttu-id="e59f1-117">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pRes</span><span class="sxs-lookup"><span data-stu-id="e59f1-117">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pRes</span></span>

<span data-ttu-id="e59f1-118">[**D3D12 \_& superfície do \_ \_ espaço de SUBrecurso posicionado**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)</span><span class="sxs-lookup"><span data-stu-id="e59f1-118">[**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) const& Footprint</span></span>

</dd> <dt>

<span data-ttu-id="e59f1-119">**\_ \_ \_ Local de cópia de textura de CD3DX12 (ID3D12RESOURCE \* pRes, uint sub)**</span><span class="sxs-lookup"><span data-stu-id="e59f1-119">**CD3DX12\_TEXTURE\_COPY\_LOCATION(ID3D12Resource\* pRes, UINT Sub)**</span></span>
</dt> <dd>

<span data-ttu-id="e59f1-120">Cria uma nova instância de um \_ local de cópia de textura CD3DX12 \_ \_ , inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="e59f1-120">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initializing the following parameters:</span></span>

<span data-ttu-id="e59f1-121">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pRes</span><span class="sxs-lookup"><span data-stu-id="e59f1-121">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pRes</span></span>

<span data-ttu-id="e59f1-122">Sub-UINT</span><span class="sxs-lookup"><span data-stu-id="e59f1-122">UINT Sub</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e59f1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e59f1-123">Requirements</span></span>



| <span data-ttu-id="e59f1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e59f1-124">Requirement</span></span> | <span data-ttu-id="e59f1-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e59f1-125">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e59f1-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e59f1-126">Header</span></span><br/> | <dl> <span data-ttu-id="e59f1-127"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="e59f1-127"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e59f1-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e59f1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e59f1-129">**\_Local de \_ cópia de textura D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="e59f1-129">**D3D12\_TEXTURE\_COPY\_LOCATION**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
</dt> <dt>

[<span data-ttu-id="e59f1-130">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="e59f1-130">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





