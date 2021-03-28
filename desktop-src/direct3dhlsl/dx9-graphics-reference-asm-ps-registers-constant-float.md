---
title: Registro float de constante (referência do HLSL PS)
description: Registro de entrada do sombreador de pixel para uma constante de ponto flutuante de 4D.
ms.assetid: e4f46a48-c81e-4105-901b-332b92fa6195
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05bb382b745d172ea4b81f9920154e7c79a58c2d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366450"
---
# <a name="constant-float-register-hlsl-ps-reference"></a><span data-ttu-id="b2d5a-103">Registro float de constante (referência do HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="b2d5a-103">Constant float register (HLSL PS reference)</span></span>

<span data-ttu-id="b2d5a-104">Registro de entrada do sombreador de pixel para uma constante de ponto flutuante de 4D.</span><span class="sxs-lookup"><span data-stu-id="b2d5a-104">Pixel shader input register for a 4D floating-point constant.</span></span>

<span data-ttu-id="b2d5a-105">Eles podem ser definidos usando [def-PS](def---ps.md) ou [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).</span><span class="sxs-lookup"><span data-stu-id="b2d5a-105">They can be set using [def - ps](def---ps.md) or [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).</span></span>

<span data-ttu-id="b2d5a-106">O comportamento das constantes do sombreador foi alterado entre o Direct3D 8 e o Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="b2d5a-106">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="b2d5a-107">Para o Direct3D 9, as constantes definidas com defx atribuem valores ao espaço constante do sombreador.</span><span class="sxs-lookup"><span data-stu-id="b2d5a-107">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="b2d5a-108">O tempo de vida de uma constante declarada com defx é restrito apenas à execução desse sombreador.</span><span class="sxs-lookup"><span data-stu-id="b2d5a-108">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="b2d5a-109">Por outro lado, as constantes definidas usando as APIs SetXXXShaderConstantX inicializam constantes no espaço global.</span><span class="sxs-lookup"><span data-stu-id="b2d5a-109">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="b2d5a-110">As constantes no espaço global não são copiadas para o espaço local (visível para o sombreador) até que SetxxxShaderConstants seja chamado.</span><span class="sxs-lookup"><span data-stu-id="b2d5a-110">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="b2d5a-111">Para o Direct3D 8, as constantes definidas com defx ou as APIs atribuem valores ao espaço constante do sombreador.</span><span class="sxs-lookup"><span data-stu-id="b2d5a-111">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="b2d5a-112">Cada vez que o sombreador é executado, as constantes são usadas pelo sombreador atual, independentemente da técnica usada para defini-los.</span><span class="sxs-lookup"><span data-stu-id="b2d5a-112">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="examples"></a><span data-ttu-id="b2d5a-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b2d5a-113">Examples</span></span>

<span data-ttu-id="b2d5a-114">Aqui está um exemplo declarando duas constantes de ponto flutuante em um sombreador.</span><span class="sxs-lookup"><span data-stu-id="b2d5a-114">Here is an example declaring two floating-point constants within a shader.</span></span>


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



<span data-ttu-id="b2d5a-115">Essas constantes são carregadas toda vez que [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader) é chamado.</span><span class="sxs-lookup"><span data-stu-id="b2d5a-115">These constants are loaded every time [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader) is called.</span></span>

<span data-ttu-id="b2d5a-116">Se você estiver definindo valores constantes com a API, não haverá nenhuma declaração de sombreador necessária.</span><span class="sxs-lookup"><span data-stu-id="b2d5a-116">If you are setting constant values with the API, there is no shader declaration required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2d5a-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b2d5a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2d5a-118">Register</span><span class="sxs-lookup"><span data-stu-id="b2d5a-118">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 