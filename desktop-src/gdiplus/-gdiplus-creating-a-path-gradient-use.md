---
description: A classe PathGradientBrush permite que você personalize a maneira como preenche uma forma com cores que mudam gradualmente.
ms.assetid: f6a8085c-3d6a-494f-a1ee-5fa96efb1aae
title: Criando um gradiente de caminho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729ef39793547b1485525f8cf1fd5b344773e7a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557703"
---
# <a name="creating-a-path-gradient"></a>Criando um gradiente de caminho

A classe [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) permite que você personalize a maneira como preenche uma forma com cores que mudam gradualmente. Um objeto **PathGradientBrush** tem um caminho de limite e um ponto central. Você pode especificar uma cor para o ponto central e outra cor para o limite. Você também pode especificar cores separadas para cada um dos vários pontos ao longo do limite.

> [!Note]  
> No GDI+, um caminho é uma sequência de linhas e curvas mantidas por um objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) . Para obter mais informações sobre caminhos de GDI+, consulte [caminhos](-gdiplus-paths-about.md) e [construção e caminhos de desenho](-gdiplus-constructing-and-drawing-paths-use.md).

 

O exemplo a seguir preenche uma elipse com pincel de gradiente de caminho. A cor central é definida como azul e a cor do limite é definida como azul-piscina.


```
// Create a path that consists of a single ellipse.
GraphicsPath path;
path.AddEllipse(0, 0, 140, 70);

// Use the path to construct a brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to blue.
pthGrBrush.SetCenterColor(Color(255, 0, 0, 255));

// Set the color along the entire boundary of the path to aqua.
Color colors[] = {Color(255, 0, 255, 255)};
int count = 1;
pthGrBrush.SetSurroundColors(colors, &count);

graphics.FillEllipse(&pthGrBrush, 0, 0, 140, 70);
```



A ilustração a seguir mostra a elipse preenchida.

![ilustração mostrando uma elipse com preenchimento gradual](images/pathgradient1.png)

Por padrão, um pincel de gradiente de caminho não é estendido para fora do limite do caminho. Se você usar o pincel de gradiente de caminho para preencher uma forma que ultrapasse o limite do caminho, a área da tela fora do caminho não será preenchida. A ilustração a seguir mostra o que acontece se você alterar a chamada de [**Graphics:: FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inreal_inreal_inreal_inreal)) no código anterior para `graphics.FillRectangle(&pthGrBrush, 0, 10, 200, 40)` .

![ilustração mostrando uma fatia horizontal da elipse anterior](images/pathgradient2.png)

## <a name="specifying-points-on-the-boundary"></a>Especificando pontos no limite

O exemplo a seguir constrói um pincel de gradiente de caminho de um caminho em forma de estrela. O código chama o método [**PathGradientBrush:: SetCenterColor**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor) para definir a cor em centróide da estrela para vermelho. Em seguida, o código chama o método [**PathGradientBrush:: SetSurroundColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setsurroundcolors) para especificar várias cores (armazenadas na matriz [**Colors**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) ) nos pontos individuais da matriz [**Points**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) . A instrução de código final preenche o caminho em forma de estrela com o pincel de gradiente de caminho.


```
// Put the points of a polygon in an array.
Point points[] = {Point(75, 0),    Point(100, 50), 
                  Point(150, 50),  Point(112, 75),
                  Point(150, 150), Point(75, 100), 
                  Point(0, 150),   Point(37, 75), 
                  Point(0, 50),    Point(50, 50)};

// Use the array of points to construct a path.
GraphicsPath path;
path.AddLines(points, 10);

// Use the path to construct a path gradient brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to red.
pthGrBrush.SetCenterColor(Color(255, 255, 0, 0));

// Set the colors of the points in the array.
Color colors[] = {Color(255, 0, 0, 0),   Color(255, 0, 255, 0),
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255), 
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0), 
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255),
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0)};

int count = 10;
pthGrBrush.SetSurroundColors(colors, &count);

// Fill the path with the path gradient brush.
graphics.FillPath(&pthGrBrush, &path);
```



A ilustração a seguir mostra a estrela preenchida.

![ilustração mostrando uma estrela de cinco pontas que preenche de vermelho no centro para várias cores em cada ponto da estrela](images/pathgradient3.png)

O exemplo a seguir constrói um pincel de gradiente de caminho com base em uma matriz de pontos. Uma cor é atribuída a cada um dos cinco pontos na matriz. Se você fosse conectar os cinco pontos por linhas retas, obteria um polígono de cinco lados. Uma cor também é atribuída ao centro (centróide) desse polígono — neste exemplo, o centro (80, 75) é definido como branco. A instrução de código final no exemplo preenche um retângulo com o pincel de gradiente de caminho.

