---
description: É difícil de visualizar a rotação em um espaço de cor quadridimensional.
ms.assetid: 099f76a3-2da3-4f2b-8f8d-557d144451dc
title: Cores de rotação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea322179bd4a46021d181abedd1797d6bdda7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827094"
---
# <a name="rotating-colors"></a><span data-ttu-id="49384-103">Cores de rotação</span><span class="sxs-lookup"><span data-stu-id="49384-103">Rotating Colors</span></span>

<span data-ttu-id="49384-104">É difícil de visualizar a rotação em um espaço de cor quadridimensional.</span><span class="sxs-lookup"><span data-stu-id="49384-104">Rotation in a four-dimensional color space is difficult to visualize.</span></span> <span data-ttu-id="49384-105">Podemos pode facilitar a visualização da rotação concordando em manter um dos componentes de cor fixos.</span><span class="sxs-lookup"><span data-stu-id="49384-105">We can make it easier to visualize rotation by agreeing to keep one of the color components fixed.</span></span> <span data-ttu-id="49384-106">Suponha que concordamos em manter o componente alfa fixo em 1 (completamente opaco).</span><span class="sxs-lookup"><span data-stu-id="49384-106">Suppose we agree to keep the alpha component fixed at 1 (fully opaque).</span></span> <span data-ttu-id="49384-107">Em seguida, é possível visualizar um espaço de cores tridimensional com os eixos vermelho, verde e azul como mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="49384-107">Then we can visualize a three-dimensional color space with red, green, and blue axes as shown in the following illustration.</span></span>

![ilustração de uma exibição em perspectiva de um espaço de cores tridimensional com eixos rotulados como vermelho, verde e azul](images/recoloring03.png)

<span data-ttu-id="49384-109">Podemos pensar em uma cor como um ponto no espaço 3D.</span><span class="sxs-lookup"><span data-stu-id="49384-109">A color can be thought of as a point in 3-D space.</span></span> <span data-ttu-id="49384-110">Por exemplo, o ponto (1, 0, 0) no espaço representa a cor vermelha e o ponto (0, 1, 0) no espaço representa a cor verde.</span><span class="sxs-lookup"><span data-stu-id="49384-110">For example, the point (1, 0, 0) in space represents the color red, and the point (0, 1, 0) in space represents the color green.</span></span>

<span data-ttu-id="49384-111">A ilustração a seguir mostra o que significa girar a cor (1, 0, 0) por meio de um ângulo de 60 graus no plano vermelho-verde.</span><span class="sxs-lookup"><span data-stu-id="49384-111">The following illustration shows what it means to rotate the color (1, 0, 0) through an angle of 60 degrees in the Red-Green plane.</span></span> <span data-ttu-id="49384-112">Podemos pensar no giro de um plano paralelo ao plano vermelho-verde como um giro sobre o eixo azul.</span><span class="sxs-lookup"><span data-stu-id="49384-112">Rotation in a plane parallel to the Red-Green plane can be thought of as rotation about the blue axis.</span></span>

![ilustração que mostra o ponto (1, 0, 0) girado 60 graus para (0,5, 0,866, 0)](images/recoloring04.png)

<span data-ttu-id="49384-114">A ilustração a seguir mostra como inicializar uma matriz de cores para executar giros de cada um dos três eixos de coordenadas (vermelho, verde e azul).</span><span class="sxs-lookup"><span data-stu-id="49384-114">The following illustration shows how to initialize a color matrix to perform rotations about each of the three coordinate axes (red, green, blue).</span></span>

![ilustração mostrando matrizes de cores que executam rotações sobre cada um dos três eixos de coordenadas](images/recoloring05.png)

<span data-ttu-id="49384-116">O exemplo a seguir usa uma imagem que aparece em uma cor (1, 0, 0,6) e aplica um giro de 60 graus sobre o eixo azul.</span><span class="sxs-lookup"><span data-stu-id="49384-116">The following example takes an image that is all one color (1, 0, 0.6) and applies a 60-degree rotation about the blue axis.</span></span> <span data-ttu-id="49384-117">O ângulo da rotação é removido em um plano que é paralelo ao plano de Red-Green.</span><span class="sxs-lookup"><span data-stu-id="49384-117">The angle of the rotation is swept out in a plane that is parallel to the Red-Green plane.</span></span>


```
Image            image(L"RotationInput.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();
REAL             degrees = 60;
REAL             pi = acos(-1);  // the angle whose cosine is -1.
REAL             r = degrees * pi / 180;  // degrees to radians

ColorMatrix colorMatrix = {
   cos(r),  sin(r), 0.0f, 0.0f, 0.0f,
   -sin(r), cos(r), 0.0f, 0.0f, 0.0f,
   0.0f,    0.0f,   1.0f, 0.0f, 0.0f,
   0.0f,    0.0f,   0.0f, 1.0f, 0.0f,
   0.0f,    0.0f,   0.0f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(130, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



<span data-ttu-id="49384-118">A ilustração a seguir mostra a imagem original à esquerda e a imagem com giro de cor à direita.</span><span class="sxs-lookup"><span data-stu-id="49384-118">The following illustration shows the original image on the left and the color-rotated image on the right.</span></span>

![ilustração mostrando retângulos preenchidos com a imagem original (violeta vermelha) e imagem girada em cores (verde-marinho)](images/colortrans5.png)

<span data-ttu-id="49384-120">A rotação de cores executada no exemplo de código anterior pode ser visualizada da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="49384-120">The color rotation performed in the preceding code example can be visualized as follows.</span></span>

![ilustração mostrando um espaço de cores 3D e o ponto (1, 0, 0,6) girado 60 graus para (0,5, 0,866, 0,6)](images/recoloring06.png)

 

 



