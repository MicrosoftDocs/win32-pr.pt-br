---
description: Configurar o formato de saída de vídeo
ms.assetid: 1969072e-575e-49b4-88db-4c7e7a5a1c37
title: Configurar o formato de saída de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d09ac64d7f43e6c39377277544867491a93a6f3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104555916"
---
# <a name="configure-the-video-output-format"></a>Configurar o formato de saída de vídeo

> [!Note]  
> A funcionalidade descrita neste tópico foi preterida. Para configurar o formato de saída do dispositivo de captura, um aplicativo deve usar a estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) retornada por [**IAMStreamConfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) no parâmetro *PGTO* .

 

Um dispositivo de captura pode dar suporte a um intervalo de formatos de saída. Por exemplo, um dispositivo pode dar suporte a RGB de 16 bits, a RGB de 32 bits e a YUYV. Dentro de cada um desses formatos, o dispositivo pode dar suporte a um intervalo de tamanhos de quadros.

Em um dispositivo WDM, a interface [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) é usada para relatar quais formatos são compatíveis com o dispositivo e para definir o formato. (Para dispositivos VFW herdados, use a caixa de diálogo VFW do formato de vídeo, conforme descrito em [exibir caixas de diálogo de captura do VFW](display-vfw-capture-dialog-boxes.md).) A interface **IAMStreamConfig** é exposta no PIN de captura do filtro de captura, no PIN de visualização ou em ambos. Use o método [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) para obter o ponteiro de interface:


```C++
IAMStreamConfig *pConfig = NULL;
hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, // Preview pin.
    0,    // Any media type.
    pCap, // Pointer to the capture filter.
    IID_IAMStreamConfig, (void**)&pConfig);
```



O dispositivo tem uma lista de tipos de mídia com suporte. Para cada tipo de mídia, o dispositivo também fornece um conjunto de recursos. Isso inclui o intervalo de tamanhos de quadro que estão disponíveis para esse formato, quão bem o dispositivo pode alongar ou reduzir a imagem e o intervalo de taxas de quadros.

Para obter o número de tipos de mídia, chame o método [**IAMStreamConfig:: GetNumberOfCapabilities**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getnumberofcapabilities) . O método retorna dois valores:

-   O número de tipos de mídia.
-   O tamanho da estrutura que contém as informações de recursos.

O valor de tamanho é necessário porque a interface [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) é usada para áudio e vídeo (e pode ser estendida para outros tipos de mídia). Para vídeo, os recursos são descritos usando a [**estrutura \_ \_ \_ Caps de configuração do fluxo de vídeo**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) , enquanto o áudio usa a estrutura [**\_ \_ \_ Caps de configuração do fluxo de áudio**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) .

Para enumerar os tipos de mídia, chame o método [**IAMStreamConfig:: GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) com um índice de base zero. O método **GetStreamCaps** retorna um tipo de mídia e a estrutura de recursos correspondente:


```C++
int iCount = 0, iSize = 0;
hr = pConfig->GetNumberOfCapabilities(&iCount, &iSize);

// Check the size to make sure we pass in the correct structure.
if (iSize == sizeof(VIDEO_STREAM_CONFIG_CAPS))
{
    // Use the video capabilities structure.

    for (int iFormat = 0; iFormat < iCount; iFormat++)
    {
        VIDEO_STREAM_CONFIG_CAPS scc;
        AM_MEDIA_TYPE *pmtConfig;
        hr = pConfig->GetStreamCaps(iFormat, &pmtConfig, (BYTE*)&scc);
        if (SUCCEEDED(hr))
        {
            /* Examine the format, and possibly use it. */

            // Delete the media type when you are done.
            DeleteMediaType(pmtConfig);
        }
}
```



Observe como as estruturas são alocadas para o método [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) . O método aloca a estrutura do tipo de mídia, enquanto o chamador aloca a estrutura de recursos. Forçar a estrutura de recursos para um ponteiro de matriz de bytes. Depois de concluir o tipo de mídia, exclua a estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) , juntamente com o bloco de formato do tipo de mídia.

Você pode configurar o dispositivo para usar um formato retornado no método [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) . Basta chamar [**IAMStreamConfig:: SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) com o tipo de mídia:


