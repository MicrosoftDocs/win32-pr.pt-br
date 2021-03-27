---
description: As seções a seguir descrevem vários dos novos recursos do Windows GDI+.
ms.assetid: 0257a23c-560e-472e-863a-6ab5881dc156
title: Novos recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca79ddb4cabd14cc2eaa2493033a78cc7377f8e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647109"
---
# <a name="new-features"></a>Novos recursos

As seções a seguir descrevem vários dos novos recursos do Windows GDI+.

-   [Pincéis de Gradiente](#gradient-brushes)
-   [Linhas Cardeal](#cardinal-splines)
-   [Objetos de caminho independentes](#independent-path-objects)
-   [Transformações e o objeto de matriz](#transformations-and-the-matrix-object)
-   [Regiões escalonáveis](#scalable-regions)
-   [Mesclagem alfa](#alpha-blending)
-   [Suporte para vários formatos de imagem](#support-for-multiple-image-formats)

## <a name="gradient-brushes"></a>Pincéis de Gradiente

O GDI+ expande o Windows Graphics Device Interface (GDI) fornecendo pincéis de gradiente linear e de gradiente de caminho para preencher formas, caminhos e regiões. Os pincéis de gradiente também podem ser usados para desenhar linhas, curvas e caminhos. Quando você preenche uma forma com um pincel de gradiente linear, a cor muda gradualmente à medida que você se move pela forma. Por exemplo, suponha que você crie um pincel de gradiente horizontal especificando azul na borda esquerda de uma forma e verde na borda direita. Quando você preencher essa forma com o pincel de gradiente horizontal, ele mudará gradualmente de azul para verde à medida que você mudar de sua borda esquerda para sua borda direita. Da mesma forma, uma forma preenchida com um pincel de gradiente vertical mudará a cor à medida que você passar de cima para baixo. A ilustração a seguir mostra uma elipse preenchida com um pincel de gradiente horizontal e uma região preenchida com um pincel de gradiente diagonal.

![ilustração de uma forma preenchida por um gradiente horizontal e uma registrada por um gradiente diagonal](images/aboutgdip01-art01.png)

Ao preencher uma forma com um pincel de gradiente de caminho, você tem uma variedade de opções para especificar como as cores são alteradas à medida que você passa de uma parte da forma para outra. Uma opção é ter uma cor central e uma cor de limite para que os pixels mudem gradualmente de uma cor para a outra à medida que você move do meio da forma para as bordas externas. A ilustração a seguir mostra um caminho (criado a partir de um par de linhas de Bézier) preenchido com um pincel de gradiente de caminho.

![ilustração de uma forma semelhante a um sinal de infinito, preenchida em azul onde as metades se encontram para a água nas bordas](images/aboutgdip01-art02.png)

## <a name="cardinal-splines"></a>Linhas Cardeal

O GDI+ dá suporte a polilinhas Cardeal, que não têm suporte em GDI. Um spline cardinal é uma sequência de curvas individuais unidas para formar uma curva maior. O spline é especificado por uma matriz de pontos e passa por cada ponto nessa matriz. Um spline Cardinal passa suavemente (sem cantos nítidos) por cada ponto na matriz e, portanto, é mais refinado do que um caminho criado pela conexão de linhas retas. A ilustração a seguir mostra dois caminhos, um criado pela conexão de linhas retas e um criado como um spline cardinal.

![ilustração mostrando os mesmos cinco pontos duas vezes: uma vez conectado por um spline Cardinal, o outro por segmentos de linha](images/aboutgdip01-art03.png)

## <a name="independent-path-objects"></a>Objetos de caminho independentes

No GDI, um caminho pertence a um contexto de dispositivo e o caminho é destruído conforme é desenhado. Com o GDI+, o desenho é executado por um objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , e você pode criar e manter vários objetos [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) separados do objeto **Graphics** . Um objeto **GraphicsPath** não é destruído pela ação de desenho, portanto, você pode usar o mesmo objeto **GraphicsPath** para desenhar um caminho várias vezes.

## <a name="transformations-and-the-matrix-object"></a>Transformações e o objeto de matriz

O GDI+ fornece o objeto [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) , uma ferramenta poderosa que torna as transformações (rotações, traduções etc.) fáceis e flexíveis. Um objeto de matriz funciona em conjunto com os objetos que são transformados. Por exemplo, um objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) tem um método [**GraphicsPath:: Transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) que recebe o endereço de um objeto **Matrix** como um argumento. Uma única matriz 3 × 3 pode armazenar uma transformação ou uma sequência de transformações. A ilustração a seguir mostra um caminho antes e depois de uma sequência de duas transformações (primeira escala e, em seguida, girar).

![ilustração mostrando o contorno de uma forma e, em seguida, a mesma estrutura de tópicos, mas mais estreita e girada](images/aboutgdip01-art04.png)

## <a name="scalable-regions"></a>Regiões escalonáveis

A GDI+ expande enormemente o GDI com seu suporte para regiões. No GDI, as regiões são armazenadas em coordenadas de dispositivo e a única transformação que pode ser aplicada a uma região é uma tradução. O GDI+ armazena regiões em coordenadas mundiais e permite que uma região passe por qualquer transformação (dimensionamento, por exemplo) que possa ser armazenada em uma matriz de transformação. A ilustração a seguir mostra uma região antes e depois de uma sequência de três transformações: escala, rotação e conversão.

![ilustração mostrando uma forma centralizada em eixos de coordenadas, em seguida, a mesma forma, mas maior, girada e convertida à direita](images/aboutgdip01-art05.png)

## <a name="alpha-blending"></a>Mesclagem alfa

Observe que, na figura anterior, você pode ver a região não transformada (preenchida com vermelho) por meio da região transtransformada (preenchida com um pincel de hachura). Isso se torna possível pela mistura alfa, que é suportada pelo GDI+. Com a mistura alfa, você pode especificar a transparência de uma cor de preenchimento. Uma cor transparente é mesclada com a cor do plano de fundo — quanto mais transparente você fizer uma cor de preenchimento, mais o plano de fundo será exibido. A ilustração a seguir mostra quatro elipses que são preenchidas com a mesma cor (vermelho) em diferentes níveis de transparência.

![ilustração mostrando quatro elipses de transparência variável sobrepondo um retângulo semitransparente](images/aboutgdip01-art06.png)

## <a name="support-for-multiple-image-formats"></a>Suporte para vários formatos de imagem

O GDI+ fornece a [**imagem**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), o [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)e as classes de [**metarquivo**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) , que permitem carregar, salvar e manipular imagens em uma variedade de formatos. Há suporte para os seguintes formatos:

-   BMP
-   GIF
-   JPEG
-   Exif
-   PNG
-   TIFF
-   ICON
-   WINDOWS MANAGEMENT FRAMEWORK
-   EMF

 

 



