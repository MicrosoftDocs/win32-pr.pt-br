---
description: O estado de gráficos &\# 8212; região de recorte, transformações e configurações de qualidade &\# 8212; é armazenado em um objeto de gráfico.
ms.assetid: 98b9fa12-02e7-42bf-9cbd-03ee696188f6
title: Contêineres de elementos gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8bf6469d0835137be1bb76b7727fd961bba16b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551957"
---
# <a name="graphics-containers"></a><span data-ttu-id="314f2-103">Contêineres de elementos gráficos</span><span class="sxs-lookup"><span data-stu-id="314f2-103">Graphics Containers</span></span>

<span data-ttu-id="314f2-104">Estado de gráficos — região de recorte, transformações e configurações de qualidade — é armazenado em um objeto de [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="314f2-104">Graphics state — clipping region, transformations, and quality settings — is stored in a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="314f2-105">O Windows GDI+ permite que você substitua temporariamente ou aumente parte do estado em um objeto **gráfico** usando um contêiner.</span><span class="sxs-lookup"><span data-stu-id="314f2-105">Windows GDI+ allows you to temporarily replace or augment part of the state in a **Graphics** object by using a container.</span></span> <span data-ttu-id="314f2-106">Você inicia um contêiner chamando o método [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) de um objeto **Graphics** e encerra um contêiner chamando o método [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) .</span><span class="sxs-lookup"><span data-stu-id="314f2-106">You start a container by calling the [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) method of a **Graphics** object, and you end a container by calling the [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) method.</span></span> <span data-ttu-id="314f2-107">Entre os **elementos gráficos:: BeginContainer** e **Graphics:: EndContainer**, todas as alterações de estado feitas no objeto **gráfico** pertencem ao contêiner e não substituem o estado existente do objeto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="314f2-107">In between **Graphics::BeginContainer** and **Graphics::EndContainer**, any state changes you make to the **Graphics** object belong to the container and do not overwrite the existing state of the **Graphics** object.</span></span>

<span data-ttu-id="314f2-108">O exemplo a seguir cria um contêiner dentro de um objeto de [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="314f2-108">The following example creates a container within a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="314f2-109">A transformação mundial do objeto **gráfico** é uma tradução de 200 unidades à direita, e a transformação mundial do contêiner é uma tradução 100 unidades para baixo.</span><span class="sxs-lookup"><span data-stu-id="314f2-109">The world transformation of the **Graphics** object is a translation 200 units to the right, and the world transformation of the container is a translation 100 units down.</span></span>


```
myGraphics.TranslateTransform(200.0f, 0.0f);

myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.TranslateTransform(0.0f, 100.0f);
   myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
myGraphics.EndContainer(myGraphicsContainer);

myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
```



<span data-ttu-id="314f2-110">Observe que no exemplo anterior, a instrução `myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50)` feita entre as chamadas para [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) e [**gráficos:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) produz um retângulo diferente da mesma instrução feita após a chamada para **Graphics:: EndContainer**.</span><span class="sxs-lookup"><span data-stu-id="314f2-110">Note that in the previous example, the statement `myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50)` made in between the calls to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) and [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) produces a different rectangle than the same statement made after the call to **Graphics::EndContainer**.</span></span> <span data-ttu-id="314f2-111">Somente a tradução horizontal se aplica à chamada **DrawRectangle** feita fora do contêiner.</span><span class="sxs-lookup"><span data-stu-id="314f2-111">Only the horizontal translation applies to the **DrawRectangle** call made outside of the container.</span></span> <span data-ttu-id="314f2-112">Ambas as transformações — a tradução horizontal de 200 unidades e a tradução vertical de 100 unidades — aplicam-se à chamada [**Graphics::D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) feitas dentro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="314f2-112">Both transformations — the horizontal translation of 200 units and the vertical translation of 100 units — apply to the [**Graphics::DrawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) call made inside the container.</span></span> <span data-ttu-id="314f2-113">A ilustração a seguir mostra os dois retângulos.</span><span class="sxs-lookup"><span data-stu-id="314f2-113">The following illustration shows the two rectangles.</span></span>

![captura de tela de uma janela com dois retângulos desenhados com uma caneta azul, um posicionado acima do outro](images/aboutgdip05-art17.png)

<span data-ttu-id="314f2-115">Os contêineres podem ser aninhados em contêineres.</span><span class="sxs-lookup"><span data-stu-id="314f2-115">Containers can be nested within containers.</span></span> <span data-ttu-id="314f2-116">O exemplo a seguir cria um contêiner dentro de um objeto de [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e outro contêiner dentro do primeiro contêiner.</span><span class="sxs-lookup"><span data-stu-id="314f2-116">The following example creates a container within a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and another container within the first container.</span></span> <span data-ttu-id="314f2-117">A transformação mundial do objeto **gráfico** é uma tradução 100 unidades na direção x e 80 unidades na direção y.</span><span class="sxs-lookup"><span data-stu-id="314f2-117">The world transformation of the **Graphics** object is a translation 100 units in the x direction and 80 units in the y direction.</span></span> <span data-ttu-id="314f2-118">A transformação mundial do primeiro contêiner é uma rotação de 30 graus.</span><span class="sxs-lookup"><span data-stu-id="314f2-118">The world transformation of the first container is a 30-degree rotation.</span></span> <span data-ttu-id="314f2-119">A transformação mundial do segundo contêiner é um dimensionamento por um fator de 2 na direção x.</span><span class="sxs-lookup"><span data-stu-id="314f2-119">The world transformation of the second container is a scaling by a factor of 2 in the x direction.</span></span> <span data-ttu-id="314f2-120">Uma chamada para o método [**Graphics::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) é feita dentro do segundo contêiner.</span><span class="sxs-lookup"><span data-stu-id="314f2-120">A call to the [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) method is made inside the second container.</span></span>


```
myGraphics.TranslateTransform(100.0f, 80.0f, MatrixOrderAppend);

container1 = myGraphics.BeginContainer();
   myGraphics.RotateTransform(30.0f, MatrixOrderAppend);

   container2 = myGraphics.BeginContainer();
      myGraphics.ScaleTransform(2.0f, 1.0f);
      myGraphics.DrawEllipse(&myPen, -30, -20, 60, 40);
   myGraphics.EndContainer(container2);

myGraphics.EndContainer(container1);
```



<span data-ttu-id="314f2-121">A ilustração a seguir mostra a elipse.</span><span class="sxs-lookup"><span data-stu-id="314f2-121">The following illustration shows the ellipse.</span></span>

![captura de tela de uma janela que contém uma elipse azul girada com seu centro rotulado como (100, 80)](images/aboutgdip05-art18.png)

<span data-ttu-id="314f2-123">Observe que todas as três transformações se aplicam à chamada [**Graphics::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) feitas no segundo contêiner (interno).</span><span class="sxs-lookup"><span data-stu-id="314f2-123">Note that all three transformations apply to the [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) call made in the second (innermost) container.</span></span> <span data-ttu-id="314f2-124">Observe também a ordem das transformações: primeira escala, em seguida, girar e depois converter.</span><span class="sxs-lookup"><span data-stu-id="314f2-124">Also note the order of the transformations: first scale, then rotate, then translate.</span></span> <span data-ttu-id="314f2-125">A transformação mais interna é aplicada primeiro e a transformação externa é aplicada por último.</span><span class="sxs-lookup"><span data-stu-id="314f2-125">The innermost transformation is applied first, and the outermost transformation is applied last.</span></span>

<span data-ttu-id="314f2-126">Qualquer propriedade de um objeto de [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) pode ser definida dentro de um contêiner (entre chamadas para [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) e [**Graphics:: nocontainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)).</span><span class="sxs-lookup"><span data-stu-id="314f2-126">Any property of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object can be set inside a container (in between calls to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) and [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)).</span></span> <span data-ttu-id="314f2-127">Por exemplo, uma região de recorte pode ser definida dentro de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="314f2-127">For example, a clipping region can be set inside a container.</span></span> <span data-ttu-id="314f2-128">Qualquer desenho feito dentro do contêiner será restrito à região de recorte desse contêiner e também será restrito às regiões de recorte de todos os contêineres externos e à região de recorte do objeto **gráfico** em si.</span><span class="sxs-lookup"><span data-stu-id="314f2-128">Any drawing done inside the container will be restricted to the clipping region of that container and will also be restricted to the clipping regions of any outer containers and the clipping region of the **Graphics** object itself.</span></span>

<span data-ttu-id="314f2-129">As propriedades discutidas até agora – a transformação do mundo e a região de recorte — são combinadas por contêineres aninhados.</span><span class="sxs-lookup"><span data-stu-id="314f2-129">The properties discussed so far — the world transformation and the clipping region — are combined by nested containers.</span></span> <span data-ttu-id="314f2-130">Outras propriedades são temporariamente substituídas por um contêiner aninhado.</span><span class="sxs-lookup"><span data-stu-id="314f2-130">Other properties are temporarily replaced by a nested container.</span></span> <span data-ttu-id="314f2-131">Por exemplo, se você definir o modo de suavização como SmoothingModeAntiAlias dentro de um contêiner, os métodos de desenho chamados dentro desse contêiner usarão o modo de suavização de antialias, mas os métodos de desenho chamados após [**Graphics:: Nocontainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) usarão o modo de suavização que estava em vigor antes da chamada para [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).</span><span class="sxs-lookup"><span data-stu-id="314f2-131">For example, if you set the smoothing mode to SmoothingModeAntiAlias within a container, any drawing methods called inside that container will use the antialias smoothing mode, but drawing methods called after [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) will use the smoothing mode that was in place before the call to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).</span></span>

