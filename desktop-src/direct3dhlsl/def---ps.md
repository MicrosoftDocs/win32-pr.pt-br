---
title: def-PS
description: Define constantes de ponto flutuante do sombreador de pixel.
ms.assetid: 679b3074-73f3-48de-8c7a-f43bff76b25a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b4f035df97de2645983862dd68aa7ec80fc22d4b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008306"
---
# <a name="def---ps"></a><span data-ttu-id="1b3b8-103">def-PS</span><span class="sxs-lookup"><span data-stu-id="1b3b8-103">def - ps</span></span>

<span data-ttu-id="1b3b8-104">Define constantes de ponto flutuante do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="1b3b8-104">Defines pixel shader floating-point constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b3b8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b3b8-105">Syntax</span></span>



| <span data-ttu-id="1b3b8-106">def DST, fVvalue1, fValue2, fValue3, fValue4</span><span class="sxs-lookup"><span data-stu-id="1b3b8-106">def dst, fVvalue1, fValue2, fValue3, fValue4</span></span> |
|----------------------------------------------|



 

<span data-ttu-id="1b3b8-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="1b3b8-107">Where:</span></span>

-   <span data-ttu-id="1b3b8-108">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="1b3b8-108">dst is the destination register.</span></span>
-   <span data-ttu-id="1b3b8-109">fValue1 fValue4 são valores de ponto flutuante..</span><span class="sxs-lookup"><span data-stu-id="1b3b8-109">fValue1 to fValue4 are floating-point values..</span></span>

## <a name="remarks"></a><span data-ttu-id="1b3b8-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b3b8-110">Remarks</span></span>



| <span data-ttu-id="1b3b8-111">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="1b3b8-111">Pixel shader versions</span></span> | <span data-ttu-id="1b3b8-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="1b3b8-112">1\_1</span></span> | <span data-ttu-id="1b3b8-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="1b3b8-113">1\_2</span></span> | <span data-ttu-id="1b3b8-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="1b3b8-114">1\_3</span></span> | <span data-ttu-id="1b3b8-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="1b3b8-115">1\_4</span></span> | <span data-ttu-id="1b3b8-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1b3b8-116">2\_0</span></span> | <span data-ttu-id="1b3b8-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="1b3b8-117">2\_x</span></span> | <span data-ttu-id="1b3b8-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="1b3b8-118">2\_sw</span></span> | <span data-ttu-id="1b3b8-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1b3b8-119">3\_0</span></span> | <span data-ttu-id="1b3b8-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="1b3b8-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="1b3b8-121">def</span><span class="sxs-lookup"><span data-stu-id="1b3b8-121">def</span></span>                   | <span data-ttu-id="1b3b8-122">x</span><span class="sxs-lookup"><span data-stu-id="1b3b8-122">x</span></span>    | <span data-ttu-id="1b3b8-123">x</span><span class="sxs-lookup"><span data-stu-id="1b3b8-123">x</span></span>    | <span data-ttu-id="1b3b8-124">x</span><span class="sxs-lookup"><span data-stu-id="1b3b8-124">x</span></span>    | <span data-ttu-id="1b3b8-125">x</span><span class="sxs-lookup"><span data-stu-id="1b3b8-125">x</span></span>    | <span data-ttu-id="1b3b8-126">x</span><span class="sxs-lookup"><span data-stu-id="1b3b8-126">x</span></span>    | <span data-ttu-id="1b3b8-127">x</span><span class="sxs-lookup"><span data-stu-id="1b3b8-127">x</span></span>    | <span data-ttu-id="1b3b8-128">x</span><span class="sxs-lookup"><span data-stu-id="1b3b8-128">x</span></span>     | <span data-ttu-id="1b3b8-129">x</span><span class="sxs-lookup"><span data-stu-id="1b3b8-129">x</span></span>    | <span data-ttu-id="1b3b8-130">x</span><span class="sxs-lookup"><span data-stu-id="1b3b8-130">x</span></span>     |



 

<span data-ttu-id="1b3b8-131">Há duas maneiras de definir uma constante de ponto flutuante em um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="1b3b8-131">There are two ways to set a floating-point constant in a pixel shader.</span></span>

1.  <span data-ttu-id="1b3b8-132">Use def para definir a constante diretamente dentro de um sombreador.</span><span class="sxs-lookup"><span data-stu-id="1b3b8-132">Use def to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="1b3b8-133">Use a API para definir uma constante com [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).</span><span class="sxs-lookup"><span data-stu-id="1b3b8-133">Use the API to set a constant with [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).</span></span>

<span data-ttu-id="1b3b8-134">def define uma constante de sombreador cujo valor é carregado sempre que um sombreador é definido como um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1b3b8-134">def defines a shader constant whose value is loaded any time a shader is set to a device.</span></span> <span data-ttu-id="1b3b8-135">Elas são chamadas de constantes imediatas.</span><span class="sxs-lookup"><span data-stu-id="1b3b8-135">These are called immediate constants.</span></span> <span data-ttu-id="1b3b8-136">Constantes imediatas têm precedência sobre constantes definidas pelo método de API.</span><span class="sxs-lookup"><span data-stu-id="1b3b8-136">Immediate constants take precedence over constants set by the API method.</span></span>

-   <span data-ttu-id="1b3b8-137">Deve aparecer antes da primeira instrução aritmética ou de endereçamento no sombreador.</span><span class="sxs-lookup"><span data-stu-id="1b3b8-137">Must appear before the first arithmetic or addressing instruction in shader.</span></span>
-   <span data-ttu-id="1b3b8-138">Podem ser combinados com as instruções [DCL-(SM2, SM3-PS ASM)](dcl---ps.md) (que são o outro tipo de instrução que reside no início de um sombreador).</span><span class="sxs-lookup"><span data-stu-id="1b3b8-138">Can be intermixed with [dcl - (sm2, sm3 - ps asm)](dcl---ps.md) instructions (which are the other type of instruction that resides at the beginning of a shader).</span></span>
-   <span data-ttu-id="1b3b8-139">o registro de hora de verão deve ser um [registro constante](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="1b3b8-139">dst register must be a [constant register](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>
-   <span data-ttu-id="1b3b8-140">A máscara de gravação deve estar cheia (padrão).</span><span class="sxs-lookup"><span data-stu-id="1b3b8-140">Write mask must be full (default).</span></span>
-   <span data-ttu-id="1b3b8-141">Se um [registro constante](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) for definido várias vezes em um sombreador, o último persistirá.</span><span class="sxs-lookup"><span data-stu-id="1b3b8-141">If a [constant register](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) is defined multiple times in a shader, the last one persists.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b3b8-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1b3b8-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b3b8-143">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="1b3b8-143">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 