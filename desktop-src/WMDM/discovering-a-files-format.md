---
title: Descobrindo o formato de um arquivo
description: Descobrindo o formato de um arquivo
ms.assetid: f1b3f811-8161-41ca-a92c-2735c0bec2e8
keywords:
- Windows Gerenciador de Dispositivos de mídia, formatos de arquivo
- Gerenciador de Dispositivos, formatos de arquivo
- Guia de programação, formatos de arquivo
- aplicativos de área de trabalho, formatos de arquivo
- criando Windows aplicativos de Gerenciador de Dispositivos de mídia, formatos de arquivo
- gravando arquivos em dispositivos, formatos de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83706a3026968a694d3629551d310db9021b7f8c8118f3d98621751a95af26b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585325"
---
# <a name="discovering-a-files-format"></a>Descobrindo o formato de um arquivo

Antes de enviar um arquivo para o dispositivo, um aplicativo deve determinar se o dispositivo dá suporte a esse formato de arquivo.

Descobrir o formato de um arquivo pode ser complexo. A maneira mais simples é criar uma lista de extensões de arquivo mapeadas para \_ valores de enumeração WMDM FORMATCODE específicos. No entanto, há alguns problemas com esse sistema: um é que um único formato pode ter várias extensões (como .jpg,. jpe e. jpeg para imagens JPEG). Além disso, a mesma extensão de arquivo pode ser usada por programas diferentes para formatos diferentes.

Para superar as limitações de um mapeamento estrito, é melhor que um aplicativo Verifique se o formato corresponde à extensão. o SDK do DirectShow fornece ferramentas que permitem que um aplicativo descubra um conjunto limitado de detalhes sobre a maioria dos tipos de arquivo de mídia. o SDK do formato de mídia Windows expõe um grande número de detalhes, mas apenas sobre arquivos ASF. como todos os tipos de arquivo devem ter seu código de formato verificado se possível, é, portanto, melhor usar DirectShow para descobrir ou verificar o código de formato básico e usar o SDK do formato de mídia Windows para descobrir quaisquer metadados adicionais desejados sobre arquivos ASF. DirectShow também pode ser usado para descobrir metadados básicos para arquivos não ASF.

Veja a seguir uma maneira de descobrir um formato de arquivo usando mapeamento de extensão e DirectShow.

Primeiro, compare a extensão de nome de arquivo com uma lista de extensões conhecidas. Certifique-se de fazer a comparação não diferencia maiúsculas de minúsculas. Se a extensão não for mapeada, defina o formato como WMDM \_ FORMATCODE \_ undefined.

-   Se o código de formato não foi encontrado (ou se você deseja verificar se um arquivo é um arquivo de mídia), você pode executar as seguintes etapas:
    1.  crie um objeto de Detector de mídia DirectShow usando **CoCreateInstance**(CLSID \_ MediaDet) e recuperando a interface **IMediaDet** .
    2.  Abra o arquivo chamando **IMediaDet::p UT \_ filename**. Essa chamada falhará se o arquivo estiver protegido.
    3.  Obtenha o tipo de mídia do fluxo padrão chamando **IMediaDet:: get \_ StreamMediaType**, que retorna um **tipo de \_ mídia \_ am**.
    4.  Obtenha o número de fluxos chamando **IMediaDet:: get \_ OutputStreams**.
        -   Se houver apenas um fluxo e ele for áudio, o tipo de arquivo será WMDM \_ FORMATCODE \_ UNDEFINEDAUDIO
        -   Se houver apenas um fluxo e ele for vídeo, o tipo de arquivo será WMDM \_ FORMATCODE \_ UNDEFINEDVIDEO
        -   Se houver apenas um fluxo e ele for um vídeo e a taxa de bits for zero, o tipo de arquivo será WMDM \_ FORMATCODE \_ WINDOWSIMAGEFORMAT.

Você também pode tentar corresponder codecs de áudio ou vídeo dos membros **VIDEOINFOHEADER** ou **WAVEFORMATEX** recuperados de **Get \_ StreamMediaType**.

a função C++ a seguir demonstra a correspondência de extensão de arquivo e o uso de DirectShow para tentar analisar arquivos desconhecidos.


