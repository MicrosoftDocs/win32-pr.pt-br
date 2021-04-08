---
description: D3DX é uma biblioteca de utilitários que fornece serviços auxiliares. É uma camada acima do componente do Direct3D.
ms.assetid: a44d25de-f79d-4132-a75a-0c22ccd84341
title: Suporte à função matemática no D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac69e0385919b015d1f8d3e7d47e221c06a04fbb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087591"
---
# <a name="math-function-support-in-d3dx-direct3d-9"></a><span data-ttu-id="0b7be-104">Suporte à função matemática no D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0b7be-104">Math Function Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="0b7be-105">D3DX é uma biblioteca de utilitários que fornece serviços auxiliares.</span><span class="sxs-lookup"><span data-stu-id="0b7be-105">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="0b7be-106">É uma camada acima do componente do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="0b7be-106">It is a layer above the Direct3D component.</span></span>

## <a name="math"></a><span data-ttu-id="0b7be-107">Matemática</span><span class="sxs-lookup"><span data-stu-id="0b7be-107">Math</span></span>

<span data-ttu-id="0b7be-108">O suporte a matemática, contido em um conjunto de funções, é fornecido para:</span><span class="sxs-lookup"><span data-stu-id="0b7be-108">Math support, contained in a set of functions, is provided for:</span></span>

-   <span data-ttu-id="0b7be-109">Cálculos de cores</span><span class="sxs-lookup"><span data-stu-id="0b7be-109">Color calculations</span></span>
-   <span data-ttu-id="0b7be-110">Aviões</span><span class="sxs-lookup"><span data-stu-id="0b7be-110">Planes</span></span>
-   <span data-ttu-id="0b7be-111">Manipulação de matriz</span><span class="sxs-lookup"><span data-stu-id="0b7be-111">Matrix manipulation</span></span>
-   <span data-ttu-id="0b7be-112">Os quatérnios</span><span class="sxs-lookup"><span data-stu-id="0b7be-112">Quaternions</span></span>
-   <span data-ttu-id="0b7be-113">vetores 2D</span><span class="sxs-lookup"><span data-stu-id="0b7be-113">2D vectors</span></span>
-   <span data-ttu-id="0b7be-114">vetores 3D</span><span class="sxs-lookup"><span data-stu-id="0b7be-114">3D vectors</span></span>
-   <span data-ttu-id="0b7be-115">vetores 4D</span><span class="sxs-lookup"><span data-stu-id="0b7be-115">4D vectors</span></span>

<span data-ttu-id="0b7be-116">Observe que, quando combinado com as sobrecargas de C++, o suporte para tipos de matemática 3D básico é extensivo.</span><span class="sxs-lookup"><span data-stu-id="0b7be-116">Please note that when coupled with the C++ overloads, the support for basic 3D math types is extensive.</span></span>

<span data-ttu-id="0b7be-117">Para obter mais informações sobre essas funções, consulte [D3DX Functions](dx9-graphics-reference-d3dx-functions.md).</span><span class="sxs-lookup"><span data-stu-id="0b7be-117">For more information about these functions, see [D3DX Functions](dx9-graphics-reference-d3dx-functions.md).</span></span> <span data-ttu-id="0b7be-118">Para ajudar a localizar a função de que você precisa, elas são divididas em várias pastas.</span><span class="sxs-lookup"><span data-stu-id="0b7be-118">To help find the function you need, they are broken up in several folders.</span></span>

## <a name="float16"></a><span data-ttu-id="0b7be-119">FLOAT16</span><span class="sxs-lookup"><span data-stu-id="0b7be-119">FLOAT16</span></span>

<span data-ttu-id="0b7be-120">Ao usar o tipo de dados FLOAT16, certifique-se de limitar os valores para um máximo de D3DX \_ 16F \_ Max.</span><span class="sxs-lookup"><span data-stu-id="0b7be-120">When using the FLOAT16 data type, be sure to limit values to a maximum of D3DX\_16F\_MAX.</span></span> <span data-ttu-id="0b7be-121">Qualquer valor de FLOAT16 que exceda isso resultará em um comportamento indefinido no pipeline.</span><span class="sxs-lookup"><span data-stu-id="0b7be-121">Any FLOAT16 value that exceeds this will result in undefined behavior in the pipeline.</span></span> <span data-ttu-id="0b7be-122">Consulte [outras constantes D3DX](other-d3dx-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0b7be-122">See [Other D3DX Constants](other-d3dx-constants.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b7be-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0b7be-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b7be-124">D3DX</span><span class="sxs-lookup"><span data-stu-id="0b7be-124">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 



