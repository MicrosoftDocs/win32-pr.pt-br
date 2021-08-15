---
description: As seções a seguir descrevem várias maneiras pelas quais a programação com Windows GDI+ é diferente da programação com Windows Graphics Device Interface (GDI).
ms.assetid: 89a154c1-6a49-45d6-a73c-94b0b1567408
title: Alterações no modelo de programação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05dd8b74662d0141405b9d11b9b4446ffb19dd4ef3bfdec788afe7a51a8c681a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118249883"
---
# <a name="changes-in-the-programming-model"></a>Alterações no modelo de programação

As seções a seguir descrevem várias maneiras pelas quais a programação com Windows GDI+ é diferente da programação com Windows Graphics Device Interface (GDI).

-   [Contextos, alças e objetos gráficos do dispositivo](#device-contexts-handles-and-graphics-objects)
-   [Duas maneiras de desenhar uma linha](#two-ways-to-draw-a-line)
    -   [Desenhando uma linha com GDI](#drawing-a-line-with-gdi)
    -   [Desenhando uma linha com GDI+ e a interface de classe C++](#drawing-a-line-with-gdi-and-the-c-class-interface)
-   [Canetas, pincéis, caminhos, imagens e fontes como parâmetros](#pens-brushes-paths-images-and-fonts-as-parameters)
-   [Sobrecarga de método](#method-overloading)
-   [Nenhuma posição mais atual](#no-more-current-position)
-   [Métodos separados para desenhar e preencher](#separate-methods-for-draw-and-fill)
-   [Construindo regiões](#constructing-regions)

## <a name="device-contexts-handles-and-graphics-objects"></a>Contextos, alças e objetos gráficos do dispositivo

Se você escreveu programas usando GDI (a interface do dispositivo gráfico incluída nas versões anteriores do Windows), você está familiarizado com a ideia de um DC (contexto de dispositivo). Um contexto de dispositivo é uma estrutura usada pelo Windows para armazenar informações sobre os recursos de um dispositivo de exibição específico e atributos que especificam como os itens serão desenhados nesse dispositivo. Um contexto de dispositivo para uma exibição de vídeo também é associado a uma janela específica na exibição. Primeiro, você obtém um handle para um HDC (contexto de dispositivo) e, em seguida, passa esse handle como um argumento para funções GDI que realmente fazem o desenho. Você também passa o handle como um argumento para funções GDI que obtém ou defini os atributos do contexto do dispositivo.

Ao usar GDI+, você não precisa se preocupar tanto com os handles e os contextos do dispositivo quanto ao usar a GDI. Você simplesmente cria um objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e, em seguida, invoca seus métodos no estilo familiar orientado a objeto — myGraphicsObject.DrawLine(*parameters*). O **objeto Graphics** está no núcleo GDI+, assim como o contexto do dispositivo está no núcleo da GDI. O contexto do dispositivo e o objeto Gráficos têm funções **semelhantes,** mas há algumas diferenças fundamentais entre o modelo de programação baseado em identificador usado com contextos de dispositivo (GDI) e o modelo orientado a objeto usado com objetos **gráficos** (GDI+).

O [**objeto Gráficos,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) como o contexto do dispositivo, está associado a uma janela específica na tela e contém atributos (por exemplo, modo de suavização e dica de renderização de texto) que especificam como os itens devem ser desenhados. No entanto, **o objeto Gráficos** não está vinculado a uma caneta, pincel, caminho, imagem ou fonte como um contexto de dispositivo. Por exemplo, no GDI, antes de usar um contexto de dispositivo para desenhar uma linha, você deve chamar [SelectObject](/windows/win32/api/wingdi/nf-wingdi-selectobject) para associar um objeto de caneta ao contexto do dispositivo. Isso é conhecido como selecionar a caneta no contexto do dispositivo. Todas as linhas desenhadas no contexto do dispositivo usarão essa caneta até que você selecione uma caneta diferente. Com GDI+, você passa um [**objeto Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) como um argumento para o [método DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) da **classe Graphics.** Você pode usar um objeto **Caneta diferente** em cada uma de uma série de chamadas DrawLine sem precisar associar um determinado objeto **Pen** a um **objeto Graphics.**

## <a name="two-ways-to-draw-a-line"></a>Duas maneiras de desenhar uma linha

Os dois exemplos a seguir desenham uma linha vermelha de largura 3 do local (20, 10) para o local (200.100). O primeiro exemplo chama GDI e o segundo chama GDI+ por meio da interface de classe C++.

-   [Desenhando uma linha com GDI](#drawing-a-line-with-gdi)
-   [Desenhando uma linha com GDI+ e a interface de classe C++](#drawing-a-line-with-gdi-and-the-c-class-interface)

### <a name="drawing-a-line-with-gdi"></a>Desenhando uma linha com GDI

Para desenhar uma linha com gDI, você precisa de dois objetos: um contexto de dispositivo e uma caneta. Você obterá um handle para um contexto de dispositivo chamando [**BeginPaint**](/windows/win32/api/winuser/nf-winuser-beginpaint)e um handle para uma caneta chamando [CreatePen](/windows/win32/api/wingdi/nf-wingdi-createpen). Em seguida, chame [SelectObject](/windows/win32/api/wingdi/nf-wingdi-selectobject) para selecionar a caneta no contexto do dispositivo. Você pode definir a posição da caneta como (20, 10) chamando [MoveToEx](/windows/win32/api/wingdi/nf-wingdi-movetoex) e, em seguida, desenhando uma linha dessa posição de caneta como (200, 100) chamando **LineTo**. Observe que MoveToEx e [LineTo](/windows/win32/api/wingdi/nf-wingdi-lineto) recebem **hdc** como um argumento.


```
HDC          hdc;
PAINTSTRUCT  ps;
HPEN         hPen;
HPEN         hPenOld;
hdc = BeginPaint(hWnd, &ps);
   hPen = CreatePen(PS_SOLID, 3, RGB(255, 0, 0));
   hPenOld = (HPEN)SelectObject(hdc, hPen);
   MoveToEx(hdc, 20, 10, NULL);
   LineTo(hdc, 200, 100);
   SelectObject(hdc, hPenOld);
   DeleteObject(hPen);
EndPaint(hWnd, &ps);
```



### <a name="drawing-a-line-with-gdi-and-the-c-class-interface"></a>Desenhando uma linha com GDI+ e a interface de classe C++

Para desenhar uma linha com GDI+ e a interface de classe C++, você precisa de um objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e um [**objeto Pen.**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) Observe que você não solicita Windows para lidar com esses objetos. Em vez disso, você usa construtores para criar uma instância da classe **Graphics** (um objeto **Graphics)** e uma instância da classe **Pen** (um **objeto Pen).** Desenhar uma linha envolve chamar o [**método Graphics::D rawLine**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) da **classe Graphics.** O primeiro parâmetro do **método Graphics::D rawLine** é um ponteiro para o **objeto Pen.** Esse é um esquema mais simples e flexível do que selecionar uma caneta em um contexto de dispositivo, conforme mostrado no exemplo de GDI anterior.


```
HDC          hdc;
PAINTSTRUCT  ps;
Pen*         myPen;
Graphics*    myGraphics;
hdc = BeginPaint(hWnd, &ps);
   myPen = new Pen(Color(255, 255, 0, 0), 3);
   myGraphics = new Graphics(hdc);
   myGraphics->DrawLine(myPen, 20, 10, 200, 100);
   delete myGraphics;
   delete myPen;
EndPaint(hWnd, &ps);
```



## <a name="pens-brushes-paths-images-and-fonts-as-parameters"></a>Canetas, pincéis, caminhos, imagens e fontes como parâmetros

Os exemplos anteriores mostram que os objetos [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) podem ser criados e mantidos separadamente do [**objeto Graphics,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) que fornece os métodos de desenho. [**Objetos Brush,**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) [**GraphicsPath,**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)e [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) também podem ser criados e mantidos separadamente do **objeto Graphics.** Muitos dos métodos de desenho fornecidos pela classe **Graphics** recebem um objeto **Brush**, **GraphicsPath,** **Image** ou **Font** como um argumento. Por exemplo, o endereço de um objeto **Brush** é passado como um argumento para o método [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) e o endereço de um **objeto GraphicsPath** é passado como um argumento para o método [**Graphics::D rawPath.**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) Da mesma forma, os endereços **dos objetos Image** e **Font** são passados para os [métodos DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_)) e [DrawString.](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) Isso é diferente do GDI em que você seleciona um pincel, caminho, imagem ou fonte no contexto do dispositivo e, em seguida, passa um alça para o contexto do dispositivo como um argumento para uma função de desenho.

## <a name="method-overloading"></a>Sobrecarga de método

Muitos dos métodos GDI+ estão sobrecarregados; ou seja, vários métodos compartilham o mesmo nome, mas têm listas de parâmetros diferentes. Por exemplo, o [método DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) da [**classe Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) vem nos seguintes formulários:


```
Status DrawLine(IN const Pen* pen,
                IN REAL x1,
                IN REAL y1,
                IN REAL x2,
                IN REAL y2);
Status DrawLine(IN const Pen* pen,
                IN const PointF& pt1,
                IN const PointF& pt2);
Status DrawLine(IN const Pen* pen,
                IN INT x1,
                IN INT y1,
                IN INT x2,
                IN INT y2);
    
Status DrawLine(IN const Pen* pen,
                IN const Point& pt1,
                IN const Point& pt2);
```



Todas as quatro variações [de DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) acima recebem um ponteiro para um objeto [**Pen,**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) as coordenadas do ponto inicial e as coordenadas do ponto final. As duas primeiras variações recebem as coordenadas como números de ponto flutuante e as duas últimas variações recebem as coordenadas como inteiros. A primeira e a terceira variações recebem as coordenadas como uma lista de quatro números separados, enquanto a segunda e a quarta variações recebem as coordenadas como um par de objetos [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) (ou [**PointF).**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)

## <a name="no-more-current-position"></a>Nenhuma posição mais atual

Observe que, nos [métodos DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) mostrados anteriormente, o ponto de partida e o ponto final da linha são recebidos como argumentos. Esta é uma partida do esquema GDI em que você chama **MoveToEx** para definir a posição da caneta atual seguida por **LineTo** para desenhar uma linha começando em (**x1**, **y1**) e terminando em (**x2**, **y2**). GDI+ como um todo abandonaram a noção de posição atual.

## <a name="separate-methods-for-draw-and-fill"></a>Métodos separados para desenhar e preencher

GDI+ é mais flexível do que a GDI quando se trata de desenhar os contornos e preencher os interiores de formas como retângulos. A GDI tem [uma função Rectangle](/windows/win32/api/wingdi/nf-wingdi-rectangle) que desenha o contorno e preenche o interior de um retângulo em uma única etapa. O contorno é desenhado com a caneta selecionada no momento e o interior é preenchido com o pincel selecionado no momento.


```
hBrush = CreateHatchBrush(HS_CROSS, RGB(0, 0, 255));
hPen = CreatePen(PS_SOLID, 3, RGB(255, 0, 0));
SelectObject(hdc, hBrush);
SelectObject(hdc, hPen);
Rectangle(hdc, 100, 50, 200, 80);
```



GDI+ tem métodos separados para desenhar o contorno e preencher o interior de um retângulo. O [método DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inreal_inreal_inreal_inreal)) da classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) tem o endereço de um objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) como um de seus parâmetros e o [método FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) tem o endereço de um objeto [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) como um de seus parâmetros.


```
HatchBrush* myHatchBrush = new HatchBrush(
   HatchStyleCross,
   Color(255, 0, 255, 0),
   Color(255, 0, 0, 255));
Pen* myPen = new Pen(Color(255, 255, 0, 0), 3);
myGraphics.FillRectangle(myHatchBrush, 100, 50, 100, 30);
myGraphics.DrawRectangle(myPen, 100, 50, 100, 30);
```



Observe que [os métodos FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) e [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inreal_inreal_inreal_inreal)) GDI+ recebem argumentos que especificam a borda esquerda, a parte superior, a largura e a altura do retângulo. Isso é diferente da função retângulo[GDI,](/windows/win32/api/wingdi/nf-wingdi-rectangle) que aceita argumentos que especificam a borda esquerda, a borda direita, a parte superior e a inferior do retângulo. Observe também que o construtor da classe [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) no GDI+ tem quatro parâmetros. Os últimos três parâmetros são os valores vermelho, verde e azul usuais; o primeiro parâmetro é o valor alfa, que especifica a extensão até a qual a cor que está sendo desenhada é mesclada com a cor da tela de fundo.

## <a name="constructing-regions"></a>Construindo regiões

A GDI fornece várias funções para criar regiões: CreateRectRgn, CreateEllpticRgn, CreateRoundRectRgn, CreatePolygonRgn e CreatePolyPolygonRgn. Você pode [](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) esperar que a classe Region no GDI+ tenha construtores análogos que levam retângulos, reellipses, retângulos arredondados e polígonos como argumentos, mas esse não é o caso. A **classe Region** no GDI+ fornece um construtor que recebe uma referência de objeto [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) e outro construtor que recebe o endereço de um [**objeto GraphicsPath.**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) Se você quiser construir uma região com base em uma elipse, retângulo arredondado ou polígono, poderá facilmente fazer isso criando um objeto **GraphicsPath** (que contém uma elipse, por exemplo) e, em seguida, passando o endereço desse **objeto GraphicsPath** para um construtor **de** Região.

GDI+ facilita a formação de regiões complexas combinando formas e caminhos. A [**classe Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) tem métodos [Union](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-union(inconstrectf_)) e [Intersect](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-intersect(inconstgraphicspath)) que você pode usar para aumentar uma região existente com um caminho ou outra região. Um bom recurso do esquema GDI+ é que um [**objeto GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) não é destruído quando é passado como um argumento para um construtor **de** Região. No GDI, você pode converter um caminho em uma região com a função [PathToRegion,](/windows/win32/api/wingdi/nf-wingdi-pathtoregion) mas o caminho é destruído no processo. Além disso, um objeto **GraphicsPath** não é destruído quando seu endereço é passado como um argumento para um método Union ou Intersect, portanto, você pode usar um determinado caminho como um bloco de construção para várias regiões separadas. Isso é mostrado no exemplo a seguir. Suponha que **onePath** seja um ponteiro para **um objeto GraphicsPath** (simples ou complexo) que já foi inicializado.


```
Region  region1(rect1);
Region  region2(rect2);
region1.Union(onePath);
region2.Intersect(onePath);
```



 

 
