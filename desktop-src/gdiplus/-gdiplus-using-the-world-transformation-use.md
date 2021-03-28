---
description: A transformação do mundo é uma propriedade da classe Graphics.
ms.assetid: 22f43b29-ea7b-4faf-9795-2242bf704ed3
title: Usando a transformação global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2138df1bbd2be6d3329695fc6898da49da93b3b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164443"
---
# <a name="using-the-world-transformation"></a><span data-ttu-id="fd8e7-103">Usando a transformação global</span><span class="sxs-lookup"><span data-stu-id="fd8e7-103">Using the World Transformation</span></span>

<span data-ttu-id="fd8e7-104">A transformação do mundo é uma propriedade da classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="fd8e7-104">The world transformation is a property of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="fd8e7-105">Os números que especificam a transformação do mundo são armazenados em um objeto [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) , que representa uma matriz 3 × 3.</span><span class="sxs-lookup"><span data-stu-id="fd8e7-105">The numbers that specify the world transformation are stored in a [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) object, which represents a 3 ×3 matrix.</span></span> <span data-ttu-id="fd8e7-106">As classes **Matrix** e **Graphics** têm vários métodos para definir os números na matriz de transformação mundial.</span><span class="sxs-lookup"><span data-stu-id="fd8e7-106">The **Matrix** and **Graphics** classes have several methods for setting the numbers in the world transformation matrix.</span></span> <span data-ttu-id="fd8e7-107">Os exemplos nesta seção manipulam retângulos porque os retângulos são fáceis de desenhar e é fácil ver os efeitos das transformações em retângulos.</span><span class="sxs-lookup"><span data-stu-id="fd8e7-107">The examples in this section manipulate rectangles because rectangles are easy to draw and it is easy to see the effects of transformations on rectangles.</span></span>

<span data-ttu-id="fd8e7-108">Começamos criando um retângulo de 50 por 50 e localizando-o na origem (0, 0).</span><span class="sxs-lookup"><span data-stu-id="fd8e7-108">We start by creating a 50 by 50 rectangle and locating it at the origin (0, 0).</span></span> <span data-ttu-id="fd8e7-109">A origem está localizada no canto superior esquerdo da área de cliente.</span><span class="sxs-lookup"><span data-stu-id="fd8e7-109">The origin is at the upper-left corner of the client area.</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="fd8e7-110">O código a seguir aplica uma transformação de escala que expande o retângulo por um fator de 1,75 na direção x e encolhe o retângulo por um fator de 0,5 na direção y:</span><span class="sxs-lookup"><span data-stu-id="fd8e7-110">The following code applies a scaling transformation that expands the rectangle by a factor of 1.75 in the x direction and shrinks the rectangle by a factor of 0.5 in the y direction:</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="fd8e7-111">O resultado é um retângulo que é maior na direção x e menor na direção y que o original.</span><span class="sxs-lookup"><span data-stu-id="fd8e7-111">The result is a rectangle that is longer in the x direction and shorter in the y direction than the original.</span></span>

<span data-ttu-id="fd8e7-112">Para girar o retângulo em vez de dimensioná-lo, use o código a seguir em vez do código anterior:</span><span class="sxs-lookup"><span data-stu-id="fd8e7-112">To rotate the rectangle instead of scaling it, use the following code instead of the preceding code:</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.RotateTransform(28.0f);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="fd8e7-113">Para converter o retângulo, use o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="fd8e7-113">To translate the rectangle, use the following code:</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.DrawRectangle(&pen, rect);
```



 

 



