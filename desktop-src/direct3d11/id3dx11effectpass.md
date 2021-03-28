---
title: Interface ID3DX11EffectPass (D3dx11effect. h)
description: Uma interface ID3DX11EffectPass encapsula as atribuições de estado dentro de uma técnica. O tempo de vida de um objeto ID3DX11EffectPass é igual ao tempo de vida de seu objeto ID3DX11Effect pai.
ms.assetid: 4d86c362-b0f8-4396-86de-c7c89710f46d
keywords:
- Interface ID3DX11EffectPass Direct3D 11
- Interface ID3DX11EffectPass Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectPass
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a26732543d1033cfc439755df6ac397d2a28ec1b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173136"
---
# <a name="id3dx11effectpass-interface"></a><span data-ttu-id="6ba4e-105">Interface ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="6ba4e-105">ID3DX11EffectPass interface</span></span>

<span data-ttu-id="6ba4e-106">Uma interface **ID3DX11EffectPass** encapsula as atribuições de estado dentro de uma técnica.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-106">An **ID3DX11EffectPass** interface encapsulates state assignments within a technique.</span></span>

<span data-ttu-id="6ba4e-107">O tempo de vida de um objeto **ID3DX11EffectPass** é igual ao tempo de vida de seu objeto [**ID3DX11Effect**](id3dx11effect.md) pai.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-107">The lifetime of an **ID3DX11EffectPass** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="6ba4e-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="6ba4e-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6ba4e-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="6ba4e-109">Methods</span></span>

<span data-ttu-id="6ba4e-110">A interface **ID3DX11EffectPass** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-110">The **ID3DX11EffectPass** interface has these methods.</span></span>



| <span data-ttu-id="6ba4e-111">Método</span><span class="sxs-lookup"><span data-stu-id="6ba4e-111">Method</span></span>                                                                   | <span data-ttu-id="6ba4e-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="6ba4e-112">Description</span></span>                                                       |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="6ba4e-113">**Aplicar**</span><span class="sxs-lookup"><span data-stu-id="6ba4e-113">**Apply**</span></span>](id3dx11effectpass-apply.md)                                 | <span data-ttu-id="6ba4e-114">Defina o estado contido em uma passagem para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-114">Set the state contained in a pass to the device.</span></span><br/>       |
| [<span data-ttu-id="6ba4e-115">**ComputeStateBlockMask**</span><span class="sxs-lookup"><span data-stu-id="6ba4e-115">**ComputeStateBlockMask**</span></span>](id3dx11effectpass-computestateblockmask.md) | <span data-ttu-id="6ba4e-116">Gere uma máscara para permitir/impedir alterações de estado.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-116">Generate a mask for allowing/preventing state changes.</span></span><br/> |
| [<span data-ttu-id="6ba4e-117">**GetAnnotationByIndex**</span><span class="sxs-lookup"><span data-stu-id="6ba4e-117">**GetAnnotationByIndex**</span></span>](id3dx11effectpass-getannotationbyindex.md)   | <span data-ttu-id="6ba4e-118">Obter uma anotação por índice.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-118">Get an annotation by index.</span></span><br/>                            |
| [<span data-ttu-id="6ba4e-119">**GetAnnotationByName**</span><span class="sxs-lookup"><span data-stu-id="6ba4e-119">**GetAnnotationByName**</span></span>](id3dx11effectpass-getannotationbyname.md)     | <span data-ttu-id="6ba4e-120">Obter uma anotação por nome.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-120">Get an annotation by name.</span></span><br/>                             |
| [<span data-ttu-id="6ba4e-121">**GetComputeShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="6ba4e-121">**GetComputeShaderDesc**</span></span>](id3dx11effectpass-getcomputeshaderdesc.md)   | <span data-ttu-id="6ba4e-122">Obtenha uma descrição do sombreador de computação.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-122">Get a compute-shader description.</span></span><br/>                      |
| [<span data-ttu-id="6ba4e-123">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="6ba4e-123">**GetDesc**</span></span>](id3dx11effectpass-getdesc.md)                             | <span data-ttu-id="6ba4e-124">Obtenha uma descrição de Pass.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-124">Get a pass description.</span></span><br/>                                |
| [<span data-ttu-id="6ba4e-125">**GetDomainShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="6ba4e-125">**GetDomainShaderDesc**</span></span>](id3dx11effectpass-getdomainshaderdesc.md)     | <span data-ttu-id="6ba4e-126">Obtenha uma descrição do sombreador de domínio.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-126">Get a domain-shader description.</span></span><br/>                       |
| [<span data-ttu-id="6ba4e-127">**GetGeometryShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="6ba4e-127">**GetGeometryShaderDesc**</span></span>](id3dx11effectpass-getgeometryshaderdesc.md) | <span data-ttu-id="6ba4e-128">Obtenha uma descrição do sombreador Geometry.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-128">Get a geometry-shader description.</span></span><br/>                     |
| [<span data-ttu-id="6ba4e-129">**GetHullShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="6ba4e-129">**GetHullShaderDesc**</span></span>](id3dx11effectpass-gethullshaderdesc.md)         | <span data-ttu-id="6ba4e-130">Obtenha a descrição de envoltória-Shader.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-130">Get hull-shader description.</span></span><br/>                           |
| [<span data-ttu-id="6ba4e-131">**GetPixelShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="6ba4e-131">**GetPixelShaderDesc**</span></span>](id3dx11effectpass-getpixelshaderdesc.md)       | <span data-ttu-id="6ba4e-132">Obtenha uma descrição do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-132">Get a pixel-shader description.</span></span><br/>                        |
| [<span data-ttu-id="6ba4e-133">**GetVertexShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="6ba4e-133">**GetVertexShaderDesc**</span></span>](id3dx11effectpass-getvertexshaderdesc.md)     | <span data-ttu-id="6ba4e-134">Obter uma descrição de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-134">Get a vertex-shader description.</span></span><br/>                       |
| [<span data-ttu-id="6ba4e-135">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="6ba4e-135">**IsValid**</span></span>](id3dx11effectpass-isvalid.md)                             | <span data-ttu-id="6ba4e-136">Teste uma passagem para ver se ela contém uma sintaxe válida.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-136">Test a pass to see if it contains valid syntax.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="6ba4e-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ba4e-137">Remarks</span></span>

