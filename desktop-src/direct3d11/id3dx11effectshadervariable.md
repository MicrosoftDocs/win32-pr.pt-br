---
title: Interface ID3DX11EffectShaderVariable (D3dx11effect. h)
description: Uma interface de sombreador-variável acessa uma variável de sombreador.
ms.assetid: e547a5e9-7b60-4a85-806d-272be55d12e7
keywords:
- Interface ID3DX11EffectShaderVariable Direct3D 11
- Interface ID3DX11EffectShaderVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcbb011591f715b4bac57dfa34f640ea90278f6b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989312"
---
# <a name="id3dx11effectshadervariable-interface"></a><span data-ttu-id="589d7-105">Interface ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="589d7-105">ID3DX11EffectShaderVariable interface</span></span>

<span data-ttu-id="589d7-106">Uma interface de sombreador-variável acessa uma variável de sombreador.</span><span class="sxs-lookup"><span data-stu-id="589d7-106">A shader-variable interface accesses a shader variable.</span></span>

## <a name="members"></a><span data-ttu-id="589d7-107">Membros</span><span class="sxs-lookup"><span data-stu-id="589d7-107">Members</span></span>

<span data-ttu-id="589d7-108">A interface **ID3DX11EffectShaderVariable** herda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="589d7-108">The **ID3DX11EffectShaderVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="589d7-109">**ID3DX11EffectShaderVariable** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="589d7-109">**ID3DX11EffectShaderVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="589d7-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="589d7-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="589d7-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="589d7-111">Methods</span></span>

<span data-ttu-id="589d7-112">A interface **ID3DX11EffectShaderVariable** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="589d7-112">The **ID3DX11EffectShaderVariable** interface has these methods.</span></span>



| <span data-ttu-id="589d7-113">Método</span><span class="sxs-lookup"><span data-stu-id="589d7-113">Method</span></span>                                                                                                           | <span data-ttu-id="589d7-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="589d7-114">Description</span></span>                                            |
|:-----------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------|
| [<span data-ttu-id="589d7-115">**GetComputeShader**</span><span class="sxs-lookup"><span data-stu-id="589d7-115">**GetComputeShader**</span></span>](id3dx11effectshadervariable-getcomputeshader.md)                                         | <span data-ttu-id="589d7-116">Obtenha um sombreador de computação.</span><span class="sxs-lookup"><span data-stu-id="589d7-116">Get a compute shader.</span></span><br/>                       |
| [<span data-ttu-id="589d7-117">**GetDomainShader**</span><span class="sxs-lookup"><span data-stu-id="589d7-117">**GetDomainShader**</span></span>](id3dx11effectshadervariable-getdomainshader.md)                                           | <span data-ttu-id="589d7-118">Obtenha um sombreador de domínio.</span><span class="sxs-lookup"><span data-stu-id="589d7-118">Get a domain shader.</span></span><br/>                        |
| [<span data-ttu-id="589d7-119">**GetGeometryShader**</span><span class="sxs-lookup"><span data-stu-id="589d7-119">**GetGeometryShader**</span></span>](id3dx11effectshadervariable-getgeometryshader.md)                                       | <span data-ttu-id="589d7-120">Obter um sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="589d7-120">Get a geometry shader.</span></span><br/>                      |
| [<span data-ttu-id="589d7-121">**GetHullShader**</span><span class="sxs-lookup"><span data-stu-id="589d7-121">**GetHullShader**</span></span>](id3dx11effectshadervariable-gethullshader.md)                                               | <span data-ttu-id="589d7-122">Obtenha um sombreador envoltória.</span><span class="sxs-lookup"><span data-stu-id="589d7-122">Get a hull shader.</span></span><br/>                          |
| [<span data-ttu-id="589d7-123">**GetInputSignatureElementDesc**</span><span class="sxs-lookup"><span data-stu-id="589d7-123">**GetInputSignatureElementDesc**</span></span>](id3dx11effectshadervariable-getinputsignatureelementdesc.md)                 | <span data-ttu-id="589d7-124">Obtenha uma descrição de assinatura de entrada.</span><span class="sxs-lookup"><span data-stu-id="589d7-124">Get an input-signature description.</span></span><br/>         |
| [<span data-ttu-id="589d7-125">**GetOutputSignatureElementDesc**</span><span class="sxs-lookup"><span data-stu-id="589d7-125">**GetOutputSignatureElementDesc**</span></span>](id3dx11effectshadervariable-getoutputsignatureelementdesc.md)               | <span data-ttu-id="589d7-126">Obtenha uma descrição de assinatura de saída.</span><span class="sxs-lookup"><span data-stu-id="589d7-126">Get an output-signature description.</span></span><br/>        |
| [<span data-ttu-id="589d7-127">**GetPatchConstantSignatureElementDesc**</span><span class="sxs-lookup"><span data-stu-id="589d7-127">**GetPatchConstantSignatureElementDesc**</span></span>](id3dx11effectshadervariable-getpatchconstantsignatureelementdesc.md) | <span data-ttu-id="589d7-128">Obtenha uma descrição da assinatura constante de patch.</span><span class="sxs-lookup"><span data-stu-id="589d7-128">Get a patch constant signature description.</span></span><br/> |
| [<span data-ttu-id="589d7-129">**GetPixelShader**</span><span class="sxs-lookup"><span data-stu-id="589d7-129">**GetPixelShader**</span></span>](id3dx11effectshadervariable-getpixelshader.md)                                             | <span data-ttu-id="589d7-130">Obtenha um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="589d7-130">Get a pixel shader.</span></span><br/>                         |
| [<span data-ttu-id="589d7-131">**GetShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="589d7-131">**GetShaderDesc**</span></span>](id3dx11effectshadervariable-getshaderdesc.md)                                               | <span data-ttu-id="589d7-132">Obter uma descrição do sombreador.</span><span class="sxs-lookup"><span data-stu-id="589d7-132">Get a shader description.</span></span><br/>                   |
| [<span data-ttu-id="589d7-133">**GetVertexShader**</span><span class="sxs-lookup"><span data-stu-id="589d7-133">**GetVertexShader**</span></span>](id3dx11effectshadervariable-getvertexshader.md)                                           | <span data-ttu-id="589d7-134">Obter um sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="589d7-134">Get a vertex shader.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="589d7-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="589d7-135">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="589d7-136">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="589d7-136">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="589d7-137">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="589d7-137">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="589d7-138">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="589d7-138">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="589d7-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="589d7-139">Requirements</span></span>



| <span data-ttu-id="589d7-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="589d7-140">Requirement</span></span> | <span data-ttu-id="589d7-141">Valor</span><span class="sxs-lookup"><span data-stu-id="589d7-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="589d7-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="589d7-142">Header</span></span><br/>  | <dl> <span data-ttu-id="589d7-143"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="589d7-143"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="589d7-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="589d7-144">Library</span></span><br/> | <dl> <span data-ttu-id="589d7-145"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="589d7-145"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="589d7-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="589d7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="589d7-147">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="589d7-147">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="589d7-148">Efeitos 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="589d7-148">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="589d7-149">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="589d7-149">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





