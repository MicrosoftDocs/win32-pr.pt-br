---
description: O tópico usando uma matriz de cores para definir valores Alfa em imagens mostra um método não destrutivo para alterar os valores Alfa de uma imagem.
ms.assetid: 38c6254d-5191-4948-804a-1a4427aab7c6
title: Definindo os valores Alfa de pixels individuais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cd45bf32284ffc9a8cef13f368cff59e1e8a74f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501662"
---
# <a name="setting-the-alpha-values-of-individual-pixels"></a><span data-ttu-id="b7940-103">Definindo os valores Alfa de pixels individuais</span><span class="sxs-lookup"><span data-stu-id="b7940-103">Setting the Alpha Values of Individual Pixels</span></span>

<span data-ttu-id="b7940-104">O tópico [usando uma matriz de cores para definir valores Alfa em imagens](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md) mostra um método não destrutivo para alterar os valores Alfa de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="b7940-104">The topic [Using a Color Matrix to Set Alpha Values in Images](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md) shows a nondestructive method for changing the alpha values of an image.</span></span> <span data-ttu-id="b7940-105">O exemplo nesse tópico renderiza uma imagem semitransparentemente, mas os dados de pixel no bitmap não são alterados.</span><span class="sxs-lookup"><span data-stu-id="b7940-105">The example in that topic renders an image semitransparently, but the pixel data in the bitmap is not changed.</span></span> <span data-ttu-id="b7940-106">Os valores Alfa são alterados somente durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="b7940-106">The alpha values are altered only during rendering.</span></span>

<span data-ttu-id="b7940-107">O exemplo a seguir mostra como alterar os valores Alfa de pixels individuais.</span><span class="sxs-lookup"><span data-stu-id="b7940-107">The following example shows how to change the alpha values of individual pixels.</span></span> <span data-ttu-id="b7940-108">O código no exemplo realmente altera as informações alfa em um objeto [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) .</span><span class="sxs-lookup"><span data-stu-id="b7940-108">The code in the example actually changes the alpha information in a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="b7940-109">A abordagem é muito mais lenta do que usar uma matriz de cores e um objeto [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) , mas lhe dá controle sobre os pixels individuais no bitmap.</span><span class="sxs-lookup"><span data-stu-id="b7940-109">The approach is much slower than using a color matrix and an [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object but gives you control over the individual pixels in the bitmap.</span></span>


```
INT iWidth = bitmap.GetWidth();
INT iHeight = bitmap.GetHeight();
Color color, colorTemp;
for(INT iRow = 0; iRow < iHeight; iRow++)
{
   for(INT iColumn = 0; iColumn < iWidth; iColumn++)
   {
      bitmap.GetPixel(iColumn, iRow, &color);
      colorTemp.SetValue(color.MakeARGB(
         (BYTE)(255 * iColumn / iWidth), 
         color.GetRed(),
         color.GetGreen(),
         color.GetBlue()));
      bitmap.SetPixel(iColumn, iRow, colorTemp);
   }
}
// First draw a wide black line.
Pen pen(Color(255, 0, 0, 0), 25);
graphics.DrawLine(&pen, 10, 35, 200, 35);
// Now draw the modified bitmap.
graphics.DrawImage(&bitmap, 30, 0, iWidth, iHeight);
```



<span data-ttu-id="b7940-110">A ilustração a seguir mostra a imagem resultante.</span><span class="sxs-lookup"><span data-stu-id="b7940-110">The following illustration shows the resulting image.</span></span>

![ilustração mostrando uma imagem que fica mais opaca da esquerda para a direita, em um retângulo preto](images/image3.png)

<span data-ttu-id="b7940-112">O exemplo de código anterior usa loops aninhados para alterar o valor alfa de cada pixel no bitmap.</span><span class="sxs-lookup"><span data-stu-id="b7940-112">The preceding code example uses nested loops to change the alpha value of each pixel in the bitmap.</span></span> <span data-ttu-id="b7940-113">Para cada pixel, [**bitmap:: GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) Obtém a cor existente, [**Color:: SetValue**](/windows/desktop/api/Gdipluscolor/nf-gdipluscolor-color-setvalue) cria uma cor temporária que contém o novo valor alfa e, em seguida, [**bitmap:: SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) define a nova cor.</span><span class="sxs-lookup"><span data-stu-id="b7940-113">For each pixel, [**Bitmap::GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) gets the existing color, [**Color::SetValue**](/windows/desktop/api/Gdipluscolor/nf-gdipluscolor-color-setvalue) creates a temporary color that contains the new alpha value, and then [**Bitmap::SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) sets the new color.</span></span> <span data-ttu-id="b7940-114">O valor alfa é definido com base na coluna do bitmap.</span><span class="sxs-lookup"><span data-stu-id="b7940-114">The alpha value is set based on the column of the bitmap.</span></span> <span data-ttu-id="b7940-115">Na primeira coluna, alfa é definido como 0.</span><span class="sxs-lookup"><span data-stu-id="b7940-115">In the first column, alpha is set to 0.</span></span> <span data-ttu-id="b7940-116">Na última coluna, alfa é definido como 255.</span><span class="sxs-lookup"><span data-stu-id="b7940-116">In the last column, alpha is set to 255.</span></span> <span data-ttu-id="b7940-117">Portanto, a imagem resultante vai de totalmente transparente (na borda esquerda) para totalmente opaca (na borda direita).</span><span class="sxs-lookup"><span data-stu-id="b7940-117">So the resulting image goes from fully transparent (on the left edge) to fully opaque (on the right edge).</span></span>

<span data-ttu-id="b7940-118">[**Bitmap:: GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) e [**bitmap:: SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) lhe dão controle dos valores de pixel individuais.</span><span class="sxs-lookup"><span data-stu-id="b7940-118">[**Bitmap::GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) and [**Bitmap::SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) give you control of the individual pixel values.</span></span> <span data-ttu-id="b7940-119">No entanto, o uso de **bitmap:: GetPixel** e **bitmap:: SetPixel** não é tão rápido quanto usar a classe [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) e a estrutura [**ColorMatrix**](/windows/desktop/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) .</span><span class="sxs-lookup"><span data-stu-id="b7940-119">However, using **Bitmap::GetPixel** and **Bitmap::SetPixel** is not nearly as fast as using the [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) class and the [**ColorMatrix**](/windows/desktop/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) structure.</span></span>

 

 



