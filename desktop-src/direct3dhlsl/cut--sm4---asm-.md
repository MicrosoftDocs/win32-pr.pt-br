---
title: recortar (sm4-ASM)
description: Instrução Geometry Shader que conclui a topologia primitiva atual (se algum vértice tiver sido emitido) e iniciará uma nova topologia do tipo declarado pelo sombreador Geometry.
ms.assetid: 9B28E33D-F518-4844-BE3F-BE61B5F08B4F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c462d2f4dc2e0c6b4076f577610c93794e890af
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104967094"
---
# <a name="cut-sm4---asm"></a><span data-ttu-id="7ea42-103">recortar (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="7ea42-103">cut (sm4 - asm)</span></span>

<span data-ttu-id="7ea42-104">Instrução Geometry Shader que conclui a topologia primitiva atual (se algum vértice tiver sido emitido) e iniciará uma nova topologia do tipo declarado pelo sombreador Geometry.</span><span class="sxs-lookup"><span data-stu-id="7ea42-104">Geometry Shader instruction that completes the current primitive topology (if any vertices have been emitted), and starts a new topology of the type declared by the Geometry Shader.</span></span>



| <span data-ttu-id="7ea42-105">recortar</span><span class="sxs-lookup"><span data-stu-id="7ea42-105">cut</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="7ea42-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ea42-106">Remarks</span></span>

<span data-ttu-id="7ea42-107">Quando o **recorte** é executado, a primeira coisa que acontece é que qualquer topologia emitida anteriormente pela invocação do sombreador de geometria é concluída.</span><span class="sxs-lookup"><span data-stu-id="7ea42-107">When **cut** is executed, the first thing that happens is that any previously emitted topology by the Geometry Shader invocation is completed.</span></span> <span data-ttu-id="7ea42-108">Se não forem emitidos vértices suficientes para a topologia primitiva anterior, eles serão descartados.</span><span class="sxs-lookup"><span data-stu-id="7ea42-108">If not enough vertices were emitted for the previous primitive topology, they are discarded.</span></span> <span data-ttu-id="7ea42-109">Como as únicas topologias de saída disponíveis para o sombreador Geometry são PointList, linestrip e Trianglestrip, nunca há vértices sobrantes após o **corte**.</span><span class="sxs-lookup"><span data-stu-id="7ea42-109">Because the only available output topologies for the Geometry Shader are pointlist, linestrip, and trianglestrip, there are never any leftover vertices upon **cut**.</span></span>

<span data-ttu-id="7ea42-110">Depois que a topologia anterior, se houver, for concluída, **Cut** fará com que uma nova topologia comece, usando a topologia declarada como a saída do sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="7ea42-110">After the previous topology, if any, is completed, **cut** causes a new topology to begin, using the topology declared as the Geometry Shader output.</span></span>

## <a name="restrictions"></a><span data-ttu-id="7ea42-111">Restrições</span><span class="sxs-lookup"><span data-stu-id="7ea42-111">Restrictions</span></span>

-   <span data-ttu-id="7ea42-112">A instrução **Cut** aplica-se somente ao sombreador Geometry.</span><span class="sxs-lookup"><span data-stu-id="7ea42-112">The **cut** instruction applies only to the Geometry Shader.</span></span>
-   <span data-ttu-id="7ea42-113">**recortar** pode aparecer qualquer número de vezes no sombreador de geometria, incluindo dentro do controle de fluxo.</span><span class="sxs-lookup"><span data-stu-id="7ea42-113">**cut** can appear any number of times in the Geometry Shader, including within flow control.</span></span>
-   <span data-ttu-id="7ea42-114">Se o sombreador de geometria terminar e os vértices tiverem sido emitidos, a topologia que ele está compilando será concluída, como se um **recorte** fosse executado como a última instrução.</span><span class="sxs-lookup"><span data-stu-id="7ea42-114">If the Geometry Shader ends and vertices have been emitted, the topology they are building is completed, as if a **cut** was executed as the last instruction.</span></span>
-   <span data-ttu-id="7ea42-115">Se os fluxos tiverem sido declarados, o [ \_ fluxo de recorte](cut-stream---sm5---asm-.md) deverá ser usado em vez de **recortado**.</span><span class="sxs-lookup"><span data-stu-id="7ea42-115">If streams have been declared, then [cut\_stream](cut-stream---sm5---asm-.md) must be used instead of **cut**.</span></span>

<span data-ttu-id="7ea42-116">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="7ea42-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7ea42-117">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="7ea42-117">Vertex Shader</span></span> | <span data-ttu-id="7ea42-118">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="7ea42-118">Geometry Shader</span></span> | <span data-ttu-id="7ea42-119">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="7ea42-119">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="7ea42-120">x</span><span class="sxs-lookup"><span data-stu-id="7ea42-120">x</span></span>               |              |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7ea42-121">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="7ea42-121">Minimum Shader Model</span></span>

<span data-ttu-id="7ea42-122">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7ea42-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7ea42-123">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="7ea42-123">Shader Model</span></span>                                              | <span data-ttu-id="7ea42-124">Com suporte</span><span class="sxs-lookup"><span data-stu-id="7ea42-124">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7ea42-125">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="7ea42-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7ea42-126">sim</span><span class="sxs-lookup"><span data-stu-id="7ea42-126">yes</span></span>       |
| [<span data-ttu-id="7ea42-127">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="7ea42-127">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7ea42-128">sim</span><span class="sxs-lookup"><span data-stu-id="7ea42-128">yes</span></span>       |
| [<span data-ttu-id="7ea42-129">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="7ea42-129">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7ea42-130">sim</span><span class="sxs-lookup"><span data-stu-id="7ea42-130">yes</span></span>       |
| [<span data-ttu-id="7ea42-131">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7ea42-131">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7ea42-132">não</span><span class="sxs-lookup"><span data-stu-id="7ea42-132">no</span></span>        |
| [<span data-ttu-id="7ea42-133">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7ea42-133">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7ea42-134">não</span><span class="sxs-lookup"><span data-stu-id="7ea42-134">no</span></span>        |
| [<span data-ttu-id="7ea42-135">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7ea42-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7ea42-136">não</span><span class="sxs-lookup"><span data-stu-id="7ea42-136">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7ea42-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7ea42-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ea42-138">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7ea42-138">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




