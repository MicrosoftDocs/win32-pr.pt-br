---
description: O Windows GDI+ desenha linhas, retângulos e outras figuras em um sistema de coordenadas.
ms.assetid: a43bcb27-473b-4ca2-a937-2b54384ab86b
title: Visão geral de elementos gráficos vetoriais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e9bfe98585ef8e073cf1c563c237436b7c982bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553344"
---
# <a name="overview-of-vector-graphics"></a>Visão geral de elementos gráficos vetoriais

O Windows GDI+ desenha linhas, retângulos e outras figuras em um sistema de coordenadas. Você pode escolher entre uma variedade de sistemas de coordenadas, mas o sistema de coordenadas padrão tem a origem no canto superior esquerdo com o eixo x apontando para a direita e o eixo y apontando para baixo. A unidade de medida no sistema de coordenadas padrão é o pixel.

![ilustração de um sistema de coordenadas com o eixo x estendendo para a direita e o eixo y se estendendo](images/aboutgdip02-art01.png)

Um monitor de computador cria sua exibição em uma matriz retangular de pontos chamados de elementos de imagem ou pixels. O número de pixels que aparecem na tela varia de um monitor para o outro e o número de pixels que aparecem em um monitor individual normalmente pode ser configurado para alguma extensão pelo usuário.

![ilustração de uma grade retangular, com três células na grade rotuladas por suas coordenadas](images/aboutgdip02-art02.png)

Ao usar o GDI+ para desenhar uma linha, um retângulo ou uma curva, você fornece certas informações de chave sobre o item a ser desenhado. Por exemplo, você pode especificar uma linha fornecendo dois pontos e especificar um retângulo fornecendo um ponto, uma altura e uma largura. O GDI+ funciona em conjunto com o software de driver de vídeo para determinar quais pixels devem ser ativados para mostrar a linha, o retângulo ou a curva. A ilustração a seguir mostra os pixels que são ativados para exibir uma linha do ponto (4, 2) ao ponto (12, 8).

![ilustração mostrando uma grade retangular com células preenchidas para indicar uma linha entre dois pontos de extremidade](images/aboutgdip02-art03.png)

Ao longo do tempo, determinados blocos de construção básicos mostraram ser mais úteis para criar imagens bidimensionais. Esses blocos de construção, todos suportados pelo GDI+, são fornecidos na seguinte lista:

-   Linhas
-   Retângulos
-   Elipses
-   Arcos
-   Polígonos
-   Splines cardinais
-   Splines de Bézier

A classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) no GDI+ fornece os seguintes métodos para desenhar os itens na lista anterior: [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)), [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrectf_)), [DrawPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpointf_inint)), [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal)), [DrawCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint)) (para as polilinhas Cardeal) e [DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inconstpoint__inconstpoint__inconstpoint__inconstpoint_)). Cada um desses métodos é sobrecarregado; ou seja, cada método vem em várias variações com diferentes listas de parâmetros. Por exemplo, uma variação do método DrawLine recebe o endereço de um objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) e quatro inteiros, enquanto outra variação do método DrawLine recebe o endereço de um objeto **Pen** e duas referências a objetos [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) .

Os métodos para desenhar linhas, retângulos e polilinhados de Bézier têm métodos plural complementares que desenham vários itens em uma única chamada: [DrawLines](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawlines(inconstpen_inconstpointf_inint)), [DrawRectangles](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangles(inconstpen_inconstrect_inint))e [DrawBeziers](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbeziers(inconstpen_inconstpoint_inint)). Além disso, o método [DrawCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint)) tem um método complementar, [DrawClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)), que fecha uma curva conectando o ponto final da curva ao ponto de partida.

Todos os métodos de desenho da classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) funcionam em conjunto com um objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . Portanto, para desenhar qualquer coisa, você deve criar pelo menos dois objetos: um objeto **gráfico** e um objeto de **caneta** . O objeto **Pen** armazena os atributos do item a ser desenhado, como largura e cor da linha. O endereço do objeto **Pen** é passado como um dos argumentos para o método Drawing. Por exemplo, uma variação do método [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) recebe o endereço de um objeto **Pen** e quatro inteiros, conforme mostrado no código a seguir, que desenha um retângulo com uma largura de 100, uma altura de 50 e um canto superior esquerdo de (20, 10).


```
myGraphics.DrawRectangle(&myPen, 20, 10, 100, 50);
```



 

 



