---
description: O Windows GDI+ fornece contêineres que você pode usar para substituir temporariamente ou aumentar parte do estado em um objeto gráfico.
ms.assetid: f3fce8ef-903a-4b9d-b76c-562739d02eb3
title: Contêineres de elementos gráficos aninhados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29f9d9feac3494b423d844cb1e3da359af33eaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921431"
---
# <a name="nested-graphics-containers"></a><span data-ttu-id="c0067-103">Contêineres de elementos gráficos aninhados</span><span class="sxs-lookup"><span data-stu-id="c0067-103">Nested Graphics Containers</span></span>

<span data-ttu-id="c0067-104">O Windows GDI+ fornece contêineres que você pode usar para substituir temporariamente ou aumentar parte do estado em um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="c0067-104">Windows GDI+ provides containers that you can use to temporarily replace or augment part of the state in a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="c0067-105">Você cria um contêiner chamando o método [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) de um objeto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="c0067-105">You create a container by calling the [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) method of a **Graphics** object.</span></span> <span data-ttu-id="c0067-106">Você pode chamar os **elementos gráficos:: BeginContainer** repetidamente para formar Contêineres aninhados.</span><span class="sxs-lookup"><span data-stu-id="c0067-106">You can call **Graphics::BeginContainer** repeatedly to form nested containers.</span></span>

## <a name="transformations-in-nested-containers"></a><span data-ttu-id="c0067-107">Transformações em contêineres aninhados</span><span class="sxs-lookup"><span data-stu-id="c0067-107">Transformations in Nested Containers</span></span>

<span data-ttu-id="c0067-108">O exemplo a seguir cria um objeto de [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e um contêiner dentro desse objeto de **gráfico** .</span><span class="sxs-lookup"><span data-stu-id="c0067-108">The following example creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a container within that **Graphics** object.</span></span> <span data-ttu-id="c0067-109">A transformação mundial do objeto **gráfico** é uma tradução 100 unidades na direção x e 80 unidades na direção y.</span><span class="sxs-lookup"><span data-stu-id="c0067-109">The world transformation of the **Graphics** object is a translation 100 units in the x direction and 80 units in the y direction.</span></span> <span data-ttu-id="c0067-110">A transformação global do contêiner é uma rotação de 30 graus.</span><span class="sxs-lookup"><span data-stu-id="c0067-110">The world transformation of the container is a 30-degree rotation.</span></span> <span data-ttu-id="c0067-111">O código faz a chamada</span><span class="sxs-lookup"><span data-stu-id="c0067-111">The code makes the call</span></span>


```
DrawRectangle(&pen, -60, -30, 120, 60)
```



<span data-ttu-id="c0067-112">caixas.</span><span class="sxs-lookup"><span data-stu-id="c0067-112">twice.</span></span> <span data-ttu-id="c0067-113">A primeira chamada para [**gráficos::D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) está *dentro do contêiner*; ou seja, a chamada está entre as chamadas para [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) e [**gráficos:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer).</span><span class="sxs-lookup"><span data-stu-id="c0067-113">The first call to [**Graphics::DrawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) is *inside the container*; that is, the call is in between the calls to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) and [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer).</span></span> <span data-ttu-id="c0067-114">A segunda chamada para **Graphics::D rawrectangle** é após a chamada para **Graphics:: EndContainer**.</span><span class="sxs-lookup"><span data-stu-id="c0067-114">The second call to **Graphics::DrawRectangle** is after the call to **Graphics::EndContainer**.</span></span>


```
Graphics           graphics(hdc);
Pen                pen(Color(255, 255, 0, 0));
GraphicsContainer  graphicsContainer;

graphics.TranslateTransform(100.0f, 80.0f);

graphicsContainer = graphics.BeginContainer();
   graphics.RotateTransform(30.0f);
   graphics.DrawRectangle(&pen, -60, -30, 120, 60);
graphics.EndContainer(graphicsContainer);

graphics.DrawRectangle(&pen, -60, -30, 120, 60);
```