<span data-ttu-id="314f2-132">Para obter outro exemplo de como combinar as transformações mundiais de um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e um contêiner, suponha que você queira desenhar um olho e colocá-lo em vários locais em uma sequência de rostos.</span><span class="sxs-lookup"><span data-stu-id="314f2-132">For another example of combining the world transformations of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a container, suppose you want to draw an eye and place it at various locations on a sequence of faces.</span></span> <span data-ttu-id="314f2-133">O exemplo a seguir desenha um olho centralizado na origem do sistema de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="314f2-133">The following example draws an eye centered at the origin of the coordinate system.</span></span>


```
void DrawEye(Graphics* pGraphics)
{
   GraphicsContainer eyeContainer;
   
   eyeContainer = pGraphics->BeginContainer();

      Pen myBlackPen(Color(255, 0, 0, 0));
      SolidBrush myGreenBrush(Color(255, 0, 128, 0));
      SolidBrush myBlackBrush(Color(255, 0, 0, 0));

      GraphicsPath myTopPath;
      myTopPath.AddEllipse(-30, -50, 60, 60);

      GraphicsPath myBottomPath;
      myBottomPath.AddEllipse(-30, -10, 60, 60);

      Region myTopRegion(&myTopPath);
      Region myBottomRegion(&myBottomPath);

      // Draw the outline of the eye.
      // The outline of the eye consists of two ellipses.
      // The top ellipse is clipped by the bottom ellipse, and
      // the bottom ellipse is clipped by the top ellipse.
      pGraphics->SetClip(&myTopRegion);
      pGraphics->DrawPath(&myBlackPen, &myBottomPath);
      pGraphics->SetClip(&myBottomRegion);
      pGraphics->DrawPath(&myBlackPen, &myTopPath);

      // Fill the iris.
      // The iris is clipped by the bottom ellipse.
      pGraphics->FillEllipse(&myGreenBrush, -10, -15, 20, 22);

      // Fill the pupil.
      pGraphics->FillEllipse(&myBlackBrush, -3, -7, 6, 9);

   pGraphics->EndContainer(eyeContainer);
}
```



