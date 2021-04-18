---
description: Lista as funções de plano fornecidas pelo DirectXMath.
ms.assetid: 6505e72e-4af5-5db3-4fc0-f83fa77692b1
title: Funções de plano de biblioteca DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b3f450b4dbaa5ed1b4348ad8b090210c14e2022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768217"
---
# <a name="directxmath-library-plane-functions"></a><span data-ttu-id="62bfa-103">Funções de plano de biblioteca DirectXMath</span><span class="sxs-lookup"><span data-stu-id="62bfa-103">DirectXMath Library plane functions</span></span>

<span data-ttu-id="62bfa-104">Lista as funções de plano fornecidas pelo DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="62bfa-104">Lists the plane functions provided by DirectXMath.</span></span>

<span data-ttu-id="62bfa-105">Essas funções usam um XMVECTOR 4-vector para representar os coeficientes da equação de plano, ax + by + cz + D = 0, em que o componente X é um, o componente Y é B, o Z-Component é C e o W-Component é D.</span><span class="sxs-lookup"><span data-stu-id="62bfa-105">These functions use an XMVECTOR 4-vector to represent the coefficients of the plane equation, Ax+By+Cz+D = 0, where the X-component is A, the Y-component is B, the Z-component is C, and the W-component is D.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="62bfa-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="62bfa-106">In this section</span></span>



