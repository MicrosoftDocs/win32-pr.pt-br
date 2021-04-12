---
description: Capturando vídeo em um arquivo de mídia do Windows
ms.assetid: cc23bfce-34b9-4976-8602-e0602c7da2af
title: Capturando vídeo em um arquivo de mídia do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6442c1cf3751beac8d4eba751452d9573e9eede
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104172484"
---
# <a name="capturing-video-to-a-windows-media-file"></a>Capturando vídeo em um arquivo de mídia do Windows

Para capturar vídeo e codificá-lo em um arquivo de vídeo do Windows Media (WMV), conecte o PIN de captura ao filtro de [gravador ASF do WM](wm-asf-writer-filter.md) , conforme mostrado no diagrama a seguir.

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



O valor MEDIASUBTYPE \_ ASF informa ao construtor de grafo de captura para usar o filtro de gravador ASF do WM como o coletor de arquivos. O construtor de grafo de captura cria o filtro, adiciona-o ao grafo e chama [**IFileSinkFilter:: SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) para definir o nome do arquivo de saída. Ele retorna um ponteiro para o filtro como um parâmetro de saída (


```
pASFWriter
```



no exemplo anterior).

Use a interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) no gravador ASF do WM para definir o perfil do Windows Media. Você deve fazer isso antes de conectar qualquer Pin no gravador ASF do WM.


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



Cada PIN de entrada no filtro de gravador ASF do WM corresponde a um fluxo no perfil do Windows Media. Você deve conectar cada PIN para que o conteúdo do arquivo corresponda ao perfil.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Capturando vídeo em um arquivo](capturing-video-to-a-file.md)
</dt> </dl>

 

 



