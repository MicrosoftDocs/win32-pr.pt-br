---
description: Um polígono é uma figura fechada com três ou mais lados retos.
ms.assetid: f1155341-83f3-4805-8d42-a1910515db31
title: Polígonos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe67ec2d062579df0510c100a80d06715be4199e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647104"
---
# <a name="polygons"></a>Polígonos

Um polígono é uma figura fechada com três ou mais lados retos. Por exemplo, um triângulo é um polígono com três lados, um retângulo é um polígono com quatro lados e um Pentágono é um polígono com cinco lados. A ilustração a seguir mostra diversos polígonos.

![ilustração mostrando cinco polígonos de diferentes formas, tamanhos e cores](images/aboutgdip02-art07.png)

Para desenhar um polígono, você precisa de um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , um objeto de [**caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) e uma matriz de objetos [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) (ou [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)). O objeto **Graphics** fornece o método [DrawPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpoint_inint)) . O objeto **Pen** armazena os atributos do polígono, como largura e cor da linha, e a matriz de objetos **Point** armazena os pontos a serem conectados por linhas retas. Os endereços do objeto **Pen** e a matriz de objetos **Point** são passados como argumentos para o método DrawPolygon. O exemplo a seguir desenha um polígono com três lados. Observe que há apenas três pontos em **myPointArray**: (0, 0), (50, 30) e (30, 60). O método DrawPolygon fecha automaticamente o polígono, desenhando uma linha de (30, 60) de volta para o ponto de partida (0, 0);


```
Point myPointArray[] =
   {Point(0, 0), Point(50, 30), Point(30, 60)};
myGraphics.DrawPolygon(&myPen, myPointArray, 3);
```



A ilustração a seguir mostra o polígono.

![ilustração mostrando um triângulo em relação a eixos de coordenadas](images/aboutgdip02-art08.png)

 

 



