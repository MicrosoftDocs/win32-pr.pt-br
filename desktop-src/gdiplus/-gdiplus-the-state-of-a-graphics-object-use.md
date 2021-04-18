---
description: A classe Graphics é a essência do Windows GDI+. Para desenhar qualquer coisa, você cria um objeto de gráfico, define suas propriedades e chama seus métodos (DrawLine, DrawImage, drawstring e similares).
ms.assetid: 7d70f9fe-c0b2-4d65-815d-483d06df96ad
title: O estado de um objeto de elementos gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661733f944b08633b5df84eed3ac488e612d9e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554127"
---
# <a name="the-state-of-a-graphics-object"></a><span data-ttu-id="a993f-104">O estado de um objeto de elementos gráficos</span><span class="sxs-lookup"><span data-stu-id="a993f-104">The State of a Graphics Object</span></span>

<span data-ttu-id="a993f-105">A classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) é a essência do Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="a993f-105">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class is at the heart of Windows GDI+.</span></span> <span data-ttu-id="a993f-106">Para desenhar qualquer coisa, você cria um objeto de **gráfico** , define suas propriedades e chama seus métodos ( [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)), [drawstring](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))e similares).</span><span class="sxs-lookup"><span data-stu-id="a993f-106">To draw anything, you create a **Graphics** object, set its properties, and call its methods ( [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)), [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)), and the like).</span></span>

<span data-ttu-id="a993f-107">O exemplo a seguir constrói um objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e um objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) e, em seguida, chama o método [**Graphics::D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) do objeto **Graphics** :</span><span class="sxs-lookup"><span data-stu-id="a993f-107">The following example constructs a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object and then calls the [**Graphics::DrawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) method of the **Graphics** object:</span></span>


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



<span data-ttu-id="a993f-108">No código anterior, o método [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) retorna um identificador para um contexto de dispositivo e esse identificador é passado para o construtor de [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="a993f-108">In the preceding code, the [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) method returns a handle to a device context, and that handle is passed to the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span> <span data-ttu-id="a993f-109">Um contexto de dispositivo é uma estrutura (mantida pelo Windows) que contém informações sobre o dispositivo de vídeo específico que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="a993f-109">A device context is a structure (maintained by Windows) that holds information about the particular display device being used.</span></span>

## <a name="graphics-state"></a><span data-ttu-id="a993f-110">Estado gráfico</span><span class="sxs-lookup"><span data-stu-id="a993f-110">Graphics State</span></span>

<span data-ttu-id="a993f-111">Um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) faz mais do que fornecer métodos de desenho, como [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) e [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)).</span><span class="sxs-lookup"><span data-stu-id="a993f-111">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object does more than provide drawing methods, such as [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) and [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)).</span></span> <span data-ttu-id="a993f-112">Um objeto **gráfico** também mantém o estado gráfico, que pode ser dividido nas seguintes categorias:</span><span class="sxs-lookup"><span data-stu-id="a993f-112">A **Graphics** object also maintains graphics state, which can be divided into the following categories:</span></span>

-   <span data-ttu-id="a993f-113">Um link para um contexto de dispositivo</span><span class="sxs-lookup"><span data-stu-id="a993f-113">A link to a device context</span></span>
-   <span data-ttu-id="a993f-114">Configurações de qualidade</span><span class="sxs-lookup"><span data-stu-id="a993f-114">Quality settings</span></span>
-   <span data-ttu-id="a993f-115">Transformações</span><span class="sxs-lookup"><span data-stu-id="a993f-115">Transformations</span></span>
-   <span data-ttu-id="a993f-116">Uma região de recorte</span><span class="sxs-lookup"><span data-stu-id="a993f-116">A clipping region</span></span>

### <a name="device-context"></a><span data-ttu-id="a993f-117">Contexto do dispositivo</span><span class="sxs-lookup"><span data-stu-id="a993f-117">Device Context</span></span>

<span data-ttu-id="a993f-118">Como programador de aplicativos, você não precisa pensar na interação entre um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e seu contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a993f-118">As an application programmer, you don't have to think about the interaction between a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and its device context.</span></span> <span data-ttu-id="a993f-119">Essa interação é tratada pela GDI+ em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="a993f-119">This interaction is handled by GDI+ behind the scenes.</span></span>

### <a name="quality-settings"></a><span data-ttu-id="a993f-120">Configurações de Qualidade</span><span class="sxs-lookup"><span data-stu-id="a993f-120">Quality Settings</span></span>

