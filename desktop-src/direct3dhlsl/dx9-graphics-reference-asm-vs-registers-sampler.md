---
title: Amostra (Direct3D 9 ASM-vs)
description: Um amostra é um pseudo registro de entrada para um sombreador de vértice, que é usado para identificar o estágio de amostragem. Há quatro exemplos de sombreadores de vértice S0 para S3. Quatro superfícies de textura podem ser lidas em uma única passagem de sombreador.
ms.assetid: a4588ced-24e2-4d4e-93e4-35a985bafaa4
keywords:
- Amostra, tipo (Direct3D 9 ASM-vs)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 685f261da9d56dc29c0632d01cabbf29cd13a00f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366653"
---
# <a name="sampler-direct3d-9-asm-vs"></a><span data-ttu-id="11911-106">Amostra (Direct3D 9 ASM-vs)</span><span class="sxs-lookup"><span data-stu-id="11911-106">Sampler (Direct3D 9 asm-vs)</span></span>

<span data-ttu-id="11911-107">Um amostra é um pseudo registro de entrada para um sombreador de vértice, que é usado para identificar o estágio de amostragem.</span><span class="sxs-lookup"><span data-stu-id="11911-107">A sampler is a input pseudo-register for a vertex shader, which is used to identify the sampling stage.</span></span> <span data-ttu-id="11911-108">Há quatro exemplos de sombreador de vértice: S0 para S3.</span><span class="sxs-lookup"><span data-stu-id="11911-108">There are four vertex shader samplers: s0 to s3.</span></span> <span data-ttu-id="11911-109">Quatro superfícies de textura podem ser lidas em uma única passagem de sombreador.</span><span class="sxs-lookup"><span data-stu-id="11911-109">Four texture surfaces can be read in a single shader pass.</span></span>

<span data-ttu-id="11911-110">As amostras (Direct3D 9 ASM-vs) s são superregistradas porque você não pode ler ou gravar diretamente nelas.</span><span class="sxs-lookup"><span data-stu-id="11911-110">Sampler (Direct3D 9 asm-vs)s are pseudo registers because you cannot directly read or write to them.</span></span>

<span data-ttu-id="11911-111">Uma unidade de amostragem corresponde ao estágio de amostragem de textura, encapsulando o estado específico de amostragem fornecido por [**Setsamplestate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="11911-111">A sampling unit corresponds to the texture sampling stage, encapsulating the sampling-specific state provided by [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span></span> <span data-ttu-id="11911-112">Cada amostra identifica exclusivamente uma única superfície de textura, que é definida para a amostra correspondente usando [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span><span class="sxs-lookup"><span data-stu-id="11911-112">Each sampler uniquely identifies a single texture surface, which is set to the corresponding sampler using the [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="11911-113">No entanto, a mesma superfície de textura pode ser definida em vários exemplos.</span><span class="sxs-lookup"><span data-stu-id="11911-113">However, the same texture surface can be set at multiple samplers.</span></span>

<span data-ttu-id="11911-114">No momento do desenho, uma textura não pode ser definida simultaneamente como um destino de renderização e uma textura em um estágio.</span><span class="sxs-lookup"><span data-stu-id="11911-114">At draw time, a texture cannot be simultaneously set as a render target and a texture at a stage.</span></span>

<span data-ttu-id="11911-115">Como há quatro amostras, até quatro superfícies de textura podem ser lidas em uma única passagem de sombreador.</span><span class="sxs-lookup"><span data-stu-id="11911-115">Because there are four samplers, up to four texture surfaces can be read from in a single shader pass.</span></span> <span data-ttu-id="11911-116">Um amostra pode aparecer como o único argumento na instrução de carga de textura: [texldl-vs](texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="11911-116">A sampler might appear as the only argument in the texture load instruction: [texldl - vs](texldl---vs.md).</span></span>

<span data-ttu-id="11911-117">No vs \_ 3 \_ 0, se um amostra for usado, ele precisará ser declarado no início do programa de sombreador usando a instrução [DCL \_ SampleType (SM3-vs ASM)](dcl-samplertype---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="11911-117">In vs\_3\_0, if a sampler is used, it needs to be declared at the beginning of the shader program using the [dcl\_samplerType (sm3 - vs asm)](dcl-samplertype---vs.md) instruction.</span></span>



| <span data-ttu-id="11911-118">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="11911-118">Vertex shader versions</span></span> | <span data-ttu-id="11911-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="11911-119">1\_1</span></span> | <span data-ttu-id="11911-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="11911-120">2\_0</span></span> | <span data-ttu-id="11911-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="11911-121">2\_sw</span></span> | <span data-ttu-id="11911-122">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="11911-122">2\_x</span></span> | <span data-ttu-id="11911-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="11911-123">3\_0</span></span> | <span data-ttu-id="11911-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="11911-124">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="11911-125">Exemplo</span><span class="sxs-lookup"><span data-stu-id="11911-125">Sampler</span></span>                |      |      |       |      | <span data-ttu-id="11911-126">x</span><span class="sxs-lookup"><span data-stu-id="11911-126">x</span></span>    | <span data-ttu-id="11911-127">x</span><span class="sxs-lookup"><span data-stu-id="11911-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="11911-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="11911-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11911-129">Registros de sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="11911-129">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> <dt>

[<span data-ttu-id="11911-130">Texturas de vértice no vs \_ 3 \_ 0 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="11911-130">Vertex Textures in vs\_3\_0 (DirectX HLSL)</span></span>](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0)
</dt> </dl>

 

 