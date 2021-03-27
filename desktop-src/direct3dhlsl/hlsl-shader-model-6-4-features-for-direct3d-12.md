---
title: Modelo de sombreador HLSL 6,4
description: Descreve os intrínsecos do Machine Learning adicionados ao modelo de sombreador HLSL 6,4.
ms.topic: article
ms.date: 02/21/2019
ms.openlocfilehash: 10e74b268243ab059c2d0945887a6d429d40bb53
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103837702"
---
# <a name="hlsl-shader-model-64"></a><span data-ttu-id="9d82f-103">Modelo de sombreador HLSL 6,4</span><span class="sxs-lookup"><span data-stu-id="9d82f-103">HLSL Shader Model 6.4</span></span>

<span data-ttu-id="9d82f-104">Descreve os intrínsecos do Machine Learning adicionados ao modelo de sombreador HLSL 6,4.</span><span class="sxs-lookup"><span data-stu-id="9d82f-104">Describes the machine learning intrinsics added to HLSL Shader Model 6.4.</span></span>

## <a name="shader-model-64"></a><span data-ttu-id="9d82f-105">Modelo do sombreador 6,4</span><span class="sxs-lookup"><span data-stu-id="9d82f-105">Shader Model 6.4</span></span>
<span data-ttu-id="9d82f-106">Esses intrínsecos são um recurso necessário/com suporte do Shader Model 6,4.</span><span class="sxs-lookup"><span data-stu-id="9d82f-106">These intrinsics are a required/supported feature of Shader model 6.4.</span></span> <span data-ttu-id="9d82f-107">Consequentemente, nenhuma verificação de bit de recurso separada é necessária, além de garantir o uso do modelo de sombreador 6,4.</span><span class="sxs-lookup"><span data-stu-id="9d82f-107">Consequently, no separate capability bit check is required, beyond assuring the use of Shader Model 6.4.</span></span> <span data-ttu-id="9d82f-108">O cliente mínimo com suporte para essas rotinas é Windows 10, versão 1903.</span><span class="sxs-lookup"><span data-stu-id="9d82f-108">The minimum supported client for these routines is Windows 10, version 1903.</span></span>

## <a name="shading-language-intrinsics"></a><span data-ttu-id="9d82f-109">Intrínsecos da linguagem de sombreamento</span><span class="sxs-lookup"><span data-stu-id="9d82f-109">Shading language intrinsics</span></span>

### <a name="unsigned-integer-dot-product-of-4-elements-and-accumulate"></a><span data-ttu-id="9d82f-110">Inteiro não atribuído Dot-Product de 4 elementos e acumular</span><span class="sxs-lookup"><span data-stu-id="9d82f-110">Unsigned Integer Dot-Product of 4 Elements and Accumulate</span></span>
```syntax
uint32 dot4add_u8packed(uint32 a, uint32 b, uint32 acc); // ubyte4 a, b;
```
 
<span data-ttu-id="9d82f-111">Um ponto inteiro sem sinal de 4 dimensões-produto com adicionar.</span><span class="sxs-lookup"><span data-stu-id="9d82f-111">A 4-dimensional unsigned integer dot-product with add.</span></span> <span data-ttu-id="9d82f-112">Multiplica cada par correspondente de bytes int de 8 bits não assinados nas duas DWORDs de entrada e soma os resultados no acumulador inteiro não assinado de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9d82f-112">Multiplies together each corresponding pair of unsigned 8-bit int bytes in the two input DWORDs, and sums the results into the 32-bit unsigned integer accumulator.</span></span> <span data-ttu-id="9d82f-113">Essa instrução opera em uma única rota SIMD de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9d82f-113">This instruction operates within a single 32-bit wide SIMD lane.</span></span> <span data-ttu-id="9d82f-114">As entradas também são presumidas como quantidades de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9d82f-114">The inputs are also assumed to be 32-bit quantities.</span></span>
 
### <a name="signed-integer-dot-product-of-4-elements-and-accumulate"></a><span data-ttu-id="9d82f-115">Inteiro assinado Dot-Product de 4 elementos e acumular</span><span class="sxs-lookup"><span data-stu-id="9d82f-115">Signed Integer Dot-Product of 4 Elements and Accumulate</span></span>
```syntax
int32 dot4add_i8packed(uint32 a, uint32 b, int32 acc); // signed byte4 a, b;
```

