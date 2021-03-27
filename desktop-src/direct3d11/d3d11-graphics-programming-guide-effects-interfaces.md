---
title: Interfaces do sistema de efeito (Direct3D 11)
description: O sistema de efeitos define várias interfaces para o gerenciamento do estado de efeito.
ms.assetid: 5cba6055-d153-4837-9a08-96efbde5f48f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af76a54be06e52e320743ca945abb31d1d50d213
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635250"
---
# <a name="effect-system-interfaces-direct3d-11"></a><span data-ttu-id="81f59-103">Interfaces do sistema de efeito (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="81f59-103">Effect System Interfaces (Direct3D 11)</span></span>

<span data-ttu-id="81f59-104">O sistema de efeitos define várias interfaces para o gerenciamento do estado de efeito.</span><span class="sxs-lookup"><span data-stu-id="81f59-104">The effect system defines several interfaces for managing effect state.</span></span> <span data-ttu-id="81f59-105">Há dois tipos de interfaces: aqueles usados pelo tempo de execução para renderizar uma interface de efeito e reflexão para obter e definir variáveis de efeito.</span><span class="sxs-lookup"><span data-stu-id="81f59-105">There are two types of interfaces: those used by the runtime to render an effect and reflection interfaces for getting and setting effect variables.</span></span>

