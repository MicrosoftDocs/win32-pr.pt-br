---
description: Funções de dispositivo para aplicativos multimídia herdados do Windows
ms.assetid: 54dcaa0e-2652-406d-ba24-c8885924acc6
title: Funções de dispositivo para aplicativos multimídia herdados do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a4ad6728659e4c865aed773575268844fe330e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105751981"
---
# <a name="device-roles-for-legacy-windows-multimedia-applications"></a>Funções de dispositivo para aplicativos multimídia herdados do Windows

> [!Note]  
> A API MMDevice dá suporte a funções de dispositivo. No entanto, a interface do usuário no Windows Vista não implementa o suporte para esse recurso. O suporte da interface do usuário para funções de dispositivo pode ser implementado em uma versão futura do Windows. Para obter mais informações, consulte [funções de dispositivo no Windows Vista](device-roles-in-windows-vista.md).

 

As funções herdadas **waveOutXxx** e **waveInXxx** de multimídia do Windows não fornecem meios para um aplicativo selecionar o [dispositivo de ponto de extremidade de áudio](audio-endpoint-devices.md) que o usuário atribuiu a uma função de [dispositivo](device-roles.md)específica. No entanto, no Windows Vista, as APIs de áudio principais podem ser usadas em conjunto com um aplicativo multimídia do Windows para habilitar a seleção de dispositivos com base na função do dispositivo. Por exemplo, com a ajuda da [API MMDevice](mmdevice-api.md), um aplicativo **waveOutXxx** pode identificar o dispositivo de ponto de extremidade de áudio atribuído a uma função, identificar o dispositivo de saída de forma de onda correspondente e chamar a função **waveOutOpen** para abrir uma instância do dispositivo. Para obter mais informações sobre **waveOutXxx** e **waveInXxx**, consulte a documentação do SDK do Windows.

O exemplo de código a seguir mostra como obter a ID do dispositivo de forma de onda para o dispositivo de ponto de extremidade de renderização atribuído a uma função de dispositivo específica:


```C++
//-----------------------------------------------------------
// This function gets the waveOut ID of the audio endpoint
// device that is currently assigned to the specified device
// role. The caller can use the waveOut ID to open the
// waveOut device that corresponds to the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

HRESULT GetWaveOutId(ERole role, int *pWaveOutId)
{
    HRESULT hr;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    WCHAR *pstrEndpointIdKey = NULL;
    WCHAR *pstrEndpointId = NULL;

    if (pWaveOutId == NULL)
    {
        return E_POINTER;
    }

    // Create an audio endpoint device enumerator.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get the audio endpoint device that the user has
    // assigned to the specified device role.
    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, role,
                                              &pDevice);
    EXIT_ON_ERROR(hr)

    // Get the endpoint ID string of the audio endpoint device.
    hr = pDevice->GetId(&pstrEndpointIdKey);
    EXIT_ON_ERROR(hr)

    // Get the size of the endpoint ID string.
    size_t  cbEndpointIdKey;

    hr = StringCbLength(pstrEndpointIdKey,
                        STRSAFE_MAX_CCH * sizeof(WCHAR),
                        &cbEndpointIdKey);
    EXIT_ON_ERROR(hr)

    // Include terminating null in string size.
    cbEndpointIdKey += sizeof(WCHAR);

    // Allocate a buffer for a second string of the same size.
    pstrEndpointId = (WCHAR*)CoTaskMemAlloc(cbEndpointIdKey);
    if (pstrEndpointId == NULL)
    {
        EXIT_ON_ERROR(hr = E_OUTOFMEMORY)
    }

    // Each for-loop iteration below compares the endpoint ID
    // string of the audio endpoint device to the endpoint ID
    // string of an enumerated waveOut device. If the strings
    // match, then we've found the waveOut device that is
    // assigned to the specified device role.
    int waveOutId;
    int cWaveOutDevices = waveOutGetNumDevs();

    for (waveOutId = 0; waveOutId < cWaveOutDevices; waveOutId++)
    {
        MMRESULT mmr;
        size_t cbEndpointId;

        // Get the size (including the terminating null) of
        // the endpoint ID string of the waveOut device.
        mmr = waveOutMessage((HWAVEOUT)IntToPtr(waveOutId),
                             DRV_QUERYFUNCTIONINSTANCEIDSIZE,
                             (DWORD_PTR)&cbEndpointId, NULL);
        if (mmr != MMSYSERR_NOERROR ||
            cbEndpointIdKey != cbEndpointId)  // do sizes match?
        {
            continue;  // not a matching device
        }

        // Get the endpoint ID string for this waveOut device.
        mmr = waveOutMessage((HWAVEOUT)IntToPtr(waveOutId),
                             DRV_QUERYFUNCTIONINSTANCEID,
                             (DWORD_PTR)pstrEndpointId,
                             cbEndpointId);
        if (mmr != MMSYSERR_NOERROR)
        {
            continue;
        }

        // Check whether the endpoint ID string of this waveOut
        // device matches that of the audio endpoint device.
        if (lstrcmpi(pstrEndpointId, pstrEndpointIdKey) == 0)
        {
            *pWaveOutId = waveOutId;  // found match
            hr = S_OK;
            break;
        }
    }

    if (waveOutId == cWaveOutDevices)
    {
        // We reached the end of the for-loop above without
        // finding a waveOut device with a matching endpoint
        // ID string. This behavior is quite unexpected.
        hr = E_UNEXPECTED;
    }

Exit:
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);
    CoTaskMemFree(pstrEndpointIdKey);  // NULL pointer okay
    CoTaskMemFree(pstrEndpointId);
    return hr;
}
```



