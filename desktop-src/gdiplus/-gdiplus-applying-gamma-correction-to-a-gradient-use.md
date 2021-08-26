---
description: Você pode habilitar a correção gama para um pincel de gradiente passando TRUE para o método PathGradientBrush::SetGammaCorrection desse pincel.
ms.assetid: 47472e41-f469-44f4-8b39-cf3982b79f9e
title: Aplicando a correção gama a um gradiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eae76306e5c68804d76777d9fc80c65d06904702487a8b60f80659b9d16a96ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888536"
---
# <a name="applying-gamma-correction-to-a-gradient"></a>Aplicando a correção gama a um gradiente

Você pode habilitar a correção gama para um pincel de gradiente passando **TRUE** para o [**método PathGradientBrush::SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) desse pincel. Você pode desabilitar a correção gama passando **FALSE** para o **método PathGradientBrush::SetGammaCorrection.** A correção gama está desabilitada por padrão.

O exemplo a seguir cria um pincel de gradiente linear e usa esse pincel para preencher dois retângulos. O primeiro retângulo é preenchido sem correção gama e o segundo retângulo é preenchido com correção gama.


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 255, 0, 0),   // Opaque red
   Color(255, 0, 0, 255));  // Opaque blue

graphics.FillRectangle(&linGrBrush, 0, 0, 200, 50);
linGrBrush.SetGammaCorrection(TRUE);
graphics.FillRectangle(&linGrBrush, 0, 60, 200, 50); 
```



A ilustração a seguir mostra os dois retângulos preenchidos. O retângulo superior, que não tem correção gama, aparece escuro no meio. O retângulo inferior, que tem correção gama, parece ter uma intensidade mais uniforme.

![ilustração mostrando dois retângulos: o preenchimento colorido do primeiro varia de intensidade, o preenchimento do segundo varia menos](images/gammagradient1.png)

O exemplo a seguir cria um pincel de gradiente de caminho com base em um caminho em forma de estrela. O código usa o pincel de gradiente de caminho com a correção gama desabilitada (o padrão) para preencher o caminho. Em seguida, o código passa **TRUE** para o [**método PathGradientBrush::SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) para habilitar a correção gama para o pincel de gradiente de caminho. A chamada para [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) define a transformação mundial de um objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para que a chamada subsequente a [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) preencha uma estrela que fica à direita da primeira estrela.


```
// Put the points of a polygon in an array.
Point points[] = {Point(75, 0), Point(100, 50), 
                  Point(150, 50), Point(112, 75),
                  Point(150, 150), Point(75, 100), 
                  Point(0, 150), Point(37, 75), 
                  Point(0, 50), Point(50, 50)};

// Use the array of points to construct a path.
GraphicsPath path;
path.AddLines(points, 10);

// Use the path to construct a path gradient brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to red.
pthGrBrush.SetCenterColor(Color(255, 255, 0, 0));

// Set the colors of the points in the array.
Color colors[] = {Color(255, 0, 0, 0),   Color(255, 0, 255, 0),
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255), 
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0), 
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255),
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0)};

int count = 10;
pthGrBrush.SetSurroundColors(colors, &count);

// Fill the path with the path gradient brush.
graphics.FillPath(&pthGrBrush, &path);
pthGrBrush.SetGammaCorrection(TRUE);
graphics.TranslateTransform(200.0f, 0.0f);
graphics.FillPath(&pthGrBrush, &path);
```



A ilustração a seguir mostra a saída do código anterior. A estrela à direita tem correção gama. Observe que a estrela à esquerda, que não tem correção gama, tem áreas que parecem escuras.

![ilustração de dois inícios de cinco pontos com preenchimento de gradiente colorido; o primeiro tem áreas escuras, o segundo não](images/gammagradient2.png)

 

 



