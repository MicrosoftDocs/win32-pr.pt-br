---
title: Estrutura de CD3DX12_DEPTH_STENCIL_DESC1 (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura DESC1 de estêncil de profundidade de D3D12 \_ \_ .
ms.assetid: 8EB008F9-212D-486E-9C62-D7BA9D3C6807
keywords:
- Estrutura de CD3DX12_DEPTH_STENCIL_DESC1
topic_type:
- apiref
api_name:
- CD3DX12_DEPTH_STENCIL_DESC1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976c05ec4f3ca85ccfcebb6a13dbe408ba05c64e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105747451"
---
# <a name="cd3dx12_depth_stencil_desc1-structure"></a><span data-ttu-id="0555e-104">\_ \_ Estrutura DESC1 de estêncil de profundidade de CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="0555e-104">CD3DX12\_DEPTH\_STENCIL\_DESC1 structure</span></span>

<span data-ttu-id="0555e-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**DESC1 de estêncil de profundidade de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) .</span><span class="sxs-lookup"><span data-stu-id="0555e-105">A helper structure to enable easy initialization of a [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="0555e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0555e-106">Syntax</span></span>


```C++
struct CD3DX12_DEPTH_STENCIL_DESC1  : public D3D12_DEPTH_STENCIL_DESC1{
  CD3DX12_DEPTH_STENCIL_DESC1 CD3DX12_DEPTH_STENCIL_DESC1();
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(const D3D12_DEPTH_STENCIL_DESC1& o);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(const D3D12_DEPTH_STENCIL_DESC& o);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(CD3DX12_DEFAULT);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(BOOL depthEnable, D3D12_DEPTH_WRITE_MASK depthWriteMask, D3D12_COMPARISON_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12_STENCIL_OP frontStencilFailOp, D3D12_STENCIL_OP frontStencilDepthFailOp, D3D12_STENCIL_OP frontStencilPassOp, D3D12_COMPARISON_FUNC frontStencilFunc, D3D12_STENCIL_OP backStencilFailOp, D3D12_STENCIL_OP backStencilDepthFailOp, D3D12_STENCIL_OP backStencilPassOp, D3D12_COMPARISON_FUNC backStencilFunc, BOOL depthBoundsTestEnable);
                              ~CD3DX12_DEPTH_STENCIL_DESC1();
                              operator const D3D12_DEPTH_STENCIL_DESC1&() const;
                              operator const D3D12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="0555e-107">Membros</span><span class="sxs-lookup"><span data-stu-id="0555e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0555e-108">**\_ \_ \_ DESC1 de estêncil de profundidade de CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="0555e-108">**CD3DX12\_DEPTH\_STENCIL\_DESC1()**</span></span>
</dt> <dd>

<span data-ttu-id="0555e-109">Cria uma instância nova e não inicializada de um DESC1 de \_ estêncil de profundidade de CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0555e-109">Creates a new, uninitialized, instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1.</span></span>

</dd> <dt>

<span data-ttu-id="0555e-110">**\_ \_ estêncil de profundidade de CD3DX12 explícito \_ DESC1 (const D3D12 \_ Depth \_ estêncil \_ DESC1& o)**</span><span class="sxs-lookup"><span data-stu-id="0555e-110">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(const D3D12\_DEPTH\_STENCIL\_DESC1& o)**</span></span>
</dt> <dd>

<span data-ttu-id="0555e-111">Cria uma nova instância de um estêncil de profundidade de CD3DX12 \_ \_ \_ DESC1, inicializada com valores copiados de uma estrutura [**\_ DESC1 de \_ estêncil \_ de profundidade D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) .</span><span class="sxs-lookup"><span data-stu-id="0555e-111">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with values copied from a [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0555e-112">**\_ \_ estêncil de profundidade de CD3DX12 explícito \_ DESC1 (const D3D12 \_ Depth \_ estêncil \_ desc& o)**</span><span class="sxs-lookup"><span data-stu-id="0555e-112">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(const D3D12\_DEPTH\_STENCIL\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="0555e-113">Cria uma nova instância de um estêncil de profundidade de CD3DX12 \_ \_ \_ DESC1, inicializada com valores copiados de uma estrutura [**\_ desc de \_ estêncil \_ de profundidade D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="0555e-113">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with values copied from a [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) structure</span></span>

<span data-ttu-id="0555e-114">e o membro **DepthBoundsTestEnable** adicional definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="0555e-114">and the additional **DepthBoundsTestEnable** member set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="0555e-115">**\_ \_ \_ DESC1 de estêncil de profundidade de CD3DX12 explícito ( \_ padrão CD3DX12)**</span><span class="sxs-lookup"><span data-stu-id="0555e-115">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="0555e-116">Cria uma nova instância de um estêncil de profundidade de CD3DX12 \_ \_ \_ DESC1, inicializada com o estado padrão prescrito por D3DX12:</span><span class="sxs-lookup"><span data-stu-id="0555e-116">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the default state prescribed by D3DX12:</span></span>

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
    DepthBoundsTestEnable = FALSE;
          
```

</dd> <dt>

<span data-ttu-id="0555e-117">**\_ \_ estêncil de profundidade de CD3DX12 explícito \_ DESC1 (bool depthEnable, D3D12 \_ profundidade de gravação de \_ \_ máscara DepthWriteMask, D3D12 de \_ comparação \_ Func DEPTHFUNC, bool STENCILENABLE, UINT8 StencilReadMask, UINT8 stencilWriteMask, D3D12 \_ estêncil \_ op FrontStencilFailOp, D3D12 \_ stencil \_ op frontStencilDepthFailOp, D3D12 \_ estêncil op frontStencilPassOp, D3D12 Comparison Func frontStencilFunc, D3D12 \_ estêncil op backStencilFailOp, \_ \_ \_ \_ D3D12 \_ stencil \_ op backStencilDepthFailOp, D3D12 estêncil op backStencilPassOp, D3D12 \_ Comparison Func backStencilFunc, \_ \_ \_ bool depthBoundsTestEnable)**</span><span class="sxs-lookup"><span data-stu-id="0555e-117">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(BOOL depthEnable, D3D12\_DEPTH\_WRITE\_MASK depthWriteMask, D3D12\_COMPARISON\_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12\_STENCIL\_OP frontStencilFailOp, D3D12\_STENCIL\_OP frontStencilDepthFailOp, D3D12\_STENCIL\_OP frontStencilPassOp, D3D12\_COMPARISON\_FUNC frontStencilFunc, D3D12\_STENCIL\_OP backStencilFailOp, D3D12\_STENCIL\_OP backStencilDepthFailOp, D3D12\_STENCIL\_OP backStencilPassOp, D3D12\_COMPARISON\_FUNC backStencilFunc, BOOL depthBoundsTestEnable)**</span></span>
</dt> <dd>

<span data-ttu-id="0555e-118">Cria uma nova instância de um estêncil de profundidade de CD3DX12 \_ \_ \_ DESC1, inicializada com os valores passados na lista de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0555e-118">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.</span></span>

</dd> <dt>

<span data-ttu-id="0555e-119">**~ CD3DX12 \_ \_ de estêncil \_ de profundidade DESC1 ()**</span><span class="sxs-lookup"><span data-stu-id="0555e-119">**~CD3DX12\_DEPTH\_STENCIL\_DESC1()**</span></span>
</dt> <dd>

<span data-ttu-id="0555e-120">Destrói uma instância de um estêncil de \_ profundidade de D3DX12 \_ \_ DESC1.</span><span class="sxs-lookup"><span data-stu-id="0555e-120">Destroys an instance of a D3DX12\_DEPTH\_STENCIL\_DESC1.</span></span>

</dd> <dt>

<span data-ttu-id="0555e-121">**D3D12 \_ \_ de estêncil const \_ de profundidade de DESC1& () const**</span><span class="sxs-lookup"><span data-stu-id="0555e-121">**operator const D3D12\_DEPTH\_STENCIL\_DESC1&() const**</span></span>
</dt> <dd>

<span data-ttu-id="0555e-122">Conversão implícita em uma \_ estrutura DESC1 de estêncil de profundidade de D3D12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0555e-122">Implicit conversion to a D3D12\_DEPTH\_STENCIL\_DESC1 structure.</span></span> <span data-ttu-id="0555e-123">Como \_ \_ o estêncil de profundidade de D3D12 \_ DESC1 é o tipo subjacente de estêncil de profundidade de CD3DX12 \_ \_ \_ DESC1, o objeto é simplesmente retornado como um estêncil de profundidade de D3D12 const \_ \_ \_ DESC1 referência a si mesmo.</span><span class="sxs-lookup"><span data-stu-id="0555e-123">Because D3D12\_DEPTH\_STENCIL\_DESC1 is the underlying type of CD3DX12\_DEPTH\_STENCIL\_DESC1, the object is simply returned as a const D3D12\_DEPTH\_STENCIL\_DESC1 reference to itself.</span></span>

</dd> <dt>

<span data-ttu-id="0555e-124">**\_ \_ const D3D12 de estêncil de profundidade de operador const \_ () constante**</span><span class="sxs-lookup"><span data-stu-id="0555e-124">**operator const D3D12\_DEPTH\_STENCIL\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="0555e-125">Conversão implícita em um \_ valor de \_ estrutura desc de estêncil de profundidade de D3D12 \_ .</span><span class="sxs-lookup"><span data-stu-id="0555e-125">Implicit conversion to a D3D12\_DEPTH\_STENCIL\_DESC structure value.</span></span> <span data-ttu-id="0555e-126">Como \_ o estêncil de profundidade D3D12 \_ \_ DESC não é o tipo subjacente de DESC1 de estêncil de profundidade de CD3DX12 \_ \_ \_ , uma nova \_ \_ instância de DESC de estêncil de profundidade D3D12 \_ é criada e retornada por valor.</span><span class="sxs-lookup"><span data-stu-id="0555e-126">Because D3D12\_DEPTH\_STENCIL\_DESC is not the underlying type of CD3DX12\_DEPTH\_STENCIL\_DESC1, a new D3D12\_DEPTH\_STENCIL\_DESC instance is created and returned by value.</span></span> <span data-ttu-id="0555e-127">Observe que \_ o estêncil de profundidade D3D12 \_ \_ DESC não inclui o membro **DepthBoundsTestEnable** , portanto, esse valor é perdido na conversão.</span><span class="sxs-lookup"><span data-stu-id="0555e-127">Note that D3D12\_DEPTH\_STENCIL\_DESC does not include the **DepthBoundsTestEnable** member, so this value is lost in the conversion.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0555e-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0555e-128">Requirements</span></span>



| <span data-ttu-id="0555e-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="0555e-129">Requirement</span></span> | <span data-ttu-id="0555e-130">Valor</span><span class="sxs-lookup"><span data-stu-id="0555e-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0555e-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0555e-131">Header</span></span><br/> | <dl> <span data-ttu-id="0555e-132"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="0555e-132"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0555e-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="0555e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0555e-134">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="0555e-134">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="0555e-135">**Estêncil de profundidade de D3D12 \_ \_ \_ DESC1**</span><span class="sxs-lookup"><span data-stu-id="0555e-135">**D3D12\_DEPTH\_STENCIL\_DESC1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> <dt>

[<span data-ttu-id="0555e-136">**Desc. de estêncil de profundidade de D3D12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0555e-136">**D3D12\_DEPTH\_STENCIL\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 





