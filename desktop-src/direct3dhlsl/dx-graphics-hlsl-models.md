---
title: Modelos de sombreador vs. perfis de sombreador
description: Modelos de sombreador vs. perfis de sombreador
ms.assetid: 6224f05e-20b1-42ea-96fb-63dd0edb720e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93a8d5c02662bff285c13461e8d716b03b8553b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822898"
---
# <a name="shader-models-vs-shader-profiles"></a><span data-ttu-id="c703d-103">Modelos de sombreador vs. perfis de sombreador</span><span class="sxs-lookup"><span data-stu-id="c703d-103">Shader Models vs Shader Profiles</span></span>

<span data-ttu-id="c703d-104">A linguagem de sombreamento de alto nível do DirectX implementa uma série de modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c703d-104">The High Level Shading Language for DirectX implements a series of shader models.</span></span> <span data-ttu-id="c703d-105">Usando o HLSL, você pode criar sombreadores programáveis C para o pipeline do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="c703d-105">Using HLSL, you can create C-like programmable shaders for the Direct3D pipeline.</span></span> <span data-ttu-id="c703d-106">Cada modelo de sombreador se baseia nos recursos do modelo antes dele, implementando mais funcionalidade com menos restrições.</span><span class="sxs-lookup"><span data-stu-id="c703d-106">Each shader model builds on the capabilites of the model before it, implementing more functionality with fewer restrictions.</span></span>

<span data-ttu-id="c703d-107">O modelo de sombreador 1 foi iniciado com DirectX 8 e instruções do tipo assembly e C-like incluídas.</span><span class="sxs-lookup"><span data-stu-id="c703d-107">Shader model 1 started with DirectX 8 and included assembly level and C-like instructions.</span></span> <span data-ttu-id="c703d-108">Esse modelo tem muitas limitações causadas pelo hardware de sombreador programável antecipado.</span><span class="sxs-lookup"><span data-stu-id="c703d-108">This model has many limitations caused by early programmable shader hardware.</span></span> <span data-ttu-id="c703d-109">O Shader Model 2 e 3 expandiu muito o número de instruções e os sombreadores constantes podem usar.</span><span class="sxs-lookup"><span data-stu-id="c703d-109">Shader model 2 and 3 greatly expanded on the number of instructions, and constants shaders could use.</span></span> <span data-ttu-id="c703d-110">Eles são muito mais eficientes do que o Shader Model 1, mas ainda têm algumas das limitações existentes do primeiro modelo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c703d-110">They are much more powerful than shader model 1, but still carry some of the existing limitations of the first shader model.</span></span>

<span data-ttu-id="c703d-111">A partir do Windows Vista, o Shader Model 4 é uma reformulação completa.</span><span class="sxs-lookup"><span data-stu-id="c703d-111">Starting with Windows Vista, shader model 4 is a complete redesign.</span></span> <span data-ttu-id="c703d-112">Ele permite instruções e constantes ilimitadas (dentro das restrições de hardware da sua máquina), tem objetos modelados para tornar a amostragem de textura mais limpa e mais eficiente e tem as menores restrições de qualquer modelo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c703d-112">It allows unlimited instructions and constants (within hardware constraints of your machine), has templated objects to make texture sampling cleaner and more efficient, and has the fewest restrictions of any shader model.</span></span> <span data-ttu-id="c703d-113">No entanto, ele requer o Windows Driver Model que só está disponível no sistema operacional Windows Vista (ou posterior).</span><span class="sxs-lookup"><span data-stu-id="c703d-113">It does however require the Windows Driver Model which is only available on the Windows Vista (or later) operating system.</span></span>

## <a name="shader-profiles"></a><span data-ttu-id="c703d-114">Perfis de sombreador</span><span class="sxs-lookup"><span data-stu-id="c703d-114">Shader Profiles</span></span>

