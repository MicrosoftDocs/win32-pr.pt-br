---
description: 'O Windows GDI+ usa três espaços de coordenadas: mundo, página e dispositivo.'
ms.assetid: eb20f5e9-25f5-4f27-8ea5-83f6819425ed
title: Tipos de sistemas de coordenadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e259f43d4fc0d6a74021f3a6125f85652f51ac95
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120621"
---
# <a name="types-of-coordinate-systems"></a>Tipos de sistemas de coordenadas

O Windows GDI+ usa três espaços de coordenadas: mundo, página e dispositivo. Quando você faz a chamada `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` , os pontos que passa para o método [**Graphics::D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) – (0, 0) e (160, 80) — estão no espaço de coordenadas do mundo. Antes que o GDI+ possa desenhar a linha na tela, as coordenadas passam por uma sequência de transformações. Uma transformação converte coordenadas mundiais em coordenadas de página e outra transformação converte coordenadas de página em coordenadas de dispositivo.

Suponha que você queira trabalhar com um sistema de coordenadas cuja origem está no corpo da área de cliente em vez do canto superior esquerdo. Digamos, por exemplo, que você queira que a origem esteja a 100 pixels da borda esquerda da área de cliente e a 50 pixels da parte superior da área de cliente. A ilustração a seguir mostra esse sistema de coordenadas.

![captura de tela de uma janela que contém eixos de coordenadas rotulados](images/aboutgdip05-art01.png)

Quando faz a chamada `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)`, você obtém a linha mostrada na ilustração a seguir.

![captura de tela da janela anterior, mas com uma linha azul sendo estendida diagonalmente da origem](images/aboutgdip05-art02.png)

As coordenadas dos pontos de extremidade da sua linha nos três espaços de coordenadas são as seguintes:



| Space       |  Coordenadas do ponto de extremidade                       |
|--------|-------------------------|
| World (Mundo)  | (0, 0) a (160, 80)     |
| ?   | (100, 50) a (260, 130) |
| Dispositivo | (100, 50) a (260, 130) |



 

Observe que o espaço de coordenadas de página tem sua origem no canto superior esquerdo da área de cliente; sempre será esse o caso. Observe também que, como a unidade de medida é o pixel, as coordenadas do dispositivo são as mesmas que as coordenadas da página. Se você definir a unidade de medida como algo diferente de pixels (por exemplo, polegadas), as coordenadas do dispositivo serão diferentes das coordenadas da página.

A transformação que mapeia coordenadas mundiais para coordenadas de página é chamada de *transformação mundial* e é mantida por um objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . No exemplo anterior, a transformação do mundo é uma tradução 100 unidades na direção x e 50 unidades na direção y. O exemplo a seguir define a transformação mundial de um objeto **Graphics** e, em seguida, usa esse objeto **Graphics** para desenhar a linha mostrada na figura anterior.


```
myGraphics.TranslateTransform(100.0f, 50.0f);

myGraphics.DrawLine(&myPen, 0, 0, 160, 80);
```



A transformação que mapeia coordenadas de página para coordenadas de dispositivo é chamada de *transformação de página*. A classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornece quatro métodos para manipular e inspecionar a transformação página: [**Graphics:: SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit), [**gráficos:: GetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit), [**Graphics:: SetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale)e [**Graphics:: GetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale). A classe **Graphics** também fornece dois métodos, [**Graphics:: GetDpiX**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) e [**Graphics:: GetDpiY**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy), para examinar os pontos horizontais e verticais por polegada do dispositivo de vídeo.

Você pode usar o método [**Graphics:: SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) da classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para especificar uma unidade de medida. O exemplo a seguir desenha uma linha de (0, 0) para (2, 1) em que o ponto (2, 1) é de 2 polegadas à direita e 1 polegada para baixo a partir do ponto (0, 0).


```
myGraphics.SetPageUnit(UnitInch);

myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



> [!Note]
> Se você não especificar uma largura de caneta ao construir a caneta, o exemplo anterior desenhará uma linha com uma polegada de largura. Você pode especificar a largura da caneta no segundo argumento para o construtor de [**caneta**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) :
> <br/><br/>
> `Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.

 

Se presumirmos que o dispositivo de vídeo tenha 96 pontos por polegada na direção horizontal e 96 pontos por polegada na direção vertical, os pontos de extremidade da linha no exemplo anterior têm as seguintes coordenadas nos três espaços de coordenadas:



| Space       | Coordenadas do ponto de extremidade                    |
|--------|---------------------|
| World (Mundo)  | (0, 0) a (2, 1)    |
| ?   | (0, 0) a (2, 1)    |
| Dispositivo | (0, 0) a (192, 96) |



 

É possível combinar as transformações global e de página para obter uma variedade de resultados. Por exemplo, suponha que você queira usar polegadas como a unidade de medida e queira que a origem se seu sistema de coordenadas esteja a 2 polegadas da borda esquerda da área de cliente e a 1/2 polegada da parte superior da área de cliente. O exemplo a seguir define as transformações World e Page de um objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e, em seguida, desenha uma linha de (0, 0) para (2, 1).


```
myGraphics.TranslateTransform(2.0f, 0.5f);
myGraphics.SetPageUnit(UnitInch);
myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



A ilustração a seguir mostra a linha e o sistema de coordenadas.

![captura de tela da janela anterior, mas mais larga, com os eixos posicionados à esquerda e rotulados de forma diferente](images/aboutgdip05-art03.png)

Se presumirmos que o dispositivo de vídeo tenha 96 pontos por polegada na direção horizontal e 96 pontos por polegada na direção vertical, os pontos de extremidade da linha no exemplo anterior têm as seguintes coordenadas nos três espaços de coordenadas:



| Space       | Coordenadas do ponto de extremidade                        |
|--------|-------------------------|
| World (Mundo)  | (0, 0) a (2, 1)        |
| ?   | (2, 0.5) a (4, 1.5)    |
| Dispositivo | (192, 48) a (384, 144) |



 

 

 
