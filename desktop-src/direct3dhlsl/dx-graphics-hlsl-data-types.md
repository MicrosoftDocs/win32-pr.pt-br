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
ms.openlocfilehash: 8cee02e38180b903b235c32ebc2c7ca486777b20
ms.sourcegitcommit: 316ce582d9b972634a0521e0380e054e9cbb5bae
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/03/2021
ms.locfileid: "104989120"
---
# <a name="data-types-hlsl"></a><span data-ttu-id="03c36-104">Tipos de dados (HLSL)</span><span class="sxs-lookup"><span data-stu-id="03c36-104">Data Types (HLSL)</span></span>

<span data-ttu-id="03c36-105">O HLSL dá suporte a muitos tipos diferentes de dados intrínsecos.</span><span class="sxs-lookup"><span data-stu-id="03c36-105">HLSL supports many different intrinsic data types.</span></span> <span data-ttu-id="03c36-106">Esta tabela mostra quais tipos usar para definir variáveis de sombreador.</span><span class="sxs-lookup"><span data-stu-id="03c36-106">This table shows which types to use to define shader variables.</span></span>



|                                                                                                                         |                                            |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span data-ttu-id="03c36-107">Usar este tipo intrínseco</span><span class="sxs-lookup"><span data-stu-id="03c36-107">Use This Intrinsic Type</span></span>                                                                                                 | <span data-ttu-id="03c36-108">Para definir essa variável de sombreador</span><span class="sxs-lookup"><span data-stu-id="03c36-108">To Define This Shader Variable</span></span>             |
| [<span data-ttu-id="03c36-109">Único</span><span class="sxs-lookup"><span data-stu-id="03c36-109">Scalar</span></span>](dx-graphics-hlsl-scalar.md)                                                                                   | <span data-ttu-id="03c36-110">Escalar de um componente</span><span class="sxs-lookup"><span data-stu-id="03c36-110">One-component scalar</span></span>                       |
| <span data-ttu-id="03c36-111">[Vetor](dx-graphics-hlsl-vector.md), [matriz](dx-graphics-hlsl-matrix.md)</span><span class="sxs-lookup"><span data-stu-id="03c36-111">[Vector](dx-graphics-hlsl-vector.md), [Matrix](dx-graphics-hlsl-matrix.md)</span></span>                                            | <span data-ttu-id="03c36-112">Vetor ou matriz de vários componentes</span><span class="sxs-lookup"><span data-stu-id="03c36-112">Multiple-component vector or matrix</span></span>        |
| <span data-ttu-id="03c36-113">[Amostra](dx-graphics-hlsl-sampler.md), [textura](dx-graphics-hlsl-texture.md) ou [buffer](dx-graphics-hlsl-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="03c36-113">[Sampler](dx-graphics-hlsl-sampler.md), [Texture](dx-graphics-hlsl-texture.md) or [Buffer](dx-graphics-hlsl-buffer.md)</span></span>   | <span data-ttu-id="03c36-114">Objeto de amostra, textura ou buffer</span><span class="sxs-lookup"><span data-stu-id="03c36-114">Sampler, texture, or buffer object</span></span>         |
| <span data-ttu-id="03c36-115">[Struct](dx-graphics-hlsl-struct.md), [definido pelo usuário](dx-graphics-hlsl-user-defined.md)</span><span class="sxs-lookup"><span data-stu-id="03c36-115">[Struct](dx-graphics-hlsl-struct.md), [User Defined](dx-graphics-hlsl-user-defined.md)</span></span>                                | <span data-ttu-id="03c36-116">Estrutura personalizada ou typedef</span><span class="sxs-lookup"><span data-stu-id="03c36-116">Custom structure or typedef</span></span>                |
| <span data-ttu-id="03c36-117">Array</span><span class="sxs-lookup"><span data-stu-id="03c36-117">Array</span></span>                                                                                   | <span data-ttu-id="03c36-118">Expressões escalares literais declaradas contendo a maioria dos outros tipos</span><span class="sxs-lookup"><span data-stu-id="03c36-118">Literal scalar expressions declared containing most other types</span></span>                       |
| [<span data-ttu-id="03c36-119">Objeto de estado</span><span class="sxs-lookup"><span data-stu-id="03c36-119">State Object</span></span>](dx-graphics-hlsl-state-object.md) | <span data-ttu-id="03c36-120">Representações de HLSL de objetos de estado</span><span class="sxs-lookup"><span data-stu-id="03c36-120">HLSL representations of state objects</span></span> |


 

<span data-ttu-id="03c36-121">Para ajudá-lo a entender melhor como usar vetores e matrizes no HLSL, talvez você queira ler essas informações básicas sobre como o HLSL usa a matemática [por componente](dx-graphics-hlsl-per-component-math.md) .</span><span class="sxs-lookup"><span data-stu-id="03c36-121">To help you better understand how to use vectors and matrices in HLSL, you may want to read this background information on how HLSL uses [per-component](dx-graphics-hlsl-per-component-math.md) math.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03c36-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="03c36-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03c36-123">Variáveis (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="03c36-123">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 




