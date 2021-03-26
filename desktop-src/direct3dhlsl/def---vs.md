---
title: def-vs
description: Define as constantes do sombreador de vértice.
ms.assetid: 13274e16-990f-4de8-9c99-6c268c7c06ef
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b5a55cb13eb7197986349c602ec35855a3f6364
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162398"
---
# <a name="def---vs"></a><span data-ttu-id="28496-103">def-vs</span><span class="sxs-lookup"><span data-stu-id="28496-103">def - vs</span></span>

<span data-ttu-id="28496-104">Define as constantes do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="28496-104">Defines vertex shader constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="28496-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="28496-105">Syntax</span></span>



| <span data-ttu-id="28496-106">def DST, float1, float2, float3, FLOAT4</span><span class="sxs-lookup"><span data-stu-id="28496-106">def dst, float1, float2, float3, float4</span></span> |
|-----------------------------------------|



 

<span data-ttu-id="28496-107">onde</span><span class="sxs-lookup"><span data-stu-id="28496-107">where</span></span>

-   <span data-ttu-id="28496-108">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="28496-108">dst is the destination register.</span></span>
-   <span data-ttu-id="28496-109">float1, float2, float3, FLOAT4 são quatro números de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="28496-109">float1, float2, float3, float4 are four floating point numbers.</span></span>

## <a name="remarks"></a><span data-ttu-id="28496-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="28496-110">Remarks</span></span>



| <span data-ttu-id="28496-111">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="28496-111">Vertex shader versions</span></span> | <span data-ttu-id="28496-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="28496-112">1\_1</span></span> | <span data-ttu-id="28496-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="28496-113">2\_0</span></span> | <span data-ttu-id="28496-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="28496-114">2\_x</span></span> | <span data-ttu-id="28496-115">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="28496-115">2\_sw</span></span> | <span data-ttu-id="28496-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="28496-116">3\_0</span></span> | <span data-ttu-id="28496-117">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="28496-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="28496-118">def</span><span class="sxs-lookup"><span data-stu-id="28496-118">def</span></span>                    | <span data-ttu-id="28496-119">x</span><span class="sxs-lookup"><span data-stu-id="28496-119">x</span></span>    | <span data-ttu-id="28496-120">x</span><span class="sxs-lookup"><span data-stu-id="28496-120">x</span></span>    | <span data-ttu-id="28496-121">x</span><span class="sxs-lookup"><span data-stu-id="28496-121">x</span></span>    | <span data-ttu-id="28496-122">x</span><span class="sxs-lookup"><span data-stu-id="28496-122">x</span></span>     | <span data-ttu-id="28496-123">x</span><span class="sxs-lookup"><span data-stu-id="28496-123">x</span></span>    | <span data-ttu-id="28496-124">x</span><span class="sxs-lookup"><span data-stu-id="28496-124">x</span></span>     |



 

<span data-ttu-id="28496-125">A instrução def define uma constante de sombreador cujo valor é carregado sempre que um sombreador é definido como um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="28496-125">The def instruction defines a shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="28496-126">Elas são chamadas de constantes imediatas.</span><span class="sxs-lookup"><span data-stu-id="28496-126">These are called immediate constants.</span></span> <span data-ttu-id="28496-127">Constantes imediatas têm precedência sobre constantes definidas por métodos de API SetVertexShaderConstantF.</span><span class="sxs-lookup"><span data-stu-id="28496-127">Immediate constants take precedence over constants set by API methods SetVertexShaderConstantF.</span></span>

<span data-ttu-id="28496-128">Há duas maneiras de definir uma constante em um sombreador.</span><span class="sxs-lookup"><span data-stu-id="28496-128">There are two ways to set a constant in a shader.</span></span>

1.  <span data-ttu-id="28496-129">Use def-vs para definir a constante diretamente dentro de um sombreador.</span><span class="sxs-lookup"><span data-stu-id="28496-129">Use def - vs to define the constant directly inside a shader.</span></span>

    <span data-ttu-id="28496-130">def-vs só pode definir constantes de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="28496-130">def - vs can only define floating-point constants.</span></span>

2.  <span data-ttu-id="28496-131">Use os métodos de API para definir uma constante.</span><span class="sxs-lookup"><span data-stu-id="28496-131">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="28496-132">Use [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf) para definir uma constante de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="28496-132">Use [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf) to set a floating-point constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28496-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="28496-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28496-134">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="28496-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="28496-135">defi-vs</span><span class="sxs-lookup"><span data-stu-id="28496-135">defi - vs</span></span>](defi---vs.md)
</dt> <dt>

[<span data-ttu-id="28496-136">DEFB-vs</span><span class="sxs-lookup"><span data-stu-id="28496-136">defb - vs</span></span>](defb---vs.md)
</dt> </dl>

 

 