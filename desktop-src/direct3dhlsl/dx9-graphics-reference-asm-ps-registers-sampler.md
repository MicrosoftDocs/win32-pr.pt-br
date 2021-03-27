---
title: Amostra (Direct3D 9 ASM-PS)
description: Um amostra é um pseudo registro de entrada para um sombreador de pixel, que é usado para identificar o estágio de amostragem.
ms.assetid: 37cc28ae-fbd0-4f81-9e8e-f9609980d84e
keywords:
- Amostra, tipo (Direct3D 9 ASM-PS)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77875eed0827ad6bcb6d89111b13b6a31232dd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007726"
---
# <a name="sampler-direct3d-9-asm-ps"></a><span data-ttu-id="586bb-104">Amostra (Direct3D 9 ASM-PS)</span><span class="sxs-lookup"><span data-stu-id="586bb-104">Sampler (Direct3D 9 asm-ps)</span></span>

<span data-ttu-id="586bb-105">Um amostra é um pseudo registro de entrada para um sombreador de pixel, que é usado para identificar o estágio de amostragem.</span><span class="sxs-lookup"><span data-stu-id="586bb-105">A sampler is a input pseudo-register for a pixel shader, which is used to identify the sampling stage.</span></span> <span data-ttu-id="586bb-106">Existem registros de estágio de amostragem de sombreador de 16 pixels: S0 para S15.</span><span class="sxs-lookup"><span data-stu-id="586bb-106">There are 16 pixel shader sampling stage registers: s0 to s15.</span></span> <span data-ttu-id="586bb-107">Portanto, até 16 superfícies de textura podem ser lidas em uma única passagem de sombreador.</span><span class="sxs-lookup"><span data-stu-id="586bb-107">Therefore, up to 16 texture surfaces can be read in a single shader pass.</span></span> <span data-ttu-id="586bb-108">As instruções que usam um registro de amostra são texld e texldp.</span><span class="sxs-lookup"><span data-stu-id="586bb-108">The instructions that use a sampler register are texld and texldp.</span></span>

<span data-ttu-id="586bb-109">A amostra deve ser declarada antes do uso com a instrução [DCL \_ SampleType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="586bb-109">Sampler must be declared before use with the [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md) instruction.</span></span>



| <span data-ttu-id="586bb-110">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="586bb-110">Pixel shader versions</span></span> | <span data-ttu-id="586bb-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="586bb-111">1\_1</span></span> | <span data-ttu-id="586bb-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="586bb-112">1\_2</span></span> | <span data-ttu-id="586bb-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="586bb-113">1\_3</span></span> | <span data-ttu-id="586bb-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="586bb-114">1\_4</span></span> | <span data-ttu-id="586bb-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="586bb-115">2\_0</span></span> | <span data-ttu-id="586bb-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="586bb-116">2\_sw</span></span> | <span data-ttu-id="586bb-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="586bb-117">2\_x</span></span> | <span data-ttu-id="586bb-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="586bb-118">3\_0</span></span> | <span data-ttu-id="586bb-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="586bb-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="586bb-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="586bb-120">Sampler</span></span>               |      |      |      |      | <span data-ttu-id="586bb-121">x</span><span class="sxs-lookup"><span data-stu-id="586bb-121">x</span></span>    | <span data-ttu-id="586bb-122">x</span><span class="sxs-lookup"><span data-stu-id="586bb-122">x</span></span>     | <span data-ttu-id="586bb-123">x</span><span class="sxs-lookup"><span data-stu-id="586bb-123">x</span></span>    | <span data-ttu-id="586bb-124">x</span><span class="sxs-lookup"><span data-stu-id="586bb-124">x</span></span>    | <span data-ttu-id="586bb-125">x</span><span class="sxs-lookup"><span data-stu-id="586bb-125">x</span></span>     |



 

<span data-ttu-id="586bb-126">Os exemplos são pseudo-registros porque você não pode ler ou gravar diretamente neles.</span><span class="sxs-lookup"><span data-stu-id="586bb-126">Samplers are pseudo registers because you cannot directly read or write to them.</span></span>

<span data-ttu-id="586bb-127">Uma unidade de amostragem corresponde ao estágio de amostragem de textura, encapsulando o estado específico de amostragem fornecido por [**Setsamplestate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="586bb-127">A sampling unit corresponds to the texture sampling stage, encapsulating the sampling-specific state provided by [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span></span> <span data-ttu-id="586bb-128">Cada amostra identifica exclusivamente uma única superfície de textura, que é definida para a amostra correspondente usando [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span><span class="sxs-lookup"><span data-stu-id="586bb-128">Each sampler uniquely identifies a single texture surface, which is set to the corresponding sampler using the [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="586bb-129">No entanto, a mesma superfície de textura pode ser definida em vários exemplos.</span><span class="sxs-lookup"><span data-stu-id="586bb-129">However, the same texture surface can be set at multiple samplers.</span></span>

<span data-ttu-id="586bb-130">No momento do desenho, uma textura não pode ser definida simultaneamente como um destino de renderização e uma textura em um estágio.</span><span class="sxs-lookup"><span data-stu-id="586bb-130">At draw time, a texture cannot be simultaneously set as a render target and a texture at a stage.</span></span>

<span data-ttu-id="586bb-131">Um amostra pode aparecer como o único argumento na instrução de carga de textura: [texldl-PS](texldl---ps.md).</span><span class="sxs-lookup"><span data-stu-id="586bb-131">A sampler might appear as the only argument in the texture load instruction: [texldl - ps](texldl---ps.md).</span></span>

<span data-ttu-id="586bb-132">No PS \_ 3 \_ 0, se um amostra for usado, ele precisará ser declarado no início do programa de sombreador usando a instrução [DCL \_ SampleType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="586bb-132">In ps\_3\_0, if a sampler is used, it needs to be declared at the beginning of the shader program using the [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md) instruction.</span></span>

<span data-ttu-id="586bb-133">A amostragem de uma textura com uma dimensão superior à do presente nas coordenadas de textura é inválida.</span><span class="sxs-lookup"><span data-stu-id="586bb-133">Sampling a texture with a higher dimension than is present in the texture coordinates is illegal.</span></span> <span data-ttu-id="586bb-134">A amostragem de uma textura com uma dimensão menor do que a presente nas coordenadas de textura ignorará as coordenadas de textura extra.</span><span class="sxs-lookup"><span data-stu-id="586bb-134">Sampling a texture with a lower dimension than is present in the texture coordinates will ignore the extra texture coordinates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="586bb-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="586bb-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="586bb-136">Register</span><span class="sxs-lookup"><span data-stu-id="586bb-136">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 