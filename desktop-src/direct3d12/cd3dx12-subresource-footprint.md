---
title: Estrutura de CD3DX12_SUBRESOURCE_FOOTPRINT (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de superfície de subrecurso do D3D12 \_ .
ms.assetid: 17266FB0-41B5-4A70-A896-206B54F5E76F
keywords:
- Estrutura de CD3DX12_SUBRESOURCE_FOOTPRINT
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_FOOTPRINT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab58e9a007d736222d9525d7a064456a1a9a7f14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812024"
---
# <a name="cd3dx12_subresource_footprint-structure"></a><span data-ttu-id="25fcc-104">\_Estrutura de superfície do SUBrecurso do CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="25fcc-104">CD3DX12\_SUBRESOURCE\_FOOTPRINT structure</span></span>

<span data-ttu-id="25fcc-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ superfície de subrecurso do D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) .</span><span class="sxs-lookup"><span data-stu-id="25fcc-105">A helper structure to enable easy initialization of a [**D3D12\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="25fcc-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25fcc-106">Syntax</span></span>


```C++
struct CD3DX12_SUBRESOURCE_FOOTPRINT  : public D3D12_SUBRESOURCE_FOOTPRINT{
   CD3DX12_SUBRESOURCE_FOOTPRINT();
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_SUBRESOURCE_FOOTPRINT &o);
   CD3DX12_SUBRESOURCE_FOOTPRINT(DXGI_FORMAT format, UINT width, UINT height, UINT depth, UINT rowPitch);
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_RESOURCE_DESC& resDesc, UINT rowPitch);
   operator const D3D12_SUBRESOURCE_FOOTPRINT&() const;
};
```



## <a name="members"></a><span data-ttu-id="25fcc-107">Membros</span><span class="sxs-lookup"><span data-stu-id="25fcc-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="25fcc-108">**CD3DX12 da \_ \_ superfície do subrecurso ()**</span><span class="sxs-lookup"><span data-stu-id="25fcc-108">**CD3DX12\_SUBRESOURCE\_FOOTPRINT()**</span></span>
</dt> <dd>

<span data-ttu-id="25fcc-109">Cria uma nova instância, não inicializada, de uma \_ superfície de SUBRECURSO CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="25fcc-109">Creates a new, uninitialized, instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT.</span></span>

</dd> <dt>

<span data-ttu-id="25fcc-110">**\_superfície de SUBRECURSO CD3DX12 explícito \_ (const D3D12 \_ superfície do subrecurso \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="25fcc-110">**explicit CD3DX12\_SUBRESOURCE\_FOOTPRINT(const D3D12\_SUBRESOURCE\_FOOTPRINT &o)**</span></span>
</dt> <dd>

<span data-ttu-id="25fcc-111">Cria uma nova instância de uma \_ superfície de SUBRECURSO CD3DX12 \_ , inicializada com o conteúdo de outra estrutura de [**\_ \_ superfície de subrecurso D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) .</span><span class="sxs-lookup"><span data-stu-id="25fcc-111">Creates a new instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT, initialized with the contents of another [**D3D12\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) structure.</span></span>

</dd> <dt>

<span data-ttu-id="25fcc-112">**\_Superfície de SUBRECURSO CD3DX12 \_ ( \_ formato de formato dxgi, largura UINT, altura UINT, profundidade uint, semidensidade uint)**</span><span class="sxs-lookup"><span data-stu-id="25fcc-112">**CD3DX12\_SUBRESOURCE\_FOOTPRINT(DXGI\_FORMAT format, UINT width, UINT height, UINT depth, UINT rowPitch)**</span></span>
</dt> <dd>

<span data-ttu-id="25fcc-113">Cria uma nova instância de uma \_ superfície de SUBRECURSO CD3DX12 \_ , inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="25fcc-113">Creates a new instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT, initializing the following parameters:</span></span>

<span data-ttu-id="25fcc-114">[**Dxgi \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato</span><span class="sxs-lookup"><span data-stu-id="25fcc-114">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="25fcc-115">Largura de UINT</span><span class="sxs-lookup"><span data-stu-id="25fcc-115">UINT width</span></span>

<span data-ttu-id="25fcc-116">Altura UINT</span><span class="sxs-lookup"><span data-stu-id="25fcc-116">UINT height</span></span>

<span data-ttu-id="25fcc-117">Profundidade de UINT</span><span class="sxs-lookup"><span data-stu-id="25fcc-117">UINT depth</span></span>

<span data-ttu-id="25fcc-118">Semidensidade UINT</span><span class="sxs-lookup"><span data-stu-id="25fcc-118">UINT rowPitch</span></span>

</dd> <dt>

<span data-ttu-id="25fcc-119">**\_superfície de SUBRECURSO CD3DX12 explícito \_ (const D3D12 \_ recurso \_ desc& RESDESC, semidensidade uint)**</span><span class="sxs-lookup"><span data-stu-id="25fcc-119">**explicit CD3DX12\_SUBRESOURCE\_FOOTPRINT(const D3D12\_RESOURCE\_DESC& resDesc, UINT rowPitch)**</span></span>
</dt> <dd>

<span data-ttu-id="25fcc-120">Cria uma nova instância de uma \_ superfície de SUBRECURSO CD3DX12 \_ , inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="25fcc-120">Creates a new instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT, initializing the following parameters:</span></span>

<span data-ttu-id="25fcc-121">[**D3D12 \_ RECURSO \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)& resDesc</span><span class="sxs-lookup"><span data-stu-id="25fcc-121">[**D3D12\_RESOURCE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)& resDesc</span></span>

<span data-ttu-id="25fcc-122">Semidensidade UINT</span><span class="sxs-lookup"><span data-stu-id="25fcc-122">UINT rowPitch</span></span>

</dd> <dt>

<span data-ttu-id="25fcc-123">**constante de D3D12 \_ de subrecurso \_ de constante de operador de& () const**</span><span class="sxs-lookup"><span data-stu-id="25fcc-123">**operator const D3D12\_SUBRESOURCE\_FOOTPRINT&() const**</span></span>
</dt> <dd>

<span data-ttu-id="25fcc-124">Define o & operador de passagem por referência para o tipo de estrutura pai.</span><span class="sxs-lookup"><span data-stu-id="25fcc-124">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25fcc-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25fcc-125">Requirements</span></span>



| <span data-ttu-id="25fcc-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="25fcc-126">Requirement</span></span> | <span data-ttu-id="25fcc-127">Valor</span><span class="sxs-lookup"><span data-stu-id="25fcc-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="25fcc-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="25fcc-128">Header</span></span><br/> | <dl> <span data-ttu-id="25fcc-129"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="25fcc-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25fcc-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="25fcc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25fcc-131">**\_Superfície do SUBrecurso do D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="25fcc-131">**D3D12\_SUBRESOURCE\_FOOTPRINT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
</dt> <dt>

[<span data-ttu-id="25fcc-132">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="25fcc-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

