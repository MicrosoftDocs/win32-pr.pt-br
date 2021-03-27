---
description: Para desenhar linhas e retângulos, você precisa de um objeto gráfico e um objeto de caneta. O objeto Graphics fornece o método DrawLine e o objeto Pen armazena os recursos da linha, como Color e Width.
ms.assetid: f2e4144f-f2f1-49db-bfdf-ffce3023b4cb
title: Uso de uma caneta para desenhar linhas e retângulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b335caf7e2ecbad6bc49965ff757809c3b1179c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921425"
---
# <a name="using-a-pen-to-draw-lines-and-rectangles"></a>Uso de uma caneta para desenhar linhas e retângulos

Para desenhar linhas e retângulos, você precisa de um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e um objeto de [**caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . O objeto **Graphics** fornece o método [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) e o objeto **Pen** armazena os recursos da linha, como Color e Width.

O exemplo a seguir desenha uma linha de (20, 10) para (300, 100). Suponha que **gráficos** seja um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) existente.


```
Pen pen(Color(255, 0, 0, 0));
graphics.DrawLine(&pen, 20, 10, 300, 100);
```



A primeira instrução do código usa o construtor da classe [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) para criar uma caneta preta. O argumento One passado para o construtor **Pen** é um objeto [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) . Os valores usados para construir o objeto de **cor** — (255, 0, 0, 0) — correspondem aos componentes alfa, vermelho, verde e azul da cor. Esses valores definem uma caneta preta opaca.

O exemplo a seguir desenha um retângulo com seu canto superior esquerdo em (10, 10). O retângulo tem uma largura de 100 e uma altura de 50. O segundo argumento passado para o construtor de [**caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) indica que a largura da caneta é de 5 pixels.


```
Pen blackPen(Color(255, 0, 0, 0), 5);
stat = graphics.DrawRectangle(&blackPen, 10, 10, 100, 50);
```



Quando o retângulo é desenhado, a caneta é centralizada no limite do retângulo. Como a largura da caneta é 5, os lados do retângulo são desenhados com 5 pixels de largura, de forma que 1 pixel é desenhado no próprio limite, 2 pixels são desenhados no interior e 2 pixels são desenhados fora. Para obter mais detalhes sobre alinhamento de caneta, consulte [definindo a largura e o alinhamento da caneta](-gdiplus-setting-pen-width-and-alignment-use.md).

A ilustração a seguir mostra o retângulo resultante. As linhas pontilhadas mostram onde o retângulo deveria ser desenhado se a largura da caneta tivesse um pixel. A exibição ampliada do canto superior esquerdo do retângulo mostra que as linhas pretas espessas são centralizadas nessas linhas pontilhadas.

![ilustração de um retângulo desenhado com uma linha preta espessa que circunda uma linha pontilhada cinza e fina](images/pens1.png)

 

 



