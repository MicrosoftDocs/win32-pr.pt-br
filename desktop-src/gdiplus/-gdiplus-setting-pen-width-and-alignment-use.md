---
description: 'Ao criar um objeto de caneta, você pode fornecer a largura da caneta como um dos argumentos para o construtor. Você também pode alterar a largura da caneta usando o método Pen:: SetWidth.'
ms.assetid: b529ba0b-1786-4925-88bd-1a8369fc368c
title: Definindo a largura e o alinhamento da caneta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca59895cc73480b054302091342c8f8f4f410b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563086"
---
# <a name="setting-pen-width-and-alignment"></a><span data-ttu-id="73b23-104">Definindo a largura e o alinhamento da caneta</span><span class="sxs-lookup"><span data-stu-id="73b23-104">Setting Pen Width and Alignment</span></span>

<span data-ttu-id="73b23-105">Ao criar um objeto de [**caneta**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) , você pode fornecer a largura da caneta como um dos argumentos para o construtor.</span><span class="sxs-lookup"><span data-stu-id="73b23-105">When you create a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object, you can supply the pen width as one of the arguments to the constructor.</span></span> <span data-ttu-id="73b23-106">Você também pode alterar a largura da caneta usando o método [**Pen:: SetWidth**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setwidth) .</span><span class="sxs-lookup"><span data-stu-id="73b23-106">You can also change the pen width by using the [**Pen::SetWidth**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setwidth) method.</span></span>

<span data-ttu-id="73b23-107">Uma linha teórica tem uma largura de zero.</span><span class="sxs-lookup"><span data-stu-id="73b23-107">A theoretical line has a width of zero.</span></span> <span data-ttu-id="73b23-108">Quando você desenha uma linha, os pixels são centralizados na linha teórica.</span><span class="sxs-lookup"><span data-stu-id="73b23-108">When you draw a line, the pixels are centered on the theoretical line.</span></span> <span data-ttu-id="73b23-109">O exemplo a seguir desenha uma linha especificada duas vezes: uma vez com uma caneta preta de largura 1 e uma vez com uma caneta verde de largura 10.</span><span class="sxs-lookup"><span data-stu-id="73b23-109">The following example draws a specified line twice: once with a black pen of width 1 and once with a green pen of width 10.</span></span>


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the line with the wide green pen.
stat = graphics.DrawLine(&greenPen, 10, 100, 100, 50);

// Draw the same line with the thin black pen.
stat = graphics.DrawLine(&blackPen, 10, 100, 100, 50);
```



<span data-ttu-id="73b23-110">A ilustração a seguir mostra a saída do código anterior.</span><span class="sxs-lookup"><span data-stu-id="73b23-110">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="73b23-111">Os pixels verdes e os pixels pretos são centralizados na linha teórica.</span><span class="sxs-lookup"><span data-stu-id="73b23-111">The green pixels and the black pixels are centered on the theoretical line.</span></span>

![<span data-ttu-id="73b23-112">ilustração mostrando uma linha fina, diagonal e preta cercada por uma linha verde</span><span class="sxs-lookup"><span data-stu-id="73b23-112">illustration showing a thin, diagonal, black line surrounded by a wide, green line</span></span> ](images/pens1a.png)

<span data-ttu-id="73b23-113">O exemplo a seguir desenha um retângulo especificado duas vezes: uma vez com uma caneta preta de largura 1 e uma vez com uma caneta verde de largura 10.</span><span class="sxs-lookup"><span data-stu-id="73b23-113">The following example draws a specified rectangle twice: once with a black pen of width 1 and once with a green pen of width 10.</span></span> <span data-ttu-id="73b23-114">O código passa o valor **PenAlignmentCenter** (um elemento da enumeração [**PenAlignment**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-penalignment) ) para o método [**Pen:: setAlignment**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setalignment) para especificar que os pixels desenhados com a caneta verde estejam centralizados no limite do retângulo.</span><span class="sxs-lookup"><span data-stu-id="73b23-114">The code passes the value **PenAlignmentCenter** (an element of the [**PenAlignment**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-penalignment) enumeration) to the [**Pen::SetAlignment**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setalignment) method to specify that the pixels drawn with the green pen are centered on the boundary of the rectangle.</span></span>


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the rectangle with the wide green pen.
stat = graphics.DrawRectangle(&greenPen, 10, 100, 50, 50);

// Draw the same rectangle with the thin black pen.
stat = graphics.DrawRectangle(&blackPen, 10, 100, 50, 50);
```



<span data-ttu-id="73b23-115">A ilustração a seguir mostra a saída do código anterior.</span><span class="sxs-lookup"><span data-stu-id="73b23-115">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="73b23-116">Os pixels verdes são centralizados no retângulo teórico, que é representado pelos pixels pretos.</span><span class="sxs-lookup"><span data-stu-id="73b23-116">The green pixels are centered on the theoretical rectangle, which is represented by the black pixels.</span></span>

![ilustração mostrando uma linha preta fina na forma de um retângulo, cercada por uma linha verde mais larga](images/pens2.png)

<span data-ttu-id="73b23-118">Você pode alterar o alinhamento da caneta verde modificando a terceira instrução no exemplo anterior, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="73b23-118">You can change the green pen's alignment by modifying the third statement in the preceding example as follows:</span></span>


```
stat = greenPen.SetAlignment(PenAlignmentInset);
```



<span data-ttu-id="73b23-119">Agora os pixels na linha verde larga aparecem no interior do retângulo conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="73b23-119">Now the pixels in the wide green line appear on the inside of the rectangle as shown in the following illustration.</span></span>

![ilustração mostrando uma linha preta fina na forma de um retângulo, colocando uma linha verde larga da mesma forma](images/pens3.png)

 

 



