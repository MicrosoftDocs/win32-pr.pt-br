---
title: Estrutura de CD3DX12_PACKED_MIP_INFO (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ \_ estrutura de informações MIP empacotada D3D12 \_ .
ms.assetid: B3549D78-C354-48FC-A012-1F835DBD585E
keywords:
- Estrutura de CD3DX12_PACKED_MIP_INFO
topic_type:
- apiref
api_name:
- CD3DX12_PACKED_MIP_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4565bbac6189cffc5358213437463b4abc0322
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105773090"
---
# <a name="cd3dx12_packed_mip_info-structure"></a><span data-ttu-id="43559-104">\_Estrutura de \_ informações MIP EMPACOTAda CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="43559-104">CD3DX12\_PACKED\_MIP\_INFO structure</span></span>

<span data-ttu-id="43559-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ \_ informações MIP empacotada D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) .</span><span class="sxs-lookup"><span data-stu-id="43559-105">A helper structure to enable easy initialization of a [**D3D12\_PACKED\_MIP\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="43559-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43559-106">Syntax</span></span>


```C++
struct CD3DX12_PACKED_MIP_INFO  : public D3D12_PACKED_MIP_INFO{
   CD3DX12_PACKED_MIP_INFO();
   explicit CD3DX12_PACKED_MIP_INFO(const D3D12_PACKED_MIP_INFO &o);
   CD3DX12_PACKED_MIP_INFO(UINT8 numStandardMips, UINT8 numPackedMips, UINT numTilesForPackedMips, UINT startTileIndexInOverallResource);
   operator const D3D12_PACKED_MIP_INFO&() const;
};
```



## <a name="members"></a><span data-ttu-id="43559-107">Membros</span><span class="sxs-lookup"><span data-stu-id="43559-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="43559-108">**CD3DX12 \_ \_ informações de MIP compactadas \_ ()**</span><span class="sxs-lookup"><span data-stu-id="43559-108">**CD3DX12\_PACKED\_MIP\_INFO()**</span></span>
</dt> <dd>

<span data-ttu-id="43559-109">Cria uma nova instância não inicializada de uma \_ informação de MIP empacotada CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="43559-109">Creates a new, uninitialized, instance of a CD3DX12\_PACKED\_MIP\_INFO.</span></span>

</dd> <dt>

<span data-ttu-id="43559-110">**\_informações explícitas \_ de MIP compactadas do CD3DX12 \_ (const D3D12 \_ informações de MIP empacotadas \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="43559-110">**explicit CD3DX12\_PACKED\_MIP\_INFO(const D3D12\_PACKED\_MIP\_INFO &o)**</span></span>
</dt> <dd>

<span data-ttu-id="43559-111">Cria uma nova instância de uma \_ informação de MIP empacotada CD3DX12 \_ \_ , inicializada com o conteúdo de outra estrutura de [**\_ \_ \_ informações MIP empacotada D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) .</span><span class="sxs-lookup"><span data-stu-id="43559-111">Creates a new instance of a CD3DX12\_PACKED\_MIP\_INFO, initialized with the contents of another [**D3D12\_PACKED\_MIP\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) structure.</span></span>

</dd> <dt>

<span data-ttu-id="43559-112">**CD3DX12 \_ informações de MIP compactadas \_ \_ (UINT8 NumStandardMips, UINT8 NumPackedMips, UINT NumTilesForPackedMips, uint startTileIndexInOverallResource)**</span><span class="sxs-lookup"><span data-stu-id="43559-112">**CD3DX12\_PACKED\_MIP\_INFO(UINT8 numStandardMips, UINT8 numPackedMips, UINT numTilesForPackedMips, UINT startTileIndexInOverallResource)**</span></span>
</dt> <dd>

<span data-ttu-id="43559-113">Cria uma nova instância de uma CD3DX12 \_ de \_ informações MIP compactadas \_ , inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="43559-113">Creates a new instance of a CD3DX12\_PACKED\_MIP\_INFO, initializing the following parameters:</span></span>

<span data-ttu-id="43559-114">UINT8 numStandardMips</span><span class="sxs-lookup"><span data-stu-id="43559-114">UINT8 numStandardMips</span></span>

<span data-ttu-id="43559-115">UINT8 numPackedMips</span><span class="sxs-lookup"><span data-stu-id="43559-115">UINT8 numPackedMips</span></span>

<span data-ttu-id="43559-116">NumTilesForPackedMips UINT</span><span class="sxs-lookup"><span data-stu-id="43559-116">UINT numTilesForPackedMips</span></span>

<span data-ttu-id="43559-117">StartTileIndexInOverallResource UINT</span><span class="sxs-lookup"><span data-stu-id="43559-117">UINT startTileIndexInOverallResource</span></span>

</dd> <dt>

<span data-ttu-id="43559-118">**\_const do operador D3D12 \_ pacotes \_ de informações de MIP compactados& () constante**</span><span class="sxs-lookup"><span data-stu-id="43559-118">**operator const D3D12\_PACKED\_MIP\_INFO&() const**</span></span>
</dt> <dd>

<span data-ttu-id="43559-119">Define o & operador de passagem por referência para o tipo de estrutura pai.</span><span class="sxs-lookup"><span data-stu-id="43559-119">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="43559-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43559-120">Requirements</span></span>



| <span data-ttu-id="43559-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="43559-121">Requirement</span></span> | <span data-ttu-id="43559-122">Valor</span><span class="sxs-lookup"><span data-stu-id="43559-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="43559-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43559-123">Header</span></span><br/> | <dl> <span data-ttu-id="43559-124"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="43559-124"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43559-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="43559-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43559-126">**\_Informações de \_ MIP compactadas pelo D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="43559-126">**D3D12\_PACKED\_MIP\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info)
</dt> <dt>

[<span data-ttu-id="43559-127">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="43559-127">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





