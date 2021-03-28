---
description: O Windows GDI+ fornece a imagem e as classes de bitmap para armazenar e manipular imagens.
ms.assetid: fcd7f3d9-8bad-44f8-8c9c-c2f5df4a7241
title: Uso de uma matriz de cores para transformar uma única cor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db56d0a64c36c08a5415d76e3fb184158d473268
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104561547"
---
# <a name="using-a-color-matrix-to-transform-a-single-color"></a><span data-ttu-id="01114-103">Uso de uma matriz de cores para transformar uma única cor</span><span class="sxs-lookup"><span data-stu-id="01114-103">Using a Color Matrix to Transform a Single Color</span></span>

<span data-ttu-id="01114-104">O Windows GDI+ fornece a [**imagem**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) e as classes de [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) para armazenar e manipular imagens.</span><span class="sxs-lookup"><span data-stu-id="01114-104">Windows GDI+ provides the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) and [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) classes for storing and manipulating images.</span></span> <span data-ttu-id="01114-105">Objetos de **imagem** e **bitmap** armazenam a cor de cada pixel como um número de 32 bits: 8 bits cada para vermelho, verde, azul e alfa.</span><span class="sxs-lookup"><span data-stu-id="01114-105">**Image** and **Bitmap** objects store the color of each pixel as a 32-bit number: 8 bits each for red, green, blue, and alpha.</span></span> <span data-ttu-id="01114-106">Cada um dos quatro componentes é um número de 0 a 255, sendo que 0 representa nenhuma intensidade e 255 representa intensidade total.</span><span class="sxs-lookup"><span data-stu-id="01114-106">Each of the four components is a number from 0 through 255, with 0 representing no intensity and 255 representing full intensity.</span></span> <span data-ttu-id="01114-107">O componente alfa especifica a transparência da cor: 0 é completamente transparente e 255 é totalmente opaca.</span><span class="sxs-lookup"><span data-stu-id="01114-107">The alpha component specifies the transparency of the color: 0 is fully transparent, and 255 is fully opaque.</span></span>

<span data-ttu-id="01114-108">Um vetor de cor é uma tupla de 4 do formulário (vermelho, verde, azul, alfa).</span><span class="sxs-lookup"><span data-stu-id="01114-108">A color vector is a 4-tuple of the form (red, green, blue, alpha).</span></span> <span data-ttu-id="01114-109">Por exemplo, o vetor de cor (0, 255, 0, 255) representa uma cor opaca que não tem nenhum vermelho nem azul, mas tem verde na intensidade total.</span><span class="sxs-lookup"><span data-stu-id="01114-109">For example, the color vector (0, 255, 0, 255) represents an opaque color that has no red or blue, but has green at full intensity.</span></span>

