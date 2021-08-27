---
description: Transformações de pré-processamento do decodificador MPEG
ms.assetid: c7ae0137-0d02-46da-9532-738d805e327d
title: Transformações de pré-processamento do decodificador MPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c05ecf25bedb2a90af239715a3becb9a0adc198ed315d2b2c4deea4b380711
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075806"
---
# <a name="mpeg-decoder-preprocessing-transformations"></a>Transformações de pré-processamento do decodificador MPEG

**Letterbox e PanScan**

A imagem 4x3 pode ser formada pelo preenchimento da parte superior e inferior da imagem (conhecida como imagem letterbox) ou pela extração de uma parte 4x3 da imagem (conhecida como uma imagem PanScan). Os menus e os fluxos de subspícone são sobreposição na parte superior da imagem de vídeo final. As imagens de proporção 16x9 são armazenadas em um formato anamórfico 4x3. Alongar a taxa de proporção 4x3 anamórfica 720x480 vídeo de origem para uma taxa de proporção 16x9 forma a imagem de aspecto original 16x9.

Abaixo está uma descrição de como exibir corretamente cada um dos modos e seus destaques:

-   **Widescreen:** O vídeo de origem se estendeu para a maior área 16x9 da janela de saída. Os destaques são relativos ao interior da área 16x9. As barras pretas devem ser adicionadas à parte superior e inferior ou aos lados para manter uma área 16x9.
-   **Verificação panorár digital:** No vídeo 16x9, use o deslocamento horizontal fornecido no fluxo MPEG2 para extrair uma subwindow 4x3. Coloque a subwindow 4x3 na maior área 4x3 da janela do cliente de saída. As coordenadas do realçam são relativas à janela de saída 4x3 e não têm nenhuma relação com o vídeo de origem 16x9. As barras pretas devem ser adicionadas à parte superior e inferior ou aos lados para manter uma área 4x3.
-   **Caixa de texto:** Compute a maior área 4x3 da janela de saída. As barras pretas devem ser adicionadas à parte superior e inferior ou aos lados para manter uma área 4x3. O vídeo de origem anamórfico 4x3 (que representa uma imagem 16x9) é colocado na maior subwindow 16x9 dentro da área 4x3. As barras pretas devem ser adicionadas à parte superior e inferior da subwindow para manter uma área 16x9. As coordenadas do realçam são relativas à área 4x3 e não têm nenhuma relação com o vídeo de origem 16x9. É possível que um disco especifique um realçando que esteja fora da área 16x9 (mas ainda na janela 4x3). Para o vídeo 4x3, o vídeo é colocado na maior área de saída 4x3 da janela do cliente de saída. As barras pretas devem ser adicionadas à parte superior e inferior ou aos lados para manter uma área 4x3.

**Pré-processamento do MPEG com o Navegador de DVD e a VMR**

Atualmente, o decodificador é passado um tipo de mídia FORMAT MPEG2 VIDEO (cujo bloco de formato aponta para uma estrutura \_ \_ [**MPEG2VIDEOINFO).**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) Nos pinos de saída, o decodificador produz um tipo de mídia FORMAT VideoInfo2, cujo bloco de formato aponta \_ para uma [**estrutura VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) O campo **dwReserved** da estrutura foi renomeado para **sinalizadores dwControls.**

O **membro dwControlFlags** agora conterá os novos bits.



| Rótulo | Valor |
|--------------------------|------------|
| AMCONTROL \_ USADO          | 0x00000001 |
| AMCONTROL \_ PAD \_ TO \_ 4x3  | 0x00000002 |
| AMCONTROL \_ PAD \_ TO \_ 16x9 | 0x00000004 |



 

AMCONTROL USED é usado para testar se há suporte para \_ esses novos sinalizadores. Um filtro de origem deve definir o sinalizador AMCONTROL USED e ver se \_ QueryAccept(MediaType) é bem-sucedido no pino downstream. Se ele for rejeitado, os sinalizadores AMCONTROL não poderão ser usados e dwReserved1 deverá ser definido como 0.

