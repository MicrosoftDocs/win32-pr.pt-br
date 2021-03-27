---
title: Registro booliano constante (referência de HLSL VS)
description: Esse registro é uma coleção de bits usada em instruções de controle de fluxo estático (por exemplo, se bool-vs-else-vs-endif-vs).
ms.assetid: bd02d03b-c228-481a-9c98-7442be4cdd07
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9b32841f060a29fce2918daca8f8fd008529bef1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967200"
---
# <a name="constant-boolean-register-hlsl-vs-reference"></a><span data-ttu-id="901e0-103">Registro booliano constante (referência de HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="901e0-103">Constant Boolean register (HLSL VS reference)</span></span>

<span data-ttu-id="901e0-104">Esse registro é uma coleção de bits usada em instruções de controle de fluxo estático (por exemplo, [se bool-vs](if-bool---vs.md)  -  [else-vs](else---vs.md), x  -  [](endif---vs.md)).</span><span class="sxs-lookup"><span data-stu-id="901e0-104">This register is a collection of bits used in static flow control instructions (for example, [if bool - vs](if-bool---vs.md) - [else - vs](else---vs.md) - [endif - vs](endif---vs.md)).</span></span> <span data-ttu-id="901e0-105">Há 16 deles, portanto, um sombreador pode ter 16 condições de ramificação independentes.</span><span class="sxs-lookup"><span data-stu-id="901e0-105">There are 16 of them, therefore, a shader can have 16 independent branch conditions.</span></span> <span data-ttu-id="901e0-106">Eles podem ser definidos usando [DEFB-vs](defb---vs.md) ou [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb).</span><span class="sxs-lookup"><span data-stu-id="901e0-106">They can be set using [defb - vs](defb---vs.md) or [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb).</span></span>

<span data-ttu-id="901e0-107">O comportamento das constantes do sombreador foi alterado entre o Direct3D 8 e o Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="901e0-107">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="901e0-108">Para o Direct3D 9, as constantes definidas com defx atribuem valores ao espaço constante do sombreador.</span><span class="sxs-lookup"><span data-stu-id="901e0-108">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="901e0-109">O tempo de vida de uma constante declarada com defx é restrito apenas à execução desse sombreador.</span><span class="sxs-lookup"><span data-stu-id="901e0-109">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="901e0-110">Por outro lado, as constantes definidas usando as APIs SetXXXShaderConstantX inicializam constantes no espaço global.</span><span class="sxs-lookup"><span data-stu-id="901e0-110">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="901e0-111">As constantes no espaço global não são copiadas para o espaço local (visível para o sombreador) até que SetxxxShaderConstants seja chamado.</span><span class="sxs-lookup"><span data-stu-id="901e0-111">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="901e0-112">Para o Direct3D 8, as constantes definidas com defx ou as APIs atribuem valores ao espaço constante do sombreador.</span><span class="sxs-lookup"><span data-stu-id="901e0-112">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="901e0-113">Cada vez que o sombreador é executado, as constantes são usadas pelo sombreador atual, independentemente da técnica usada para defini-los.</span><span class="sxs-lookup"><span data-stu-id="901e0-113">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="901e0-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="901e0-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="901e0-115">Registros de sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="901e0-115">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 