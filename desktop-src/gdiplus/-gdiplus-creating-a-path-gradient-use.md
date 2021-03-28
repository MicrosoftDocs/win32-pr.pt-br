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
# <a name="creating-a-path-gradient"></a><span data-ttu-id="c2a47-103">Criando um gradiente de caminho</span><span class="sxs-lookup"><span data-stu-id="c2a47-103">Creating a Path Gradient</span></span>

<span data-ttu-id="c2a47-104">A classe [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) permite que você personalize a maneira como preenche uma forma com cores que mudam gradualmente.</span><span class="sxs-lookup"><span data-stu-id="c2a47-104">The [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) class allows you to customize the way you fill a shape with gradually changing colors.</span></span> <span data-ttu-id="c2a47-105">Um objeto **PathGradientBrush** tem um caminho de limite e um ponto central.</span><span class="sxs-lookup"><span data-stu-id="c2a47-105">A **PathGradientBrush** object has a boundary path and a center point.</span></span> <span data-ttu-id="c2a47-106">Você pode especificar uma cor para o ponto central e outra cor para o limite.</span><span class="sxs-lookup"><span data-stu-id="c2a47-106">You can specify one color for the center point and another color for the boundary.</span></span> <span data-ttu-id="c2a47-107">Você também pode especificar cores separadas para cada um dos vários pontos ao longo do limite.</span><span class="sxs-lookup"><span data-stu-id="c2a47-107">You can also specify separate colors for each of several points along the boundary.</span></span>

> [!Note]  
> <span data-ttu-id="c2a47-108">No GDI+, um caminho é uma sequência de linhas e curvas mantidas por um objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) .</span><span class="sxs-lookup"><span data-stu-id="c2a47-108">In GDI+, a path is a sequence of lines and curves maintained by a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span> <span data-ttu-id="c2a47-109">Para obter mais informações sobre caminhos de GDI+, consulte [caminhos](-gdiplus-paths-about.md) e [construção e caminhos de desenho](-gdiplus-constructing-and-drawing-paths-use.md).</span><span class="sxs-lookup"><span data-stu-id="c2a47-109">For more information about GDI+ paths, see [Paths](-gdiplus-paths-about.md) and [Constructing and Drawing Paths](-gdiplus-constructing-and-drawing-paths-use.md).</span></span>

 

<span data-ttu-id="c2a47-110">O exemplo a seguir preenche uma elipse com pincel de gradiente de caminho.</span><span class="sxs-lookup"><span data-stu-id="c2a47-110">The following example fills an ellipse with a path gradient brush.</span></span> <span data-ttu-id="c2a47-111">A cor central é definida como azul e a cor do limite é definida como azul-piscina.</span><span class="sxs-lookup"><span data-stu-id="c2a47-111">The center color is set to blue and the boundary color is set to aqua.</span></span>


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



<span data-ttu-id="c2a47-112">A ilustração a seguir mostra a elipse preenchida.</span><span class="sxs-lookup"><span data-stu-id="c2a47-112">The following illustration shows the filled ellipse.</span></span>

![ilustração mostrando uma elipse com preenchimento gradual](images/pathgradient1.png)

<span data-ttu-id="c2a47-114">Por padrão, um pincel de gradiente de caminho não é estendido para fora do limite do caminho.</span><span class="sxs-lookup"><span data-stu-id="c2a47-114">By default, a path gradient brush does not extend outside the boundary of the path.</span></span> <span data-ttu-id="c2a47-115">Se você usar o pincel de gradiente de caminho para preencher uma forma que ultrapasse o limite do caminho, a área da tela fora do caminho não será preenchida.</span><span class="sxs-lookup"><span data-stu-id="c2a47-115">If you use the path gradient brush to fill a shape that extends beyond the boundary of the path, the area of the screen outside the path will not be filled.</span></span> <span data-ttu-id="c2a47-116">A ilustração a seguir mostra o que acontece se você alterar a chamada de [**Graphics:: FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inreal_inreal_inreal_inreal)) no código anterior para `graphics.FillRectangle(&pthGrBrush, 0, 10, 200, 40)` .</span><span class="sxs-lookup"><span data-stu-id="c2a47-116">The following illustration shows what happens if you change the [**Graphics::FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inreal_inreal_inreal_inreal)) call in the preceding code to `graphics.FillRectangle(&pthGrBrush, 0, 10, 200, 40)`.</span></span>

![ilustração mostrando uma fatia horizontal da elipse anterior](images/pathgradient2.png)

