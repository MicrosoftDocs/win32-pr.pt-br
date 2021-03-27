---
description: Uma elipse é especificada por seu retângulo delimitador. A ilustração a seguir mostra uma elipse junto a seu retângulo delimitador.
ms.assetid: 45e80501-4d64-480b-a7c7-3af52c00a0aa
title: Elipses e arcos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8b1aaaff5ff27191ed7f0bf64ddbcb414be6319
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091469"
---
# <a name="ellipses-and-arcs"></a><span data-ttu-id="6c1d3-104">Elipses e arcos</span><span class="sxs-lookup"><span data-stu-id="6c1d3-104">Ellipses and Arcs</span></span>

<span data-ttu-id="6c1d3-105">Uma elipse é especificada por seu retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="6c1d3-105">An ellipse is specified by its bounding rectangle.</span></span> <span data-ttu-id="6c1d3-106">A ilustração a seguir mostra uma elipse junto a seu retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="6c1d3-106">The following illustration shows an ellipse along with its bounding rectangle.</span></span>

![ilustração de uma elipse colocada dentro de um retângulo delimitador](images/aboutgdip02-art05.png)

<span data-ttu-id="6c1d3-108">Para desenhar uma elipse, você precisa de um objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e um objeto de [**caneta**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="6c1d3-108">To draw an ellipse, you need a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="6c1d3-109">O objeto **Graphics** fornece o método [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) e o objeto **Pen** armazena os atributos da elipse, como largura e cor da linha.</span><span class="sxs-lookup"><span data-stu-id="6c1d3-109">The **Graphics** object provides the [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) method, and the **Pen** object stores attributes of the ellipse, such as line width and color.</span></span> <span data-ttu-id="6c1d3-110">O endereço do objeto **Pen** é passado como um dos argumentos para o método DrawEllipse.</span><span class="sxs-lookup"><span data-stu-id="6c1d3-110">The address of the **Pen** object is passed as one of the arguments to the DrawEllipse method.</span></span> <span data-ttu-id="6c1d3-111">Os argumentos restantes passados para o método DrawEllipse especificam o retângulo delimitador para a elipse.</span><span class="sxs-lookup"><span data-stu-id="6c1d3-111">The remaining arguments passed to the DrawEllipse method specify the bounding rectangle for the ellipse.</span></span> <span data-ttu-id="6c1d3-112">O exemplo a seguir desenha uma elipse; o retângulo delimitador tem uma largura de 160, uma altura de 80 e um canto superior esquerdo de (100, 50).</span><span class="sxs-lookup"><span data-stu-id="6c1d3-112">The following example draws an ellipse; the bounding rectangle has a width of 160, a height of 80, and an upper-left corner of (100, 50).</span></span>


```
myGraphics.DrawEllipse(&myPen, 100, 50, 160, 80);
```



<span data-ttu-id="6c1d3-113">[DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) é um método sobrecarregado da classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , portanto, há várias maneiras de fornecer argumentos.</span><span class="sxs-lookup"><span data-stu-id="6c1d3-113">[DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) is an overloaded method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="6c1d3-114">Por exemplo, você pode construir um objeto [**Rect**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect) e passar uma referência para o objeto **Rect** como um argumento para o método DrawEllipse.</span><span class="sxs-lookup"><span data-stu-id="6c1d3-114">For example, you can construct a [**Rect**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect) object and pass a reference to the **Rect** object as an argument to the DrawEllipse method.</span></span>


```
Rect myRect(100, 50, 160, 80);
myGraphics.DrawEllipse(&myPen, myRect);
```



<span data-ttu-id="6c1d3-115">Um arco é uma parte de uma elipse.</span><span class="sxs-lookup"><span data-stu-id="6c1d3-115">An arc is a portion of an ellipse.</span></span> <span data-ttu-id="6c1d3-116">Para desenhar um arco, você chama o método [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) da classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="6c1d3-116">To draw an arc, you call the [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="6c1d3-117">Os parâmetros do método DrawArc são os mesmos que os parâmetros do método [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) , exceto que DrawArc requer um ângulo inicial e um ângulo de flecha.</span><span class="sxs-lookup"><span data-stu-id="6c1d3-117">The parameters of the DrawArc method are the same as the parameters of the [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) method, except that DrawArc requires a starting angle and sweep angle.</span></span> <span data-ttu-id="6c1d3-118">O exemplo a seguir desenha um arco com um ângulo inicial de 30 graus e um ângulo de flecha de 180 graus.</span><span class="sxs-lookup"><span data-stu-id="6c1d3-118">The following example draws an arc with a starting angle of 30 degrees and a sweep angle of 180 degrees.</span></span>


```
myGraphics.DrawArc(&myPen, 100, 50, 160, 80, 30, 180);
```



<span data-ttu-id="6c1d3-119">A ilustração a seguir mostra o arco, a elipse e o retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="6c1d3-119">The following illustration shows the arc, the ellipse, and the bounding rectangle.</span></span>

![ilustração de uma elipse dentro de um retângulo delimitador; a metade esquerda inferior da elipse é desenhada em vermelho](images/aboutgdip02-art06.png)

 

 



