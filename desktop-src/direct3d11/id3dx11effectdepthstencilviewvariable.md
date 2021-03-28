---
title: Interface ID3DX11EffectDepthStencilViewVariable (D3dx11effect. h)
description: Uma interface de profundidade-estêncil-exibição-variável acessa uma exibição de estêncil de profundidade.
ms.assetid: 316bf0cc-a7cd-4a40-932a-d566e3c2001e
keywords:
- Interface ID3DX11EffectDepthStencilViewVariable Direct3D 11
- Interface ID3DX11EffectDepthStencilViewVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51961bd1300157eef4acb4dd15484d5146a166f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173091"
---
# <a name="id3dx11effectdepthstencilviewvariable-interface"></a><span data-ttu-id="f425d-105">Interface ID3DX11EffectDepthStencilViewVariable</span><span class="sxs-lookup"><span data-stu-id="f425d-105">ID3DX11EffectDepthStencilViewVariable interface</span></span>

<span data-ttu-id="f425d-106">Uma interface de profundidade-estêncil-exibição-variável acessa uma exibição de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="f425d-106">A depth-stencil-view-variable interface accesses a depth-stencil view.</span></span>

## <a name="members"></a><span data-ttu-id="f425d-107">Membros</span><span class="sxs-lookup"><span data-stu-id="f425d-107">Members</span></span>

<span data-ttu-id="f425d-108">A interface **ID3DX11EffectDepthStencilViewVariable** herda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="f425d-108">The **ID3DX11EffectDepthStencilViewVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="f425d-109">**ID3DX11EffectDepthStencilViewVariable** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f425d-109">**ID3DX11EffectDepthStencilViewVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="f425d-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="f425d-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f425d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="f425d-111">Methods</span></span>

<span data-ttu-id="f425d-112">A interface **ID3DX11EffectDepthStencilViewVariable** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f425d-112">The **ID3DX11EffectDepthStencilViewVariable** interface has these methods.</span></span>



| <span data-ttu-id="f425d-113">Método</span><span class="sxs-lookup"><span data-stu-id="f425d-113">Method</span></span>                                                                                     | <span data-ttu-id="f425d-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="f425d-114">Description</span></span>                                              |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| [<span data-ttu-id="f425d-115">**GetDepthStencil**</span><span class="sxs-lookup"><span data-stu-id="f425d-115">**GetDepthStencil**</span></span>](id3dx11effectdepthstencilviewvariable-getdepthstencil.md)           | <span data-ttu-id="f425d-116">Obtenha um recurso de exibição de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="f425d-116">Get a depth-stencil-view resource.</span></span><br/>            |
| [<span data-ttu-id="f425d-117">**GetDepthStencilArray**</span><span class="sxs-lookup"><span data-stu-id="f425d-117">**GetDepthStencilArray**</span></span>](id3dx11effectdepthstencilviewvariable-getdepthstencilarray.md) | <span data-ttu-id="f425d-118">Obtenha uma matriz de recursos de exibição de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="f425d-118">Get an array of depth-stencil-view resources.</span></span><br/> |
| [<span data-ttu-id="f425d-119">**SetDepthStencil**</span><span class="sxs-lookup"><span data-stu-id="f425d-119">**SetDepthStencil**</span></span>](id3dx11effectdepthstencilviewvariable-setdepthstencil.md)           | <span data-ttu-id="f425d-120">Defina um recurso de exibição de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="f425d-120">Set a depth-stencil-view resource.</span></span><br/>            |
| [<span data-ttu-id="f425d-121">**SetDepthStencilArray**</span><span class="sxs-lookup"><span data-stu-id="f425d-121">**SetDepthStencilArray**</span></span>](id3dx11effectdepthstencilviewvariable-setdepthstencilarray.md) | <span data-ttu-id="f425d-122">Defina uma matriz de recursos de exibição de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="f425d-122">Set an array of depth-stencil-view resources.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f425d-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="f425d-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f425d-124">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="f425d-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f425d-125">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="f425d-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f425d-126">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f425d-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f425d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f425d-127">Requirements</span></span>



| <span data-ttu-id="f425d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f425d-128">Requirement</span></span> | <span data-ttu-id="f425d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="f425d-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f425d-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f425d-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f425d-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f425d-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f425d-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f425d-132">Library</span></span><br/> | <dl> <span data-ttu-id="f425d-133"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="f425d-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f425d-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="f425d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f425d-135">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="f425d-135">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="f425d-136">Efeitos 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="f425d-136">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="f425d-137">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="f425d-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





