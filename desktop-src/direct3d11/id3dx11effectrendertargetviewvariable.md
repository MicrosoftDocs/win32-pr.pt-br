---
title: Interface ID3DX11EffectRenderTargetViewVariable (D3dx11effect. h)
description: Uma interface render-Target-View acessa um destino render.
ms.assetid: 35c4e1da-05a8-4f1c-8730-58e3c90ad213
keywords:
- Interface ID3DX11EffectRenderTargetViewVariable Direct3D 11
- Interface ID3DX11EffectRenderTargetViewVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5b20f83639fd973016bbe263d9d21dae7b295c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968582"
---
# <a name="id3dx11effectrendertargetviewvariable-interface"></a><span data-ttu-id="e2fd6-105">Interface ID3DX11EffectRenderTargetViewVariable</span><span class="sxs-lookup"><span data-stu-id="e2fd6-105">ID3DX11EffectRenderTargetViewVariable interface</span></span>

<span data-ttu-id="e2fd6-106">Uma interface render-Target-View acessa um destino render.</span><span class="sxs-lookup"><span data-stu-id="e2fd6-106">A render-target-view interface accesses a render target.</span></span>

## <a name="members"></a><span data-ttu-id="e2fd6-107">Membros</span><span class="sxs-lookup"><span data-stu-id="e2fd6-107">Members</span></span>

<span data-ttu-id="e2fd6-108">A interface **ID3DX11EffectRenderTargetViewVariable** herda de [**ID3DX11EffectRasterizerVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="e2fd6-108">The **ID3DX11EffectRenderTargetViewVariable** interface inherits from [**ID3DX11EffectRasterizerVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="e2fd6-109">**ID3DX11EffectRenderTargetViewVariable** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e2fd6-109">**ID3DX11EffectRenderTargetViewVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="e2fd6-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="e2fd6-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e2fd6-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="e2fd6-111">Methods</span></span>

<span data-ttu-id="e2fd6-112">A interface **ID3DX11EffectRenderTargetViewVariable** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e2fd6-112">The **ID3DX11EffectRenderTargetViewVariable** interface has these methods.</span></span>



| <span data-ttu-id="e2fd6-113">Método</span><span class="sxs-lookup"><span data-stu-id="e2fd6-113">Method</span></span>                                                                                     | <span data-ttu-id="e2fd6-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="e2fd6-114">Description</span></span>                                |
|:-------------------------------------------------------------------------------------------|:-------------------------------------------|
| [<span data-ttu-id="e2fd6-115">**GetRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="e2fd6-115">**GetRenderTarget**</span></span>](id3dx11effectrendertargetviewvariable-getrendertarget.md)           | <span data-ttu-id="e2fd6-116">Obter um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="e2fd6-116">Get a render-target.</span></span><br/>            |
| [<span data-ttu-id="e2fd6-117">**GetRenderTargetArray**</span><span class="sxs-lookup"><span data-stu-id="e2fd6-117">**GetRenderTargetArray**</span></span>](id3dx11effectrendertargetviewvariable-getrendertargetarray.md) | <span data-ttu-id="e2fd6-118">Obtenha uma matriz de destinos de renderização.</span><span class="sxs-lookup"><span data-stu-id="e2fd6-118">Get an array of render-targets.</span></span><br/> |
| [<span data-ttu-id="e2fd6-119">**SetRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="e2fd6-119">**SetRenderTarget**</span></span>](id3dx11effectrendertargetviewvariable-setrendertarget.md)           | <span data-ttu-id="e2fd6-120">Defina um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="e2fd6-120">Set a render-target.</span></span><br/>            |
| [<span data-ttu-id="e2fd6-121">**SetRenderTargetArray**</span><span class="sxs-lookup"><span data-stu-id="e2fd6-121">**SetRenderTargetArray**</span></span>](id3dx11effectrendertargetviewvariable-setrendertargetarray.md) | <span data-ttu-id="e2fd6-122">Defina uma matriz de destinos de renderização.</span><span class="sxs-lookup"><span data-stu-id="e2fd6-122">Set an array of render-targets.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e2fd6-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2fd6-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e2fd6-124">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="e2fd6-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e2fd6-125">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="e2fd6-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e2fd6-126">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e2fd6-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e2fd6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2fd6-127">Requirements</span></span>



| <span data-ttu-id="e2fd6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2fd6-128">Requirement</span></span> | <span data-ttu-id="e2fd6-129">Valor</span><span class="sxs-lookup"><span data-stu-id="e2fd6-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2fd6-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e2fd6-130">Header</span></span><br/>  | <dl> <span data-ttu-id="e2fd6-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2fd6-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e2fd6-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e2fd6-132">Library</span></span><br/> | <dl> <span data-ttu-id="e2fd6-133"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="e2fd6-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2fd6-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2fd6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2fd6-135">**ID3DX11EffectRasterizerVariable**</span><span class="sxs-lookup"><span data-stu-id="e2fd6-135">**ID3DX11EffectRasterizerVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="e2fd6-136">Efeitos 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="e2fd6-136">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="e2fd6-137">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="e2fd6-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





