---
title: Interface ID3DX11EffectBlendVariable (D3dx11effect. h)
description: A interface Blend-Variable acessa o estado de mesclagem.
ms.assetid: 8a6e6e7e-2f1e-4e16-8d28-ffc7f3f018d6
keywords:
- Interface ID3DX11EffectBlendVariable Direct3D 11
- Interface ID3DX11EffectBlendVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57a0a8a3ec0c2a3d92dfc9579fff8b3769dcfc5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930753"
---
# <a name="id3dx11effectblendvariable-interface"></a><span data-ttu-id="4b3c5-105">Interface ID3DX11EffectBlendVariable</span><span class="sxs-lookup"><span data-stu-id="4b3c5-105">ID3DX11EffectBlendVariable interface</span></span>

<span data-ttu-id="4b3c5-106">A interface Blend-Variable acessa o estado de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="4b3c5-106">The blend-variable interface accesses blend state.</span></span>

## <a name="members"></a><span data-ttu-id="4b3c5-107">Membros</span><span class="sxs-lookup"><span data-stu-id="4b3c5-107">Members</span></span>

<span data-ttu-id="4b3c5-108">A interface **ID3DX11EffectBlendVariable** herda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="4b3c5-108">The **ID3DX11EffectBlendVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="4b3c5-109">**ID3DX11EffectBlendVariable** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4b3c5-109">**ID3DX11EffectBlendVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="4b3c5-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="4b3c5-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4b3c5-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="4b3c5-111">Methods</span></span>

<span data-ttu-id="4b3c5-112">A interface **ID3DX11EffectBlendVariable** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="4b3c5-112">The **ID3DX11EffectBlendVariable** interface has these methods.</span></span>



| <span data-ttu-id="4b3c5-113">Método</span><span class="sxs-lookup"><span data-stu-id="4b3c5-113">Method</span></span>                                                                    | <span data-ttu-id="4b3c5-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b3c5-114">Description</span></span>                                          |
|:--------------------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="4b3c5-115">**GetBackingStore**</span><span class="sxs-lookup"><span data-stu-id="4b3c5-115">**GetBackingStore**</span></span>](id3dx11effectblendvariable-getbackingstore.md)     | <span data-ttu-id="4b3c5-116">Obter um ponteiro para uma variável de estado de mistura.</span><span class="sxs-lookup"><span data-stu-id="4b3c5-116">Get a pointer to a blend-state variable.</span></span><br/>  |
| [<span data-ttu-id="4b3c5-117">**Getblendstate**</span><span class="sxs-lookup"><span data-stu-id="4b3c5-117">**GetBlendState**</span></span>](id3dx11effectblendvariable-getblendstate.md)         | <span data-ttu-id="4b3c5-118">Obtenha um ponteiro para uma interface de estado de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="4b3c5-118">Get a pointer to a blend-state interface.</span></span><br/> |
| [<span data-ttu-id="4b3c5-119">**Setblendstate**</span><span class="sxs-lookup"><span data-stu-id="4b3c5-119">**SetBlendState**</span></span>](id3dx11effectblendvariable-setblendstate.md)         | <span data-ttu-id="4b3c5-120">Define o estado de mesclagem de um efeito.</span><span class="sxs-lookup"><span data-stu-id="4b3c5-120">Sets an effect's blend-state.</span></span><br/>             |
| [<span data-ttu-id="4b3c5-121">**UndoSetBlendState**</span><span class="sxs-lookup"><span data-stu-id="4b3c5-121">**UndoSetBlendState**</span></span>](id3dx11effectblendvariable-undosetblendstate.md) | <span data-ttu-id="4b3c5-122">Reverte um estado de mesclagem definido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="4b3c5-122">Reverts a previously set blend-state.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="4b3c5-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b3c5-123">Remarks</span></span>

<span data-ttu-id="4b3c5-124">Uma interface [**ID3DX11EffectVariable**](id3dx11effectvariable.md) é criada quando um efeito é lido na memória.</span><span class="sxs-lookup"><span data-stu-id="4b3c5-124">An [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface is created when an effect is read into memory.</span></span>

<span data-ttu-id="4b3c5-125">As variáveis de efeito são salvas na memória no repositório de backup; Quando uma técnica é aplicada, os valores no repositório de backup são copiados para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4b3c5-125">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="4b3c5-126">Você pode usar qualquer um desses métodos para retornar o estado.</span><span class="sxs-lookup"><span data-stu-id="4b3c5-126">You can use either of these methods to return state.</span></span>

> [!Note]  
> <span data-ttu-id="4b3c5-127">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="4b3c5-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="4b3c5-128">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="4b3c5-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="4b3c5-129">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="4b3c5-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4b3c5-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b3c5-130">Requirements</span></span>



| <span data-ttu-id="4b3c5-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b3c5-131">Requirement</span></span> | <span data-ttu-id="4b3c5-132">Valor</span><span class="sxs-lookup"><span data-stu-id="4b3c5-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b3c5-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4b3c5-133">Header</span></span><br/>  | <dl> <span data-ttu-id="4b3c5-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b3c5-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4b3c5-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4b3c5-135">Library</span></span><br/> | <dl> <span data-ttu-id="4b3c5-136"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="4b3c5-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b3c5-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b3c5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b3c5-138">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="4b3c5-138">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="4b3c5-139">Efeitos 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="4b3c5-139">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="4b3c5-140">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="4b3c5-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





