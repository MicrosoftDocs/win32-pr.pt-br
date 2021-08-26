---
description: GDI+ fornece gradientes lineares horizontais, verticais e diagonais. Por padrão, a cor em um gradiente linear muda uniformemente. No entanto, você pode personalizar um gradiente linear para que a cor mude de maneira não uniforme.
ms.assetid: 9b0236b2-be6b-4918-a106-5b0e6c3dd5ff
title: Criando um gradiente linear
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 922c4f1fc805aae25f53ed206d1b3e9112afbd3fa51ba544e121a70839d79d0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015188"
---
# <a name="creating-a-linear-gradient"></a>Criando um gradiente linear

GDI+ fornece gradientes lineares horizontais, verticais e diagonais. Por padrão, a cor em um gradiente linear muda uniformemente. No entanto, você pode personalizar um gradiente linear para que a cor mude de maneira não uniforme.

-   [Gradientes lineares horizontais](#horizontal-linear-gradients)
-   [Personalizando gradientes lineares](#customizing-linear-gradients)
-   [Gradientes lineares diagonais](#diagonal-linear-gradients)

## <a name="horizontal-linear-gradients"></a>Gradientes lineares horizontais

O exemplo a seguir usa um pincel de gradiente linear horizontal para preencher uma linha, uma elipse e um retângulo:


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 255, 0, 0),   // opaque red
   Color(255, 0, 0, 255));  // opaque blue

Pen pen(&linGrBrush);

graphics.DrawLine(&pen, 0, 10, 200, 10);
graphics.FillEllipse(&linGrBrush, 0, 30, 200, 100);
graphics.FillRectangle(&linGrBrush, 0, 155, 500, 30);
```



O construtor [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) recebe quatro argumentos: dois pontos e duas cores. O primeiro ponto (0, 10) é associado à primeira cor (vermelho) e o segundo ponto (200, 10) é associado à segunda cor (azul). Como seria de esperar, a linha desenhada de (10, 0) a (200, 10) muda gradualmente de vermelho para azul.

Os 10s nos pontos (50, 10) e (200, 10) não são importantes. O que é importante é que os dois pontos tenham a mesma coordenada de segunda, a linha que os conecta é horizontal. A elipse e o retângulo também mudam gradualmente de vermelho para azul conforme a coordenada horizontal vai de 0 a 200.

A ilustração a seguir mostra a linha, a elipse e o retângulo. Observe que o gradiente de cores repete-se à medida que a coordenada horizontal aumenta além de 200.

![ilustração mostrando um gradiente horizontal que preenche uma linha e uma elipse e um retângulo maior que a elipse](images/lineargradient1.png)

## <a name="customizing-linear-gradients"></a>Personalizando gradientes lineares

No exemplo anterior, os componentes de cor mudam linearmente conforme você vai de uma coordenada horizontal de 0 para uma coordenada horizontal de 200. Por exemplo, um ponto cuja primeira coordenada esteja a meio caminho entre 0 e 200 terá um componente azul a meio caminho entre 0 e 255.

GDI+ permite que você ajuste a maneira como uma cor varia de uma borda de um gradiente para a outra. Suponha que você queira criar um pincel de gradiente que mude de preto para vermelho de acordo com a tabela a seguir.



| Coordenada horizontal | Componentes RGB |
|-----------------------|----------------|
| 0                     | (0, 0, 0)      |
| 40                    | (128, 0, 0)    |
| 200                   | (255, 0, 0)    |



 

Observe que o componente vermelho está na metade da intensidade quando a coordenada horizontal está a apenas 20% do caminho de 0 a 200.

O exemplo a seguir chama o método [**LinearGradientBrush:: setblend**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblend) de um objeto [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) para associar três intensidades relativas a três posições relativas. Como na tabela anterior, uma intensidade relativa de 0,5 é associada a uma posição relativa de 0,2. O código preenche uma elipse e um retângulo com o pincel de gradiente.


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 0, 0, 0),     // opaque black 
   Color(255, 255, 0, 0));  // opaque red

REAL relativeIntensities[] = {0.0f, 0.5f, 1.0f};
REAL relativePositions[]   = {0.0f, 0.2f, 1.0f};

linGrBrush.SetBlend(relativeIntensities, relativePositions, 3);

graphics.FillEllipse(&linGrBrush, 0, 30, 200, 100);
graphics.FillRectangle(&linGrBrush, 0, 155, 500, 30);
```



A ilustração a seguir mostra o retângulo e elipse resultantes.

![ilustração mostrando um gradiente horizontal que preenche uma elipse e um retângulo maior que a elipse](images/lineargradient2.png)

## <a name="diagonal-linear-gradients"></a>Gradientes lineares diagonais

Os gradientes nos exemplos anteriores eram horizontais; ou seja, a cor muda gradualmente à medida que você se move ao longo de qualquer linha horizontal. Você também pode definir gradientes verticais e gradientes diagonais. O código a seguir passa os pontos (0, 0) e (200, 100) para um construtor [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) . A cor azul é associada a (0, 0) e a cor verde é associada a (200, 100). Uma linha (com largura da caneta de 10) e uma elipse são preenchidas com o pincel de gradiente linear.


```
LinearGradientBrush linGrBrush(
   Point(0, 0),
   Point(200, 100),
   Color(255, 0, 0, 255),   // opaque blue
   Color(255, 0, 255, 0));  // opaque green

Pen pen(&linGrBrush, 10);

graphics.DrawLine(&pen, 0, 0, 600, 300);
graphics.FillEllipse(&linGrBrush, 10, 100, 200, 100);
```



A ilustração a seguir mostra a linha e a elipse. Observe que a cor na elipse muda gradualmente à medida que você se move ao longo de qualquer linha paralela à linha que passa por (0, 0) e (200, 100).

![ilustração mostrando um gradiente diagonal que preenche uma elipse e uma linha diagonal](images/lineargradient3.png)

 

 



