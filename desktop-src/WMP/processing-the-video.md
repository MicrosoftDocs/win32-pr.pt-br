---
title: Processando o vídeo
description: Processando o vídeo
ms.assetid: 2fa337dd-34c0-4a09-8c20-21f6103627dd
keywords:
- Plug-ins do Windows Media Player, DSP de vídeo
- plug-ins, DSP de vídeo
- plug-ins de processamento de sinal digital, processamento de vídeo
- Plug-ins do DSP, processamento de vídeo
- plug-ins de DSP de vídeo, processamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a8d21aaa3999d05ea3628ff341c74379b07a6dd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007730"
---
# <a name="processing-the-video"></a><span data-ttu-id="a4f70-108">Processando o vídeo</span><span class="sxs-lookup"><span data-stu-id="a4f70-108">Processing the Video</span></span>

<span data-ttu-id="a4f70-109">Os detalhes do processamento de vídeo variam para cada formato; está além do escopo desta documentação para fornecer esses detalhes.</span><span class="sxs-lookup"><span data-stu-id="a4f70-109">The details of processing video vary for each format; it is beyond the scope of this documentation to provide these details.</span></span> <span data-ttu-id="a4f70-110">Em um sentido geral, o objetivo do plug-in é alterar os dados de cor no buffer de entrada e, em seguida, copiar os dados para o buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="a4f70-110">In a general sense, the goal of the plug-in is to change the color data in the input buffer and then copy the data to the output buffer.</span></span>

<span data-ttu-id="a4f70-111">O plug-in de exemplo processa dois tipos de formatos de vídeo: YUV e RGB.</span><span class="sxs-lookup"><span data-stu-id="a4f70-111">The sample plug-in processes two types of video formats: YUV and RGB.</span></span>

<span data-ttu-id="a4f70-112">Para vídeo YUV, as informações de cor vermelha e azul são codificadas nos valores de você e V e o nível de luminância é representado pelo valor Y; o valor verde é codificado e pode ser recuperado usando um algoritmo.</span><span class="sxs-lookup"><span data-stu-id="a4f70-112">For YUV video, the red and blue color information is encoded in the U and V values and the luminance level is represented by the Y value; the green value is encoded and can be recovered by using an algorithm.</span></span> <span data-ttu-id="a4f70-113">O plug-in de exemplo simplesmente altera os valores de você e V para afetar o nível de cor.</span><span class="sxs-lookup"><span data-stu-id="a4f70-113">The sample plug-in simply changes the U and V values to affect the color level.</span></span> <span data-ttu-id="a4f70-114">Cada U ou V byte tem um valor entre zero e 255.</span><span class="sxs-lookup"><span data-stu-id="a4f70-114">Each U or V byte has a value between zero and 255.</span></span> <span data-ttu-id="a4f70-115">O plug-in primeiro ajusta cada valor a ser representado por um intervalo de-128 a 127 e, em seguida, dimensiona o valor pelo fator de escala fornecido.</span><span class="sxs-lookup"><span data-stu-id="a4f70-115">The plug-in first adjusts each value to be represented by a range from -128 to 127, and then scales the value by the supplied scale factor.</span></span> <span data-ttu-id="a4f70-116">Por fim, o código ajusta o valor novamente para o intervalo original de zero a 255 e copia os dados para o buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="a4f70-116">Finally, the code adjusts the value again for the original zero-to-255 range and copies the data to the output buffer.</span></span> <span data-ttu-id="a4f70-117">O código de exemplo a seguir processa o vídeo UYVY.</span><span class="sxs-lookup"><span data-stu-id="a4f70-117">The following example code processes UYVY video.</span></span> <span data-ttu-id="a4f70-118">Nesse formato, todos os outros bytes são um valor U ou Y.</span><span class="sxs-lookup"><span data-stu-id="a4f70-118">In this format, every other byte is a U or Y value.</span></span>


```C++
while( dwHeight-- )
{
    DWORD x = dwWidth; 

        while( x-- )
        {
        // Scale the U and V bytes to 128.
        // Just copy the Y bytes.
        if( x%2 )
        {
            pbTarget[x] = pbSource[x];
        }
        else
        {
            long temp = (long)((pbSource[x] - 128) * m_fScaleFactor);

            // Truncate if exceeded full scale.
            if (temp > 127)
            temp = 127;
            if (temp < -128)
            temp = -128;

            pbTarget[x] = temp + 128;
        }
    }

    // Move the pointers to the next row.
    pbSource += lStrideIn;
    pbTarget += lStrideOut;
}

```



<span data-ttu-id="a4f70-119">Para vídeo RGB, as informações de cor e luminância são codificadas como valores vermelho, verde e azul separados.</span><span class="sxs-lookup"><span data-stu-id="a4f70-119">For RGB video, the color and luminance information is encoded as separate red, green, and blue values.</span></span> <span data-ttu-id="a4f70-120">O plug-in de exemplo calcula a média dos três valores para determinar o valor de cinza e, em seguida, ajusta cada valor de cor usando o fator de escala fornecido.</span><span class="sxs-lookup"><span data-stu-id="a4f70-120">The sample plug-in computes the average of the three values to determine the value for gray, and then adjusts each color value by using the supplied scale factor.</span></span> <span data-ttu-id="a4f70-121">Mais uma vez, os valores devem ser normalizados para o intervalo-128 a 127 antes do dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="a4f70-121">Once again, the values must be normalized for the -128 to 127 range before scaling.</span></span> <span data-ttu-id="a4f70-122">O código a seguir de Process32Bit mostra o processo para RGB32:</span><span class="sxs-lookup"><span data-stu-id="a4f70-122">The following code from Process32Bit shows the process for RGB32:</span></span>


```C++
while( dwHeight-- )
{
    RGBQUAD* pPixelIn = (RGBQUAD*)pbSource;
    RGBQUAD* pPixelOut = (RGBQUAD*)pbTarget;

    for( DWORD x = 0; x < dwWidth; x++ )
    {
    // Get the color bytes.
    long lBlue = (long) pPixelIn[x].rgbBlue;
    long lGreen = (long) pPixelIn[x].rgbGreen;
    long lRed = (long) pPixelIn[x].rgbRed;

    // Compute the average for gray.
    long lAverage = ( lBlue + lGreen + lRed ) / 3;

    // Scale the colors to the average.
    pPixelOut[x].rgbBlue = (BYTE)( ( lBlue - lAverage ) * m_fScaleFactor  + lAverage );
    pPixelOut[x].rgbGreen = (BYTE)( ( lGreen - lAverage ) * m_fScaleFactor  + lAverage );
    pPixelOut[x].rgbRed = (BYTE)( ( lRed - lAverage ) * m_fScaleFactor  + lAverage );
    pPixelOut[x].rgbReserved = pPixelIn[x].rgbReserved;
    }

    // Move the pointers to the next row.
    pbSource += lStrideIn;
    pbTarget += lStrideOut;
}

```



<span data-ttu-id="a4f70-123">Para obter mais informações sobre formatos de vídeo, consulte o [site FOURCC](../directshow/fourcc-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a4f70-123">For more information about video formats, see the [FourCC website](../directshow/fourcc-codes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4f70-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a4f70-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4f70-125">**Implementando um plug-in de DSP de vídeo**</span><span class="sxs-lookup"><span data-stu-id="a4f70-125">**Implementing a Video DSP Plug-in**</span></span>](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 