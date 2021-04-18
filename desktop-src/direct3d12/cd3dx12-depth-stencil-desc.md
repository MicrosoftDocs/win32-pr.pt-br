---
title: Estrutura de CD3DX12_DEPTH_STENCIL_DESC (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura desc de estêncil de profundidade de D3D12 \_ \_ .
ms.assetid: D3DB04C3-4564-45A4-830A-E63B8D308B33
keywords:
- Estrutura de CD3DX12_DEPTH_STENCIL_DESC
topic_type:
- apiref
api_name:
- CD3DX12_DEPTH_STENCIL_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f36a071251a12c4d27d06586775c01759b88d38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105750520"
---
# <a name="cd3dx12_depth_stencil_desc-structure"></a><span data-ttu-id="ce70e-104">\_ \_ Estrutura desc de estêncil de profundidade de CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="ce70e-104">CD3DX12\_DEPTH\_STENCIL\_DESC structure</span></span>

<span data-ttu-id="ce70e-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**desc de estêncil de profundidade de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) .</span><span class="sxs-lookup"><span data-stu-id="ce70e-105">A helper structure to enable easy initialization of a [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce70e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce70e-106">Syntax</span></span>


```C++
struct CD3DX12_DEPTH_STENCIL_DESC  : public D3D12_DEPTH_STENCIL_DESC{
   CD3DX12_DEPTH_STENCIL_DESC();
   explicit CD3DX12_DEPTH_STENCIL_DESC(const D3D12_DEPTH_STENCIL_DESC& o);
   explicit CD3DX12_DEPTH_STENCIL_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_DEPTH_STENCIL_DESC(BOOL depthEnable, D3D12_DEPTH_WRITE_MASK depthWriteMask, D3D12_COMPARISON_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12_STENCIL_OP frontStencilFailOp, D3D12_STENCIL_OP frontStencilDepthFailOp, D3D12_STENCIL_OP frontStencilPassOp, D3D12_COMPARISON_FUNC frontStencilFunc, D3D12_STENCIL_OP backStencilFailOp, D3D12_STENCIL_OP backStencilDepthFailOp, D3D12_STENCIL_OP backStencilPassOp, D3D12_COMPARISON_FUNC backStencilFunc);
   ~CD3DX12_DEPTH_STENCIL_DESC();
   operator const D3D12_DEPTH_STENCIL_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="ce70e-107">Membros</span><span class="sxs-lookup"><span data-stu-id="ce70e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ce70e-108">**\_ \_ Estêncil de profundidade \_ de CD3DX12 DESC ()**</span><span class="sxs-lookup"><span data-stu-id="ce70e-108">**CD3DX12\_DEPTH\_STENCIL\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="ce70e-109">Cria uma nova instância, não inicializada, de um \_ estêncil de profundidade D3DX12 \_ \_ desc.</span><span class="sxs-lookup"><span data-stu-id="ce70e-109">Creates a new, uninitialized, instance of a D3DX12\_DEPTH\_STENCIL\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="ce70e-110">**\_ \_ estêncil de profundidade de CD3DX12 explícito \_ DESC (const D3D12 \_ Depth \_ estêncil \_ desc& o)**</span><span class="sxs-lookup"><span data-stu-id="ce70e-110">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC(const D3D12\_DEPTH\_STENCIL\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="ce70e-111">Cria uma nova instância de um estêncil de profundidade de D3DX12 \_ \_ \_ DESC, inicializada com o conteúdo de outra estrutura [**desc de estêncil de profundidade de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) .</span><span class="sxs-lookup"><span data-stu-id="ce70e-111">Creates a new instance of a D3DX12\_DEPTH\_STENCIL\_DESC, initialized with the contents of another [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ce70e-112">**\_ \_ estêncil de profundidade de CD3DX12 explícito \_ DESC ( \_ padrão CD3DX12)**</span><span class="sxs-lookup"><span data-stu-id="ce70e-112">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="ce70e-113">Cria uma nova instância de um \_ estêncil de profundidade D3DX12 \_ \_ DESC, inicializada com parâmetros padrão.</span><span class="sxs-lookup"><span data-stu-id="ce70e-113">Creates a new instance of a D3DX12\_DEPTH\_STENCIL\_DESC, initialized with default parameters.</span></span>

``` syntax
        DepthEnable = TRUE;  
        DepthWriteMask = D3D12_DEPTH_WRITE_MASK_ALL;  
        DepthFunc = D3D12_COMPARISON_FUNC_LESS;  
        StencilEnable = FALSE;  
        StencilReadMask = D3D12_DEFAULT_STENCIL_READ_MASK;  
        StencilWriteMask = D3D12_DEFAULT_STENCIL_WRITE_MASK;  
        const D3D12_DEPTH_STENCILOP_DESC defaultStencilOp =  
        { D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_KEEP, D3D12_COMPARISON_FUNC_ALWAYS };  
        FrontFace = defaultStencilOp;  
        BackFace = defaultStencilOp;  
```

</dd> <dt>

<span data-ttu-id="ce70e-114">**\_ \_ estêncil de profundidade de CD3DX12 explícito \_ DESC (bool depthEnable, D3D12 \_ profundidade \_ Write \_ Mask depthWriteMask, D3D12 \_ Comparison \_ Func DEPTHFUNC, bool STENCILENABLE, UINT8 StencilReadMask, UINT8 stencilWriteMask, D3D12 \_ estêncil \_ op FrontStencilFailOp, D3D12 \_ stencil \_ op frontStencilDepthFailOp, D3D12 \_ estêncil op \_ frontStencilPassOp, D3D12 \_ Comparison Func frontStencilFunc, D3D12 \_ \_ estêncil op backStencilFailOp \_ , D3D12 \_ stencil \_ \_ \_ \_ \_ op backStencilDepthFailOp, D3D12 estêncil op backStencilPassOp, D3D12 Comparison Func backStencilFunc)**</span><span class="sxs-lookup"><span data-stu-id="ce70e-114">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC(BOOL depthEnable, D3D12\_DEPTH\_WRITE\_MASK depthWriteMask, D3D12\_COMPARISON\_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12\_STENCIL\_OP frontStencilFailOp, D3D12\_STENCIL\_OP frontStencilDepthFailOp, D3D12\_STENCIL\_OP frontStencilPassOp, D3D12\_COMPARISON\_FUNC frontStencilFunc, D3D12\_STENCIL\_OP backStencilFailOp, D3D12\_STENCIL\_OP backStencilDepthFailOp, D3D12\_STENCIL\_OP backStencilPassOp, D3D12\_COMPARISON\_FUNC backStencilFunc)**</span></span>
</dt> <dd>

<span data-ttu-id="ce70e-115">Cria uma nova instância de um \_ estêncil de profundidade D3DX12 \_ \_ DESC, inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="ce70e-115">Creates a new instance of a D3DX12\_DEPTH\_STENCIL\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="ce70e-116">DepthEnable BOOL</span><span class="sxs-lookup"><span data-stu-id="ce70e-116">BOOL depthEnable</span></span>

<span data-ttu-id="ce70e-117">[**D3D12 \_ \_ \_ Máscara de gravação de profundidade**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) depthWriteMask</span><span class="sxs-lookup"><span data-stu-id="ce70e-117">[**D3D12\_DEPTH\_WRITE\_MASK**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) depthWriteMask</span></span>

<span data-ttu-id="ce70e-118">[**D3D12 \_ COMPARAÇÃO de \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) depthFunc</span><span class="sxs-lookup"><span data-stu-id="ce70e-118">[**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) depthFunc</span></span>

<span data-ttu-id="ce70e-119">StencilEnable BOOL</span><span class="sxs-lookup"><span data-stu-id="ce70e-119">BOOL stencilEnable</span></span>

<span data-ttu-id="ce70e-120">UINT8 stencilReadMask</span><span class="sxs-lookup"><span data-stu-id="ce70e-120">UINT8 stencilReadMask</span></span>

<span data-ttu-id="ce70e-121">UINT8 stencilWriteMask</span><span class="sxs-lookup"><span data-stu-id="ce70e-121">UINT8 stencilWriteMask</span></span>

<span data-ttu-id="ce70e-122">[**D3D12 \_ FrontStencilFailOp \_ op de estêncil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)</span><span class="sxs-lookup"><span data-stu-id="ce70e-122">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilFailOp</span></span>

<span data-ttu-id="ce70e-123">[**D3D12 \_ FrontStencilDepthFailOp \_ op de estêncil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)</span><span class="sxs-lookup"><span data-stu-id="ce70e-123">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilDepthFailOp</span></span>

<span data-ttu-id="ce70e-124">[**D3D12 \_ FrontStencilPassOp \_ op de estêncil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)</span><span class="sxs-lookup"><span data-stu-id="ce70e-124">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilPassOp</span></span>

<span data-ttu-id="ce70e-125">[**D3D12 \_ COMPARAÇÃO de \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) frontStencilFunc</span><span class="sxs-lookup"><span data-stu-id="ce70e-125">[**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) frontStencilFunc</span></span>

<span data-ttu-id="ce70e-126">[**D3D12 \_ BackStencilFailOp \_ op de estêncil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)</span><span class="sxs-lookup"><span data-stu-id="ce70e-126">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilFailOp</span></span>

<span data-ttu-id="ce70e-127">[**D3D12 \_ BackStencilDepthFailOp \_ op de estêncil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)</span><span class="sxs-lookup"><span data-stu-id="ce70e-127">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilDepthFailOp</span></span>

<span data-ttu-id="ce70e-128">[**D3D12 \_ BackStencilPassOp \_ op de estêncil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)</span><span class="sxs-lookup"><span data-stu-id="ce70e-128">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilPassOp</span></span>

<span data-ttu-id="ce70e-129">[**D3D12 \_ COMPARAÇÃO de \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) backStencilFunc</span><span class="sxs-lookup"><span data-stu-id="ce70e-129">[**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) backStencilFunc</span></span>

</dd> <dt>

<span data-ttu-id="ce70e-130">**~ \_ \_ Estêncil de profundidade \_ de CD3DX12 DESC ()**</span><span class="sxs-lookup"><span data-stu-id="ce70e-130">**~CD3DX12\_DEPTH\_STENCIL\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="ce70e-131">Destrói uma instância de um estêncil de \_ profundidade \_ CD3DX12 \_ desc.</span><span class="sxs-lookup"><span data-stu-id="ce70e-131">Destroys an instance of a CD3DX12\_DEPTH\_STENCIL\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="ce70e-132">**\_const D3D12 de profundidade \_ de estêncil const \_& () constante**</span><span class="sxs-lookup"><span data-stu-id="ce70e-132">**operator const D3D12\_DEPTH\_STENCIL\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="ce70e-133">Define o & operador de passagem por referência para o tipo de estrutura pai.</span><span class="sxs-lookup"><span data-stu-id="ce70e-133">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce70e-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce70e-134">Requirements</span></span>



| <span data-ttu-id="ce70e-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce70e-135">Requirement</span></span> | <span data-ttu-id="ce70e-136">Valor</span><span class="sxs-lookup"><span data-stu-id="ce70e-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ce70e-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ce70e-137">Header</span></span><br/> | <dl> <span data-ttu-id="ce70e-138"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce70e-138"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce70e-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce70e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce70e-140">**Desc. de estêncil de profundidade de D3D12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ce70e-140">**D3D12\_DEPTH\_STENCIL\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> <dt>

[<span data-ttu-id="ce70e-141">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="ce70e-141">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





