---
description: 'Você pode habilitar a correção gama para um pincel de gradiente passando TRUE para o método PathGradientBrush:: SetGammaCorrection desse pincel.'
ms.assetid: 47472e41-f469-44f4-8b39-cf3982b79f9e
title: Aplicando a correção gama a um gradiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e51673e8be4fd289286ce5e4e3e8f7c5469724
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091490"
---
# <a name="applying-gamma-correction-to-a-gradient"></a>Aplicando a correção gama a um gradiente

Você pode habilitar a correção gama para um pincel de gradiente passando **true** para o método [**PathGradientBrush:: SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) desse pincel. Você pode desabilitar a correção gama passando **false** para o método **PathGradientBrush:: SetGammaCorrection** . A correção gama é desabilitada por padrão.

O exemplo a seguir cria um pincel de gradiente linear e usa esse pincel para preencher dois retângulos. O primeiro retângulo é preenchido sem a correção gama e o segundo retângulo é preenchido com a correção gama.


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



A ilustração a seguir mostra os dois retângulos preenchidos. O retângulo superior, que não tem a correção gama, aparece escuro no meio. O retângulo inferior, que tem a correção gama, parece ter mais intensidade uniforme.

![ilustração mostrando dois retângulos: o preenchimento colorido do primeiro varia em intensidade, o preenchimento da segunda varia menos](images/gammagradient1.png)

O exemplo a seguir cria um pincel de gradiente de caminho com base em um caminho em formato de estrela. O código usa o pincel de gradiente de caminho com a correção gama desabilitada (o padrão) para preencher o caminho. Em seguida, o código passa **true** para o método [**PathGradientBrush:: SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) para habilitar a correção gama para o pincel de gradiente de caminho. A chamada para [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) define a transformação mundial de um objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para que a chamada subsequente para [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) Preencha uma estrela que fica à direita da primeira estrela.


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



A ilustração a seguir mostra a saída do código anterior. A estrela à direita tem correção de gama. Observe que a estrela à esquerda, que não tem a correção gama, tem áreas que parecem escuras.

![ilustração de 2 5-pontos de início com preenchimento gradiente colorido; a primeira tem áreas escuras, a segunda não](images/gammagradient2.png)

 

 



