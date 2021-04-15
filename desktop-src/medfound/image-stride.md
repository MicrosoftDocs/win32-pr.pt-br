---
description: Stride da imagem
ms.assetid: 13cd1106-48b3-4522-ac09-8efbaab5c31d
title: Stride da imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 813c0f3d99297758761bdfb5973fc2b16e3339f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104561425"
---
# <a name="image-stride"></a><span data-ttu-id="35a84-103">Stride da imagem</span><span class="sxs-lookup"><span data-stu-id="35a84-103">Image Stride</span></span>

<span data-ttu-id="35a84-104">Quando uma imagem de vídeo é armazenada na memória, o buffer de memória pode conter bytes de preenchimento extras após cada linha de pixels.</span><span class="sxs-lookup"><span data-stu-id="35a84-104">When a video image is stored in memory, the memory buffer might contain extra padding bytes after each row of pixels.</span></span> <span data-ttu-id="35a84-105">Os bytes de preenchimento afetam a forma como a imagem é armazenada na memória, mas não afetam o modo como a imagem é exibida.</span><span class="sxs-lookup"><span data-stu-id="35a84-105">The padding bytes affect how the image is stored in memory, but do not affect how the image is displayed.</span></span>

<span data-ttu-id="35a84-106">O *Stride* é o número de bytes de uma linha de pixels na memória até a próxima linha de pixels na memória.</span><span class="sxs-lookup"><span data-stu-id="35a84-106">The *stride* is the number of bytes from one row of pixels in memory to the next row of pixels in memory.</span></span> <span data-ttu-id="35a84-107">O stride também é chamado de *pitch*.</span><span class="sxs-lookup"><span data-stu-id="35a84-107">Stride is also called *pitch*.</span></span> <span data-ttu-id="35a84-108">Se os bytes de preenchimento estiverem presentes, o stride será mais largo do que a largura da imagem, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="35a84-108">If padding bytes are present, the stride is wider than the width of the image, as shown in the following illustration.</span></span>

![diagrama mostrando uma imagem e preenchimento.](images/c85c6a40-f0a8-48a3-b465-39ceada66339.gif)

<span data-ttu-id="35a84-110">Dois buffers que contêm quadros de vídeo com dimensões iguais podem ter dois passos diferentes.</span><span class="sxs-lookup"><span data-stu-id="35a84-110">Two buffers that contain video frames with equal dimensions can have two different strides.</span></span> <span data-ttu-id="35a84-111">Se você processar uma imagem de vídeo, deverá levar em conta o Stride.</span><span class="sxs-lookup"><span data-stu-id="35a84-111">If you process a video image, you must take the stride into account.</span></span>

<span data-ttu-id="35a84-112">Além disso, há duas maneiras pelas quais uma imagem pode ser organizada na memória.</span><span class="sxs-lookup"><span data-stu-id="35a84-112">In addition, there are two ways that an image can be arranged in memory.</span></span> <span data-ttu-id="35a84-113">Em uma imagem de *cima para baixo* , a linha superior de pixels na imagem aparece primeiro na memória.</span><span class="sxs-lookup"><span data-stu-id="35a84-113">In a *top-down* image, the top row of pixels in the image appears first in memory.</span></span> <span data-ttu-id="35a84-114">Em uma imagem de *baixo* , a última linha de pixels aparece primeiro na memória.</span><span class="sxs-lookup"><span data-stu-id="35a84-114">In a *bottom-up* image, the last row of pixels appears first in memory.</span></span> <span data-ttu-id="35a84-115">A ilustração a seguir mostra a diferença entre uma imagem de cima para baixo e uma imagem de baixo para cima.</span><span class="sxs-lookup"><span data-stu-id="35a84-115">The following illustration shows the difference between a top-down image and a bottom-up image.</span></span>

![diagrama mostrando imagens de cima para baixo e de baixo para cima.](images/f03bd9ff-0cf3-4a56-88c5-5b8c44637272.gif)

<span data-ttu-id="35a84-117">Uma imagem inferior tem um stride negativo, porque o stride é definido como o número de bytes que precisam ser movidos para baixo em uma linha de pixels, em relação à imagem exibida.</span><span class="sxs-lookup"><span data-stu-id="35a84-117">A bottom-up image has a negative stride, because stride is defined as the number of bytes need to move down a row of pixels, relative to the displayed image.</span></span> <span data-ttu-id="35a84-118">As imagens YUV devem ser sempre de cima para baixo e qualquer imagem contida em uma superfície do Direct3D deve ser de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="35a84-118">YUV images should always be top-down, and any image that is contained in a Direct3D surface must be top-down.</span></span> <span data-ttu-id="35a84-119">As imagens RGB na memória do sistema geralmente são de baixo para cima.</span><span class="sxs-lookup"><span data-stu-id="35a84-119">RGB images in system memory are usually bottom-up.</span></span>