-   [<span data-ttu-id="81f59-106">Interfaces de tempo de execução de efeito</span><span class="sxs-lookup"><span data-stu-id="81f59-106">Effect Runtime Interfaces</span></span>](#effect-runtime-interfaces)
-   [<span data-ttu-id="81f59-107">Interfaces de reflexão de efeito</span><span class="sxs-lookup"><span data-stu-id="81f59-107">Effect Reflection Interfaces</span></span>](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a><span data-ttu-id="81f59-108">Interfaces de tempo de execução de efeito</span><span class="sxs-lookup"><span data-stu-id="81f59-108">Effect Runtime Interfaces</span></span>

<span data-ttu-id="81f59-109">Use interfaces de tempo de execução para renderizar um efeito.</span><span class="sxs-lookup"><span data-stu-id="81f59-109">Use runtime interfaces to render an effect.</span></span>



| <span data-ttu-id="81f59-110">Interfaces de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="81f59-110">Runtime Interfaces</span></span>                                       | <span data-ttu-id="81f59-111">Description</span><span class="sxs-lookup"><span data-stu-id="81f59-111">Description</span></span>                                                    |
|----------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="81f59-112">**ID3DX11Effect**</span><span class="sxs-lookup"><span data-stu-id="81f59-112">**ID3DX11Effect**</span></span>](id3dx11effect.md)                   | <span data-ttu-id="81f59-113">Coleção de um ou mais grupos e técnicas para renderização.</span><span class="sxs-lookup"><span data-stu-id="81f59-113">Collection of one or more groups and techniques for rendering.</span></span> |
| [<span data-ttu-id="81f59-114">**ID3DX11EffectPass**</span><span class="sxs-lookup"><span data-stu-id="81f59-114">**ID3DX11EffectPass**</span></span>](id3dx11effectpass.md)           | <span data-ttu-id="81f59-115">Uma coleção de atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="81f59-115">A collection of state assignments.</span></span>                             |
| [<span data-ttu-id="81f59-116">**ID3DX11EffectTechnique**</span><span class="sxs-lookup"><span data-stu-id="81f59-116">**ID3DX11EffectTechnique**</span></span>](id3dx11effecttechnique.md) | <span data-ttu-id="81f59-117">Uma coleção de um ou mais passos.</span><span class="sxs-lookup"><span data-stu-id="81f59-117">A collection of one or more passes.</span></span>                            |
| [<span data-ttu-id="81f59-118">**ID3DX11EffectGroup**</span><span class="sxs-lookup"><span data-stu-id="81f59-118">**ID3DX11EffectGroup**</span></span>](id3dx11effectgroup.md)         | <span data-ttu-id="81f59-119">Uma coleção de uma ou mais técnicas.</span><span class="sxs-lookup"><span data-stu-id="81f59-119">A collection of one or more techniques.</span></span>                        |



 

## <a name="effect-reflection-interfaces"></a><span data-ttu-id="81f59-120">Interfaces de reflexão de efeito</span><span class="sxs-lookup"><span data-stu-id="81f59-120">Effect Reflection Interfaces</span></span>

<span data-ttu-id="81f59-121">A reflexão é implementada no sistema de efeitos para dar suporte ao estado de efeito de leitura (e gravação).</span><span class="sxs-lookup"><span data-stu-id="81f59-121">Reflection is implemented in the effect system to support reading (and writing) effect state.</span></span> <span data-ttu-id="81f59-122">Há várias maneiras de acessar variáveis de efeito.</span><span class="sxs-lookup"><span data-stu-id="81f59-122">There are multiple ways to access effect variables.</span></span>

### <a name="setting-groups-of-effect-state"></a><span data-ttu-id="81f59-123">Definindo grupos de estado de efeito</span><span class="sxs-lookup"><span data-stu-id="81f59-123">Setting Groups of Effect State</span></span>

<span data-ttu-id="81f59-124">Use essas interfaces para obter e definir um grupo de estado.</span><span class="sxs-lookup"><span data-stu-id="81f59-124">Use these interfaces to get and set a group of state.</span></span>



| <span data-ttu-id="81f59-125">Interfaces de reflexão</span><span class="sxs-lookup"><span data-stu-id="81f59-125">Reflection Interfaces</span></span>                                                          | <span data-ttu-id="81f59-126">Description</span><span class="sxs-lookup"><span data-stu-id="81f59-126">Description</span></span>                      |
|--------------------------------------------------------------------------------|----------------------------------|
| [<span data-ttu-id="81f59-127">**ID3DX11EffectBlendVariable**</span><span class="sxs-lookup"><span data-stu-id="81f59-127">**ID3DX11EffectBlendVariable**</span></span>](id3dx11effectblendvariable.md)               | <span data-ttu-id="81f59-128">Obter e definir o estado de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="81f59-128">Get and set blend state.</span></span>         |
| [<span data-ttu-id="81f59-129">**ID3DX11EffectDepthStencilVariable**</span><span class="sxs-lookup"><span data-stu-id="81f59-129">**ID3DX11EffectDepthStencilVariable**</span></span>](id3dx11effectdepthstencilvariable.md) | <span data-ttu-id="81f59-130">Obter e definir o estado de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="81f59-130">Get and set depth-stencil state.</span></span> |
| [<span data-ttu-id="81f59-131">**ID3DX11EffectRasterizerVariable**</span><span class="sxs-lookup"><span data-stu-id="81f59-131">**ID3DX11EffectRasterizerVariable**</span></span>](id3dx11effectrasterizervariable.md)     | <span data-ttu-id="81f59-132">Obter e definir o estado do rasterizador.</span><span class="sxs-lookup"><span data-stu-id="81f59-132">Get and set rasterizer state.</span></span>    |
| [<span data-ttu-id="81f59-133">**ID3DX11EffectSamplerVariable**</span><span class="sxs-lookup"><span data-stu-id="81f59-133">**ID3DX11EffectSamplerVariable**</span></span>](id3dx11effectsamplervariable.md)           | <span data-ttu-id="81f59-134">Obter e definir o estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="81f59-134">Get and set sampler state.</span></span>       |



 

### <a name="setting-effect-resources"></a><span data-ttu-id="81f59-135">Definindo recursos de efeito</span><span class="sxs-lookup"><span data-stu-id="81f59-135">Setting Effect Resources</span></span>

<span data-ttu-id="81f59-136">Use essas interfaces para obter e definir recursos.</span><span class="sxs-lookup"><span data-stu-id="81f59-136">Use these interfaces to get and set resources.</span></span>



| <span data-ttu-id="81f59-137">Interfaces de reflexão</span><span class="sxs-lookup"><span data-stu-id="81f59-137">Reflection Interfaces</span></span>                                                                        | <span data-ttu-id="81f59-138">Description</span><span class="sxs-lookup"><span data-stu-id="81f59-138">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="81f59-139">**ID3DX11EffectConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="81f59-139">**ID3DX11EffectConstantBuffer**</span></span>](id3dx11effectconstantbuffer.md)                           | <span data-ttu-id="81f59-140">Acessar dados em um buffer de textura ou buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="81f59-140">Access data in a texture buffer or constant buffer.</span></span> |
| [<span data-ttu-id="81f59-141">**ID3DX11EffectDepthStencilViewVariable**</span><span class="sxs-lookup"><span data-stu-id="81f59-141">**ID3DX11EffectDepthStencilViewVariable**</span></span>](id3dx11effectdepthstencilviewvariable.md)       | <span data-ttu-id="81f59-142">Acesse dados em um recurso de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="81f59-142">Access data in a depth-stencil resource.</span></span>            |
| [<span data-ttu-id="81f59-143">**ID3DX11EffectRenderTargetViewVariable**</span><span class="sxs-lookup"><span data-stu-id="81f59-143">**ID3DX11EffectRenderTargetViewVariable**</span></span>](id3dx11effectrendertargetviewvariable.md)       | <span data-ttu-id="81f59-144">Acessar dados em um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="81f59-144">Access data in a render target.</span></span>                     |
| [<span data-ttu-id="81f59-145">**ID3DX11EffectShaderResourceVariable**</span><span class="sxs-lookup"><span data-stu-id="81f59-145">**ID3DX11EffectShaderResourceVariable**</span></span>](id3dx11effectshaderresourcevariable.md)           | <span data-ttu-id="81f59-146">Acessar dados em um recurso de sombreador.</span><span class="sxs-lookup"><span data-stu-id="81f59-146">Access data in a shader resource.</span></span>                   |
| [<span data-ttu-id="81f59-147">**ID3DX11EffectUnorderedAccessViewVariable**</span><span class="sxs-lookup"><span data-stu-id="81f59-147">**ID3DX11EffectUnorderedAccessViewVariable**</span></span>](id3dx11effectunorderedaccessviewvariable.md) | <span data-ttu-id="81f59-148">Acesse dados em uma exibição de acesso não ordenada.</span><span class="sxs-lookup"><span data-stu-id="81f59-148">Access data in an unordered access view.</span></span>            |



 

