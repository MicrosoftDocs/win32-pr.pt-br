---
title: Interface ID3DX11EffectDepthStencilVariable (D3dx11effect. h)
description: Uma interface de profundidade-estêncil-variável acessa o estado de estêncil de profundidade.
ms.assetid: 8fb1be19-eed4-4d69-bbbe-94484531eba2
keywords:
- Interface ID3DX11EffectDepthStencilVariable Direct3D 11
- Interface ID3DX11EffectDepthStencilVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d7aa520df0c13c81435421d5f605f901a61da6e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930709"
---
# <a name="id3dx11effectdepthstencilvariable-interface"></a><span data-ttu-id="4c1c2-105">Interface ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="4c1c2-105">ID3DX11EffectDepthStencilVariable interface</span></span>

<span data-ttu-id="4c1c2-106">Uma interface de profundidade-estêncil-variável acessa o estado de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="4c1c2-106">A depth-stencil-variable interface accesses depth-stencil state.</span></span>

## <a name="members"></a><span data-ttu-id="4c1c2-107">Membros</span><span class="sxs-lookup"><span data-stu-id="4c1c2-107">Members</span></span>

<span data-ttu-id="4c1c2-108">A interface **ID3DX11EffectDepthStencilVariable** herda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="4c1c2-108">The **ID3DX11EffectDepthStencilVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="4c1c2-109">**ID3DX11EffectDepthStencilVariable** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4c1c2-109">**ID3DX11EffectDepthStencilVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="4c1c2-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="4c1c2-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4c1c2-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="4c1c2-111">Methods</span></span>

<span data-ttu-id="4c1c2-112">A interface **ID3DX11EffectDepthStencilVariable** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="4c1c2-112">The **ID3DX11EffectDepthStencilVariable** interface has these methods.</span></span>



| <span data-ttu-id="4c1c2-113">Método</span><span class="sxs-lookup"><span data-stu-id="4c1c2-113">Method</span></span>                                                                                         | <span data-ttu-id="4c1c2-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="4c1c2-114">Description</span></span>                                                               |
|:-----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="4c1c2-115">**GetBackingStore**</span><span class="sxs-lookup"><span data-stu-id="4c1c2-115">**GetBackingStore**</span></span>](id3dx11effectdepthstencilvariable-getbackingstore.md)                   | <span data-ttu-id="4c1c2-116">Obtenha um ponteiro para uma variável que contém o estado de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="4c1c2-116">Get a pointer to a variable that contains depth-stencil state.</span></span><br/> |
| [<span data-ttu-id="4c1c2-117">**GetDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="4c1c2-117">**GetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-getdepthstencilstate.md)         | <span data-ttu-id="4c1c2-118">Obtenha um ponteiro para uma interface de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="4c1c2-118">Get a pointer to a depth-stencil interface.</span></span><br/>                    |
| [<span data-ttu-id="4c1c2-119">**SetDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="4c1c2-119">**SetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)         | <span data-ttu-id="4c1c2-120">Define o estado de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="4c1c2-120">Sets the depth stencil state.</span></span><br/>                                  |
| [<span data-ttu-id="4c1c2-121">**UndoSetDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="4c1c2-121">**UndoSetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md) | <span data-ttu-id="4c1c2-122">Reverte um estado de estêncil de profundidade definido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="4c1c2-122">Reverts a previously set depth stencil state.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="4c1c2-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c1c2-123">Remarks</span></span>

<span data-ttu-id="4c1c2-124">Uma interface [**ID3DX11EffectVariable**](id3dx11effectvariable.md) é criada quando um efeito é lido na memória.</span><span class="sxs-lookup"><span data-stu-id="4c1c2-124">An [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface is created when an effect is read into memory.</span></span>

<span data-ttu-id="4c1c2-125">As variáveis de efeito são salvas na memória no repositório de backup; Quando uma técnica é aplicada, os valores no repositório de backup são copiados para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4c1c2-125">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="4c1c2-126">Você pode usar qualquer um desses métodos para retornar o estado.</span><span class="sxs-lookup"><span data-stu-id="4c1c2-126">You can use either of these methods to return state.</span></span>

> [!Note]  
> <span data-ttu-id="4c1c2-127">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="4c1c2-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="4c1c2-128">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="4c1c2-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="4c1c2-129">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="4c1c2-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4c1c2-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c1c2-130">Requirements</span></span>



| <span data-ttu-id="4c1c2-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c1c2-131">Requirement</span></span> | <span data-ttu-id="4c1c2-132">Valor</span><span class="sxs-lookup"><span data-stu-id="4c1c2-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c1c2-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4c1c2-133">Header</span></span><br/>  | <dl> <span data-ttu-id="4c1c2-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c1c2-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4c1c2-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4c1c2-135">Library</span></span><br/> | <dl> <span data-ttu-id="4c1c2-136"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="4c1c2-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c1c2-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c1c2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c1c2-138">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="4c1c2-138">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="4c1c2-139">Efeitos 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="4c1c2-139">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="4c1c2-140">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="4c1c2-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





