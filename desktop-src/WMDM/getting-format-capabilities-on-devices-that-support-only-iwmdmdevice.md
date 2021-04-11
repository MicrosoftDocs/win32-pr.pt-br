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
# <a name="getting-format-capabilities-through-iwmdmdevice"></a>Obtendo recursos de formato por meio de IWMDMDevice

O método recomendado para consultar um dispositivo para seus recursos de reprodução é [**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability). No entanto, se um dispositivo não oferecer suporte a esse método, o aplicativo poderá chamar [**IWMDMDevice:: GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) para recuperar uma matriz de formatos de áudio com suporte como estruturas [**\_ WAVEFORMATEX**](-waveformatex.md) e formatos MIME como cadeias de caracteres do dispositivo.

As etapas a seguir mostram como um aplicativo pode usar esse método para consultar um dispositivo em busca de formatos com suporte:

1.  Chame **GetFormatSupport** para recuperar matrizes de formatos de áudio e MIME.
2.  Faça um loop pelos formatos de áudio recuperados e examine cada estrutura [**\_ WAVEFORMATEX**](-waveformatex.md) para tentar encontrar um formato de áudio aceitável
3.  Faça um loop pelas cadeias de caracteres de formato MIME recuperadas (se desejado) para localizar um tipo de arquivo aceitável. O SDK não define constantes para formatos MIME; Você deve usar os valores padrão do setor (que podem ser encontrados no site da iana.org). Um dispositivo deve listar os tipos MIME específicos aos quais ele dá suporte.

O código C++ a seguir demonstra a recuperação de recursos de formato de um dispositivo, usando **GetFormatSupport**.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Descobrindo recursos de formato de dispositivo**](discovering-device-format-capabilities.md)
</dt> <dt>

[**Obtendo recursos de formato em dispositivos que dão suporte a IWMDMDevice3**](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
</dt> </dl>

 

 