### <a name="setting-other-effect-variables"></a><span data-ttu-id="81f59-149">Definindo outras variáveis de efeito</span><span class="sxs-lookup"><span data-stu-id="81f59-149">Setting Other Effect Variables</span></span>

<span data-ttu-id="81f59-150">Use essas interfaces para obter e definir o estado pelo tipo de variável.</span><span class="sxs-lookup"><span data-stu-id="81f59-150">Use these interfaces to get and set state by the variable type.</span></span>



| <span data-ttu-id="81f59-151">Interfaces de reflexão</span><span class="sxs-lookup"><span data-stu-id="81f59-151">Reflection Interfaces</span></span>                                                            | <span data-ttu-id="81f59-152">Description</span><span class="sxs-lookup"><span data-stu-id="81f59-152">Description</span></span>               |
|----------------------------------------------------------------------------------|---------------------------|
| [<span data-ttu-id="81f59-153">**ID3DX11EffectClassInstanceVariable**</span><span class="sxs-lookup"><span data-stu-id="81f59-153">**ID3DX11EffectClassInstanceVariable**</span></span>](id3dx11effectclassinstancevariable.md) | <span data-ttu-id="81f59-154">Obter uma instância de classe.</span><span class="sxs-lookup"><span data-stu-id="81f59-154">Get a class instance.</span></span>     |
| [<span data-ttu-id="81f59-155">**ID3DX11EffectInterfaceVariable**</span><span class="sxs-lookup"><span data-stu-id="81f59-155">**ID3DX11EffectInterfaceVariable**</span></span>](id3dx11effectinterfacevariable.md)         | <span data-ttu-id="81f59-156">Obter e definir uma interface.</span><span class="sxs-lookup"><span data-stu-id="81f59-156">Get and set an interface.</span></span> |
| [<span data-ttu-id="81f59-157">**ID3DX11EffectMatrixVariable**</span><span class="sxs-lookup"><span data-stu-id="81f59-157">**ID3DX11EffectMatrixVariable**</span></span>](id3dx11effectmatrixvariable.md)               | <span data-ttu-id="81f59-158">Obter e definir uma matriz.</span><span class="sxs-lookup"><span data-stu-id="81f59-158">Get and set a matrix.</span></span>     |
| [<span data-ttu-id="81f59-159">**ID3DX11EffectScalarVariable**</span><span class="sxs-lookup"><span data-stu-id="81f59-159">**ID3DX11EffectScalarVariable**</span></span>](id3dx11effectscalarvariable.md)               | <span data-ttu-id="81f59-160">Obter e definir um escalar.</span><span class="sxs-lookup"><span data-stu-id="81f59-160">Get and set a scalar.</span></span>     |
| [<span data-ttu-id="81f59-161">**ID3DX11EffectShaderVariable**</span><span class="sxs-lookup"><span data-stu-id="81f59-161">**ID3DX11EffectShaderVariable**</span></span>](id3dx11effectshadervariable.md)               | <span data-ttu-id="81f59-162">Obter uma variável de sombreador.</span><span class="sxs-lookup"><span data-stu-id="81f59-162">Get a shader variable.</span></span>    |
| [<span data-ttu-id="81f59-163">**ID3DX11EffectStringVariable**</span><span class="sxs-lookup"><span data-stu-id="81f59-163">**ID3DX11EffectStringVariable**</span></span>](id3dx11effectstringvariable.md)               | <span data-ttu-id="81f59-164">Obter e definir uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="81f59-164">Get and set a string.</span></span>     |
| [<span data-ttu-id="81f59-165">**ID3DX11EffectType**</span><span class="sxs-lookup"><span data-stu-id="81f59-165">**ID3DX11EffectType**</span></span>](id3dx11effecttype.md)                                   | <span data-ttu-id="81f59-166">Obter um tipo de variável.</span><span class="sxs-lookup"><span data-stu-id="81f59-166">Get a variable type.</span></span>      |
| [<span data-ttu-id="81f59-167">**ID3DX11EffectVectorVariable**</span><span class="sxs-lookup"><span data-stu-id="81f59-167">**ID3DX11EffectVectorVariable**</span></span>](id3dx11effectvectorvariable.md)               | <span data-ttu-id="81f59-168">Obter e definir um vetor.</span><span class="sxs-lookup"><span data-stu-id="81f59-168">Get and set a vector.</span></span>     |



 

<span data-ttu-id="81f59-169">Todas as interfaces de reflexão derivam de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="81f59-169">All reflection interfaces derive from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="81f59-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="81f59-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81f59-171">Efeitos (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="81f59-171">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[<span data-ttu-id="81f59-172">Guia de programação para Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="81f59-172">Programming Guide for Direct3D 11</span></span>](dx-graphics-overviews.md)
</dt> </dl>

 

 