<span data-ttu-id="35a84-120">As transformações de vídeo, em particular, precisam lidar com os buffers com progressos incompatíveis, pois o buffer de entrada pode não corresponder ao buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="35a84-120">Video transforms in particular need to handle buffers with mismatched strides, because the input buffer might not match the output buffer.</span></span> <span data-ttu-id="35a84-121">Por exemplo, suponha que você deseja converter uma imagem de origem e gravar o resultado em uma imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="35a84-121">For example, suppose that you want to convert a source image and write the result to a destination image.</span></span> <span data-ttu-id="35a84-122">Suponha que ambas as imagens tenham a mesma largura e altura, mas que podem não ter o mesmo formato de pixel ou o mesmo Stride de imagem.</span><span class="sxs-lookup"><span data-stu-id="35a84-122">Assume that both images have the same width and height, but might not have the same pixel format or the same image stride.</span></span>

<span data-ttu-id="35a84-123">O código de exemplo a seguir mostra uma abordagem generalizada para gravar esse tipo de função.</span><span class="sxs-lookup"><span data-stu-id="35a84-123">The following example code shows a generalized approach for writing this kind of function.</span></span> <span data-ttu-id="35a84-124">Esse não é um exemplo funcional completo, pois abstrai muitos dos detalhes específicos.</span><span class="sxs-lookup"><span data-stu-id="35a84-124">This is not a complete working example, because it abstracts many of the specific details.</span></span>


```C++
void ProcessVideoImage(
    BYTE*       pDestScanLine0,     
    LONG        lDestStride,        
    const BYTE* pSrcScanLine0,      
    LONG        lSrcStride,         
    DWORD       dwWidthInPixels,     
    DWORD       dwHeightInPixels
    )
{
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        SOURCE_PIXEL_TYPE *pSrcPixel = (SOURCE_PIXEL_TYPE*)pDestScanLine0;
        DEST_PIXEL_TYPE *pDestPixel = (DEST_PIXEL_TYPE*)pSrcScanLine0;

        for (DWORD x = 0; x < dwWidthInPixels; x +=2)
        {
            pDestPixel[x] = TransformPixelValue(pSrcPixel[x]);
        }
        pDestScanLine0 += lDestStride;
        pSrcScanLine0 += lSrcStride;
    }
}
```



<span data-ttu-id="35a84-125">Essa função usa seis parâmetros:</span><span class="sxs-lookup"><span data-stu-id="35a84-125">This function takes six parameters:</span></span>

-   <span data-ttu-id="35a84-126">Um ponteiro para o início da verificação da linha 0 na imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="35a84-126">A pointer to the start of scan line 0 in the destination image.</span></span>
-   <span data-ttu-id="35a84-127">O stride da imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="35a84-127">The stride of the destination image.</span></span>
-   <span data-ttu-id="35a84-128">Um ponteiro para o início da verificação da linha 0 na imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="35a84-128">A pointer to the start of scan line 0 in the source image.</span></span>
-   <span data-ttu-id="35a84-129">O stride da imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="35a84-129">The stride of the source image.</span></span>
-   <span data-ttu-id="35a84-130">A largura da imagem em pixels.</span><span class="sxs-lookup"><span data-stu-id="35a84-130">The width of the image in pixels.</span></span>
-   <span data-ttu-id="35a84-131">A altura da imagem em pixels.</span><span class="sxs-lookup"><span data-stu-id="35a84-131">The height of the image in pixels.</span></span>

