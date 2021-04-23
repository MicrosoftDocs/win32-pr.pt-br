---
description: Transformações de pré-processamento do decodificador MPEG
ms.assetid: c7ae0137-0d02-46da-9532-738d805e327d
title: Transformações de pré-processamento do decodificador MPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d7bcf8eeda8062606ce0046a55e34d3c2d90fe
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908894"
---
# <a name="mpeg-decoder-preprocessing-transformations"></a>Transformações de pré-processamento do decodificador MPEG

**Letterbox e PanScan**

A imagem 4x3 pode ser formada preenchendo a parte superior e inferior da imagem (chamada de imagem Letterbox) ou extraindo uma parte 4x3 da imagem (chamada de imagem PanScan). Os fluxos de menus e subimagem são sobrepostos sobre a imagem de vídeo final. As imagens de taxa de 16x9 são armazenadas em um formato 4x3 Anamorphic. Esticar o vídeo de origem 720x480 de proporção de 4x3 de Anamorphic para uma taxa de proporção 16x9 forma a imagem de aspecto do 16x9 original.

Veja abaixo uma descrição de como exibir corretamente cada um dos modos e seus destaques:

-   **Tela widescreen:** O vídeo de origem ampliado para a maior área de 16x9 da janela de saída. Os destaques são relativos ao interior da área 16x9. As barras pretas devem ser adicionadas à parte superior e inferior ou aos lados para manter uma área 16x9.
-   **Verificação de Pan:** No vídeo do 16x9, use o deslocamento horizontal fornecido no fluxo MPEG2 para extrair uma subjanela 4x3. Coloque a subjanela 4x3 na área de maior 4x3 da janela do cliente de saída. As coordenadas do realce são relativas à janela de saída 4x3 e não têm relação com o vídeo 16x9 de origem. As barras pretas devem ser adicionadas à parte superior e inferior ou aos lados para manter uma área 4x3.
-   **Letterbox:** Calcule a maior área de 4x3 da janela de saída. As barras pretas devem ser adicionadas à parte superior e inferior ou aos lados para manter uma área 4x3. O vídeo Anamorphic de origem 4x3 (representando uma imagem 16x9) é colocado na maior subjanela 16x9 dentro da área 4x3. As barras pretas devem ser adicionadas à parte superior e inferior da subjanela para manter uma área 16x9. As coordenadas do realce são relativas à área 4x3 e não têm relação com o vídeo 16x9 de origem. É possível que um disco especifique um realce que está fora da área 16x9 (mas ainda na janela 4x3). Para vídeo 4x3, o vídeo é colocado na área de saída maior 4x3 da janela do cliente de saída. As barras pretas devem ser adicionadas à parte superior e inferior ou aos lados para manter uma área 4x3.

**Pré-processamento de MPEG com o navegador de DVD e o VMR**

Atualmente, o decodificador é passado \_ como um tipo de mídia de vídeo MPEG2 de formato \_ (cujo bloco de formato aponta para uma estrutura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) ). Nos Pins de saída, o decodificador produz um tipo de mídia de formato \_ VideoInfo2, cujo bloco de formato aponta para uma estrutura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) . O campo **dwReserved** da estrutura foi renomeado para sinalizadores **dwControls** .

O membro **dwControlFlags** agora conterá os novos bits.



| Label | Valor |
|--------------------------|------------|
| AMCONTROL \_ usado          | 0x00000001 |
| AMCONTROL \_ pad \_ para \_ 4x3  | 0x00000002 |
| AMCONTROL \_ pad \_ para \_ 16x9 | 0x00000004 |



 

O AMCONTROL \_ usado é usado para testar se há suporte para esses novos sinalizadores. Um filtro de origem deve definir o \_ sinalizador AMCONTROL usado e ver se o QueryAccept (MediaType) foi bem sucedido no PIN do downstream. Se ele for rejeitado, os sinalizadores AMCONTROL não poderão ser usados e dwReserved1 deverá ser definido como 0.

AMCONTROL \_ pad \_ para \_ 4x3 indica que a imagem deve ser preenchida e exibida em uma área de 4x3.

AMCONTROL \_ pad \_ para \_ 16x9 indica que a imagem deve ser preenchida e exibida em uma área de 16x9.

O decodificador deve copiar ou processar os bits de forma oculta. Se o decodificador executar o formato Letterbox em si, ele deverá alterar a taxa de proporção de pixel, preencher a imagem e remover os bits AMCONTROL correspondentes \_ \* .

O MPEG2VIDEOINFO. dwFlags agora contém três sinalizadores para controlar como o conteúdo deve ser exibido:

