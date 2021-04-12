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
# <a name="capturing-video-to-a-windows-media-file"></a><span data-ttu-id="b91cd-103">Capturando vídeo em um arquivo de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="b91cd-103">Capturing Video to a Windows Media File</span></span>

<span data-ttu-id="b91cd-104">Para capturar vídeo e codificá-lo em um arquivo de vídeo do Windows Media (WMV), conecte o PIN de captura ao filtro de [gravador ASF do WM](wm-asf-writer-filter.md) , conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="b91cd-104">To capture video and encode it to a Windows Media Video (WMV) file, connect the capture pin to the [WM ASF Writer](wm-asf-writer-filter.md) filter, as shown in the following diagram.</span></span>

![Grafo de captura de mídia do Windows](images/vidcap03.png)

<span data-ttu-id="b91cd-106">A maneira mais fácil de criar esse grafo é especificando MEDIASUBTYPE \_ ASF no método [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) :</span><span class="sxs-lookup"><span data-stu-id="b91cd-106">The easiest way to build this graph is by specifing MEDIASUBTYPE\_Asf in the [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) method:</span></span>


```C++
IBaseFilter* pASFWriter = 0;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Asf,   // Create a Windows Media file.
    L"C:\\VidCap.wmv",   // File name.
    &pASFWriter,         // Receives a pointer to the filter.
    NULL);  // Receives an IFileSinkFilter interface pointer (optional).
```



<span data-ttu-id="b91cd-107">O valor MEDIASUBTYPE \_ ASF informa ao construtor de grafo de captura para usar o filtro de gravador ASF do WM como o coletor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="b91cd-107">The value MEDIASUBTYPE\_Asf tells the Capture Graph Builder to use the WM ASF Writer filter as the file sink.</span></span> <span data-ttu-id="b91cd-108">O construtor de grafo de captura cria o filtro, adiciona-o ao grafo e chama [**IFileSinkFilter:: SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) para definir o nome do arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="b91cd-108">The Capture Graph Builder creates the filter, adds it to the graph, and calls [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) to set the name of the output file.</span></span> <span data-ttu-id="b91cd-109">Ele retorna um ponteiro para o filtro como um parâmetro de saída (</span><span class="sxs-lookup"><span data-stu-id="b91cd-109">It returns a pointer to the filter as an outgoing parameter (</span></span>


```
pASFWriter
```



<span data-ttu-id="b91cd-110">no exemplo anterior).</span><span class="sxs-lookup"><span data-stu-id="b91cd-110">in the previous example).</span></span>

<span data-ttu-id="b91cd-111">Use a interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) no gravador ASF do WM para definir o perfil do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b91cd-111">Use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) interface on the WM ASF Writer to set the Windows Media profile.</span></span> <span data-ttu-id="b91cd-112">Você deve fazer isso antes de conectar qualquer Pin no gravador ASF do WM.</span><span class="sxs-lookup"><span data-stu-id="b91cd-112">You must do this before you connect any pins on the WM ASF Writer.</span></span>


```C++
IConfigAsfWriter *pConfig = 0;
hr = pASFWriter->QueryInterface(IID_IConfigAsfWriter, (void**)&pConfig);
if (SUCCEEDED(hr))
{
     // Configure the ASF Writer filter.
    pConfig->Release();
}
```



<span data-ttu-id="b91cd-113">Para obter mais informações sobre como configurar o perfil, consulte [criando arquivos ASF no DirectShow](creating-asf-files-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="b91cd-113">For more information about setting the profile, see [Creating ASF Files in DirectShow](creating-asf-files-in-directshow.md).</span></span>

<span data-ttu-id="b91cd-114">Chame [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para conectar o filtro de captura ao gravador ASF:</span><span class="sxs-lookup"><span data-stu-id="b91cd-114">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) to connect the capture filter to the ASF Writer:</span></span>


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE,   // Capture pin.
    &MEDIATYPE_Video,        // Video. Use MEDIATYPE_Audio for audio.
    pCap,                    // Pointer to the capture filter. 
    0, 
    pASFWriter);             // Pointer to the sink filter (ASF Writer).
```



<span data-ttu-id="b91cd-115">Cada PIN de entrada no filtro de gravador ASF do WM corresponde a um fluxo no perfil do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b91cd-115">Each input pin on the WM ASF Writer filter corresponds to a stream in the Windows Media profile.</span></span> <span data-ttu-id="b91cd-116">Você deve conectar cada PIN para que o conteúdo do arquivo corresponda ao perfil.</span><span class="sxs-lookup"><span data-stu-id="b91cd-116">You must connect every pin, so that the file content matches the profile.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b91cd-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b91cd-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b91cd-118">Capturando vídeo em um arquivo</span><span class="sxs-lookup"><span data-stu-id="b91cd-118">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



