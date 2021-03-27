---
title: Referência do sombreador ASM
description: Os sombreadores orientam o pipeline gráfico programável.
ms.assetid: 2c58815c-83b5-4ae8-a192-ba865b485bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2941f4c32d03187ce08266bf1382cd1d94301ce0
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2019
ms.locfileid: "104967148"
---
# <a name="asm-shader-reference"></a><span data-ttu-id="e3acb-103">Referência do sombreador ASM</span><span class="sxs-lookup"><span data-stu-id="e3acb-103">Asm Shader Reference</span></span>

<span data-ttu-id="e3acb-104">Os sombreadores orientam o pipeline gráfico programável.</span><span class="sxs-lookup"><span data-stu-id="e3acb-104">Shaders drive the programmable graphics pipeline.</span></span>

## <a name="vertex-shader-reference"></a><span data-ttu-id="e3acb-105">Referência de sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="e3acb-105">Vertex Shader Reference</span></span>

-   [<span data-ttu-id="e3acb-106">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="e3acb-106">vs\_1\_1</span></span>](dx9-graphics-reference-asm-vs-1-1.md)
-   [<span data-ttu-id="e3acb-107">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e3acb-107">vs\_2\_0</span></span>](dx9-graphics-reference-asm-vs-2-0.md)
-   [<span data-ttu-id="e3acb-108">vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e3acb-108">vs\_2\_x</span></span>](dx9-graphics-reference-asm-vs-2-x.md)
-   [<span data-ttu-id="e3acb-109">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e3acb-109">vs\_3\_0</span></span>](dx9-graphics-reference-asm-vs-3-0.md)

<span data-ttu-id="e3acb-110">[Diferenças de sombreador de vértice](dx9-graphics-reference-asm-vs-differences.md) resume as diferenças entre as versões de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="e3acb-110">[Vertex Shader Differences](dx9-graphics-reference-asm-vs-differences.md) summarizes the differences between vertex shader versions.</span></span>

## <a name="pixel-shader-reference"></a><span data-ttu-id="e3acb-111">Referência de sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="e3acb-111">Pixel Shader Reference</span></span>

-   [<span data-ttu-id="e3acb-112">PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="e3acb-112">ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4</span></span>](dx9-graphics-reference-asm-ps-1-x.md)
-   [<span data-ttu-id="e3acb-113">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e3acb-113">ps\_2\_0</span></span>](dx9-graphics-reference-asm-ps-2-0.md)
-   [<span data-ttu-id="e3acb-114">PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e3acb-114">ps\_2\_x</span></span>](dx9-graphics-reference-asm-ps-2-x.md)
-   [<span data-ttu-id="e3acb-115">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e3acb-115">ps\_3\_0</span></span>](dx9-graphics-reference-asm-ps-3-0.md)

<span data-ttu-id="e3acb-116">[Diferenças de sombreador de pixel](dx9-graphics-reference-asm-ps-differences.md) resume as diferenças entre versões de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="e3acb-116">[Pixel Shader Differences](dx9-graphics-reference-asm-ps-differences.md) summarizes the differences between pixel shader versions.</span></span>

## <a name="shader-model-4-and-5-reference"></a><span data-ttu-id="e3acb-117">Referência do modelo do sombreador 4 e 5</span><span class="sxs-lookup"><span data-stu-id="e3acb-117">Shader Model 4 and 5 Reference</span></span>

<span data-ttu-id="e3acb-118">As seções de assembly do [sombreador Model 4](dx-graphics-hlsl-sm4-asm.md) e do [sombreador Model 5](shader-model-5-assembly--directx-hlsl-.md) descrevem as instruções que dão suporte ao Shader Model 4 e 5.</span><span class="sxs-lookup"><span data-stu-id="e3acb-118">The [Shader Model 4 Assembly](dx-graphics-hlsl-sm4-asm.md) and [Shader Model 5 Assembly](shader-model-5-assembly--directx-hlsl-.md) sections describe the instructions that shader model 4 and 5 support.</span></span>

## <a name="behavior-of-constant-registers-in-assembly-shaders"></a><span data-ttu-id="e3acb-119">Comportamento de registros constantes em sombreadores de assembly</span><span class="sxs-lookup"><span data-stu-id="e3acb-119">Behavior of Constant Registers in Assembly Shaders</span></span>

<span data-ttu-id="e3acb-120">Há duas maneiras de definir registros constantes em um sombreador de assembly:</span><span class="sxs-lookup"><span data-stu-id="e3acb-120">There are two ways to set constant registers in an assembly shader:</span></span>

-   <span data-ttu-id="e3acb-121">Declare uma constante de sombreador no código do assembly usando uma das \* instruções def.</span><span class="sxs-lookup"><span data-stu-id="e3acb-121">Declare a shader constant in assembly code using one of the def\* instructions.</span></span>
-   <span data-ttu-id="e3acb-122">Use um dos métodos de \* \* \* API Set ShaderConstant \* .</span><span class="sxs-lookup"><span data-stu-id="e3acb-122">Use one of the Set\*\*\*ShaderConstant\* API methods.</span></span>

### <a name="direct3d-9-shader-constants"></a><span data-ttu-id="e3acb-123">Constantes do sombreador do Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="e3acb-123">Direct3D 9 Shader Constants</span></span>

<span data-ttu-id="e3acb-124">No Direct3D 9, o tempo de vida das constantes definidas em um determinado sombreador é restrito à execução somente desse sombreador (e não é substituível).</span><span class="sxs-lookup"><span data-stu-id="e3acb-124">In Direct3D 9 the lifetime of defined constants in a given shader is confined to the execution of that shader only (and is non-overridable).</span></span> <span data-ttu-id="e3acb-125">Constantes definidas no Direct3D 9 não têm efeitos colaterais fora do sombreador.</span><span class="sxs-lookup"><span data-stu-id="e3acb-125">Defined constants in Direct3D 9 have no side effects outside of the shader.</span></span>

<span data-ttu-id="e3acb-126">Veja um exemplo usando o Direct3D 9:</span><span class="sxs-lookup"><span data-stu-id="e3acb-126">Here's an example using Direct3D 9:</span></span>


```
Given: 
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1:
    Call Set***Shader shader1
    Call Set***ShaderConstant* to set c4
    Call Draw
    Result: The shader will see the def'd value in c4

    
Given: 
    Scenario 1 has just completed
    Create shader2 (which references c4 but does not use the def instruction
      to define it) 

Scenario 2: 
    Call Set***Shader shader2
    Call Draw
    Result: The shader will see the value last set in c4 by 
     Set***ShaderConstant* in scenario 1. This is because shader 2 
     didn't def c4.
```



<span data-ttu-id="e3acb-127">No Direct3D 9, chamar get \* \* \* ShaderConstant \* recuperará apenas valores constantes definidos por meio de Set \* \* \* ShaderConstant \* .</span><span class="sxs-lookup"><span data-stu-id="e3acb-127">In Direct3D 9, calling Get\*\*\*ShaderConstant\* will only retrieve constant values set via Set\*\*\*ShaderConstant\*.</span></span>

### <a name="direct3d-8-shader-constants"></a><span data-ttu-id="e3acb-128">Constantes do sombreador do Direct3D 8</span><span class="sxs-lookup"><span data-stu-id="e3acb-128">Direct3D 8 Shader Constants</span></span>

<span data-ttu-id="e3acb-129">Esse comportamento é diferente no Direct3D 8. x.</span><span class="sxs-lookup"><span data-stu-id="e3acb-129">This behavior is different in Direct3D 8.x.</span></span>


```
Given:
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1 (repeated with Direct3D 8):
    Call Set***Shader with shader1
    Call Set***ShaderConstant to set c4
    Call Draw
    Result: The shader will see the value in c4 from Set***ShaderConstant
```



<span data-ttu-id="e3acb-130">No Direct3D 8. x Set \* \* \* ShaderConstant entra em vigor imediatamente.</span><span class="sxs-lookup"><span data-stu-id="e3acb-130">In Direct3D 8.x Set\*\*\*ShaderConstant takes effect immediately.</span></span> <span data-ttu-id="e3acb-131">Considere este cenário:</span><span class="sxs-lookup"><span data-stu-id="e3acb-131">Consider this scenario:</span></span>


```
Given:
    Create shader1 which references c4 and defines it with the def instruction
    
Scenario 3:
    Call Set***Shader with shader1
    Call Draw
    Result: The shader will see the def'd value in c4

Given:
    Scenario 3 has just completed
    Create shader2 (which references c4 but does not use the def instruction 
      to define it)     
    
Scenario 4 :    
    Call Set***Shader with shader2
    Call Draw
    Result: The shader will see the def'd value in c4 (set by def in shader 1)
```



<span data-ttu-id="e3acb-132">O resultado indesejável é que a ordem na qual os sombreadores são definidos pode afetar o comportamento observado de sombreadores individuais.</span><span class="sxs-lookup"><span data-stu-id="e3acb-132">The undesirable result is that the order in which the shaders are set could affect the observed behavior of individual shaders.</span></span>

## <a name="shader-driver-model-requirements"></a><span data-ttu-id="e3acb-133">Requisitos de modelo de driver do sombreador</span><span class="sxs-lookup"><span data-stu-id="e3acb-133">Shader Driver Model Requirements</span></span>

<span data-ttu-id="e3acb-134">As interfaces do Direct3D 9 são restritas a drivers de interface de driver de dispositivo (DDI) que são do nível DirectX 7 e superior.</span><span class="sxs-lookup"><span data-stu-id="e3acb-134">Direct3D 9 interfaces are restricted to device driver interface (DDI) drivers that are DirectX 7-level and above.</span></span> <span data-ttu-id="e3acb-135">Para verificar o nível de DDI, execute a [ferramenta de diagnóstico do DirectX](https://msdn.microsoft.com/library/Ee416792(v=VS.85).aspx) e examine o arquivo de texto salvo.</span><span class="sxs-lookup"><span data-stu-id="e3acb-135">To check the DDI level, run the [DirectX Diagnostic Tool](https://msdn.microsoft.com/library/Ee416792(v=VS.85).aspx) and examine the saved text file.</span></span>

<span data-ttu-id="e3acb-136">Para referência, as interfaces do Direct3D 8 funcionam apenas em drivers de DDI que são de nível DirectX 6 e acima.</span><span class="sxs-lookup"><span data-stu-id="e3acb-136">For reference, Direct3D 8 interfaces work only on DDI drivers that are DirectX 6-level and above.</span></span>

## <a name="shader-binary-format"></a><span data-ttu-id="e3acb-137">Formato binário do sombreador</span><span class="sxs-lookup"><span data-stu-id="e3acb-137">Shader Binary Format</span></span>

<span data-ttu-id="e3acb-138">O layout de bits bit do fluxo de instrução do sombreador é definido em D3d9types. h.</span><span class="sxs-lookup"><span data-stu-id="e3acb-138">The bitwise layout of the shader instruction stream is defined in D3d9types.h.</span></span> <span data-ttu-id="e3acb-139">Se você quiser projetar seu próprio compilador de sombreador ou ferramentas de construção e desejar obter mais informações sobre o fluxo do token do sombreador, consulte o kit de desenvolvimento de driver do Direct3D 9 (DDK).</span><span class="sxs-lookup"><span data-stu-id="e3acb-139">If you want to design your own shader compiler or construction tools and you want more information about the shader token stream, refer to the Direct3D 9 Driver Development Kit (DDK).</span></span>

## <a name="c-like-shader-language"></a><span data-ttu-id="e3acb-140">Linguagem de sombreador semelhante a C</span><span class="sxs-lookup"><span data-stu-id="e3acb-140">C-like Shader Language</span></span>

<span data-ttu-id="e3acb-141">Consulte a [referência do HLSL](dx-graphics-hlsl-reference.md) para ter uma linguagem de sombreador semelhante a C.</span><span class="sxs-lookup"><span data-stu-id="e3acb-141">See [HLSL Reference](dx-graphics-hlsl-reference.md) to experience a C-like shader language.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3acb-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e3acb-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3acb-143">Referência para HLSL</span><span class="sxs-lookup"><span data-stu-id="e3acb-143">Reference for HLSL</span></span>](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 




