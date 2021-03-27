---
title: Interface ID3DX11EffectVariable (D3dx11effect. h)
description: A interface ID3DX11EffectVariable é a classe base para todas as variáveis de efeito. O tempo de vida de um objeto ID3DX11EffectVariable é igual ao tempo de vida de seu objeto ID3DX11Effect pai.
ms.assetid: 07f1b7d7-c266-49ae-b79a-7a645521df89
keywords:
- Interface ID3DX11EffectVariable Direct3D 11
- Interface ID3DX11EffectVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1df38a12c54776072bb922ffc4cd5bcd0d79776
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664055"
---
# <a name="id3dx11effectvariable-interface"></a><span data-ttu-id="8a68f-105">Interface ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="8a68f-105">ID3DX11EffectVariable interface</span></span>

<span data-ttu-id="8a68f-106">A interface **ID3DX11EffectVariable** é a classe base para todas as variáveis de efeito.</span><span class="sxs-lookup"><span data-stu-id="8a68f-106">The **ID3DX11EffectVariable** interface is the base class for all effect variables.</span></span>

<span data-ttu-id="8a68f-107">O tempo de vida de um objeto **ID3DX11EffectVariable** é igual ao tempo de vida de seu objeto [**ID3DX11Effect**](id3dx11effect.md) pai.</span><span class="sxs-lookup"><span data-stu-id="8a68f-107">The lifetime of an **ID3DX11EffectVariable** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="8a68f-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="8a68f-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8a68f-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="8a68f-109">Methods</span></span>

<span data-ttu-id="8a68f-110">A interface **ID3DX11EffectVariable** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="8a68f-110">The **ID3DX11EffectVariable** interface has these methods.</span></span>



