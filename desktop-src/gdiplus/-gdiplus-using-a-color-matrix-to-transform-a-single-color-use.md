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
# <a name="using-a-color-matrix-to-transform-a-single-color"></a>Uso de uma matriz de cores para transformar uma única cor

O Windows GDI+ fornece a [**imagem**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) e as classes de [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) para armazenar e manipular imagens. Objetos de **imagem** e **bitmap** armazenam a cor de cada pixel como um número de 32 bits: 8 bits cada para vermelho, verde, azul e alfa. Cada um dos quatro componentes é um número de 0 a 255, sendo que 0 representa nenhuma intensidade e 255 representa intensidade total. O componente alfa especifica a transparência da cor: 0 é completamente transparente e 255 é totalmente opaca.

Um vetor de cor é uma tupla de 4 do formulário (vermelho, verde, azul, alfa). Por exemplo, o vetor de cor (0, 255, 0, 255) representa uma cor opaca que não tem nenhum vermelho nem azul, mas tem verde na intensidade total.

Outra Convenção para representar cores usa o número 1 para intensidade máxima e o número 0 para intensidade mínima. Usando essa convenção, a cor descrita no parágrafo anterior seria representada pelo vetor (0, 1, 0, 1). A GDI+ usa a Convenção de 1 como intensidade total quando executa transformações de cor.

Você pode aplicar transformações lineares (rotação, dimensionamento e similares) a vetores de cor multiplicando por uma matriz 4 × 4. No entanto, você não pode usar uma matriz 4 × 4 para executar uma conversão (não linear). Se você adicionar uma quinta coordenada fictícia (por exemplo, o número 1) a cada um dos vetores de cor, poderá usar uma matriz de 5 × 5 para aplicar qualquer combinação de transformações e traduções lineares. Uma transformação que consiste em uma transformação linear seguida por uma translação é chamada de transformação afim. Uma matriz de 5 × 5 que representa uma transformação afim é chamada de matriz homogênea para uma transformação de 4 espaços. O elemento na quinta linha e quinta coluna de uma matriz homogênea de 5 × 5 deve ser 1 e todas as outras entradas na quinta coluna devem ser 0.

Por exemplo, suponha que você queira começar com a cor (0,2, 0,0, 0,4, 1,0) e aplicar as seguintes transformações:

1.  Duplicar o componente vermelho
2.  Adicionar 0,2 aos componentes vermelhos, verdes e azuis

A multiplicação de matriz a seguir executará o par de transformações na ordem listada.

![ilustração mostrando uma matriz 5x1 de números multiplicada por uma matriz 5x5 para criar uma nova matriz 5x1](images/recoloring01.png)

Os elementos de uma matriz de cores são indexados (baseados em zero) por linha e coluna. Por exemplo, a entrada na quinta linha e a terceira coluna da matriz M é denotada por M \[ 4 \] \[ 2 \] .

A matriz de identidade 5 × 5 (mostrada na ilustração a seguir) tem 1s na diagonal e 0s em todos os outros lugares. Se você multiplicar um vetor de cor pela matriz de identidade, o vetor de cor não mudará. Uma maneira conveniente de formar a matriz de uma transformação de cor é começar com a matriz de identidade e fazer uma pequena alteração que produza a transformação desejada.

![ilustração mostrando uma matriz de identidade 5x5; 1s na parte superior esquerda para a diagonal inferior direita e 0s em todos os outros lugares](images/recoloring02.png)

Para uma discussão mais detalhada de matrizes e transformações, consulte [Sistemas de coordenadas e transformações](-gdiplus-coordinate-systems-and-transformations-about.md).

O exemplo a seguir usa uma imagem toda de uma cor (0,2, 0,0, 0,4, 1,0) e aplica a transformação descrita nos parágrafos anteriores.


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



A ilustração a seguir mostra a imagem original à esquerda e a imagem transformada à direita.

![ilustração mostrando um retângulo preenchido por uma cor sólida escura e, em seguida, um preenchido por uma cor sólida mais clara ](images/colortrans1.png)

O código no exemplo anterior usa as seguintes etapas para executar a recoloração:

1.  Inicializar uma estrutura [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) .
2.  Crie um objeto [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) e passe o endereço da estrutura [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) para o método [**ImageAttributes:: SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) do objeto **ImageAttributes** .
3.  Passe o endereço do objeto [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) para o método de [métodos DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) de um objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

 

 



