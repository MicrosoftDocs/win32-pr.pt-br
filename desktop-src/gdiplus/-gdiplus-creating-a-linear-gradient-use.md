---
description: O GDI+ fornece gradientes lineares horizontais, verticais e diagonais. Por padrão, a cor em um gradiente linear muda uniformemente. No entanto, você pode personalizar um gradiente linear para que a cor mude de maneira não uniforme.
ms.assetid: 9b0236b2-be6b-4918-a106-5b0e6c3dd5ff
title: Criando um gradiente linear
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d66b9f5a3a07061e8b3d19140c25a9f3a33052a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554840"
---
# <a name="creating-a-linear-gradient"></a><span data-ttu-id="8c923-105">Criando um gradiente linear</span><span class="sxs-lookup"><span data-stu-id="8c923-105">Creating a Linear Gradient</span></span>

<span data-ttu-id="8c923-106">O GDI+ fornece gradientes lineares horizontais, verticais e diagonais.</span><span class="sxs-lookup"><span data-stu-id="8c923-106">GDI+ provides horizontal, vertical, and diagonal linear gradients.</span></span> <span data-ttu-id="8c923-107">Por padrão, a cor em um gradiente linear muda uniformemente.</span><span class="sxs-lookup"><span data-stu-id="8c923-107">By default, the color in a linear gradient changes uniformly.</span></span> <span data-ttu-id="8c923-108">No entanto, você pode personalizar um gradiente linear para que a cor mude de maneira não uniforme.</span><span class="sxs-lookup"><span data-stu-id="8c923-108">However, you can customize a linear gradient so that the color changes in a non-uniform fashion.</span></span>

