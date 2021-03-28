---
description: Uma transformação global é uma transformação que se aplica a todos os itens desenhados por um determinado objeto gráfico.
ms.assetid: 9f744c2a-f1f3-4a7e-ab0c-37aa1df01623
title: Transformações globais e locais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2682fef6a6236b9da7ec0ec1e5ab5484ad9f90d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563609"
---
# <a name="global-and-local-transformations"></a><span data-ttu-id="85d48-103">Transformações globais e locais</span><span class="sxs-lookup"><span data-stu-id="85d48-103">Global and Local Transformations</span></span>

<span data-ttu-id="85d48-104">Uma transformação global é uma transformação que se aplica a todos os itens desenhados por um determinado objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="85d48-104">A global transformation is a transformation that applies to every item drawn by a given [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="85d48-105">Para criar uma transformação global, construa um objeto **Graphics** e, em seguida, chame o método [**gráficos:: SetTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settransform) .</span><span class="sxs-lookup"><span data-stu-id="85d48-105">To create a global transformation, construct a **Graphics** object, and then call its [**Graphics::SetTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settransform) method.</span></span> <span data-ttu-id="85d48-106">O método **Graphics:: SetTransform** manipula um objeto [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) que está associado ao objeto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="85d48-106">The **Graphics::SetTransform** method manipulates a [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) object that is associated with the **Graphics** object.</span></span> <span data-ttu-id="85d48-107">A transformação armazenada nesse objeto de **matriz** é chamada de *transformação mundial*.</span><span class="sxs-lookup"><span data-stu-id="85d48-107">The transformation stored in that **Matrix** object is called the *world transformation*.</span></span> <span data-ttu-id="85d48-108">A transformação mundial pode ser uma simples transformação afim ou uma sequência complexa de transformações afim, mas independentemente de sua complexidade, a transformação mundial é armazenada em um único objeto **matriz** .</span><span class="sxs-lookup"><span data-stu-id="85d48-108">The world transformation can be a simple affine transformation or a complex sequence of affine transformations, but regardless of its complexity, the world transformation is stored in a single **Matrix** object.</span></span>

<span data-ttu-id="85d48-109">A classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornece vários métodos para criar uma transformação do mundo composto: [**gráficos:: MultiplyTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-multiplytransform), [**Graphics:: RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform), [**Graphics:: ScaleTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-scaletransform)e [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform).</span><span class="sxs-lookup"><span data-stu-id="85d48-109">The [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides several methods for building up a composite world transformation: [**Graphics::MultiplyTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-multiplytransform), [**Graphics::RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform), [**Graphics::ScaleTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-scaletransform), and [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform).</span></span> <span data-ttu-id="85d48-110">O exemplo a seguir desenha uma elipse duas vezes: uma vez antes de criar uma transformação global e outra vez depois.</span><span class="sxs-lookup"><span data-stu-id="85d48-110">The following example draws an ellipse twice: once before creating a world transformation and once after.</span></span> <span data-ttu-id="85d48-111">A transformação primeiro é dimensionada por um fator de 0,5 na direção y e, em seguida, move 50 unidades na direção x e gira 30 graus.</span><span class="sxs-lookup"><span data-stu-id="85d48-111">The transformation first scales by a factor of 0.5 in the y direction, then translates 50 units in the x direction, and then rotates 30 degrees.</span></span>


```
myGraphics.DrawEllipse(&myPen, 0, 0, 100, 50);
myGraphics.ScaleTransform(1.0f, 0.5f);
myGraphics.TranslateTransform(50.0f, 0.0f, MatrixOrderAppend);
myGraphics.RotateTransform(30.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myPen, 0, 0, 100, 50);
```



<span data-ttu-id="85d48-112">A ilustração a seguir mostra a elipse original e a elipse transformada.</span><span class="sxs-lookup"><span data-stu-id="85d48-112">The following illustration shows the original ellipse and the transformed ellipse.</span></span>

![captura de tela de uma janela que contém duas reticências sobrepostas; um é mais estreito e girado](images/aboutgdip05-art14.png)

> [!Note]  
> <span data-ttu-id="85d48-114">No exemplo anterior, a elipse é girada sobre a origem do sistema de coordenadas, que está no canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="85d48-114">In the previous example, the ellipse is rotated about the origin of the coordinate system, which is at the upper–left corner of the client area.</span></span> <span data-ttu-id="85d48-115">Isso produz um resultado diferente de girar a elipse sobre seu próprio centro.</span><span class="sxs-lookup"><span data-stu-id="85d48-115">This produces a different result than rotating the ellipse about its own center.</span></span>

 

<span data-ttu-id="85d48-116">Uma transformação local é uma transformação que se aplica a um item específico a ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="85d48-116">A local transformation is a transformation that applies to a specific item to be drawn.</span></span> <span data-ttu-id="85d48-117">Por exemplo, um objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) tem um método [**GraphicsPath:: Transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) que permite transformar os pontos de dados desse caminho.</span><span class="sxs-lookup"><span data-stu-id="85d48-117">For example, a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object has a [**GraphicsPath::Transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) method that allows you to transform the data points of that path.</span></span> <span data-ttu-id="85d48-118">O exemplo a seguir desenha um retângulo sem transformação e um caminho com uma transformação de rotação.</span><span class="sxs-lookup"><span data-stu-id="85d48-118">The following example draws a rectangle with no transformation and a path with a rotation transformation.</span></span> <span data-ttu-id="85d48-119">(Suponha que não haja nenhuma transformação global.)</span><span class="sxs-lookup"><span data-stu-id="85d48-119">(Assume that there is no world transformation.)</span></span>


```
 
Matrix myMatrix;
myMatrix.Rotate(45.0f);
myGraphicsPath.Transform(&myMatrix);
myGraphics.DrawRectangle(&myPen, 10, 10, 100, 50);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="85d48-120">Você pode combinar a transformação global com transformações locais para obter uma variedade de resultados.</span><span class="sxs-lookup"><span data-stu-id="85d48-120">You can combine the world transformation with local transformations to achieve a variety of results.</span></span> <span data-ttu-id="85d48-121">Por exemplo, você pode usar a transformação global para revisar o sistema de coordenadas e usar transformações locais para girar e dimensionar objetos desenhados no novo sistema de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="85d48-121">For example, you can use the world transformation to revise the coordinate system and use local transformations to rotate and scale objects drawn on the new coordinate system.</span></span>

<span data-ttu-id="85d48-122">Suponha que você deseje obter um sistema de coordenadas que tenha sua origem 200 pixels da borda esquerda da área de cliente e 150 pixels da parte superior da área de cliente.</span><span class="sxs-lookup"><span data-stu-id="85d48-122">Suppose you want a coordinate system that has its origin 200 pixels from the left edge of the client area and 150 pixels from the top of the client area.</span></span> <span data-ttu-id="85d48-123">Além disso, suponha que você deseje que a unidade de medida seja o pixel, com o eixo x apontando para a direita e o eixo y apontando para cima.</span><span class="sxs-lookup"><span data-stu-id="85d48-123">Furthermore, assume that you want the unit of measure to be the pixel, with the x-axis pointing to the right and the y-axis pointing up.</span></span> <span data-ttu-id="85d48-124">O sistema de coordenadas padrão tem o eixo y apontando para baixo, assim, você precisa executar uma reflexão no eixo horizontal.</span><span class="sxs-lookup"><span data-stu-id="85d48-124">The default coordinate system has the y-axis pointing down, so you need to perform a reflection across the horizontal axis.</span></span> <span data-ttu-id="85d48-125">A ilustração a seguir mostra a matriz de uma reflexão assim.</span><span class="sxs-lookup"><span data-stu-id="85d48-125">The following illustration shows the matrix of such a reflection.</span></span>

![ilustração mostrando uma matriz de três por três](images/aboutgdip05-art15.png)

<span data-ttu-id="85d48-127">Em seguida, suponha que você precisa executar uma translação de 200 unidades para a direita e 150 unidades para baixo.</span><span class="sxs-lookup"><span data-stu-id="85d48-127">Next, assume you need to perform a translation 200 units to the right and 150 units down.</span></span>

<span data-ttu-id="85d48-128">O exemplo a seguir estabelece o sistema de coordenadas que acabou de ser descrito definindo a transformação mundial de um objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="85d48-128">The following example establishes the coordinate system just described by setting the world transformation of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>


```
Matrix myMatrix(1.0f, 0.0f, 0.0f, -1.0f, 0.0f, 0.0f);
myGraphics.SetTransform(&myMatrix);
myGraphics.TranslateTransform(200.0f, 150.0f, MatrixOrderAppend);
```



<span data-ttu-id="85d48-129">O código a seguir (colocado após o código no exemplo anterior) cria um caminho que consiste em um único retângulo com seu canto inferior esquerdo na origem do novo sistema de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="85d48-129">The following code (placed after the code in the preceding example) creates a path that consists of a single rectangle with its lower-left corner at the origin of the new coordinate system.</span></span> <span data-ttu-id="85d48-130">O retângulo é preenchido uma vez sem transformação local e uma vez com transformação local.</span><span class="sxs-lookup"><span data-stu-id="85d48-130">The rectangle is filled once with no local transformation and once with a local transformation.</span></span> <span data-ttu-id="85d48-131">A transformação local consiste em uma colocação em escala horizontal por um fator de 2 seguida por uma rotação de 30 graus.</span><span class="sxs-lookup"><span data-stu-id="85d48-131">The local transformation consists of a horizontal scaling by a factor of 2 followed by a 30-degree rotation.</span></span>


```
// Create the path.
GraphicsPath myGraphicsPath;
Rect myRect(0, 0, 60, 60);
myGraphicsPath.AddRectangle(myRect);

// Fill the path on the new coordinate system.
// No local transformation
myGraphics.FillPath(&mySolidBrush1, &myGraphicsPath);

// Transform the path.
Matrix myPathMatrix;
myPathMatrix.Scale(2, 1);
myPathMatrix.Rotate(30, MatrixOrderAppend);
myGraphicsPath.Transform(&myPathMatrix);

// Fill the transformed path on the new coordinate system.
myGraphics.FillPath(&mySolidBrush2, &myGraphicsPath);
```



<span data-ttu-id="85d48-132">A ilustração a seguir mostra o novo sistema de coordenadas e os dois retângulos.</span><span class="sxs-lookup"><span data-stu-id="85d48-132">The following illustration shows the new coordinate system and the two rectangles.</span></span>

![captura de tela de um eixo x e y e um quadrado azul sobreposto por um rectagle semitransparente girado em volta do seu canto inferior esquerdo](images/aboutgdip05-art16.png)

 

 



