---
title: tex2Dlod
description: Amostras de uma textura 2D com mipmaps. O LOD mipmap é especificado em t.w.
ms.assetid: 689eff39-f6ac-4c25-8b92-ca68707ae8ad
keywords:
- tex2Dlod HLSL
topic_type:
- apiref
api_name:
- tex2Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f63a922fe86dc10d984369a1a872f84089b4db34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967174"
---
# <a name="tex2dlod"></a><span data-ttu-id="ec9aa-105">tex2Dlod</span><span class="sxs-lookup"><span data-stu-id="ec9aa-105">tex2Dlod</span></span>

<span data-ttu-id="ec9aa-106">Amostras de uma textura 2D com mipmaps.</span><span class="sxs-lookup"><span data-stu-id="ec9aa-106">Samples a 2D texture with mipmaps.</span></span> <span data-ttu-id="ec9aa-107">O LOD mipmap é especificado em t.w.</span><span class="sxs-lookup"><span data-stu-id="ec9aa-107">The mipmap LOD is specified in t.w.</span></span>



| <span data-ttu-id="ec9aa-108">RET tex2Dlod (s, t)</span><span class="sxs-lookup"><span data-stu-id="ec9aa-108">ret tex2Dlod(s, t)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="ec9aa-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec9aa-109">Parameters</span></span>



| <span data-ttu-id="ec9aa-110">Item</span><span class="sxs-lookup"><span data-stu-id="ec9aa-110">Item</span></span>                                                   | <span data-ttu-id="ec9aa-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="ec9aa-111">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="ec9aa-112"><span id="s"></span><span id="S"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="ec9aa-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="ec9aa-113">\[no \] estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="ec9aa-113">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="ec9aa-114"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="ec9aa-114"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="ec9aa-115">\[na \] coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="ec9aa-115">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="ec9aa-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ec9aa-116">Return Value</span></span>

<span data-ttu-id="ec9aa-117">O valor dos dados de textura.</span><span class="sxs-lookup"><span data-stu-id="ec9aa-117">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="ec9aa-118">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="ec9aa-118">Type Description</span></span>



