---
description: Curvas de parâmetro
ms.assetid: c073e7d0-c119-4c36-a5b2-b31dd6326ac8
title: Curvas de parâmetro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3c482112c8bd76217f5cbdabdf3cda13b09c3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087771"
---
# <a name="parameter-curves"></a><span data-ttu-id="a42e4-103">Curvas de parâmetro</span><span class="sxs-lookup"><span data-stu-id="a42e4-103">Parameter Curves</span></span>

<span data-ttu-id="a42e4-104">Os parâmetros de mídia podem seguir uma curva ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="a42e4-104">Media parameters are able to follow a curve over time.</span></span> <span data-ttu-id="a42e4-105">Cada curva é descrita por uma fórmula matemática e dois pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="a42e4-105">Each curve is described by a mathematical formula and two end-points.</span></span> <span data-ttu-id="a42e4-106">Cada ponto de extremidade é definido por um tempo de referência e o valor da curva nesse momento.</span><span class="sxs-lookup"><span data-stu-id="a42e4-106">Each end-point is defined by a reference time and the value of the curve at that time.</span></span> <span data-ttu-id="a42e4-107">A fórmula é usada para calcular valores intermediários entre os pontos e determina a forma da curva.</span><span class="sxs-lookup"><span data-stu-id="a42e4-107">The formula is used to calculate intermediate values between the points, and determines the shape of the curve.</span></span> <span data-ttu-id="a42e4-108">As curvas possíveis são:</span><span class="sxs-lookup"><span data-stu-id="a42e4-108">The possible curves are:</span></span>

-   <span data-ttu-id="a42e4-109">Relacionados</span><span class="sxs-lookup"><span data-stu-id="a42e4-109">Jump</span></span>
-   <span data-ttu-id="a42e4-110">Linear</span><span class="sxs-lookup"><span data-stu-id="a42e4-110">Linear</span></span>
-   <span data-ttu-id="a42e4-111">Square</span><span class="sxs-lookup"><span data-stu-id="a42e4-111">Square</span></span>
-   <span data-ttu-id="a42e4-112">Quadrado inverso</span><span class="sxs-lookup"><span data-stu-id="a42e4-112">Inverse square</span></span>
-   <span data-ttu-id="a42e4-113">Seno</span><span class="sxs-lookup"><span data-stu-id="a42e4-113">Sine</span></span>

<span data-ttu-id="a42e4-114">"Salto" significa saltar diretamente para o valor final.</span><span class="sxs-lookup"><span data-stu-id="a42e4-114">"Jump" means jump directly to the end value.</span></span> <span data-ttu-id="a42e4-115">As outras curvas são mostradas no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="a42e4-115">The other curves are shown in the following diagram.</span></span>

![curvas de parâmetro](images/param-curves01.png)

<span data-ttu-id="a42e4-117">Matematicamente, as curvas funcionam da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="a42e4-117">Mathematically, the curves work as follows.</span></span> <span data-ttu-id="a42e4-118">Suponha que uma curva comece no tempo *t*₀ com um valor de *v*₀ e termine no time *t*₁ com um valor de *v*₁.</span><span class="sxs-lookup"><span data-stu-id="a42e4-118">Suppose that a curve begins at time *t*₀ with a value of *v*₀, and ends at time *t*₁ with a value of *v*₁.</span></span> <span data-ttu-id="a42e4-119">Os dois pontos que definem a curva são (*t*₀, *v*₀) e (*t*₁, *v*₁).</span><span class="sxs-lookup"><span data-stu-id="a42e4-119">The two points that define the curve are (*t*₀, *v*₀) and (*t*₁, *v*₁).</span></span>

-   <span data-ttu-id="a42e4-120">Deixe que Δ *t* seja a duração total da curva, *t*₁ –*t*₀.</span><span class="sxs-lookup"><span data-stu-id="a42e4-120">Let Δ *t* be the total duration of the curve, *t*₁–*t*₀.</span></span>
-   <span data-ttu-id="a42e4-121">Deixe que Δ *v* seja o intervalo entre os valores inicial e final, *v*₁ –*v*₀.</span><span class="sxs-lookup"><span data-stu-id="a42e4-121">Let Δ *v* be the interval between the starting and ending values, *v*₁–*v*₀.</span></span>
-   <span data-ttu-id="a42e4-122">A qualquer momento, *t* ₀ *<*= *t*  <=  *t*₁, deixe Δ *t*' = *t*–*t*₀.</span><span class="sxs-lookup"><span data-stu-id="a42e4-122">At any time *t* such that *t*₀ <= *t* <= *t*₁, let Δ *t*' = *t*–*t*₀.</span></span>

