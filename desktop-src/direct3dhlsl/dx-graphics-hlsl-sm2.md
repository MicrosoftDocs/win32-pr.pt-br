---
title: Modelo de sombreador 2
description: O Shader Model 2 adicionou funcionalidades adicionais ao Shader Model 1.
ms.assetid: 53c367d2-5b6a-4afa-894a-8ab9927169d5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 88bd2f6292687c5387fadf65f8f43437904168cc
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104988647"
---
# <a name="shader-model-2"></a><span data-ttu-id="0a86a-103">Modelo de sombreador 2</span><span class="sxs-lookup"><span data-stu-id="0a86a-103">Shader Model 2</span></span>

<span data-ttu-id="0a86a-104">O Shader Model 2 adicionou funcionalidades adicionais ao [Shader Model 1](dx-graphics-hlsl-sm1.md).</span><span class="sxs-lookup"><span data-stu-id="0a86a-104">Shader Model 2 added additional capabilities to [shader model 1](dx-graphics-hlsl-sm1.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0a86a-105">Recurso</span><span class="sxs-lookup"><span data-stu-id="0a86a-105">Feature</span></span></td>
<td><span data-ttu-id="0a86a-106">Funcionalidade</span><span class="sxs-lookup"><span data-stu-id="0a86a-106">Capability</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a86a-107">Conjunto de instruções</span><span class="sxs-lookup"><span data-stu-id="0a86a-107">Instruction Set</span></span></td>
<td><ul>
<li><span data-ttu-id="0a86a-108"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Funções HLSL</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a86a-108"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL functions</strong></a></span></span></li>
<li><span data-ttu-id="0a86a-109">Instruções de assembly (consulte <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-0.md">instruções-VS_2_0</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-x.md">instruções-vs_2_x</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-0.md">instruções de PS_2_0</a>, instruções de <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-x.md">ps_2_x</a>)</span><span class="sxs-lookup"><span data-stu-id="0a86a-109">Assembly instructions (see <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-0.md">Instructions - vs_2_0</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-x.md">Instructions - vs_2_x</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-0.md">ps_2_0 Instructions</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-x.md">ps_2_x Instructions</a>)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a86a-110">Conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="0a86a-110">Register Set</span></span></td>
<td><ul>
<li><span data-ttu-id="0a86a-111">Registros de sombreador de pixel (consulte <a href="dx9-graphics-reference-asm-ps-registers-ps-2-0.md">registros de PS_2_0</a>, <a href="dx9-graphics-reference-asm-ps-registers-ps-2-x.md">registros de ps_2_x</a>)</span><span class="sxs-lookup"><span data-stu-id="0a86a-111">Pixel shader registers (see <a href="dx9-graphics-reference-asm-ps-registers-ps-2-0.md">ps_2_0 Registers</a>, <a href="dx9-graphics-reference-asm-ps-registers-ps-2-x.md">ps_2_x Registers</a>)</span></span></li>
<li><span data-ttu-id="0a86a-112">Registros de sombreador de vértice (consulte <a href="dx9-graphics-reference-asm-vs-registers-vs-2-0.md">Registers-VS_2_0</a>, <a href="dx9-graphics-reference-asm-vs-registers-vs-2-x.md">registers-vs_2_x</a>)</span><span class="sxs-lookup"><span data-stu-id="0a86a-112">Vertex shader registers (see <a href="dx9-graphics-reference-asm-vs-registers-vs-2-0.md">Registers - vs_2_0</a>, <a href="dx9-graphics-reference-asm-vs-registers-vs-2-x.md">Registers - vs_2_x</a>)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a86a-113">Sombreador máximo de pixel</span><span class="sxs-lookup"><span data-stu-id="0a86a-113">Pixel Shader Max</span></span></td>
<td><ul>
<li><span data-ttu-id="0a86a-114">ps_2_0-32 Texture + 64 aritmético</span><span class="sxs-lookup"><span data-stu-id="0a86a-114">ps_2_0 - 32 texture + 64 arithmetic</span></span></li>
<li><span data-ttu-id="0a86a-115">ps_2_x-96 mínimo e até o número de Slots em D3DCAPS9. D3DPSHADERCAPS2_0. NumInstructionSlots.</span><span class="sxs-lookup"><span data-stu-id="0a86a-115">ps_2_x - 96 minimum, and up to the number of slots in D3DCAPS9.D3DPSHADERCAPS2_0.NumInstructionSlots.</span></span> <span data-ttu-id="0a86a-116">Consulte D3DPSHADERCAPS2_0</span><span class="sxs-lookup"><span data-stu-id="0a86a-116">See D3DPSHADERCAPS2_0</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a86a-117">Sombreador máximo do vértice</span><span class="sxs-lookup"><span data-stu-id="0a86a-117">Vertex Shader Max</span></span></td>
<td><span data-ttu-id="0a86a-118">256 instruções</span><span class="sxs-lookup"><span data-stu-id="0a86a-118">256 instructions</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a86a-119">Perfis de sombreador</span><span class="sxs-lookup"><span data-stu-id="0a86a-119">Shader Profiles</span></span></td>
<td><span data-ttu-id="0a86a-120">ps_2_0, ps_2_x, vs_2_0 vs_2_x</span><span class="sxs-lookup"><span data-stu-id="0a86a-120">ps_2_0, ps_2_x, vs_2_0, vs_2_x</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0a86a-121">Para obter mais detalhes sobre o modelo de sombreador 2, consulte:</span><span class="sxs-lookup"><span data-stu-id="0a86a-121">For more details on shader model 2, see:</span></span>

-   <span data-ttu-id="0a86a-122">[Sombreador de pixel 2,0](dx9-graphics-reference-asm-ps-2-0.md), [sombreador de pixel 2. x](dx9-graphics-reference-asm-ps-2-x.md)</span><span class="sxs-lookup"><span data-stu-id="0a86a-122">[Pixel Shader 2.0](dx9-graphics-reference-asm-ps-2-0.md), [Pixel Shader 2.x](dx9-graphics-reference-asm-ps-2-x.md)</span></span>
-   <span data-ttu-id="0a86a-123">[Sombreador de vértice 2,0](dx9-graphics-reference-asm-vs-2-0.md), [sombreador de vértice 2. x](dx9-graphics-reference-asm-vs-2-x.md)</span><span class="sxs-lookup"><span data-stu-id="0a86a-123">[Vertex Shader 2.0](dx9-graphics-reference-asm-vs-2-0.md), [Vertex Shader 2.x](dx9-graphics-reference-asm-vs-2-x.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a86a-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0a86a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a86a-125">Modelos de sombreador vs. perfis de sombreador</span><span class="sxs-lookup"><span data-stu-id="0a86a-125">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




