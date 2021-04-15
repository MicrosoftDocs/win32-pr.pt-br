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
# <a name="image-stride"></a>Stride da imagem

Quando uma imagem de vídeo é armazenada na memória, o buffer de memória pode conter bytes de preenchimento extras após cada linha de pixels. Os bytes de preenchimento afetam a forma como a imagem é armazenada na memória, mas não afetam o modo como a imagem é exibida.

O *Stride* é o número de bytes de uma linha de pixels na memória até a próxima linha de pixels na memória. O stride também é chamado de *pitch*. Se os bytes de preenchimento estiverem presentes, o stride será mais largo do que a largura da imagem, conforme mostrado na ilustração a seguir.

![diagrama mostrando uma imagem e preenchimento.](images/c85c6a40-f0a8-48a3-b465-39ceada66339.gif)

Dois buffers que contêm quadros de vídeo com dimensões iguais podem ter dois passos diferentes. Se você processar uma imagem de vídeo, deverá levar em conta o Stride.

Além disso, há duas maneiras pelas quais uma imagem pode ser organizada na memória. Em uma imagem de *cima para baixo* , a linha superior de pixels na imagem aparece primeiro na memória. Em uma imagem de *baixo* , a última linha de pixels aparece primeiro na memória. A ilustração a seguir mostra a diferença entre uma imagem de cima para baixo e uma imagem de baixo para cima.

![diagrama mostrando imagens de cima para baixo e de baixo para cima.](images/f03bd9ff-0cf3-4a56-88c5-5b8c44637272.gif)

Uma imagem inferior tem um stride negativo, porque o stride é definido como o número de bytes que precisam ser movidos para baixo em uma linha de pixels, em relação à imagem exibida. As imagens YUV devem ser sempre de cima para baixo e qualquer imagem contida em uma superfície do Direct3D deve ser de cima para baixo. As imagens RGB na memória do sistema geralmente são de baixo para cima.

As transformações de vídeo, em particular, precisam lidar com os buffers com progressos incompatíveis, pois o buffer de entrada pode não corresponder ao buffer de saída. Por exemplo, suponha que você deseja converter uma imagem de origem e gravar o resultado em uma imagem de destino. Suponha que ambas as imagens tenham a mesma largura e altura, mas que podem não ter o mesmo formato de pixel ou o mesmo Stride de imagem.

O código de exemplo a seguir mostra uma abordagem generalizada para gravar esse tipo de função. Esse não é um exemplo funcional completo, pois abstrai muitos dos detalhes específicos.


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



Essa função usa seis parâmetros:

-   Um ponteiro para o início da verificação da linha 0 na imagem de destino.
-   O stride da imagem de destino.
-   Um ponteiro para o início da verificação da linha 0 na imagem de origem.
-   O stride da imagem de origem.
-   A largura da imagem em pixels.
-   A altura da imagem em pixels.

A ideia geral é processar uma linha de cada vez, iterando em cada pixel na linha. Suponha que o tipo de pixel de origem \_ \_ e o tipo de pixel do destino \_ \_ sejam estruturas que representam o layout de pixel para as imagens de origem e de destino, respectivamente. (Por exemplo, o RGB de 32 bits usa a estrutura [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) . Nem todo formato de pixel tem uma estrutura predefinida.) A conversão do ponteiro de matriz para o tipo de estrutura permite que você acesse os componentes RGB ou YUV de cada pixel. No início de cada linha, a função armazena um ponteiro para a linha. No final da linha, ele incrementa o ponteiro pela largura do Stride da imagem, o que avança o ponteiro para a próxima linha.

Este exemplo chama uma função hipotética chamada TransformPixelValue para cada pixel. Pode ser qualquer função que calcule um pixel de destino a partir de um pixel de origem. É claro que os detalhes exatos dependerão da tarefa específica. Por exemplo, se você tiver um formato de YUV planar, deverá acessar os planos de croma independentemente do plano Luma; com vídeo entrelaçado, talvez seja necessário processar os campos separadamente; e assim por diante.

Para dar um exemplo mais concreto, o código a seguir converte uma imagem RGB de 32 bits em uma imagem AYUV. Os pixels RGB são acessados usando uma estrutura [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) e os pixels AYUV são acessados usando uma estrutura de estrutura [**DXVA2 \_ AYUVSample8**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_ayuvsample8) .


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



O exemplo a seguir converte uma imagem RGB de 32 bits em uma imagem YV12. Este exemplo mostra como tratar um formato YUV de planar. (YV12 é um formato planar 4:2:0.) Neste exemplo, a função mantém três ponteiros separados para os três planos na imagem de destino. No entanto, a abordagem básica é a mesma do exemplo anterior.


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



Em todos esses exemplos, supõe-se que o aplicativo já tenha determinado o stride da imagem. Às vezes, você pode obter essas informações do buffer de mídia. Caso contrário, você deve calculá-lo com base no formato de vídeo. Para obter mais informações sobre como calcular o stride de imagem e trabalhar com buffers de mídia para vídeo, consulte [buffers de vídeo não compactados](uncompressed-video-buffers.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de mídia de vídeo](video-media-types.md)
</dt> <dt>

[Tipos de mídia](media-types.md)
</dt> </dl>

 

 
