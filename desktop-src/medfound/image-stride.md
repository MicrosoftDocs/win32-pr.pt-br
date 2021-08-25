---
description: Passo da imagem
ms.assetid: 13cd1106-48b3-4522-ac09-8efbaab5c31d
title: Passo da imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360afb6fdeca4c543957326b041654d75ff17b66db8918e42d781d414e8b7586
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958137"
---
# <a name="image-stride"></a>Passo da imagem

Quando uma imagem de vídeo é armazenada na memória, o buffer de memória pode conter bytes de preenchimento extra após cada linha de pixels. Os bytes de preenchimento afetam como a imagem é armazenada na memória, mas não afetam como a imagem é exibida.

O *stride* é o número de bytes de uma linha de pixels na memória para a próxima linha de pixels na memória. Stride também é chamado *de tom*. Se bytes de preenchimento estão presentes, o stride é maior do que a largura da imagem, conforme mostrado na ilustração a seguir.

![diagrama mostrando uma imagem mais preenchimento.](images/c85c6a40-f0a8-48a3-b465-39ceada66339.gif)

Dois buffers que contêm quadros de vídeo com dimensões iguais podem ter dois passos diferentes. Se você processar uma imagem de vídeo, deverá levar em conta o passo a passo.

Além disso, há duas maneiras pelas quais uma imagem pode ser organizada na memória. Em uma *imagem de cima* para baixo, a linha superior de pixels na imagem aparece primeiro na memória. Em uma *imagem de baixo* para cima, a última linha de pixels aparece primeiro na memória. A ilustração a seguir mostra a diferença entre uma imagem de cima para baixo e uma imagem de baixo para cima.

![diagrama mostrando imagens de cima para baixo e de baixo para cima.](images/f03bd9ff-0cf3-4a56-88c5-5b8c44637272.gif)

Uma imagem de baixo para cima tem um avanço negativo, pois stride é definido como o número de bytes que precisam mover para baixo uma linha de pixels, em relação à imagem exibida. As imagens YUV sempre devem estar de cima para baixo e qualquer imagem contida em uma superfície Direct3D deve estar de cima para baixo. As imagens RGB na memória do sistema geralmente são de baixo para cima.

As transformaçãos de vídeo em particular precisam lidar com buffers com passadas incompatibilidades, pois o buffer de entrada pode não corresponder ao buffer de saída. Por exemplo, suponha que você queira converter uma imagem de origem e gravar o resultado em uma imagem de destino. Suponha que ambas as imagens tenham a mesma largura e altura, mas talvez não tenham o mesmo formato de pixel ou a mesma distância da imagem.

O código de exemplo a seguir mostra uma abordagem generalizada para escrever esse tipo de função. Esse não é um exemplo de trabalho completo, pois abstrai muitos dos detalhes específicos.


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



Essa função aceita seis parâmetros:

-   Um ponteiro para o início da linha de verificação 0 na imagem de destino.
-   O avanço da imagem de destino.
-   Um ponteiro para o início da linha de verificação 0 na imagem de origem.
-   O avanço da imagem de origem.
-   A largura da imagem em pixels.
-   A altura da imagem em pixels.

A ideia geral é processar uma linha por vez, iterando em cada pixel na linha. Suponha que SOURCE PIXEL TYPE e DEST PIXEL TYPE sejam estruturas que representam o layout de pixel para as imagens de origem e de \_ \_ \_ \_ destino, respectivamente. (Por exemplo, o RGB de 32 bits usa a [**estrutura RGBQUAD.**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) Nem todo formato de pixel tem uma estrutura predefinida.) A transmissão do ponteiro de matriz para o tipo de estrutura permite que você acesse os componentes RGB ou YUV de cada pixel. No início de cada linha, a função armazena um ponteiro para a linha. No final da linha, ele incrementa o ponteiro pela largura da distância da imagem, o que avança o ponteiro para a próxima linha.

Este exemplo chama uma função hipotética chamada TransformPixelValue para cada pixel. Pode ser qualquer função que calcule um pixel de destino de um pixel de origem. É claro que os detalhes exatos dependerão da tarefa específica. Por exemplo, se você tiver um formato YUV planar, deverá acessar os planos de chroma independentemente do plano luma; com vídeo entrelaçados, talvez seja necessário processar os campos separadamente; e assim por diante.

Para dar um exemplo mais concreto, o código a seguir converte uma imagem RGB de 32 bits em uma imagem AYUV. Os pixels RGB são acessados usando uma estrutura [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) e os pixels AYUV são acessados usando uma estrutura [**DXVA2 \_ AYUVSample8.**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_ayuvsample8)


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



O exemplo a seguir converte uma imagem RGB de 32 bits em uma imagem YV12. Este exemplo mostra como lidar com um formato YUV planar. (YV12 é um formato planar 4:2:0.) Neste exemplo, a função mantém três ponteiros separados para os três planos na imagem de destino. No entanto, a abordagem básica é a mesma do exemplo anterior.


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



Em todos esses exemplos, supõe-se que o aplicativo já tenha determinado o progresso da imagem. Às vezes, você pode obter essas informações do buffer de mídia. Caso contrário, você deve calculá-lo com base no formato de vídeo. Para obter mais informações sobre como calcular o passo da imagem e trabalhar com buffers de mídia para vídeo, consulte [Buffers de vídeo descompactados.](uncompressed-video-buffers.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de mídia de vídeo](video-media-types.md)
</dt> <dt>

[Tipos de mídia](media-types.md)
</dt> </dl>

 

 
