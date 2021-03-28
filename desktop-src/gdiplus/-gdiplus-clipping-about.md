---
description: O recorte envolve restringir o desenho a uma determinada região. A ilustração a seguir mostra a cadeia de caracteres &\# 0034; Olá&\# 0034; recortado em uma região em formato de coração.
ms.assetid: 58cc052d-31af-4410-81b9-defbad08a1dc
title: Recorte (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 156ae2209a3b7135cde2804103531eaf7b519d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010871"
---
# <a name="clipping-gdi"></a><span data-ttu-id="1ad59-104">Recorte (GDI+)</span><span class="sxs-lookup"><span data-stu-id="1ad59-104">Clipping (GDI+)</span></span>

<span data-ttu-id="1ad59-105">O recorte envolve restringir o desenho a uma determinada região.</span><span class="sxs-lookup"><span data-stu-id="1ad59-105">Clipping involves restricting drawing to a certain region.</span></span> <span data-ttu-id="1ad59-106">A ilustração a seguir mostra a cadeia de caracteres "Olá" recortada para uma região em formato de coração.</span><span class="sxs-lookup"><span data-stu-id="1ad59-106">The following illustration shows the string "Hello" clipped to a heart-shaped region.</span></span>

![ilustração mostrando partes da cadeia de caracteres "Olá" em um coração vermelho](images/aboutgdip02-art30.png)

<span data-ttu-id="1ad59-108">As regiões podem ser construídas a partir de caminhos, e os caminhos podem conter os contornos das cadeias de caracteres, para que você possa usar texto com contorno para recorte.</span><span class="sxs-lookup"><span data-stu-id="1ad59-108">Regions can be constructed from paths, and paths can contain the outlines of strings, so you can use outlined text for clipping.</span></span> <span data-ttu-id="1ad59-109">A ilustração a seguir mostra um conjunto de elipses concêntricas recortados para o interior de uma cadeia de caracteres de texto.</span><span class="sxs-lookup"><span data-stu-id="1ad59-109">The following illustration shows a set of concentric ellipses clipped to the interior of a string of text.</span></span>

![ilustração mostrando a cadeia de caracteres "Olá" preenchida por um padrão de círculos concêntricos](images/aboutgdip02-art31.png)

<span data-ttu-id="1ad59-111">Para desenhar com recorte, crie um objeto de [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , chame seu método [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) e, em seguida, chame os métodos de desenho desse mesmo objeto **gráfico** .</span><span class="sxs-lookup"><span data-stu-id="1ad59-111">To draw with clipping, create a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, call its [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) method, and then call the drawing methods of that same **Graphics** object.</span></span> <span data-ttu-id="1ad59-112">O exemplo a seguir desenha uma linha recortada em uma região retangular.</span><span class="sxs-lookup"><span data-stu-id="1ad59-112">The following example draws a line that is clipped to a rectangular region.</span></span>


```
Region myRegion(Rect(20, 30, 100, 50));
myGraphics.DrawRectangle(&myPen, 20, 30, 100, 50);  
myGraphics.SetClip(&myRegion, CombineModeReplace);
myGraphics.DrawLine(&myPen, 0, 0, 200, 200);
```



<span data-ttu-id="1ad59-113">A ilustração a seguir mostra a região retangular junto com a linha recortada.</span><span class="sxs-lookup"><span data-stu-id="1ad59-113">The following illustration shows the rectangular region along with the clipped line.</span></span>

![ilustração mostrando um retângulo com uma linha diagonal de cima para baixo](images/aboutgdip02-art31a.png)

 

 