<span data-ttu-id="a993f-121">Um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) tem várias propriedades que influenciam a qualidade dos itens que são desenhados na tela.</span><span class="sxs-lookup"><span data-stu-id="a993f-121">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object has several properties that influence the quality of the items that are drawn on the screen.</span></span> <span data-ttu-id="a993f-122">Você pode exibir e manipular essas propriedades chamando métodos get e Set.</span><span class="sxs-lookup"><span data-stu-id="a993f-122">You can view and manipulate these properties by calling get and set methods.</span></span> <span data-ttu-id="a993f-123">Por exemplo, você pode chamar o método [**Graphics:: SetTextRenderingHint**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) para especificar o tipo de anti-aliasing (se houver) aplicado ao texto.</span><span class="sxs-lookup"><span data-stu-id="a993f-123">For example, you can call the [**Graphics::SetTextRenderingHint**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) method to specify the type of antialiasing (if any) applied to text.</span></span> <span data-ttu-id="a993f-124">Outros métodos definidos que influenciam a qualidade são [**elementos gráficos:: SetSmoothingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode), [**Graphics:: SetCompositingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode), [**Graphics:: SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality)e [**Graphics:: setinterpolamode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setinterpolationmode).</span><span class="sxs-lookup"><span data-stu-id="a993f-124">Other set methods that influence quality are [**Graphics::SetSmoothingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode), [**Graphics::SetCompositingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode), [**Graphics::SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality), and [**Graphics::SetInterpolationMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setinterpolationmode).</span></span>

<span data-ttu-id="a993f-125">O exemplo a seguir desenha duas elipses, uma com o modo de suavização definido como [\* \* \* \* SmoothingModeAntiAlias \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) \* \* e outra com o modo de suavização definido como [\* \* \* \* SmoothingModeHighSpeed \* \* \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode):</span><span class="sxs-lookup"><span data-stu-id="a993f-125">The following example draws two ellipses, one with the smoothing mode set to [\*\*\*\*SmoothingModeAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) and one with the smoothing mode set to [\*\*\*\*SmoothingModeHighSpeed\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode):</span></span>


```
Graphics graphics(hdc);
Pen pen(Color(255, 0, 255, 0));  // opaque green

graphics.SetSmoothingMode(SmoothingModeAntiAlias);
graphics.DrawEllipse(&pen, 0, 0, 200, 100);
graphics.SetSmoothingMode(SmoothingModeHighSpeed);
graphics.DrawEllipse(&pen, 0, 150, 200, 100);
```



### <a name="transformations"></a><span data-ttu-id="a993f-126">Transformações</span><span class="sxs-lookup"><span data-stu-id="a993f-126">Transformations</span></span>

<span data-ttu-id="a993f-127">Um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) mantém duas transformações (mundo e página) que são aplicadas a todos os itens desenhados por esse objeto **gráfico** .</span><span class="sxs-lookup"><span data-stu-id="a993f-127">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object maintains two transformations (world and page) that are applied to all items drawn by that **Graphics** object.</span></span> <span data-ttu-id="a993f-128">Qualquer transformação afim pode ser armazenada na transformação global.</span><span class="sxs-lookup"><span data-stu-id="a993f-128">Any affine transformation can be stored in the world transformation.</span></span> <span data-ttu-id="a993f-129">Transformações afins incluem colocação em escala, rotação, reflexão, distorção e translação.</span><span class="sxs-lookup"><span data-stu-id="a993f-129">Affine transformations include scaling, rotating, reflecting, skewing, and translating.</span></span> <span data-ttu-id="a993f-130">A transformação de página pode ser usada para colocação em escala e para alterar unidades (por exemplo, pixels em polegadas).</span><span class="sxs-lookup"><span data-stu-id="a993f-130">The page transformation can be used for scaling and for changing units (for example, pixels to inches).</span></span> <span data-ttu-id="a993f-131">Para obter mais informações sobre transformações, consulte [coordenar sistemas e transformações](-gdiplus-coordinate-systems-and-transformations-about.md).</span><span class="sxs-lookup"><span data-stu-id="a993f-131">For more information on transformations, see [Coordinate Systems and Transformations](-gdiplus-coordinate-systems-and-transformations-about.md).</span></span>

