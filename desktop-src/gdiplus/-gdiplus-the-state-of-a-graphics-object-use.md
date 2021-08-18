---
description: a classe Graphics é o coração de Windows GDI+. Para desenhar qualquer coisa, você cria um objeto de gráfico, define suas propriedades e chama seus métodos (DrawLine, DrawImage, drawstring e similares).
ms.assetid: 7d70f9fe-c0b2-4d65-815d-483d06df96ad
title: O estado de um objeto de elementos gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f68a2ba754aadc1f7d2572dcbc2ac40d08d7fe95d382ce60511cd72d441bb80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977326"
---
# <a name="the-state-of-a-graphics-object"></a>O estado de um objeto de elementos gráficos

a classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) é o coração de Windows GDI+. Para desenhar qualquer coisa, você cria um objeto de **gráfico** , define suas propriedades e chama seus métodos ( [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)), [drawstring](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))e similares).

O exemplo a seguir constrói um objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e um objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) e, em seguida, chama o método [**Graphics::D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) do objeto **Graphics** :


```
HDC          hdc;
PAINTSTRUCT  ps;

hdc = BeginPaint(hWnd, &ps);
{
   Graphics graphics(hdc);
   Pen pen(Color(255, 0, 0, 255));  // opaque blue
   graphics.DrawRectangle(&pen, 10, 10, 200, 100);
}
EndPaint(hWnd, &ps);
```



No código anterior, o método [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) retorna um identificador para um contexto de dispositivo e esse identificador é passado para o construtor de [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . um contexto de dispositivo é uma estrutura (mantida por Windows) que contém informações sobre o dispositivo de vídeo específico que está sendo usado.

## <a name="graphics-state"></a>Estado gráfico

Um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) faz mais do que fornecer métodos de desenho, como [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) e [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)). Um objeto **gráfico** também mantém o estado gráfico, que pode ser dividido nas seguintes categorias:

-   Um link para um contexto de dispositivo
-   Configurações de qualidade
-   Transformações
-   Uma região de recorte

### <a name="device-context"></a>Contexto do dispositivo

Como programador de aplicativos, você não precisa pensar na interação entre um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e seu contexto de dispositivo. essa interação é manipulada por GDI+ nos bastidores.

### <a name="quality-settings"></a>Configurações de Qualidade

Um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) tem várias propriedades que influenciam a qualidade dos itens que são desenhados na tela. Você pode exibir e manipular essas propriedades chamando métodos get e Set. Por exemplo, você pode chamar o método [**Graphics:: SetTextRenderingHint**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) para especificar o tipo de anti-aliasing (se houver) aplicado ao texto. Outros métodos definidos que influenciam a qualidade são [**elementos gráficos:: SetSmoothingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode), [**Graphics:: SetCompositingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode), [**Graphics:: SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality)e [**Graphics:: setinterpolamode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setinterpolationmode).

O exemplo a seguir desenha duas elipses, uma com o modo de suavização definido como [* * * * SmoothingModeAntiAlias * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) * * e outra com o modo de suavização definido como [* * * * SmoothingModeHighSpeed * * * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode):


```
Graphics graphics(hdc);
Pen pen(Color(255, 0, 255, 0));  // opaque green

graphics.SetSmoothingMode(SmoothingModeAntiAlias);
graphics.DrawEllipse(&pen, 0, 0, 200, 100);
graphics.SetSmoothingMode(SmoothingModeHighSpeed);
graphics.DrawEllipse(&pen, 0, 150, 200, 100);
```



### <a name="transformations"></a>Transformações

Um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) mantém duas transformações (mundo e página) que são aplicadas a todos os itens desenhados por esse objeto **gráfico** . Qualquer transformação afim pode ser armazenada na transformação global. Transformações afins incluem colocação em escala, rotação, reflexão, distorção e translação. A transformação de página pode ser usada para colocação em escala e para alterar unidades (por exemplo, pixels em polegadas). Para obter mais informações sobre transformações, consulte [coordenar sistemas e transformações](-gdiplus-coordinate-systems-and-transformations-about.md).

O exemplo a seguir define as transformações World e Page de um objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . A transformação global é definida com uma rotação de 30 graus. A transformação página é definida para que as coordenadas passadas para o segundo [**gráfico::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) será tratado como milímetros em vez de pixels. O código faz duas chamadas idênticas para o método **Graphics::D rawellipse** . A transformação do mundo é aplicada ao primeiro **elemento gráfico::D chamada rawellipse** , e ambas as transformações (mundo e página) são aplicadas à segunda **imagem::D** chamada de rawellipse.


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0));

graphics.ResetTransform();
graphics.RotateTransform(30.0f);            // World transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
graphics.SetPageUnit(UnitMillimeter);       // Page transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
```



A ilustração a seguir mostra as duas elipses. Observe que a rotação de 30 graus é sobre a origem do sistema de coordenadas (canto superior esquerdo da área de cliente), e não sobre os centros das elipses. Observe também que a largura da caneta de 1 significa 1 pixel para a primeira elipse e 1 milímetro para a segunda elipse.

![captura de tela de uma janela que contém uma elipse pequena, fina e uma elipse grande e espessa](images/graphicsascon1.png)

 

### <a name="clipping-region"></a>Área de recorte

Um objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) mantém uma região de recorte que se aplica a todos os itens desenhados por esse objeto **gráfico** . Você pode definir a região de recorte chamando o método [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) .

O exemplo a seguir cria uma região em forma de mais (+), formando a união de dois retângulos. Essa região é designada como a região de recorte de um objeto de [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Em seguida, o código desenha duas linhas restritas ao interior da área de recorte.


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0), 5);  // opaque red, width 5
SolidBrush brush(Color(255, 180, 255, 255));  // opaque aqua

// Create a plus-shaped region by forming the union of two rectangles.
Region region(Rect(50, 0, 50, 150));
region.Union(Rect(0, 50, 150, 50));
graphics.FillRegion(&brush, &region);

// Set the clipping region.
graphics.SetClip(&region);

// Draw two clipped lines.
graphics.DrawLine(&pen, 0, 30, 150, 160);
graphics.DrawLine(&pen, 40, 20, 190, 150);
```



A ilustração a seguir mostra as linhas recortadas.

![ilustração mostrando uma forma colorida cruzada por duas linhas diagonais em vermelho](images/graphicsascon2.png)

 

 
