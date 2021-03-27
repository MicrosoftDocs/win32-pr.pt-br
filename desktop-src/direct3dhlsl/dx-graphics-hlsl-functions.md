---
title: Funções (referência de HLSL)
description: As funções encapsulam instruções HLSL.
ms.assetid: b6f934e5-eac7-4859-b1d0-698632011e1d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 59b0bfcb2079329d4d7ad7c02e7e5a326d22c236
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104293604"
---
# <a name="functions-hlsl-reference"></a><span data-ttu-id="5ce40-103">Funções (referência de HLSL)</span><span class="sxs-lookup"><span data-stu-id="5ce40-103">Functions (HLSL reference)</span></span>

<span data-ttu-id="5ce40-104">As funções encapsulam instruções HLSL.</span><span class="sxs-lookup"><span data-stu-id="5ce40-104">Functions encapsulate HLSL statements.</span></span> <span data-ttu-id="5ce40-105">Isso permite que você depure um conjunto de funções e, em seguida, reutilize-as em sombreadores ou efeitos.</span><span class="sxs-lookup"><span data-stu-id="5ce40-105">This enables you to debug a set of functions and then reuse them across shaders or effects.</span></span> <span data-ttu-id="5ce40-106">Talvez você queira criar uma função que encapsula a funcionalidade de um sombreador de vértice, sombreador de pixel ou sombreador de textura.</span><span class="sxs-lookup"><span data-stu-id="5ce40-106">You may want to create a function that encapsulates the functionality of a vertex shader, pixel shader or texture shader.</span></span> <span data-ttu-id="5ce40-107">Em outras ocasiões, convém escrever uma função auxiliar que executa uma tarefa comumente usada e, em seguida, chamar essa função auxiliar a partir de sua função de sombreador.</span><span class="sxs-lookup"><span data-stu-id="5ce40-107">Other times, you may want to write a helper function that performs some commonly used task, and then call that helper function from your shader function.</span></span> <span data-ttu-id="5ce40-108">As regras para escrever funções de sombreador para HLSL são muito parecidas com a gravação de funções de C.</span><span class="sxs-lookup"><span data-stu-id="5ce40-108">The rules for writing shader functions for HLSL are very similar to writing C functions.</span></span>

-   [<span data-ttu-id="5ce40-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ce40-109">Syntax</span></span>](dx-graphics-hlsl-function-syntax.md)
-   [<span data-ttu-id="5ce40-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ce40-110">Parameters</span></span>](dx-graphics-hlsl-function-parameters.md)
-   [<span data-ttu-id="5ce40-111">Instrução Return</span><span class="sxs-lookup"><span data-stu-id="5ce40-111">Return Statement</span></span>](dx-graphics-hlsl-return.md)
-   [<span data-ttu-id="5ce40-112">Assinaturas</span><span class="sxs-lookup"><span data-stu-id="5ce40-112">Signatures</span></span>](dx-graphics-hlsl-signatures.md)

<span data-ttu-id="5ce40-113">O HLSL também tem várias [**funções intrínsecas internas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md).</span><span class="sxs-lookup"><span data-stu-id="5ce40-113">HLSL also has a number of built-in [**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md).</span></span> <span data-ttu-id="5ce40-114">Como todas as funções intrínsecas são testadas e otimizadas para desempenho, é recomendável usar uma função intrínseca onde for possível, em vez de criar sua própria função.</span><span class="sxs-lookup"><span data-stu-id="5ce40-114">Because all intrinsic functions are tested and performance optimized, it is good practice to use an intrinsic function where possible instead of creating your own function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ce40-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5ce40-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ce40-116">Sintaxe de linguagem (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5ce40-116">Language Syntax (DirectX HLSL)</span></span>](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




