---
title: Diferenças entre os efeitos 10 e os efeitos 11
description: Este tópico mostra as diferenças entre os efeitos 10 e 11.
ms.assetid: c3e5e6bc-c544-49ee-b6d9-021ce87f9b12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29af1b9e7aec72f96a62e0f62668b81a6eec8367
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641332"
---
# <a name="differences-between-effects-10-and-effects-11"></a><span data-ttu-id="22d49-103">Diferenças entre os efeitos 10 e os efeitos 11</span><span class="sxs-lookup"><span data-stu-id="22d49-103">Differences Between Effects 10 and Effects 11</span></span>

<span data-ttu-id="22d49-104">Este tópico mostra as diferenças entre os efeitos 10 e 11.</span><span class="sxs-lookup"><span data-stu-id="22d49-104">This topic shows the differences between Effects 10 and Effects 11.</span></span>

## <a name="device-contexts-threading-and-cloning"></a><span data-ttu-id="22d49-105">Contextos de dispositivo, threading e clonagem</span><span class="sxs-lookup"><span data-stu-id="22d49-105">Device Contexts, Threading, and Cloning</span></span>

<span data-ttu-id="22d49-106">A interface ID3D10Device foi dividida em duas interfaces no Direct3D 11: ID3D11Device e ID3D11DeviceContext.</span><span class="sxs-lookup"><span data-stu-id="22d49-106">The ID3D10Device interface has been split into two interfaces in Direct3D 11: ID3D11Device and ID3D11DeviceContext.</span></span> <span data-ttu-id="22d49-107">Você pode criar vários ID3D11DeviceContexts para facilitar a execução simultânea em vários threads.</span><span class="sxs-lookup"><span data-stu-id="22d49-107">You can create multiple ID3D11DeviceContexts to facilitate concurrent execution on multiple threads.</span></span> <span data-ttu-id="22d49-108">Os efeitos 11 ampliam esse conceito para a estrutura de efeitos.</span><span class="sxs-lookup"><span data-stu-id="22d49-108">Effects 11 extends this concept to the Effects framework.</span></span>

<span data-ttu-id="22d49-109">O tempo de execução dos efeitos 11 é de thread único.</span><span class="sxs-lookup"><span data-stu-id="22d49-109">The Effects 11 runtime is single-threaded.</span></span> <span data-ttu-id="22d49-110">Por esse motivo, você não deve usar uma única instância ID3DX11Effect com vários threads simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="22d49-110">For this reason, you should not use a single ID3DX11Effect instance with multiple threads concurrently.</span></span>

<span data-ttu-id="22d49-111">Para usar o tempo de execução Effects 11 em várias instâncias, você deve criar instâncias ID3DX11Effect separadas.</span><span class="sxs-lookup"><span data-stu-id="22d49-111">To use the Effects 11 runtime on multiple instances, you must create separate ID3DX11Effect instances.</span></span> <span data-ttu-id="22d49-112">Como o ID3D11DeviceContext também é de thread único, você deve passar diferentes instâncias de ID3D11DeviceContext para cada instância de efeito ao aplicar.</span><span class="sxs-lookup"><span data-stu-id="22d49-112">Because the ID3D11DeviceContext is also single-threaded, you should pass different ID3D11DeviceContext instances to each effect instance on Apply.</span></span> <span data-ttu-id="22d49-113">Você pode usar esses contextos de dispositivo separados para criar listas de comandos para que o thread de renderização possa aplicá-las no contexto do dispositivo imediato.</span><span class="sxs-lookup"><span data-stu-id="22d49-113">You can use these separate device contexts to create command lists so that the rendering thread can apply them on the immediate device context.</span></span>

