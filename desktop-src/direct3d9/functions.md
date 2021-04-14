---
description: Uma função é o bloco de construção de um sombreador criado na linguagem de alto nível. Se você preferir escrever sombreadores em uma linguagem em estilo C em vez de em linguagem de assembly, convém escrever funções.
ms.assetid: vs|directx_sdk|~\functions.htm
title: Sintaxe da função de efeito (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21e239359877813e64acea8b5f404a6ade59c992
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500264"
---
# <a name="effect-function-syntax-direct3d-9"></a><span data-ttu-id="8261d-104">Sintaxe da função de efeito (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8261d-104">Effect Function Syntax (Direct3D 9)</span></span>

<span data-ttu-id="8261d-105">Uma função é o bloco de construção de um sombreador criado na linguagem de alto nível.</span><span class="sxs-lookup"><span data-stu-id="8261d-105">A function is the building block for a shader created in the high-level language.</span></span> <span data-ttu-id="8261d-106">Se você preferir escrever sombreadores em uma linguagem em estilo C em vez de em linguagem de assembly, convém escrever funções.</span><span class="sxs-lookup"><span data-stu-id="8261d-106">If you prefer to write shaders in a C-style language instead of in assembly language, you will want to write functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="8261d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8261d-107">Syntax</span></span>


```
type id ( [ parameters ] )  
    { body }
```



<span data-ttu-id="8261d-108">As funções não alteram valores de parâmetro em um efeito.</span><span class="sxs-lookup"><span data-stu-id="8261d-108">Functions do not change parameter values in an effect.</span></span>

-   <span data-ttu-id="8261d-109">tipo-qualquer [referência válida para](../direct3dhlsl/dx-graphics-hlsl-reference.md) o tipo HLSL.</span><span class="sxs-lookup"><span data-stu-id="8261d-109">type - Any valid [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) type.</span></span>
-   <span data-ttu-id="8261d-110">ID-um nome exclusivo.</span><span class="sxs-lookup"><span data-stu-id="8261d-110">id - A unique name.</span></span>
-   <span data-ttu-id="8261d-111">parâmetros-parâmetros de função.</span><span class="sxs-lookup"><span data-stu-id="8261d-111">parameters - Function parameters.</span></span>
-   <span data-ttu-id="8261d-112">corpo-o corpo da função.</span><span class="sxs-lookup"><span data-stu-id="8261d-112">body - The body of the function.</span></span>

<span data-ttu-id="8261d-113">As funções são criadas a partir da linguagem de alto nível.</span><span class="sxs-lookup"><span data-stu-id="8261d-113">Functions are built from the high-level language.</span></span> <span data-ttu-id="8261d-114">Consulte [a referência para HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md).</span><span class="sxs-lookup"><span data-stu-id="8261d-114">See [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8261d-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8261d-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8261d-116">Formato do efeito</span><span class="sxs-lookup"><span data-stu-id="8261d-116">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
