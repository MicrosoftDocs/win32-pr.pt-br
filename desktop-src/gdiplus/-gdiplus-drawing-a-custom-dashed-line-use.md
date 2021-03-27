---
description: O Windows GDI+ fornece vários estilos de traço listados na enumeração DashStyle. Se esses estilos de traço padrão não atenderem às suas necessidades, você poderá criar um padrão de traço personalizado.
ms.assetid: 0e75de3b-1006-4c8f-875c-eeb0782f24b0
title: Desenhando uma linha tracejada personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e108dcd6b32a47befcdd99d1f23e90c33d08446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988278"
---
# <a name="drawing-a-custom-dashed-line"></a><span data-ttu-id="0ff07-104">Desenhando uma linha tracejada personalizada</span><span class="sxs-lookup"><span data-stu-id="0ff07-104">Drawing a Custom Dashed Line</span></span>

<span data-ttu-id="0ff07-105">O Windows GDI+ fornece vários estilos de traço listados na enumeração [**DashStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-dashstyle) .</span><span class="sxs-lookup"><span data-stu-id="0ff07-105">Windows GDI+ provides several dash styles that are listed in the [**DashStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-dashstyle) enumeration.</span></span> <span data-ttu-id="0ff07-106">Se esses estilos de traço padrão não atenderem às suas necessidades, você poderá criar um padrão de traço personalizado.</span><span class="sxs-lookup"><span data-stu-id="0ff07-106">If those standard dash styles don't suit your needs, you can create a custom dash pattern.</span></span>

<span data-ttu-id="0ff07-107">Para desenhar uma linha tracejada personalizada, coloque os comprimentos dos traços e espaços em uma matriz e passe o endereço da matriz como um argumento para o método [**Pen:: SetDashPattern**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setdashpattern) de um objeto [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="0ff07-107">To draw a custom dashed line, put the lengths of the dashes and spaces in an array and pass the address of the array as an argument to the [**Pen::SetDashPattern**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setdashpattern) method of a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="0ff07-108">O exemplo a seguir desenha uma linha tracejada personalizada com base na matriz {5, 2, 15, 4}.</span><span class="sxs-lookup"><span data-stu-id="0ff07-108">The following example draws a custom dashed line based on the array {5, 2, 15, 4}.</span></span> <span data-ttu-id="0ff07-109">Se você multiplicar os elementos da matriz pela largura da caneta de 5, obterá {25, 10, 75, 20}.</span><span class="sxs-lookup"><span data-stu-id="0ff07-109">If you multiply the elements of the array by the pen width of 5, you get {25, 10, 75, 20}.</span></span> <span data-ttu-id="0ff07-110">Os traços exibidos alternam de comprimento entre 25 e 75 e os espaços alternam de comprimento entre 10 e 20.</span><span class="sxs-lookup"><span data-stu-id="0ff07-110">The displayed dashes alternate in length between 25 and 75, and the spaces alternate in length between 10 and 20.</span></span>


```
REAL dashValues[4] = {5, 2, 15, 4};
Pen blackPen(Color(255, 0, 0, 0), 5);
blackPen.SetDashPattern(dashValues, 4);
stat = graphics.DrawLine(&blackPen, Point(5, 5), Point(405, 5));
```



<span data-ttu-id="0ff07-111">A ilustração a seguir mostra a linha tracejada resultante.</span><span class="sxs-lookup"><span data-stu-id="0ff07-111">The following illustration shows the resulting dashed line.</span></span> <span data-ttu-id="0ff07-112">Observe que o traço final deve ser menor do que 25 unidades para que a linha possa terminar em (405, 5).</span><span class="sxs-lookup"><span data-stu-id="0ff07-112">Note that the final dash has to be shorter than 25 units so that the line can end at (405, 5).</span></span>

![ilustração mostrando uma linha tracejada; cada segmento é uma linha curta seguida de um longo](images/pens6.png)

 

 



