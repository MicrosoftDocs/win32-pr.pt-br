---
description: Saiba mais sobre o suporte à função matemática em D3DX. D3DX é uma biblioteca de utilitários que fornece serviços auxiliares. É uma camada acima do componente Direct3D.
ms.assetid: a44d25de-f79d-4132-a75a-0c22ccd84341
title: Suporte à função matemática no D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a28c32b13d185694e4ffa41c314cf9f77cbb18b7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407519"
---
# <a name="math-function-support-in-d3dx-direct3d-9"></a><span data-ttu-id="e5cb2-105">Suporte à função matemática no D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e5cb2-105">Math Function Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="e5cb2-106">D3DX é uma biblioteca de utilitários que fornece serviços auxiliares.</span><span class="sxs-lookup"><span data-stu-id="e5cb2-106">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="e5cb2-107">É uma camada acima do componente Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e5cb2-107">It is a layer above the Direct3D component.</span></span>

## <a name="math"></a><span data-ttu-id="e5cb2-108">Matemática</span><span class="sxs-lookup"><span data-stu-id="e5cb2-108">Math</span></span>

<span data-ttu-id="e5cb2-109">O suporte matemático, contido em um conjunto de funções, é fornecido para:</span><span class="sxs-lookup"><span data-stu-id="e5cb2-109">Math support, contained in a set of functions, is provided for:</span></span>

-   <span data-ttu-id="e5cb2-110">Cálculos de cores</span><span class="sxs-lookup"><span data-stu-id="e5cb2-110">Color calculations</span></span>
-   <span data-ttu-id="e5cb2-111">Aviões</span><span class="sxs-lookup"><span data-stu-id="e5cb2-111">Planes</span></span>
-   <span data-ttu-id="e5cb2-112">Manipulação de matriz</span><span class="sxs-lookup"><span data-stu-id="e5cb2-112">Matrix manipulation</span></span>
-   <span data-ttu-id="e5cb2-113">Quaternions</span><span class="sxs-lookup"><span data-stu-id="e5cb2-113">Quaternions</span></span>
-   <span data-ttu-id="e5cb2-114">Vetores 2D</span><span class="sxs-lookup"><span data-stu-id="e5cb2-114">2D vectors</span></span>
-   <span data-ttu-id="e5cb2-115">Vetores 3D</span><span class="sxs-lookup"><span data-stu-id="e5cb2-115">3D vectors</span></span>
-   <span data-ttu-id="e5cb2-116">Vetores 4D</span><span class="sxs-lookup"><span data-stu-id="e5cb2-116">4D vectors</span></span>

<span data-ttu-id="e5cb2-117">Observe que, quando juntamente com as sobrecargas do C++, o suporte para tipos de matemática 3D básicos é extenso.</span><span class="sxs-lookup"><span data-stu-id="e5cb2-117">Please note that when coupled with the C++ overloads, the support for basic 3D math types is extensive.</span></span>

<span data-ttu-id="e5cb2-118">Para obter mais informações sobre essas funções, consulte [Funções D3DX](dx9-graphics-reference-d3dx-functions.md).</span><span class="sxs-lookup"><span data-stu-id="e5cb2-118">For more information about these functions, see [D3DX Functions](dx9-graphics-reference-d3dx-functions.md).</span></span> <span data-ttu-id="e5cb2-119">Para ajudar a encontrar a função de que você precisa, elas são divididas em várias pastas.</span><span class="sxs-lookup"><span data-stu-id="e5cb2-119">To help find the function you need, they are broken up in several folders.</span></span>

## <a name="float16"></a><span data-ttu-id="e5cb2-120">FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e5cb2-120">FLOAT16</span></span>

<span data-ttu-id="e5cb2-121">Ao usar o tipo de dados FLOAT16, certifique-se de limitar os valores a um máximo de D3DX \_ 16F \_ MAX.</span><span class="sxs-lookup"><span data-stu-id="e5cb2-121">When using the FLOAT16 data type, be sure to limit values to a maximum of D3DX\_16F\_MAX.</span></span> <span data-ttu-id="e5cb2-122">Qualquer valor FLOAT16 que exceder isso resultará em comportamento indefinido no pipeline.</span><span class="sxs-lookup"><span data-stu-id="e5cb2-122">Any FLOAT16 value that exceeds this will result in undefined behavior in the pipeline.</span></span> <span data-ttu-id="e5cb2-123">Consulte [Outras constantes D3DX.](other-d3dx-constants.md)</span><span class="sxs-lookup"><span data-stu-id="e5cb2-123">See [Other D3DX Constants](other-d3dx-constants.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5cb2-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e5cb2-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5cb2-125">D3dx</span><span class="sxs-lookup"><span data-stu-id="e5cb2-125">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 



