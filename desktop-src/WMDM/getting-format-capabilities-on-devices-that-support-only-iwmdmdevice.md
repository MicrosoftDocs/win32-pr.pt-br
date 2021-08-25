---
title: Obter recursos de formato por meio de IWMDMDevice
description: Obter recursos de formato em dispositivos que só suportam IWMDMDevice
ms.assetid: bff079a1-d192-4e53-9b1d-9ad3b5dcca51
keywords:
- Windows Recursos Gerenciador de Dispositivos mídia, funcionalidades do dispositivo
- Gerenciador de Dispositivos,funcionalidades do dispositivo
- guia de programação, funcionalidades do dispositivo
- aplicativos da área de trabalho, funcionalidades do dispositivo
- criando Windows mídia Gerenciador de Dispositivos aplicativos, funcionalidades do dispositivo
- escrevendo arquivos em dispositivos, funcionalidades de dispositivo
- Método IWMDMDevice
- Windows Media Gerenciador de Dispositivos, método IWMDMDevice
- Gerenciador de Dispositivos,método IWMDMDevice
- guia de programação, método IWMDMDevice
- aplicativos da área de trabalho, método IWMDMDevice
- criando Windows mídia Gerenciador de Dispositivos aplicativos, método IWMDMDevice
- escrevendo arquivos em dispositivos, método IWMDMDevice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3fe71969b48ded5616ee34e90a3420a77f468dfd9fb7f2cf0c6d14168a6fbb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957517"
---
# <a name="getting-format-capabilities-through-iwmdmdevice"></a>Obter recursos de formato por meio de IWMDMDevice

O método recomendado para consultar um dispositivo para seus recursos de reprodução é [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability). No entanto, se um dispositivo não dá suporte a esse método, o aplicativo pode chamar [**IWMDMDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) para recuperar uma matriz de formatos de áudio com suporte como estruturas [**\_ WAVEFORMATEX**](-waveformatex.md) e formatos MIME como cadeias de caracteres do dispositivo.

As etapas a seguir mostram como um aplicativo pode usar esse método para consultar um dispositivo em busca de formatos com suporte:

1.  Chame **GetFormatSupport** para recuperar matrizes de formatos de áudio e mime.
2.  Loop pelos formatos de áudio recuperados e examine cada estrutura [**\_ WAVEFORMATEX**](-waveformatex.md) para tentar encontrar um formato de áudio aceitável
3.  Loop pelas cadeias de caracteres de formato MIME recuperadas (se desejado) para encontrar um tipo de arquivo aceitável. O SDK não define constantes para formatos MIME; você deve usar valores padrão do setor (que podem ser encontrados no site iana.org Web). Um dispositivo deve listar os tipos MIME específicos aos quais ele dá suporte.

O código C++ a seguir demonstra a recuperação de funcionalidades de formato de um dispositivo, usando **GetFormatSupport**.


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

[**Descoberta de funcionalidades de formato de dispositivo**](discovering-device-format-capabilities.md)
</dt> <dt>

[**Obter recursos de formato em dispositivos que suportam IWMDMDevice3**](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
</dt> </dl>

 

 




