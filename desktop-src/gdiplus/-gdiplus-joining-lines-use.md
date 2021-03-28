---
description: Uma junção de linha é a área comum que é formada por duas linhas cujas extremidades se encontram ou se sobrepõem.
ms.assetid: 4ec3e76a-2531-4869-a5b0-c595198e8345
title: Unindo linhas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2ab0bc53239b9a0d9327a26e25eed1c93c685b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553427"
---
# <a name="joining-lines"></a><span data-ttu-id="d1824-103">Unindo linhas</span><span class="sxs-lookup"><span data-stu-id="d1824-103">Joining Lines</span></span>

<span data-ttu-id="d1824-104">Uma junção de linha é a área comum que é formada por duas linhas cujas extremidades se encontram ou se sobrepõem.</span><span class="sxs-lookup"><span data-stu-id="d1824-104">A line join is the common area that is formed by two lines whose ends meet or overlap.</span></span> <span data-ttu-id="d1824-105">O Windows GDI+ fornece quatro estilos de junção de linha: Mitre, bisel, Round e Mitre recortados.</span><span class="sxs-lookup"><span data-stu-id="d1824-105">Windows GDI+ provides four line join styles: miter, bevel, round, and miter clipped.</span></span> <span data-ttu-id="d1824-106">O estilo de junção de linha é uma propriedade da classe [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="d1824-106">Line join style is a property of the [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) class.</span></span> <span data-ttu-id="d1824-107">Quando você especifica um estilo de junção de linha para uma caneta e, em seguida, usa essa caneta para desenhar um caminho, o estilo de junção especificado é aplicado a todas as linhas conectadas no caminho.</span><span class="sxs-lookup"><span data-stu-id="d1824-107">When you specify a line join style for a pen and then use that pen to draw a path, the specified join style is applied to all the connected lines in the path.</span></span>

<span data-ttu-id="d1824-108">Você pode especificar o estilo de junção de linha usando o método [**Pen:: SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) da classe [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="d1824-108">You can specify the line join style by using the [**Pen::SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) method of the [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) class.</span></span> <span data-ttu-id="d1824-109">O exemplo a seguir demonstra uma junção de linha chanfrada entre uma linha horizontal e uma linha vertical:</span><span class="sxs-lookup"><span data-stu-id="d1824-109">The following example demonstrates a beveled line join between a horizontal line and a vertical line:</span></span>


```
GraphicsPath path;
Pen penJoin(Color(255, 0, 0, 255), 8);

path.StartFigure();
path.AddLine(Point(50, 200), Point(100, 200));
path.AddLine(Point(100, 200), Point(100, 250));

penJoin.SetLineJoin(LineJoinBevel);
graphics.DrawPath(&penJoin, &path);
```



<span data-ttu-id="d1824-110">A ilustração a seguir mostra a junção de linha chanfrada resultante.</span><span class="sxs-lookup"><span data-stu-id="d1824-110">The following illustration shows the resulting beveled line join.</span></span>

![ilustração que mostra duas linhas que atendem a um ângulo direito, com uma junção bevelled](images/pens5.png)

<span data-ttu-id="d1824-112">No exemplo anterior, o valor (**LineJoinBevel**) passado para o método [**Pen:: SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) é um elemento da enumeração [**LineJoin**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linejoin) .</span><span class="sxs-lookup"><span data-stu-id="d1824-112">In the preceding example, the value (**LineJoinBevel**) passed to the [**Pen::SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) method is an element of the [**LineJoin**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linejoin) enumeration.</span></span>

 

 



