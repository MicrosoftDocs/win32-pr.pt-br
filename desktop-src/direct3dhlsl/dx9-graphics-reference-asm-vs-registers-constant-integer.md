---
title: Registro de inteiro constante (referência de HLSL VS)
description: Os registros inteiros constantes são usados somente por loop-vs e Rep-vs.
ms.assetid: da9916d4-655b-4c98-99a4-1abfa66459b5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4cf2612eccb891ce0cffd04955e4997173e84007
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967206"
---
# <a name="constant-integer-register-hlsl-vs-reference"></a><span data-ttu-id="16748-103">Registro de inteiro constante (referência de HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="16748-103">Constant Integer Register (HLSL VS reference)</span></span>

<span data-ttu-id="16748-104">Os registros inteiros constantes são usados somente por [loop-vs](loop---vs.md) e [Rep-vs](rep---vs.md).</span><span class="sxs-lookup"><span data-stu-id="16748-104">Constant integer registers are used only by [loop - vs](loop---vs.md) and [rep - vs](rep---vs.md).</span></span>

<span data-ttu-id="16748-105">Eles podem ser definidos usando [defi-vs](defi---vs.md) ou [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti).</span><span class="sxs-lookup"><span data-stu-id="16748-105">They can be set using [defi - vs](defi---vs.md) or [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti).</span></span>

<span data-ttu-id="16748-106">Quando usado como um argumento para a instrução [loop-vs](loop---vs.md) :</span><span class="sxs-lookup"><span data-stu-id="16748-106">When used as an argument to the [loop - vs](loop---vs.md) instruction:</span></span>

-   <span data-ttu-id="16748-107">. x é a contagem de iteração.</span><span class="sxs-lookup"><span data-stu-id="16748-107">.x is the iteration count.</span></span> <span data-ttu-id="16748-108">([Rep-vs](rep---vs.md) usa apenas este componente).</span><span class="sxs-lookup"><span data-stu-id="16748-108">([rep - vs](rep---vs.md) uses only this component).</span></span>
-   <span data-ttu-id="16748-109">. y é o valor inicial para o contador de loop.</span><span class="sxs-lookup"><span data-stu-id="16748-109">.y is the initial value for the loop counter.</span></span>
-   <span data-ttu-id="16748-110">. z é a etapa de incremento para o contador de loop.</span><span class="sxs-lookup"><span data-stu-id="16748-110">.z is the increment step for the loop counter.</span></span>

<span data-ttu-id="16748-111">O comportamento das constantes do sombreador foi alterado entre o Direct3D 8 e o Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="16748-111">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="16748-112">Para o Direct3D 9, as constantes definidas com defx atribuem valores ao espaço constante do sombreador.</span><span class="sxs-lookup"><span data-stu-id="16748-112">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="16748-113">O tempo de vida de uma constante declarada com defx é restrito apenas à execução desse sombreador.</span><span class="sxs-lookup"><span data-stu-id="16748-113">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="16748-114">Por outro lado, as constantes definidas usando as APIs SetXXXShaderConstantX inicializam constantes no espaço global.</span><span class="sxs-lookup"><span data-stu-id="16748-114">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="16748-115">As constantes no espaço global não são copiadas para o espaço local (visível para o sombreador) até que SetxxxShaderConstants seja chamado.</span><span class="sxs-lookup"><span data-stu-id="16748-115">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="16748-116">Para o Direct3D 8, as constantes definidas com defx ou as APIs atribuem valores ao espaço constante do sombreador.</span><span class="sxs-lookup"><span data-stu-id="16748-116">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="16748-117">Cada vez que o sombreador é executado, as constantes são usadas pelo sombreador atual, independentemente da técnica usada para defini-los.</span><span class="sxs-lookup"><span data-stu-id="16748-117">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="16748-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="16748-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16748-119">Registros de sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="16748-119">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 