AMCONTROL PAD TO 4x3 indica que a imagem deve ser preenchimento e \_ exibida em uma área \_ \_ 4x3.

AMCONTROL PAD TO 16x9 indica que a imagem deve ser preenchimento e exibida em uma área \_ \_ \_ 16x9.

O decodificador deve copiar ou processar os bits às escuras. Se o decodificador executar o próprio letterboxing, ele deverá alterar a taxa de proporção de pixel, pad da imagem e remover os bits AMCONTROL \_ \* correspondentes.

O MPEG2VIDEOINFO.dwFlags agora contém três sinalizadores para controlar como o conteúdo deve ser exibido:

-   `AMMPEG2_DoPanScan (0x00000001)`: se esse sinalizador for definido, o decodificador de vídeo MPEG-2 deverá recortar a imagem de saída com base em vetores de verificação panorárca na extensão de exibição de imagem e alterar a taxa de proporção da imagem para \_ \_ 4x3. A VMR não deve receber um exemplo 16x9 com esse sinalizador. Uma implementação simples pode alterar o retângulo de origem para indicar uma região de origem de 540 largura com uma borda esquerda igual ao deslocamento de exibição na extensão de \_ exibição de \_ imagem.
-   `AMMPEG2_LetterboxAnalogOut (0x00000020)`: quando um decodificador de hardware exibe esse fluxo para uma saída de vídeo (geralmente um conector SVIDEO no cartão), ele deve aplicar as regras para exibir um exemplo 16x9 em uma exibição 4x3.

    Um decodificador de software (ou um decodificador de hardware que produz a saída enviada para a VMR) tem duas opções ao processar imagens:

    1.  Ignore esse sinalizador e passe o conteúdo videoInfoHeader2 para a VMR (o sinalizador AMCONTROL \_ PAD \_ TO \_ 4x3 [](dvd-navigator-filter.md) já será definido pelo Navegador de DVD no exemplo). A VMR encontrará um exemplo de vídeo 16x9 com o sinalizador AMCONTROL PAD TO 4x3 definido e um fluxo \_ \_ de \_ subpicture 4x3. O aplicativo deve definir os retângulos de destino normalizados de saída dos dois fluxos para ter a mesma largura.
    2.  Converta o fluxo anamórfico em uma imagem 4x3, preenchimento da parte superior e inferior da imagem e definindo a taxa de proporção da imagem como 4x3 (consulte Letterbox acima) e removendo o PAD AMCONTROL \_ \_ PARA \_ 4x3 bit do VIDEOINFOHEADER2.

    Os decodificadores directXVA que mesclam os fluxos de vídeo e subpicture terão que processar esse sinalizador. Se o hardware não puder dimensionar a subpicture mesclada, o decodificador deverá produzir um fluxo de subspícone separado para que a VMR se misture com o vídeo.

-   `AMMPEG2_WidescreenAnalogOut (0x00000200)`: quando um decodificador de hardware exibe esse fluxo para uma saída de vídeo (geralmente um conector SVIDEO no cartão), ele deve assumir uma exibição 16x9 (anamórfica).

    Um decodificador de software (ou um decodificador de hardware que produz a saída enviada para a VMR) tem duas opções ao processar uma imagem anamórfica:

    1.  Ignore esse sinalizador e copie o conteúdo videoInfoHeader2 para a VMR. A VMR colocará imagens 4x3 em 16x9 se elas têm o \_ AMCONTROL PAD \_ TO \_ 16x9 definido.
    2.  Pad da imagem de saída para uma imagem 16x9 e remova o PAINEL AMCONTROL \_ \_ TO \_ 16x9 bit.

A maioria dos decodificadores deve usar **GetMediaType** para detectar uma alteração de mídia no pino de entrada e copiar o conteúdo **de VIDEOINFOHEADER2** (contido no **MPEG2INFOHEADER**) para o pino de saída. Provavelmente, eles processarão apenas o bit PanScan.

O código de exemplo a seguir mostra como copiar o conteúdo **VIDEOINFOHEADER2** de um pino de entrada para um pino de saída.


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



 

 