<span data-ttu-id="6ba4e-138">Uma passagem é um bloco de código que define os objetos de estado de renderização e os sombreadores.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-138">A pass is a block of code that sets render-state objects and shaders.</span></span> <span data-ttu-id="6ba4e-139">Uma passagem é declarada dentro de uma técnica.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-139">A pass is declared within a technique.</span></span>

<span data-ttu-id="6ba4e-140">Para obter uma interface de passagem de efeito, chame um método como [**ID3DX11EffectTechnique:: GetPassByName**](id3dx11effecttechnique-getpassbyname.md).</span><span class="sxs-lookup"><span data-stu-id="6ba4e-140">To get an effect-pass interface, call a method like [**ID3DX11EffectTechnique::GetPassByName**](id3dx11effecttechnique-getpassbyname.md).</span></span>

> [!Note]  
> <span data-ttu-id="6ba4e-141">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-141">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6ba4e-142">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-142">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6ba4e-143">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="6ba4e-143">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6ba4e-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ba4e-144">Requirements</span></span>



| <span data-ttu-id="6ba4e-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ba4e-145">Requirement</span></span> | <span data-ttu-id="6ba4e-146">Valor</span><span class="sxs-lookup"><span data-stu-id="6ba4e-146">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ba4e-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ba4e-147">Header</span></span><br/>  | <dl> <span data-ttu-id="6ba4e-148"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ba4e-148"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6ba4e-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6ba4e-149">Library</span></span><br/> | <dl> <span data-ttu-id="6ba4e-150"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="6ba4e-150"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ba4e-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ba4e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ba4e-152">Efeitos 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="6ba4e-152">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="6ba4e-153">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="6ba4e-153">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





