---
description: O estado de gráficos &\# 8212; região de recorte, transformações e configurações de qualidade &\# 8212; é armazenado em um objeto de gráfico.
ms.assetid: 98b9fa12-02e7-42bf-9cbd-03ee696188f6
title: Contêineres de elementos gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8bf6469d0835137be1bb76b7727fd961bba16b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551957"
---
# <a name="graphics-containers"></a>Contêineres de elementos gráficos

Estado de gráficos — região de recorte, transformações e configurações de qualidade — é armazenado em um objeto de [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . O Windows GDI+ permite que você substitua temporariamente ou aumente parte do estado em um objeto **gráfico** usando um contêiner. Você inicia um contêiner chamando o método [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) de um objeto **Graphics** e encerra um contêiner chamando o método [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) . Entre os **elementos gráficos:: BeginContainer** e **Graphics:: EndContainer**, todas as alterações de estado feitas no objeto **gráfico** pertencem ao contêiner e não substituem o estado existente do objeto **Graphics** .

O exemplo a seguir cria um contêiner dentro de um objeto de [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . A transformação mundial do objeto **gráfico** é uma tradução de 200 unidades à direita, e a transformação mundial do contêiner é uma tradução 100 unidades para baixo.


```
myGraphics.TranslateTransform(200.0f, 0.0f);

myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.TranslateTransform(0.0f, 100.0f);
   myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
myGraphics.EndContainer(myGraphicsContainer);

myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
```



Observe que no exemplo anterior, a instrução `myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50)` feita entre as chamadas para [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) e [**gráficos:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) produz um retângulo diferente da mesma instrução feita após a chamada para **Graphics:: EndContainer**. Somente a tradução horizontal se aplica à chamada **DrawRectangle** feita fora do contêiner. Ambas as transformações — a tradução horizontal de 200 unidades e a tradução vertical de 100 unidades — aplicam-se à chamada [**Graphics::D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) feitas dentro do contêiner. A ilustração a seguir mostra os dois retângulos.

![captura de tela de uma janela com dois retângulos desenhados com uma caneta azul, um posicionado acima do outro](images/aboutgdip05-art17.png)

Os contêineres podem ser aninhados em contêineres. O exemplo a seguir cria um contêiner dentro de um objeto de [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e outro contêiner dentro do primeiro contêiner. A transformação mundial do objeto **gráfico** é uma tradução 100 unidades na direção x e 80 unidades na direção y. A transformação mundial do primeiro contêiner é uma rotação de 30 graus. A transformação mundial do segundo contêiner é um dimensionamento por um fator de 2 na direção x. Uma chamada para o método [**Graphics::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) é feita dentro do segundo contêiner.


```
myGraphics.TranslateTransform(100.0f, 80.0f, MatrixOrderAppend);

container1 = myGraphics.BeginContainer();
   myGraphics.RotateTransform(30.0f, MatrixOrderAppend);

   container2 = myGraphics.BeginContainer();
      myGraphics.ScaleTransform(2.0f, 1.0f);
      myGraphics.DrawEllipse(&myPen, -30, -20, 60, 40);
   myGraphics.EndContainer(container2);

myGraphics.EndContainer(container1);
```



A ilustração a seguir mostra a elipse.

![captura de tela de uma janela que contém uma elipse azul girada com seu centro rotulado como (100, 80)](images/aboutgdip05-art18.png)

Observe que todas as três transformações se aplicam à chamada [**Graphics::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) feitas no segundo contêiner (interno). Observe também a ordem das transformações: primeira escala, em seguida, girar e depois converter. A transformação mais interna é aplicada primeiro e a transformação externa é aplicada por último.

Qualquer propriedade de um objeto de [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) pode ser definida dentro de um contêiner (entre chamadas para [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) e [**Graphics:: nocontainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)). Por exemplo, uma região de recorte pode ser definida dentro de um contêiner. Qualquer desenho feito dentro do contêiner será restrito à região de recorte desse contêiner e também será restrito às regiões de recorte de todos os contêineres externos e à região de recorte do objeto **gráfico** em si.

As propriedades discutidas até agora – a transformação do mundo e a região de recorte — são combinadas por contêineres aninhados. Outras propriedades são temporariamente substituídas por um contêiner aninhado. Por exemplo, se você definir o modo de suavização como SmoothingModeAntiAlias dentro de um contêiner, os métodos de desenho chamados dentro desse contêiner usarão o modo de suavização de antialias, mas os métodos de desenho chamados após [**Graphics:: Nocontainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) usarão o modo de suavização que estava em vigor antes da chamada para [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).

Para obter outro exemplo de como combinar as transformações mundiais de um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e um contêiner, suponha que você queira desenhar um olho e colocá-lo em vários locais em uma sequência de rostos. O exemplo a seguir desenha um olho centralizado na origem do sistema de coordenadas.


```
void DrawEye(Graphics* pGraphics)
{
   GraphicsContainer eyeContainer;
   
   eyeContainer = pGraphics->BeginContainer();

      Pen myBlackPen(Color(255, 0, 0, 0));
      SolidBrush myGreenBrush(Color(255, 0, 128, 0));
      SolidBrush myBlackBrush(Color(255, 0, 0, 0));

      GraphicsPath myTopPath;
      myTopPath.AddEllipse(-30, -50, 60, 60);

      GraphicsPath myBottomPath;
      myBottomPath.AddEllipse(-30, -10, 60, 60);

      Region myTopRegion(&myTopPath);
      Region myBottomRegion(&myBottomPath);

      // Draw the outline of the eye.
      // The outline of the eye consists of two ellipses.
      // The top ellipse is clipped by the bottom ellipse, and
      // the bottom ellipse is clipped by the top ellipse.
      pGraphics->SetClip(&myTopRegion);
      pGraphics->DrawPath(&myBlackPen, &myBottomPath);
      pGraphics->SetClip(&myBottomRegion);
      pGraphics->DrawPath(&myBlackPen, &myTopPath);

      // Fill the iris.
      // The iris is clipped by the bottom ellipse.
      pGraphics->FillEllipse(&myGreenBrush, -10, -15, 20, 22);

      // Fill the pupil.
      pGraphics->FillEllipse(&myBlackBrush, -3, -7, 6, 9);

   pGraphics->EndContainer(eyeContainer);
}
```



A ilustração a seguir mostra os eixos de olho e de coordenadas.

![ilustração mostrando um olho composto de três elipses: uma para a estrutura de tópicos, íris e Pupil](images/aboutgdip05-art19.png)

A função DrawEye, definida no exemplo anterior, recebe o endereço de um objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e cria imediatamente um contêiner dentro desse objeto **Graphics** . Esse contêiner separa qualquer código que chame a função DrawEye das configurações de propriedade feitas durante a execução da função DrawEye. Por exemplo, o código na função DrawEye define a região de recorte do objeto **Graphics** , mas quando DrawEye retorna o controle para a rotina de chamada, a região de recorte será como era antes da chamada para DrawEye.

O exemplo a seguir desenha três elipses (rostos), cada uma com um olho dentro.


```
// Draw an ellipse with center at (100, 100).
myGraphics.TranslateTransform(100.0f, 100.0f);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Draw the eye at the center of the ellipse.
DrawEye(&myGraphics);

// Draw an ellipse with center at 200, 100.
myGraphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Rotate the eye 40 degrees, and draw it 30 units above
// the center of the ellipse.
myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.RotateTransform(-40.0f);
   myGraphics.TranslateTransform(0.0f, -30.0f, MatrixOrderAppend);
   DrawEye(&myGraphics);
myGraphics.EndContainer(myGraphicsContainer);

// Draw a ellipse with center at (300.0f, 100.0f).
myGraphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Stretch and rotate the eye, and draw it at the 
// center of the ellipse.
myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.ScaleTransform(2.0f, 1.5f);
   myGraphics.RotateTransform(45.0f, MatrixOrderAppend);
   DrawEye(&myGraphics);
myGraphics.EndContainer(myGraphicsContainer);
```



A ilustração a seguir mostra as três reticências.

![captura de tela de uma janela com três elipses, cada uma delas contendo um olho em um tamanho e uma rotação diferentes](images/aboutgdip05-art20.png)

No exemplo anterior, todas as reticências são desenhadas com a chamada `DrawEllipse(&myBlackPen, -40, -60, 80, 120)` , que desenha uma elipse centralizada na origem do sistema de coordenadas. As reticências são movidas para fora do canto superior esquerdo da área do cliente, definindo a transformação mundial do objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . A instrução faz com que a primeira elipse seja centralizada em (100, 100). A instrução faz com que o centro da segunda elipse seja de 100 unidades à direita do centro da primeira elipse. Da mesma forma, o centro da terceira elipse é de 100 unidades à direita do centro da segunda elipse.

Os contêineres no exemplo anterior são usados para transformar o olho em relação ao centro de uma determinada elipse. O primeiro olho é desenhado no centro da elipse sem transformação, portanto, a chamada DrawEye não está dentro de um contêiner. O segundo olho é girado em 40 graus e desenhado em 30 unidades acima do centro da elipse, portanto, a função DrawEye e os métodos que definem a transformação são chamados dentro de um contêiner. O terceiro olho é alongado e girado e desenhado no centro da elipse. Como no segundo olho, a função DrawEye e os métodos que definem a transformação são chamados dentro de um contêiner.

 

 
