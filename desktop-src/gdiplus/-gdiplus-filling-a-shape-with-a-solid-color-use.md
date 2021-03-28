---
description: Para preencher uma forma com uma cor sólida, crie um objeto SolidBrush e, em seguida, passe o endereço desse objeto SolidBrush como um argumento para um dos métodos Fill da classe Graphics.
ms.assetid: cedef138-5047-4a72-8b89-5a95062a351c
title: Preenchendo uma forma com uma cor sólida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c4a6221d84c4a891d377d974f168468917799e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988878"
---
# <a name="filling-a-shape-with-a-solid-color"></a><span data-ttu-id="1667a-103">Preenchendo uma forma com uma cor sólida</span><span class="sxs-lookup"><span data-stu-id="1667a-103">Filling a Shape with a Solid Color</span></span>

<span data-ttu-id="1667a-104">Para preencher uma forma com uma cor sólida, crie um objeto [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) e, em seguida, passe o endereço desse objeto **SolidBrush** como um argumento para um dos métodos Fill da classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="1667a-104">To fill a shape with a solid color, create a [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object, and then pass the address of that **SolidBrush** object as an argument to one of the fill methods of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="1667a-105">O exemplo a seguir mostra como preencher uma elipse com a cor vermelho:</span><span class="sxs-lookup"><span data-stu-id="1667a-105">The following example shows how to fill an ellipse with the color red:</span></span>


```
SolidBrush solidBrush(Color(255, 255, 0, 0));
stat = graphics.FillEllipse(&solidBrush, 0, 0, 100, 60);
```



<span data-ttu-id="1667a-106">No exemplo anterior, o construtor [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) usa uma referência de objeto de [**cor**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) como seu único argumento.</span><span class="sxs-lookup"><span data-stu-id="1667a-106">In the preceding example, the [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) constructor takes a [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) object reference as its only argument.</span></span> <span data-ttu-id="1667a-107">Os valores usados pelo construtor **Color** representam os componentes alfa, Red, Green e Blue da cor.</span><span class="sxs-lookup"><span data-stu-id="1667a-107">The values used by the **Color** constructor represent the alpha, red, green, and blue components of the color.</span></span> <span data-ttu-id="1667a-108">Cada um desses valores deve estar no intervalo de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="1667a-108">Each of these values must be in the range 0 through 255.</span></span> <span data-ttu-id="1667a-109">O primeiro 255 indica que a cor é totalmente opaca e o segundo 255 indica que o componente vermelho é de intensidade total.</span><span class="sxs-lookup"><span data-stu-id="1667a-109">The first 255 indicates that the color is fully opaque, and the second 255 indicates that the red component is at full intensity.</span></span> <span data-ttu-id="1667a-110">Os dois zeros indicam que os componentes verde e azul têm uma intensidade igual a 0.</span><span class="sxs-lookup"><span data-stu-id="1667a-110">The two zeros indicate that the green and blue components both have an intensity of 0.</span></span>

<span data-ttu-id="1667a-111">Os quatro números (0, 0, 100, 60) passados para o método [**Graphics:: FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inint_inint_inint_inint)) especificam o local e o tamanho do retângulo delimitador para a elipse.</span><span class="sxs-lookup"><span data-stu-id="1667a-111">The four numbers (0, 0, 100, 60) passed to the [**Graphics::FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inint_inint_inint_inint)) method specify the location and size of the bounding rectangle for the ellipse.</span></span> <span data-ttu-id="1667a-112">O retângulo tem um canto superior esquerdo de (0, 0), uma largura de 100 e uma altura de 60.</span><span class="sxs-lookup"><span data-stu-id="1667a-112">The rectangle has an upper-left corner of (0, 0), a width of 100, and a height of 60.</span></span>

 

 