| <span data-ttu-id="8a68f-111">Método</span><span class="sxs-lookup"><span data-stu-id="8a68f-111">Method</span></span>                                                                           | <span data-ttu-id="8a68f-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a68f-112">Description</span></span>                                            |
|:---------------------------------------------------------------------------------|:-------------------------------------------------------|
| [<span data-ttu-id="8a68f-113">**Asblend**</span><span class="sxs-lookup"><span data-stu-id="8a68f-113">**AsBlend**</span></span>](id3dx11effectvariable-asblend.md)                                 | <span data-ttu-id="8a68f-114">Obter uma variável de combinação de efeito.</span><span class="sxs-lookup"><span data-stu-id="8a68f-114">Get a effect-blend variable.</span></span><br/>                |
| [<span data-ttu-id="8a68f-115">**AsClassInstance**</span><span class="sxs-lookup"><span data-stu-id="8a68f-115">**AsClassInstance**</span></span>](id3dx11effectvariable-asclassinstance.md)                 | <span data-ttu-id="8a68f-116">Obtenha uma variável de instância de classe.</span><span class="sxs-lookup"><span data-stu-id="8a68f-116">Get a class-instance variable.</span></span><br/>              |
| [<span data-ttu-id="8a68f-117">**AsConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="8a68f-117">**AsConstantBuffer**</span></span>](id3dx11effectvariable-asconstantbuffer.md)               | <span data-ttu-id="8a68f-118">Obter um buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="8a68f-118">Get a constant buffer.</span></span><br/>                      |
| [<span data-ttu-id="8a68f-119">**AsDepthStencil**</span><span class="sxs-lookup"><span data-stu-id="8a68f-119">**AsDepthStencil**</span></span>](id3dx11effectvariable-asdepthstencil.md)                   | <span data-ttu-id="8a68f-120">Obtenha uma variável de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="8a68f-120">Get a depth-stencil variable.</span></span><br/>               |
| [<span data-ttu-id="8a68f-121">**AsDepthStencilView**</span><span class="sxs-lookup"><span data-stu-id="8a68f-121">**AsDepthStencilView**</span></span>](id3dx11effectvariable-asdepthstencilview.md)           | <span data-ttu-id="8a68f-122">Obtenha uma variável de exibição de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="8a68f-122">Get a depth-stencil-view variable.</span></span><br/>          |
| [<span data-ttu-id="8a68f-123">**Asinterface**</span><span class="sxs-lookup"><span data-stu-id="8a68f-123">**AsInterface**</span></span>](id3dx11effectvariable-asinterface.md)                         | <span data-ttu-id="8a68f-124">Obter uma variável de interface.</span><span class="sxs-lookup"><span data-stu-id="8a68f-124">Get an interface variable.</span></span><br/>                  |
| [<span data-ttu-id="8a68f-125">**Asmatrix**</span><span class="sxs-lookup"><span data-stu-id="8a68f-125">**AsMatrix**</span></span>](id3dx11effectvariable-asmatrix.md)                               | <span data-ttu-id="8a68f-126">Obter uma variável de matriz.</span><span class="sxs-lookup"><span data-stu-id="8a68f-126">Get a matrix variable.</span></span><br/>                      |
| [<span data-ttu-id="8a68f-127">**Asrasterizador**</span><span class="sxs-lookup"><span data-stu-id="8a68f-127">**AsRasterizer**</span></span>](id3dx11effectvariable-asrasterizer.md)                       | <span data-ttu-id="8a68f-128">Obter uma variável de rasterizador.</span><span class="sxs-lookup"><span data-stu-id="8a68f-128">Get a rasterizer variable.</span></span><br/>                  |
| [<span data-ttu-id="8a68f-129">**AsRenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="8a68f-129">**AsRenderTargetView**</span></span>](id3dx11effectvariable-asrendertargetview.md)           | <span data-ttu-id="8a68f-130">Obter uma variável render-Target-View.</span><span class="sxs-lookup"><span data-stu-id="8a68f-130">Get a render-target-view variable.</span></span><br/>          |
| [<span data-ttu-id="8a68f-131">**De exemplo**</span><span class="sxs-lookup"><span data-stu-id="8a68f-131">**AsSampler**</span></span>](id3dx11effectvariable-assampler.md)                             | <span data-ttu-id="8a68f-132">Obter uma variável de amostra.</span><span class="sxs-lookup"><span data-stu-id="8a68f-132">Get a sampler variable.</span></span><br/>                     |
| [<span data-ttu-id="8a68f-133">**Asscaler**</span><span class="sxs-lookup"><span data-stu-id="8a68f-133">**AsScalar**</span></span>](id3dx11effectvariable-asscalar.md)                               | <span data-ttu-id="8a68f-134">Obter uma variável escalar.</span><span class="sxs-lookup"><span data-stu-id="8a68f-134">Get a scalar variable.</span></span><br/>                      |
| [<span data-ttu-id="8a68f-135">**Asshadr**</span><span class="sxs-lookup"><span data-stu-id="8a68f-135">**AsShader**</span></span>](id3dx11effectvariable-asshader.md)                               | <span data-ttu-id="8a68f-136">Obter uma variável de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8a68f-136">Get a shader variable.</span></span><br/>                      |
| [<span data-ttu-id="8a68f-137">**AsShaderResource**</span><span class="sxs-lookup"><span data-stu-id="8a68f-137">**AsShaderResource**</span></span>](id3dx11effectvariable-asshaderresource.md)               | <span data-ttu-id="8a68f-138">Obter uma variável de recurso de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8a68f-138">Get a shader-resource variable.</span></span><br/>             |
| [<span data-ttu-id="8a68f-139">**AsString**</span><span class="sxs-lookup"><span data-stu-id="8a68f-139">**AsString**</span></span>](id3dx11effectvariable-asstring.md)                               | <span data-ttu-id="8a68f-140">Obter uma variável de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8a68f-140">Get a string variable.</span></span><br/>                      |
| [<span data-ttu-id="8a68f-141">**AsUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="8a68f-141">**AsUnorderedAccessView**</span></span>](id3dx11effectvariable-asunorderedaccessview.md)     | <span data-ttu-id="8a68f-142">Obter uma variável de exibição de acesso não ordenado.</span><span class="sxs-lookup"><span data-stu-id="8a68f-142">Get an unordered-access-view variable.</span></span><br/>      |
| [<span data-ttu-id="8a68f-143">**Asvector**</span><span class="sxs-lookup"><span data-stu-id="8a68f-143">**AsVector**</span></span>](id3dx11effectvariable-asvector.md)                               | <span data-ttu-id="8a68f-144">Obter uma variável de vetor.</span><span class="sxs-lookup"><span data-stu-id="8a68f-144">Get a vector variable.</span></span><br/>                      |
| [<span data-ttu-id="8a68f-145">**GetAnnotationByIndex**</span><span class="sxs-lookup"><span data-stu-id="8a68f-145">**GetAnnotationByIndex**</span></span>](id3dx11effectvariable-getannotationbyindex.md)       | <span data-ttu-id="8a68f-146">Obter uma anotação por índice.</span><span class="sxs-lookup"><span data-stu-id="8a68f-146">Get an annotation by index.</span></span><br/>                 |
| [<span data-ttu-id="8a68f-147">**GetAnnotationByName**</span><span class="sxs-lookup"><span data-stu-id="8a68f-147">**GetAnnotationByName**</span></span>](id3dx11effectvariable-getannotationbyname.md)         | <span data-ttu-id="8a68f-148">Obter uma anotação por nome.</span><span class="sxs-lookup"><span data-stu-id="8a68f-148">Get an annotation by name.</span></span><br/>                  |
| [<span data-ttu-id="8a68f-149">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="8a68f-149">**GetDesc**</span></span>](id3dx11effectvariable-getdesc.md)                                 | <span data-ttu-id="8a68f-150">Obtenha uma descrição.</span><span class="sxs-lookup"><span data-stu-id="8a68f-150">Get a description.</span></span><br/>                          |
| [<span data-ttu-id="8a68f-151">**GetElement**</span><span class="sxs-lookup"><span data-stu-id="8a68f-151">**GetElement**</span></span>](id3dx11effectvariable-getelement.md)                           | <span data-ttu-id="8a68f-152">Obter um elemento de matriz.</span><span class="sxs-lookup"><span data-stu-id="8a68f-152">Get an array element.</span></span><br/>                       |
| [<span data-ttu-id="8a68f-153">**GetMemberByIndex**</span><span class="sxs-lookup"><span data-stu-id="8a68f-153">**GetMemberByIndex**</span></span>](id3dx11effectvariable-getmemberbyindex.md)               | <span data-ttu-id="8a68f-154">Obter um membro de estrutura por índice.</span><span class="sxs-lookup"><span data-stu-id="8a68f-154">Get a structure member by index.</span></span><br/>            |
| [<span data-ttu-id="8a68f-155">**GetMemberByName**</span><span class="sxs-lookup"><span data-stu-id="8a68f-155">**GetMemberByName**</span></span>](id3dx11effectvariable-getmemberbyname.md)                 | <span data-ttu-id="8a68f-156">Obter um membro da estrutura por nome.</span><span class="sxs-lookup"><span data-stu-id="8a68f-156">Get a structure member by name.</span></span><br/>             |
| [<span data-ttu-id="8a68f-157">**GetMemberBySemantic**</span><span class="sxs-lookup"><span data-stu-id="8a68f-157">**GetMemberBySemantic**</span></span>](id3dx11effectvariable-getmemberbysemantic.md)         | <span data-ttu-id="8a68f-158">Obtenha um membro de estrutura por semântica.</span><span class="sxs-lookup"><span data-stu-id="8a68f-158">Get a structure member by semantic.</span></span><br/>         |
| [<span data-ttu-id="8a68f-159">**GetParentConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="8a68f-159">**GetParentConstantBuffer**</span></span>](id3dx11effectvariable-getparentconstantbuffer.md) | <span data-ttu-id="8a68f-160">Obter um buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="8a68f-160">Get a constant buffer.</span></span><br/>                      |
| [<span data-ttu-id="8a68f-161">**GetRawValue**</span><span class="sxs-lookup"><span data-stu-id="8a68f-161">**GetRawValue**</span></span>](id3dx11effectvariable-getrawvalue.md)                         | <span data-ttu-id="8a68f-162">Obter dados.</span><span class="sxs-lookup"><span data-stu-id="8a68f-162">Get data.</span></span><br/>                                   |
| [<span data-ttu-id="8a68f-163">**GetType**</span><span class="sxs-lookup"><span data-stu-id="8a68f-163">**GetType**</span></span>](id3dx11effectvariable-gettype.md)                                 | <span data-ttu-id="8a68f-164">Obter informações de tipo.</span><span class="sxs-lookup"><span data-stu-id="8a68f-164">Get type information.</span></span><br/>                       |
| [<span data-ttu-id="8a68f-165">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="8a68f-165">**IsValid**</span></span>](id3dx11effectvariable-isvalid.md)                                 | <span data-ttu-id="8a68f-166">Compare o tipo de dados com os dados armazenados.</span><span class="sxs-lookup"><span data-stu-id="8a68f-166">Compare the data type with the data stored.</span></span><br/> |
| [<span data-ttu-id="8a68f-167">**SetRawValue**</span><span class="sxs-lookup"><span data-stu-id="8a68f-167">**SetRawValue**</span></span>](id3dx11effectvariable-setrawvalue.md)                         | <span data-ttu-id="8a68f-168">Definir dados.</span><span class="sxs-lookup"><span data-stu-id="8a68f-168">Set data.</span></span><br/>                                   |



 

## <a name="remarks"></a><span data-ttu-id="8a68f-169">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a68f-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8a68f-170">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="8a68f-170">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="8a68f-171">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="8a68f-171">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="8a68f-172">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="8a68f-172">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8a68f-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a68f-173">Requirements</span></span>



| <span data-ttu-id="8a68f-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a68f-174">Requirement</span></span> | <span data-ttu-id="8a68f-175">Valor</span><span class="sxs-lookup"><span data-stu-id="8a68f-175">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a68f-176">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8a68f-176">Header</span></span><br/>  | <dl> <span data-ttu-id="8a68f-177"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a68f-177"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="8a68f-178">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8a68f-178">Library</span></span><br/> | <dl> <span data-ttu-id="8a68f-179"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="8a68f-179"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a68f-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a68f-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a68f-181">Efeitos 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="8a68f-181">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="8a68f-182">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="8a68f-182">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





