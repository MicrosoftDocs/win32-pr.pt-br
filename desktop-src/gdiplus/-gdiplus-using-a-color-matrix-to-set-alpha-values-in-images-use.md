---
description: A classe de bitmap (que herda da classe Image) e a classe ImageAttributes fornecem funcionalidade para obter e definir valores de pixel.
ms.assetid: e3d67431-6098-4b2a-8910-5695a8473216
title: Uso de uma matriz de cores para definir valores alfa em imagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81180b1f09b11e37b322e37106dab1879a00bbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501658"
---
# <a name="using-a-color-matrix-to-set-alpha-values-in-images"></a><span data-ttu-id="0eda8-103">Uso de uma matriz de cores para definir valores alfa em imagens</span><span class="sxs-lookup"><span data-stu-id="0eda8-103">Using a Color Matrix to Set Alpha Values in Images</span></span>

<span data-ttu-id="0eda8-104">A classe de [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) (que herda da classe [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) ) e a classe [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) fornecem funcionalidade para obter e definir valores de pixel.</span><span class="sxs-lookup"><span data-stu-id="0eda8-104">The [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class (which inherits from the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class) and the [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) class provide functionality for getting and setting pixel values.</span></span> <span data-ttu-id="0eda8-105">Você pode usar a classe **ImageAttributes** para modificar os valores Alfa de uma imagem inteira ou pode chamar o método [**bitmap:: SetPixel**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) da classe **bitmap** para modificar valores de pixel individuais.</span><span class="sxs-lookup"><span data-stu-id="0eda8-105">You can use the **ImageAttributes** class to modify the alpha values for an entire image, or you can call the [**Bitmap::SetPixel**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) method of the **Bitmap** class to modify individual pixel values.</span></span> <span data-ttu-id="0eda8-106">Para obter mais informações sobre como definir valores de pixel individuais, consulte [definindo os valores Alfa de pixels individuais](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md).</span><span class="sxs-lookup"><span data-stu-id="0eda8-106">For more information on setting individual pixel values, see [Setting the Alpha Values of Individual Pixels](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md).</span></span>

<span data-ttu-id="0eda8-107">O exemplo a seguir desenha uma linha preta larga e, em seguida, exibe uma imagem opaca que cobre parte dessa linha.</span><span class="sxs-lookup"><span data-stu-id="0eda8-107">The following example draws a wide black line and then displays an opaque image that covers part of that line.</span></span>


```
Bitmap bitmap(L"Texture1.jpg");
Pen pen(Color(255, 0, 0, 0), 25);
// First draw a wide black line.
graphics.DrawLine(&pen, Point(10, 35), Point(200, 35));
// Now draw an image that covers part of the black line.
graphics.DrawImage(&bitmap,
   Rect(30, 0, bitmap.GetWidth(), bitmap.GetHeight()));
```



<span data-ttu-id="0eda8-108">A ilustração a seguir mostra a imagem resultante, que é desenhada em (30, 0).</span><span class="sxs-lookup"><span data-stu-id="0eda8-108">The following illustration shows the resulting image, which is drawn at (30, 0).</span></span> <span data-ttu-id="0eda8-109">Observe que a linha preta larga não é mostrada por meio da imagem.</span><span class="sxs-lookup"><span data-stu-id="0eda8-109">Note that the wide black line doesn't show through the image.</span></span>

![ilustração mostrando uma imagem opaca sobrepondo um retângulo preto fino e largo](images/image1.png)

<span data-ttu-id="0eda8-111">A classe [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) tem muitas propriedades que você pode usar para modificar imagens durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="0eda8-111">The [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) class has many properties that you can use to modify images during rendering.</span></span> <span data-ttu-id="0eda8-112">No exemplo a seguir, um objeto **ImageAttributes** é usado para definir todos os valores alfa como 80% do que eles eram.</span><span class="sxs-lookup"><span data-stu-id="0eda8-112">In the following example, an **ImageAttributes** object is used to set all the alpha values to 80 percent of what they were.</span></span> <span data-ttu-id="0eda8-113">Isso é feito inicializando uma matriz de cores e configurando o valor de escala alfa na matriz para 0,8.</span><span class="sxs-lookup"><span data-stu-id="0eda8-113">This is done by initializing a color matrix and setting the alpha scaling value in the matrix to 0.8.</span></span> <span data-ttu-id="0eda8-114">O endereço da matriz de cores é passado para o método [**ImageAttributes:: SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) do objeto **ImageAttributes** , e o endereço do objeto **ImageAttributes** é passado para o método [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) de um objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="0eda8-114">The address of the color matrix is passed to the [**ImageAttributes::SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) method of the **ImageAttributes** object, and the address of the **ImageAttributes** object is passed to the [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) method of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>


```
// Create a Bitmap object and load it with the texture image.
Bitmap bitmap(L"Texture1.jpg");
Pen pen(Color(255, 0, 0, 0), 25);
// Initialize the color matrix.
// Notice the value 0.8 in row 4, column 4.
ColorMatrix colorMatrix = {1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
                           0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
                           0.0f, 0.0f, 1.0f, 0.0f, 0.0f,
                           0.0f, 0.0f, 0.0f, 0.8f, 0.0f,
                           0.0f, 0.0f, 0.0f, 0.0f, 1.0f};
// Create an ImageAttributes object and set its color matrix.
ImageAttributes imageAtt;
imageAtt.SetColorMatrix(&colorMatrix, ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
// First draw a wide black line.
graphics.DrawLine(&pen, Point(10, 35), Point(200, 35));
// Now draw the semitransparent bitmap image.
INT iWidth = bitmap.GetWidth();
INT iHeight = bitmap.GetHeight();
graphics.DrawImage(
   &bitmap, 
   Rect(30, 0, iWidth, iHeight),  // Destination rectangle
   0,                             // Source rectangle X 
   0,                             // Source rectangle Y
   iWidth,                        // Source rectangle width
   iHeight,                       // Source rectangle height
   UnitPixel, 
   &imageAtt);
```



<span data-ttu-id="0eda8-115">Durante o processamento, os valores alfa no bitmap são convertidos em 80 por cento do que eram.</span><span class="sxs-lookup"><span data-stu-id="0eda8-115">During rendering, the alpha values in the bitmap are converted to 80 percent of what they were.</span></span> <span data-ttu-id="0eda8-116">Isso resulta em uma imagem que é combinada com a tela de fundo.</span><span class="sxs-lookup"><span data-stu-id="0eda8-116">This results in an image that is blended with the background.</span></span> <span data-ttu-id="0eda8-117">Como mostra a ilustração a seguir, a imagem de bitmap é transparente; é possível ver a linha preta sólida através dela.</span><span class="sxs-lookup"><span data-stu-id="0eda8-117">As the following illustration shows, the bitmap image looks transparent; you can see the solid black line through it.</span></span>

![ilustração semelhante à anterior, mas a imagem é sem transparência](images/image2.png)

<span data-ttu-id="0eda8-119">Nos pontos em que a imagem está sobre a parte branca da tela de fundo, ela é combinada com a cor branca.</span><span class="sxs-lookup"><span data-stu-id="0eda8-119">Where the image is over the white portion of the background, the image has been blended with the color white.</span></span> <span data-ttu-id="0eda8-120">Nos pontos em que imagem cruza a linha preta, ela é combinada a cor preta.</span><span class="sxs-lookup"><span data-stu-id="0eda8-120">Where the image crosses the black line, the image is blended with the color black.</span></span>

 

 