<span data-ttu-id="22d49-114">A maneira mais fácil de criar vários efeitos que encapsulam a mesma funcionalidade, para uso em vários threads, é criar um efeito e, em seguida, fazer cópias clonadas.</span><span class="sxs-lookup"><span data-stu-id="22d49-114">The easiest way to create multiple effects that encapsulate the same functionality, for use on multiple threads, is to create one effect and then make cloned copies.</span></span> <span data-ttu-id="22d49-115">A clonagem tem as seguintes vantagens em relação à criação de várias cópias do zero:</span><span class="sxs-lookup"><span data-stu-id="22d49-115">Cloning has the following advantages over creating multiple copies from scratch:</span></span>

1.  <span data-ttu-id="22d49-116">A rotina de clonagem é mais rápida do que a rotina de criação.</span><span class="sxs-lookup"><span data-stu-id="22d49-116">The cloning routine is faster than the creation routine.</span></span>
2.  <span data-ttu-id="22d49-117">Os efeitos clonados compartilham sombreadores criados, blocos de estado e instâncias de classe (para que eles não precisem ser recriados).</span><span class="sxs-lookup"><span data-stu-id="22d49-117">Cloned effects share created shaders, state blocks, and class instances (so they don't have to be recreated).</span></span>
3.  <span data-ttu-id="22d49-118">Os efeitos clonados podem compartilhar buffers constantes.</span><span class="sxs-lookup"><span data-stu-id="22d49-118">Cloned effects can share constant buffers.</span></span>
4.  <span data-ttu-id="22d49-119">Os efeitos clonados começam com o estado que corresponde ao efeito atual (valores de variável, seja ou não otimizado).</span><span class="sxs-lookup"><span data-stu-id="22d49-119">Cloned effects begin with state that matches the current effect (variable values, whether or not it has been optimized).</span></span>

<span data-ttu-id="22d49-120">Consulte [clonar um efeito](d3d11-graphics-programming-guide-effects-cloning.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="22d49-120">See [Cloning an Effect](d3d11-graphics-programming-guide-effects-cloning.md) for more information.</span></span>

## <a name="effect-pools-and-groups"></a><span data-ttu-id="22d49-121">Pools de efeitos e grupos</span><span class="sxs-lookup"><span data-stu-id="22d49-121">Effect Pools and Groups</span></span>

<span data-ttu-id="22d49-122">De longe, o uso mais predominante dos pools de efeito no Direct3D 10 era o agrupamento de materiais.</span><span class="sxs-lookup"><span data-stu-id="22d49-122">By far the most prevalent use of effect pools in Direct3D 10 was for grouping materials.</span></span> <span data-ttu-id="22d49-123">Os pools de efeito foram removidos dos efeitos 11 e os grupos foram adicionados, o que é um método mais eficiente de agrupamento de materiais.</span><span class="sxs-lookup"><span data-stu-id="22d49-123">Effect Pools have been removed from Effects 11 and groups have been added, which is a more efficient method of grouping materials.</span></span>

<span data-ttu-id="22d49-124">Um grupo de efeitos é simplesmente um conjunto de técnicas.</span><span class="sxs-lookup"><span data-stu-id="22d49-124">An effect group is simply a set of techniques.</span></span> <span data-ttu-id="22d49-125">Consulte [sintaxe do grupo de efeitos (Direct3D 11)](d3d11-effect-group-syntax.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="22d49-125">See [Effect Group Syntax (Direct3D 11)](d3d11-effect-group-syntax.md) for more information.</span></span>

<span data-ttu-id="22d49-126">Considere a seguinte hierarquia de efeito com quatro efeitos filho e um pool de efeito:</span><span class="sxs-lookup"><span data-stu-id="22d49-126">Consider the following effect hierarchy with four child effects and one effect pool:</span></span>


```
// Effect Pool
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

// Effect Child 1
#include "EffectPool.fx"
technique10 GrassMaterialLowSpec { ... }

// Effect Child 2
#include "EffectPool.fx"
technique10 GrassMaterialHighSpec { ... }

// Effect Child 3
#include "EffectPool.fx"
technique10 WaterMaterialLowSpec { ... }

// Effect Child 4
#include "EffectPool.fx"
technique10 WaterMaterialHighSpec { ... }
```



<span data-ttu-id="22d49-127">Você pode obter a mesma funcionalidade nos efeitos 11 usando grupos:</span><span class="sxs-lookup"><span data-stu-id="22d49-127">You can achieve the same functionality in Effects 11 by using groups:</span></span>


```
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

fxgroup GrassMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}

fxgroup WaterMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}
```



## <a name="new-shader-stages"></a><span data-ttu-id="22d49-128">Novos estágios de sombreador</span><span class="sxs-lookup"><span data-stu-id="22d49-128">New Shader Stages</span></span>

<span data-ttu-id="22d49-129">Há três novos estágios de sombreador no Direct3D 11: o sombreador envoltória, o sombreador de domínio e o sombreador de computação.</span><span class="sxs-lookup"><span data-stu-id="22d49-129">There are three new shader stages in Direct3D 11: the hull shader, domain shader, and compute shader.</span></span> <span data-ttu-id="22d49-130">Os efeitos 11 lidam com isso de maneira semelhante a sombreadores de vértice, sombreadores de geometria e sombreadores de pixel.</span><span class="sxs-lookup"><span data-stu-id="22d49-130">Effects 11 handles these in a similar manner to vertex shaders, geometry shaders, and pixel shaders.</span></span>

<span data-ttu-id="22d49-131">Três novos tipos de variáveis foram adicionados aos efeitos 11:</span><span class="sxs-lookup"><span data-stu-id="22d49-131">Three new variable types have been added to Effects 11:</span></span>

-   <span data-ttu-id="22d49-132">HullShader</span><span class="sxs-lookup"><span data-stu-id="22d49-132">HullShader</span></span>
-   <span data-ttu-id="22d49-133">DomainShader</span><span class="sxs-lookup"><span data-stu-id="22d49-133">DomainShader</span></span>
-   <span data-ttu-id="22d49-134">ComputeShader</span><span class="sxs-lookup"><span data-stu-id="22d49-134">ComputeShader</span></span>

<span data-ttu-id="22d49-135">Se você usar esses sombreadores em uma técnica, deverá rotular essa técnica como "technique11" e não "technique10".</span><span class="sxs-lookup"><span data-stu-id="22d49-135">If you use these shaders in a technique, you must label that technique "technique11", and not "technique10".</span></span> <span data-ttu-id="22d49-136">O sombreador de computação não pode ser definido na mesma passagem que qualquer outro Estado de gráfico (outros sombreadores, blocos de estado ou destinos de renderização).</span><span class="sxs-lookup"><span data-stu-id="22d49-136">The compute shader cannot be set in the same pass as any other graphics state (other shaders, state blocks, or render targets).</span></span>

## <a name="new-texture-types"></a><span data-ttu-id="22d49-137">Novos tipos de textura</span><span class="sxs-lookup"><span data-stu-id="22d49-137">New Texture Types</span></span>

<span data-ttu-id="22d49-138">O Direct3D 11 dá suporte aos seguintes tipos de textura:</span><span class="sxs-lookup"><span data-stu-id="22d49-138">Direct3D 11 supports the following texture types:</span></span>

-   [<span data-ttu-id="22d49-139">AppendStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="22d49-139">AppendStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [<span data-ttu-id="22d49-140">ByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="22d49-140">ByteAddressBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer)
-   [<span data-ttu-id="22d49-141">ConsumeStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="22d49-141">ConsumeStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)
-   [<span data-ttu-id="22d49-142">StructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="22d49-142">StructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer)

## <a name="unordered-access-views"></a><span data-ttu-id="22d49-143">Exibições de acesso não ordenado</span><span class="sxs-lookup"><span data-stu-id="22d49-143">Unordered Access Views</span></span>

<span data-ttu-id="22d49-144">Os efeitos 11 dão suporte à obtenção e à definição dos novos tipos de exibição de acesso não ordenado.</span><span class="sxs-lookup"><span data-stu-id="22d49-144">Effects 11 supports getting and setting the new unordered access view types.</span></span> <span data-ttu-id="22d49-145">Isso funciona de maneira semelhante a texturas.</span><span class="sxs-lookup"><span data-stu-id="22d49-145">This works in a similar manner as textures.</span></span>

<span data-ttu-id="22d49-146">Considere estes efeitos HLSL exemplo:</span><span class="sxs-lookup"><span data-stu-id="22d49-146">Consider this Effects HLSL example:</span></span>


```
  
RWTexture1D<float> myUAV;
```



<span data-ttu-id="22d49-147">Você pode definir essa variável em C++ da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="22d49-147">You can set this variable in C++ as follows:</span></span>


```
  
ID3D11UnorderedAccessView* pUAVTexture1D = NULL;
ID3DX11EffectUnorderedAccessViewVariable* pUAVVar;
pUAVVar = pEffect->GetVariableByName("myUAV")->AsUnorderedAccessView();
pUAVVar->SetUnorderedAccessView( pUAVTexture1D );
```



<span data-ttu-id="22d49-148">O Direct3D 11 dá suporte aos seguintes tipos de exibição de acesso não ordenado:</span><span class="sxs-lookup"><span data-stu-id="22d49-148">Direct3D 11 supports the following unordered access view types:</span></span>

-   <span data-ttu-id="22d49-149">RWBuffer</span><span class="sxs-lookup"><span data-stu-id="22d49-149">RWBuffer</span></span>
-   <span data-ttu-id="22d49-150">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="22d49-150">RWByteAddressBuffer</span></span>
-   <span data-ttu-id="22d49-151">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="22d49-151">RWStructuredBuffer</span></span>
-   <span data-ttu-id="22d49-152">RWTexture1D</span><span class="sxs-lookup"><span data-stu-id="22d49-152">RWTexture1D</span></span>
-   <span data-ttu-id="22d49-153">RWTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="22d49-153">RWTexture1DArray</span></span>
-   <span data-ttu-id="22d49-154">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="22d49-154">RWTexture2D</span></span>
-   <span data-ttu-id="22d49-155">RWTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="22d49-155">RWTexture2DArray</span></span>
-   <span data-ttu-id="22d49-156">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="22d49-156">RWTexture3D</span></span>

## <a name="interfaces-and-class-instances"></a><span data-ttu-id="22d49-157">Interfaces e instâncias de classe</span><span class="sxs-lookup"><span data-stu-id="22d49-157">Interfaces and Class Instances</span></span>

<span data-ttu-id="22d49-158">Para a interface e a sintaxe de classe, consulte [interfaces e classes](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).</span><span class="sxs-lookup"><span data-stu-id="22d49-158">For interface and class syntax, see [Interfaces and Classes](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).</span></span>

<span data-ttu-id="22d49-159">Para usar interfaces e classes em efeitos, consulte [interfaces e classes em efeitos](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md).</span><span class="sxs-lookup"><span data-stu-id="22d49-159">For using interfaces and classes in effects, see [Interfaces and Classes in Effects](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md).</span></span>

## <a name="addressable-stream-out"></a><span data-ttu-id="22d49-160">Fluxo de saída endereçável</span><span class="sxs-lookup"><span data-stu-id="22d49-160">Addressable Stream Out</span></span>

<span data-ttu-id="22d49-161">No Direct3D 10, os sombreadores de geometria podem produzir um fluxo de dados para a unidade de saída de fluxo e a unidade rasterizadora.</span><span class="sxs-lookup"><span data-stu-id="22d49-161">In Direct3D 10, geometry shaders could output one stream of data to the stream output unit and the rasterizer unit.</span></span> <span data-ttu-id="22d49-162">No Direct3D11, os sombreadores de geometria podem produzir até quatro fluxos de dados para a unidade de saída do fluxo e, no máximo, um desses fluxos para a unidade do rasterizador.</span><span class="sxs-lookup"><span data-stu-id="22d49-162">In Direct3D11, geometry shaders can output up to four streams of data to the stream output unit, and at most one of those streams to the rasterizer unit.</span></span> <span data-ttu-id="22d49-163">O **ConstructGSWithSO** intrínseco foi atualizado para refletir essa nova funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="22d49-163">The **ConstructGSWithSO** intrinsic has been updated to reflect this new functionality.</span></span>

<span data-ttu-id="22d49-164">Consulte [sintaxe de fluxo horizontal](d3d11-graphics-reference-effect-streamout.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="22d49-164">See [Stream Out Syntax](d3d11-graphics-reference-effect-streamout.md) for more information.</span></span>

## <a name="setting-and-unsetting-device-state"></a><span data-ttu-id="22d49-165">Definindo e desdefinindo o estado do dispositivo</span><span class="sxs-lookup"><span data-stu-id="22d49-165">Setting and Unsetting Device State</span></span>

<span data-ttu-id="22d49-166">Nos efeitos 10, você poderia tornar os buffers constantes e os buffers de textura gerenciados pelo usuário usando as funções [**ID3D10EffectConstantBuffer:: SetConstantBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-setconstantbuffer) e [**SetTextureBuffer**](id3dx11effectconstantbuffer-settexturebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="22d49-166">In Effects 10, you could make constant buffers and texture buffers user-managed by using the [**ID3D10EffectConstantBuffer::SetConstantBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-setconstantbuffer) and [**SetTextureBuffer**](id3dx11effectconstantbuffer-settexturebuffer.md) functions.</span></span> <span data-ttu-id="22d49-167">Depois de chamar essas funções, os efeitos 10 de tempo de execução não gerenciam mais o buffer constante ou o buffer de textura e o usuário deve preencher os dados usando a interface ID3D10Device.</span><span class="sxs-lookup"><span data-stu-id="22d49-167">After you call these functions, the Effects 10 runtime no longer manages the constant buffer or texture buffer and the user must fill the data by using the ID3D10Device interface.</span></span>

<span data-ttu-id="22d49-168">Nos efeitos 11, você também pode fazer com que os blocos de estado (estado de mesclagem, estado do rasterizador, estado do estêncil de profundidade e estado de amostra) sejam gerenciados pelo usuário usando as seguintes chamadas:</span><span class="sxs-lookup"><span data-stu-id="22d49-168">In Effects 11, you can also make the state blocks (blend state, rasterizer state, depth-stencil state, and sampler state) user-managed by using the following calls:</span></span>

-   [<span data-ttu-id="22d49-169">**ID3DX11EffectBlendVariable:: setblendstate**</span><span class="sxs-lookup"><span data-stu-id="22d49-169">**ID3DX11EffectBlendVariable::SetBlendState**</span></span>](id3dx11effectblendvariable-setblendstate.md)
-   [<span data-ttu-id="22d49-170">**ID3DX11EffectRasterizerVariable::SetRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="22d49-170">**ID3DX11EffectRasterizerVariable::SetRasterizerState**</span></span>](id3dx11effectrasterizervariable-setrasterizerstate.md)
-   [<span data-ttu-id="22d49-171">**ID3DX11EffectDepthStencilVariable::SetDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="22d49-171">**ID3DX11EffectDepthStencilVariable::SetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)
-   [<span data-ttu-id="22d49-172">**ID3DX11EffectSamplerVariable:: setamostrar**</span><span class="sxs-lookup"><span data-stu-id="22d49-172">**ID3DX11EffectSamplerVariable::SetSampler**</span></span>](id3dx11effectsamplervariable-setsampler.md)

<span data-ttu-id="22d49-173">Depois que você chamar essas funções, o tempo de execução dos efeitos 11 não gerenciará mais as variáveis de bloco de estado, e os valores permanecerão inalterados.</span><span class="sxs-lookup"><span data-stu-id="22d49-173">After you call these functions, the Effects 11 runtime no longer manages the state block variables, and there values will remain unchanged.</span></span> <span data-ttu-id="22d49-174">Observe que, como os blocos de estado são imutáveis, o usuário deve definir um novo bloco de estado para alterar os valores.</span><span class="sxs-lookup"><span data-stu-id="22d49-174">Note that because state blocks are immutable, the user must set a new state block to change the values.</span></span>

<span data-ttu-id="22d49-175">Você também pode reverter buffers de constantes, buffers de textura e blocos de estado para o estado não gerenciado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="22d49-175">You can also revert constant buffers, texture buffers, and state blocks to the non-user managed state.</span></span> <span data-ttu-id="22d49-176">Se você remover essas variáveis, o tempo de execução dos efeitos 11 continuará a ser atualizado quando necessário.</span><span class="sxs-lookup"><span data-stu-id="22d49-176">If you unset these variables, the Effects 11 runtime will continue to update them when necessary.</span></span> <span data-ttu-id="22d49-177">Você pode usar as seguintes chamadas para remover a definição de variáveis gerenciadas pelo usuário:</span><span class="sxs-lookup"><span data-stu-id="22d49-177">You can use the following calls to unset user managed variables:</span></span>

-   [<span data-ttu-id="22d49-178">**ID3DX11EffectConstantBuffer::UndoSetConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="22d49-178">**ID3DX11EffectConstantBuffer::UndoSetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-undosetconstantbuffer.md)
-   [<span data-ttu-id="22d49-179">**ID3DX11EffectConstantBuffer::UndoSetTextureBuffer**</span><span class="sxs-lookup"><span data-stu-id="22d49-179">**ID3DX11EffectConstantBuffer::UndoSetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-undosettexturebuffer.md)
-   [<span data-ttu-id="22d49-180">**ID3DX11EffectBlendVariable::UndoSetBlendState**</span><span class="sxs-lookup"><span data-stu-id="22d49-180">**ID3DX11EffectBlendVariable::UndoSetBlendState**</span></span>](id3dx11effectblendvariable-undosetblendstate.md)
-   [<span data-ttu-id="22d49-181">**ID3DX11EffectRasterizerVariable::UndoSetRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="22d49-181">**ID3DX11EffectRasterizerVariable::UndoSetRasterizerState**</span></span>](id3dx11effectrasterizervariable-undosetrasterizerstate.md)
-   [<span data-ttu-id="22d49-182">**ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="22d49-182">**ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md)
-   [<span data-ttu-id="22d49-183">**ID3DX11EffectSamplerVariable::UndoSetSampler**</span><span class="sxs-lookup"><span data-stu-id="22d49-183">**ID3DX11EffectSamplerVariable::UndoSetSampler**</span></span>](id3dx11effectsamplervariable-undosetsampler.md)

## <a name="effects-virtual-machine"></a><span data-ttu-id="22d49-184">Afeta a máquina virtual</span><span class="sxs-lookup"><span data-stu-id="22d49-184">Effects Virtual Machine</span></span>

<span data-ttu-id="22d49-185">A máquina virtual de efeitos, que avaliou expressões complexas fora das funções, foi removida.</span><span class="sxs-lookup"><span data-stu-id="22d49-185">The effects virtual machine, which evaluated complex expressions outside of functions, has been removed.</span></span>

<span data-ttu-id="22d49-186">Não há suporte para os seguintes exemplos de expressões complexas:</span><span class="sxs-lookup"><span data-stu-id="22d49-186">The following examples of complex expressions are not supported:</span></span>

1.  <span data-ttu-id="22d49-187">SetPixelShader (myPSArray (i \* 3 + j));</span><span class="sxs-lookup"><span data-stu-id="22d49-187">SetPixelShader( myPSArray( i \* 3 + j ) );</span></span>
2.  <span data-ttu-id="22d49-188">SetPixelShader (myPSArray ((float) i);</span><span class="sxs-lookup"><span data-stu-id="22d49-188">SetPixelShader( myPSArray( (float)i );</span></span>
3.  <span data-ttu-id="22d49-189">FILTER = i + 2;</span><span class="sxs-lookup"><span data-stu-id="22d49-189">FILTER = i + 2;</span></span>

<span data-ttu-id="22d49-190">Há suporte para os seguintes exemplos de expressões não complexas:</span><span class="sxs-lookup"><span data-stu-id="22d49-190">The following examples of non-complex expressions are supported:</span></span>

1.  <span data-ttu-id="22d49-191">SetPixelShader( myPS );</span><span class="sxs-lookup"><span data-stu-id="22d49-191">SetPixelShader( myPS );</span></span>
2.  <span data-ttu-id="22d49-192">SetPixelShader (myPS \[ i \] );</span><span class="sxs-lookup"><span data-stu-id="22d49-192">SetPixelShader( myPS\[i\] );</span></span>
3.  <span data-ttu-id="22d49-193">SetPixelShader (myPS \[ uIndex \] );//uIndex é uma variável uint</span><span class="sxs-lookup"><span data-stu-id="22d49-193">SetPixelShader( myPS\[ uIndex \] ); // uIndex is a uint variable</span></span>
4.  <span data-ttu-id="22d49-194">FILTER = i;</span><span class="sxs-lookup"><span data-stu-id="22d49-194">FILTER = i;</span></span>
5.  <span data-ttu-id="22d49-195">FILTER = ANISOTROPIC;</span><span class="sxs-lookup"><span data-stu-id="22d49-195">FILTER = ANISOTROPIC;</span></span>

<span data-ttu-id="22d49-196">Essas expressões podem aparecer em expressões de bloco de estado (como FILTER) e expressões Pass (como SetPixelShader).</span><span class="sxs-lookup"><span data-stu-id="22d49-196">These expressions could appear in state block expressions (such as FILTER) and pass expressions (such as SetPixelShader).</span></span>

## <a name="source-availability-and-location"></a><span data-ttu-id="22d49-197">Disponibilidade e local de origem</span><span class="sxs-lookup"><span data-stu-id="22d49-197">Source Availability and Location</span></span>

<span data-ttu-id="22d49-198">Os efeitos 10 foram distribuídos em D3D10.dll.</span><span class="sxs-lookup"><span data-stu-id="22d49-198">Effects 10 was distributed in D3D10.dll.</span></span> <span data-ttu-id="22d49-199">Os efeitos 11 são distribuídos como fonte, com as soluções do Visual Studio correspondentes para compilá-lo.</span><span class="sxs-lookup"><span data-stu-id="22d49-199">Effects 11 is distributed as source, with corresponding Visual Studio solutions to compile it.</span></span> <span data-ttu-id="22d49-200">Quando você cria aplicativos de tipo de efeitos, recomendamos que inclua a fonte de efeitos 11 diretamente nesses aplicativos.</span><span class="sxs-lookup"><span data-stu-id="22d49-200">When you create effects-type applications, we recommend that you include the Effects 11 source directly in those applications.</span></span>

<span data-ttu-id="22d49-201">Você pode obter efeitos 11 de [efeitos para a atualização do Direct3D 11](https://github.com/Microsoft/FX11).</span><span class="sxs-lookup"><span data-stu-id="22d49-201">You can get Effects 11 from [Effects for Direct3D 11 Update](https://github.com/Microsoft/FX11).</span></span>

## <a name="related-topics"></a><span data-ttu-id="22d49-202">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="22d49-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22d49-203">Efeitos (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="22d49-203">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 