---
title: Modelo de sombreador 4
description: O Shader Model 4 é um superconjunto dos recursos no Shader Model 3, exceto que o Shader Model 4 não oferece suporte aos recursos no Shader Model 1.
ms.assetid: 76155749-11e9-41ff-881d-8f77f2729364
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3f1964eaf84e9b0a2669f59357f54d16b1b4cbd3
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104365475"
---
# <a name="shader-model-4"></a><span data-ttu-id="ddbf2-103">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="ddbf2-103">Shader Model 4</span></span>

<span data-ttu-id="ddbf2-104">O Shader Model 4 é um superconjunto dos recursos no [Shader Model 3](dx-graphics-hlsl-sm3.md), exceto que o Shader Model 4 não oferece suporte aos recursos no Shader Model 1.</span><span class="sxs-lookup"><span data-stu-id="ddbf2-104">Shader Model 4 is a superset of the capabilities in [Shader Model 3](dx-graphics-hlsl-sm3.md), except that Shader Model 4 doesn't support the features in Shader Model 1.</span></span> <span data-ttu-id="ddbf2-105">Ele foi projetado usando um núcleo de sombreador comum que fornece um conjunto comum de recursos para todos os sombreadores programáveis, que só podem ser programados usando HLSL.</span><span class="sxs-lookup"><span data-stu-id="ddbf2-105">It has been designed using a common-shader core that gives a common set of features to all programmable shaders, which are only programmable using HLSL.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ddbf2-106">Recurso</span><span class="sxs-lookup"><span data-stu-id="ddbf2-106">Feature</span></span></th>
<th><span data-ttu-id="ddbf2-107">Funcionalidade</span><span class="sxs-lookup"><span data-stu-id="ddbf2-107">Capability</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ddbf2-108">Conjunto de instruções</span><span class="sxs-lookup"><span data-stu-id="ddbf2-108">Instruction Set</span></span></td>
<td><span data-ttu-id="ddbf2-109"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Funções HLSL</strong></a></span><span class="sxs-lookup"><span data-stu-id="ddbf2-109"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL functions</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddbf2-110">Conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="ddbf2-110">Register Set</span></span></td>
<td><span data-ttu-id="ddbf2-111">O conjunto de registros é acessível por meio de membros em buffers de textura e constantes usando a semântica HLSL para coisas como empacotamento de componentes.</span><span class="sxs-lookup"><span data-stu-id="ddbf2-111">The register set is accessible through members in constant and texture buffers using HLSL semantics for things like component packing.</span></span>
<ul>
<li><span data-ttu-id="ddbf2-112">Registros de sombreador de pixel (consulte <a href="dx-graphics-hlsl-sm4-registers-ps-4-0.md">Registers-ps_4_0</a> e <a href="dx-graphics-hlsl-sm4-registers-ps-4-1.md">registers-ps_4_1</a>)</span><span class="sxs-lookup"><span data-stu-id="ddbf2-112">Pixel shader registers (see <a href="dx-graphics-hlsl-sm4-registers-ps-4-0.md">Registers - ps_4_0</a> and <a href="dx-graphics-hlsl-sm4-registers-ps-4-1.md">Registers - ps_4_1</a>)</span></span></li>
<li><span data-ttu-id="ddbf2-113">Registros de sombreador de vértice (consulte <a href="dx-graphics-hlsl-sm4-registers-vs-4-0.md">Registers-vs_4_0</a> e <a href="dx-graphics-hlsl-sm4-registers-vs-4-1.md">registers-vs_4_1</a>)</span><span class="sxs-lookup"><span data-stu-id="ddbf2-113">Vertex shader registers (see <a href="dx-graphics-hlsl-sm4-registers-vs-4-0.md">Registers - vs_4_0</a> and <a href="dx-graphics-hlsl-sm4-registers-vs-4-1.md">Registers - vs_4_1</a>)</span></span></li>
<li><span data-ttu-id="ddbf2-114">Registros de sombreador de geometria (consulte <a href="dx-graphics-hlsl-sm4-registers-gs-4-0.md">Registers-gs_4_0</a> e <a href="dx-graphics-hlsl-sm4-registers-gs-4-1.md">registers-gs_4_1</a>)</span><span class="sxs-lookup"><span data-stu-id="ddbf2-114">Geometry shader registers (see <a href="dx-graphics-hlsl-sm4-registers-gs-4-0.md">Registers - gs_4_0</a> and <a href="dx-graphics-hlsl-sm4-registers-gs-4-1.md">Registers - gs_4_1</a>)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddbf2-115">Sombreador máximo do vértice</span><span class="sxs-lookup"><span data-stu-id="ddbf2-115">Vertex Shader Max</span></span></td>
<td><span data-ttu-id="ddbf2-116">Nenhuma restrição</span><span class="sxs-lookup"><span data-stu-id="ddbf2-116">No restriction</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddbf2-117">Sombreador máximo de pixel</span><span class="sxs-lookup"><span data-stu-id="ddbf2-117">Pixel Shader Max</span></span></td>
<td><span data-ttu-id="ddbf2-118">Nenhuma restrição</span><span class="sxs-lookup"><span data-stu-id="ddbf2-118">No restriction</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddbf2-119">Novos perfis de sombreador adicionados</span><span class="sxs-lookup"><span data-stu-id="ddbf2-119">New Shader Profiles Added</span></span></td>
<td><span data-ttu-id="ddbf2-120">gs_4_0, ps_4_0, vs_4_0, gs_4_1 *, ps_4_1*, gs_4_1 \*</span><span class="sxs-lookup"><span data-stu-id="ddbf2-120">gs_4_0, ps_4_0, vs_4_0, gs_4_1 *, ps_4_1*, gs_4_1\*</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddbf2-121">Novo perfil de Effect-Framework adicionado</span><span class="sxs-lookup"><span data-stu-id="ddbf2-121">New Effect-Framework Profile Added</span></span></td>
<td><span data-ttu-id="ddbf2-122">fx_4_0, fx_4_1 \*</span><span class="sxs-lookup"><span data-stu-id="ddbf2-122">fx_4_0, fx_4_1\*</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ddbf2-123">\* -GS \_ 4 \_ 1, PS \_ 4 \_ 1, vs \_ 4 \_ 1 e FX \_ 4 \_ 1 têm suporte no Direct3D 10,1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="ddbf2-123">\* - gs\_4\_1, ps\_4\_1, vs\_4\_1 and fx\_4\_1 are supported on Direct3D 10.1 or higher.</span></span>

