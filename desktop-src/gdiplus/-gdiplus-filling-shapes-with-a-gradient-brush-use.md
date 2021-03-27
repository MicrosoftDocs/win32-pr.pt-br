---
description: Você pode usar um pincel de gradiente para preencher uma forma com uma cor que muda gradualmente.
ms.assetid: e37b4c3a-b753-483a-990f-da3bcc70acf5
title: Preenchendo formas com um pincel de gradiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6784d0bfd59fd37f217e8d7a1cdd230348807d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988876"
---
# <a name="filling-shapes-with-a-gradient-brush"></a><span data-ttu-id="07f1f-103">Preenchendo formas com um pincel de gradiente</span><span class="sxs-lookup"><span data-stu-id="07f1f-103">Filling Shapes with a Gradient Brush</span></span>

<span data-ttu-id="07f1f-104">Você pode usar um pincel de gradiente para preencher uma forma com uma cor que muda gradualmente.</span><span class="sxs-lookup"><span data-stu-id="07f1f-104">You can use a gradient brush to fill a shape with a gradually changing color.</span></span> <span data-ttu-id="07f1f-105">Por exemplo, é possível usar um gradiente horizontal para preencher uma forma com uma cor que muda gradualmente à medida que você move da borda esquerda da forma para a borda direita.</span><span class="sxs-lookup"><span data-stu-id="07f1f-105">For example, you can use a horizontal gradient to fill a shape with color that changes gradually as you move from the left edge of the shape to the right edge.</span></span> <span data-ttu-id="07f1f-106">Imagine um retângulo com uma borda esquerda preta (representada pelos componentes vermelho, verde e azul 0, 0, 0) e uma borda direita vermelha (representada por 255, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="07f1f-106">Imagine a rectangle with a left edge that is black (represented by red, green, and blue components 0, 0, 0) and a right edge that is red (represented by 255, 0, 0).</span></span> <span data-ttu-id="07f1f-107">Se o retângulo tem 256 pixels de largura, o componente vermelho de um determinado pixel será maior do que o componente vermelho do pixel à esquerda.</span><span class="sxs-lookup"><span data-stu-id="07f1f-107">If the rectangle is 256 pixels wide, the red component of a given pixel will be one greater than the red component of the pixel to its left.</span></span> <span data-ttu-id="07f1f-108">O pixel mais à esquerda em uma linha tem componentes de cor (0, 0, 0), o segundo pixel tem (1, 0, 0), o terceiro pixel tem (2, 0, 0) e assim por diante, até chegar ao pixel mais à direita, que tem componentes de cor (255, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="07f1f-108">The leftmost pixel in a row has color components (0, 0, 0), the second pixel has (1, 0, 0), the third pixel has (2, 0, 0), and so on, until you get to the rightmost pixel, which has color components (255, 0, 0).</span></span> <span data-ttu-id="07f1f-109">Esses valores de cor interpolados compõem o gradiente de cores.</span><span class="sxs-lookup"><span data-stu-id="07f1f-109">These interpolated color values make up the color gradient.</span></span>

<span data-ttu-id="07f1f-110">Um gradiente linear muda de cor ao mover na horizontal, vertical ou em paralelo para uma linha inclinada especificada.</span><span class="sxs-lookup"><span data-stu-id="07f1f-110">A linear gradient changes color as you move horizontally, vertically, or parallel to a specified slanted line.</span></span> <span data-ttu-id="07f1f-111">Um gradiente de demarcador muda de cor ao mover sobre o interior e o limite de um demarcador.</span><span class="sxs-lookup"><span data-stu-id="07f1f-111">A path gradient changes color as you move about the interior and boundary of a path.</span></span> <span data-ttu-id="07f1f-112">É possível personalizar gradientes de demarcador para obter uma grande variedade de efeitos.</span><span class="sxs-lookup"><span data-stu-id="07f1f-112">You can customize path gradients to achieve a wide variety of effects.</span></span>

<span data-ttu-id="07f1f-113">O GDI+ fornece as classes [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) e [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) , ambas herdadas da classe [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="07f1f-113">GDI+ provides the [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) and [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) classes, both of which inherit from the [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) class.</span></span>

<span data-ttu-id="07f1f-114">Os tópicos a seguir abordam gradientes lineares e de caminho mais detalhadamente:</span><span class="sxs-lookup"><span data-stu-id="07f1f-114">The following topics cover linear and path gradients in more detail:</span></span>

-   [<span data-ttu-id="07f1f-115">Criando um gradiente linear</span><span class="sxs-lookup"><span data-stu-id="07f1f-115">Creating a Linear Gradient</span></span>](-gdiplus-creating-a-linear-gradient-use.md)
-   [<span data-ttu-id="07f1f-116">Criando um gradiente de caminho</span><span class="sxs-lookup"><span data-stu-id="07f1f-116">Creating a Path Gradient</span></span>](-gdiplus-creating-a-path-gradient-use.md)
-   [<span data-ttu-id="07f1f-117">Aplicando a correção gama a um gradiente</span><span class="sxs-lookup"><span data-stu-id="07f1f-117">Applying Gamma Correction to a Gradient</span></span>](-gdiplus-applying-gamma-correction-to-a-gradient-use.md)

 

 