A cor usada para preencher o retângulo é branca em (80, 75) e muda gradualmente à medida que você sai de (80, 75) para os pontos na matriz. Por exemplo, à medida que você passa de (80, 75) para (0, 0), a cor muda gradualmente de branco para vermelho e, à medida que você passa de (80, 75) para (160, 0), a cor muda gradualmente de branco para verde.


```
// Construct a path gradient brush based on an array of points.
PointF ptsF[] = {PointF(0.0f, 0.0f), 
                 PointF(160.0f, 0.0f), 
                 PointF(160.0f, 200.0f),
                 PointF(80.0f, 150.0f),
                 PointF(0.0f, 200.0f)};

PathGradientBrush pBrush(ptsF, 5);

// An array of five points was used to construct the path gradient
// brush. Set the color of each point in that array.
Color colors[] = {Color(255, 255, 0, 0),  // (0, 0) red
                  Color(255, 0, 255, 0),  // (160, 0) green
                  Color(255, 0, 255, 0),  // (160, 200) green
                  Color(255, 0, 0, 255),  // (80, 150) blue
                  Color(255, 255, 0, 0)}; // (0, 200) red

int count = 5;
pBrush.SetSurroundColors(colors, &count);

// Set the center color to white.
pBrush.SetCenterColor(Color(255, 255, 255, 255));

// Use the path gradient brush to fill a rectangle.
graphics.FillRectangle(&pBrush, Rect(0, 0, 180, 220));
```



Observe que não há nenhum objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) no código anterior. O construtor [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) específico no exemplo recebe um ponteiro para uma matriz de pontos, mas não requer um objeto **GraphicsPath** . Além disso, observe que o pincel de gradiente de caminho é usado para preencher um retângulo, não um caminho. O retângulo é maior do que o caminho usado para definir o pincel, portanto, parte do retângulo não é pintada pelo pincel. A ilustração a seguir mostra o retângulo (linha pontilhada) e a parte do retângulo pintado pelo pincel de gradiente de caminho.

![ilustração mostrando um retângulo limitado por uma linha pontilhada, parcialmente pintada por um gradiente com várias cores](images/gradient4.png)

## <a name="customizing-a-path-gradient"></a>Personalizando um gradiente de caminho

Uma maneira de personalizar um pincel de gradiente de caminho é definir suas escalas de foco. O ajuste de escala do foco especifica um caminho interno que se encontra dentro do caminho principal. A cor central é exibida em qualquer lugar dentro desse caminho interno e não apenas no ponto central. Para definir as escalas de foco de um pincel de gradiente de caminho, chame o método [**PathGradientBrush:: SetFocusScales**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setfocusscales) .

O exemplo a seguir cria um pincel de gradiente de caminho com base em uma trajetória elíptica. O código define a cor do limite como azul, define a cor do centro para azul-piscina e, em seguida, usa o pincel de gradiente de caminho para preencher o caminho elíptico.

Em seguida, o código define as escalas de foco do pincel de gradiente de caminho. A escala de foco de x é definida como 0,3 e a escala de foco de y é definida como 0,8. O código chama o método [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) de um objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para que a chamada subsequente para [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) Preencha uma elipse que fica à direita da primeira elipse.

Para ver o efeito de escalas de foco, imagine uma pequena elipse que compartilha seu centro com a elipse principal. A pequena elipse (interna) é a elipse principal dimensionada (sobre seu centro) horizontalmente por um fator de 0,3 e verticalmente por um fator de 0,8. Quando você vai do limite da elipse externa para o limite da elipse interna, a cor altera gradualmente de azul para azul-piscina. Quando você vai do limite da elipse interna ao centro compartilhado, a cor permanece azul-piscina.


```
// Create a path that consists of a single ellipse.
GraphicsPath path;
path.AddEllipse(0, 0, 200, 100);

// Create a path gradient brush based on the elliptical path.
PathGradientBrush pthGrBrush(&path);
pthGrBrush.SetGammaCorrection(TRUE);

// Set the color along the entire boundary to blue.
Color color(Color(255, 0, 0, 255));
INT num = 1;
pthGrBrush.SetSurroundColors(&color, &num);

// Set the center color to aqua.
pthGrBrush.SetCenterColor(Color(255, 0, 255, 255));
 
// Use the path gradient brush to fill the ellipse. 
graphics.FillPath(&pthGrBrush, &path);

// Set the focus scales for the path gradient brush.
pthGrBrush.SetFocusScales(0.3f, 0.8f);

// Use the path gradient brush to fill the ellipse again.
// Show this filled ellipse to the right of the first filled ellipse.
graphics.TranslateTransform(220.0f, 0.0f);
graphics.FillPath(&pthGrBrush, &path);
```



