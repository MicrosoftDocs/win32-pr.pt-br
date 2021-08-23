---
description: Saiba mais sobre os tipos de mídia DirectShow. O tipo de mídia é uma maneira universal e extensível de descrever formatos de mídia digital.
ms.assetid: 9984ba36-4e43-4886-a073-34b330274c9c
title: Sobre tipos de mídia (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fa3034581e443472f1b73c0bc42ca7b8b532a18120df3e067b02ad16f37930e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074890"
---
# <a name="about-media-types-directshow"></a>Sobre tipos de mídia (DirectShow)

Como DirectShow é modular, ele requer uma maneira de descrever o formato dos dados em cada ponto no grafo de filtro. Por exemplo, considere a reprodução DE AVI. Os dados entram no grafo como um fluxo de partes DE VALOR. Eles são analisados em fluxos de áudio e vídeo. O fluxo de vídeo consiste em quadros de vídeo, que provavelmente são compactados. Após a decodificação, o fluxo de vídeo é uma série de bitmaps descompactados. O fluxo de áudio passa por um processo semelhante.

Tipos de mídia: como DirectShow representa formatos

O *tipo de mídia* é uma maneira universal e extensível de descrever formatos de mídia digital. Quando dois filtros se conectam, eles concordam com um tipo de mídia. O tipo de mídia identifica que tipo de dados o filtro upstream fornecerá ao filtro downstream e o layout físico dos dados. Se dois filtros não puderem concordar com um tipo de mídia, eles não se conectarão.

Para alguns aplicativos, você nunca terá que se preocupar com tipos de mídia. Na reprodução de arquivo, por exemplo, DirectShow lida com todos os detalhes. Outros tipos de aplicativos podem precisar trabalhar diretamente com tipos de mídia.

Os tipos de mídia são definidos usando a [**estrutura AM \_ MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) Essa estrutura contém as seguintes informações:

-   **Tipo principal:** o tipo principal é um GUID que define a categoria geral dos dados. Os principais tipos incluem vídeo, áudio, fluxo de byte não esparso, dados MIDI e assim por diante.
-   **Subtipo**: o subtipo é outro GUID, que define ainda mais o formato. Por exemplo, dentro do tipo principal de vídeo, há subtipos para RGB-24, RGB-32, UYVY e assim por diante. No áudio, há áudio PCM, conteúdo MPEG-1 e outros. O subtipo fornece mais informações do que o tipo principal, mas não define tudo sobre o formato. Por exemplo, subtipos de vídeo não definem o tamanho da imagem ou a taxa de quadros. Elas são definidas pelo bloco de formato, descrito abaixo.
-   **Bloco de** formato: o bloco de formato é um bloco de dados que descreve o formato em detalhes. O bloco de formato é alocado separadamente da estrutura [**AM \_ MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) O **membro pbFormat** da estrutura **AM MEDIA \_ \_ TYPE** aponta para o bloco de formato.

    O **membro pbFormat** é digitado **\* void* _ porque o layout do bloco de formato muda dependendo do tipo de mídia. Por exemplo, o áudio PCM usa uma [estrutura _ *WAVEFORMATEX.* *](/previous-versions/dd757713(v=vs.85)) O vídeo usa várias estruturas, incluindo [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) [**e VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) O **membro formattype** da estrutura [**AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) é um GUID que especifica qual estrutura está contida no bloco de formato. Cada estrutura de formato recebe um GUID. O **membro cbFormat** especifica o tamanho do bloco de formato. Sempre verifique esses valores antes de desreferenciar o **ponteiro pbFormat.**

Se o bloco de formato for preenchido, o tipo principal e o subtipo conterão informações redundantes. No entanto, o tipo principal e o subtipo fornecem uma maneira conveniente de identificar formatos sem um bloco de formato completo. Por exemplo, você pode especificar um formato RGB genérico de 24 bits (MEDIASUBTYPE RGB24), sem saber todas as informações exigidas pela estrutura \_ [**VIDEOINFOHEADER,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) como o tamanho da imagem e a taxa de quadros.

Por exemplo, um filtro pode usar o seguinte código para verificar um tipo de mídia:


```C++
HRESULT CheckMediaType(AM_MEDIA_TYPE *pmt)
{
    if (pmt == NULL) return E_POINTER;

    // Check the major type. We're looking for video.
    if (pmt->majortype != MEDIATYPE_Video)
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the subtype. We're looking for 24-bit RGB.
    if (pmt->subtype != MEDIASUBTYPE_RGB24)
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the format type and the size of the format block.
    if ((pmt->formattype == FORMAT_VideoInfo) &&
         (pmt->cbFormat >= sizeof(VIDEOINFOHEADER) &&
         (pmt->pbFormat != NULL))
    {
        // Now it's safe to coerce the format block pointer to the
        // correct structure, as defined by the formattype GUID.
        VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    
        // Examine pVIH (not shown). If it looks OK, return S_OK.
        return S_OK;
    }

    return VFW_E_INVALIDMEDIATYPE;
}
```



A [**estrutura AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) também contém alguns campos opcionais. Eles podem ser usados para fornecer informações adicionais, mas os filtros não são necessários para usá-los:

-   **lSampleSize**. Se esse campo for não zero, ele definirá o tamanho de cada amostra. Se for zero, isso indicará que o tamanho da amostra pode mudar de exemplo para exemplo.
-   **bFixedSizeSamples.** Se esse sinalizador booliana **for TRUE,** isso significa que o valor em **lSampleSize** é válido. Caso contrário, você deve ignorar **lSampleSize**.
-   **bTemporalCompression**. Se esse sinalizador booliana for **FALSE,** isso significa que todos os quadros são quadros-chave.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O filtro Graph e seus componentes](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 
