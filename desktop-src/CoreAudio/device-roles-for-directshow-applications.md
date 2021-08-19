---
description: funções de dispositivo para aplicativos DirectShow
ms.assetid: 54f42bda-b4a0-465c-9ce6-9102d2908776
title: funções de dispositivo para aplicativos DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e22a86e5537f11b6b4153753841a2682b5ac77a043a3fa74538714a2540377
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957355"
---
# <a name="device-roles-for-directshow-applications"></a>funções de dispositivo para aplicativos DirectShow

> [!Note]  
> A [API MMDevice](mmdevice-api.md) dá suporte a funções de dispositivo. no entanto, a interface do usuário no Windows Vista não implementa o suporte para esse recurso. O suporte da interface do usuário para funções de dispositivo pode ser implementado em uma versão futura do Windows. para obter mais informações, consulte [funções de dispositivo no Windows Vista](device-roles-in-windows-vista.md).

 

a API DirectShow não fornece um meio para um aplicativo selecionar o dispositivo de [ponto de extremidade de áudio](audio-endpoint-devices.md) atribuído a uma [função de dispositivo](device-roles.md)específica. no entanto, no Windows Vista, as APIs de áudio principais podem ser usadas em conjunto com um aplicativo DirectShow para habilitar a seleção de dispositivos com base na função do dispositivo. Com a ajuda das principais APIs de áudio, o aplicativo pode:

-   Identifique o dispositivo de ponto de extremidade de áudio que o usuário atribuiu a uma função de dispositivo específica.
-   crie um filtro de renderização de áudio DirectShow com uma interface [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) que encapsula o dispositivo de ponto de extremidade de áudio.
-   crie um grafo DirectShow que incorpore o filtro.

para obter mais informações sobre DirectShow e [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter), consulte a documentação do SDK do Windows.

o exemplo de código a seguir mostra como criar um DirectShow filtro de renderização de áudio que encapsula o dispositivo de ponto de extremidade de renderização atribuído a uma função de dispositivo específica:


```C++
//-----------------------------------------------------------
// Create a DirectShow audio rendering filter that
// encapsulates the audio endpoint device that is currently
// assigned to the specified device role.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

// This application's audio session GUID
const GUID guidAudioSessionId = {
    0xb13ff52e, 0xa5cf, 0x4fca,
    {0x9f, 0xc3, 0x42, 0x26, 0x5b, 0x0b, 0x14, 0xfb}
};

HRESULT CreateAudioRenderer(ERole role, IBaseFilter** ppAudioRenderer)
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;

    if (ppAudioRenderer == NULL)
    {
        return E_POINTER;
    }

    // Activate the IBaseFilter interface on the
    // audio renderer with the specified role.
    hr = CoCreateInstance(CLSID_MMDeviceEnumerator,
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, role,
                                              &pDevice);
    EXIT_ON_ERROR(hr)

    DIRECTX_AUDIO_ACTIVATION_PARAMS  daap;
    daap.cbDirectXAudioActivationParams = sizeof(daap);
    daap.guidAudioSession = guidAudioSessionId;
    daap.dwAudioStreamFlags = AUDCLNT_STREAMFLAGS_CROSSPROCESS;

    PROPVARIANT  var;
    PropVariantInit(&var);

    var.vt = VT_BLOB;
    var.blob.cbSize = sizeof(daap);
    var.blob.pBlobData = (BYTE*)&daap;

    hr = pDevice->Activate(__uuidof(IBaseFilter),
                           CLSCTX_ALL, &var,
                           (void**)ppAudioRenderer);
    EXIT_ON_ERROR(hr)

Exit:
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);
    return hr;
}
```



No exemplo de código anterior, a função CreateAudioRenderer aceita uma função de dispositivo (eConsole, eMultimedia ou eCommunications) como um parâmetro de entrada. O segundo parâmetro é um ponteiro pelo qual a função grava o endereço de uma instância de interface [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) . Além disso, o exemplo mostra como usar o método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) para atribuir o fluxo de áudio na instância **IBaseFilter** a uma sessão de áudio de processo CRUZado com uma GUID de sessão específica do aplicativo (especificada pela constante **guidAudioSessionId** ). O terceiro parâmetro na chamada de **ativação** aponta para uma estrutura que contém o GUID de sessão e o sinalizador de processo cruzado. Se o usuário executar várias instâncias do aplicativo, os fluxos de áudio de todas as instâncias usarão o mesmo GUID de sessão e, portanto, pertencerão à mesma sessão.

Como alternativa, o chamador pode especificar **NULL** como o terceiro parâmetro na chamada de [**ativação**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) para atribuir o fluxo à sessão padrão como a sessão específica do processo com o valor GUID de sessão GUID \_ NULL. Para obter mais informações, consulte **IMMDevice:: Activate**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interoperabilidade com APIs de áudio herdadas](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