<span data-ttu-id="35a84-132">A ideia geral é processar uma linha de cada vez, iterando em cada pixel na linha.</span><span class="sxs-lookup"><span data-stu-id="35a84-132">The general idea is to process one row at a time, iterating over each pixel in the row.</span></span> <span data-ttu-id="35a84-133">Suponha que o tipo de pixel de origem \_ \_ e o tipo de pixel do destino \_ \_ sejam estruturas que representam o layout de pixel para as imagens de origem e de destino, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="35a84-133">Assume that SOURCE\_PIXEL\_TYPE and DEST\_PIXEL\_TYPE are structures representing the pixel layout for the source and destination images, respectively.</span></span> <span data-ttu-id="35a84-134">(Por exemplo, o RGB de 32 bits usa a estrutura [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) .</span><span class="sxs-lookup"><span data-stu-id="35a84-134">(For example, 32-bit RGB uses the [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structure.</span></span> <span data-ttu-id="35a84-135">Nem todo formato de pixel tem uma estrutura predefinida.) A conversão do ponteiro de matriz para o tipo de estrutura permite que você acesse os componentes RGB ou YUV de cada pixel.</span><span class="sxs-lookup"><span data-stu-id="35a84-135">Not every pixel format has a predefined structure.) Casting the array pointer to the structure type enables you to access the RGB or YUV components of each pixel.</span></span> <span data-ttu-id="35a84-136">No início de cada linha, a função armazena um ponteiro para a linha.</span><span class="sxs-lookup"><span data-stu-id="35a84-136">At the start of each row, the function stores a pointer to the row.</span></span> <span data-ttu-id="35a84-137">No final da linha, ele incrementa o ponteiro pela largura do Stride da imagem, o que avança o ponteiro para a próxima linha.</span><span class="sxs-lookup"><span data-stu-id="35a84-137">At the end of the row, it increments the pointer by the width of the image stride, which advances the pointer to the next row.</span></span>

<span data-ttu-id="35a84-138">Este exemplo chama uma função hipotética chamada TransformPixelValue para cada pixel.</span><span class="sxs-lookup"><span data-stu-id="35a84-138">This example calls a hypothetical function named TransformPixelValue for each pixel.</span></span> <span data-ttu-id="35a84-139">Pode ser qualquer função que calcule um pixel de destino a partir de um pixel de origem.</span><span class="sxs-lookup"><span data-stu-id="35a84-139">This could be any function that calculates a target pixel from a source pixel.</span></span> <span data-ttu-id="35a84-140">É claro que os detalhes exatos dependerão da tarefa específica.</span><span class="sxs-lookup"><span data-stu-id="35a84-140">Of course, the exact details will depend on the particular task.</span></span> <span data-ttu-id="35a84-141">Por exemplo, se você tiver um formato de YUV planar, deverá acessar os planos de croma independentemente do plano Luma; com vídeo entrelaçado, talvez seja necessário processar os campos separadamente; e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="35a84-141">For example, if you have a planar YUV format, you must access the chroma planes independently from the luma plane; with interlaced video, you might need to process the fields separately; and so forth.</span></span>

<span data-ttu-id="35a84-142">Para dar um exemplo mais concreto, o código a seguir converte uma imagem RGB de 32 bits em uma imagem AYUV.</span><span class="sxs-lookup"><span data-stu-id="35a84-142">To give a more concrete example, the following code converts a 32-bit RGB image into an AYUV image.</span></span> <span data-ttu-id="35a84-143">Os pixels RGB são acessados usando uma estrutura [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) e os pixels AYUV são acessados usando uma estrutura de estrutura [**DXVA2 \_ AYUVSample8**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_ayuvsample8) .</span><span class="sxs-lookup"><span data-stu-id="35a84-143">The RGB pixels are accessed using an [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structure, and the AYUV pixels are accessed using a [**DXVA2\_AYUVSample8**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_ayuvsample8) structure structure.</span></span>


```C++
//-------------------------------------------------------------------
// Name: RGB32_To_AYUV
// Description: Converts an image from RGB32 to AYUV
//-------------------------------------------------------------------
void RGB32_To_AYUV(
    BYTE*       pDest,
    LONG        lDestStride,
    const BYTE* pSrc,
    LONG        lSrcStride,
    DWORD       dwWidthInPixels,
    DWORD       dwHeightInPixels
    )
{
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        RGBQUAD             *pSrcPixel = (RGBQUAD*)pSrc;
        DXVA2_AYUVSample8   *pDestPixel = (DXVA2_AYUVSample8*)pDest;
        
        for (DWORD x = 0; x < dwWidthInPixels; x++)
        {
            pDestPixel[x].Alpha = 0x80;
            pDestPixel[x].Y = RGBtoY(pSrcPixel[x]);   
            pDestPixel[x].Cb = RGBtoU(pSrcPixel[x]);   
            pDestPixel[x].Cr = RGBtoV(pSrcPixel[x]);   
        }
        pDest += lDestStride;
        pSrc += lSrcStride;
    }
}
```



<span data-ttu-id="35a84-144">O exemplo a seguir converte uma imagem RGB de 32 bits em uma imagem YV12.</span><span class="sxs-lookup"><span data-stu-id="35a84-144">The next example converts a 32-bit RGB image to a YV12 image.</span></span> <span data-ttu-id="35a84-145">Este exemplo mostra como tratar um formato YUV de planar.</span><span class="sxs-lookup"><span data-stu-id="35a84-145">This example shows how to handle a planar YUV format.</span></span> <span data-ttu-id="35a84-146">(YV12 é um formato planar 4:2:0.) Neste exemplo, a função mantém três ponteiros separados para os três planos na imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="35a84-146">(YV12 is a planar 4:2:0 format.) In this example, the function maintains three separate pointers for the three planes in the target image.</span></span> <span data-ttu-id="35a84-147">No entanto, a abordagem básica é a mesma do exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="35a84-147">However, the basic approach is the same as the previous example.</span></span>


```C++
void RGB32_To_YV12(
    BYTE*       pDest,
    LONG        lDestStride,
    const BYTE* pSrc,
    LONG        lSrcStride,
    DWORD       dwWidthInPixels,
    DWORD       dwHeightInPixels
    )
{
    assert(dwWidthInPixels % 2 == 0);
    assert(dwHeightInPixels % 2 == 0);

    const BYTE *pSrcRow = pSrc;
    
    BYTE *pDestY = pDest;

    // Calculate the offsets for the V and U planes.

    // In YV12, each chroma plane has half the stride and half the height  
    // as the Y plane.
    BYTE *pDestV = pDest + (lDestStride * dwHeightInPixels);
    BYTE *pDestU = pDest + 
                   (lDestStride * dwHeightInPixels) + 
                   ((lDestStride * dwHeightInPixels) / 4);

    // Convert the Y plane.
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        RGBQUAD *pSrcPixel = (RGBQUAD*)pSrcRow;
        
        for (DWORD x = 0; x < dwWidthInPixels; x++)
        {
            pDestY[x] = RGBtoY(pSrcPixel[x]);    // Y0
        }
        pDestY += lDestStride;
        pSrcRow += lSrcStride;
    }

    // Convert the V and U planes.

    // YV12 is a 4:2:0 format, so each chroma sample is derived from four 
    // RGB pixels.
    pSrcRow = pSrc;
    for (DWORD y = 0; y < dwHeightInPixels; y += 2)
    {
        RGBQUAD *pSrcPixel = (RGBQUAD*)pSrcRow;
        RGBQUAD *pNextSrcRow = (RGBQUAD*)(pSrcRow + lSrcStride);

        BYTE *pbV = pDestV;
        BYTE *pbU = pDestU;

        for (DWORD x = 0; x < dwWidthInPixels; x += 2)
        {
            // Use a simple average to downsample the chroma.

            *pbV++ = ( RGBtoV(pSrcPixel[x]) +
                       RGBtoV(pSrcPixel[x + 1]) +       
                       RGBtoV(pNextSrcRow[x]) +         
                       RGBtoV(pNextSrcRow[x + 1]) ) / 4;        

            *pbU++ = ( RGBtoU(pSrcPixel[x]) +
                       RGBtoU(pSrcPixel[x + 1]) +       
                       RGBtoU(pNextSrcRow[x]) +         
                       RGBtoU(pNextSrcRow[x + 1]) ) / 4;    
        }
        pDestV += lDestStride / 2;
        pDestU += lDestStride / 2;
        
        // Skip two lines on the source image.
        pSrcRow += (lSrcStride * 2);
    }
}
```



<span data-ttu-id="35a84-148">Em todos esses exemplos, supõe-se que o aplicativo já tenha determinado o stride da imagem.</span><span class="sxs-lookup"><span data-stu-id="35a84-148">In all of these examples, it is assumed that the application has already determined the image stride.</span></span> <span data-ttu-id="35a84-149">Às vezes, você pode obter essas informações do buffer de mídia.</span><span class="sxs-lookup"><span data-stu-id="35a84-149">You can sometimes get this information from the media buffer.</span></span> <span data-ttu-id="35a84-150">Caso contrário, você deve calculá-lo com base no formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="35a84-150">Otherwise, you must calculate it based on the video format.</span></span> <span data-ttu-id="35a84-151">Para obter mais informações sobre como calcular o stride de imagem e trabalhar com buffers de mídia para vídeo, consulte [buffers de vídeo não compactados](uncompressed-video-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="35a84-151">For more information about calculating image stride and working with media buffers for video, see [Uncompressed Video Buffers](uncompressed-video-buffers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="35a84-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="35a84-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35a84-153">Tipos de mídia de vídeo</span><span class="sxs-lookup"><span data-stu-id="35a84-153">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="35a84-154">Tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="35a84-154">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 
