---
description: Da mesma forma que blocos podem ser colocados lado a lado para recobrir um piso, imagens retangulares podem ser colocadas umas ao lado das outras para preencher (organizar lado a lado) uma forma.
ms.assetid: c92aa519-647a-4cd9-b88e-b79be0116d05
title: Colocação em um formato de forma lado a imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65c0b6e2ce39f5bf5c43b0352b8997202aa7e856
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090327"
---
# <a name="tiling-a-shape-with-an-image"></a><span data-ttu-id="38538-103">Colocação em um formato de forma lado a imagem</span><span class="sxs-lookup"><span data-stu-id="38538-103">Tiling a Shape with an Image</span></span>

<span data-ttu-id="38538-104">Da mesma forma que blocos podem ser colocados lado a lado para recobrir um piso, imagens retangulares podem ser colocadas umas ao lado das outras para preencher (organizar lado a lado) uma forma.</span><span class="sxs-lookup"><span data-stu-id="38538-104">Just as tiles can be placed next to each other to cover a floor, rectangular images can be placed next to each other to fill (tile) a shape.</span></span> <span data-ttu-id="38538-105">Para organizar o interior de uma forma lado a lado, use um pincel de textura.</span><span class="sxs-lookup"><span data-stu-id="38538-105">To tile the interior of a shape, use a texture brush.</span></span> <span data-ttu-id="38538-106">Quando você constrói um objeto [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) , um dos argumentos que você passa para o construtor é o endereço de um objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="38538-106">When you construct a [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) object, one of the arguments you pass to the constructor is the address of an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span> <span data-ttu-id="38538-107">Quando você usa o pincel de textura para pintar o interior de uma forma, ela será preenchida com repetidas cópias dessa imagem.</span><span class="sxs-lookup"><span data-stu-id="38538-107">When you use the texture brush to paint the interior of a shape, the shape is filled with repeated copies of this image.</span></span>

<span data-ttu-id="38538-108">A propriedade Wrap Mode do objeto [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) determina como a imagem é orientada à medida que é repetida em uma grade retangular.</span><span class="sxs-lookup"><span data-stu-id="38538-108">The wrap mode property of the [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) object determines how the image is oriented as it is repeated in a rectangular grid.</span></span> <span data-ttu-id="38538-109">Você pode fazer todos os blocos na grade terem a mesma orientação ou fazer com que a imagem fique invertida de uma posição de grade para a próxima.</span><span class="sxs-lookup"><span data-stu-id="38538-109">You can make all the tiles in the grid have the same orientation, or you can make the image flip from one grid position to the next.</span></span> <span data-ttu-id="38538-110">A inversão pode ser horizontal, vertical ou ambas.</span><span class="sxs-lookup"><span data-stu-id="38538-110">The flipping can be horizontal, vertical, or both.</span></span> <span data-ttu-id="38538-111">Os exemplos a seguir demonstram organização lado a lado com tipos diferentes de inversão.</span><span class="sxs-lookup"><span data-stu-id="38538-111">The following examples demonstrate tiling with different types of flipping.</span></span>

## <a name="tiling-an-image"></a><span data-ttu-id="38538-112">Divisão de uma imagem</span><span class="sxs-lookup"><span data-stu-id="38538-112">Tiling an Image</span></span>

<span data-ttu-id="38538-113">Este exemplo usa a seguinte imagem 75 × 75 para dividir um retângulo 200 × 200:</span><span class="sxs-lookup"><span data-stu-id="38538-113">This example uses the following 75 ×75 image to tile a 200 ×200 rectangle:</span></span>

![ilustração usada como a base de outras ilustrações neste tópico: uma casa e uma árvore em segundo plano e centralizadas em um retângulo](images/tile1.png)


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="38538-115">A ilustração a seguir mostra como o retângulo é organizado lado a lado com a imagem.</span><span class="sxs-lookup"><span data-stu-id="38538-115">The following illustration shows how the rectangle is tiled with the image.</span></span> <span data-ttu-id="38538-116">Observe que todos os blocos têm a mesma orientação; não há nenhum inversão.</span><span class="sxs-lookup"><span data-stu-id="38538-116">Note that all tiles have the same orientation; there is no flipping.</span></span>

![ilustração mostrando a imagem base repetida horizontal e verticalmente em um retângulo grande](images/tile2.png)

 

## <a name="flipping-an-image-horizontally-while-tiling"></a><span data-ttu-id="38538-118">Invertendo uma imagem horizontalmente durante a colocação em blocos</span><span class="sxs-lookup"><span data-stu-id="38538-118">Flipping an Image Horizontally While Tiling</span></span>

