---
title: Estrutura de CD3DX12_BLEND_DESC (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura Desc do D3D12 Blend \_ .
ms.assetid: D37BB62E-904B-4953-9119-21F3B37570C0
keywords:
- Estrutura de CD3DX12_BLEND_DESC
topic_type:
- apiref
api_name:
- CD3DX12_BLEND_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb88ce003f74251c3ce34a2ca47ae2fb55f892d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791485"
---
# <a name="cd3dx12_blend_desc-structure"></a><span data-ttu-id="49e45-104">\_Estrutura desc de Blend CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="49e45-104">CD3DX12\_BLEND\_DESC structure</span></span>

<span data-ttu-id="49e45-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ \_ Desc do D3D12 Blend**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) .</span><span class="sxs-lookup"><span data-stu-id="49e45-105">A helper structure to enable easy initialization of a [**D3D12\_BLEND\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="49e45-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49e45-106">Syntax</span></span>


```C++
struct CD3DX12_BLEND_DESC  : public D3D12_BLEND_DESC{
   CD3DX12_BLEND_DESC();
   explicit CD3DX12_BLEND_DESC(const D3D12_BLEND_DESC& o);
   explicit CD3DX12_BLEND_DESC(CD3DX12_DEFAULT);
   ~CD3DX12_BLEND_DESC();
   operator const D3D12_BLEND_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="49e45-107">Membros</span><span class="sxs-lookup"><span data-stu-id="49e45-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="49e45-108">**CD3DX12 \_ Blend \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="49e45-108">**CD3DX12\_BLEND\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="49e45-109">Cria uma instância nova e não inicializada de um CD3DX12 \_ Blend \_ desc.</span><span class="sxs-lookup"><span data-stu-id="49e45-109">Creates a new, uninitialized, instance of a CD3DX12\_BLEND\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="49e45-110">**Explicit CD3DX12 \_ Blend \_ DESC (const D3D12 \_ Blend \_ desc& o)**</span><span class="sxs-lookup"><span data-stu-id="49e45-110">**explicit CD3DX12\_BLEND\_DESC(const D3D12\_BLEND\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="49e45-111">Cria uma nova instância de um CD3DX12 \_ Blend \_ DESC, inicializada com o conteúdo de outra estrutura [**\_ \_ desc D3D12 Blend**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) .</span><span class="sxs-lookup"><span data-stu-id="49e45-111">Creates a new instance of a CD3DX12\_BLEND\_DESC, initialized with the contents of another [**D3D12\_BLEND\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="49e45-112">**CD3DX12 \_ Blend \_ DESC (padrão CD3DX12 \_ ) explícito**</span><span class="sxs-lookup"><span data-stu-id="49e45-112">**explicit CD3DX12\_BLEND\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="49e45-113">Cria uma nova instância de um CD3DX12 \_ Blend \_ DESC, inicializada com parâmetros padrão.</span><span class="sxs-lookup"><span data-stu-id="49e45-113">Creates a new instance of a CD3DX12\_BLEND\_DESC, initialized with default parameters.</span></span>



| <span data-ttu-id="49e45-114">Estado</span><span class="sxs-lookup"><span data-stu-id="49e45-114">State</span></span>                                   | <span data-ttu-id="49e45-115">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="49e45-115">Default Value</span></span>                    |
|-----------------------------------------|----------------------------------|
| <span data-ttu-id="49e45-116">AlphaToCoverageEnable</span><span class="sxs-lookup"><span data-stu-id="49e45-116">AlphaToCoverageEnable</span></span>                   | <span data-ttu-id="49e45-117">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="49e45-117">**FALSE**</span></span>                        |
| <span data-ttu-id="49e45-118">IndependentBlendEnable</span><span class="sxs-lookup"><span data-stu-id="49e45-118">IndependentBlendEnable</span></span>                  | <span data-ttu-id="49e45-119">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="49e45-119">**FALSE**</span></span>                        |
| <span data-ttu-id="49e45-120">RenderTarget \[ 0 \] . BlendEnable</span><span class="sxs-lookup"><span data-stu-id="49e45-120">RenderTarget\[0\].BlendEnable</span></span>           | <span data-ttu-id="49e45-121">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="49e45-121">**FALSE**</span></span>                        |
| <span data-ttu-id="49e45-122">RenderTarget \[ 0 \] . LogicOpEnable</span><span class="sxs-lookup"><span data-stu-id="49e45-122">RenderTarget\[0\].LogicOpEnable</span></span>         | <span data-ttu-id="49e45-123">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="49e45-123">**FALSE**</span></span>                        |
| <span data-ttu-id="49e45-124">RenderTarget \[ 0 \] . SrcBlend</span><span class="sxs-lookup"><span data-stu-id="49e45-124">RenderTarget\[0\].SrcBlend</span></span>              | <span data-ttu-id="49e45-125">D3D12 \_ Blend \_ One</span><span class="sxs-lookup"><span data-stu-id="49e45-125">D3D12\_BLEND\_ONE</span></span>                |
| <span data-ttu-id="49e45-126">RenderTarget \[ 0 \] . DestBlend</span><span class="sxs-lookup"><span data-stu-id="49e45-126">RenderTarget\[0\].DestBlend</span></span>             | <span data-ttu-id="49e45-127">D3D12 \_ Blend \_ zero</span><span class="sxs-lookup"><span data-stu-id="49e45-127">D3D12\_BLEND\_ZERO</span></span>               |
| <span data-ttu-id="49e45-128">RenderTarget \[ 0 \] . BlendOp</span><span class="sxs-lookup"><span data-stu-id="49e45-128">RenderTarget\[0\].BlendOp</span></span>               | <span data-ttu-id="49e45-129">\_ \_ Adicionar op D3D12 \_ Blend</span><span class="sxs-lookup"><span data-stu-id="49e45-129">D3D12\_BLEND\_OP\_ADD</span></span>            |
| <span data-ttu-id="49e45-130">RenderTarget \[ 0 \] . SrcBlendAlpha</span><span class="sxs-lookup"><span data-stu-id="49e45-130">RenderTarget\[0\].SrcBlendAlpha</span></span>         | <span data-ttu-id="49e45-131">D3D12 \_ Blend \_ One</span><span class="sxs-lookup"><span data-stu-id="49e45-131">D3D12\_BLEND\_ONE</span></span>                |
| <span data-ttu-id="49e45-132">RenderTarget \[ 0 \] . DestBlendAlpha</span><span class="sxs-lookup"><span data-stu-id="49e45-132">RenderTarget\[0\].DestBlendAlpha</span></span>        | <span data-ttu-id="49e45-133">D3D12 \_ Blend \_ zero</span><span class="sxs-lookup"><span data-stu-id="49e45-133">D3D12\_BLEND\_ZERO</span></span>               |
| <span data-ttu-id="49e45-134">RenderTarget \[ 0 \] . BlendOpAlpha</span><span class="sxs-lookup"><span data-stu-id="49e45-134">RenderTarget\[0\].BlendOpAlpha</span></span>          | <span data-ttu-id="49e45-135">\_ \_ Adicionar op D3D12 \_ Blend</span><span class="sxs-lookup"><span data-stu-id="49e45-135">D3D12\_BLEND\_OP\_ADD</span></span>            |
| <span data-ttu-id="49e45-136">RenderTarget \[ 0 \] . LogicOp</span><span class="sxs-lookup"><span data-stu-id="49e45-136">RenderTarget\[0\].LogicOp</span></span>               | <span data-ttu-id="49e45-137">\_NOOP de \_ op \_ lógico D3D12</span><span class="sxs-lookup"><span data-stu-id="49e45-137">D3D12\_LOGIC\_OP\_NOOP</span></span>           |
| <span data-ttu-id="49e45-138">RenderTarget \[ 0 \] . RenderTargetWriteMask</span><span class="sxs-lookup"><span data-stu-id="49e45-138">RenderTarget\[0\].RenderTargetWriteMask</span></span> | <span data-ttu-id="49e45-139">\_ \_ \_ Habilitar tudo para gravação de cores do D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="49e45-139">D3D12\_COLOR\_WRITE\_ENABLE\_ALL</span></span> |



 

</dd> <dt>

<span data-ttu-id="49e45-140">**~ CD3DX12 \_ Blend \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="49e45-140">**~CD3DX12\_BLEND\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="49e45-141">Destrói uma instância de um CD3DX12 \_ Blend \_ desc.</span><span class="sxs-lookup"><span data-stu-id="49e45-141">Destroys an instance of a CD3DX12\_BLEND\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="49e45-142">**\_const do operador D3D12 Blend \_ desc& () constante**</span><span class="sxs-lookup"><span data-stu-id="49e45-142">**operator const D3D12\_BLEND\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="49e45-143">Define o & operador de passagem por referência para o tipo de estrutura pai.</span><span class="sxs-lookup"><span data-stu-id="49e45-143">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="49e45-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49e45-144">Requirements</span></span>



| <span data-ttu-id="49e45-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="49e45-145">Requirement</span></span> | <span data-ttu-id="49e45-146">Valor</span><span class="sxs-lookup"><span data-stu-id="49e45-146">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="49e45-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="49e45-147">Header</span></span><br/> | <dl> <span data-ttu-id="49e45-148"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="49e45-148"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49e45-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="49e45-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49e45-150">**D3D12 de \_ combinação \_ desc**</span><span class="sxs-lookup"><span data-stu-id="49e45-150">**D3D12\_BLEND\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> <dt>

[<span data-ttu-id="49e45-151">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="49e45-151">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