| <span data-ttu-id="62bfa-107">Tópico</span><span class="sxs-lookup"><span data-stu-id="62bfa-107">Topic</span></span>                                                               | <span data-ttu-id="62bfa-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="62bfa-108">Description</span></span>                                                                                                      |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62bfa-109">**XMPlaneDot**</span><span class="sxs-lookup"><span data-stu-id="62bfa-109">**XMPlaneDot**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanedot)<br/>                         | <span data-ttu-id="62bfa-110">Calcula o produto de ponto entre um plano de entrada e um vetor 4D.</span><span class="sxs-lookup"><span data-stu-id="62bfa-110">Calculates the dot product between an input plane and a 4D vector.</span></span><br/>                                    |
| [<span data-ttu-id="62bfa-111">**XMPlaneDotCoord**</span><span class="sxs-lookup"><span data-stu-id="62bfa-111">**XMPlaneDotCoord**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanedotcoord)<br/>               | <span data-ttu-id="62bfa-112">Calcula o produto de ponto entre um plano de entrada e um vetor 3D.</span><span class="sxs-lookup"><span data-stu-id="62bfa-112">Calculates the dot product between an input plane and a 3D vector.</span></span><br/>                                    |
| [<span data-ttu-id="62bfa-113">**XMPlaneDotNormal**</span><span class="sxs-lookup"><span data-stu-id="62bfa-113">**XMPlaneDotNormal**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanedotnormal)<br/>             | <span data-ttu-id="62bfa-114">Calcula o produto de ponto entre o vetor normal de um plano e um vetor 3D.</span><span class="sxs-lookup"><span data-stu-id="62bfa-114">Calculates the dot product between the normal vector of a plane and a 3D vector.</span></span><br/>                      |
| [<span data-ttu-id="62bfa-115">**XMPlaneEqual**</span><span class="sxs-lookup"><span data-stu-id="62bfa-115">**XMPlaneEqual**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneequal)<br/>                     | <span data-ttu-id="62bfa-116">Determina se dois planos são iguais.</span><span class="sxs-lookup"><span data-stu-id="62bfa-116">Determines if two planes are equal.</span></span><br/>                                                                   |
| [<span data-ttu-id="62bfa-117">**XMPlaneFromPointNormal**</span><span class="sxs-lookup"><span data-stu-id="62bfa-117">**XMPlaneFromPointNormal**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompointnormal)<br/> | <span data-ttu-id="62bfa-118">Computa a equação de um plano construído a partir de um ponto no plano e um vetor normal.</span><span class="sxs-lookup"><span data-stu-id="62bfa-118">Computes the equation of a plane constructed from a point in the plane and a normal vector.</span></span><br/>           |
| [<span data-ttu-id="62bfa-119">**XMPlaneFromPoints**</span><span class="sxs-lookup"><span data-stu-id="62bfa-119">**XMPlaneFromPoints**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompoints)<br/>           | <span data-ttu-id="62bfa-120">Computa a equação de um plano construído a partir de três pontos no plano.</span><span class="sxs-lookup"><span data-stu-id="62bfa-120">Computes the equation of a plane constructed from three points in the plane.</span></span><br/>                          |
| [<span data-ttu-id="62bfa-121">**XMPlaneIntersectLine**</span><span class="sxs-lookup"><span data-stu-id="62bfa-121">**XMPlaneIntersectLine**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectline)<br/>     | <span data-ttu-id="62bfa-122">Localiza a interseção entre um plano e uma linha.</span><span class="sxs-lookup"><span data-stu-id="62bfa-122">Finds the intersection between a plane and a line.</span></span><br/>                                                    |
| [<span data-ttu-id="62bfa-123">**XMPlaneIntersectPlane**</span><span class="sxs-lookup"><span data-stu-id="62bfa-123">**XMPlaneIntersectPlane**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectplane)<br/>   | <span data-ttu-id="62bfa-124">Localiza a interseção de dois planos.</span><span class="sxs-lookup"><span data-stu-id="62bfa-124">Finds the intersection of two planes.</span></span><br/>                                                                 |
| [<span data-ttu-id="62bfa-125">**XMPlaneIsInfinite**</span><span class="sxs-lookup"><span data-stu-id="62bfa-125">**XMPlaneIsInfinite**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneisinfinite)<br/>           | <span data-ttu-id="62bfa-126">Testa se algum dos coeficientes de um plano é infinito positivo ou negativo.</span><span class="sxs-lookup"><span data-stu-id="62bfa-126">Tests whether any of the coefficients of a plane is positive or negative infinity.</span></span><br/>                    |
| [<span data-ttu-id="62bfa-127">**XMPlaneIsNaN**</span><span class="sxs-lookup"><span data-stu-id="62bfa-127">**XMPlaneIsNaN**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneisnan)<br/>                     | <span data-ttu-id="62bfa-128">Testa se qualquer um dos coeficientes de um plano é um NaN.</span><span class="sxs-lookup"><span data-stu-id="62bfa-128">Tests whether any of the coefficients of a plane is a NaN.</span></span><br/>                                            |
| [<span data-ttu-id="62bfa-129">**XMPlaneNearEqual**</span><span class="sxs-lookup"><span data-stu-id="62bfa-129">**XMPlaneNearEqual**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenearequal)<br/>             | <span data-ttu-id="62bfa-130">Determina se dois planos são quase iguais.</span><span class="sxs-lookup"><span data-stu-id="62bfa-130">Determines whether two planes are nearly equal.</span></span><br/>                                                       |
| [<span data-ttu-id="62bfa-131">**XMPlaneNormalize**</span><span class="sxs-lookup"><span data-stu-id="62bfa-131">**XMPlaneNormalize**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalize)<br/>             | <span data-ttu-id="62bfa-132">Normaliza os coeficientes de um plano para que os coeficientes de x, y e z formarem um vetor normal de unidade.</span><span class="sxs-lookup"><span data-stu-id="62bfa-132">Normalizes the coefficients of a plane so that coefficients of x, y, and z form a unit normal vector.</span></span><br/> |
| [<span data-ttu-id="62bfa-133">**XMPlaneNormalizeEst**</span><span class="sxs-lookup"><span data-stu-id="62bfa-133">**XMPlaneNormalizeEst**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalizeest)<br/>       | <span data-ttu-id="62bfa-134">Estima os coeficientes de um plano para que os coeficientes de x, y e z formarem um vetor normal de unidade.</span><span class="sxs-lookup"><span data-stu-id="62bfa-134">Estimates the coefficients of a plane so that coefficients of x, y, and z form a unit normal vector.</span></span><br/>  |
| [<span data-ttu-id="62bfa-135">**XMPlaneNotEqual**</span><span class="sxs-lookup"><span data-stu-id="62bfa-135">**XMPlaneNotEqual**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenotequal)<br/>               | <span data-ttu-id="62bfa-136">Determina se dois planos são desiguais.</span><span class="sxs-lookup"><span data-stu-id="62bfa-136">Determines if two planes are unequal.</span></span><br/>                                                                 |
| [<span data-ttu-id="62bfa-137">**XMPlaneTransform**</span><span class="sxs-lookup"><span data-stu-id="62bfa-137">**XMPlaneTransform**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanetransform)<br/>             | <span data-ttu-id="62bfa-138">Transforma um plano por uma determinada matriz.</span><span class="sxs-lookup"><span data-stu-id="62bfa-138">Transforms a plane by a given matrix.</span></span><br/>                                                                 |
| [<span data-ttu-id="62bfa-139">**XMPlaneTransformStream**</span><span class="sxs-lookup"><span data-stu-id="62bfa-139">**XMPlaneTransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanetransformstream)<br/> | <span data-ttu-id="62bfa-140">Transforma um fluxo de planos por uma determinada matriz.</span><span class="sxs-lookup"><span data-stu-id="62bfa-140">Transforms a stream of planes by a given matrix.</span></span><br/>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="62bfa-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="62bfa-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62bfa-142">Funções de biblioteca DirectXMath</span><span class="sxs-lookup"><span data-stu-id="62bfa-142">DirectXMath Library Functions</span></span>](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 
