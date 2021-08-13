---
description: para desenhar linhas com Windows GDI+ você precisa criar um objeto de gráfico e um objeto de caneta.
ms.assetid: d91562ab-41e6-4bca-a320-74f490a4f88f
title: Canetas, linhas e retângulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8ac54d1e98a617492aa6f5f1194767fc56a34ffcaaee71ba71753dda08f8bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119359586"
---
# <a name="pens-lines-and-rectangles"></a>Canetas, linhas e retângulos

para desenhar linhas com Windows GDI+ você precisa criar um objeto de [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e um objeto de [**caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . O objeto **Graphics** fornece os métodos que realmente fazem o desenho, e o objeto **Pen** armazena os atributos da linha, como Color, Width e Style. Desenhar uma linha é simplesmente uma questão de chamar o método [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) do objeto **Graphics** . O endereço do objeto **Pen** é passado como um dos argumentos para o método DrawLine. O exemplo a seguir desenha uma linha do ponto (4, 2) até o ponto (12, 6).


```
myGraphics.DrawLine(&myPen, 4, 2, 12, 6);
```



[DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) é um método sobrecarregado da classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , portanto, há várias maneiras pelas quais você pode fornecê-lo com argumentos. Por exemplo, você pode construir dois objetos [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) e passar referências para os objetos **Point** como argumentos para o método DrawLine.


```
Point myStartPoint(4, 2);
Point myEndPoint(12, 6);
myGraphics.DrawLine(&myPen, myStartPoint, myEndPoint);
```



Você pode especificar determinados atributos ao construir um objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . Por exemplo, um construtor de [caneta](/windows/win32/api/gdipluspen/nf-gdipluspen-pen-pen(constpen_)) permite que você especifique a cor e a largura. O exemplo a seguir desenha uma linha azul de largura 2 de (0, 0) para (60, 30).


```
Pen myPen(Color(255, 0, 0, 255), 2);
myGraphics.DrawLine(&myPen, 0, 0, 60, 30);
```



O objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) também tem atributos, como o estilo tracejado, que você pode usar para especificar os recursos da linha. Por exemplo, o exemplo a seguir desenha uma linha tracejada de (100, 50) a (300, 80).


```
myPen.SetDashStyle(DashStyleDash);
myGraphics.DrawLine(&myPen, 100, 50, 300, 80);
```



Você pode usar vários métodos do objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) para definir muitos outros atributos da linha. Os métodos [**Pen:: SetStartCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setstartcap) e [**Pen:: SetEndCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setendcap) especificam a aparência das extremidades da linha; as extremidades podem ser simples, quadradas, arredondadas, triangulares ou uma forma personalizada. O método [**Pen:: SetLineJoin**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) permite especificar se as linhas conectadas são Mitre (Unidas com cantos nítidos), chanfradas, arredondadas ou recortadas. A ilustração a seguir mostra linhas com vários estilos de extremidade e junção.

![ilustração de duas linhas que demonstram extremidades arredondadas e circulares, cantos arredondados e com mitra e dois estilos de seta](images/aboutgdip02-art04.png)

retângulos de desenho com GDI+ é semelhante a linhas de desenho. Para desenhar um retângulo, você precisa de um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e um objeto de [**caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . O objeto **Graphics** fornece um método [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) e o objeto **Pen** armazena atributos, como largura e cor da linha. O endereço do objeto **Pen** é passado como um dos argumentos para o método DrawRectangle. O exemplo a seguir desenha um retângulo com seu canto superior esquerdo em (100, 50), uma largura de 80 e uma altura de 40.


```
myGraphics.DrawRectangle(&myPen, 100, 50, 80, 40);
```



[DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) é um método sobrecarregado da classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , portanto, há várias maneiras de fornecer argumentos. Por exemplo, você pode construir um objeto [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) e passar uma referência para o objeto **Rect** como um argumento para o método DrawRectangle.


```
Rect myRect(100, 50, 80, 40);
myGraphics.DrawRectangle(&myPen, myRect);
```



Um objeto [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) tem métodos para manipular e coletar informações sobre o retângulo. Por exemplo, os métodos [inflar](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-inflate(inint_inint)) e [offset](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-offset(inconstpoint_)) alteram o tamanho e a posição do retângulo. O método [**Rect:: IntersectsWith**](/windows/win32/api/Gdiplustypes/nf-gdiplustypes-rect-intersectswith) informa se o retângulo cruza outro retângulo determinado e o método [Contains](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-contains(inint_inint)) informa se um determinado ponto está dentro do retângulo.

 

 