<span data-ttu-id="c0067-115">No código anterior, o retângulo desenhado de dentro do contêiner é transformado primeiro pela transformação mundial do contêiner (rotação) e, em seguida, pela transformação mundial do objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) (translação).</span><span class="sxs-lookup"><span data-stu-id="c0067-115">In the preceding code, the rectangle drawn from inside the container is transformed first by the world transformation of the container (rotation) and then by the world transformation of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object (translation).</span></span> <span data-ttu-id="c0067-116">O retângulo desenhado de fora do contêiner é transformado apenas pela transformação mundial do objeto **gráfico** (translação).</span><span class="sxs-lookup"><span data-stu-id="c0067-116">The rectangle drawn from outside the container is transformed only by the world transformation of the **Graphics** object (translation).</span></span> <span data-ttu-id="c0067-117">A ilustração a seguir mostra os dois retângulos.</span><span class="sxs-lookup"><span data-stu-id="c0067-117">The following illustration shows the two rectangles.</span></span>

![captura de tela de uma janela com dois retângulos vermelhos centralizados no mesmo ponto, mas com rotações diferentes](images/nestedcontainers1.png)

 

## <a name="clipping-in-nested-containers"></a><span data-ttu-id="c0067-119">Recorte em contêineres aninhados</span><span class="sxs-lookup"><span data-stu-id="c0067-119">Clipping in Nested Containers</span></span>

