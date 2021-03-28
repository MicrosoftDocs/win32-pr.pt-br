---
title: DEFB-vs
description: Define um valor constante booliano, que deve ser carregado sempre que um sombreador for definido como um dispositivo.
ms.assetid: 1db41115-14aa-462e-a7ee-c0a53fee97d8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9bd5ef8ea4218890c025fdebc87154ca1224d33c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917329"
---
# <a name="defb---vs"></a><span data-ttu-id="87390-103">DEFB-vs</span><span class="sxs-lookup"><span data-stu-id="87390-103">defb - vs</span></span>

<span data-ttu-id="87390-104">Define um valor constante booliano, que deve ser carregado sempre que um sombreador for definido como um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="87390-104">Defines a Boolean constant value, which should be loaded anytime a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="87390-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="87390-105">Syntax</span></span>



| <span data-ttu-id="87390-106">DEFB dest, boolianvalue</span><span class="sxs-lookup"><span data-stu-id="87390-106">defb dest, booleanValue</span></span> |
|-------------------------|



 

<span data-ttu-id="87390-107">onde</span><span class="sxs-lookup"><span data-stu-id="87390-107">where</span></span>

-   <span data-ttu-id="87390-108">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="87390-108">dst is the destination register.</span></span>
-   <span data-ttu-id="87390-109">boolianvalue é um valor booliano, true ou false.</span><span class="sxs-lookup"><span data-stu-id="87390-109">booleanValue is a boolean value, either True or False.</span></span>

## <a name="remarks"></a><span data-ttu-id="87390-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="87390-110">Remarks</span></span>



| <span data-ttu-id="87390-111">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="87390-111">Vertex shader versions</span></span> | <span data-ttu-id="87390-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="87390-112">1\_1</span></span> | <span data-ttu-id="87390-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="87390-113">2\_0</span></span> | <span data-ttu-id="87390-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="87390-114">2\_x</span></span> | <span data-ttu-id="87390-115">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="87390-115">2\_sw</span></span> | <span data-ttu-id="87390-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="87390-116">3\_0</span></span> | <span data-ttu-id="87390-117">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="87390-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="87390-118">defb</span><span class="sxs-lookup"><span data-stu-id="87390-118">defb</span></span>                   |      | <span data-ttu-id="87390-119">x</span><span class="sxs-lookup"><span data-stu-id="87390-119">x</span></span>    | <span data-ttu-id="87390-120">x</span><span class="sxs-lookup"><span data-stu-id="87390-120">x</span></span>    | <span data-ttu-id="87390-121">x</span><span class="sxs-lookup"><span data-stu-id="87390-121">x</span></span>     | <span data-ttu-id="87390-122">x</span><span class="sxs-lookup"><span data-stu-id="87390-122">x</span></span>    | <span data-ttu-id="87390-123">x</span><span class="sxs-lookup"><span data-stu-id="87390-123">x</span></span>     |



 

<span data-ttu-id="87390-124">A instrução DEFB-vs define uma constante de sombreador booliana cujo valor é carregado sempre que um sombreador é definido como um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="87390-124">The defb - vs instruction defines a boolean shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="87390-125">Elas são chamadas de constantes imediatas.</span><span class="sxs-lookup"><span data-stu-id="87390-125">These are called immediate constants.</span></span> <span data-ttu-id="87390-126">Constantes imediatas têm precedência sobre constantes definidas pelo método de API SetVertexShaderConstantB.</span><span class="sxs-lookup"><span data-stu-id="87390-126">Immediate constants take precedence over constants set by the API method SetVertexShaderConstantB.</span></span>

<span data-ttu-id="87390-127">Há duas maneiras de definir uma constante booliana em um sombreador.</span><span class="sxs-lookup"><span data-stu-id="87390-127">There are two ways to set a boolean constant in a shader.</span></span>

1.  <span data-ttu-id="87390-128">Use DEFB-vs para definir a constante diretamente dentro de um sombreador.</span><span class="sxs-lookup"><span data-stu-id="87390-128">Use defb - vs to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="87390-129">Use os métodos de API para definir uma constante.</span><span class="sxs-lookup"><span data-stu-id="87390-129">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="87390-130">Use [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb) para definir uma constante booliana.</span><span class="sxs-lookup"><span data-stu-id="87390-130">Use [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb) to set a Boolean constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87390-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87390-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87390-132">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="87390-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="87390-133">def-vs</span><span class="sxs-lookup"><span data-stu-id="87390-133">def - vs</span></span>](def---vs.md)
</dt> <dt>

[<span data-ttu-id="87390-134">defi-vs</span><span class="sxs-lookup"><span data-stu-id="87390-134">defi - vs</span></span>](defi---vs.md)
</dt> </dl>

 

 