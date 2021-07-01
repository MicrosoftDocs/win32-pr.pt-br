---
title: Tipos de dados (HLSL)
description: O HLSL dá suporte a muitos tipos diferentes de dados intrínsecos. Esta tabela mostra quais tipos usar para definir variáveis de sombreador.
ms.assetid: e4b7738d-e865-4151-a204-0a5b88a913b3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c4cb8f6fd15db857daa3005c99381d437a5289f6
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129643"
---
# <a name="data-types-hlsl"></a><span data-ttu-id="42050-104">Tipos de dados (HLSL)</span><span class="sxs-lookup"><span data-stu-id="42050-104">Data Types (HLSL)</span></span>

<span data-ttu-id="42050-105">O HLSL dá suporte a muitos tipos diferentes de dados intrínsecos.</span><span class="sxs-lookup"><span data-stu-id="42050-105">HLSL supports many different intrinsic data types.</span></span> <span data-ttu-id="42050-106">Esta tabela mostra quais tipos usar para definir variáveis de sombreador.</span><span class="sxs-lookup"><span data-stu-id="42050-106">This table shows which types to use to define shader variables.</span></span>



| <span data-ttu-id="42050-107">Usar este tipo intrínseco</span><span class="sxs-lookup"><span data-stu-id="42050-107">Use this intrinsic type</span></span>                                                                                                                         | <span data-ttu-id="42050-108">Para definir essa variável de sombreador</span><span class="sxs-lookup"><span data-stu-id="42050-108">To define this shader variable</span></span>                                            |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [<span data-ttu-id="42050-109">Escalar</span><span class="sxs-lookup"><span data-stu-id="42050-109">Scalar</span></span>](dx-graphics-hlsl-scalar.md)                                                                                   | <span data-ttu-id="42050-110">Escalar de um componente</span><span class="sxs-lookup"><span data-stu-id="42050-110">One-component scalar</span></span>                       |
| <span data-ttu-id="42050-111">[Vetor](dx-graphics-hlsl-vector.md), [matriz](dx-graphics-hlsl-matrix.md)</span><span class="sxs-lookup"><span data-stu-id="42050-111">[Vector](dx-graphics-hlsl-vector.md), [Matrix](dx-graphics-hlsl-matrix.md)</span></span>                                            | <span data-ttu-id="42050-112">Vetor ou matriz de vários componentes</span><span class="sxs-lookup"><span data-stu-id="42050-112">Multiple-component vector or matrix</span></span>        |
| <span data-ttu-id="42050-113">[Amostra](dx-graphics-hlsl-sampler.md), [textura](dx-graphics-hlsl-texture.md) ou [buffer](dx-graphics-hlsl-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="42050-113">[Sampler](dx-graphics-hlsl-sampler.md), [Texture](dx-graphics-hlsl-texture.md) or [Buffer](dx-graphics-hlsl-buffer.md)</span></span>   | <span data-ttu-id="42050-114">Objeto de amostra, textura ou buffer</span><span class="sxs-lookup"><span data-stu-id="42050-114">Sampler, texture, or buffer object</span></span>         |
| <span data-ttu-id="42050-115">[Struct](dx-graphics-hlsl-struct.md), [definido pelo usuário](dx-graphics-hlsl-user-defined.md)</span><span class="sxs-lookup"><span data-stu-id="42050-115">[Struct](dx-graphics-hlsl-struct.md), [User Defined](dx-graphics-hlsl-user-defined.md)</span></span>                                | <span data-ttu-id="42050-116">Estrutura personalizada ou typedef</span><span class="sxs-lookup"><span data-stu-id="42050-116">Custom structure or typedef</span></span>                |
| <span data-ttu-id="42050-117">Array</span><span class="sxs-lookup"><span data-stu-id="42050-117">Array</span></span>                                                                                   | <span data-ttu-id="42050-118">Expressões escalares literais declaradas contendo a maioria dos outros tipos</span><span class="sxs-lookup"><span data-stu-id="42050-118">Literal scalar expressions declared containing most other types</span></span>                       |
| [<span data-ttu-id="42050-119">Objeto de estado</span><span class="sxs-lookup"><span data-stu-id="42050-119">State Object</span></span>](dx-graphics-hlsl-state-object.md) | <span data-ttu-id="42050-120">Representações de HLSL de objetos de estado</span><span class="sxs-lookup"><span data-stu-id="42050-120">HLSL representations of state objects</span></span> |


 

<span data-ttu-id="42050-121">Para ajudá-lo a entender melhor como usar vetores e matrizes no HLSL, talvez você queira ler essas informações básicas sobre como o HLSL usa a matemática [por componente](dx-graphics-hlsl-per-component-math.md) .</span><span class="sxs-lookup"><span data-stu-id="42050-121">To help you better understand how to use vectors and matrices in HLSL, you may want to read this background information on how HLSL uses [per-component](dx-graphics-hlsl-per-component-math.md) math.</span></span>

## <a name="related-topics"></a><span data-ttu-id="42050-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="42050-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42050-123">Variáveis (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="42050-123">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 