## <a name="specifying-points-on-the-boundary"></a><span data-ttu-id="c2a47-118">Especificando pontos no limite</span><span class="sxs-lookup"><span data-stu-id="c2a47-118">Specifying Points on the Boundary</span></span>

<span data-ttu-id="c2a47-119">O exemplo a seguir constrói um pincel de gradiente de caminho de um caminho em forma de estrela.</span><span class="sxs-lookup"><span data-stu-id="c2a47-119">The following example constructs a path gradient brush from a star-shaped path.</span></span> <span data-ttu-id="c2a47-120">O código chama o método [**PathGradientBrush:: SetCenterColor**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor) para definir a cor em centróide da estrela para vermelho.</span><span class="sxs-lookup"><span data-stu-id="c2a47-120">The code calls the [**PathGradientBrush::SetCenterColor**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor) method to set the color at the centroid of the star to red.</span></span> <span data-ttu-id="c2a47-121">Em seguida, o código chama o método [**PathGradientBrush:: SetSurroundColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setsurroundcolors) para especificar várias cores (armazenadas na matriz [**Colors**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) ) nos pontos individuais da matriz [**Points**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) .</span><span class="sxs-lookup"><span data-stu-id="c2a47-121">Then the code calls the [**PathGradientBrush::SetSurroundColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setsurroundcolors) method to specify various colors (stored in the [**colors**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) array) at the individual points in the [**points**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) array.</span></span> <span data-ttu-id="c2a47-122">A instrução de código final preenche o caminho em forma de estrela com o pincel de gradiente de caminho.</span><span class="sxs-lookup"><span data-stu-id="c2a47-122">The final code statement fills the star-shaped path with the path gradient brush.</span></span>


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



<span data-ttu-id="c2a47-123">A ilustração a seguir mostra a estrela preenchida.</span><span class="sxs-lookup"><span data-stu-id="c2a47-123">The following illustration shows the filled star.</span></span>

![ilustração mostrando uma estrela de cinco pontas que preenche de vermelho no centro para várias cores em cada ponto da estrela](images/pathgradient3.png)

<span data-ttu-id="c2a47-125">O exemplo a seguir constrói um pincel de gradiente de caminho com base em uma matriz de pontos.</span><span class="sxs-lookup"><span data-stu-id="c2a47-125">The following example constructs a path gradient brush based on an array of points.</span></span> <span data-ttu-id="c2a47-126">Uma cor é atribuída a cada um dos cinco pontos na matriz.</span><span class="sxs-lookup"><span data-stu-id="c2a47-126">A color is assigned to each of the five points in the array.</span></span> <span data-ttu-id="c2a47-127">Se você fosse conectar os cinco pontos por linhas retas, obteria um polígono de cinco lados.</span><span class="sxs-lookup"><span data-stu-id="c2a47-127">If you were to connect the five points by straight lines, you would get a five-sided polygon.</span></span> <span data-ttu-id="c2a47-128">Uma cor também é atribuída ao centro (centróide) desse polígono — neste exemplo, o centro (80, 75) é definido como branco.</span><span class="sxs-lookup"><span data-stu-id="c2a47-128">A color is also assigned to the center (centroid) of that polygon — in this example, the center (80, 75) is set to white.</span></span> <span data-ttu-id="c2a47-129">A instrução de código final no exemplo preenche um retângulo com o pincel de gradiente de caminho.</span><span class="sxs-lookup"><span data-stu-id="c2a47-129">The final code statement in the example fills a rectangle with the path gradient brush.</span></span>

<span data-ttu-id="c2a47-130">A cor usada para preencher o retângulo é branca em (80, 75) e muda gradualmente à medida que você sai de (80, 75) para os pontos na matriz.</span><span class="sxs-lookup"><span data-stu-id="c2a47-130">The color used to fill the rectangle is white at (80, 75) and changes gradually as you move away from (80, 75) toward the points in the array.</span></span> <span data-ttu-id="c2a47-131">Por exemplo, à medida que você passa de (80, 75) para (0, 0), a cor muda gradualmente de branco para vermelho e, à medida que você passa de (80, 75) para (160, 0), a cor muda gradualmente de branco para verde.</span><span class="sxs-lookup"><span data-stu-id="c2a47-131">For example, as you move from (80, 75) to (0, 0), the color changes gradually from white to red, and as you move from (80, 75) to (160, 0), the color changes gradually from white to green.</span></span>


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



