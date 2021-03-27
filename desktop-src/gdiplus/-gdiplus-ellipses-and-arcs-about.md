---
description: Uma elipse é especificada por seu retângulo delimitador. A ilustração a seguir mostra uma elipse junto a seu retângulo delimitador.
ms.assetid: 45e80501-4d64-480b-a7c7-3af52c00a0aa
title: Elipses e arcos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8b1aaaff5ff27191ed7f0bf64ddbcb414be6319
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091469"
---
# <a name="ellipses-and-arcs"></a>Elipses e arcos

Uma elipse é especificada por seu retângulo delimitador. A ilustração a seguir mostra uma elipse junto a seu retângulo delimitador.

![ilustração de uma elipse colocada dentro de um retângulo delimitador](images/aboutgdip02-art05.png)

Para desenhar uma elipse, você precisa de um objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e um objeto de [**caneta**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) . O objeto **Graphics** fornece o método [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) e o objeto **Pen** armazena os atributos da elipse, como largura e cor da linha. O endereço do objeto **Pen** é passado como um dos argumentos para o método DrawEllipse. Os argumentos restantes passados para o método DrawEllipse especificam o retângulo delimitador para a elipse. O exemplo a seguir desenha uma elipse; o retângulo delimitador tem uma largura de 160, uma altura de 80 e um canto superior esquerdo de (100, 50).


```
myGraphics.DrawEllipse(&myPen, 100, 50, 160, 80);
```



[DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) é um método sobrecarregado da classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , portanto, há várias maneiras de fornecer argumentos. Por exemplo, você pode construir um objeto [**Rect**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect) e passar uma referência para o objeto **Rect** como um argumento para o método DrawEllipse.


```
Rect myRect(100, 50, 160, 80);
myGraphics.DrawEllipse(&myPen, myRect);
```



Um arco é uma parte de uma elipse. Para desenhar um arco, você chama o método [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) da classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Os parâmetros do método DrawArc são os mesmos que os parâmetros do método [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) , exceto que DrawArc requer um ângulo inicial e um ângulo de flecha. O exemplo a seguir desenha um arco com um ângulo inicial de 30 graus e um ângulo de flecha de 180 graus.


```
myGraphics.DrawArc(&myPen, 100, 50, 160, 80, 30, 180);
```



A ilustração a seguir mostra o arco, a elipse e o retângulo delimitador.

![ilustração de uma elipse dentro de um retângulo delimitador; a metade esquerda inferior da elipse é desenhada em vermelho](images/aboutgdip02-art06.png)

 

 