```C++
hr = pConfig->SetFormat(pmtConfig);
```



Se o PIN não estiver conectado, ele tentará usar esse formato quando ele se conectar. Se o PIN já estiver conectado, ele tentará se reconectar usando o novo formato. Em ambos os casos, é possível que o filtro downstream rejeite o formato.

Você também pode modificar o tipo de mídia antes de passá-lo para o método [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) . É aí que entra a estrutura de [**limites de configuração do fluxo de vídeo \_ \_ \_**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) . Ele descreve todas as maneiras válidas de alterar o tipo de mídia. Para usar essas informações, você deve entender os detalhes desse tipo de mídia específico.

Por exemplo, suponha que [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) retorne um formato RGB de 24 bits, com um tamanho de quadro de 320 x 240 pixels. Você pode obter essas informações examinando o tipo principal, subtipo e bloco de formato do tipo de mídia:


```C++
if ((pmtConfig.majortype == MEDIATYPE_Video) &&
    (pmtConfig.subtype == MEDIASUBTYPE_RGB24) &&
    (pmtConfig.formattype == FORMAT_VideoInfo) &&
    (pmtConfig.cbFormat >= sizeof (VIDEOINFOHEADER)) &&
    (pmtConfig.pbFormat != NULL))
{
    VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)pmtConfig.pbFormat;
    // pVih contains the detailed format information.
    LONG lWidth = pVih->bmiHeader.biWidth;
    LONG lHeight = pVih->bmiHeader.biHeight;
}
```



A estrutura de [**configuração de fluxo de vídeo em \_ \_ \_ maiúsculas**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) fornece a largura e a altura mínima e máxima que podem ser usadas para esse tipo de mídia. Ele também fornece o tamanho da "etapa", que define os incrementos pelos quais é possível ajustar a largura ou a altura. Por exemplo, o dispositivo pode retornar o seguinte:

-   MinOutputSize: 160 x 120
-   MaxOutputSize: 320 x 240
-   OutputGranularityX: 8 pixels (tamanho da etapa horizontal)
-   OutputGranularityY: 8 pixels (tamanho da etapa vertical)

Considerando esses números, você pode definir a largura como qualquer coisa no intervalo (160, 168, 176,... 304, 312, 320) e a altura para qualquer coisa no intervalo (120, 128, 136,... 104, 112, 120). O diagrama a seguir ilustra esse processo.

![tamanhos de formato de vídeo](images/strmcap3.png)

Para definir um novo tamanho de quadro, modifique diretamente a estrutura [**am \_ Media \_ Type**](/windows/win32/api/strmif/ns-strmif-am_media_type) retornada em [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps):


```C++
pVih->bmiHeader.biWidth = 160;
pVih->bmiHeader.biHeight = 120;
pVih->bmiHeader.biSizeImage = DIBSIZE(pVih->bmiHeader);
```



Em seguida, passe o tipo de mídia para o método [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) , conforme descrito anteriormente.

Os membros **MinFrameInterval** e **MaxFrameInterval** das [**\_ \_ \_ tampas de configuração de fluxo de vídeo**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) são o comprimento mínimo e máximo de cada quadro de vídeo, que pode ser convertido em taxas de quadros da seguinte maneira:

`frames per second = 10,000,000 / frame duration`

Para solicitar uma taxa de quadros específica, modifique o valor de **AvgTimePerFrame** na estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) ou [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) no tipo de mídia. O dispositivo pode não dar suporte a todos os valores possíveis entre o mínimo e o máximo, portanto, o driver usará o valor mais próximo possível. Para ver qual valor o driver realmente usou, chame [**IAMStreamConfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) depois de chamar [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat).

Alguns drivers podem relatar **MAXLONGLONG** (0x7FFFFFFFFFFFFFFF) para o valor de **MaxFrameInterval**, o que, em vigor, significa que não há duração máxima. No entanto, talvez você queira impor uma taxa de quadros mínima em seu aplicativo, como 1 fps.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre os tipos de mídia](about-media-types.md)
</dt> <dt>

[Configurando um dispositivo de captura de vídeo](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



