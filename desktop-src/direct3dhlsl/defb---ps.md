---
title: DEFB-PS
description: Define um valor constante booliano, que deve ser carregado sempre que um sombreador for definido como um dispositivo.
ms.assetid: bb0b87cb-08a4-4790-88da-e398cea62911
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9437c7d6347da4bafae566386e09e4bc782bd16
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641568"
---
# <a name="defb---ps"></a><span data-ttu-id="34ede-103">DEFB-PS</span><span class="sxs-lookup"><span data-stu-id="34ede-103">defb - ps</span></span>

<span data-ttu-id="34ede-104">Define um valor constante booliano, que deve ser carregado sempre que um sombreador for definido como um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34ede-104">Defines a boolean constant value, which should be loaded any time a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="34ede-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="34ede-105">Syntax</span></span>



| <span data-ttu-id="34ede-106">DEFB dest, boolianvalue</span><span class="sxs-lookup"><span data-stu-id="34ede-106">defb dest, booleanValue</span></span> |
|-------------------------|



 

<span data-ttu-id="34ede-107">onde</span><span class="sxs-lookup"><span data-stu-id="34ede-107">where</span></span>

-   <span data-ttu-id="34ede-108">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="34ede-108">dst is the destination register.</span></span>
-   <span data-ttu-id="34ede-109">boolianvalue é um único valor booliano, true ou false.</span><span class="sxs-lookup"><span data-stu-id="34ede-109">booleanValue is a single boolean value, either true or false.</span></span>

## <a name="remarks"></a><span data-ttu-id="34ede-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="34ede-110">Remarks</span></span>



| <span data-ttu-id="34ede-111">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="34ede-111">Pixel shader versions</span></span> | <span data-ttu-id="34ede-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="34ede-112">1\_1</span></span> | <span data-ttu-id="34ede-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="34ede-113">1\_2</span></span> | <span data-ttu-id="34ede-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="34ede-114">1\_3</span></span> | <span data-ttu-id="34ede-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="34ede-115">1\_4</span></span> | <span data-ttu-id="34ede-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="34ede-116">2\_0</span></span> | <span data-ttu-id="34ede-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="34ede-117">2\_x</span></span> | <span data-ttu-id="34ede-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="34ede-118">2\_sw</span></span> | <span data-ttu-id="34ede-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="34ede-119">3\_0</span></span> | <span data-ttu-id="34ede-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="34ede-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="34ede-121">defb</span><span class="sxs-lookup"><span data-stu-id="34ede-121">defb</span></span>                  |      |      |      |      |      | <span data-ttu-id="34ede-122">x</span><span class="sxs-lookup"><span data-stu-id="34ede-122">x</span></span>    | <span data-ttu-id="34ede-123">x</span><span class="sxs-lookup"><span data-stu-id="34ede-123">x</span></span>     | <span data-ttu-id="34ede-124">x</span><span class="sxs-lookup"><span data-stu-id="34ede-124">x</span></span>    | <span data-ttu-id="34ede-125">x</span><span class="sxs-lookup"><span data-stu-id="34ede-125">x</span></span>     |



 

<span data-ttu-id="34ede-126">A instrução DEFB define uma constante de sombreador booliana cujo valor é carregado sempre que um sombreador é definido como um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34ede-126">The defb instruction defines a boolean shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="34ede-127">Elas são chamadas de constantes imediatas.</span><span class="sxs-lookup"><span data-stu-id="34ede-127">These are called immediate constants.</span></span> <span data-ttu-id="34ede-128">Constantes imediatas têm precedência sobre constantes definidas pelo método de API SetPixelShaderConstantB.</span><span class="sxs-lookup"><span data-stu-id="34ede-128">Immediate constants take precedence over constants set by the API method SetPixelShaderConstantB.</span></span>

<span data-ttu-id="34ede-129">Há duas maneiras de definir um booleanconstant em um sombreador.</span><span class="sxs-lookup"><span data-stu-id="34ede-129">There are two ways to set a booleanconstant in a shader.</span></span>

1.  <span data-ttu-id="34ede-130">Use DEFB para definir a constante diretamente dentro de um sombreador.</span><span class="sxs-lookup"><span data-stu-id="34ede-130">Use defb to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="34ede-131">Use os métodos de API para definir uma constante.</span><span class="sxs-lookup"><span data-stu-id="34ede-131">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="34ede-132">Use [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) para definir uma constante booliana.</span><span class="sxs-lookup"><span data-stu-id="34ede-132">Use [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) to set a Boolean constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="34ede-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="34ede-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34ede-134">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="34ede-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[<span data-ttu-id="34ede-135">def-PS</span><span class="sxs-lookup"><span data-stu-id="34ede-135">def - ps</span></span>](def---ps.md)
</dt> <dt>

[<span data-ttu-id="34ede-136">defi-PS</span><span class="sxs-lookup"><span data-stu-id="34ede-136">defi - ps</span></span>](defi---ps.md)
</dt> </dl>

 

 