<span data-ttu-id="c703d-115">Um perfil de sombreador é o destino para a compilação de um sombreador; Esta tabela lista os perfis de sombreador que têm suporte em cada modelo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c703d-115">A shader profile is the target for compiling a shader; this table lists the shader profiles that are supported by each shader model.</span></span>



|                                                    |                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c703d-116">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="c703d-116">Shader Model</span></span>                                       | <span data-ttu-id="c703d-117">Perfis de sombreador</span><span class="sxs-lookup"><span data-stu-id="c703d-117">Shader Profiles</span></span>                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="c703d-118">Modelo de sombreador 1</span><span class="sxs-lookup"><span data-stu-id="c703d-118">Shader Model 1</span></span>](dx-graphics-hlsl-sm1.md)         | <span data-ttu-id="c703d-119">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="c703d-119">vs\_1\_1</span></span>                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="c703d-120">Modelo de sombreador 2</span><span class="sxs-lookup"><span data-stu-id="c703d-120">Shader Model 2</span></span>](dx-graphics-hlsl-sm2.md)         | <span data-ttu-id="c703d-121">PS \_ 2 \_ 0, PS \_ 2 \_ x, vs \_ 2 \_ 0, vs \_ 2 \_ x, PS \_ 4 \_ 0 \_ nível \_ 9 0 \_ , PS \_ 4 \_ 0 \_ nível \_ 9 \_ 1, PS \_ 4 \_ 0 \_ nível \_ 9 \_ 3, vs \_ 4 \_ 0 \_ nível \_ 9 \_ 0, vs \_ 4 \_ 0 \_ nível \_ 9 \_ 1, vs \_ 4 \_ 0 \_ nível \_ 9 \_ 3, lib \_ 4 \_ 0 \_ nível \_ 9 \_ 1, lib \_ 4 \_ 0 \_ nível \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c703d-121">ps\_2\_0, ps\_2\_x, vs\_2\_0, vs\_2\_x, ps\_4\_0\_level\_9\_0, ps\_4\_0\_level\_9\_1, ps\_4\_0\_level\_9\_3, vs\_4\_0\_level\_9\_0, vs\_4\_0\_level\_9\_1, vs\_4\_0\_level\_9\_3, lib\_4\_0\_level\_9\_1, lib\_4\_0\_level\_9\_3</span></span>                                                                      |
| [<span data-ttu-id="c703d-122">Modelo de sombreador 3</span><span class="sxs-lookup"><span data-stu-id="c703d-122">Shader Model 3</span></span>](dx-graphics-hlsl-sm3.md)         | <span data-ttu-id="c703d-123">PS \_ 3 \_ 0, vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c703d-123">ps\_3\_0, vs\_3\_0</span></span>                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="c703d-124">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="c703d-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)         | <span data-ttu-id="c703d-125">cs \_ 4 \_ 0, GS \_ 4 \_ 0, PS \_ 4 \_ 0, vs \_ 4 \_ 0, cs \_ 4 \_ 1, GS \_ 4 \_ 1, PS \_ 4 \_ 1, vs \_ 4 \_ 1, lib \_ 4 \_ 0, lib \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="c703d-125">cs\_4\_0, gs\_4\_0, ps\_4\_0, vs\_4\_0, cs\_4\_1, gs\_4\_1, ps\_4\_1, vs\_4\_1, lib\_4\_0, lib\_4\_1</span></span>                                                                                                                                                                                                  |
| [<span data-ttu-id="c703d-126">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c703d-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="c703d-127">cs \_ 5 \_ 0, DS \_ 5 0 \_ , GS \_ 5 \_ 0, HS \_ 5 \_ 0, PS \_ 5 \_ 0, vs \_ 5 \_ 0, lib \_ 5 \_ 0 (embora GS \_ 4 \_ 0, GS \_ 4 \_ 1, PS \_ 4 \_ 0, PS \_ 4 \_ 1, vs \_ 4 \_ 0 e vs \_ 4 \_ 1 foram introduzidos no Shader Model 4,0, o Shader Model 5 adiciona suporte a esses perfis de sombreador para buffers estruturados e buffers de endereço de byte</span><span class="sxs-lookup"><span data-stu-id="c703d-127">cs\_5\_0, ds\_5\_0, gs\_5\_0, hs\_5\_0, ps\_5\_0, vs\_5\_0, lib\_5\_0 (Although gs\_4\_0, gs\_4\_1, ps\_4\_0, ps\_4\_1, vs\_4\_0, and vs\_4\_1 were introduced in shader model 4.0, shader model 5 adds support to these shader profiles for structured buffers and byte address buffers.)</span></span><br/> |
| [<span data-ttu-id="c703d-128">Modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="c703d-128">Shader Model 6</span></span>](shader-model-6-0.md)             | <span data-ttu-id="c703d-129">cs \_ 6 \_ 0, DS \_ 6 \_ 0, GS \_ 6 \_ 0, HS \_ 6 \_ 0, PS \_ 6 \_ 0, vs \_ 6 \_ 0, lib \_ 6 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c703d-129">cs\_6\_0, ds\_6\_0, gs\_6\_0, hs\_6\_0, ps\_6\_0, vs\_6\_0, lib\_6\_0</span></span>                                                                                                                                                                                                                                 |



 



|                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c703d-130">Diferenças entre o Direct3D 9 e o Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="c703d-130">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="c703d-131">O Direct3D 9 introduziu os modelos de sombreador 1, 2 e 3.</span><span class="sxs-lookup"><span data-stu-id="c703d-131">Direct3D 9 introduced shader models 1, 2, and 3.</span></span><br/> <span data-ttu-id="c703d-132">O Direct3D 10 introduziu o modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="c703d-132">Direct3D 10 introduced shader model 4.</span></span><br/> <span data-ttu-id="c703d-133">O Direct3D 10,1 introduziu o modelo de sombreador 4,1.</span><span class="sxs-lookup"><span data-stu-id="c703d-133">Direct3D 10.1 introduced shader model 4.1.</span></span><br/> |



 

## <a name="effect-profiles"></a><span data-ttu-id="c703d-134">Perfis de efeito</span><span class="sxs-lookup"><span data-stu-id="c703d-134">Effect Profiles</span></span>

<span data-ttu-id="c703d-135">Um perfil de efeito é o destino da compilação de um efeito/sombreador; Esta tabela lista os perfis de efeito que são suportados por cada versão do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="c703d-135">An effect profile is the target for compiling an effect/shader; this table lists the effect profiles that are supported by each version of Direct3D.</span></span>



|                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c703d-136">Diferenças entre o Direct3D 9 e o Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="c703d-136">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="c703d-137">O Direct3D 9 introduziu os perfis de estrutura de efeito FX \_ 1 \_ 0 e FX \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="c703d-137">Direct3D 9 introduced effect-framework profiles fx\_1\_0 and fx\_2\_0.</span></span><br/> <span data-ttu-id="c703d-138">O Direct3D 10 introduziu o perfil de estrutura de efeito FX \_ 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="c703d-138">Direct3D 10 introduced effect-framework profile fx\_4\_0.</span></span><br/> <span data-ttu-id="c703d-139">O Direct3D 10,1 introduziu o perfil de estrutura de efeito FX \_ 4 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="c703d-139">Direct3D 10.1 introduced effect-framework profile fx\_4\_1.</span></span><br/> <span data-ttu-id="c703d-140">O Direct3D 11 introduziu o perfil de estrutura de efeito FX \_ 5 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="c703d-140">Direct3D 11 introduced effect-framework profile fx\_5\_0.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="c703d-141">Esses perfis de efeitos herdados são preteridos.</span><span class="sxs-lookup"><span data-stu-id="c703d-141">These legacy effects profiles are deprecated.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c703d-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c703d-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c703d-143">Referência para HLSL</span><span class="sxs-lookup"><span data-stu-id="c703d-143">Reference for HLSL</span></span>](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 





