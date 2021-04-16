---
title: Estrutura de CD3DX12_RASTERIZER_DESC (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura Desc do rasterizador D3D12 \_ .
ms.assetid: 28AA8256-1CAF-484F-B219-0F0461BA947C
keywords:
- Estrutura de CD3DX12_RASTERIZER_DESC
topic_type:
- apiref
api_name:
- CD3DX12_RASTERIZER_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 078b9e92d25cb5309b4cd97d35586192a37eed90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761599"
---
# <a name="cd3dx12_rasterizer_desc-structure"></a><span data-ttu-id="446bb-104">\_Estrutura Desc do rasterizador CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="446bb-104">CD3DX12\_RASTERIZER\_DESC structure</span></span>

<span data-ttu-id="446bb-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ \_ Desc do rasterizador D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) .</span><span class="sxs-lookup"><span data-stu-id="446bb-105">A helper structure to enable easy initialization of a [**D3D12\_RASTERIZER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="446bb-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="446bb-106">Syntax</span></span>


```C++
struct CD3DX12_RASTERIZER_DESC  : public D3D12_RASTERIZER_DESC{
   CD3DX12_RASTERIZER_DESC();
   explicit CD3DX12_RASTERIZER_DESC(const D3D12_RASTERIZER_DESC& o);
   explicit CD3DX12_RASTERIZER_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_RASTERIZER_DESC(D3D12_FILL_MODE fillMode, D3D12_CULL_MODE cullMode, BOOL frontCounterClockwise, INT depthBias, FLOAT depthBiasClamp, FLOAT slopeScaledDepthBias, BOOL depthClipEnable, BOOL multisampleEnable, BOOL antialiasedLineEnable, UINT forcedSampleCount, D3D12_CONSERVATIVE_RASTERIZATION_MODE conservativeRaster);
   ~CD3DX12_RASTERIZER_DESC();
   operator const D3D12_RASTERIZER_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="446bb-107">Membros</span><span class="sxs-lookup"><span data-stu-id="446bb-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="446bb-108">**CD3DX12 \_ do rasterizador \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="446bb-108">**CD3DX12\_RASTERIZER\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="446bb-109">Cria uma instância nova e não inicializada de uma CD3DX12 do \_ rasterizador \_ desc.</span><span class="sxs-lookup"><span data-stu-id="446bb-109">Creates a new, uninitialized, instance of a CD3DX12\_RASTERIZER\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="446bb-110">**CD3DX12 \_ de rasterizador explícito \_ (const D3D12 \_ rasterizador \_ desc& o)**</span><span class="sxs-lookup"><span data-stu-id="446bb-110">**explicit CD3DX12\_RASTERIZER\_DESC(const D3D12\_RASTERIZER\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="446bb-111">Cria uma nova instância de um \_ rasterizador CD3DX12 \_ DESC, inicializada com o conteúdo de outra estrutura de [**D3D12 do \_ rasterizador \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) .</span><span class="sxs-lookup"><span data-stu-id="446bb-111">Creates a new instance of a CD3DX12\_RASTERIZER\_DESC, initialized with the contents of another [**D3D12\_RASTERIZER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="446bb-112">**CD3DX12 \_ de rasterizador explícito \_ ( \_ padrão CD3DX12)**</span><span class="sxs-lookup"><span data-stu-id="446bb-112">**explicit CD3DX12\_RASTERIZER\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="446bb-113">Cria uma nova instância de um \_ rasterizador CD3DX12 \_ DESC, inicializada com parâmetros padrão.</span><span class="sxs-lookup"><span data-stu-id="446bb-113">Creates a new instance of a CD3DX12\_RASTERIZER\_DESC, initialized with default parameters.</span></span>

``` syntax
        FillMode = D3D12_FILL_MODE_SOLID;  
        CullMode = D3D12_CULL_MODE_BACK;  
        FrontCounterClockwise = FALSE;  
        DepthBias = D3D12_DEFAULT_DEPTH_BIAS;  
        DepthBiasClamp = D3D12_DEFAULT_DEPTH_BIAS_CLAMP;  
        SlopeScaledDepthBias = D3D12_DEFAULT_SLOPE_SCALED_DEPTH_BIAS;  
        DepthClipEnable = TRUE;  
        MultisampleEnable = FALSE;  
        AntialiasedLineEnable = FALSE;  
        ForcedSampleCount = 0;  
        ConservativeRaster = D3D12_CONSERVATIVE_RASTERIZATION_MODE_OFF;  
```

</dd> <dt>

<span data-ttu-id="446bb-114">**Explicit CD3DX12 \_ rasterizador \_ DESC (D3D12 \_ modo de preenchimento \_ fillMode, D3D12 selecionar \_ \_ modo de seleção, bool FrontCounterClockwise, int DepthBias, float DepthBiasClamp, float SlopeScaledDepthBias, BOOL DepthClipEnable, bool MultisampleEnable, bool antialiasedLineEnable, uint forcedSampleCount, \_ D3D12 \_ modo de rasterização conservador conservativeRaster \_ )**</span><span class="sxs-lookup"><span data-stu-id="446bb-114">**explicit CD3DX12\_RASTERIZER\_DESC(D3D12\_FILL\_MODE fillMode, D3D12\_CULL\_MODE cullMode, BOOL frontCounterClockwise, INT depthBias, FLOAT depthBiasClamp, FLOAT slopeScaledDepthBias, BOOL depthClipEnable, BOOL multisampleEnable, BOOL antialiasedLineEnable, UINT forcedSampleCount, D3D12\_CONSERVATIVE\_RASTERIZATION\_MODE conservativeRaster)**</span></span>
</dt> <dd>

<span data-ttu-id="446bb-115">Cria uma nova instância de um \_ rasterizador CD3DX12 \_ DESC, inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="446bb-115">Creates a new instance of a CD3DX12\_RASTERIZER\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="446bb-116">[**D3D12 \_ \_Modo de preenchimento**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode) fillMode</span><span class="sxs-lookup"><span data-stu-id="446bb-116">[**D3D12\_FILL\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode) fillMode</span></span>

<span data-ttu-id="446bb-117">[**D3D12 \_ \_Modo de seleção**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode) de seleção</span><span class="sxs-lookup"><span data-stu-id="446bb-117">[**D3D12\_CULL\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode) cullMode</span></span>

<span data-ttu-id="446bb-118">FrontCounterClockwise BOOL</span><span class="sxs-lookup"><span data-stu-id="446bb-118">BOOL frontCounterClockwise</span></span>

<span data-ttu-id="446bb-119">DepthBias INT</span><span class="sxs-lookup"><span data-stu-id="446bb-119">INT depthBias</span></span>

<span data-ttu-id="446bb-120">DepthBiasClamp flutuante</span><span class="sxs-lookup"><span data-stu-id="446bb-120">FLOAT depthBiasClamp</span></span>

<span data-ttu-id="446bb-121">SlopeScaledDepthBias flutuante</span><span class="sxs-lookup"><span data-stu-id="446bb-121">FLOAT slopeScaledDepthBias</span></span>

<span data-ttu-id="446bb-122">DepthClipEnable BOOL</span><span class="sxs-lookup"><span data-stu-id="446bb-122">BOOL depthClipEnable</span></span>

<span data-ttu-id="446bb-123">MultisampleEnable BOOL</span><span class="sxs-lookup"><span data-stu-id="446bb-123">BOOL multisampleEnable</span></span>

<span data-ttu-id="446bb-124">AntialiasedLineEnable BOOL</span><span class="sxs-lookup"><span data-stu-id="446bb-124">BOOL antialiasedLineEnable</span></span>

<span data-ttu-id="446bb-125">ForcedSampleCount UINT</span><span class="sxs-lookup"><span data-stu-id="446bb-125">UINT forcedSampleCount</span></span>

<span data-ttu-id="446bb-126">[**D3D12 \_ \_ \_ Modo de rasterização conservador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) conservativeRaster</span><span class="sxs-lookup"><span data-stu-id="446bb-126">[**D3D12\_CONSERVATIVE\_RASTERIZATION\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) conservativeRaster</span></span>

</dd> <dt>

<span data-ttu-id="446bb-127">**~ CD3DX12 \_ do rasterizador \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="446bb-127">**~CD3DX12\_RASTERIZER\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="446bb-128">Destrói uma instância de um \_ rasterizador CD3DX12 \_ desc.</span><span class="sxs-lookup"><span data-stu-id="446bb-128">Destroys an instance of a CD3DX12\_RASTERIZER\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="446bb-129">**\_const de D3D12 const do rasterizador \_ desc& () constante**</span><span class="sxs-lookup"><span data-stu-id="446bb-129">**operator const D3D12\_RASTERIZER\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="446bb-130">Define o & operador de passagem por referência para o tipo de estrutura pai.</span><span class="sxs-lookup"><span data-stu-id="446bb-130">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="446bb-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="446bb-131">Requirements</span></span>



| <span data-ttu-id="446bb-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="446bb-132">Requirement</span></span> | <span data-ttu-id="446bb-133">Valor</span><span class="sxs-lookup"><span data-stu-id="446bb-133">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="446bb-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="446bb-134">Header</span></span><br/> | <dl> <span data-ttu-id="446bb-135"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="446bb-135"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="446bb-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="446bb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="446bb-137">**D3D12 do \_ rasterizador \_ desc**</span><span class="sxs-lookup"><span data-stu-id="446bb-137">**D3D12\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> <dt>

[<span data-ttu-id="446bb-138">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="446bb-138">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





