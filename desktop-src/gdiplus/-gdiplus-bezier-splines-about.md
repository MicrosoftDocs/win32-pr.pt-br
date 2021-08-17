---
description: 'Um spline B&233;zier é uma curva especificada por quatro pontos: dois pontos de extremidade (p1 e p2) e dois pontos de controle \# (c1 e c2).'
ms.assetid: 3ee279ea-20cc-4089-b1a5-13bf1c7c4942
title: Bezier Splines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87bcc9c56baa9cd1b3e93187ef00f9d6a2c8c1d218262c946028ed70429de18d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119399566"
---
# <a name="bezier-splines"></a>Bezier Splines

Uma spline de Bézier é uma curva especificada por quatro pontos: dois pontos de extremidade (p1 e p2) e dois pontos de controle (c1 e c2). A curva começa em p1 e termina em p2. A curva não passa pelos pontos de controle, mas os pontos de controle atuam como magnéticos, endossando a curva em determinadas direções e influenciando a maneira como a curva se inclina. A ilustração a seguir mostra uma curva de Bézier junto com seus pontos de extremidade e de controle.

![ilustração mostrando um spline de bezier com dois pontos de extremidade e dois pontos de controle](images/aboutgdip02-art11a.png)

Observe que a curva começa em p1 e se move para o ponto de controle c1. A linha tangente da curva em p1 é a linha desenhada de p1 a c1. Observe também que a linha tangente no ponto de extremidade p2 é a linha desenhada de c2 a p2.

Para desenhar um spline bézier, você precisa de [**um objeto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e um [**objeto Caneta.**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) O **objeto Graphics** fornece o [método DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inint_inint_inint_inint_inint_inint_inint_inint)) e o objeto **Pen** armazena atributos da curva, como largura e cor da linha. O endereço do objeto **Pen** é passado como um dos argumentos para o método DrawBezier. Os argumentos restantes passados para o método DrawBezier são os pontos de extremidade e os pontos de controle. O exemplo a seguir desenha um spline bézier com ponto de partida (0, 0), pontos de controle (40, 20) e (80, 150) e ponto final (100, 10).


```
myGraphics.DrawBezier(&myPen, 0, 0, 40, 20, 80, 150, 100, 10);
```



A ilustração a seguir mostra a curva, os pontos de controle e duas linhas tangentes.

![ilustração mostrando um spline de bezier com dois pontos de extremidade, dois pontos de controle e duas linhas tangentes](images/aboutgdip02-art12.png)

As splines de Bézier foram desenvolvidos originalmente por Pierre Bézier para projetos da indústria automotiva. Desde então, eles se mostraram muito úteis em muitos tipos de design auxiliado por computador e também são usados para definir os contornos das fontes. Splines de Bézier podem gerar uma grande variedade de formas, algumas das quais são mostradas na ilustração a seguir.

![ilustração mostrando três splines de bezier](images/aboutgdip02-art13.png)

 

 



