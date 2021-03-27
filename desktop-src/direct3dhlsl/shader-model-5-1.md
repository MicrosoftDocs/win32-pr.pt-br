---
title: Modelo do sombreador 5,1
description: Esta seção contém as páginas de referência para o modelo 5,1 do sombreador HLSL, introduzidas com D3D12.
ms.assetid: 814FAC95-7FD5-450F-964B-18E687DBCC56
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5fd2f2a2f4ebe86a090ebade8ebf8a033a7c612
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988575"
---
# <a name="shader-model-51"></a><span data-ttu-id="b48c0-103">Modelo do sombreador 5,1</span><span class="sxs-lookup"><span data-stu-id="b48c0-103">Shader Model 5.1</span></span>

<span data-ttu-id="b48c0-104">Esta seção contém as páginas de referência para o modelo 5,1 do sombreador HLSL, introduzidas com D3D12.</span><span class="sxs-lookup"><span data-stu-id="b48c0-104">This section contains the reference pages for HLSL Shader Model 5.1, introduced with D3D12.</span></span>

<span data-ttu-id="b48c0-105">O Shader Model 5,1 é funcionalmente muito semelhante ao [modelo de sombreador 5](d3d11-graphics-reference-sm5.md), a principal alteração é mais flexibilidade na seleção de recursos, permitindo a indexação de matrizes de descritores de dentro de um sombreador.</span><span class="sxs-lookup"><span data-stu-id="b48c0-105">Shader Model 5.1 is functionally very similar to [Shader Model 5](d3d11-graphics-reference-sm5.md), the main change is more flexibility in resource selection by allowing indexing of arrays of descriptors from within a shader.</span></span>



| <span data-ttu-id="b48c0-106">Recurso</span><span class="sxs-lookup"><span data-stu-id="b48c0-106">Feature</span></span>                   | <span data-ttu-id="b48c0-107">Funcionalidade</span><span class="sxs-lookup"><span data-stu-id="b48c0-107">Capability</span></span>                                                                |
|---------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="b48c0-108">Conjunto de instruções</span><span class="sxs-lookup"><span data-stu-id="b48c0-108">Instruction Set</span></span>           | [<span data-ttu-id="b48c0-109">**Funções intrínsecas HLSL**</span><span class="sxs-lookup"><span data-stu-id="b48c0-109">**HLSL intrinsic functions**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)  |
| <span data-ttu-id="b48c0-110">Sombreador máximo do vértice</span><span class="sxs-lookup"><span data-stu-id="b48c0-110">Vertex Shader Max</span></span>         | <span data-ttu-id="b48c0-111">Nenhuma restrição</span><span class="sxs-lookup"><span data-stu-id="b48c0-111">No restriction</span></span>                                                            |
| <span data-ttu-id="b48c0-112">Sombreador máximo de pixel</span><span class="sxs-lookup"><span data-stu-id="b48c0-112">Pixel Shader Max</span></span>          | <span data-ttu-id="b48c0-113">Nenhuma restrição</span><span class="sxs-lookup"><span data-stu-id="b48c0-113">No restriction</span></span>                                                            |
| <span data-ttu-id="b48c0-114">Novos perfis de sombreador adicionados</span><span class="sxs-lookup"><span data-stu-id="b48c0-114">New Shader Profiles Added</span></span> | <span data-ttu-id="b48c0-115">cs \_ 5 \_ 1, DS \_ 5 \_ 1, GS \_ 5 \_ 1, HS \_ 5 \_ 1, PS \_ 5 \_ 1, vs \_ 5 \_ 1, rootsig \_ 1 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b48c0-115">cs\_5\_1, ds\_5\_1, gs\_5\_1, hs\_5\_1, ps\_5\_1, vs\_5\_1, rootsig\_1\_0</span></span> |



 

## <a name="in-this-section"></a><span data-ttu-id="b48c0-116">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="b48c0-116">In this section</span></span>



| <span data-ttu-id="b48c0-117">Tópico</span><span class="sxs-lookup"><span data-stu-id="b48c0-117">Topic</span></span>                                                                           | <span data-ttu-id="b48c0-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="b48c0-118">Description</span></span>                                                           |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="b48c0-119">Objetos do Shader Model 5,1</span><span class="sxs-lookup"><span data-stu-id="b48c0-119">Shader Model 5.1 Objects</span></span>](shader-model-5-1-objects.md)<br/>             | <span data-ttu-id="b48c0-120">Os seguintes objetos foram adicionados ao modelo do sombreador 5,1.</span><span class="sxs-lookup"><span data-stu-id="b48c0-120">The following objects have been added to shader model 5.1.</span></span><br/> |
| [<span data-ttu-id="b48c0-121">Valores de sistema do modelo do sombreador 5,1</span><span class="sxs-lookup"><span data-stu-id="b48c0-121">Shader Model 5.1 System Values</span></span>](shader-model-5-1-system-values.md)<br/> | <span data-ttu-id="b48c0-122">O Shader Model 5,1 adiciona os novos valores de sistema a seguir.</span><span class="sxs-lookup"><span data-stu-id="b48c0-122">Shader Model 5.1 adds the following new system values.</span></span><br/>     |



 

## <a name="related-topics"></a><span data-ttu-id="b48c0-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b48c0-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b48c0-124">Modelos de sombreador vs. perfis de sombreador</span><span class="sxs-lookup"><span data-stu-id="b48c0-124">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> <dt>

[<span data-ttu-id="b48c0-125">Recursos do HLSL Shader Model 5,1 para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b48c0-125">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> </dl>

 

 





