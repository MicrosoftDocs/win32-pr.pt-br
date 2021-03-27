---
title: Registro booliano constante (referência do HLSL PS)
description: Esse registro é uma coleção de bits usada em instruções de controle de fluxo estático (por exemplo, se bool-PS-else-PS-endif-PS).
ms.assetid: fb4abe19-d0cf-48ac-866e-4be60cc86bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4868be7c22ce5a6a1881ad7db8acf0af65330c04
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641562"
---
# <a name="constant-boolean-register-hlsl-ps-reference"></a><span data-ttu-id="928cd-103">Registro booliano constante (referência do HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="928cd-103">Constant Boolean register (HLSL PS reference)</span></span>

<span data-ttu-id="928cd-104">Esse registro é uma coleção de bits usada em instruções de controle de fluxo estático (por exemplo, [se bool-PS](if-bool---ps.md)  -  [else-PS](else---ps.md)  -  [endif-PS](endif---ps.md)).</span><span class="sxs-lookup"><span data-stu-id="928cd-104">This register is a collection of bits used in static flow control instructions (for example, [if bool - ps](if-bool---ps.md) - [else - ps](else---ps.md) - [endif - ps](endif---ps.md)).</span></span> <span data-ttu-id="928cd-105">Há 16 deles, portanto, um sombreador pode ter 16 condições de ramificação independentes.</span><span class="sxs-lookup"><span data-stu-id="928cd-105">There are 16 of them, therefore, a shader can have 16 independent branch conditions.</span></span> <span data-ttu-id="928cd-106">Eles podem ser definidos usando [DEFB-PS](defb---ps.md) ou [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb).</span><span class="sxs-lookup"><span data-stu-id="928cd-106">They can be set using [defb - ps](defb---ps.md) or [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb).</span></span>

<span data-ttu-id="928cd-107">O comportamento das constantes do sombreador foi alterado entre o Direct3D 8 e o Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="928cd-107">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="928cd-108">Para o Direct3D 9, as constantes definidas com defx atribuem valores ao espaço constante do sombreador.</span><span class="sxs-lookup"><span data-stu-id="928cd-108">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="928cd-109">O tempo de vida de uma constante declarada com defx é restrito apenas à execução desse sombreador.</span><span class="sxs-lookup"><span data-stu-id="928cd-109">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="928cd-110">Por outro lado, as constantes definidas usando as APIs SetXXXShaderConstantX inicializam constantes no espaço global.</span><span class="sxs-lookup"><span data-stu-id="928cd-110">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="928cd-111">As constantes no espaço global não são copiadas para o espaço local (visível para o sombreador) até que SetxxxShaderConstants seja chamado.</span><span class="sxs-lookup"><span data-stu-id="928cd-111">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="928cd-112">Para o Direct3D 8, as constantes definidas com defx ou as APIs atribuem valores ao espaço constante do sombreador.</span><span class="sxs-lookup"><span data-stu-id="928cd-112">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="928cd-113">Cada vez que o sombreador é executado, as constantes são usadas pelo sombreador atual, independentemente da técnica usada para defini-los.</span><span class="sxs-lookup"><span data-stu-id="928cd-113">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>



| <span data-ttu-id="928cd-114">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="928cd-114">Pixel shader versions</span></span>     | <span data-ttu-id="928cd-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="928cd-115">1\_1</span></span> | <span data-ttu-id="928cd-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="928cd-116">1\_2</span></span> | <span data-ttu-id="928cd-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="928cd-117">1\_3</span></span> | <span data-ttu-id="928cd-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="928cd-118">1\_4</span></span> | <span data-ttu-id="928cd-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="928cd-119">2\_0</span></span> | <span data-ttu-id="928cd-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="928cd-120">2\_sw</span></span> | <span data-ttu-id="928cd-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="928cd-121">2\_x</span></span> | <span data-ttu-id="928cd-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="928cd-122">3\_0</span></span> | <span data-ttu-id="928cd-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="928cd-123">3\_sw</span></span> |
|---------------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="928cd-124">Registro booliano constante</span><span class="sxs-lookup"><span data-stu-id="928cd-124">Constant Boolean register</span></span> |      |      |      |      |      |       | <span data-ttu-id="928cd-125">x</span><span class="sxs-lookup"><span data-stu-id="928cd-125">x</span></span>    | <span data-ttu-id="928cd-126">x</span><span class="sxs-lookup"><span data-stu-id="928cd-126">x</span></span>    | <span data-ttu-id="928cd-127">x</span><span class="sxs-lookup"><span data-stu-id="928cd-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="928cd-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="928cd-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="928cd-129">Register</span><span class="sxs-lookup"><span data-stu-id="928cd-129">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 