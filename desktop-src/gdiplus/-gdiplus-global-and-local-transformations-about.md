---
description: Uma transformação global é uma transformação que se aplica a todos os itens desenhados por um determinado objeto gráfico.
ms.assetid: 9f744c2a-f1f3-4a7e-ab0c-37aa1df01623
title: Transformações globais e locais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2682fef6a6236b9da7ec0ec1e5ab5484ad9f90d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563609"
---
# <a name="global-and-local-transformations"></a>Transformações globais e locais

Uma transformação global é uma transformação que se aplica a todos os itens desenhados por um determinado objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Para criar uma transformação global, construa um objeto **Graphics** e, em seguida, chame o método [**gráficos:: SetTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settransform) . O método **Graphics:: SetTransform** manipula um objeto [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) que está associado ao objeto **Graphics** . A transformação armazenada nesse objeto de **matriz** é chamada de *transformação mundial*. A transformação mundial pode ser uma simples transformação afim ou uma sequência complexa de transformações afim, mas independentemente de sua complexidade, a transformação mundial é armazenada em um único objeto **matriz** .

A classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornece vários métodos para criar uma transformação do mundo composto: [**gráficos:: MultiplyTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-multiplytransform), [**Graphics:: RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform), [**Graphics:: ScaleTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-scaletransform)e [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform). O exemplo a seguir desenha uma elipse duas vezes: uma vez antes de criar uma transformação global e outra vez depois. A transformação primeiro é dimensionada por um fator de 0,5 na direção y e, em seguida, move 50 unidades na direção x e gira 30 graus.


```
myGraphics.DrawEllipse(&myPen, 0, 0, 100, 50);
myGraphics.ScaleTransform(1.0f, 0.5f);
myGraphics.TranslateTransform(50.0f, 0.0f, MatrixOrderAppend);
myGraphics.RotateTransform(30.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myPen, 0, 0, 100, 50);
```



A ilustração a seguir mostra a elipse original e a elipse transformada.

![captura de tela de uma janela que contém duas reticências sobrepostas; um é mais estreito e girado](images/aboutgdip05-art14.png)

> [!Note]  
> No exemplo anterior, a elipse é girada sobre a origem do sistema de coordenadas, que está no canto superior esquerdo da área do cliente. Isso produz um resultado diferente de girar a elipse sobre seu próprio centro.

 

Uma transformação local é uma transformação que se aplica a um item específico a ser desenhado. Por exemplo, um objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) tem um método [**GraphicsPath:: Transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) que permite transformar os pontos de dados desse caminho. O exemplo a seguir desenha um retângulo sem transformação e um caminho com uma transformação de rotação. (Suponha que não haja nenhuma transformação global.)


```
 
Matrix myMatrix;
myMatrix.Rotate(45.0f);
myGraphicsPath.Transform(&myMatrix);
myGraphics.DrawRectangle(&myPen, 10, 10, 100, 50);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



Você pode combinar a transformação global com transformações locais para obter uma variedade de resultados. Por exemplo, você pode usar a transformação global para revisar o sistema de coordenadas e usar transformações locais para girar e dimensionar objetos desenhados no novo sistema de coordenadas.

Suponha que você deseje obter um sistema de coordenadas que tenha sua origem 200 pixels da borda esquerda da área de cliente e 150 pixels da parte superior da área de cliente. Além disso, suponha que você deseje que a unidade de medida seja o pixel, com o eixo x apontando para a direita e o eixo y apontando para cima. O sistema de coordenadas padrão tem o eixo y apontando para baixo, assim, você precisa executar uma reflexão no eixo horizontal. A ilustração a seguir mostra a matriz de uma reflexão assim.

![ilustração mostrando uma matriz de três por três](images/aboutgdip05-art15.png)

Em seguida, suponha que você precisa executar uma translação de 200 unidades para a direita e 150 unidades para baixo.

O exemplo a seguir estabelece o sistema de coordenadas que acabou de ser descrito definindo a transformação mundial de um objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .


```
Matrix myMatrix(1.0f, 0.0f, 0.0f, -1.0f, 0.0f, 0.0f);
myGraphics.SetTransform(&myMatrix);
myGraphics.TranslateTransform(200.0f, 150.0f, MatrixOrderAppend);
```



O código a seguir (colocado após o código no exemplo anterior) cria um caminho que consiste em um único retângulo com seu canto inferior esquerdo na origem do novo sistema de coordenadas. O retângulo é preenchido uma vez sem transformação local e uma vez com transformação local. A transformação local consiste em uma colocação em escala horizontal por um fator de 2 seguida por uma rotação de 30 graus.


```
// Create the path.
GraphicsPath myGraphicsPath;
Rect myRect(0, 0, 60, 60);
myGraphicsPath.AddRectangle(myRect);

// Fill the path on the new coordinate system.
// No local transformation
myGraphics.FillPath(&mySolidBrush1, &myGraphicsPath);

// Transform the path.
Matrix myPathMatrix;
myPathMatrix.Scale(2, 1);
myPathMatrix.Rotate(30, MatrixOrderAppend);
myGraphicsPath.Transform(&myPathMatrix);

// Fill the transformed path on the new coordinate system.
myGraphics.FillPath(&mySolidBrush2, &myGraphicsPath);
```



A ilustração a seguir mostra o novo sistema de coordenadas e os dois retângulos.

![captura de tela de um eixo x e y e um quadrado azul sobreposto por um rectagle semitransparente girado em volta do seu canto inferior esquerdo](images/aboutgdip05-art16.png)

 

 



