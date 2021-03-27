---
description: Você pode girar, refletir e distorcer uma imagem especificando pontos de destino para os cantos superior esquerdo, superior direito e inferior esquerdo da imagem original.
ms.assetid: 1e982d84-8749-451b-89a8-81440fcee439
title: Girando, refletindo e distorcendo imagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5637cb8be0290d96a164042086e997bc878c0227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921427"
---
# <a name="rotating-reflecting-and-skewing-images"></a><span data-ttu-id="64f9b-103">Girando, refletindo e distorcendo imagens</span><span class="sxs-lookup"><span data-stu-id="64f9b-103">Rotating, Reflecting, and Skewing Images</span></span>

<span data-ttu-id="64f9b-104">Você pode girar, refletir e distorcer uma imagem especificando pontos de destino para os cantos superior esquerdo, superior direito e inferior esquerdo da imagem original.</span><span class="sxs-lookup"><span data-stu-id="64f9b-104">You can rotate, reflect, and skew an image by specifying destination points for the upper-left, upper-right, and lower-left corners of the original image.</span></span> <span data-ttu-id="64f9b-105">Os três pontos de destino determinam uma transformação afim que mapeia a imagem retangular original para um paralelogramo.</span><span class="sxs-lookup"><span data-stu-id="64f9b-105">The three destination points determine an affine transformation that maps the original rectangular image to a parallelogram.</span></span> <span data-ttu-id="64f9b-106">(O canto inferior direito da imagem original é mapeado para o quarto canto do paralelogramo, que é calculado a partir dos três pontos de destino especificados.)</span><span class="sxs-lookup"><span data-stu-id="64f9b-106">(The lower-right corner of the original image is mapped to the fourth corner of the parallelogram, which is calculated from the three specified destination points.)</span></span>

<span data-ttu-id="64f9b-107">Por exemplo, suponha que a imagem original é um retângulo com o canto superior esquerdo em (0, 0), o canto superior direito em (100, 0) e o canto inferior esquerdo em (0, 50).</span><span class="sxs-lookup"><span data-stu-id="64f9b-107">For example, suppose the original image is a rectangle with upper-left corner at (0, 0), upper-right corner at (100, 0), and lower-left corner at (0, 50).</span></span> <span data-ttu-id="64f9b-108">Agora suponha que mapeiemos esses três pontos para os pontos de destino da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="64f9b-108">Now suppose we map those three points to destination points as follows.</span></span>



| <span data-ttu-id="64f9b-109">Ponto original</span><span class="sxs-lookup"><span data-stu-id="64f9b-109">Original point</span></span>       | <span data-ttu-id="64f9b-110">Ponto de destino</span><span class="sxs-lookup"><span data-stu-id="64f9b-110">Destination point</span></span> |
|----------------------|-------------------|
| <span data-ttu-id="64f9b-111">Superior esquerdo (0, 0)</span><span class="sxs-lookup"><span data-stu-id="64f9b-111">Upper-left (0, 0)</span></span>    | <span data-ttu-id="64f9b-112">(200, 20)</span><span class="sxs-lookup"><span data-stu-id="64f9b-112">(200, 20)</span></span>         |
| <span data-ttu-id="64f9b-113">Superior direito (100, 0)</span><span class="sxs-lookup"><span data-stu-id="64f9b-113">Upper-right (100, 0)</span></span> | <span data-ttu-id="64f9b-114">(110, 100)</span><span class="sxs-lookup"><span data-stu-id="64f9b-114">(110, 100)</span></span>        |
| <span data-ttu-id="64f9b-115">Inferior esquerdo (0, 50)</span><span class="sxs-lookup"><span data-stu-id="64f9b-115">Lower-left (0, 50)</span></span>   | <span data-ttu-id="64f9b-116">(250, 30)</span><span class="sxs-lookup"><span data-stu-id="64f9b-116">(250, 30)</span></span>         |



 

<span data-ttu-id="64f9b-117">A ilustração a seguir mostra a imagem original e a imagem mapeada para o paralelogramo.</span><span class="sxs-lookup"><span data-stu-id="64f9b-117">The following illustration shows the original image and the image mapped to the parallelogram.</span></span> <span data-ttu-id="64f9b-118">A imagem original foi distorcida, refletida, girada e movida.</span><span class="sxs-lookup"><span data-stu-id="64f9b-118">The original image has been skewed, reflected, rotated, and translated.</span></span> <span data-ttu-id="64f9b-119">O eixo x ao longo da borda superior da imagem original é mapeado para a linha que percorre (200, 20) e (110, 100).</span><span class="sxs-lookup"><span data-stu-id="64f9b-119">The x-axis along the top edge of the original image is mapped to the line that runs through (200, 20) and (110, 100).</span></span> <span data-ttu-id="64f9b-120">O eixo y ao longo da borda esquerda da imagem original é mapeado para a linha que percorre (200, 20) e (250, 30).</span><span class="sxs-lookup"><span data-stu-id="64f9b-120">The y-axis along the left edge of the original image is mapped to the line that runs through (200, 20) and (250, 30).</span></span>

![ilustração mostrando faixas coloridas na origem dos eixos de coordenadas e nas mesmas faixas inclinadas e em um local, rotação e tamanho diferentes](images/stripes1.png)

<span data-ttu-id="64f9b-122">O exemplo a seguir produz as imagens mostradas na ilustração anterior.</span><span class="sxs-lookup"><span data-stu-id="64f9b-122">The following example produces the images shown in the preceding illustration.</span></span>


```
Point destinationPoints[] = {
   Point(200, 20),   // destination for upper-left point of original
   Point(110, 100),  // destination for upper-right point of original
   Point(250, 30)};  // destination for lower-left point of original
Image image(L"Stripes.bmp");
// Draw the image unaltered with its upper-left corner at (0, 0).
graphics.DrawImage(&image, 0, 0);
// Draw the image mapped to the parallelogram.
graphics.DrawImage(&image, destinationPoints, 3); 
```



<span data-ttu-id="64f9b-123">A ilustração a seguir mostra uma transformação semelhante aplicada a uma imagem fotográfica.</span><span class="sxs-lookup"><span data-stu-id="64f9b-123">The following illustration shows a similar transformation applied to a photographic image.</span></span>

![ilustração mostrando a mesma foto duas vezes; o segundo é invertido, inclinado, e tem tamanho, rotação e local diferentes](images/transformedclimber.png)

<span data-ttu-id="64f9b-125">A ilustração a seguir mostra uma transformação semelhante aplicada a um metarquivo.</span><span class="sxs-lookup"><span data-stu-id="64f9b-125">The following illustration shows a similar transformation applied to a metafile.</span></span>

![ilustração mostrando formas e texto, em seguida, novamente, mas invertido, inclinado e com localização, rotação e tamanho diferentes](images/transformedmetafile.png)

 

 