<span data-ttu-id="c0067-120">O exemplo a seguir ilustra como contêineres aninhados lidam com regiões de recorte.</span><span class="sxs-lookup"><span data-stu-id="c0067-120">The following example illustrates how nested containers handle clipping regions.</span></span> <span data-ttu-id="c0067-121">O código cria um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e um contêiner dentro desse objeto **gráfico** .</span><span class="sxs-lookup"><span data-stu-id="c0067-121">The code creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a container within that **Graphics** object.</span></span> <span data-ttu-id="c0067-122">A região de recorte do objeto de **gráficos** é um retângulo e a região de recorte do contêiner é uma elipse.</span><span class="sxs-lookup"><span data-stu-id="c0067-122">The clipping region of the **Graphics** object is a rectangle, and the clipping region of the container is an ellipse.</span></span> <span data-ttu-id="c0067-123">O código faz duas chamadas para o método [**Graphics::D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) .</span><span class="sxs-lookup"><span data-stu-id="c0067-123">The code makes two calls to the [**Graphics::DrawLine**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method.</span></span> <span data-ttu-id="c0067-124">A primeira chamada para **gráficos::D rawline** está dentro do contêiner e a segunda chamada para **Graphics::D rawline** está fora do contêiner (após a chamada para [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)).</span><span class="sxs-lookup"><span data-stu-id="c0067-124">The first call to **Graphics::DrawLine** is inside the container, and the second call to **Graphics::DrawLine** is outside the container (after the call to [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)).</span></span> <span data-ttu-id="c0067-125">A primeira linha é recortada pela interseção das duas áreas de recorte.</span><span class="sxs-lookup"><span data-stu-id="c0067-125">The first line is clipped by the intersection of the two clipping regions.</span></span> <span data-ttu-id="c0067-126">A segunda linha é recortada apenas pela região de recorte retangular do objeto de **gráficos** .</span><span class="sxs-lookup"><span data-stu-id="c0067-126">The second line is clipped only by the rectangular clipping region of the **Graphics** object.</span></span>


```
Graphics           graphics(hdc);
GraphicsContainer  graphicsContainer;
Pen                redPen(Color(255, 255, 0, 0), 2);
Pen                bluePen(Color(255, 0, 0, 255), 2);
SolidBrush         aquaBrush(Color(255, 180, 255, 255));
SolidBrush         greenBrush(Color(255, 150, 250, 130));

graphics.SetClip(Rect(50, 65, 150, 120));
graphics.FillRectangle(&aquaBrush, 50, 65, 150, 120);

graphicsContainer = graphics.BeginContainer();
   // Create a path that consists of a single ellipse.
   GraphicsPath path;
   path.AddEllipse(75, 50, 100, 150);

  // Construct a region based on the path.
   Region region(&path);
   graphics.FillRegion(&greenBrush, &region);

   graphics.SetClip(&region);
   graphics.DrawLine(&redPen, 50, 0, 350, 300);
graphics.EndContainer(graphicsContainer);

graphics.DrawLine(&bluePen, 70, 0, 370, 300);
```



<span data-ttu-id="c0067-127">A ilustração a seguir mostra as duas linhas recortadas.</span><span class="sxs-lookup"><span data-stu-id="c0067-127">The following illustration shows the two clipped lines.</span></span>

![ilustração de uma elipse dentro de um retângulo, com uma linha recortada pela elipse e a outra pelo retângulo](images/nestedcontainers2.png)

<span data-ttu-id="c0067-129">Como os dois exemplos anteriores mostram, as transformações e áreas de recorte são cumulativas em contêineres aninhados.</span><span class="sxs-lookup"><span data-stu-id="c0067-129">As the two preceding examples show, transformations and clipping regions are cumulative in nested containers.</span></span> <span data-ttu-id="c0067-130">Se você definir as transformações mundiais do contêiner e do objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , ambas as transformações serão aplicadas aos itens extraídos de dentro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c0067-130">If you set the world transformations of the container and the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, both transformations will apply to items drawn from inside the container.</span></span> <span data-ttu-id="c0067-131">A transformação do contêiner será aplicada primeiro e a transformação do objeto de **gráficos** será aplicada em segundo lugar.</span><span class="sxs-lookup"><span data-stu-id="c0067-131">The transformation of the container will be applied first, and the transformation of the **Graphics** object will be applied second.</span></span> <span data-ttu-id="c0067-132">Se você definir as regiões de recorte do contêiner e o objeto de **gráficos** , os itens extraídos de dentro do contêiner serão recortados pela interseção das duas regiões de recorte.</span><span class="sxs-lookup"><span data-stu-id="c0067-132">If you set the clipping regions of the container and the **Graphics** object, items drawn from inside the container will be clipped by the intersection of the two clipping regions.</span></span>

## <a name="quality-settings-in-nested-containers"></a><span data-ttu-id="c0067-133">Configurações de qualidade em contêineres aninhados</span><span class="sxs-lookup"><span data-stu-id="c0067-133">Quality Settings in Nested Containers</span></span>

<span data-ttu-id="c0067-134">As configurações de qualidade ( [**SmoothingMode**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode), [**TextRenderingHint**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)e like) em Contêineres aninhados não são cumulativas; em vez disso, as configurações de qualidade do contêiner substituem temporariamente as configurações de qualidade de um objeto de [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="c0067-134">Quality settings ( [**SmoothingMode**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode), [**TextRenderingHint**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint), and the like) in nested containers are not cumulative; rather, the quality settings of the container temporarily replace the quality settings of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="c0067-135">Quando você cria um novo contêiner, as configurações de qualidade do contêiner são definidas com valores padrão.</span><span class="sxs-lookup"><span data-stu-id="c0067-135">When you create a new container, the quality settings for that container are set to default values.</span></span> <span data-ttu-id="c0067-136">Por exemplo, suponha que você tenha um objeto **gráfico** com um modo de suavização de [\* \* \* \* SmoothingModeAntiAlias \* \* \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode).</span><span class="sxs-lookup"><span data-stu-id="c0067-136">For example, suppose you have a **Graphics** object with a smoothing mode of [\*\*\*\*SmoothingModeAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode).</span></span> <span data-ttu-id="c0067-137">Quando você cria um contêiner, o modo de suavização dentro do contêiner é o modo de suavização padrão.</span><span class="sxs-lookup"><span data-stu-id="c0067-137">When you create a container, the smoothing mode inside the container is the default smoothing mode.</span></span> <span data-ttu-id="c0067-138">Você tem a liberdade de definir o modo de suavização do contêiner e os itens desenhados de dentro do contêiner serão desenhados de acordo com o modo é definido por você.</span><span class="sxs-lookup"><span data-stu-id="c0067-138">You are free to set the smoothing mode of the container, and any items drawn from inside the container will be drawn according to the mode you set.</span></span> <span data-ttu-id="c0067-139">Os itens desenhados após a chamada para [**gráficos:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) serão desenhados de acordo com o modo de suavização (\* \* \* *[SmoothingModeAntiAlias \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)* \*) que estava em vigor antes da chamada para [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).</span><span class="sxs-lookup"><span data-stu-id="c0067-139">Items drawn after the call to [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) will be drawn according to the smoothing mode ([\*\*\*\*SmoothingModeAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)) that was in place before the call to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).</span></span>

## <a name="several-layers-of-nested-containers"></a><span data-ttu-id="c0067-140">Várias camadas de contêineres aninhados</span><span class="sxs-lookup"><span data-stu-id="c0067-140">Several Layers of Nested Containers</span></span>

<span data-ttu-id="c0067-141">Você não está limitado a um contêiner em um objeto de [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="c0067-141">You are not limited to one container in a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="c0067-142">É possível criar uma sequência de contêineres, cada um deles aninhado no anterior e é possível especificar a transformação global, a área de recorte e as configurações de qualidade de cada um desses contêineres aninhados.</span><span class="sxs-lookup"><span data-stu-id="c0067-142">You can create a sequence of containers, each nested in the preceding, and you can specify the world transformation, clipping region, and quality settings of each of those nested containers.</span></span> <span data-ttu-id="c0067-143">Se você chamar um método de desenho de dentro do contêiner mais interno, as transformações serão aplicadas em ordem, começando pelo contêiner mais interno e terminando com mais externo.</span><span class="sxs-lookup"><span data-stu-id="c0067-143">If you call a drawing method from inside the innermost container, the transformations will be applied in order, starting with the innermost container and ending with the outermost container.</span></span> <span data-ttu-id="c0067-144">Itens desenhados de dentro do contêiner mais interno serão recortados pela interseção de todas as áreas de recorte.</span><span class="sxs-lookup"><span data-stu-id="c0067-144">Items drawn from inside the innermost container will be clipped by the intersection of all the clipping regions.</span></span>

<span data-ttu-id="c0067-145">O exemplo a seguir cria um objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e define sua dica de renderização de texto como [\* \* \* \* TextRenderingHintAntiAlias \* \* \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint).</span><span class="sxs-lookup"><span data-stu-id="c0067-145">The following example creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and sets its text rendering hint to [\*\*\*\*TextRenderingHintAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint).</span></span> <span data-ttu-id="c0067-146">O código cria dois contêineres, um aninhado dentro do outro.</span><span class="sxs-lookup"><span data-stu-id="c0067-146">The code creates two containers, one nested within the other.</span></span> <span data-ttu-id="c0067-147">A dica de renderização de texto do contêiner externo é definida como [\* \* \* \* TextRenderingHintSingleBitPerPixel \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)\* \*, e a dica de renderização de texto do contêiner interno é definida como [\* \* \* \* TextRenderingHintAntiAlias \* \* \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint).</span><span class="sxs-lookup"><span data-stu-id="c0067-147">The text rendering hint of the outer container is set to [\*\*\*\*TextRenderingHintSingleBitPerPixel\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint), and the text rendering hint of the inner container is set to [\*\*\*\*TextRenderingHintAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint).</span></span> <span data-ttu-id="c0067-148">O código desenha três cadeias de caracteres: uma do contêiner interno, uma do contêiner externo e outra do objeto **gráfico** em si.</span><span class="sxs-lookup"><span data-stu-id="c0067-148">The code draws three strings: one from the inner container, one from the outer container, and one from the **Graphics** object itself.</span></span>


```
Graphics graphics(hdc);
GraphicsContainer innerContainer;
GraphicsContainer outerContainer;
SolidBrush brush(Color(255, 0, 0, 255));
FontFamily fontFamily(L"Times New Roman");
Font font(&fontFamily, 36, FontStyleRegular, UnitPixel);

graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);

outerContainer = graphics.BeginContainer();

   graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);

   innerContainer = graphics.BeginContainer();
      graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
      graphics.DrawString(L"Inner Container", 15, &font,
         PointF(20, 10), &brush);
   graphics.EndContainer(innerContainer);

   graphics.DrawString(L"Outer Container", 15, &font, PointF(20, 50), &brush);

graphics.EndContainer(outerContainer);

graphics.DrawString(L"Graphics Object", 15, &font, PointF(20, 90), &brush);
```



<span data-ttu-id="c0067-149">A ilustração a seguir mostra as três cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c0067-149">The following illustration shows the three strings.</span></span> <span data-ttu-id="c0067-150">As cadeias de caracteres desenhadas do contêiner interno e do objeto de [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) são suavizadas por anti-aliasing.</span><span class="sxs-lookup"><span data-stu-id="c0067-150">The strings drawn from the inner container and the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object are smoothed by antialiasing.</span></span> <span data-ttu-id="c0067-151">A cadeia de caracteres extraída do contêiner externo não é suavizada por anti-aliasing devido à configuração TextRenderingHintSingleBitPerPixel.</span><span class="sxs-lookup"><span data-stu-id="c0067-151">The string drawn from the outer container is not smoothed by antialiasing because of the TextRenderingHintSingleBitPerPixel setting.</span></span>

![ilustração de um retângulo que contém a mesma cadeia de caracteres; somente os caracteres da primeira e da última linha são suaves](images/nestedcontainers3.png)

 

 