No exemplo de código anterior, a função GetWaveOutId aceita uma função de dispositivo (eConsole, eMultimedia ou eCommunications) como um parâmetro de entrada. O segundo parâmetro é um ponteiro pelo qual a função grava a ID do dispositivo de formato de onda para o dispositivo de saída de onda atribuído à função especificada. O aplicativo pode então chamar **waveOutOpen** com essa ID para abrir o dispositivo.

O loop principal no exemplo de código anterior contém duas chamadas para a função **waveOutMessage** . A primeira chamada envia uma \_ mensagem drv QUERYFUNCTIONINSTANCEIDSIZE para recuperar o tamanho, em bytes, da [cadeia de caracteres de ID do ponto de extremidade](endpoint-id-strings.md) do dispositivo de forma de onda identificado pelo parâmetro *waveOutId* . (A cadeia de caracteres de ID do ponto de extremidade identifica o dispositivo de ponto de extremidade de áudio que possui a abstração de dispositivo de onda.) O tamanho relatado por essa chamada inclui o espaço para o caractere nulo de terminação no final da cadeia de caracteres. O programa pode usar as informações de tamanho para alocar um buffer que seja grande o suficiente para conter toda a cadeia de caracteres de ID do ponto de extremidade.

A segunda chamada para **waveOutMessage** envia uma \_ mensagem QUERYFUNCTIONINSTANCEID drv para recuperar a cadeia de caracteres de ID do dispositivo do dispositivo de saída de forma de onda. O código de exemplo compara essa cadeia de caracteres com a cadeia de caracteres de ID do dispositivo do dispositivo de ponto de extremidade de áudio com a função de dispositivo especificada. Se as cadeias de caracteres corresponderem, a função gravará a ID do dispositivo de formato de onda no local apontado pelo parâmetro *pWaveOutId*. O chamador pode usar essa ID para abrir o dispositivo de saída de onda que tem a função de dispositivo especificada.

O Windows Vista dá suporte às \_ mensagens QUERYFUNCTIONINSTANCEIDSIZE e drv \_ QUERYFUNCTIONINSTANCEID drv. Eles não têm suporte em versões anteriores do Windows, incluindo o Windows Server 2003, o Windows XP e o Windows 2000.

A função no exemplo de código anterior Obtém a ID do dispositivo de formato de onda para um dispositivo de renderização, mas, com algumas modificações, ela pode ser adaptada para obter a ID do dispositivo de formato de onda para um dispositivo de captura. O aplicativo pode então chamar **waveInOpen** com essa ID para abrir o dispositivo. Para alterar o exemplo de código anterior para obter a ID do dispositivo de forma de onda para o dispositivo de ponto de extremidade de captura de áudio atribuído a uma função específica, faça o seguinte:

-   Substitua todas as chamadas de função **waveOutXxx** no exemplo anterior pelas chamadas de função **waveInXxx** correspondentes.
-   Alterar identificador tipo HWAVEOUT para HWAVEIN.
-   Substitua eRender constante de enumeração [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) por eCapture.

No Windows Vista, as funções **waveOutOpen** e **waveInOpen** sempre atribuem os fluxos de áudio que eles criam para a sessão padrão — a sessão específica do processo que é identificada pelo valor GUID de sessão GUID \_ NULL.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interoperabilidade com APIs de áudio herdadas](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



