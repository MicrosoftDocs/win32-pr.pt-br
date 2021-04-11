---
title: Obtendo recursos de formato por meio de IWMDMDevice
description: Obtendo recursos de formato em dispositivos que dão suporte apenas a IWMDMDevice
ms.assetid: bff079a1-d192-4e53-9b1d-9ad3b5dcca51
keywords:
- Windows Media Gerenciador de Dispositivos, recursos do dispositivo
- Gerenciador de Dispositivos, recursos do dispositivo
- Guia de programação, recursos do dispositivo
- aplicativos de desktop, recursos de dispositivo
- Criando aplicativos de Gerenciador de Dispositivos de mídia do Windows, recursos do dispositivo
- gravando arquivos em dispositivos, recursos do dispositivo
- Método IWMDMDevice
- Windows Media Gerenciador de Dispositivos, método IWMDMDevice
- Gerenciador de Dispositivos, método IWMDMDevice
- Guia de programação, método IWMDMDevice
- aplicativos de área de trabalho, método IWMDMDevice
- Criando aplicativos de Gerenciador de Dispositivos de mídia do Windows, método IWMDMDevice
- gravando arquivos em dispositivos, método IWMDMDevice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a923919611b40197b1deed30e781042e008ef41
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/27/2019
ms.locfileid: "104293628"
---
# <a name="getting-format-capabilities-through-iwmdmdevice"></a><span data-ttu-id="72b85-116">Obtendo recursos de formato por meio de IWMDMDevice</span><span class="sxs-lookup"><span data-stu-id="72b85-116">Getting format capabilities through IWMDMDevice</span></span>

<span data-ttu-id="72b85-117">O método recomendado para consultar um dispositivo para seus recursos de reprodução é [**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span><span class="sxs-lookup"><span data-stu-id="72b85-117">The recommended method for querying a device for its playback capabilities is [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span></span> <span data-ttu-id="72b85-118">No entanto, se um dispositivo não oferecer suporte a esse método, o aplicativo poderá chamar [**IWMDMDevice:: GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) para recuperar uma matriz de formatos de áudio com suporte como estruturas [**\_ WAVEFORMATEX**](-waveformatex.md) e formatos MIME como cadeias de caracteres do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72b85-118">However, if a device does not support this method, the application instead can call [**IWMDMDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) to retrieve an array of supported audio formats as [**\_WAVEFORMATEX**](-waveformatex.md) structures and MIME formats as strings from the device.</span></span>

<span data-ttu-id="72b85-119">As etapas a seguir mostram como um aplicativo pode usar esse método para consultar um dispositivo em busca de formatos com suporte:</span><span class="sxs-lookup"><span data-stu-id="72b85-119">The following steps show how an application can use this method to query a device for supported formats:</span></span>

1.  <span data-ttu-id="72b85-120">Chame **GetFormatSupport** para recuperar matrizes de formatos de áudio e MIME.</span><span class="sxs-lookup"><span data-stu-id="72b85-120">Call **GetFormatSupport** to retrieve arrays of both audio and mime formats.</span></span>
2.  <span data-ttu-id="72b85-121">Faça um loop pelos formatos de áudio recuperados e examine cada estrutura [**\_ WAVEFORMATEX**](-waveformatex.md) para tentar encontrar um formato de áudio aceitável</span><span class="sxs-lookup"><span data-stu-id="72b85-121">Loop through the retrieved audio formats and examine each [**\_WAVEFORMATEX**](-waveformatex.md) structure to try to find an acceptable audio format</span></span>
3.  <span data-ttu-id="72b85-122">Faça um loop pelas cadeias de caracteres de formato MIME recuperadas (se desejado) para localizar um tipo de arquivo aceitável.</span><span class="sxs-lookup"><span data-stu-id="72b85-122">Loop through the retrieved MIME format strings (if desired) to find an acceptable file type.</span></span> <span data-ttu-id="72b85-123">O SDK não define constantes para formatos MIME; Você deve usar os valores padrão do setor (que podem ser encontrados no site da iana.org).</span><span class="sxs-lookup"><span data-stu-id="72b85-123">The SDK does not define constants for MIME formats; you should use industry standard values (which can be found at the iana.org Web site).</span></span> <span data-ttu-id="72b85-124">Um dispositivo deve listar os tipos MIME específicos aos quais ele dá suporte.</span><span class="sxs-lookup"><span data-stu-id="72b85-124">A device should list the specific MIME types that it supports.</span></span>

<span data-ttu-id="72b85-125">O código C++ a seguir demonstra a recuperação de recursos de formato de um dispositivo, usando **GetFormatSupport**.</span><span class="sxs-lookup"><span data-stu-id="72b85-125">The following C++ code demonstrates retrieving format capabilities from a device, using **GetFormatSupport**.</span></span>


```C++
// Function to print out device caps for a device 
// that supports only IWMDMDevice.
void CWMDMController::GetCaps(IWMDMDevice* pDevice)
{
    HRESULT hr = S_OK;

    // Get all capabilities for audio and mime support.
    _WAVEFORMATEX* pAudioFormats;
    LPWSTR* pMimeFormats;
    UINT numAudioFormats = 0;
    UINT numMimeFormats = 0;
    hr = pDevice->GetFormatSupport(
        &pAudioFormats,
        &numAudioFormats,
        &pMimeFormats,
        &numMimeFormats);
    if (FAILED(hr)) return;

    // Print out audio format data.
    if (numAudioFormats > 0)
    {
        // TODO: Display a banner for the supported audio-format listing.
    }
    else
    {
        // TODO: Display a message indicating that no audio formats are supported.
    }
    for (int i = 0; i < numAudioFormats; i++)
    {
       // TODO: For each valid audio format, display the max channel, 
       // max samples/second, avg. bytes/sec, block alignment, and 
       // max bits/sample values.
    }

    // Print out MIME formats.
    if (numMimeFormats > 0)
        // TODO: Display a banner to precede the MIME format listing.
    else
        // TODO: Display a banner indicating that no MIME formats are supported.
    for (i = 0; i < numMimeFormats; i++)
    {
        // TODO: Display the specified MIME format.
    }
    return;
}
```



## <a name="related-topics"></a><span data-ttu-id="72b85-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="72b85-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72b85-127">**Descobrindo recursos de formato de dispositivo**</span><span class="sxs-lookup"><span data-stu-id="72b85-127">**Discovering Device Format Capabilities**</span></span>](discovering-device-format-capabilities.md)
</dt> <dt>

[<span data-ttu-id="72b85-128">**Obtendo recursos de formato em dispositivos que dão suporte a IWMDMDevice3**</span><span class="sxs-lookup"><span data-stu-id="72b85-128">**Getting Format Capabilities on Devices That Support IWMDMDevice3**</span></span>](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
</dt> </dl>

 

 




