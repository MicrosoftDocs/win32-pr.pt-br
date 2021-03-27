---
description: As seções a seguir descrevem várias maneiras de programação com o Windows GDI+, diferente da programação com o Windows Graphics Device Interface (GDI).
ms.assetid: 89a154c1-6a49-45d6-a73c-94b0b1567408
title: Alterações no modelo de programação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a90cd6f1c3a6ebab1e55562e67cb4926f0ffedf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010872"
---
# <a name="changes-in-the-programming-model"></a>Alterações no modelo de programação

As seções a seguir descrevem várias maneiras de programação com o Windows GDI+, diferente da programação com o Windows Graphics Device Interface (GDI).

-   [Contextos de dispositivo, identificadores e objetos gráficos](#device-contexts-handles-and-graphics-objects)
-   [Duas maneiras de desenhar uma linha](#two-ways-to-draw-a-line)
    -   [Desenhando uma linha com GDI](#drawing-a-line-with-gdi)
    -   [Desenhando uma linha com GDI+ e a interface de classe C++](#drawing-a-line-with-gdi-and-the-c-class-interface)
-   [Canetas, pincéis, caminhos, imagens e fontes como parâmetros](#pens-brushes-paths-images-and-fonts-as-parameters)
-   [Sobrecarga de método](#method-overloading)
-   [Não há mais posição atual](#no-more-current-position)
-   [Métodos separados para desenhar e preencher](#separate-methods-for-draw-and-fill)
-   [Construindo regiões](#constructing-regions)

## <a name="device-contexts-handles-and-graphics-objects"></a>Contextos de dispositivo, identificadores e objetos gráficos

Se você escreveu programas usando o GDI (a interface de dispositivo de gráficos incluída nas versões anteriores do Windows), você está familiarizado com a ideia de um DC (contexto de dispositivo). Um contexto de dispositivo é uma estrutura usada pelo Windows para armazenar informações sobre os recursos de um determinado dispositivo de vídeo e atributos que especificam como os itens serão desenhados nesse dispositivo. Um contexto de dispositivo para uma exibição de vídeo também é associado a uma janela específica na exibição. Primeiro, você obtém um identificador para um contexto de dispositivo (HDC) e, em seguida, passa esse identificador como um argumento para funções GDI que realmente fazem o desenho. Você também passa a alça como um argumento para funções GDI que obtêm ou definem os atributos do contexto do dispositivo.

Ao usar o GDI+, você não precisa se preocupar com identificadores e contextos de dispositivo como faz ao usar o GDI. Você simplesmente cria um objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e, em seguida, invoca seus métodos no conhecido estilo orientado a objeto – mygraphicsobject. DrawLine (*Parameters*). O objeto **Graphics** está no núcleo de GDI+ assim como o contexto do dispositivo está no núcleo da GDI. O contexto do dispositivo e o objeto de **gráficos** desempenham funções semelhantes, mas há algumas diferenças fundamentais entre o modelo de programação baseado em identificador usado com a GDI (contextos de dispositivo) e o modelo orientado a objeto usado com objetos **gráficos** (GDI+).

O objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , como o contexto do dispositivo, é associado a uma janela específica na tela e contém atributos (por exemplo, modo de suavização e dica de renderização de texto) que especificam como os itens devem ser desenhados. No entanto, o objeto **gráfico** não está vinculado a uma caneta, pincel, caminho, imagem ou fonte, uma vez que um contexto de dispositivo é. Por exemplo, em GDI, antes de poder usar um contexto de dispositivo para desenhar uma linha, você deve chamar [SelectObject](/windows/win32/api/wingdi/nf-wingdi-selectobject) para associar um objeto de caneta ao contexto do dispositivo. Isso é chamado de seleção da caneta no contexto do dispositivo. Todas as linhas desenhadas no contexto do dispositivo usarão essa caneta até que você selecione uma caneta diferente. Com o GDI+, você passa um objeto de [**caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) como um argumento para o método [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) da classe **Graphics** . Você pode usar um objeto de **caneta** diferente em cada uma das séries de chamadas DrawLine sem a necessidade de associar um objeto **Pen** específico a um objeto **Graphics** .

## <a name="two-ways-to-draw-a-line"></a>Duas maneiras de desenhar uma linha

Os dois exemplos a seguir desenham uma linha vermelha de largura 3 do local (20, 10) para o local (200.100). O primeiro exemplo chama GDI e o segundo chama GDI+ por meio da interface de classe C++.

-   [Desenhando uma linha com GDI](#drawing-a-line-with-gdi)
-   [Desenhando uma linha com GDI+ e a interface de classe C++](#drawing-a-line-with-gdi-and-the-c-class-interface)

### <a name="drawing-a-line-with-gdi"></a>Desenhando uma linha com GDI

Para desenhar uma linha com GDI, você precisa de dois objetos: um contexto de dispositivo e uma caneta. Você Obtém um identificador para um contexto de dispositivo chamando [**BeginPaint**](/windows/win32/api/winuser/nf-winuser-beginpaint)e um identificador para uma caneta chamando [CreatePen](/windows/win32/api/wingdi/nf-wingdi-createpen). Em seguida, chame [SelectObject](/windows/win32/api/wingdi/nf-wingdi-selectobject) para selecionar a caneta no contexto do dispositivo. Você define a posição da caneta como (20, 10) chamando [MoveToEx](/windows/win32/api/wingdi/nf-wingdi-movetoex) e, em seguida, desenha uma linha da posição da caneta para (200, 100) chamando **LineTo**. Observe que MoveToEx e [LineTo](/windows/win32/api/wingdi/nf-wingdi-lineto) recebem **HDC** como um argumento.


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

Para desenhar uma linha com GDI+ e a interface de classe C++, você precisa de um objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e de uma [**caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . Observe que você não pede que o Windows lide com esses objetos. Em vez disso, você usa construtores para criar uma instância da classe **Graphics** (um objeto **Graphics** ) e uma instância da classe **Pen** (um objeto **Pen** ). Desenhar uma linha envolve chamar o método [**Graphics::D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) da classe **Graphics** . O primeiro parâmetro do método **Graphics::D rawline** é um ponteiro para o objeto **Pen** . Esse é um esquema mais simples e mais flexível do que selecionar uma caneta em um contexto de dispositivo, conforme mostrado no exemplo de GDI anterior.


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

Os exemplos anteriores mostram que os objetos de [**caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) podem ser criados e mantidos separadamente do objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , que fornece os métodos de desenho. Os objetos [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush), [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath), [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)e [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) também podem ser criados e mantidos separadamente do objeto **Graphics** . Muitos dos métodos de desenho fornecidos pela classe **Graphics** recebem um objeto **Brush**, **GraphicsPath**, **Image** ou **Font** como um argumento. Por exemplo, o endereço de um objeto de **pincel** é passado como um argumento para o método [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) e o endereço de um objeto **GraphicsPath** é passado como um argumento para o método [**Graphics::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) . Da mesma forma, os endereços de objetos de **imagem** e de **fonte** são passados para os métodos [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_)) e [drawstring](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) . Isso é diferente do GDI em que você seleciona um pincel, caminho, imagem ou fonte no contexto do dispositivo e, em seguida, passa um identificador para o contexto do dispositivo como um argumento para uma função de desenho.

## <a name="method-overloading"></a>Sobrecarga de método

Muitos dos métodos GDI+ estão sobrecarregados; ou seja, vários métodos compartilham o mesmo nome, mas têm diferentes listas de parâmetros. Por exemplo, o método [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) da classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) vem nos seguintes formatos:


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



Todas as quatro variações de [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) acima recebem um ponteiro para um objeto de [**caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) , as coordenadas do ponto de partida e as coordenadas do ponto final. As duas primeiras variações recebem as coordenadas como números de ponto flutuante e as duas últimas variações recebem as coordenadas como inteiros. A primeira e terceira variações recebem as coordenadas como uma lista de quatro números separados, enquanto a segunda e a quarta variações recebem as coordenadas como um par de objetos [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) (ou [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)).

## <a name="no-more-current-position"></a>Não há mais posição atual

Observe que nos métodos [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) mostrados anteriormente, o ponto de partida e o ponto final da linha são recebidos como argumentos. Essa é uma partida do esquema GDI em que você chama **MoveToEx** para definir a posição atual da caneta seguida de **LineTo** para desenhar uma linha começando em (**X1**, **Y1**) e terminando em (**X2**, **Y2**). A GDI+ como um todo abandonou a noção da posição atual.

## <a name="separate-methods-for-draw-and-fill"></a>Métodos separados para desenhar e preencher

A GDI+ é mais flexível do que a GDI quando se trata de desenhar os contornos e preencher os interiores de formas como retângulos. O GDI tem uma função [Rectangle](/windows/win32/api/wingdi/nf-wingdi-rectangle) que desenha o contorno e preenche o interior de um retângulo em uma única etapa. O contorno é desenhado com a caneta selecionada no momento e o interior é preenchido com o pincel selecionado no momento.


```
hBrush = CreateHatchBrush(HS_CROSS, RGB(0, 0, 255));
hPen = CreatePen(PS_SOLID, 3, RGB(255, 0, 0));
SelectObject(hdc, hBrush);
SelectObject(hdc, hPen);
Rectangle(hdc, 100, 50, 200, 80);
```



O GDI+ tem métodos separados para desenhar a estrutura de tópicos e preencher o interior de um retângulo. O método [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inreal_inreal_inreal_inreal)) da classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) tem o endereço de um objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) como um de seus parâmetros, e o método [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) tem o endereço de um objeto [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) como um de seus parâmetros.


```
HatchBrush* myHatchBrush = new HatchBrush(
   HatchStyleCross,
   Color(255, 0, 255, 0),
   Color(255, 0, 0, 255));
Pen* myPen = new Pen(Color(255, 255, 0, 0), 3);
myGraphics.FillRectangle(myHatchBrush, 100, 50, 100, 30);
myGraphics.DrawRectangle(myPen, 100, 50, 100, 30);
```



Observe que os métodos [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) e [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inreal_inreal_inreal_inreal)) em GDI+ recebem argumentos que especificam a borda esquerda do retângulo, a parte superior, a largura e a altura. Isso está em contraste com a função[Rectangle](/windows/win32/api/wingdi/nf-wingdi-rectangle) do GDI, que usa argumentos que especificam a borda esquerda do retângulo, a borda direita, superior e inferior. Observe também que o construtor da classe [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) em GDI+ tem quatro parâmetros. Os três últimos parâmetros são os valores vermelho, verde e azul usuais; o primeiro parâmetro é o valor alfa, que especifica a extensão para a qual a cor que está sendo desenhada é mesclada com a cor do plano de fundo.

## <a name="constructing-regions"></a>Construindo regiões

O GDI fornece várias funções para criar regiões: CreateRectRgn, CreateEllpticRgn, CreateRoundRectRgn, CreatePolygonRgn e CreatePolyPolygonRgn. Você pode esperar que a classe [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) em GDI+ tenha construtores análogos que usam retângulos, reticências, retângulos arredondados e polígonos como argumentos, mas esse não é o caso. A classe **Region** em GDI+ fornece um construtor que recebe uma referência de objeto [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) e outro construtor que recebe o endereço de um objeto [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) . Se você quiser construir uma região com base em uma elipse, um retângulo arredondado ou um polígono, poderá facilmente fazer isso criando um objeto **GraphicsPath** (que contém uma elipse, por exemplo) e, em seguida, passando o endereço desse objeto **GraphicsPath** para um construtor de **região** .

A GDI+ torna mais fácil formar regiões complexas combinando formas e caminhos. A classe [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) tem os métodos [Union](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-union(inconstrectf_)) e [Intersect](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-intersect(inconstgraphicspath)) que você pode usar para aumentar uma região existente com um caminho ou outra região. Um bom recurso do esquema GDI+ é que um objeto [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) não é destruído quando é passado como um argumento para um construtor de **região** . No GDI, você pode converter um caminho para uma região com a função [PathToRegion](/windows/win32/api/wingdi/nf-wingdi-pathtoregion) , mas o caminho é destruído no processo. Além disso, um objeto **GraphicsPath** não é destruído quando seu endereço é passado como um argumento para um método Union ou Intersect, para que você possa usar um determinado caminho como um bloco de construção para várias regiões separadas. Isso é mostrado no exemplo a seguir. Suponha que **onePath** é um ponteiro para um objeto **GraphicsPath** (simples ou complexo) que já foi inicializado.


```
Region  region1(rect1);
Region  region2(rect2);
region1.Union(onePath);
region2.Intersect(onePath);
```



 

 
