---
description: 'Um B&\# 233; zier spline é uma curva especificada por quatro pontos: dois pontos de extremidade (P1 e P2) e dois pontos de controle (C1 e C2).'
ms.assetid: 3ee279ea-20cc-4089-b1a5-13bf1c7c4942
title: Linhas de Bézier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd725e64f9ba0035849d2d1d6fbc03d5efa0b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091489"
---
# <a name="bezier-splines"></a>Linhas de Bézier

Uma spline de Bézier é uma curva especificada por quatro pontos: dois pontos de extremidade (p1 e p2) e dois pontos de controle (c1 e c2). A curva começa em p1 e termina em p2. A curva não passa pelos pontos de controle, mas os pontos de controle atuam como ímãs, puxando a curva em determinadas direções e influenciando a forma como a curva dobra. A ilustração a seguir mostra uma curva de Bézier junto com seus pontos de extremidade e de controle.

![ilustração mostrando um spline de Bézier com dois pontos de extremidade e dois pontos de controle](images/aboutgdip02-art11a.png)

Observe que a curva começa em P1 e se move para o ponto de controle C1. A linha tangente da curva em p1 é a linha desenhada de p1 a c1. Observe também que a linha tangente no ponto de extremidade P2 é a linha desenhada de C2 para P2.

Para desenhar um spline Bézier, você precisa de um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e um objeto de [**caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . O objeto **Graphics** fornece o método [DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inint_inint_inint_inint_inint_inint_inint_inint)) e o objeto **Pen** armazena os atributos da curva, como largura e cor da linha. O endereço do objeto **Pen** é passado como um dos argumentos para o método DrawBezier. Os argumentos restantes passados para o método DrawBezier são os pontos de extremidade e de controle. O exemplo a seguir desenha um spline Bézier com ponto inicial (0, 0), pontos de controle (40, 20) e (80, 150) e ponto final (100, 10).


```
myGraphics.DrawBezier(&myPen, 0, 0, 40, 20, 80, 150, 100, 10);
```



A ilustração a seguir mostra a curva, os pontos de controle e duas linhas tangentes.

![ilustração mostrando um spline de Bézier com dois pontos de extremidade, dois pontos de controle e duas linhas tangentes](images/aboutgdip02-art12.png)

As splines de Bézier foram desenvolvidos originalmente por Pierre Bézier para projetos da indústria automotiva. Desde que eles tenham sido comprovadamente muito úteis em muitos tipos de design auxiliado por computador e também são usados para definir os contornos das fontes. Splines de Bézier podem gerar uma grande variedade de formas, algumas das quais são mostradas na ilustração a seguir.

![ilustração mostrando três linhas de Bézier](images/aboutgdip02-art13.png)

 

 



