---
description: Para desenhar linhas e retângulos, você precisa de um objeto gráfico e um objeto de caneta. O objeto Graphics fornece o método DrawLine e o objeto Pen armazena os recursos da linha, como Color e Width.
ms.assetid: f2e4144f-f2f1-49db-bfdf-ffce3023b4cb
title: Uso de uma caneta para desenhar linhas e retângulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b335caf7e2ecbad6bc49965ff757809c3b1179c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921425"
---
# <a name="using-a-pen-to-draw-lines-and-rectangles"></a><span data-ttu-id="9ffa8-104">Uso de uma caneta para desenhar linhas e retângulos</span><span class="sxs-lookup"><span data-stu-id="9ffa8-104">Using a Pen to Draw Lines and Rectangles</span></span>

<span data-ttu-id="9ffa8-105">Para desenhar linhas e retângulos, você precisa de um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e um objeto de [**caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="9ffa8-105">To draw lines and rectangles, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="9ffa8-106">O objeto **Graphics** fornece o método [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) e o objeto **Pen** armazena os recursos da linha, como Color e Width.</span><span class="sxs-lookup"><span data-stu-id="9ffa8-106">The **Graphics** object provides the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method, and the **Pen** object stores features of the line, such as color and width.</span></span>

<span data-ttu-id="9ffa8-107">O exemplo a seguir desenha uma linha de (20, 10) para (300, 100).</span><span class="sxs-lookup"><span data-stu-id="9ffa8-107">The following example draws a line from (20, 10) to (300, 100).</span></span> <span data-ttu-id="9ffa8-108">Suponha que **gráficos** seja um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) existente.</span><span class="sxs-lookup"><span data-stu-id="9ffa8-108">Assume **graphics** is an existing [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>


```
Pen pen(Color(255, 0, 0, 0));
graphics.DrawLine(&pen, 20, 10, 300, 100);
```



<span data-ttu-id="9ffa8-109">A primeira instrução do código usa o construtor da classe [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) para criar uma caneta preta.</span><span class="sxs-lookup"><span data-stu-id="9ffa8-109">The first statement of code uses the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) class constructor to create a black pen.</span></span> <span data-ttu-id="9ffa8-110">O argumento One passado para o construtor **Pen** é um objeto [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="9ffa8-110">The one argument passed to the **Pen** constructor is a [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="9ffa8-111">Os valores usados para construir o objeto de **cor** — (255, 0, 0, 0) — correspondem aos componentes alfa, vermelho, verde e azul da cor.</span><span class="sxs-lookup"><span data-stu-id="9ffa8-111">The values used to construct the **Color** object — (255, 0, 0, 0) — correspond to the alpha, red, green, and blue components of the color.</span></span> <span data-ttu-id="9ffa8-112">Esses valores definem uma caneta preta opaca.</span><span class="sxs-lookup"><span data-stu-id="9ffa8-112">These values define an opaque black pen.</span></span>

<span data-ttu-id="9ffa8-113">O exemplo a seguir desenha um retângulo com seu canto superior esquerdo em (10, 10).</span><span class="sxs-lookup"><span data-stu-id="9ffa8-113">The following example draws a rectangle with its upper-left corner at (10, 10).</span></span> <span data-ttu-id="9ffa8-114">O retângulo tem uma largura de 100 e uma altura de 50.</span><span class="sxs-lookup"><span data-stu-id="9ffa8-114">The rectangle has a width of 100 and a height of 50.</span></span> <span data-ttu-id="9ffa8-115">O segundo argumento passado para o construtor de [**caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) indica que a largura da caneta é de 5 pixels.</span><span class="sxs-lookup"><span data-stu-id="9ffa8-115">The second argument passed to the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) constructor indicates that the pen width is 5 pixels.</span></span>


```
Pen blackPen(Color(255, 0, 0, 0), 5);
stat = graphics.DrawRectangle(&blackPen, 10, 10, 100, 50);
```



<span data-ttu-id="9ffa8-116">Quando o retângulo é desenhado, a caneta é centralizada no limite do retângulo.</span><span class="sxs-lookup"><span data-stu-id="9ffa8-116">When the rectangle is drawn, the pen is centered on the rectangle's boundary.</span></span> <span data-ttu-id="9ffa8-117">Como a largura da caneta é 5, os lados do retângulo são desenhados com 5 pixels de largura, de forma que 1 pixel é desenhado no próprio limite, 2 pixels são desenhados no interior e 2 pixels são desenhados fora.</span><span class="sxs-lookup"><span data-stu-id="9ffa8-117">Because the pen width is 5, the sides of the rectangle are drawn 5 pixels wide, such that 1 pixel is drawn on the boundary itself, 2 pixels are drawn on the inside, and 2 pixels are drawn on the outside.</span></span> <span data-ttu-id="9ffa8-118">Para obter mais detalhes sobre alinhamento de caneta, consulte [definindo a largura e o alinhamento da caneta](-gdiplus-setting-pen-width-and-alignment-use.md).</span><span class="sxs-lookup"><span data-stu-id="9ffa8-118">For more details on pen alignment, see [Setting Pen Width and Alignment](-gdiplus-setting-pen-width-and-alignment-use.md).</span></span>

<span data-ttu-id="9ffa8-119">A ilustração a seguir mostra o retângulo resultante.</span><span class="sxs-lookup"><span data-stu-id="9ffa8-119">The following illustration shows the resulting rectangle.</span></span> <span data-ttu-id="9ffa8-120">As linhas pontilhadas mostram onde o retângulo deveria ser desenhado se a largura da caneta tivesse um pixel.</span><span class="sxs-lookup"><span data-stu-id="9ffa8-120">The dotted lines show where the rectangle would have been drawn if the pen width had been one pixel.</span></span> <span data-ttu-id="9ffa8-121">A exibição ampliada do canto superior esquerdo do retângulo mostra que as linhas pretas espessas são centralizadas nessas linhas pontilhadas.</span><span class="sxs-lookup"><span data-stu-id="9ffa8-121">The enlarged view of the upper-left corner of the rectangle shows that the thick black lines are centered on those dotted lines.</span></span>

![ilustração de um retângulo desenhado com uma linha preta espessa que circunda uma linha pontilhada cinza e fina](images/pens1.png)

 

 



