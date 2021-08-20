---
description: capturando vídeo em um arquivo de mídia Windows
ms.assetid: cc23bfce-34b9-4976-8602-e0602c7da2af
title: capturando vídeo em um arquivo de mídia Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3268d3a3df4a24c5836dba81f7ef4cf0b872907f09367d3212d27c38c0dd4414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158696"
---
# <a name="capturing-video-to-a-windows-media-file"></a>capturando vídeo em um arquivo de mídia Windows

para capturar vídeo e codificá-lo em um arquivo de vídeo de mídia Windows (WMV), conecte o pin de captura ao filtro de [gravador ASF do WM](wm-asf-writer-filter.md) , conforme mostrado no diagrama a seguir.

![Grafo de captura de mídia do Windows](images/vidcap03.png)

A maneira mais fácil de criar esse grafo é especificando MEDIASUBTYPE \_ ASF no método [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) :


```C++
IBaseFilter* pASFWriter = 0;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Asf,   // Create a Windows Media file.
    L"C:\\VidCap.wmv",   // File name.
    &pASFWriter,         // Receives a pointer to the filter.
    NULL);  // Receives an IFileSinkFilter interface pointer (optional).
```



o valor MEDIASUBTYPE \_ Asf informa ao construtor de Graph de captura para usar o filtro de gravador Asf do WM como o coletor de arquivos. o construtor de Graph de captura cria o filtro, adiciona-o ao grafo e chama [**IFileSinkFilter:: setfilename**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) para definir o nome do arquivo de saída. Ele retorna um ponteiro para o filtro como um parâmetro de saída (


```
pASFWriter
```



no exemplo anterior).

Use a interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) no gravador ASF do WM para definir o perfil de mídia Windows. Você deve fazer isso antes de conectar qualquer Pin no gravador ASF do WM.


```C++
IConfigAsfWriter *pConfig = 0;
hr = pASFWriter->QueryInterface(IID_IConfigAsfWriter, (void**)&pConfig);
if (SUCCEEDED(hr))
{
     // Configure the ASF Writer filter.
    pConfig->Release();
}
```



Para obter mais informações sobre como configurar o perfil, consulte [criando arquivos ASF no DirectShow](creating-asf-files-in-directshow.md).

Chame [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para conectar o filtro de captura ao gravador ASF:


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE,   // Capture pin.
    &MEDIATYPE_Video,        // Video. Use MEDIATYPE_Audio for audio.
    pCap,                    // Pointer to the capture filter. 
    0, 
    pASFWriter);             // Pointer to the sink filter (ASF Writer).
```



cada pin de entrada no filtro de gravador ASF do WM corresponde a um fluxo no perfil de mídia Windows. Você deve conectar cada PIN para que o conteúdo do arquivo corresponda ao perfil.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Capturando vídeo em um arquivo](capturing-video-to-a-file.md)
</dt> </dl>

 

 



