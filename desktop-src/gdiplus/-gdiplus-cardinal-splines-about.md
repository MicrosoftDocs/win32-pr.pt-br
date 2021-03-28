---
description: Um spline cardinal é uma sequência de curvas individuais unidas para formar uma curva maior.
ms.assetid: 4fc62f00-7006-4ade-bfcc-091a3a97d889
title: Linhas Cardeal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d85c0163e405a6f9346f521b4057eb936108cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169097"
---
# <a name="cardinal-splines"></a>Linhas Cardeal

Um spline cardinal é uma sequência de curvas individuais unidas para formar uma curva maior. O spline é especificado por uma matriz de pontos e um parâmetro de tensão. Um spline cardinal passa suavemente pelos pontos na matriz. Não há cantos agudos nem mudanças abruptas na inclinação da curva. A ilustração a seguir mostra um conjunto de pontos e um spline cardinal que passa pelos pontos no conjunto.

![ilustração mostrando uma spline cardeal que passa por seis pontos definidos](images/aboutgdip02-art09.gif)

Um spline físico é uma peça fina de madeira ou outro material flexível. Antes do advento do splines matemáticos, os designers usavam splines físicos para desenhar curvas. O designer colocava o spline em um pedaço de papel e ancorava-o em um determinado conjunto de pontos. Em seguida, o designer poderia criar uma curva desenhando ao longo do spline com um lápis. Um determinado conjunto de pontos podia produzir uma variedade de curvas, dependendo das propriedades do spline físico. Por exemplo, um spline com uma alta resistência à curvatura geraria uma curva diferente daquela de um spline extremamente flexível.

As fórmulas para splines matemáticos são baseadas nas propriedades de barras flexíveis, portanto, as curvas produzidas por splines matemáticos são semelhantes às curvas antes produzidas por splines físicos. Assim como splines físicos de tensão diferente produzirão curvas diferentes em um determinado conjunto de pontos, splines matemáticos com valores diferentes para o parâmetro de tensão produzirão curvas diferentes em um determinado conjunto de pontos. A ilustração a seguir mostra quatro splines cardinais passando pelo mesmo conjunto de pontos. A tensão é mostrada para cada spline. Observe que uma tensão de 0 corresponde à tensão física infinita, forçando a curva a levar a maneira mais curta (linhas retas) entre pontos. Uma tensão de 1 corresponde à ausência de tensão física, permitindo que o spline siga o caminho de menor curvatura total. Com valores de tensão superiores a 1, a curva comporta-se como uma mola comprimida, pressionada para seguir um caminho mais longo.

![ilustração mostrando quatro linhas Cardeal por meio dos mesmos três pontos](images/aboutgdip02-art10.gif)

Observe que as quatro linhas na figura anterior compartilham a mesma linha tangente no ponto de partida. A tangente é a linha desenhada do ponto de partida até o próximo seguinte ao longo da curva. Da mesma forma, a tangente compartilhada no ponto final é a linha desenhada do ponto final até o ponto anterior na curva.

Para desenhar uma spline Cardeal, você precisa de um objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , um objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) e uma matriz de objetos [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) . O objeto **Graphics** fornece o método [DrawCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpointf_inint_inreal)) , que desenha o spline, e o objeto **Pen** armazena os atributos da spline, como a largura e a cor da linha. A matriz de objetos **Point** armazena os pontos que a curva passará. O exemplo a seguir desenha uma spline cardeal que passa pelos pontos em *myPointArray*. O terceiro parâmetro é a tensão.


```
myGraphics.DrawCurve(&myPen, myPointArray, 3, 1.5f);
```



 

 



