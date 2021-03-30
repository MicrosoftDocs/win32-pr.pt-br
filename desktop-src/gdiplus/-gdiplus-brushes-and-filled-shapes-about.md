---
description: Uma figura fechada, como um retângulo ou uma elipse, consiste em uma estrutura de tópicos e um interior.
ms.assetid: 889558d5-9181-43ff-b862-e92966324208
title: Pincéis e formas preenchidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eb772be88ce26325337fd9c88fc0319631895e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555652"
---
# <a name="brushes-and-filled-shapes"></a><span data-ttu-id="9eab5-103">Pincéis e formas preenchidas</span><span class="sxs-lookup"><span data-stu-id="9eab5-103">Brushes and Filled Shapes</span></span>

<span data-ttu-id="9eab5-104">Uma figura fechada, como um retângulo ou uma elipse, consiste em uma estrutura de tópicos e um interior.</span><span class="sxs-lookup"><span data-stu-id="9eab5-104">A closed figure such as a rectangle or an ellipse consists of an outline and an interior.</span></span> <span data-ttu-id="9eab5-105">A estrutura de tópicos é desenhada com um objeto de [**caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) e o interior é preenchido com um objeto de [**pincel**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="9eab5-105">The outline is drawn with a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object and the interior is filled with a [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span> <span data-ttu-id="9eab5-106">O Windows GDI+ fornece várias classes de pincel para preencher os interiores de figuras fechadas: [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)e [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush).</span><span class="sxs-lookup"><span data-stu-id="9eab5-106">Windows GDI+ provides several brush classes for filling the interiors of closed figures: [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush), and [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush).</span></span> <span data-ttu-id="9eab5-107">Todas essas classes herdam da classe **Brush** .</span><span class="sxs-lookup"><span data-stu-id="9eab5-107">All these classes inherit from the **Brush** class.</span></span> <span data-ttu-id="9eab5-108">A ilustração a seguir mostra um retângulo preenchido com um pincel sólido e uma elipse preenchida com um pincel de hachura.</span><span class="sxs-lookup"><span data-stu-id="9eab5-108">The following illustration shows a rectangle filled with a solid brush and an ellipse filled with a hatch brush.</span></span>

![ilustração mostrando um retângulo azul e uma elipse magenta preenchida com um padrão de hachura azul](images/aboutgdip02-art17.png)

 

-   [<span data-ttu-id="9eab5-110">Pincéis Sólidos</span><span class="sxs-lookup"><span data-stu-id="9eab5-110">Solid Brushes</span></span>](#solid-brushes)
-   [<span data-ttu-id="9eab5-111">Pincéis de Hachura</span><span class="sxs-lookup"><span data-stu-id="9eab5-111">Hatch Brushes</span></span>](#hatch-brushes)
-   [<span data-ttu-id="9eab5-112">Pincéis de Textura</span><span class="sxs-lookup"><span data-stu-id="9eab5-112">Texture Brushes</span></span>](#texture-brushes)
-   [<span data-ttu-id="9eab5-113">Pincéis de Gradiente</span><span class="sxs-lookup"><span data-stu-id="9eab5-113">Gradient Brushes</span></span>](#gradient-brushes)

## <a name="solid-brushes"></a><span data-ttu-id="9eab5-114">Pincéis Sólidos</span><span class="sxs-lookup"><span data-stu-id="9eab5-114">Solid Brushes</span></span>

<span data-ttu-id="9eab5-115">Para preencher uma forma fechada, você precisa de um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e um objeto de [**pincel**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="9eab5-115">To fill a closed shape, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span> <span data-ttu-id="9eab5-116">O objeto **Graphics** fornece métodos, como [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) e [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inconstrectf_)), e o objeto **Brush** armazena os atributos do preenchimento, como Color e Pattern.</span><span class="sxs-lookup"><span data-stu-id="9eab5-116">The **Graphics** object provides methods, such as [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) and [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inconstrectf_)), and the **Brush** object stores attributes of the fill, such as color and pattern.</span></span> <span data-ttu-id="9eab5-117">O endereço do objeto **Brush** é passado como um dos argumentos para o método Fill.</span><span class="sxs-lookup"><span data-stu-id="9eab5-117">The address of the **Brush** object is passed as one of the arguments to the fill method.</span></span> <span data-ttu-id="9eab5-118">O exemplo a seguir preenche uma elipse com uma cor vermelha sólida.</span><span class="sxs-lookup"><span data-stu-id="9eab5-118">The following example fills an ellipse with a solid red color.</span></span>


```
SolidBrush mySolidBrush(Color(255, 255, 0, 0));
myGraphics.FillEllipse(&mySolidBrush, 0, 0, 60, 40);
```



<span data-ttu-id="9eab5-119">Observe que, no exemplo anterior, o pincel é do tipo [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), que é herdado de [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush).</span><span class="sxs-lookup"><span data-stu-id="9eab5-119">Note that in the preceding example, the brush is of type [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), which inherits from [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush).</span></span>

## <a name="hatch-brushes"></a><span data-ttu-id="9eab5-120">Pincéis de Hachura</span><span class="sxs-lookup"><span data-stu-id="9eab5-120">Hatch Brushes</span></span>

<span data-ttu-id="9eab5-121">Ao preencher uma forma com um pincel de hachura, é necessário especificar uma cor de primeiro plano, uma cor da tela de fundo e um estilo de hachura.</span><span class="sxs-lookup"><span data-stu-id="9eab5-121">When you fill a shape with a hatch brush, you specify a foreground color, a background color, and a hatch style.</span></span> <span data-ttu-id="9eab5-122">A cor de primeiro plano é a cor da hachura.</span><span class="sxs-lookup"><span data-stu-id="9eab5-122">The foreground color is the color of the hatching.</span></span>


```
HatchBrush myHatchBrush(
   HatchStyleVertical, 
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0));
```



<span data-ttu-id="9eab5-123">O GDI+ fornece mais de 50 estilos de hachura, especificados em [**HatchStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-hatchstyle).</span><span class="sxs-lookup"><span data-stu-id="9eab5-123">GDI+ provides more than 50 hatch styles, specified in [**HatchStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-hatchstyle).</span></span> <span data-ttu-id="9eab5-124">Os três estilos mostrados na ilustração a seguir são horizontal, ForwardDiagonal e Cross.</span><span class="sxs-lookup"><span data-stu-id="9eab5-124">The three styles shown in the following illustration are Horizontal, ForwardDiagonal, and Cross.</span></span>

![ilustração mostrando três elipses com cor azul, cada uma com um estilo de hachura diferente](images/aboutgdip02-art18.png)

 

## <a name="texture-brushes"></a><span data-ttu-id="9eab5-126">Pincéis de Textura</span><span class="sxs-lookup"><span data-stu-id="9eab5-126">Texture Brushes</span></span>

<span data-ttu-id="9eab5-127">Com um pincel de textura, é possível preencher uma forma com um padrão armazenado em um bitmap.</span><span class="sxs-lookup"><span data-stu-id="9eab5-127">With a texture brush, you can fill a shape with a pattern stored in a bitmap.</span></span> <span data-ttu-id="9eab5-128">Por exemplo, suponha que a imagem a seguir seja armazenada em um arquivo de disco chamado MyTexture.bmp.</span><span class="sxs-lookup"><span data-stu-id="9eab5-128">For example, suppose the following picture is stored in a disk file named MyTexture.bmp.</span></span>

![captura de tela de um quadrado pequeno preenchido com várias cores](images/aboutgdip02-art19.png)

<span data-ttu-id="9eab5-130">O exemplo a seguir preenche uma elipse repetindo a imagem armazenada em MyTexture.bmp.</span><span class="sxs-lookup"><span data-stu-id="9eab5-130">The following example fills an ellipse by repeating the picture stored in MyTexture.bmp.</span></span>


```
Image myImage(L"MyTexture.bmp");
TextureBrush myTextureBrush(&myImage);
myGraphics.FillEllipse(&myTextureBrush, 0, 0, 100, 50);
```



<span data-ttu-id="9eab5-131">A ilustração a seguir mostra a elipse preenchida.</span><span class="sxs-lookup"><span data-stu-id="9eab5-131">The following illustration shows the filled ellipse.</span></span>

![ilustração mostrando uma elipse preenchida com o padrão definido anteriormente](images/aboutgdip02-art20.png)

 

## <a name="gradient-brushes"></a><span data-ttu-id="9eab5-133">Pincéis de Gradiente</span><span class="sxs-lookup"><span data-stu-id="9eab5-133">Gradient Brushes</span></span>

<span data-ttu-id="9eab5-134">Você pode usar um pincel de gradiente para preencher uma forma com uma cor que muda gradualmente de uma parte da forma para outra.</span><span class="sxs-lookup"><span data-stu-id="9eab5-134">You can use a gradient brush to fill a shape with a color that changes gradually from one part of the shape to another.</span></span> <span data-ttu-id="9eab5-135">Por exemplo, um pincel de gradiente horizontal mudará a cor à medida que você mover do lado esquerdo de uma figura para o lado direito.</span><span class="sxs-lookup"><span data-stu-id="9eab5-135">For example, a horizontal gradient brush will change color as you move from the left side of a figure to the right side.</span></span> <span data-ttu-id="9eab5-136">O exemplo a seguir preenche uma elipse com um pincel de gradiente horizontal que muda de azul para verde à medida que você move do lado esquerdo da elipse para o lado direito.</span><span class="sxs-lookup"><span data-stu-id="9eab5-136">The following example fills an ellipse with a horizontal gradient brush that changes from blue to green as you move from the left side of the ellipse to the right side.</span></span>


```
LinearGradientBrush myLinearGradientBrush(
   myRect,
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0),
   LinearGradientModeHorizontal);
myGraphics.FillEllipse(&myLinearGradientBrush, myRect); 
```



<span data-ttu-id="9eab5-137">A ilustração a seguir mostra a elipse preenchida.</span><span class="sxs-lookup"><span data-stu-id="9eab5-137">The following illustration shows the filled ellipse.</span></span>

![ilustração mostrando uma elipse com preenchimento gradual: azul à direita para verde à esquerda](images/aboutgdip02-art21.png)

<span data-ttu-id="9eab5-139">Um pincel de gradiente de caminho pode ser configurado para alterar a cor à medida que você passa do centro de uma figura para o limite.</span><span class="sxs-lookup"><span data-stu-id="9eab5-139">A path gradient brush can be configured to change color as you move from the center of a figure toward the boundary.</span></span>

![ilustration de uma elipse que é azul escuro no centro, sombreamento para azul claro na borda](images/aboutgdip02-art22.png)

<span data-ttu-id="9eab5-141">Pincéis de gradiente de caminho são bastante flexíveis.</span><span class="sxs-lookup"><span data-stu-id="9eab5-141">Path gradient brushes are quite flexible.</span></span> <span data-ttu-id="9eab5-142">O pincel de gradiente usado para preencher o triângulo nas seguintes ilustrações altera gradualmente de vermelho no centro para cada uma das três cores diferentes nos vértices.</span><span class="sxs-lookup"><span data-stu-id="9eab5-142">The gradient brush used to fill the triangle in the following illustration changes gradually from red at the center to each of three different colors at the vertices.</span></span>

![ilustração de um triângulo que é vermelho no centro, sombreamento para uma cor diferente em cada vértice](images/aboutgdip02-art23.png)

 

 