<span data-ttu-id="314f2-134">A ilustração a seguir mostra os eixos de olho e de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="314f2-134">The following illustration shows the eye and the coordinate axes.</span></span>

![ilustração mostrando um olho composto de três elipses: uma para a estrutura de tópicos, íris e Pupil](images/aboutgdip05-art19.png)

<span data-ttu-id="314f2-136">A função DrawEye, definida no exemplo anterior, recebe o endereço de um objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e cria imediatamente um contêiner dentro desse objeto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="314f2-136">The DrawEye function, defined in the previous example receives the address of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and immediately creates a container within that **Graphics** object.</span></span> <span data-ttu-id="314f2-137">Esse contêiner separa qualquer código que chame a função DrawEye das configurações de propriedade feitas durante a execução da função DrawEye.</span><span class="sxs-lookup"><span data-stu-id="314f2-137">This container insulates any code that calls the DrawEye function from property settings made during the execution of the DrawEye function.</span></span> <span data-ttu-id="314f2-138">Por exemplo, o código na função DrawEye define a região de recorte do objeto **Graphics** , mas quando DrawEye retorna o controle para a rotina de chamada, a região de recorte será como era antes da chamada para DrawEye.</span><span class="sxs-lookup"><span data-stu-id="314f2-138">For example, code in the DrawEye function sets the clipping region of the **Graphics** object, but when DrawEye returns control to the calling routine, the clipping region will be as it was before the call to DrawEye.</span></span>