<span data-ttu-id="c2a47-132">Observe que não há nenhum objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) no código anterior.</span><span class="sxs-lookup"><span data-stu-id="c2a47-132">Note that there is no [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object in the preceding code.</span></span> <span data-ttu-id="c2a47-133">O construtor [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) específico no exemplo recebe um ponteiro para uma matriz de pontos, mas não requer um objeto **GraphicsPath** .</span><span class="sxs-lookup"><span data-stu-id="c2a47-133">The particular [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) constructor in the example receives a pointer to an array of points but does not require a **GraphicsPath** object.</span></span> <span data-ttu-id="c2a47-134">Além disso, observe que o pincel de gradiente de caminho é usado para preencher um retângulo, não um caminho.</span><span class="sxs-lookup"><span data-stu-id="c2a47-134">Also, note that the path gradient brush is used to fill a rectangle, not a path.</span></span> <span data-ttu-id="c2a47-135">O retângulo é maior do que o caminho usado para definir o pincel, portanto, parte do retângulo não é pintada pelo pincel.</span><span class="sxs-lookup"><span data-stu-id="c2a47-135">The rectangle is larger than the path used to define the brush, so some of the rectangle is not painted by the brush.</span></span> <span data-ttu-id="c2a47-136">A ilustração a seguir mostra o retângulo (linha pontilhada) e a parte do retângulo pintado pelo pincel de gradiente de caminho.</span><span class="sxs-lookup"><span data-stu-id="c2a47-136">The following illustration shows the rectangle (dotted line) and the portion of the rectangle painted by the path gradient brush.</span></span>

![ilustração mostrando um retângulo limitado por uma linha pontilhada, parcialmente pintada por um gradiente com várias cores](images/gradient4.png)

## <a name="customizing-a-path-gradient"></a><span data-ttu-id="c2a47-138">Personalizando um gradiente de caminho</span><span class="sxs-lookup"><span data-stu-id="c2a47-138">Customizing a Path Gradient</span></span>

<span data-ttu-id="c2a47-139">Uma maneira de personalizar um pincel de gradiente de caminho é definir suas escalas de foco.</span><span class="sxs-lookup"><span data-stu-id="c2a47-139">One way to customize a path gradient brush is to set its focus scales.</span></span> <span data-ttu-id="c2a47-140">O ajuste de escala do foco especifica um caminho interno que se encontra dentro do caminho principal.</span><span class="sxs-lookup"><span data-stu-id="c2a47-140">The focus scales specify an inner path that lies inside the main path.</span></span> <span data-ttu-id="c2a47-141">A cor central é exibida em qualquer lugar dentro desse caminho interno e não apenas no ponto central.</span><span class="sxs-lookup"><span data-stu-id="c2a47-141">The center color is displayed everywhere inside that inner path rather than only at the center point.</span></span> <span data-ttu-id="c2a47-142">Para definir as escalas de foco de um pincel de gradiente de caminho, chame o método [**PathGradientBrush:: SetFocusScales**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setfocusscales) .</span><span class="sxs-lookup"><span data-stu-id="c2a47-142">To set the focus scales of a path gradient brush, call the [**PathGradientBrush::SetFocusScales**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setfocusscales) method.</span></span>

<span data-ttu-id="c2a47-143">O exemplo a seguir cria um pincel de gradiente de caminho com base em uma trajetória elíptica.</span><span class="sxs-lookup"><span data-stu-id="c2a47-143">The following example creates a path gradient brush based on an elliptical path.</span></span> <span data-ttu-id="c2a47-144">O código define a cor do limite como azul, define a cor do centro para azul-piscina e, em seguida, usa o pincel de gradiente de caminho para preencher o caminho elíptico.</span><span class="sxs-lookup"><span data-stu-id="c2a47-144">The code sets the boundary color to blue, sets the center color to aqua, and then uses the path gradient brush to fill the elliptical path.</span></span>

<span data-ttu-id="c2a47-145">Em seguida, o código define as escalas de foco do pincel de gradiente de caminho.</span><span class="sxs-lookup"><span data-stu-id="c2a47-145">Next the code sets the focus scales of the path gradient brush.</span></span> <span data-ttu-id="c2a47-146">A escala de foco de x é definida como 0,3 e a escala de foco de y é definida como 0,8.</span><span class="sxs-lookup"><span data-stu-id="c2a47-146">The x focus scale is set to 0.3, and the y focus scale is set to 0.8.</span></span> <span data-ttu-id="c2a47-147">O código chama o método [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) de um objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para que a chamada subsequente para [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) Preencha uma elipse que fica à direita da primeira elipse.</span><span class="sxs-lookup"><span data-stu-id="c2a47-147">The code calls the [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object so that the subsequent call to [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) fills an ellipse that sits to the right of the first ellipse.</span></span>

<span data-ttu-id="c2a47-148">Para ver o efeito de escalas de foco, imagine uma pequena elipse que compartilha seu centro com a elipse principal.</span><span class="sxs-lookup"><span data-stu-id="c2a47-148">To see the effect of the focus scales, imagine a small ellipse that shares its center with the main ellipse.</span></span> <span data-ttu-id="c2a47-149">A pequena elipse (interna) é a elipse principal dimensionada (sobre seu centro) horizontalmente por um fator de 0,3 e verticalmente por um fator de 0,8.</span><span class="sxs-lookup"><span data-stu-id="c2a47-149">The small (inner) ellipse is the main ellipse scaled (about its center) horizontally by a factor of 0.3 and vertically by a factor of 0.8.</span></span> <span data-ttu-id="c2a47-150">Quando você vai do limite da elipse externa para o limite da elipse interna, a cor altera gradualmente de azul para azul-piscina.</span><span class="sxs-lookup"><span data-stu-id="c2a47-150">As you move from the boundary of the outer ellipse to the boundary of the inner ellipse, the color changes gradually from blue to aqua.</span></span> <span data-ttu-id="c2a47-151">Quando você vai do limite da elipse interna ao centro compartilhado, a cor permanece azul-piscina.</span><span class="sxs-lookup"><span data-stu-id="c2a47-151">As you move from the boundary of the inner ellipse to the shared center, the color remains aqua.</span></span>


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



<span data-ttu-id="c2a47-152">A ilustração a seguir mostra a saída do código anterior.</span><span class="sxs-lookup"><span data-stu-id="c2a47-152">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="c2a47-153">A elipse à esquerda é azul-piscina somente no ponto central.</span><span class="sxs-lookup"><span data-stu-id="c2a47-153">The ellipse on the left is aqua only at the center point.</span></span> <span data-ttu-id="c2a47-154">A elipse à direita é azul-piscina em qualquer lugar dentro do caminho interno.</span><span class="sxs-lookup"><span data-stu-id="c2a47-154">The ellipse on the right is aqua everywhere inside the inner path.</span></span>

![ilustração mostrando duas reticências que sombream de azul-piscina a azul: a primeira tem muito pouca água; o segundo tem muito mais](images/focusscales1.png)

<span data-ttu-id="c2a47-156">Outra maneira de personalizar um pincel de gradiente de caminho é especificar uma matriz de cores predefinidas e uma matriz de posições de interpolação.</span><span class="sxs-lookup"><span data-stu-id="c2a47-156">Another way to customize a path gradient brush is to specify an array of preset colors and an array of interpolation positions.</span></span>

<span data-ttu-id="c2a47-157">O exemplo a seguir cria um pincel de gradiente de caminho com base em um triângulo.</span><span class="sxs-lookup"><span data-stu-id="c2a47-157">The following example creates a path gradient brush based on a triangle.</span></span> <span data-ttu-id="c2a47-158">O código chama o método [**PathGradientBrush:: SetInterpolationColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setinterpolationcolors) do pincel de gradiente de caminho para especificar uma matriz de cores de interpolação (verde escuro, água, azul) e uma matriz de posições de interpolação (0, 0,25, 1).</span><span class="sxs-lookup"><span data-stu-id="c2a47-158">The code calls the [**PathGradientBrush::SetInterpolationColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setinterpolationcolors) method of the path gradient brush to specify an array of interpolation colors (dark green, aqua, blue) and an array of interpolation positions (0, 0.25, 1).</span></span> <span data-ttu-id="c2a47-159">Ao mudar do limite do triângulo ao ponto central, a cor gradualmente muda de verde-escuro para azul-piscina e, em seguida, de azul-piscina para azul.</span><span class="sxs-lookup"><span data-stu-id="c2a47-159">As you move from the boundary of the triangle to the center point, the color changes gradually from dark green to aqua and then from aqua to blue.</span></span> <span data-ttu-id="c2a47-160">A alteração de verde-escuro para azul-piscina ocorre em 25 por cento da distância de verde-escuro para azul.</span><span class="sxs-lookup"><span data-stu-id="c2a47-160">The change from dark green to aqua happens in 25 percent of the distance from dark green to blue.</span></span>


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



<span data-ttu-id="c2a47-161">A ilustração a seguir mostra a saída do código anterior.</span><span class="sxs-lookup"><span data-stu-id="c2a47-161">The following illustration shows the output of the preceding code.</span></span>

![ilustração que mostra um triângulo que sombreia de azul no centro, para azul-piscina, para verde nas bordas](images/pathgradient4.png)

## <a name="setting-the-center-point"></a><span data-ttu-id="c2a47-163">Configurando o ponto central</span><span class="sxs-lookup"><span data-stu-id="c2a47-163">Setting the Center Point</span></span>

<span data-ttu-id="c2a47-164">Por padrão, o ponto central de um pincel de gradiente de caminho é o centroide de caminho usado para construir o pincel.</span><span class="sxs-lookup"><span data-stu-id="c2a47-164">By default, the center point of a path gradient brush is at the centroid of the path used to construct the brush.</span></span> <span data-ttu-id="c2a47-165">Você pode alterar o local do ponto central chamando o método [**PathGradientBrush:: SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) da classe [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) .</span><span class="sxs-lookup"><span data-stu-id="c2a47-165">You can change the location of the center point by calling the [**PathGradientBrush::SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) method of the [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) class.</span></span>

<span data-ttu-id="c2a47-166">O exemplo a seguir cria um pincel de gradiente de caminho com base em uma elipse.</span><span class="sxs-lookup"><span data-stu-id="c2a47-166">The following example creates a path gradient brush based on an ellipse.</span></span> <span data-ttu-id="c2a47-167">O centro da elipse é em (70, 35), mas o ponto central do pincel de gradiente de caminho é definido como (120, 40).</span><span class="sxs-lookup"><span data-stu-id="c2a47-167">The center of the ellipse is at (70, 35), but the center point of the path gradient brush is set to (120, 40).</span></span>


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



<span data-ttu-id="c2a47-168">A ilustração a seguir mostra a elipse preenchida e o ponto central do pincel de gradiente de caminho.</span><span class="sxs-lookup"><span data-stu-id="c2a47-168">The following illustration shows the filled ellipse and the center point of the path gradient brush.</span></span>

![ilustração mostrando uma elipse que preenche de azul para azul-piscina de um ponto central próximo a uma extremidade](images/pathgradient5.png)

<span data-ttu-id="c2a47-170">Você pode definir o ponto central de um pincel de gradiente de caminho para um local fora do caminho que foi usado para construir o pincel.</span><span class="sxs-lookup"><span data-stu-id="c2a47-170">You can set the center point of a path gradient brush to a location outside the path that was used to construct the brush.</span></span> <span data-ttu-id="c2a47-171">No código anterior, se você substituir a chamada para [**PathGradientBrush:: SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) por `pthGrBrush.SetCenterPoint(Point(145, 35))` , você receberá o seguinte resultado.</span><span class="sxs-lookup"><span data-stu-id="c2a47-171">In the preceding code, if you replace the call to [**PathGradientBrush::SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) with `pthGrBrush.SetCenterPoint(Point(145, 35))`, you will get the following result.</span></span>

![ilustração mostrando uma elipse que preenche de vermelho para amarelo de um ponto central que está fora da borda da elipse](images/pathgradient6.png)

<span data-ttu-id="c2a47-173">Na ilustração anterior, os pontos na extremidade direita da elipse não são azul puro (embora muito parecido).</span><span class="sxs-lookup"><span data-stu-id="c2a47-173">In the preceding illustration, the points at the far right of the ellipse are not pure blue (although they are very close).</span></span> <span data-ttu-id="c2a47-174">As cores no gradiente são posicionadas como se o preenchimento tivesse tido permissão para alcançar o ponto (145, 35), a cor teria atingido o azul puro (0, 0, 255).</span><span class="sxs-lookup"><span data-stu-id="c2a47-174">The colors in the gradient are positioned as if the fill had been allowed to reach the point (145, 35), the color would have reached pure blue (0, 0, 255).</span></span> <span data-ttu-id="c2a47-175">Mas o preenchimento nunca atinge (145, 35), pois um pincel de gradiente de caminho pinta apenas dentro de seu caminho.</span><span class="sxs-lookup"><span data-stu-id="c2a47-175">But the fill never reaches (145, 35) because a path gradient brush paints only inside its path.</span></span>

 

 
