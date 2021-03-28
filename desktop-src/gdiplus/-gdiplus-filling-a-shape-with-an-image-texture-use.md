---
description: Você pode preencher uma forma fechada com uma textura usando a classe Image e a classe TextureBrush.
ms.assetid: 12e1e132-a93f-4438-8a1d-9036a43a8fd8
title: Preenchendo uma forma com uma textura de imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3f1bf6ba04311310ab1985de1d1aaccd45db43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091467"
---
# <a name="filling-a-shape-with-an-image-texture"></a><span data-ttu-id="379fb-103">Preenchendo uma forma com uma textura de imagem</span><span class="sxs-lookup"><span data-stu-id="379fb-103">Filling a Shape with an Image Texture</span></span>

<span data-ttu-id="379fb-104">Você pode preencher uma forma fechada com uma textura usando a classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e a classe [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) .</span><span class="sxs-lookup"><span data-stu-id="379fb-104">You can fill a closed shape with a texture by using the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class and the [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) class.</span></span>

<span data-ttu-id="379fb-105">O exemplo a seguir preenche uma elipse com uma imagem.</span><span class="sxs-lookup"><span data-stu-id="379fb-105">The following example fills an ellipse with an image.</span></span> <span data-ttu-id="379fb-106">O código constrói um objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e, em seguida, passa o endereço desse objeto **Image** como um argumento para um construtor [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) .</span><span class="sxs-lookup"><span data-stu-id="379fb-106">The code constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object, and then passes the address of that **Image** object as an argument to a [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) constructor.</span></span> <span data-ttu-id="379fb-107">A terceira instrução de código dimensiona a imagem e a quarta instrução preenche a elipse com cópias repetidas da imagem dimensionada:</span><span class="sxs-lookup"><span data-stu-id="379fb-107">The third code statement scales the image, and the fourth statement fills the ellipse with repeated copies of the scaled image:</span></span>


```
Image image(L"ImageFile.jpg");
TextureBrush tBrush(&image);
stat = tBrush.SetTransform(&Matrix(75.0/640.0, 0.0f, 0.0f,
   75.0/480.0, 0.0f, 0.0f));
stat = graphics.FillEllipse(&tBrush,Rect(0, 150, 150, 250));
```



<span data-ttu-id="379fb-108">No exemplo de código anterior, o método [**TextureBrush:: SetTransform**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform) define a transformação que é aplicada à imagem antes de ser desenhada.</span><span class="sxs-lookup"><span data-stu-id="379fb-108">In the preceding code example, the [**TextureBrush::SetTransform**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform) method sets the transformation that is applied to the image before it is drawn.</span></span> <span data-ttu-id="379fb-109">Suponha que a imagem original possui uma largura de 640 pixels e uma altura de 480 pixels.</span><span class="sxs-lookup"><span data-stu-id="379fb-109">Assume that the original image has a width of 640 pixels and a height of 480 pixels.</span></span> <span data-ttu-id="379fb-110">A transformação reduz a imagem para 75 × 75, definindo os valores de dimensionamento horizontal e vertical.</span><span class="sxs-lookup"><span data-stu-id="379fb-110">The transform shrinks the image to 75 ×75, by setting the horizontal and vertical scaling values.</span></span>

> [!Note]  
> <span data-ttu-id="379fb-111">No exemplo anterior, o tamanho da imagem é 75 × 75 e o tamanho da elipse é 150 × 250.</span><span class="sxs-lookup"><span data-stu-id="379fb-111">In the preceding example, the image size is 75 ×75, and the ellipse size is 150 ×250.</span></span> <span data-ttu-id="379fb-112">Como a imagem é menor do que a elipse que ela está preenchendo, a elipse é organizada lado a lado com a imagem.</span><span class="sxs-lookup"><span data-stu-id="379fb-112">Because the image is smaller than the ellipse it is filling, the ellipse is tiled with the image.</span></span> <span data-ttu-id="379fb-113">Lado a lado significa que a imagem é repetida horizontal e verticalmente até o limite da forma ser atingido.</span><span class="sxs-lookup"><span data-stu-id="379fb-113">Tiling means that the image is repeated horizontally and vertically until the boundary of the shape is reached.</span></span> <span data-ttu-id="379fb-114">Para obter mais informações sobre a colocação em blocos, consulte [organizar uma forma em um formato com uma imagem](-gdiplus-tiling-a-shape-with-an-image-use.md).</span><span class="sxs-lookup"><span data-stu-id="379fb-114">For more information on tiling, see [Tiling a Shape with an Image](-gdiplus-tiling-a-shape-with-an-image-use.md).</span></span>

 

 

 



