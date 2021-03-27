---
title: Registro de inteiro constante (referência do HLSL PS)
description: Os registros inteiros constantes são usados somente por loop-PS e Rep-PS.
ms.assetid: 85720ec0-b6aa-4a24-910c-3ad0468300dc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9b03a27a95f84ae30a70147caaf5662e1949cf18
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967201"
---
# <a name="constant-integer-register-hlsl-ps-reference"></a><span data-ttu-id="f21fb-103">Registro de inteiro constante (referência do HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="f21fb-103">Constant integer register (HLSL PS reference)</span></span>

<span data-ttu-id="f21fb-104">Os registros inteiros constantes são usados somente por [loop-PS](loop---ps.md) e [Rep-PS](rep---ps.md).</span><span class="sxs-lookup"><span data-stu-id="f21fb-104">Constant integer registers are used only by [loop - ps](loop---ps.md) and [rep - ps](rep---ps.md).</span></span>

<span data-ttu-id="f21fb-105">Eles podem ser definidos usando [defi-PS](defi---ps.md) ou [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti).</span><span class="sxs-lookup"><span data-stu-id="f21fb-105">They can be set using [defi - ps](defi---ps.md) or [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti).</span></span>

<span data-ttu-id="f21fb-106">Quando usado como um argumento para a instrução do [loop-PS](loop---ps.md) :</span><span class="sxs-lookup"><span data-stu-id="f21fb-106">When used as an argument to the [loop - ps](loop---ps.md) instruction:</span></span>

-   <span data-ttu-id="f21fb-107">. x é a contagem de iteração.</span><span class="sxs-lookup"><span data-stu-id="f21fb-107">.x is the iteration count.</span></span> <span data-ttu-id="f21fb-108">(o[Rep-PS](rep---ps.md) usa apenas este componente).</span><span class="sxs-lookup"><span data-stu-id="f21fb-108">([rep - ps](rep---ps.md) uses only this component).</span></span>
-   <span data-ttu-id="f21fb-109">. y é o valor inicial para o contador de loop.</span><span class="sxs-lookup"><span data-stu-id="f21fb-109">.y is the initial value for the loop counter.</span></span>
-   <span data-ttu-id="f21fb-110">. z é a etapa de incremento para o contador de loop.</span><span class="sxs-lookup"><span data-stu-id="f21fb-110">.z is the increment step for the loop counter.</span></span>



| <span data-ttu-id="f21fb-111">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="f21fb-111">Pixel shader versions</span></span>     | <span data-ttu-id="f21fb-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="f21fb-112">1\_1</span></span> | <span data-ttu-id="f21fb-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="f21fb-113">1\_2</span></span> | <span data-ttu-id="f21fb-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f21fb-114">1\_3</span></span> | <span data-ttu-id="f21fb-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="f21fb-115">1\_4</span></span> | <span data-ttu-id="f21fb-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f21fb-116">2\_0</span></span> | <span data-ttu-id="f21fb-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f21fb-117">2\_sw</span></span> | <span data-ttu-id="f21fb-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f21fb-118">2\_x</span></span> | <span data-ttu-id="f21fb-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f21fb-119">3\_0</span></span> | <span data-ttu-id="f21fb-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f21fb-120">3\_sw</span></span> |
|---------------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="f21fb-121">Registro de inteiro constante</span><span class="sxs-lookup"><span data-stu-id="f21fb-121">Constant Integer Register</span></span> |      |      |      |      |      |       | <span data-ttu-id="f21fb-122">x</span><span class="sxs-lookup"><span data-stu-id="f21fb-122">x</span></span>    | <span data-ttu-id="f21fb-123">x</span><span class="sxs-lookup"><span data-stu-id="f21fb-123">x</span></span>    | <span data-ttu-id="f21fb-124">x</span><span class="sxs-lookup"><span data-stu-id="f21fb-124">x</span></span>     |



 

<span data-ttu-id="f21fb-125">O comportamento das constantes do sombreador foi alterado entre o Direct3D 8 e o Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="f21fb-125">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="f21fb-126">Para o Direct3D 9, as constantes definidas com defx atribuem valores ao espaço constante do sombreador.</span><span class="sxs-lookup"><span data-stu-id="f21fb-126">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="f21fb-127">O tempo de vida de uma constante declarada com defx é restrito apenas à execução desse sombreador.</span><span class="sxs-lookup"><span data-stu-id="f21fb-127">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="f21fb-128">Por outro lado, as constantes definidas usando as APIs SetXXXShaderConstantX inicializam constantes no espaço global.</span><span class="sxs-lookup"><span data-stu-id="f21fb-128">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="f21fb-129">As constantes no espaço global não são copiadas para o espaço local (visível para o sombreador) até que SetxxxShaderConstants seja chamado.</span><span class="sxs-lookup"><span data-stu-id="f21fb-129">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="f21fb-130">Para o Direct3D 8, as constantes definidas com defx ou as APIs atribuem valores ao espaço constante do sombreador.</span><span class="sxs-lookup"><span data-stu-id="f21fb-130">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="f21fb-131">Cada vez que o sombreador é executado, as constantes são usadas pelo sombreador atual, independentemente da técnica usada para defini-los.</span><span class="sxs-lookup"><span data-stu-id="f21fb-131">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f21fb-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f21fb-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f21fb-133">Register</span><span class="sxs-lookup"><span data-stu-id="f21fb-133">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 