![cálculo de parâmetro](images/param-curves02.png)

<span data-ttu-id="a42e4-124">O valor do parâmetro na hora *t* é:</span><span class="sxs-lookup"><span data-stu-id="a42e4-124">The value of the parameter at time *t* is:</span></span>

<span data-ttu-id="a42e4-125">*v* = f (Δ *t*'/Δ *t* ) \* Δ *v*  +  *v*₀</span><span class="sxs-lookup"><span data-stu-id="a42e4-125">*v* = f( Δ *t*' / Δ *t* ) \* Δ *v* + *v*₀</span></span>

<span data-ttu-id="a42e4-126">em que f (x) é uma função determinada pelo tipo de curva:</span><span class="sxs-lookup"><span data-stu-id="a42e4-126">where f(x) is a function determined by the curve type:</span></span>

-   <span data-ttu-id="a42e4-127">Linear: y = x</span><span class="sxs-lookup"><span data-stu-id="a42e4-127">Linear: y = x</span></span>
-   <span data-ttu-id="a42e4-128">Quadrado: y = x ^ 2</span><span class="sxs-lookup"><span data-stu-id="a42e4-128">Square: y = x^2</span></span>
-   <span data-ttu-id="a42e4-129">Quadrado inverso: y = sqrt (x)</span><span class="sxs-lookup"><span data-stu-id="a42e4-129">Inverse square: y = sqrt(x)</span></span>
-   <span data-ttu-id="a42e4-130">Seno: y = \[ sin (Πx – π/2) + 1 \] /2</span><span class="sxs-lookup"><span data-stu-id="a42e4-130">Sine: y = \[ sin(πx – π/2) + 1 \] / 2</span></span>

<span data-ttu-id="a42e4-131">Observe que Δ *t*' < Δ *t*, portanto, o termo Δ *t*'/Δ *t* varia de 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="a42e4-131">Observe that Δ *t*' < Δ *t*, so the term Δ *t*'/Δ *t* ranges from 0 to 1.</span></span> <span data-ttu-id="a42e4-132">Portanto, f (x) também varia de 0 a 1 e *v* sempre cai entre *v*₀ e *v*₁.</span><span class="sxs-lookup"><span data-stu-id="a42e4-132">Therefore, f(x) also ranges from 0 to 1, and *v* always falls between *v*₀ and *v*₁.</span></span> <span data-ttu-id="a42e4-133">Isso é verdadeiro se *v*₀ < *v*₁ ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="a42e4-133">This is true whether *v*₀ < *v*₁ or vice versa.</span></span> <span data-ttu-id="a42e4-134">Em outras palavras, a curva é limitada pelo retângulo (*t*₀, *v*₀, *t*₁, *v*₁).</span><span class="sxs-lookup"><span data-stu-id="a42e4-134">In other words, the curve is bounded by the rectangle (*t*₀, *v*₀, *t*₁, *v*₁).</span></span>

<span data-ttu-id="a42e4-135">Para a curva senoidal, o valor de (Πx – π/2) varia de – π/2 a π/2, o que significa que o sin (Πx – π/2) varia de – 1 a 1.</span><span class="sxs-lookup"><span data-stu-id="a42e4-135">For the sine curve, the value of (πx – π/2) ranges from –π/2 to π/2, which means that sin(πx – π/2) ranges from –1 to 1.</span></span> <span data-ttu-id="a42e4-136">O resultado é normalizado para que f (x) se encaixe no intervalo (0 – 1).</span><span class="sxs-lookup"><span data-stu-id="a42e4-136">The result is then normalized so that f(x) falls into the range (0–1).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a42e4-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a42e4-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a42e4-138">Parâmetros de mídia</span><span class="sxs-lookup"><span data-stu-id="a42e4-138">Media Parameters</span></span>](media-parameters.md)
</dt> </dl>

 

 



