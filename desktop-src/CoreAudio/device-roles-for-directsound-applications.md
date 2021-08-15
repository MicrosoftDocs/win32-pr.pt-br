---
description: Funções de dispositivo para aplicativos DirectSound
ms.assetid: 7d82d67f-aad8-4e5b-ac65-87d75774e613
title: Funções de dispositivo para aplicativos DirectSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3037b767d7ddfb96d892c789608f23523efed465535258c336496f3f23d82f19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957325"
---
# <a name="device-roles-for-directsound-applications"></a>Funções de dispositivo para aplicativos DirectSound

> [!Note]  
> A [API MMDevice](mmdevice-api.md) dá suporte a funções de dispositivo. no entanto, a interface do usuário no Windows Vista não implementa o suporte para esse recurso. O suporte da interface do usuário para funções de dispositivo pode ser implementado em uma versão futura do Windows. para obter mais informações, consulte [funções de dispositivo no Windows Vista](device-roles-in-windows-vista.md).

 

A API do DirectSound não fornece um meio para um aplicativo selecionar o [dispositivo de ponto de extremidade de áudio](audio-endpoint-devices.md) que o usuário atribuiu a uma função de [dispositivo](device-roles.md)específica. no entanto, no Windows Vista, as APIs de áudio principais podem ser usadas em conjunto com um aplicativo DirectSound para habilitar a seleção de dispositivos com base na função do dispositivo. Com a ajuda das principais APIs de áudio, o aplicativo pode identificar o dispositivo de ponto de extremidade de áudio atribuído a uma função específica, obter o GUID do dispositivo DirectSound para o dispositivo de ponto de extremidade e chamar a função **DirectSoundCreate** ou **DirectSoundCaptureCreate** para criar uma instância de interface **IDirectSound** ou **IDirectSoundCapture** que encapsula o dispositivo de ponto de extremidade. para obter mais informações sobre o DirectSound, consulte a documentação do SDK do Windows.

O exemplo de código a seguir mostra como obter o GUID do dispositivo DirectSound para o dispositivo de renderização ou de captura que está atualmente atribuído a uma função de dispositivo específica:


```C++
//-----------------------------------------------------------
// Get the DirectSound or DirectSoundCapture device GUID for
// an audio endpoint device. If flow = eRender, the function
// gets the DirectSound device GUID for the rendering device
// with the specified device role. If flow = eCapture, the
// function gets the DirectSoundCapture device GUID for the
// capture device with the specified device role.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

HRESULT GetDirectSoundGuid(EDataFlow flow, ERole role, GUID* pDevGuid)
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IPropertyStore *pProps = NULL;

    PROPVARIANT var;
    PropVariantInit(&var);

    if (pDevGuid == NULL)
    {
        return E_POINTER;
    }

    // Get a device enumerator for the audio endpoint
    // devices in the system.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get the endpoint device with the specified dataflow
    // direction (eRender or eCapture) and device role.
    hr = pEnumerator->GetDefaultAudioEndpoint(flow, role,
                                              &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->OpenPropertyStore(STGM_READ, &pProps);
    EXIT_ON_ERROR(hr)

    // Get the DirectSound or DirectSoundCapture device GUID
    // (in WCHAR string format) for the endpoint device.
    hr = pProps->GetValue(PKEY_AudioEndpoint_GUID, &var);
    EXIT_ON_ERROR(hr)

    // Convert the WCHAR string to a GUID structure.
    hr = CLSIDFromString(var.pwszVal, pDevGuid);
    EXIT_ON_ERROR(hr)

Exit:
    PropVariantClear(&var);
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);
    SAFE_RELEASE(pProps);
    return hr;
}
```



No exemplo de código anterior, a função GetDirectSoundGuid aceita uma direção de fluxo de dados (eRender ou eCapture) e uma função de dispositivo (eConsole, eMultimedia ou eCommunications) como parâmetros de entrada. O terceiro parâmetro é um ponteiro pelo qual a função grava um GUID de dispositivo que o aplicativo pode fornecer como um parâmetro de entrada para a função **DirectSoundCreate** ou **DirectSoundCaptureCreate** .

O exemplo de código anterior Obtém o GUID do dispositivo DirectSound por:

-   Criar uma instância de interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) que representa o dispositivo de ponto de extremidade de áudio que tem a direção de fluxo de dados e a função de dispositivo especificadas.
-   Abrindo o repositório de propriedades do dispositivo de ponto de extremidade de áudio.
-   Obtendo a propriedade [**PKEY \_ AudioEndpoint \_ GUID**](pkey-audioendpoint-guid.md) do repositório de propriedades. O valor da propriedade é uma representação de cadeia de caracteres do GUID do dispositivo DirectSound para o dispositivo de ponto de extremidade de áudio.
-   Chamar a função [**CLSIDFromString**](https://www.bing.com/search?q=**CLSIDFromString**) para converter a representação da cadeia de caracteres do GUID do dispositivo em uma estrutura de GUID. para obter mais informações sobre o **CLSIDFromString**, consulte a documentação do SDK do Windows.

Depois de obter um GUID de dispositivo da função GetDirectSoundGuid, o aplicativo pode chamar **DirectSoundCreate** ou **DIRECTSOUNDCAPTURECREATE** com esse GUID para criar o dispositivo de captura ou a renderização do DirectSound que encapsula o dispositivo de ponto de extremidade de áudio. Quando o DirectSound cria um dispositivo dessa forma, ele sempre atribui o fluxo de áudio do dispositivo à sessão padrão — a sessão de áudio específica do processo que é identificada pelo valor GUID da sessão GUID \_ NULL.

Se o aplicativo exigir que o DirectSound atribua o fluxo a uma sessão de áudio de processo cruzado ou a uma sessão com um GUID de sessão não **nulo** , ele deverá chamar o método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) para criar um objeto **IDirectSound** ou **IDirectSoundCapture** em vez de usar a técnica mostrada no exemplo de código anterior. para obter um exemplo de código que mostra como usar o método **Activate** para especificar uma sessão de áudio de processo cruzado ou um GUID de sessão não **nulo** para um fluxo, consulte [funções de dispositivo para aplicativos DirectShow](device-roles-for-directshow-applications.md). o exemplo de código nessa seção mostra como criar um filtro de DirectShow, mas, com pequenas modificações, o código pode ser adaptado para criar um dispositivo DirectSound.

A função GetDirectSoundGuid no exemplo de código anterior chama a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar um enumerador para os dispositivos de ponto de extremidade de áudio no sistema. A menos que o programa de chamada chamou anteriormente a função [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar a biblioteca com, a chamada **CoCreateInstance** falhará. para obter mais informações sobre **CoCreateInstance**, **coinitialize** e **CoInitializeEx**, consulte a documentação do SDK do Windows.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interoperabilidade com APIs de áudio herdadas](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