<span data-ttu-id="9d82f-116">Um item de ponto inteiro com sinal 4-dimensional com Add.</span><span class="sxs-lookup"><span data-stu-id="9d82f-116">A 4-dimensional signed integer dot-product with add.</span></span> <span data-ttu-id="9d82f-117">Multiplica cada par correspondente de bytes int de 8 bits assinados nos dois DWORDs de entrada e soma os resultados no acumulador inteiro com sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9d82f-117">Multiplies together each corresponding pair of signed 8-bit int bytes in the two input DWORDs, and sums the results into the 32-bit signed integer accumulator.</span></span> <span data-ttu-id="9d82f-118">Essa instrução opera em uma única rota SIMD de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9d82f-118">This instruction operates within a single 32-bit wide SIMD lane.</span></span> <span data-ttu-id="9d82f-119">As entradas também são presumidas como quantidades de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9d82f-119">The inputs are also assumed to be 32-bit quantities.</span></span>
 
### <a name="single-precision-floating-point-2-element-dot-product-and-accumulate"></a><span data-ttu-id="9d82f-120">Ponto flutuante de precisão única de dois elementos Dot-Product e acumular</span><span class="sxs-lookup"><span data-stu-id="9d82f-120">Single Precision Floating Point 2-Element Dot-Product and Accumulate</span></span>
```syntax
float dot2add( half2 a, half2 b, float acc );
```

<span data-ttu-id="9d82f-121">Um ponto flutuante bidimensional, ponto-produto de vetores half2 com Add.</span><span class="sxs-lookup"><span data-stu-id="9d82f-121">A 2-dimensional floating point dot-product of half2 vectors with add.</span></span> <span data-ttu-id="9d82f-122">Multiplica os elementos dos dois vetores de entrada float de meia precisão juntos e soma os resultados no acumulador float de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9d82f-122">Multiplies the elements of the two half-precision float input vectors together and sums the results into the 32-bit float accumulator.</span></span> <span data-ttu-id="9d82f-123">Estas instruções operam em uma única rota SIMD de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9d82f-123">This instructions operates within a single 32-bit wide SIMD lane.</span></span> <span data-ttu-id="9d82f-124">As entradas são quantidades de 16 bits incluídas na mesma pista.</span><span class="sxs-lookup"><span data-stu-id="9d82f-124">The inputs are 16-bit quantities packed into the same lane.</span></span>

<span data-ttu-id="9d82f-125">Isso é abordado no bit de recurso de baixa precisão (indicando que a metade nativa e o suporte curto estão presentes).</span><span class="sxs-lookup"><span data-stu-id="9d82f-125">This is covered under the low-precision feature bit (indicating that native half and short support are present).</span></span>

### <a name="sv_shadingrate"></a><span data-ttu-id="9d82f-126">SV_ShadingRate</span><span class="sxs-lookup"><span data-stu-id="9d82f-126">SV_ShadingRate</span></span>
```syntax
uint shadingRate : SV_ShadingRate
```

<span data-ttu-id="9d82f-127">Um inteiro sem sinal representando quantos pixels de destino são gravados por cada invocação do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="9d82f-127">An unsigned integer representing how many target pixels are written by each invocation of the pixel shader.</span></span> <span data-ttu-id="9d82f-128">Os valores válidos pertencem ao conjunto de valores de enumeração [D3D12_SHADING_RATE](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate).</span><span class="sxs-lookup"><span data-stu-id="9d82f-128">Valid values belong to set of enumeration values [D3D12_SHADING_RATE](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate).</span></span>

<span data-ttu-id="9d82f-129">Esse valor de sistema está disponível em plataformas [D3D12_VARIABLE_SHADING_RATE_TIER_2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) ou superior.</span><span class="sxs-lookup"><span data-stu-id="9d82f-129">This system value is available on platforms that are [D3D12_VARIABLE_SHADING_RATE_TIER_2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) or higher.</span></span> <span data-ttu-id="9d82f-130">Ele pode ser gravado a partir de no máximo um vértice ou estágios de sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="9d82f-130">It can be written from at most one of vertex or geometry shader stages.</span></span> <span data-ttu-id="9d82f-131">Ele pode ser lido no estágio pixel shader.</span><span class="sxs-lookup"><span data-stu-id="9d82f-131">It can be read from the pixel shader stage.</span></span> <span data-ttu-id="9d82f-132">Para obter mais informações, consulte [sombreamento de taxa variável](../direct3d12/vrs.md).</span><span class="sxs-lookup"><span data-stu-id="9d82f-132">For more information, see the [Variable-rate Shading](../direct3d12/vrs.md).</span></span>