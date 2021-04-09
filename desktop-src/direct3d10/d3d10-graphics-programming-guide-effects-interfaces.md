---
description: 'O sistema de efeitos define várias interfaces para o gerenciamento do estado de efeito. Há dois tipos de interfaces: aqueles usados pelo tempo de execução para renderizar uma interface de efeito e reflexão para obter e definir variáveis de efeito.'
ms.assetid: 068d49d2-0e14-4080-9fee-20d984f22545
title: Interfaces do sistema de efeito (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40b21d98bedaec65550343260e7c52e2df1c302
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089046"
---
# <a name="effect-system-interfaces-direct3d-10"></a><span data-ttu-id="bf6b4-104">Interfaces do sistema de efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="bf6b4-104">Effect System Interfaces (Direct3D 10)</span></span>

<span data-ttu-id="bf6b4-105">O sistema de efeitos define várias interfaces para o gerenciamento do estado de efeito.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-105">The effect system defines several interfaces for managing effect state.</span></span> <span data-ttu-id="bf6b4-106">Há dois tipos de interfaces: aqueles usados pelo tempo de execução para renderizar uma interface de efeito e reflexão para obter e definir variáveis de efeito.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-106">There are two types of interfaces: those used by the runtime to render an effect and reflection interfaces for getting and setting effect variables.</span></span>

-   [<span data-ttu-id="bf6b4-107">Interfaces de tempo de execução de efeito</span><span class="sxs-lookup"><span data-stu-id="bf6b4-107">Effect Runtime Interfaces</span></span>](#effect-runtime-interfaces)
-   [<span data-ttu-id="bf6b4-108">Interfaces de reflexão de efeito</span><span class="sxs-lookup"><span data-stu-id="bf6b4-108">Effect Reflection Interfaces</span></span>](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a><span data-ttu-id="bf6b4-109">Interfaces de tempo de execução de efeito</span><span class="sxs-lookup"><span data-stu-id="bf6b4-109">Effect Runtime Interfaces</span></span>

<span data-ttu-id="bf6b4-110">Use interfaces de tempo de execução para renderizar um efeito.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-110">Use runtime interfaces to render an effect.</span></span>



| <span data-ttu-id="bf6b4-111">Interfaces de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="bf6b4-111">Runtime Interfaces</span></span>                                               | <span data-ttu-id="bf6b4-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf6b4-112">Description</span></span>                                                          |
|------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="bf6b4-113">**Interface ID3D10Effect**</span><span class="sxs-lookup"><span data-stu-id="bf6b4-113">**ID3D10Effect Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                   | <span data-ttu-id="bf6b4-114">Coleção de uma ou mais técnicas para renderização.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-114">Collection of one or more techniques for rendering.</span></span>                  |
| <span data-ttu-id="bf6b4-115">[**Interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bf6b4-115">[**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span></span>                 | <span data-ttu-id="bf6b4-116">Uma interface para adicionar comportamentos personalizados ao ler arquivos de inclusão.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-116">An interface for adding custom behaviors when reading include files.</span></span> |
| [<span data-ttu-id="bf6b4-117">**Interface ID3D10EffectPass**</span><span class="sxs-lookup"><span data-stu-id="bf6b4-117">**ID3D10EffectPass Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)           | <span data-ttu-id="bf6b4-118">Uma coleção de atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-118">A collection of state assignments.</span></span>                                   |
| [<span data-ttu-id="bf6b4-119">**Interface ID3D10EffectPool**</span><span class="sxs-lookup"><span data-stu-id="bf6b4-119">**ID3D10EffectPool Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)           | <span data-ttu-id="bf6b4-120">Crie um local de memória para as variáveis a serem compartilhadas entre os efeitos.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-120">Create a memory location for variables to be shared between effects.</span></span> |
| [<span data-ttu-id="bf6b4-121">**Interface ID3D10EffectTechnique**</span><span class="sxs-lookup"><span data-stu-id="bf6b4-121">**ID3D10EffectTechnique Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique) | <span data-ttu-id="bf6b4-122">Uma coleção de um ou mais passos.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-122">A collection of one or more passes.</span></span>                                  |



 

## <a name="effect-reflection-interfaces"></a><span data-ttu-id="bf6b4-123">Interfaces de reflexão de efeito</span><span class="sxs-lookup"><span data-stu-id="bf6b4-123">Effect Reflection Interfaces</span></span>

<span data-ttu-id="bf6b4-124">A reflexão é implementada no sistema de efeitos para dar suporte ao estado de efeito de leitura (e gravação).</span><span class="sxs-lookup"><span data-stu-id="bf6b4-124">Reflection is implemented in the effect system to support reading (and writing) effect state.</span></span> <span data-ttu-id="bf6b4-125">Há várias maneiras de acessar variáveis de efeito.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-125">There are multiple ways to access effect variables.</span></span>

### <a name="setting-groups-of-effect-state"></a><span data-ttu-id="bf6b4-126">Definindo grupos de estado de efeito</span><span class="sxs-lookup"><span data-stu-id="bf6b4-126">Setting Groups of Effect State</span></span>

<span data-ttu-id="bf6b4-127">Use essas interfaces para obter e definir um grupo de estado.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-127">Use these interfaces to get and set a group of state.</span></span>



| <span data-ttu-id="bf6b4-128">Interfaces de reflexão</span><span class="sxs-lookup"><span data-stu-id="bf6b4-128">Reflection Interfaces</span></span>                                                                  | <span data-ttu-id="bf6b4-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf6b4-129">Description</span></span>                      |
|----------------------------------------------------------------------------------------|----------------------------------|
| [<span data-ttu-id="bf6b4-130">**Interface ID3D10EffectBlendVariable**</span><span class="sxs-lookup"><span data-stu-id="bf6b4-130">**ID3D10EffectBlendVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)               | <span data-ttu-id="bf6b4-131">Obter e definir o estado de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-131">Get and set blend state.</span></span>         |
| [<span data-ttu-id="bf6b4-132">**Interface ID3D10EffectDepthStencilVariable**</span><span class="sxs-lookup"><span data-stu-id="bf6b4-132">**ID3D10EffectDepthStencilVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable) | <span data-ttu-id="bf6b4-133">Obter e definir o estado de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-133">Get and set depth-stencil state.</span></span> |
| [<span data-ttu-id="bf6b4-134">**Interface ID3D10EffectRasterizerVariable**</span><span class="sxs-lookup"><span data-stu-id="bf6b4-134">**ID3D10EffectRasterizerVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)     | <span data-ttu-id="bf6b4-135">Obter e definir o estado do rasterizador.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-135">Get and set rasterizer state.</span></span>    |
| [<span data-ttu-id="bf6b4-136">**Interface ID3D10EffectSamplerVariable**</span><span class="sxs-lookup"><span data-stu-id="bf6b4-136">**ID3D10EffectSamplerVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)           | <span data-ttu-id="bf6b4-137">Obter e definir o estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-137">Get and set sampler state.</span></span>       |



 

### <a name="setting-effect-resources"></a><span data-ttu-id="bf6b4-138">Definindo recursos de efeito</span><span class="sxs-lookup"><span data-stu-id="bf6b4-138">Setting Effect Resources</span></span>

<span data-ttu-id="bf6b4-139">Use essas interfaces para obter e definir recursos.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-139">Use these interfaces to get and set resources.</span></span>



| <span data-ttu-id="bf6b4-140">Interfaces de reflexão</span><span class="sxs-lookup"><span data-stu-id="bf6b4-140">Reflection Interfaces</span></span>                                                                          | <span data-ttu-id="bf6b4-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf6b4-141">Description</span></span>                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="bf6b4-142">**Interface ID3D10EffectConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="bf6b4-142">**ID3D10EffectConstantBuffer Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | <span data-ttu-id="bf6b4-143">Acessar dados em um buffer de textura ou buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-143">Access data in a texture buffer or constant buffer.</span></span> |
| [<span data-ttu-id="bf6b4-144">**Interface ID3D10EffectDepthStencilViewVariable**</span><span class="sxs-lookup"><span data-stu-id="bf6b4-144">**ID3D10EffectDepthStencilViewVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | <span data-ttu-id="bf6b4-145">Acesse dados em um recurso de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-145">Access data in a depth-stencil resource.</span></span>            |
| [<span data-ttu-id="bf6b4-146">**Interface ID3D10EffectRenderTargetViewVariable**</span><span class="sxs-lookup"><span data-stu-id="bf6b4-146">**ID3D10EffectRenderTargetViewVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | <span data-ttu-id="bf6b4-147">Acessar dados em um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-147">Access data in a render target.</span></span>                     |
| [<span data-ttu-id="bf6b4-148">**Interface ID3D10EffectShaderResourceVariable**</span><span class="sxs-lookup"><span data-stu-id="bf6b4-148">**ID3D10EffectShaderResourceVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | <span data-ttu-id="bf6b4-149">Acessar dados em um recurso de sombreador.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-149">Access data in a shader resource.</span></span>                   |



 

### <a name="setting-other-effect-variables"></a><span data-ttu-id="bf6b4-150">Definindo outras variáveis de efeito</span><span class="sxs-lookup"><span data-stu-id="bf6b4-150">Setting Other Effect Variables</span></span>

<span data-ttu-id="bf6b4-151">Use essas interfaces para obter e definir o estado pelo tipo de variável.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-151">Use these interfaces to get and set state by the variable type.</span></span>



| <span data-ttu-id="bf6b4-152">Interfaces de reflexão</span><span class="sxs-lookup"><span data-stu-id="bf6b4-152">Reflection Interfaces</span></span>                                                      | <span data-ttu-id="bf6b4-153">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf6b4-153">Description</span></span>                    |
|----------------------------------------------------------------------------|--------------------------------|
| [<span data-ttu-id="bf6b4-154">**Interface ID3D10EffectMatrixVariable**</span><span class="sxs-lookup"><span data-stu-id="bf6b4-154">**ID3D10EffectMatrixVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable) | <span data-ttu-id="bf6b4-155">Obter e definir uma matriz.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-155">Get and set a matrix.</span></span>          |
| [<span data-ttu-id="bf6b4-156">**Interface ID3D10EffectScalarVariable**</span><span class="sxs-lookup"><span data-stu-id="bf6b4-156">**ID3D10EffectScalarVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable) | <span data-ttu-id="bf6b4-157">Obter e definir um escalar.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-157">Get and set a scalar.</span></span>          |
| [<span data-ttu-id="bf6b4-158">**Interface ID3D10EffectShaderVariable**</span><span class="sxs-lookup"><span data-stu-id="bf6b4-158">**ID3D10EffectShaderVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable) | <span data-ttu-id="bf6b4-159">Obter e definir uma variável de sombreador.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-159">Get and set a shader variable.</span></span> |
| [<span data-ttu-id="bf6b4-160">**Interface ID3D10EffectStringVariable**</span><span class="sxs-lookup"><span data-stu-id="bf6b4-160">**ID3D10EffectStringVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable) | <span data-ttu-id="bf6b4-161">Obter e definir uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-161">Get and set a string.</span></span>          |
| [<span data-ttu-id="bf6b4-162">**Interface ID3D10EffectType**</span><span class="sxs-lookup"><span data-stu-id="bf6b4-162">**ID3D10EffectType Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                     | <span data-ttu-id="bf6b4-163">Obter um tipo de variável.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-163">Get a variable type.</span></span>           |
| [<span data-ttu-id="bf6b4-164">**Interface ID3D10EffectVectorVariable**</span><span class="sxs-lookup"><span data-stu-id="bf6b4-164">**ID3D10EffectVectorVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable) | <span data-ttu-id="bf6b4-165">Obter e definir um vetor.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-165">Get and set a vector.</span></span>          |



 

<span data-ttu-id="bf6b4-166">Todas as interfaces de reflexão derivam da [**interface ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).</span><span class="sxs-lookup"><span data-stu-id="bf6b4-166">All reflection interfaces derive from [**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf6b4-167">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bf6b4-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf6b4-168">Effect</span><span class="sxs-lookup"><span data-stu-id="bf6b4-168">Effects</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> <dt>

[<span data-ttu-id="bf6b4-169">Guia de programação para Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="bf6b4-169">Programming Guide for Direct3D 10</span></span>](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
