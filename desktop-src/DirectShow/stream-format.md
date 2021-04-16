---
description: Formato do fluxo
ms.assetid: 7ed095f2-b541-4b99-8afc-9acba58081cd
title: Formato do fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75413c28f0871db0168e27685de49fd35b682224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779227"
---
# <a name="stream-format"></a><span data-ttu-id="c5061-103">Formato do fluxo</span><span class="sxs-lookup"><span data-stu-id="c5061-103">Stream Format</span></span>

<span data-ttu-id="c5061-104">O driver MSDV e o UVC podem produzir dois formatos de DV: áudio Intercalado ou vídeo somente.</span><span class="sxs-lookup"><span data-stu-id="c5061-104">Both the MSDV and the UVC driver can output two DV formats: interleaved audio-video, or video only.</span></span> <span data-ttu-id="c5061-105">Áudio Intercalado-vídeo é o formato original do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c5061-105">Interleaved audio-video is the original format from the device.</span></span> <span data-ttu-id="c5061-106">O formato somente de vídeo contém os mesmos dados, mas os exemplos são marcados como sem dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="c5061-106">The video-only format contains the same data, but the samples are marked as having no audio data.</span></span> <span data-ttu-id="c5061-107">O formato somente vídeo existe principalmente para compatibilidade com aplicativos que usam vídeo para Windows.</span><span class="sxs-lookup"><span data-stu-id="c5061-107">The video-only format exists mainly for compatibility with applications that use Video for Windows.</span></span> <span data-ttu-id="c5061-108">Para obter mais informações, consulte [tipos-1 vs. tipo-2 DV AVI files](type-1-vs--type-2-dv-avi-files.md).</span><span class="sxs-lookup"><span data-stu-id="c5061-108">For more information, see [Type-1 vs. Type-2 DV AVI Files](type-1-vs--type-2-dv-avi-files.md).</span></span>

<span data-ttu-id="c5061-109">**Driver MSDV**</span><span class="sxs-lookup"><span data-stu-id="c5061-109">**MSDV Driver**</span></span>

<span data-ttu-id="c5061-110">O driver MSDV tem dois pinos de saída.</span><span class="sxs-lookup"><span data-stu-id="c5061-110">The MSDV driver has two output pins.</span></span> <span data-ttu-id="c5061-111">O primeiro pino de saída envia dados intercalados e o segundo PIN de saída envia dados somente de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c5061-111">The first output pin sends interleaved data, and the second output pin sends video-only data.</span></span> <span data-ttu-id="c5061-112">Somente um PIN de saída pode ser conectado por vez.</span><span class="sxs-lookup"><span data-stu-id="c5061-112">Only one output pin can be connected at a time.</span></span> <span data-ttu-id="c5061-113">Para selecionar um formato, conecte o PIN de saída apropriado.</span><span class="sxs-lookup"><span data-stu-id="c5061-113">To select a format, connect the appropriate output pin.</span></span> <span data-ttu-id="c5061-114">Você pode usar a interface [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) no pino de saída para localizar o formato.</span><span class="sxs-lookup"><span data-stu-id="c5061-114">You can use the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface on the output pin to find the format.</span></span>

<span data-ttu-id="c5061-115">**Driver UVC**</span><span class="sxs-lookup"><span data-stu-id="c5061-115">**UVC Driver**</span></span>

<span data-ttu-id="c5061-116">Ao contrário do driver MSDV, o driver UVC fornece os dois formatos do mesmo PIN.</span><span class="sxs-lookup"><span data-stu-id="c5061-116">Unlike the MSDV driver, the UVC driver delivers both formats from the same pin.</span></span> <span data-ttu-id="c5061-117">O formato padrão é somente vídeo.</span><span class="sxs-lookup"><span data-stu-id="c5061-117">The default format is video-only.</span></span> <span data-ttu-id="c5061-118">Para selecionar o formato, use a interface **IAMStreamConfig** no pino de saída.</span><span class="sxs-lookup"><span data-stu-id="c5061-118">To select the format, use the **IAMStreamConfig** interface on the output pin.</span></span> <span data-ttu-id="c5061-119">Chame o método **GetStreamCaps** para enumerar os tipos de mídia no pino de saída.</span><span class="sxs-lookup"><span data-stu-id="c5061-119">Call the **GetStreamCaps** method to enumerate the media types on the output pin.</span></span> <span data-ttu-id="c5061-120">Para cada tipo de mídia, se o tipo principal corresponder ao formato desejado, chame **SetFormat** e transmita esse tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="c5061-120">For each media type, if the major type matches the desired format, call **SetFormat** and pass in that media type.</span></span>



| <span data-ttu-id="c5061-121">Formatar</span><span class="sxs-lookup"><span data-stu-id="c5061-121">Format</span></span>                      | <span data-ttu-id="c5061-122">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="c5061-122">Major type</span></span>             |
|-----------------------------|------------------------|
| <span data-ttu-id="c5061-123">Áudio e vídeo intercalados</span><span class="sxs-lookup"><span data-stu-id="c5061-123">Interleaved audio and video</span></span> | <span data-ttu-id="c5061-124">MEDIATYPE \_ intercalado</span><span class="sxs-lookup"><span data-stu-id="c5061-124">MEDIATYPE\_Interleaved</span></span> |
| <span data-ttu-id="c5061-125">Somente vídeo</span><span class="sxs-lookup"><span data-stu-id="c5061-125">Video only</span></span>                  | <span data-ttu-id="c5061-126">Vídeo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="c5061-126">MEDIATYPE\_Video</span></span>       |



 

<span data-ttu-id="c5061-127">A função a seguir define o formato com base no GUID de tipo principal.</span><span class="sxs-lookup"><span data-stu-id="c5061-127">The following function sets the format based on the major type GUID.</span></span>


```C++
HRESULT SetStreamFormat(IAMStreamConfig *pConfig, const GUID& majorType)
{
    if (pConfig == NULL)
    {
        return E_POINTER;
    }

    // Get the number of stream capabilities.
    int count = 0, size = 0;
    HRESULT hr = pConfig->GetNumberOfCapabilities(&count, &size);
    if (FAILED(hr))
    {
        return hr;
    }

    // Allocate memory for the stream capabilities structure.
    BYTE *pCaps = new BYTE[size];
    if (pCaps == NULL)
    {
        return E_OUTOFMEMORY;
    }
    
    // Enumerate the stream capabilities.
    bool bFoundType = false;
    for (int ix = 0; ix < count; ix++)
    {
        AM_MEDIA_TYPE *pmt;
        hr = pConfig->GetStreamCaps(ix, &pmt, pCaps);
        if (FAILED(hr))
        {
            break;
        }
        else if (pmt->majortype == majorType)
        {
            // This is the media type we want.
            bFoundType = true;
            hr = pConfig->SetFormat(pmt);
            DeleteMediaType(pmt);
            break;
        }
        DeleteMediaType(pmt);
    }
    delete [] pCaps;
    if (FAILED(hr))
    {
        return hr;
    }
    return bFoundType ? S_OK : E_FAIL;
}
```



<span data-ttu-id="c5061-128">O driver MSDV também dá suporte a **IAMStreamConfig**, para que você possa escrever código que funcione para ambos os tipos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c5061-128">The MSDV driver also supports **IAMStreamConfig**, so you can write code that works for both device types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5061-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c5061-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5061-130">Controlando uma camcorder DV</span><span class="sxs-lookup"><span data-stu-id="c5061-130">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