<span data-ttu-id="01114-110">Outra Convenção para representar cores usa o número 1 para intensidade máxima e o número 0 para intensidade mínima.</span><span class="sxs-lookup"><span data-stu-id="01114-110">Another convention for representing colors uses the number 1 for maximum intensity and the number 0 for minimum intensity.</span></span> <span data-ttu-id="01114-111">Usando essa convenção, a cor descrita no parágrafo anterior seria representada pelo vetor (0, 1, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="01114-111">Using that convention, the color described in the preceding paragraph would be represented by the vector (0, 1, 0, 1).</span></span> <span data-ttu-id="01114-112">A GDI+ usa a Convenção de 1 como intensidade total quando executa transformações de cor.</span><span class="sxs-lookup"><span data-stu-id="01114-112">GDI+ uses the convention of 1 as full intensity when it performs color transformations.</span></span>

<span data-ttu-id="01114-113">Você pode aplicar transformações lineares (rotação, dimensionamento e similares) a vetores de cor multiplicando por uma matriz 4 × 4.</span><span class="sxs-lookup"><span data-stu-id="01114-113">You can apply linear transformations (rotation, scaling, and the like) to color vectors by multiplying by a 4 ×4 matrix.</span></span> <span data-ttu-id="01114-114">No entanto, você não pode usar uma matriz 4 × 4 para executar uma conversão (não linear).</span><span class="sxs-lookup"><span data-stu-id="01114-114">However, you cannot use a 4 ×4 matrix to perform a translation (nonlinear).</span></span> <span data-ttu-id="01114-115">Se você adicionar uma quinta coordenada fictícia (por exemplo, o número 1) a cada um dos vetores de cor, poderá usar uma matriz de 5 × 5 para aplicar qualquer combinação de transformações e traduções lineares.</span><span class="sxs-lookup"><span data-stu-id="01114-115">If you add a dummy fifth coordinate (for example, the number 1) to each of the color vectors, you can use a 5 ×5 matrix to apply any combination of linear transformations and translations.</span></span> <span data-ttu-id="01114-116">Uma transformação que consiste em uma transformação linear seguida por uma translação é chamada de transformação afim.</span><span class="sxs-lookup"><span data-stu-id="01114-116">A transformation consisting of a linear transformation followed by a translation is called an affine transformation.</span></span> <span data-ttu-id="01114-117">Uma matriz de 5 × 5 que representa uma transformação afim é chamada de matriz homogênea para uma transformação de 4 espaços.</span><span class="sxs-lookup"><span data-stu-id="01114-117">A 5 ×5 matrix that represents an affine transformation is called a homogeneous matrix for a 4-space transformation.</span></span> <span data-ttu-id="01114-118">O elemento na quinta linha e quinta coluna de uma matriz homogênea de 5 × 5 deve ser 1 e todas as outras entradas na quinta coluna devem ser 0.</span><span class="sxs-lookup"><span data-stu-id="01114-118">The element in the fifth row and fifth column of a 5 ×5 homogeneous matrix must be 1, and all of the other entries in the fifth column must be 0.</span></span>

<span data-ttu-id="01114-119">Por exemplo, suponha que você queira começar com a cor (0,2, 0,0, 0,4, 1,0) e aplicar as seguintes transformações:</span><span class="sxs-lookup"><span data-stu-id="01114-119">For example, suppose you want to start with the color (0.2, 0.0, 0.4, 1.0) and apply the following transformations:</span></span>

1.  <span data-ttu-id="01114-120">Duplicar o componente vermelho</span><span class="sxs-lookup"><span data-stu-id="01114-120">Double the red component</span></span>
2.  <span data-ttu-id="01114-121">Adicionar 0,2 aos componentes vermelhos, verdes e azuis</span><span class="sxs-lookup"><span data-stu-id="01114-121">Add 0.2 to the red, green, and blue components</span></span>

<span data-ttu-id="01114-122">A multiplicação de matriz a seguir executará o par de transformações na ordem listada.</span><span class="sxs-lookup"><span data-stu-id="01114-122">The following matrix multiplication will perform the pair of transformations in the order listed.</span></span>

![ilustração mostrando uma matriz 5x1 de números multiplicada por uma matriz 5x5 para criar uma nova matriz 5x1](images/recoloring01.png)

<span data-ttu-id="01114-124">Os elementos de uma matriz de cores são indexados (baseados em zero) por linha e coluna.</span><span class="sxs-lookup"><span data-stu-id="01114-124">The elements of a color matrix are indexed (zero-based) by row and then column.</span></span> <span data-ttu-id="01114-125">Por exemplo, a entrada na quinta linha e a terceira coluna da matriz M é denotada por M \[ 4 \] \[ 2 \] .</span><span class="sxs-lookup"><span data-stu-id="01114-125">For example, the entry in the fifth row and third column of matrix M is denoted by M\[4\]\[2\].</span></span>

<span data-ttu-id="01114-126">A matriz de identidade 5 × 5 (mostrada na ilustração a seguir) tem 1s na diagonal e 0s em todos os outros lugares.</span><span class="sxs-lookup"><span data-stu-id="01114-126">The 5 ×5 identity matrix (shown in the following illustration) has 1s on the diagonal and 0s everywhere else.</span></span> <span data-ttu-id="01114-127">Se você multiplicar um vetor de cor pela matriz de identidade, o vetor de cor não mudará.</span><span class="sxs-lookup"><span data-stu-id="01114-127">If you multiply a color vector by the identity matrix, the color vector does not change.</span></span> <span data-ttu-id="01114-128">Uma maneira conveniente de formar a matriz de uma transformação de cor é começar com a matriz de identidade e fazer uma pequena alteração que produza a transformação desejada.</span><span class="sxs-lookup"><span data-stu-id="01114-128">A convenient way to form the matrix of a color transformation is to start with the identity matrix and make a small change that produces the desired transformation.</span></span>

![ilustração mostrando uma matriz de identidade 5x5; 1s na parte superior esquerda para a diagonal inferior direita e 0s em todos os outros lugares](images/recoloring02.png)

<span data-ttu-id="01114-130">Para uma discussão mais detalhada de matrizes e transformações, consulte [Sistemas de coordenadas e transformações](-gdiplus-coordinate-systems-and-transformations-about.md).</span><span class="sxs-lookup"><span data-stu-id="01114-130">For a more detailed discussion of matrices and transformations, see [Coordinate Systems and Transformations](-gdiplus-coordinate-systems-and-transformations-about.md).</span></span>

<span data-ttu-id="01114-131">O exemplo a seguir usa uma imagem toda de uma cor (0,2, 0,0, 0,4, 1,0) e aplica a transformação descrita nos parágrafos anteriores.</span><span class="sxs-lookup"><span data-stu-id="01114-131">The following example takes an image that is all one color (0.2, 0.0, 0.4, 1.0) and applies the transformation described in the preceding paragraphs.</span></span>


```
Image            image(L"InputColor.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   2.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 1.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 1.0f, 0.0f,
   0.2f, 0.2f, 0.2f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10);

graphics.DrawImage(
   &image, 
   Rect(120, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



<span data-ttu-id="01114-132">A ilustração a seguir mostra a imagem original à esquerda e a imagem transformada à direita.</span><span class="sxs-lookup"><span data-stu-id="01114-132">The following illustration shows the original image on the left and the transformed image on the right.</span></span>

![<span data-ttu-id="01114-133">ilustração mostrando um retângulo preenchido por uma cor sólida escura e, em seguida, um preenchido por uma cor sólida mais clara</span><span class="sxs-lookup"><span data-stu-id="01114-133">illustration showing a rectangle filled by a dark solid color and then one filled by a lighter solid color</span></span> ](images/colortrans1.png)

<span data-ttu-id="01114-134">O código no exemplo anterior usa as seguintes etapas para executar a recoloração:</span><span class="sxs-lookup"><span data-stu-id="01114-134">The code in the preceding example uses the following steps to perform the recoloring:</span></span>

1.  <span data-ttu-id="01114-135">Inicializar uma estrutura [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) .</span><span class="sxs-lookup"><span data-stu-id="01114-135">Initialize a [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) structure.</span></span>
2.  <span data-ttu-id="01114-136">Crie um objeto [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) e passe o endereço da estrutura [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) para o método [**ImageAttributes:: SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) do objeto **ImageAttributes** .</span><span class="sxs-lookup"><span data-stu-id="01114-136">Create an [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object and pass the address of the [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) structure to the [**ImageAttributes::SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) method of the **ImageAttributes** object.</span></span>
3.  <span data-ttu-id="01114-137">Passe o endereço do objeto [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) para o método de [métodos DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) de um objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="01114-137">Pass the address of the [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object to the [DrawImage Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) method of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

 

 