| <span data-ttu-id="ec9aa-119">Name</span><span class="sxs-lookup"><span data-stu-id="ec9aa-119">Name</span></span> | <span data-ttu-id="ec9aa-120">Entrada/saída</span><span class="sxs-lookup"><span data-stu-id="ec9aa-120">In/Out</span></span> | [<span data-ttu-id="ec9aa-121">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="ec9aa-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="ec9aa-122">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="ec9aa-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="ec9aa-123">Tamanho</span><span class="sxs-lookup"><span data-stu-id="ec9aa-123">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="ec9aa-124">s</span><span class="sxs-lookup"><span data-stu-id="ec9aa-124">s</span></span>    | <span data-ttu-id="ec9aa-125">in</span><span class="sxs-lookup"><span data-stu-id="ec9aa-125">in</span></span>     | [<span data-ttu-id="ec9aa-126">**objeto**</span><span class="sxs-lookup"><span data-stu-id="ec9aa-126">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="ec9aa-127">sampler2D</span><span class="sxs-lookup"><span data-stu-id="ec9aa-127">sampler2D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="ec9aa-128">1</span><span class="sxs-lookup"><span data-stu-id="ec9aa-128">1</span></span>    |
| <span data-ttu-id="ec9aa-129">t</span><span class="sxs-lookup"><span data-stu-id="ec9aa-129">t</span></span>    | <span data-ttu-id="ec9aa-130">in</span><span class="sxs-lookup"><span data-stu-id="ec9aa-130">in</span></span>     | [<span data-ttu-id="ec9aa-131">**vetor**</span><span class="sxs-lookup"><span data-stu-id="ec9aa-131">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="ec9aa-132">**barra**</span><span class="sxs-lookup"><span data-stu-id="ec9aa-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ec9aa-133">4</span><span class="sxs-lookup"><span data-stu-id="ec9aa-133">4</span></span>    |
| <span data-ttu-id="ec9aa-134">RET</span><span class="sxs-lookup"><span data-stu-id="ec9aa-134">ret</span></span>  | <span data-ttu-id="ec9aa-135">out</span><span class="sxs-lookup"><span data-stu-id="ec9aa-135">out</span></span>    | [<span data-ttu-id="ec9aa-136">**vetor**</span><span class="sxs-lookup"><span data-stu-id="ec9aa-136">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="ec9aa-137">**barra**</span><span class="sxs-lookup"><span data-stu-id="ec9aa-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ec9aa-138">4</span><span class="sxs-lookup"><span data-stu-id="ec9aa-138">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ec9aa-139">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="ec9aa-139">Minimum Shader Model</span></span>

<span data-ttu-id="ec9aa-140">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ec9aa-140">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ec9aa-141">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="ec9aa-141">Shader Model</span></span>                                                                       | <span data-ttu-id="ec9aa-142">Com suporte</span><span class="sxs-lookup"><span data-stu-id="ec9aa-142">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="ec9aa-143">[Modelo do sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="ec9aa-143">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) and higher shader models</span></span> | <span data-ttu-id="ec9aa-144">sim</span><span class="sxs-lookup"><span data-stu-id="ec9aa-144">yes</span></span>       |
| [<span data-ttu-id="ec9aa-145">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ec9aa-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                          | <span data-ttu-id="ec9aa-146">não</span><span class="sxs-lookup"><span data-stu-id="ec9aa-146">no</span></span>        |
| [<span data-ttu-id="ec9aa-147">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ec9aa-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="ec9aa-148">não</span><span class="sxs-lookup"><span data-stu-id="ec9aa-148">no</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="ec9aa-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec9aa-149">Remarks</span></span>

<span data-ttu-id="ec9aa-150">A partir do Direct3D 10, você pode usar a nova sintaxe HLSL para acessar texturas e outros recursos.</span><span class="sxs-lookup"><span data-stu-id="ec9aa-150">Starting with Direct3D 10, you can use new HLSL syntax to access textures and other resources.</span></span> <span data-ttu-id="ec9aa-151">Você pode substituir funções de pesquisa de textura de estilo intrínseco, como **tex2Dlod**, por um estilo mais orientado a objeto.</span><span class="sxs-lookup"><span data-stu-id="ec9aa-151">You can replace intrinsic-style texture lookup functions, such as **tex2Dlod**, with a more object-oriented style.</span></span> <span data-ttu-id="ec9aa-152">Nesse estilo orientado a objeto, as texturas são dissociadas dos exemplos e têm métodos para carregar e obter amostragem.</span><span class="sxs-lookup"><span data-stu-id="ec9aa-152">In this object-oriented style, textures are decoupled from samplers and have methods for loading and sampling.</span></span>

<span data-ttu-id="ec9aa-153">Para obter uma amostra de uma textura 2D, em vez de usar **tex2Dlod** como neste código:</span><span class="sxs-lookup"><span data-stu-id="ec9aa-153">To sample a 2D texture, instead of using **tex2Dlod** as in this code:</span></span>


```
sampler S;
...
color = tex2Dlod(S, Location);
```



<span data-ttu-id="ec9aa-154">Use o método [SampleLevel](dx-graphics-hlsl-to-samplelevel.md) de um [**objeto de textura**](dx-graphics-hlsl-to-type.md) como neste código:</span><span class="sxs-lookup"><span data-stu-id="ec9aa-154">Use the [SampleLevel](dx-graphics-hlsl-to-samplelevel.md) method of a [**Texture Object**](dx-graphics-hlsl-to-type.md) as in this code:</span></span>


```
Texture2D MyTexture;
SamplerState MySampler;
...
color = MyTexture.SampleLevel(MySampler, Location, LOD);
```



<span data-ttu-id="ec9aa-155">Para usar as funções de pesquisa de textura de estilo intrínseco, como **tex2Dlod**, com o [modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e superior, use [**D3DCOMPILE habilitar a \_ \_ \_ compatibilidade com versões anteriores**](d3dcompile-constants.md) para compilar.</span><span class="sxs-lookup"><span data-stu-id="ec9aa-155">To use the intrinsic-style texture lookup functions, such as **tex2Dlod**, with [shader model 4](dx-graphics-hlsl-sm4.md) and higher, use [**D3DCOMPILE\_ENABLE\_BACKWARDS\_COMPATIBILITY**](d3dcompile-constants.md) to compile.</span></span> <span data-ttu-id="ec9aa-156">No entanto, se você quiser direcionar o modelo de sombreador 4 e superior (até [ \* \_ 4 \_ 0 \_ nível \_ 9 \_ \* ](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)) com o código de estilo orientado a objeto mais recente, migre para a sintaxe HLSL mais recente.</span><span class="sxs-lookup"><span data-stu-id="ec9aa-156">However, if you want to target shader model 4 and higher (even [\*\_4\_0\_level\_9\_\*](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)) with newer object-oriented style code, migrate to the newer HLSL syntax.</span></span>

## <a name="see-also"></a><span data-ttu-id="ec9aa-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec9aa-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec9aa-158">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="ec9aa-158">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

