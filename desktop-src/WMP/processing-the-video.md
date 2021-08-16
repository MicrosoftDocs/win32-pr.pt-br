---
title: Processamento do vídeo
description: Processamento do vídeo
ms.assetid: 2fa337dd-34c0-4a09-8c20-21f6103627dd
keywords:
- Windows Media Player plug-ins,DSP de vídeo
- plug-ins, DSP de vídeo
- plug-ins de processamento de sinal digital, processamento de vídeo
- Plug-ins do DSP, processamento de vídeo
- plug-ins DSP de vídeo, processamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea168199270cfe8029b7b9303a7745db2c255f4268252a5bd80472a73c6f2f29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334019"
---
# <a name="processing-the-video"></a>Processamento do vídeo

Os detalhes do vídeo de processamento variam para cada formato; está além do escopo desta documentação para fornecer esses detalhes. Em um sentido geral, o objetivo do plug-in é alterar os dados de cor no buffer de entrada e, em seguida, copiar os dados para o buffer de saída.

O plug-in de exemplo processa dois tipos de formatos de vídeo: YUV e RGB.

Para o vídeo YUV, as informações de cor vermelha e azul são codificadas nos valores de você e V e o nível de luminância é representado pelo valor Y; o valor verde é codificado e pode ser recuperado usando um algoritmo . O plug-in de exemplo simplesmente altera os valores de você e V para afetar o nível de cor. Cada byte U ou V tem um valor entre zero e 255. O plug-in primeiro ajusta cada valor a ser representado por um intervalo de -128 a 127 e, em seguida, dimensiona o valor pelo fator de escala fornecido. Por fim, o código ajusta o valor novamente para o intervalo original de zero a 255 e copia os dados para o buffer de saída. O código de exemplo a seguir processa o vídeo UYVY. Nesse formato, todos os outros byte são um valor U ou Y.


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



Para o vídeo RGB, as informações de cor e luminância são codificadas como valores vermelhos, verdes e azuis separados. O plug-in de exemplo calcula a média dos três valores para determinar o valor de cinza e, em seguida, ajusta cada valor de cor usando o fator de escala fornecido. Mais uma vez, os valores devem ser normalizados para o intervalo -128 a 127 antes do dimensionamento. O código a seguir de Process32Bit mostra o processo para RGB32:


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



Para obter mais informações sobre formatos de vídeo, consulte o site [do FourCC.](../directshow/fourcc-codes.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando um plug-in DSP de vídeo**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 