---
description: Para desenhar linhas com o Windows GDI+, você precisa criar um objeto de gráfico e um objeto de caneta.
ms.assetid: d91562ab-41e6-4bca-a320-74f490a4f88f
title: Canetas, linhas e retângulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e9749b1c1af6ca4808e797d016267bb251e6fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967752"
---
# <a name="pens-lines-and-rectangles"></a><span data-ttu-id="1237d-103">Canetas, linhas e retângulos</span><span class="sxs-lookup"><span data-stu-id="1237d-103">Pens, Lines, and Rectangles</span></span>

<span data-ttu-id="1237d-104">Para desenhar linhas com o Windows GDI+, você precisa criar um objeto de [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e um objeto de [**caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="1237d-104">To draw lines with Windows GDI+ you need to create a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="1237d-105">O objeto **Graphics** fornece os métodos que realmente fazem o desenho, e o objeto **Pen** armazena os atributos da linha, como Color, Width e Style.</span><span class="sxs-lookup"><span data-stu-id="1237d-105">The **Graphics** object provides the methods that actually do the drawing, and the **Pen** object stores attributes of the line, such as color, width, and style.</span></span> <span data-ttu-id="1237d-106">Desenhar uma linha é simplesmente uma questão de chamar o método [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) do objeto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="1237d-106">Drawing a line is simply a matter of calling the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method of the **Graphics** object.</span></span> <span data-ttu-id="1237d-107">O endereço do objeto **Pen** é passado como um dos argumentos para o método DrawLine.</span><span class="sxs-lookup"><span data-stu-id="1237d-107">The address of the **Pen** object is passed as one of the arguments to the DrawLine method.</span></span> <span data-ttu-id="1237d-108">O exemplo a seguir desenha uma linha do ponto (4, 2) até o ponto (12, 6).</span><span class="sxs-lookup"><span data-stu-id="1237d-108">The following example draws a line from the point (4, 2) to the point (12, 6).</span></span>


```
myGraphics.DrawLine(&myPen, 4, 2, 12, 6);
```



<span data-ttu-id="1237d-109">[DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) é um método sobrecarregado da classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , portanto, há várias maneiras pelas quais você pode fornecê-lo com argumentos.</span><span class="sxs-lookup"><span data-stu-id="1237d-109">[DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) is an overloaded method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="1237d-110">Por exemplo, você pode construir dois objetos [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) e passar referências para os objetos **Point** como argumentos para o método DrawLine.</span><span class="sxs-lookup"><span data-stu-id="1237d-110">For example, you can construct two [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) objects and pass references to the **Point** objects as arguments to the DrawLine method.</span></span>


```
Point myStartPoint(4, 2);
Point myEndPoint(12, 6);
myGraphics.DrawLine(&myPen, myStartPoint, myEndPoint);
```



<span data-ttu-id="1237d-111">Você pode especificar determinados atributos ao construir um objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="1237d-111">You can specify certain attributes when you construct a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="1237d-112">Por exemplo, um construtor de [caneta](/windows/win32/api/gdipluspen/nf-gdipluspen-pen-pen(constpen_)) permite que você especifique a cor e a largura.</span><span class="sxs-lookup"><span data-stu-id="1237d-112">For example, one [Pen](/windows/win32/api/gdipluspen/nf-gdipluspen-pen-pen(constpen_)) constructor allows you to specify color and width.</span></span> <span data-ttu-id="1237d-113">O exemplo a seguir desenha uma linha azul de largura 2 de (0, 0) para (60, 30).</span><span class="sxs-lookup"><span data-stu-id="1237d-113">The following example draws a blue line of width 2 from (0, 0) to (60, 30).</span></span>


```
Pen myPen(Color(255, 0, 0, 255), 2);
myGraphics.DrawLine(&myPen, 0, 0, 60, 30);
```



<span data-ttu-id="1237d-114">O objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) também tem atributos, como o estilo tracejado, que você pode usar para especificar os recursos da linha.</span><span class="sxs-lookup"><span data-stu-id="1237d-114">The [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object also has attributes, such as dash style, that you can use to specify features of the line.</span></span> <span data-ttu-id="1237d-115">Por exemplo, o exemplo a seguir desenha uma linha tracejada de (100, 50) a (300, 80).</span><span class="sxs-lookup"><span data-stu-id="1237d-115">For example, the following example draws a dashed line from (100, 50) to (300, 80).</span></span>


```
myPen.SetDashStyle(DashStyleDash);
myGraphics.DrawLine(&myPen, 100, 50, 300, 80);
```



<span data-ttu-id="1237d-116">Você pode usar vários métodos do objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) para definir muitos outros atributos da linha.</span><span class="sxs-lookup"><span data-stu-id="1237d-116">You can use various methods of the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object to set many more attributes of the line.</span></span> <span data-ttu-id="1237d-117">Os métodos [**Pen:: SetStartCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setstartcap) e [**Pen:: SetEndCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setendcap) especificam a aparência das extremidades da linha; as extremidades podem ser simples, quadradas, arredondadas, triangulares ou uma forma personalizada.</span><span class="sxs-lookup"><span data-stu-id="1237d-117">The [**Pen::SetStartCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setstartcap) and [**Pen::SetEndCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setendcap) methods specify the appearance of the ends of the line; the ends can be flat, square, rounded, triangular, or a custom shape.</span></span> <span data-ttu-id="1237d-118">O método [**Pen:: SetLineJoin**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) permite especificar se as linhas conectadas são Mitre (Unidas com cantos nítidos), chanfradas, arredondadas ou recortadas.</span><span class="sxs-lookup"><span data-stu-id="1237d-118">The [**Pen::SetLineJoin**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) method lets you specify whether connected lines are mitered (joined with sharp corners), beveled, rounded, or clipped.</span></span> <span data-ttu-id="1237d-119">A ilustração a seguir mostra linhas com vários estilos de extremidade e junção.</span><span class="sxs-lookup"><span data-stu-id="1237d-119">The following illustration shows lines with various cap and join styles.</span></span>

![ilustração de duas linhas que demonstram extremidades arredondadas e circulares, cantos arredondados e com mitra e dois estilos de seta](images/aboutgdip02-art04.png)

<span data-ttu-id="1237d-121">Retângulos de desenho com GDI+ é semelhante a linhas de desenho.</span><span class="sxs-lookup"><span data-stu-id="1237d-121">Drawing rectangles with GDI+ is similar to drawing lines.</span></span> <span data-ttu-id="1237d-122">Para desenhar um retângulo, você precisa de um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e um objeto de [**caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="1237d-122">To draw a rectangle, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="1237d-123">O objeto **Graphics** fornece um método [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) e o objeto **Pen** armazena atributos, como largura e cor da linha.</span><span class="sxs-lookup"><span data-stu-id="1237d-123">The **Graphics** object provides a [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) method, and the **Pen** object stores attributes, such as line width and color.</span></span> <span data-ttu-id="1237d-124">O endereço do objeto **Pen** é passado como um dos argumentos para o método DrawRectangle.</span><span class="sxs-lookup"><span data-stu-id="1237d-124">The address of the **Pen** object is passed as one of the arguments to the DrawRectangle method.</span></span> <span data-ttu-id="1237d-125">O exemplo a seguir desenha um retângulo com seu canto superior esquerdo em (100, 50), uma largura de 80 e uma altura de 40.</span><span class="sxs-lookup"><span data-stu-id="1237d-125">The following example draws a rectangle with its upper-left corner at (100, 50), a width of 80, and a height of 40.</span></span>


```
myGraphics.DrawRectangle(&myPen, 100, 50, 80, 40);
```



<span data-ttu-id="1237d-126">[DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) é um método sobrecarregado da classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , portanto, há várias maneiras de fornecer argumentos.</span><span class="sxs-lookup"><span data-stu-id="1237d-126">[DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) is an overloaded method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="1237d-127">Por exemplo, você pode construir um objeto [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) e passar uma referência para o objeto **Rect** como um argumento para o método DrawRectangle.</span><span class="sxs-lookup"><span data-stu-id="1237d-127">For example, you can construct a [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) object and pass a reference to the **Rect** object as an argument to the DrawRectangle method.</span></span>


```
Rect myRect(100, 50, 80, 40);
myGraphics.DrawRectangle(&myPen, myRect);
```



<span data-ttu-id="1237d-128">Um objeto [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) tem métodos para manipular e coletar informações sobre o retângulo.</span><span class="sxs-lookup"><span data-stu-id="1237d-128">A [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) object has methods for manipulating and gathering information about the rectangle.</span></span> <span data-ttu-id="1237d-129">Por exemplo, os métodos [inflar](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-inflate(inint_inint)) e [offset](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-offset(inconstpoint_)) alteram o tamanho e a posição do retângulo.</span><span class="sxs-lookup"><span data-stu-id="1237d-129">For example, the [Inflate](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-inflate(inint_inint)) and [Offset](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-offset(inconstpoint_)) methods change the size and position of the rectangle.</span></span> <span data-ttu-id="1237d-130">O método [**Rect:: IntersectsWith**](/windows/win32/api/Gdiplustypes/nf-gdiplustypes-rect-intersectswith) informa se o retângulo cruza outro retângulo determinado e o método [Contains](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-contains(inint_inint)) informa se um determinado ponto está dentro do retângulo.</span><span class="sxs-lookup"><span data-stu-id="1237d-130">The [**Rect::IntersectsWith**](/windows/win32/api/Gdiplustypes/nf-gdiplustypes-rect-intersectswith) method tells you whether the rectangle intersects another given rectangle, and the [Contains](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-contains(inint_inint)) method tells you whether a given point is inside the rectangle.</span></span>

 

 