<span data-ttu-id="ddbf2-124">O Shader Model 4 dá suporte a um novo estágio de pipeline — o estágio Geometry-Shader — que pode ser usado para criar ou modificar a geometria existente.</span><span class="sxs-lookup"><span data-stu-id="ddbf2-124">Shader Model 4 supports a new pipeline stage—the geometry-shader stage—which can be used to create or modify existing geometry.</span></span> <span data-ttu-id="ddbf2-125">Ele também inclui dois novos tipos de objeto: um objeto Stream-output criado para streaming de dados do estágio Geometry e um objeto de textura modelo que implementa funções de amostragem de textura.</span><span class="sxs-lookup"><span data-stu-id="ddbf2-125">It also includes two new object types: a stream-output object designed for streaming data out of the geometry stage, and a templated texture object that implements texture sampling functions.</span></span>

-   [<span data-ttu-id="ddbf2-126">Núcleo de sombreador comum</span><span class="sxs-lookup"><span data-stu-id="ddbf2-126">Common-Shader Core</span></span>](dx-graphics-hlsl-common-core.md)
-   [<span data-ttu-id="ddbf2-127">Constantes</span><span class="sxs-lookup"><span data-stu-id="ddbf2-127">Constants</span></span>](dx-graphics-hlsl-constants.md)
-   [<span data-ttu-id="ddbf2-128">Objeto Geometry-Shader</span><span class="sxs-lookup"><span data-stu-id="ddbf2-128">Geometry-Shader Object</span></span>](dx-graphics-hlsl-geometry-shader.md)
-   [<span data-ttu-id="ddbf2-129">Fluxo-objeto de saída</span><span class="sxs-lookup"><span data-stu-id="ddbf2-129">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
-   [<span data-ttu-id="ddbf2-130">Objeto de textura</span><span class="sxs-lookup"><span data-stu-id="ddbf2-130">Texture Object</span></span>](dx-graphics-hlsl-to-type.md)

<span data-ttu-id="ddbf2-131">O Shader Model 4 dá suporte a regras de empacotamento que determinam quão rigidamente os dados podem ser organizados quando são armazenados.</span><span class="sxs-lookup"><span data-stu-id="ddbf2-131">Shader Model 4 supports packing rules that dictate how tightly data can be arranged when it is stored.</span></span> <span data-ttu-id="ddbf2-132">Essas regras são descritas em [regras de empacotamento para variáveis constantes](dx-graphics-hlsl-packing-rules.md)</span><span class="sxs-lookup"><span data-stu-id="ddbf2-132">These rules are described in [Packing Rules for Constant Variables](dx-graphics-hlsl-packing-rules.md)</span></span>

<span data-ttu-id="ddbf2-133">A seção de [assembly do Shader Model 4](dx-graphics-hlsl-sm4-asm.md) descreve as instruções de assembly que o sombreador modelo 4 e suporte ao modelo do sombreador 4,1.</span><span class="sxs-lookup"><span data-stu-id="ddbf2-133">The [Shader Model 4 Assembly](dx-graphics-hlsl-sm4-asm.md) section describes the assembly instructions that the Shader Model 4 and Shader Model 4.1 support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ddbf2-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ddbf2-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddbf2-135">Modelos de sombreador vs. perfis de sombreador</span><span class="sxs-lookup"><span data-stu-id="ddbf2-135">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