```C++
// For IMediaDet, you must link to strmiids.lib. Also include the following:
//#include <Qedit.h>  // for IMediaDet declaration.
//#include <Dshow.h>  // for VIDEOINFOHEADER declaration.
WMDM_FORMATCODE CWMDMController::myGetWMDM_FORMATCODE(LPCWSTR pFileName)
{
    HRESULT hr = S_OK;

    // Declare the variable to hold the WMDM format code.
    WMDM_FORMATCODE fmt = WMDM_FORMATCODE_UNDEFINED;
    
    // Get the file extension.
    wstring ext = pFileName;
    ext = ext.substr(ext.find_last_of(L".") + 1);

    // This is not an exhaustive list. 
    // It is also case-sensitive.
    if (ext == L"js" || ext == L"vb")
        fmt = WMDM_FORMATCODE_SCRIPT;
    else if (ext == L".exe")
        fmt = WMDM_FORMATCODE_EXECUTABLE;
    else if (ext == L"txt")
        fmt = WMDM_FORMATCODE_TEXT;
    else if (ext == L"html" || ext == L"htm" || ext == L"shtm")
        fmt = WMDM_FORMATCODE_HTML;
    else if (ext == L"aiff")
        fmt = WMDM_FORMATCODE_AIFF;
    else if (ext == L"wav")
        fmt = WMDM_FORMATCODE_WAVE;
    else if (ext == L"mp3")
        fmt = WMDM_FORMATCODE_MP3;
    else if (ext == L"mpg" || ext == L"mpeg" || ext == L"mp2")
        fmt = WMDM_FORMATCODE_MPEG;
    else if (ext == L"bmp")
        fmt = WMDM_FORMATCODE_IMAGE_BMP;
    else if (ext == L"avi")
        fmt = WMDM_FORMATCODE_AVI;
    else if (ext == L"asf")
        fmt = WMDM_FORMATCODE_ASF;
    else if (ext == L"tif")
        fmt = WMDM_FORMATCODE_IMAGE_TIFF;
    else if (ext == L"gif")
        fmt = WMDM_FORMATCODE_IMAGE_GIF;
    else if (ext == L"pct")
        fmt = WMDM_FORMATCODE_IMAGE_PICT;
    else if (ext == L"png")
        fmt = WMDM_FORMATCODE_IMAGE_PNG;
    else if (ext == L"wma")
        fmt = WMDM_FORMATCODE_WMA;
    else if (ext == L"wpl")
        fmt = WMDM_FORMATCODE_WPLPLAYLIST;
    else if (ext == L"asx")
        fmt = WMDM_FORMATCODE_ASXPLAYLIST;
    else if (ext == L"m3u")
        fmt = WMDM_FORMATCODE_M3UPLAYLIST;
    else if (ext == L"wmv")
        fmt = WMDM_FORMATCODE_WMV;
    else if (ext == L"jpg" || ext == L"jpeg" || ext == L"jpe")
        fmt = WMDM_FORMATCODE_IMAGE_EXIF;
    else if (ext == L"jp2")
        fmt = WMDM_FORMATCODE_IMAGE_JP2;
    else if (ext == L"jpx" || ext == L"jpf")
        fmt = WMDM_FORMATCODE_IMAGE_JPX;

    // If we couldn't get the type from the extension, perhaps DirectShow 
    // can determine the type. You could also modify this to verify that 
    // the major media type matches the file extension (for example, that 
    // a .gif file has a video image stream with a bit rate of zero).
    if (fmt == WMDM_FORMATCODE_UNDEFINED)
    {
        CComPtr<IMediaDet> pIMediaDet;
        hr = pIMediaDet.CoCreateInstance(CLSID_MediaDet, NULL);
        if (hr == S_OK && pIMediaDet != NULL)
        {
            hr = pIMediaDet->put_Filename(BSTR(pFileName));
            if (FAILED(hr)) return WMDM_FORMATCODE_UNDEFINED;

            AM_MEDIA_TYPE mediaType;
            if (hr == S_OK)
            {
                hr = pIMediaDet->get_StreamMediaType(&mediaType);
                CHECK_HR(hr, 
                  "get_StreamMediaType succeeded in myGetWMDM_FORMATCODE.", 
                  "get_StreamMediaType failed in myGetWMDM_FORMATCODE.");
            }

            if (hr == S_OK)
            {
                LONG numStreams = 0;
                hr = pIMediaDet->get_OutputStreams(&numStreams);

                // If there is at least one video stream, the file is video. 
                // If there are only audio streams, it is audio.
                // Loop through all streams or until first video stream is found.
                for (int i = 0; i < numStreams; i++)
                {
                    // Choices are either VIDEOINFOHEADER or WAVEFORMATEX. 
                    // VIDEOINFOHEADER2 is not supported.
                    if (IsEqualGUID(mediaType.formattype, 
                        FORMAT_VideoInfo))
                    {
                        VIDEOINFOHEADER* data = 
                            (VIDEOINFOHEADER*) mediaType.pbFormat;

                        // If only one stream and there was no matching 
                        // extension, it is undefined video. If no 
                        // bit rate, it's a still image.
                        if (data->dwBitRate == 0) fmt = 
                            WMDM_FORMATCODE_WINDOWSIMAGEFORMAT;
                        else fmt = WMDM_FORMATCODE_UNDEFINEDVIDEO;
                        break; // Found video--any additional streams are soundtracks.
                    }
                    if (IsEqualGUID(mediaType.formattype, FORMAT_WaveFormatEx))
                    {
                        // If only one stream and there was no matching 
                        // extension, it is undefined audio. 
                        if (fmt == WMDM_FORMATCODE_UNDEFINED)
                        {
                            fmt = WMDM_FORMATCODE_UNDEFINEDAUDIO;
                        }
                        WAVEFORMATEX* data = 
                            (WAVEFORMATEX*) mediaType.pbFormat;
                    }
                } // Loop through streams.
            }     // Got a stream media type.
        }         // Created a media detector object.
    }
    return fmt;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Gravando arquivos no dispositivo**](writing-files-to-the-device.md)
</dt> </dl>

 

 




