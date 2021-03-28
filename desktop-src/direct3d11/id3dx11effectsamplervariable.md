---
title: Interface ID3DX11EffectSamplerVariable (D3dx11effect. h)
description: Uma interface de amostra acessa o estado de amostra.
ms.assetid: 8d21f829-2145-45f2-a9b4-2fdc06e0a879
keywords:
- Interface ID3DX11EffectSamplerVariable Direct3D 11
- Interface ID3DX11EffectSamplerVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b5019022cea823566611410cd6e8fd5013380b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104092001"
---
# <a name="id3dx11effectsamplervariable-interface"></a><span data-ttu-id="e47e6-105">Interface ID3DX11EffectSamplerVariable</span><span class="sxs-lookup"><span data-stu-id="e47e6-105">ID3DX11EffectSamplerVariable interface</span></span>

<span data-ttu-id="e47e6-106">Uma interface de amostra acessa o estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="e47e6-106">A sampler interface accesses sampler state.</span></span>

## <a name="members"></a><span data-ttu-id="e47e6-107">Membros</span><span class="sxs-lookup"><span data-stu-id="e47e6-107">Members</span></span>

<span data-ttu-id="e47e6-108">A interface **ID3DX11EffectSamplerVariable** herda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="e47e6-108">The **ID3DX11EffectSamplerVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="e47e6-109">**ID3DX11EffectSamplerVariable** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e47e6-109">**ID3DX11EffectSamplerVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="e47e6-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="e47e6-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e47e6-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="e47e6-111">Methods</span></span>

<span data-ttu-id="e47e6-112">A interface **ID3DX11EffectSamplerVariable** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e47e6-112">The **ID3DX11EffectSamplerVariable** interface has these methods.</span></span>



| <span data-ttu-id="e47e6-113">Método</span><span class="sxs-lookup"><span data-stu-id="e47e6-113">Method</span></span>                                                                  | <span data-ttu-id="e47e6-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="e47e6-114">Description</span></span>                                                         |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="e47e6-115">**GetBackingStore**</span><span class="sxs-lookup"><span data-stu-id="e47e6-115">**GetBackingStore**</span></span>](id3dx11effectsamplervariable-getbackingstore.md) | <span data-ttu-id="e47e6-116">Obtenha um ponteiro para uma variável que contém o estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="e47e6-116">Get a pointer to a variable that contains sampler state.</span></span><br/> |
| [<span data-ttu-id="e47e6-117">**Getamostrar**</span><span class="sxs-lookup"><span data-stu-id="e47e6-117">**GetSampler**</span></span>](id3dx11effectsamplervariable-getsampler.md)           | <span data-ttu-id="e47e6-118">Obtenha um ponteiro para uma interface de amostra.</span><span class="sxs-lookup"><span data-stu-id="e47e6-118">Get a pointer to a sampler interface.</span></span><br/>                    |
| [<span data-ttu-id="e47e6-119">**Setamostrar**</span><span class="sxs-lookup"><span data-stu-id="e47e6-119">**SetSampler**</span></span>](id3dx11effectsamplervariable-setsampler.md)           | <span data-ttu-id="e47e6-120">Defina o estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="e47e6-120">Set sampler state.</span></span><br/>                                       |
| [<span data-ttu-id="e47e6-121">**UndoSetSampler**</span><span class="sxs-lookup"><span data-stu-id="e47e6-121">**UndoSetSampler**</span></span>](id3dx11effectsamplervariable-undosetsampler.md)   | <span data-ttu-id="e47e6-122">Reverter um estado de amostra definido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e47e6-122">Revert a previously set sampler state.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="e47e6-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="e47e6-123">Remarks</span></span>

<span data-ttu-id="e47e6-124">Uma interface [**ID3DX11EffectVariable**](id3dx11effectvariable.md) é criada quando um efeito é lido na memória.</span><span class="sxs-lookup"><span data-stu-id="e47e6-124">An [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface is created when an effect is read into memory.</span></span>

<span data-ttu-id="e47e6-125">As variáveis de efeito são salvas na memória no repositório de backup; Quando uma técnica é aplicada, os valores no repositório de backup são copiados para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e47e6-125">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="e47e6-126">Você pode usar qualquer um desses métodos para retornar o estado.</span><span class="sxs-lookup"><span data-stu-id="e47e6-126">You can use either of these methods to return state.</span></span>

> [!Note]  
> <span data-ttu-id="e47e6-127">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="e47e6-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e47e6-128">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="e47e6-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e47e6-129">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e47e6-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e47e6-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e47e6-130">Requirements</span></span>



| <span data-ttu-id="e47e6-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e47e6-131">Requirement</span></span> | <span data-ttu-id="e47e6-132">Valor</span><span class="sxs-lookup"><span data-stu-id="e47e6-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e47e6-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e47e6-133">Header</span></span><br/>  | <dl> <span data-ttu-id="e47e6-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e47e6-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e47e6-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e47e6-135">Library</span></span><br/> | <dl> <span data-ttu-id="e47e6-136"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="e47e6-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e47e6-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="e47e6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e47e6-138">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="e47e6-138">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="e47e6-139">Efeitos 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="e47e6-139">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="e47e6-140">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="e47e6-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