<span data-ttu-id="38538-119">Este exemplo usa uma imagem 75 × 75 para preencher um retângulo 200 × 200.</span><span class="sxs-lookup"><span data-stu-id="38538-119">This example uses a 75 ×75 image to fill a 200 ×200 rectangle.</span></span> <span data-ttu-id="38538-120">O modo de encapsulamento é definido para inverter a imagem horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="38538-120">The wrap mode is set to flip the image horizontally.</span></span>


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipX);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="38538-121">A ilustração a seguir mostra como o retângulo é organizado lado a lado com a imagem.</span><span class="sxs-lookup"><span data-stu-id="38538-121">The following illustration shows how the rectangle is tiled with the image.</span></span> <span data-ttu-id="38538-122">Observe que, ao mudar de um bloco para o próximo em uma determinada linha, a imagem é invertida horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="38538-122">Note that as you move from one tile to the next in a given row, the image is flipped horizontally.</span></span>

![ilustração mostrando a imagem base repetida horizontalmente, mas as instâncias com números iguais são revertidas horizontalmente](images/tile3.png)

 

## <a name="flipping-an-image-vertically-while-tiling"></a><span data-ttu-id="38538-124">Invertendo uma imagem verticalmente durante a colocação em blocos</span><span class="sxs-lookup"><span data-stu-id="38538-124">Flipping an Image Vertically While Tiling</span></span>

<span data-ttu-id="38538-125">Este exemplo usa uma imagem 75 × 75 para preencher um retângulo 200 × 200.</span><span class="sxs-lookup"><span data-stu-id="38538-125">This example uses a 75 ×75 image to fill a 200 ×200 rectangle.</span></span> <span data-ttu-id="38538-126">O modo de encapsulamento é definido para inverter a imagem verticalmente.</span><span class="sxs-lookup"><span data-stu-id="38538-126">The wrap mode is set to flip the image vertically.</span></span>


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="38538-127">A ilustração a seguir mostra como o retângulo é organizado lado a lado com a imagem.</span><span class="sxs-lookup"><span data-stu-id="38538-127">The following illustration shows how the rectangle is tiled with the image.</span></span> <span data-ttu-id="38538-128">Observe que, à medida que você passa de um bloco para o próximo em uma determinada coluna, a imagem é invertida verticalmente.</span><span class="sxs-lookup"><span data-stu-id="38538-128">Note that as you move from one tile to the next in a given column, the image is flipped vertically.</span></span>

![ilustração mostrando a imagem base repetida horizontal e verticalmente, mas linhas de números iguais são revertidas verticalmente](images/tile4.png)

 

## <a name="flipping-an-image-horizontally-and-vertically-while-tiling"></a><span data-ttu-id="38538-130">Invertendo uma imagem horizontal e verticalmente durante a colocação em divisão</span><span class="sxs-lookup"><span data-stu-id="38538-130">Flipping an Image Horizontally and Vertically While Tiling</span></span>

<span data-ttu-id="38538-131">Este exemplo usa uma imagem 75 × 75 para dividir um retângulo 200 × 200.</span><span class="sxs-lookup"><span data-stu-id="38538-131">This example uses a 75 ×75 image to tile a 200 ×200 rectangle.</span></span> <span data-ttu-id="38538-132">O modo de encapsulamento é definido para inverter a imagem tanto horizontalmente quanto verticalmente.</span><span class="sxs-lookup"><span data-stu-id="38538-132">The wrap mode is set to flip the image both horizontally and vertically.</span></span>


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipXY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="38538-133">A ilustração a seguir mostra como o retângulo é organizado lado a lado pela imagem.</span><span class="sxs-lookup"><span data-stu-id="38538-133">The following illustration shows how the rectangle is tiled by the image.</span></span> <span data-ttu-id="38538-134">Observe que, ao mudar de um bloco para o próximo em uma determinada linha, a imagem é invertida horizontalmente e, ao mudar de um bloco para o próximo em uma determinada coluna, a imagem é invertida verticalmente.</span><span class="sxs-lookup"><span data-stu-id="38538-134">Note that as you move from one tile to the next in a given row, the image is flipped horizontally, and as you move from one tile to the next in a given column, the image is flipped vertically.</span></span>

![a ilustração que mostra as instâncias alternadas da imagem base em cada linha é invertida horizontalmente e as linhas alternadas são invertidas verticalmente](images/tile5.png)

 

 