-   [<span data-ttu-id="8c923-109">Gradientes lineares horizontais</span><span class="sxs-lookup"><span data-stu-id="8c923-109">Horizontal Linear Gradients</span></span>](#horizontal-linear-gradients)
-   [<span data-ttu-id="8c923-110">Personalizando gradientes lineares</span><span class="sxs-lookup"><span data-stu-id="8c923-110">Customizing Linear Gradients</span></span>](#customizing-linear-gradients)
-   [<span data-ttu-id="8c923-111">Gradientes lineares diagonais</span><span class="sxs-lookup"><span data-stu-id="8c923-111">Diagonal Linear Gradients</span></span>](#diagonal-linear-gradients)

## <a name="horizontal-linear-gradients"></a><span data-ttu-id="8c923-112">Gradientes lineares horizontais</span><span class="sxs-lookup"><span data-stu-id="8c923-112">Horizontal Linear Gradients</span></span>

<span data-ttu-id="8c923-113">O exemplo a seguir usa um pincel de gradiente linear horizontal para preencher uma linha, uma elipse e um retângulo:</span><span class="sxs-lookup"><span data-stu-id="8c923-113">The following example uses a horizontal linear gradient brush to fill a line, an ellipse, and a rectangle:</span></span>


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



<span data-ttu-id="8c923-114">O construtor [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) recebe quatro argumentos: dois pontos e duas cores.</span><span class="sxs-lookup"><span data-stu-id="8c923-114">The [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) constructor receives four arguments: two points and two colors.</span></span> <span data-ttu-id="8c923-115">O primeiro ponto (0, 10) é associado à primeira cor (vermelho) e o segundo ponto (200, 10) é associado à segunda cor (azul).</span><span class="sxs-lookup"><span data-stu-id="8c923-115">The first point (0, 10) is associated with the first color (red), and the second point (200, 10) is associated with the second color (blue).</span></span> <span data-ttu-id="8c923-116">Como seria de esperar, a linha desenhada de (10, 0) a (200, 10) muda gradualmente de vermelho para azul.</span><span class="sxs-lookup"><span data-stu-id="8c923-116">As you would expect, the line drawn from (0, 10) to (200, 10) changes gradually from red to blue.</span></span>

<span data-ttu-id="8c923-117">Os 10s nos pontos (50, 10) e (200, 10) não são importantes.</span><span class="sxs-lookup"><span data-stu-id="8c923-117">The 10s in the points (50, 10) and (200, 10) are not important.</span></span> <span data-ttu-id="8c923-118">O que é importante é que os dois pontos tenham a mesma coordenada de segunda, a linha que os conecta é horizontal.</span><span class="sxs-lookup"><span data-stu-id="8c923-118">What's important is that the two points have the same second coordinate — the line connecting them is horizontal.</span></span> <span data-ttu-id="8c923-119">A elipse e o retângulo também mudam gradualmente de vermelho para azul conforme a coordenada horizontal vai de 0 a 200.</span><span class="sxs-lookup"><span data-stu-id="8c923-119">The ellipse and the rectangle also change gradually from red to blue as the horizontal coordinate goes from 0 to 200.</span></span>

<span data-ttu-id="8c923-120">A ilustração a seguir mostra a linha, a elipse e o retângulo.</span><span class="sxs-lookup"><span data-stu-id="8c923-120">The following illustration shows the line, the ellipse, and the rectangle.</span></span> <span data-ttu-id="8c923-121">Observe que o gradiente de cores repete-se à medida que a coordenada horizontal aumenta além de 200.</span><span class="sxs-lookup"><span data-stu-id="8c923-121">Note that the color gradient repeats itself as the horizontal coordinate increases beyond 200.</span></span>

![ilustração mostrando um gradiente horizontal que preenche uma linha e uma elipse e um retângulo maior que a elipse](images/lineargradient1.png)

## <a name="customizing-linear-gradients"></a><span data-ttu-id="8c923-123">Personalizando gradientes lineares</span><span class="sxs-lookup"><span data-stu-id="8c923-123">Customizing Linear Gradients</span></span>

<span data-ttu-id="8c923-124">No exemplo anterior, os componentes de cor mudam linearmente conforme você vai de uma coordenada horizontal de 0 para uma coordenada horizontal de 200.</span><span class="sxs-lookup"><span data-stu-id="8c923-124">In the preceding example, the color components change linearly as you move from a horizontal coordinate of 0 to a horizontal coordinate of 200.</span></span> <span data-ttu-id="8c923-125">Por exemplo, um ponto cuja primeira coordenada esteja a meio caminho entre 0 e 200 terá um componente azul a meio caminho entre 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="8c923-125">For example, a point whose first coordinate is halfway between 0 and 200 will have a blue component that is halfway between 0 and 255.</span></span>

<span data-ttu-id="8c923-126">O GDI+ permite que você ajuste a maneira como uma cor varia de uma borda de um gradiente para a outra.</span><span class="sxs-lookup"><span data-stu-id="8c923-126">GDI+ allows you to adjust the way a color varies from one edge of a gradient to the other.</span></span> <span data-ttu-id="8c923-127">Suponha que você queira criar um pincel de gradiente que mude de preto para vermelho de acordo com a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8c923-127">Suppose you want to create a gradient brush that changes from black to red according to the following table.</span></span>



| <span data-ttu-id="8c923-128">Coordenada horizontal</span><span class="sxs-lookup"><span data-stu-id="8c923-128">Horizontal coordinate</span></span> | <span data-ttu-id="8c923-129">Componentes RGB</span><span class="sxs-lookup"><span data-stu-id="8c923-129">RGB components</span></span> |
|-----------------------|----------------|
| <span data-ttu-id="8c923-130">0</span><span class="sxs-lookup"><span data-stu-id="8c923-130">0</span></span>                     | <span data-ttu-id="8c923-131">(0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="8c923-131">(0, 0, 0)</span></span>      |
| <span data-ttu-id="8c923-132">40</span><span class="sxs-lookup"><span data-stu-id="8c923-132">40</span></span>                    | <span data-ttu-id="8c923-133">(128, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="8c923-133">(128, 0, 0)</span></span>    |
| <span data-ttu-id="8c923-134">200</span><span class="sxs-lookup"><span data-stu-id="8c923-134">200</span></span>                   | <span data-ttu-id="8c923-135">(255, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="8c923-135">(255, 0, 0)</span></span>    |



 

<span data-ttu-id="8c923-136">Observe que o componente vermelho está na metade da intensidade quando a coordenada horizontal está a apenas 20% do caminho de 0 a 200.</span><span class="sxs-lookup"><span data-stu-id="8c923-136">Note that the red component is at half intensity when the horizontal coordinate is only 20 percent of the way from 0 to 200.</span></span>

<span data-ttu-id="8c923-137">O exemplo a seguir chama o método [**LinearGradientBrush:: setblend**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblend) de um objeto [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) para associar três intensidades relativas a três posições relativas.</span><span class="sxs-lookup"><span data-stu-id="8c923-137">The following example calls the [**LinearGradientBrush::SetBlend**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblend) method of a [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) object to associate three relative intensities with three relative positions.</span></span> <span data-ttu-id="8c923-138">Como na tabela anterior, uma intensidade relativa de 0,5 é associada a uma posição relativa de 0,2.</span><span class="sxs-lookup"><span data-stu-id="8c923-138">As in the preceding table, a relative intensity of 0.5 is associated with a relative position of 0.2.</span></span> <span data-ttu-id="8c923-139">O código preenche uma elipse e um retângulo com o pincel de gradiente.</span><span class="sxs-lookup"><span data-stu-id="8c923-139">The code fills an ellipse and a rectangle with the gradient brush.</span></span>


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



<span data-ttu-id="8c923-140">A ilustração a seguir mostra o retângulo e elipse resultantes.</span><span class="sxs-lookup"><span data-stu-id="8c923-140">The following illustration shows the resulting ellipse and rectangle.</span></span>

![ilustração mostrando um gradiente horizontal que preenche uma elipse e um retângulo maior que a elipse](images/lineargradient2.png)

## <a name="diagonal-linear-gradients"></a><span data-ttu-id="8c923-142">Gradientes lineares diagonais</span><span class="sxs-lookup"><span data-stu-id="8c923-142">Diagonal Linear Gradients</span></span>

<span data-ttu-id="8c923-143">Os gradientes nos exemplos anteriores eram horizontais; ou seja, a cor muda gradualmente à medida que você se move ao longo de qualquer linha horizontal.</span><span class="sxs-lookup"><span data-stu-id="8c923-143">The gradients in the preceding examples have been horizontal; that is, the color changes gradually as you move along any horizontal line.</span></span> <span data-ttu-id="8c923-144">Você também pode definir gradientes verticais e gradientes diagonais.</span><span class="sxs-lookup"><span data-stu-id="8c923-144">You can also define vertical gradients and diagonal gradients.</span></span> <span data-ttu-id="8c923-145">O código a seguir passa os pontos (0, 0) e (200, 100) para um construtor [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) .</span><span class="sxs-lookup"><span data-stu-id="8c923-145">The following code passes the points (0, 0) and (200, 100) to a [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) constructor.</span></span> <span data-ttu-id="8c923-146">A cor azul é associada a (0, 0) e a cor verde é associada a (200, 100).</span><span class="sxs-lookup"><span data-stu-id="8c923-146">The color blue is associated with (0, 0), and the color green is associated with (200, 100).</span></span> <span data-ttu-id="8c923-147">Uma linha (com largura da caneta de 10) e uma elipse são preenchidas com o pincel de gradiente linear.</span><span class="sxs-lookup"><span data-stu-id="8c923-147">A line (with pen width 10) and an ellipse are filled with the linear gradient brush.</span></span>


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



<span data-ttu-id="8c923-148">A ilustração a seguir mostra a linha e a elipse.</span><span class="sxs-lookup"><span data-stu-id="8c923-148">The following illustration shows the line and the ellipse.</span></span> <span data-ttu-id="8c923-149">Observe que a cor na elipse muda gradualmente à medida que você se move ao longo de qualquer linha paralela à linha que passa por (0, 0) e (200, 100).</span><span class="sxs-lookup"><span data-stu-id="8c923-149">Note that the color in the ellipse changes gradually as you move along any line that is parallel to the line passing through (0, 0) and (200, 100).</span></span>

![ilustração mostrando um gradiente diagonal que preenche uma elipse e uma linha diagonal](images/lineargradient3.png)

 

 