A ilustração a seguir mostra a saída do código anterior. A elipse à esquerda é azul-piscina somente no ponto central. A elipse à direita é azul-piscina em qualquer lugar dentro do caminho interno.

![ilustração mostrando duas reticências que sombream de azul-piscina a azul: a primeira tem muito pouca água; o segundo tem muito mais](images/focusscales1.png)

Outra maneira de personalizar um pincel de gradiente de caminho é especificar uma matriz de cores predefinidas e uma matriz de posições de interpolação.

O exemplo a seguir cria um pincel de gradiente de caminho com base em um triângulo. O código chama o método [**PathGradientBrush:: SetInterpolationColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setinterpolationcolors) do pincel de gradiente de caminho para especificar uma matriz de cores de interpolação (verde escuro, água, azul) e uma matriz de posições de interpolação (0, 0,25, 1). Ao mudar do limite do triângulo ao ponto central, a cor gradualmente muda de verde-escuro para azul-piscina e, em seguida, de azul-piscina para azul. A alteração de verde-escuro para azul-piscina ocorre em 25 por cento da distância de verde-escuro para azul.


```
// Vertices of the triangle
Point points[] = {Point(100, 0), 
                  Point(200, 200), 
                  Point(0, 200)};

// No GraphicsPath object is created. The PathGradient
// brush is constructed directly from the array of points.
PathGradientBrush pthGrBrush(points, 3);

Color presetColors[] = {
   Color(255, 0, 128, 0),    // Dark green
   Color(255, 0, 255, 255),  // Aqua
   Color(255, 0, 0, 255)};   // Blue

REAL interpPositions[] = {
   0.0f,   // Dark green is at the boundary of the triangle.
   0.25f,  // Aqua is 25 percent of the way from the boundary
           // to the center point.
   1.0f};  // Blue is at the center point.
                  
pthGrBrush.SetInterpolationColors(presetColors, interpPositions, 3);

// Fill a rectangle that is larger than the triangle
// specified in the Point array. The portion of the
// rectangle outside the triangle will not be painted.
graphics.FillRectangle(&pthGrBrush, 0, 0, 200, 200);
```



A ilustração a seguir mostra a saída do código anterior.

![ilustração que mostra um triângulo que sombreia de azul no centro, para azul-piscina, para verde nas bordas](images/pathgradient4.png)

## <a name="setting-the-center-point"></a>Configurando o ponto central

Por padrão, o ponto central de um pincel de gradiente de caminho é o centroide de caminho usado para construir o pincel. Você pode alterar o local do ponto central chamando o método [**PathGradientBrush:: SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) da classe [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) .

O exemplo a seguir cria um pincel de gradiente de caminho com base em uma elipse. O centro da elipse é em (70, 35), mas o ponto central do pincel de gradiente de caminho é definido como (120, 40).


```
// Create a path that consists of a single ellipse.
GraphicsPath path;
path.AddEllipse(0, 0, 140, 70);

// Use the path to construct a brush.
PathGradientBrush pthGrBrush(&path);

// Set the center point to a location that is not the centroid of the path.
pthGrBrush.SetCenterPoint(Point(120, 40));

// Set the color at the center point to blue.
pthGrBrush.SetCenterColor(Color(255, 0, 0, 255));

// Set the color along the entire boundary of the path to aqua.
Color colors[] = {Color(255, 0, 255, 255)};
int count = 1;
pthGrBrush.SetSurroundColors(colors, &count);

graphics.FillEllipse(&pthGrBrush, 0, 0, 140, 70);
```



A ilustração a seguir mostra a elipse preenchida e o ponto central do pincel de gradiente de caminho.

![ilustração mostrando uma elipse que preenche de azul para azul-piscina de um ponto central próximo a uma extremidade](images/pathgradient5.png)

Você pode definir o ponto central de um pincel de gradiente de caminho para um local fora do caminho que foi usado para construir o pincel. No código anterior, se você substituir a chamada para [**PathGradientBrush:: SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) por `pthGrBrush.SetCenterPoint(Point(145, 35))` , você receberá o seguinte resultado.

![ilustração mostrando uma elipse que preenche de vermelho para amarelo de um ponto central que está fora da borda da elipse](images/pathgradient6.png)

Na ilustração anterior, os pontos na extremidade direita da elipse não são azul puro (embora muito parecido). As cores no gradiente são posicionadas como se o preenchimento tivesse tido permissão para alcançar o ponto (145, 35), a cor teria atingido o azul puro (0, 0, 255). Mas o preenchimento nunca atinge (145, 35), pois um pincel de gradiente de caminho pinta apenas dentro de seu caminho.

 

 
