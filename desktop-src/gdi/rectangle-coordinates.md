---
description: Um aplicativo deve usar uma estrutura RECT para definir um retângulo.
ms.assetid: 93c63dcb-6c8e-4c8b-aa19-6f8952d75e2e
title: Coordenadas de retângulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8a3fbc3f42c6d69a3d0eac6555b85fbfc1eecb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988788"
---
# <a name="rectangle-coordinates"></a><span data-ttu-id="a468e-103">Coordenadas de retângulo</span><span class="sxs-lookup"><span data-stu-id="a468e-103">Rectangle Coordinates</span></span>

<span data-ttu-id="a468e-104">Um aplicativo deve usar uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) para definir um retângulo.</span><span class="sxs-lookup"><span data-stu-id="a468e-104">An application must use a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to define a rectangle.</span></span> <span data-ttu-id="a468e-105">A estrutura especifica as coordenadas de dois pontos: os cantos superior esquerdo e inferior direito do retângulo.</span><span class="sxs-lookup"><span data-stu-id="a468e-105">The structure specifies the coordinates of two points: the upper left and lower right corners of the rectangle.</span></span> <span data-ttu-id="a468e-106">Os lados do retângulo se estendem desses dois pontos e são paralelos aos eixos x e y.</span><span class="sxs-lookup"><span data-stu-id="a468e-106">The sides of the rectangle extend from these two points and are parallel to the x-axis and y-axis.</span></span>

<span data-ttu-id="a468e-107">Os valores de coordenadas para um retângulo são expressos como inteiros assinados.</span><span class="sxs-lookup"><span data-stu-id="a468e-107">The coordinate values for a rectangle are expressed as signed integers.</span></span> <span data-ttu-id="a468e-108">O valor da coordenada do lado direito de um retângulo deve ser maior do que o do lado esquerdo.</span><span class="sxs-lookup"><span data-stu-id="a468e-108">The coordinate value of a rectangle's right side must be greater than that of its left side.</span></span> <span data-ttu-id="a468e-109">Da mesma forma, o valor da coordenada da parte inferior deve ser maior que o da parte superior.</span><span class="sxs-lookup"><span data-stu-id="a468e-109">Likewise, the coordinate value of the bottom must be greater than that of the top.</span></span>

<span data-ttu-id="a468e-110">Como os aplicativos podem usar retângulos para muitas finalidades diferentes, as funções de retângulo não usam uma unidade de medida explícita.</span><span class="sxs-lookup"><span data-stu-id="a468e-110">Because applications can use rectangles for many different purposes, the rectangle functions do not use an explicit unit of measure.</span></span> <span data-ttu-id="a468e-111">Em vez disso, todas as coordenadas e dimensões de retângulo são dadas em valores lógicos assinados.</span><span class="sxs-lookup"><span data-stu-id="a468e-111">Instead, all rectangle coordinates and dimensions are given in signed, logical values.</span></span> <span data-ttu-id="a468e-112">O modo de mapeamento e a função na qual o retângulo é usado determinam as unidades de medida.</span><span class="sxs-lookup"><span data-stu-id="a468e-112">The mapping mode and the function in which the rectangle is used determine the units of measure.</span></span> <span data-ttu-id="a468e-113">Para obter mais informações sobre os modos de coordenadas e de mapeamento, consulte [espaços de coordenadas e transformações](coordinate-spaces-and-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="a468e-113">For more information about coordinates and mapping modes, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).</span></span>

 

 