<span data-ttu-id="314f2-139">O exemplo a seguir desenha três elipses (rostos), cada uma com um olho dentro.</span><span class="sxs-lookup"><span data-stu-id="314f2-139">The following example draws three ellipses (faces), each with an eye inside.</span></span>


```
// Draw an ellipse with center at (100, 100).
myGraphics.TranslateTransform(100.0f, 100.0f);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Draw the eye at the center of the ellipse.
DrawEye(&myGraphics);

// Draw an ellipse with center at 200, 100.
myGraphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Rotate the eye 40 degrees, and draw it 30 units above
// the center of the ellipse.
myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.RotateTransform(-40.0f);
   myGraphics.TranslateTransform(0.0f, -30.0f, MatrixOrderAppend);
   DrawEye(&myGraphics);
myGraphics.EndContainer(myGraphicsContainer);

// Draw a ellipse with center at (300.0f, 100.0f).
myGraphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Stretch and rotate the eye, and draw it at the 
// center of the ellipse.
myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.ScaleTransform(2.0f, 1.5f);
   myGraphics.RotateTransform(45.0f, MatrixOrderAppend);
   DrawEye(&myGraphics);
myGraphics.EndContainer(myGraphicsContainer);
```



<span data-ttu-id="314f2-140">A ilustração a seguir mostra as três reticências.</span><span class="sxs-lookup"><span data-stu-id="314f2-140">The following illustration shows the three ellipses.</span></span>

![captura de tela de uma janela com três elipses, cada uma delas contendo um olho em um tamanho e uma rotação diferentes](images/aboutgdip05-art20.png)

<span data-ttu-id="314f2-142">No exemplo anterior, todas as reticências são desenhadas com a chamada `DrawEllipse(&myBlackPen, -40, -60, 80, 120)` , que desenha uma elipse centralizada na origem do sistema de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="314f2-142">In the previous example, all ellipses are drawn with the call `DrawEllipse(&myBlackPen, -40, -60, 80, 120)`, which draws an ellipse centered at the origin of the coordinate system.</span></span> <span data-ttu-id="314f2-143">As reticências são movidas para fora do canto superior esquerdo da área do cliente, definindo a transformação mundial do objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="314f2-143">The ellipses are moved away from the upper-left corner of the client area by setting the world transformation of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="314f2-144">A instrução faz com que a primeira elipse seja centralizada em (100, 100).</span><span class="sxs-lookup"><span data-stu-id="314f2-144">The statement causes the first ellipse to be centered at (100, 100).</span></span> <span data-ttu-id="314f2-145">A instrução faz com que o centro da segunda elipse seja de 100 unidades à direita do centro da primeira elipse.</span><span class="sxs-lookup"><span data-stu-id="314f2-145">The statement causes the center of the second ellipse to be 100 units to the right of the center of the first ellipse.</span></span> <span data-ttu-id="314f2-146">Da mesma forma, o centro da terceira elipse é de 100 unidades à direita do centro da segunda elipse.</span><span class="sxs-lookup"><span data-stu-id="314f2-146">Likewise, the center of the third ellipse is 100 units to the right of the center of the second ellipse.</span></span>

<span data-ttu-id="314f2-147">Os contêineres no exemplo anterior são usados para transformar o olho em relação ao centro de uma determinada elipse.</span><span class="sxs-lookup"><span data-stu-id="314f2-147">The containers in the previous example are used to transform the eye relative to the center of a given ellipse.</span></span> <span data-ttu-id="314f2-148">O primeiro olho é desenhado no centro da elipse sem transformação, portanto, a chamada DrawEye não está dentro de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="314f2-148">The first eye is drawn at the center of the ellipse with no transformation, so the DrawEye call is not inside a container.</span></span> <span data-ttu-id="314f2-149">O segundo olho é girado em 40 graus e desenhado em 30 unidades acima do centro da elipse, portanto, a função DrawEye e os métodos que definem a transformação são chamados dentro de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="314f2-149">The second eye is rotated 40 degrees and drawn 30 units above the center of the ellipse, so the DrawEye function and the methods that set the transformation are called inside a container.</span></span> <span data-ttu-id="314f2-150">O terceiro olho é alongado e girado e desenhado no centro da elipse.</span><span class="sxs-lookup"><span data-stu-id="314f2-150">The third eye is stretched and rotated and drawn at the center of the ellipse.</span></span> <span data-ttu-id="314f2-151">Como no segundo olho, a função DrawEye e os métodos que definem a transformação são chamados dentro de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="314f2-151">As with the second eye, the DrawEye function and the methods that set the transformation are called inside a container.</span></span>

 

 
