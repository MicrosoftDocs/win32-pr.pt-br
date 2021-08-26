---
description: As seções a seguir descrevem vários dos novos recursos no Windows GDI+.
ms.assetid: 0257a23c-560e-472e-863a-6ab5881dc156
title: Novos recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab303cd00f494e06d7567d93c9698878e02d178a7b4f31d230a4b47cafe279b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014856"
---
# <a name="new-features"></a>Novos recursos

As seções a seguir descrevem vários dos novos recursos no Windows GDI+.

-   [Pincéis de Gradiente](#gradient-brushes)
-   [Splines cardinais](#cardinal-splines)
-   [Objetos de caminho independentes](#independent-path-objects)
-   [Transformações e o objeto de matriz](#transformations-and-the-matrix-object)
-   [Regiões escalonáveis](#scalable-regions)
-   [Combinação alfa](#alpha-blending)
-   [Suporte para vários formatos de imagem](#support-for-multiple-image-formats)

## <a name="gradient-brushes"></a>Pincéis de Gradiente

GDI+ se expande Windows Graphics Device Interface (GDI) fornecendo gradiente linear e pincéis de gradiente de caminho para preencher formas, caminhos e regiões. Pincéis de gradiente também podem ser usados para desenhar linhas, curvas e caminhos. Quando você preenche uma forma com um pincel de gradiente linear, a cor muda gradualmente conforme você se move pela forma. Por exemplo, suponha que você crie um pincel de gradiente horizontal especificando azul na borda esquerda de uma forma e verde na borda direita. Quando você preencher essa forma com o pincel de gradiente horizontal, ele mudará gradualmente de azul para verde conforme você se move da borda esquerda para a borda direita. Da mesma forma, uma forma preenchida com um pincel de gradiente vertical mudará de cor conforme você se move de cima para baixo. A ilustração a seguir mostra uma elipse preenchida com um pincel de gradiente horizontal e uma região preenchida com um pincel de gradiente diagonal.

![ilustração de uma forma preenchida por um gradiente horizontal e uma arquivada por um gradiente diagonal](images/aboutgdip01-art01.png)

Ao preencher uma forma com um pincel de gradiente de caminho, você tem uma variedade de opções para especificar como as cores mudam conforme você se move de uma parte da forma para outra. Uma opção é ter uma cor central e uma cor de limite para que os pixels mudem gradualmente de uma cor para outra à medida que você se move do meio da forma para as bordas externas. A ilustração a seguir mostra um caminho (criado com um par de splines Bézier) preenchido com um pincel de gradiente de caminho.

![ilustração de uma forma semelhante a um sinal de infinito, preenchido do azul em que as metades se encontram até o azul nas bordas](images/aboutgdip01-art02.png)

## <a name="cardinal-splines"></a>Splines cardinais

GDI+ dá suporte a splines cardinais, que não têm suporte na GDI. Um spline cardinal é uma sequência de curvas individuais unidas para formar uma curva maior. O spline é especificado por uma matriz de pontos e passa por cada ponto nessa matriz. Um spline cardinal passa sem problemas (sem cantos nítidos) por cada ponto na matriz e, portanto, é mais refinado do que um caminho criado conectando linhas retas. A ilustração a seguir mostra dois caminhos, um criado conectando linhas retas e um criado como um spline cardinal.

![ilustração mostrando os mesmos cinco pontos duas vezes: uma vez conectada por um spline cardinal, a outra por segmentos de linha](images/aboutgdip01-art03.png)

## <a name="independent-path-objects"></a>Objetos de caminho independentes

Na GDI, um caminho pertence a um contexto de dispositivo e o caminho é destruído conforme ele é desenhado. Com GDI+, o desenho é executado por um objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e você pode criar e manter vários [**objetos GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) separados do **objeto Graphics.** Um **objeto GraphicsPath** não é destruído pela ação de desenho, portanto, você pode usar o mesmo **objeto GraphicsPath** para desenhar um caminho várias vezes.

## <a name="transformations-and-the-matrix-object"></a>Transformações e o objeto de matriz

GDI+ fornece o [**objeto Matrix,**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) uma ferramenta poderosa que torna as transformações (rotações, traduções e assim por diante) fáceis e flexíveis. Um objeto de matriz funciona em conjunto com os objetos que são transformados. Por exemplo, um [**objeto GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) tem um [**método GraphicsPath::Transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) que recebe o endereço de um objeto **Matrix** como um argumento. Uma única matriz 3×3 pode armazenar uma transformação ou uma sequência de transformações. A ilustração a seguir mostra um caminho antes e depois de uma sequência de duas transformações (primeira escala, depois girar).

![ilustração mostrando o contorno de uma forma e, em seguida, o mesmo contorno, mas mais estreito e girado](images/aboutgdip01-art04.png)

## <a name="scalable-regions"></a>Regiões escalonáveis

GDI+ se expande muito na GDI com seu suporte para regiões. Na GDI, as regiões são armazenadas em coordenadas de dispositivo e a única transformação que pode ser aplicada a uma região é uma tradução. GDI+ armazena regiões no mundo coordenadas e permite que uma região seja submetida a qualquer transformação (dimensionamento, por exemplo) que possa ser armazenada em uma matriz de transformação. A ilustração a seguir mostra uma região antes e depois de uma sequência de três transformações: dimensionar, girar e converter.

![ilustração mostrando uma forma centralizada em eixos de coordenadas, em seguida, com a mesma forma, mas maior, girada e traduzida para a direita](images/aboutgdip01-art05.png)

## <a name="alpha-blending"></a>Combinação alfa

Observe que, na figura anterior, você pode ver a região nãotransformada (preenchida com vermelho) pela região transformada (preenchida com um pincel de hatch). Isso é possibilitado pela combinação alfa, que é suportada por GDI+. Com a combinação alfa, você pode especificar a transparência de uma cor de preenchimento. Uma cor transparente é mesclada com a cor da tela de fundo – quanto mais transparente você fizer uma cor de preenchimento, mais a tela de fundo mostrará. A ilustração a seguir mostra quatro re elipses que são preenchidas com a mesma cor (vermelho) em diferentes níveis de transparência.

![ilustração mostrando quatro re elipses de transparência variável sobrepondo um retângulo semi transparente](images/aboutgdip01-art06.png)

## <a name="support-for-multiple-image-formats"></a>Suporte para vários formatos de imagem

GDI+ fornece as classes [**Image,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)e [**Metafile,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) que permitem carregar, salvar e manipular imagens em uma variedade de formatos. Os formatos a seguir são suportados:

-   BMP
-   GIF
-   JPEG
-   Exif
-   PNG
-   TIFF
-   ICON
-   WINDOWS MANAGEMENT FRAMEWORK
-   EMF

 

 



