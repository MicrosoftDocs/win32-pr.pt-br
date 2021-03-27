---
title: Registro temporário (referência do HLSL PS)
description: Os registros temporários de entrada do sombreador de pixel são usados para armazenar resultados intermediários.
ms.assetid: e61daaa1-0a9b-4b1c-b91c-56573be59ed9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7aebee99a693ac629d9cc8a372fba7589a9e29ef
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "103823476"
---
# <a name="temporary-register-hlsl-ps-reference"></a><span data-ttu-id="b96bf-103">Registro temporário (referência do HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="b96bf-103">Temporary register (HLSL PS reference)</span></span>

<span data-ttu-id="b96bf-104">Os registros temporários de entrada do sombreador de pixel são usados para armazenar resultados intermediários.</span><span class="sxs-lookup"><span data-stu-id="b96bf-104">Pixel shader input temporary registers are used to hold intermediate results.</span></span>

<span data-ttu-id="b96bf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b96bf-105">Syntax</span></span>


```
no declaration is required
```





| <span data-ttu-id="b96bf-106">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="b96bf-106">Pixel shader versions</span></span> | <span data-ttu-id="b96bf-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="b96bf-107">1\_1</span></span> | <span data-ttu-id="b96bf-108">1\_2</span><span class="sxs-lookup"><span data-stu-id="b96bf-108">1\_2</span></span> | <span data-ttu-id="b96bf-109">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b96bf-109">1\_3</span></span> | <span data-ttu-id="b96bf-110">1\_4</span><span class="sxs-lookup"><span data-stu-id="b96bf-110">1\_4</span></span> | <span data-ttu-id="b96bf-111">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b96bf-111">2\_0</span></span> | <span data-ttu-id="b96bf-112">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b96bf-112">2\_sw</span></span> | <span data-ttu-id="b96bf-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b96bf-113">2\_x</span></span> | <span data-ttu-id="b96bf-114">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b96bf-114">3\_0</span></span> | <span data-ttu-id="b96bf-115">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b96bf-115">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="b96bf-116">Registro temporário</span><span class="sxs-lookup"><span data-stu-id="b96bf-116">Temporary Register</span></span>    |      |      |      |      | <span data-ttu-id="b96bf-117">x</span><span class="sxs-lookup"><span data-stu-id="b96bf-117">x</span></span>    | <span data-ttu-id="b96bf-118">x</span><span class="sxs-lookup"><span data-stu-id="b96bf-118">x</span></span>     | <span data-ttu-id="b96bf-119">x</span><span class="sxs-lookup"><span data-stu-id="b96bf-119">x</span></span>    | <span data-ttu-id="b96bf-120">x</span><span class="sxs-lookup"><span data-stu-id="b96bf-120">x</span></span>    | <span data-ttu-id="b96bf-121">x</span><span class="sxs-lookup"><span data-stu-id="b96bf-121">x</span></span>     |



 

-   <span data-ttu-id="b96bf-122">Há 12 registros temporários de sombreador de pixel: R0 para R11.</span><span class="sxs-lookup"><span data-stu-id="b96bf-122">There are 12 pixel-shader temporary registers: r0 to r11.</span></span>
-   <span data-ttu-id="b96bf-123">Esses registros são usados para armazenar resultados intermediários durante cálculos.</span><span class="sxs-lookup"><span data-stu-id="b96bf-123">These registers are used for storing intermediate results during computations.</span></span>
-   <span data-ttu-id="b96bf-124">Se um registro temporário usar componentes que não estão definidos no código anterior, a validação do sombreador falhará.</span><span class="sxs-lookup"><span data-stu-id="b96bf-124">If a temporary register uses components that are not defined in previous code, shader validation will fail.</span></span>
-   <span data-ttu-id="b96bf-125">Essas são, pelo menos, a precisão de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="b96bf-125">These are at least floating-point precision.</span></span>
-   <span data-ttu-id="b96bf-126">Um máximo de três pode ser usado em uma única instrução.</span><span class="sxs-lookup"><span data-stu-id="b96bf-126">A maximum of three can be used in a single instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b96bf-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b96bf-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b96bf-128">Register</span><span class="sxs-lookup"><span data-stu-id="b96bf-128">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