-   `AMMPEG2_DoPanScan (0x00000001)`: Se esse sinalizador for definido, o decodificador de vídeo MPEG-2 deverá cortar a imagem de saída com base nos vetores de digitalização de Pan na extensão de exibição de imagem \_ \_ e alterar a taxa de proporção da imagem para 4x3. O VMR não deve receber um exemplo de 16x9 com esse sinalizador. Uma implementação simples pode alterar o retângulo de origem para indicar uma região de origem de 540 largo com uma borda esquerda igual ao deslocamento de exibição na extensão de exibição de imagem \_ \_ .
-   `AMMPEG2_LetterboxAnalogOut (0x00000020)`: Quando um decodificador de hardware exibe esse fluxo para uma saída de vídeo (geralmente um conector SVIDEO no cartão), ele deve aplicar as regras para exibir um exemplo de 16x9 em uma exibição de 4x3.

    Um decodificador de software (ou um decodificador de hardware produzindo saída enviada para o VMR) tem duas opções ao processar imagens:

    1.  Ignore esse sinalizador e passe o conteúdo do VideoInfoHeader2 para o VMR (o AMCONTROL \_ pad \_ para \_ 4x3 Flag já será definido pelo [navegador de DVD](dvd-navigator-filter.md) no exemplo). O VMR encontrará um exemplo de vídeo 16x9 com o AMCONTROL \_ pad \_ para \_ 4x3 conjunto de sinalizadores e um fluxo de subimagem 4x3. O aplicativo deve definir os retângulos de destino normalizados dos dois fluxos para ter a mesma largura.
    2.  Converta o fluxo Anamorphic em uma imagem 4x3 preenchendo a parte superior e inferior da imagem e definindo a taxa de proporção da imagem como 4x3 (consulte Letterbox acima) e removendo o \_ bloco AMCONTROL \_ para \_ 4x3 bit do VIDEOINFOHEADER2.

    Os decodificadores DirectXVA que mesclam os fluxos de vídeo e subimagem terão que processar esse sinalizador. Se o hardware não puder dimensionar a subimagem mesclada, o decodificador deverá produzir um fluxo de subimagem separado para o VMR para misturar com o vídeo.

-   `AMMPEG2_WidescreenAnalogOut (0x00000200)`: Quando um decodificador de hardware exibe esse fluxo para uma saída de vídeo (geralmente um conector SVIDEO no cartão), ele deve assumir uma exibição de 16x9 (Anamorphic).

    Um decodificador de software (ou um decodificador de hardware produzindo saída enviada para o VMR) tem duas opções ao processar uma imagem Anamorphic:

    1.  Ignore esse sinalizador e copie o conteúdo do VideoInfoHeader2 para o VMR. O VMR irá preencher as imagens de 4x3 para 16x9 se elas tiverem o AMCONTROL \_ pad \_ para \_ 16x9 definido.
    2.  Preencha a imagem de saída para uma imagem 16x9 e remova o AMCONTROL \_ pad \_ para \_ 16x9 bit.

A maioria dos decodificadores deve usar **GetMediaType** para detectar uma alteração de mídia no pino de entrada e copiar o conteúdo de **VIDEOINFOHEADER2** (contido no **MPEG2INFOHEADER**) para o pino de saída. Provavelmente, eles só processarão o bit PanScan.

O código de exemplo a seguir mostra como copiar o conteúdo do **VIDEOINFOHEADER2** de um PIN de entrada para um pino de saída.


```C++
#include <dvdmedia.h>
HRESULT CopyMPeg2ToVideoInfoHeader2(CMediaSample* pInSample, CMediaSample* pOutSample)
{
    HRESULT hr = S_OK;
    // Check for a media type on the input sample.
    AM_MEDIA_TYPE* pInType;
    if (pInSample->GetMediaType(&pInType) == S_OK) 
    {
        // Make sure it's an MPEG2 Video format.
        if ((pInType->formattype == FORMAT_MPEG2_VIDEO) &&
            (pInType->cbFormat >= sizeof(MPEG2VIDEOINFO)))
        {
            hr = S_OK; // Initialize hr for the CMediaType constructor.
            CMediaType outType(*pInType, &hr);
            if (FAILED(hr))
            {
                DeleteMediaType( pInType );
                return hr;
            }

            // Set the format type GUID.
            outType.SetFormatType(&FORMAT_VideoInfo2);
                
            // Truncate the format block to include just the VIDEOINFOHEADER part.
            MPEG2VIDEOINFO *pMPeg2Header = (MPEG2VIDEOINFO*)pInType->pbFormat;
            BYTE *pVIH = (BYTE*)&pMPeg2Header->hdr;
            hr = (outType.SetFormat(pVIH, sizeof(VIDEOINFOHEADER2)) ? S_OK : E_OUTOFMEMORY);
            if (SUCCEEDED(hr))
            {
                hr = pOutSample->SetMediaType(&outType);
            }
        } 
        else 
        {
            ASSERT(FALSE); // Not a MPEG2 header.
            hr = VFW_E_INVALIDMEDIATYPE;
        }
        DeleteMediaType( pInType );
    } 

    return hr;
}
```



 

 