<span data-ttu-id="a993f-132">O exemplo a seguir define as transformações World e Page de um objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="a993f-132">The following example sets the world and page transformations of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="a993f-133">A transformação global é definida com uma rotação de 30 graus.</span><span class="sxs-lookup"><span data-stu-id="a993f-133">The world transformation is set to a 30-degree rotation.</span></span> <span data-ttu-id="a993f-134">A transformação página é definida para que as coordenadas passadas para o segundo [**gráfico::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) será tratado como milímetros em vez de pixels.</span><span class="sxs-lookup"><span data-stu-id="a993f-134">The page transformation is set so that the coordinates passed to the second [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) will be treated as millimeters instead of pixels.</span></span> <span data-ttu-id="a993f-135">O código faz duas chamadas idênticas para o método **Graphics::D rawellipse** .</span><span class="sxs-lookup"><span data-stu-id="a993f-135">The code makes two identical calls to the **Graphics::DrawEllipse** method.</span></span> <span data-ttu-id="a993f-136">A transformação do mundo é aplicada ao primeiro **elemento gráfico::D chamada rawellipse** , e ambas as transformações (mundo e página) são aplicadas à segunda **imagem::D** chamada de rawellipse.</span><span class="sxs-lookup"><span data-stu-id="a993f-136">The world transformation is applied to the first **Graphics::DrawEllipse** call, and both transformations (world and page) are applied to the second **Graphics::DrawEllipse** call.</span></span>


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0));

graphics.ResetTransform();
graphics.RotateTransform(30.0f);            // World transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
graphics.SetPageUnit(UnitMillimeter);       // Page transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
```



<span data-ttu-id="a993f-137">A ilustração a seguir mostra as duas elipses.</span><span class="sxs-lookup"><span data-stu-id="a993f-137">The following illustration shows the two ellipses.</span></span> <span data-ttu-id="a993f-138">Observe que a rotação de 30 graus é sobre a origem do sistema de coordenadas (canto superior esquerdo da área de cliente), e não sobre os centros das elipses.</span><span class="sxs-lookup"><span data-stu-id="a993f-138">Note that the 30-degree rotation is about the origin of the coordinate system (upper-left corner of the client area), not about the centers of the ellipses.</span></span> <span data-ttu-id="a993f-139">Observe também que a largura da caneta de 1 significa 1 pixel para a primeira elipse e 1 milímetro para a segunda elipse.</span><span class="sxs-lookup"><span data-stu-id="a993f-139">Also note that the pen width of 1 means 1 pixel for the first ellipse and 1 millimeter for the second ellipse.</span></span>

![captura de tela de uma janela que contém uma elipse pequena, fina e uma elipse grande e espessa](images/graphicsascon1.png)

 

### <a name="clipping-region"></a><span data-ttu-id="a993f-141">Área de recorte</span><span class="sxs-lookup"><span data-stu-id="a993f-141">Clipping Region</span></span>

<span data-ttu-id="a993f-142">Um objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) mantém uma região de recorte que se aplica a todos os itens desenhados por esse objeto **gráfico** .</span><span class="sxs-lookup"><span data-stu-id="a993f-142">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object maintains a clipping region that applies to all items drawn by that **Graphics** object.</span></span> <span data-ttu-id="a993f-143">Você pode definir a região de recorte chamando o método [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) .</span><span class="sxs-lookup"><span data-stu-id="a993f-143">You can set the clipping region by calling the [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) method.</span></span>

<span data-ttu-id="a993f-144">O exemplo a seguir cria uma região em forma de mais (+), formando a união de dois retângulos.</span><span class="sxs-lookup"><span data-stu-id="a993f-144">The following example creates a plus-shaped region by forming the union of two rectangles.</span></span> <span data-ttu-id="a993f-145">Essa região é designada como a região de recorte de um objeto de [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="a993f-145">That region is designated as the clipping region of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="a993f-146">Em seguida, o código desenha duas linhas restritas ao interior da área de recorte.</span><span class="sxs-lookup"><span data-stu-id="a993f-146">Then the code draws two lines that are restricted to the interior of the clipping region.</span></span>


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



<span data-ttu-id="a993f-147">A ilustração a seguir mostra as linhas recortadas.</span><span class="sxs-lookup"><span data-stu-id="a993f-147">The following illustration shows the clipped lines.</span></span>

![ilustração mostrando uma forma colorida cruzada por duas linhas diagonais em vermelho](images/graphicsascon2.png)

 

 
