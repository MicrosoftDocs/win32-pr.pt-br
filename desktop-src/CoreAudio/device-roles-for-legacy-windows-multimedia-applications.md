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
# <a name="device-roles-for-legacy-windows-multimedia-applications"></a><span data-ttu-id="2e17e-103">Funções de dispositivo para aplicativos multimídia herdados do Windows</span><span class="sxs-lookup"><span data-stu-id="2e17e-103">Device Roles for Legacy Windows Multimedia Applications</span></span>

> [!Note]  
> <span data-ttu-id="2e17e-104">A API MMDevice dá suporte a funções de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2e17e-104">The MMDevice API supports device roles.</span></span> <span data-ttu-id="2e17e-105">No entanto, a interface do usuário no Windows Vista não implementa o suporte para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="2e17e-105">However, the user interface in Windows Vista does not implement support for this feature.</span></span> <span data-ttu-id="2e17e-106">O suporte da interface do usuário para funções de dispositivo pode ser implementado em uma versão futura do Windows.</span><span class="sxs-lookup"><span data-stu-id="2e17e-106">User interface support for device roles might be implemented in a future version of Windows.</span></span> <span data-ttu-id="2e17e-107">Para obter mais informações, consulte [funções de dispositivo no Windows Vista](device-roles-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="2e17e-107">For more information, see [Device Roles in Windows Vista](device-roles-in-windows-vista.md).</span></span>

 

<span data-ttu-id="2e17e-108">As funções herdadas **waveOutXxx** e **waveInXxx** de multimídia do Windows não fornecem meios para um aplicativo selecionar o [dispositivo de ponto de extremidade de áudio](audio-endpoint-devices.md) que o usuário atribuiu a uma função de [dispositivo](device-roles.md)específica.</span><span class="sxs-lookup"><span data-stu-id="2e17e-108">The legacy Windows multimedia **waveOutXxx** and **waveInXxx** functions provide no means for an application to select the [audio endpoint device](audio-endpoint-devices.md) that the user has assigned to a particular [device role](device-roles.md).</span></span> <span data-ttu-id="2e17e-109">No entanto, no Windows Vista, as APIs de áudio principais podem ser usadas em conjunto com um aplicativo multimídia do Windows para habilitar a seleção de dispositivos com base na função do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2e17e-109">However, in Windows Vista, the core audio APIs can be used in conjunction with a Windows multimedia application to enable device selection based on device role.</span></span> <span data-ttu-id="2e17e-110">Por exemplo, com a ajuda da [API MMDevice](mmdevice-api.md), um aplicativo **waveOutXxx** pode identificar o dispositivo de ponto de extremidade de áudio atribuído a uma função, identificar o dispositivo de saída de forma de onda correspondente e chamar a função **waveOutOpen** para abrir uma instância do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2e17e-110">For example, with the help of the [MMDevice API](mmdevice-api.md), a **waveOutXxx** application can identify the audio endpoint device that is assigned to a role, identify the corresponding waveform output device, and call the **waveOutOpen** function to open an instance of the device.</span></span> <span data-ttu-id="2e17e-111">Para obter mais informações sobre **waveOutXxx** e **waveInXxx**, consulte a documentação do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="2e17e-111">For more information about **waveOutXxx** and **waveInXxx**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="2e17e-112">O exemplo de código a seguir mostra como obter a ID do dispositivo de forma de onda para o dispositivo de ponto de extremidade de renderização atribuído a uma função de dispositivo específica:</span><span class="sxs-lookup"><span data-stu-id="2e17e-112">The following code example shows how to obtain the waveform device ID for the rendering endpoint device that is assigned to a particular device role:</span></span>


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



<span data-ttu-id="2e17e-113">No exemplo de código anterior, a função GetWaveOutId aceita uma função de dispositivo (eConsole, eMultimedia ou eCommunications) como um parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="2e17e-113">In the preceding code example, the GetWaveOutId function accepts a device role (eConsole, eMultimedia, or eCommunications) as an input parameter.</span></span> <span data-ttu-id="2e17e-114">O segundo parâmetro é um ponteiro pelo qual a função grava a ID do dispositivo de formato de onda para o dispositivo de saída de onda atribuído à função especificada.</span><span class="sxs-lookup"><span data-stu-id="2e17e-114">The second parameter is a pointer through which the function writes the waveform device ID for the waveform output device that is assigned to the specified role.</span></span> <span data-ttu-id="2e17e-115">O aplicativo pode então chamar **waveOutOpen** com essa ID para abrir o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2e17e-115">The application can then call **waveOutOpen** with this ID to open the device.</span></span>

<span data-ttu-id="2e17e-116">O loop principal no exemplo de código anterior contém duas chamadas para a função **waveOutMessage** .</span><span class="sxs-lookup"><span data-stu-id="2e17e-116">The main loop in the preceding code example contains two calls to the **waveOutMessage** function.</span></span> <span data-ttu-id="2e17e-117">A primeira chamada envia uma \_ mensagem drv QUERYFUNCTIONINSTANCEIDSIZE para recuperar o tamanho, em bytes, da [cadeia de caracteres de ID do ponto de extremidade](endpoint-id-strings.md) do dispositivo de forma de onda identificado pelo parâmetro *waveOutId* .</span><span class="sxs-lookup"><span data-stu-id="2e17e-117">The first call sends a DRV\_QUERYFUNCTIONINSTANCEIDSIZE message to retrieve the size, in bytes, of the [endpoint ID string](endpoint-id-strings.md) of the waveform device that is identified by the *waveOutId* parameter.</span></span> <span data-ttu-id="2e17e-118">(A cadeia de caracteres de ID do ponto de extremidade identifica o dispositivo de ponto de extremidade de áudio que possui a abstração de dispositivo de onda.) O tamanho relatado por essa chamada inclui o espaço para o caractere nulo de terminação no final da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2e17e-118">(The endpoint ID string identifies the audio endpoint device that underlies the waveform device abstraction.) The size reported by this call includes the space for the terminating null character at the end of the string.</span></span> <span data-ttu-id="2e17e-119">O programa pode usar as informações de tamanho para alocar um buffer que seja grande o suficiente para conter toda a cadeia de caracteres de ID do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="2e17e-119">The program can use the size information to allocate a buffer that is large enough to contain the entire endpoint ID string.</span></span>

<span data-ttu-id="2e17e-120">A segunda chamada para **waveOutMessage** envia uma \_ mensagem QUERYFUNCTIONINSTANCEID drv para recuperar a cadeia de caracteres de ID do dispositivo do dispositivo de saída de forma de onda.</span><span class="sxs-lookup"><span data-stu-id="2e17e-120">The second call to **waveOutMessage** sends a DRV\_QUERYFUNCTIONINSTANCEID message to retrieve the device ID string of the waveform output device.</span></span> <span data-ttu-id="2e17e-121">O código de exemplo compara essa cadeia de caracteres com a cadeia de caracteres de ID do dispositivo do dispositivo de ponto de extremidade de áudio com a função de dispositivo especificada.</span><span class="sxs-lookup"><span data-stu-id="2e17e-121">The example code compares this string to the device ID string of the audio endpoint device with the specified device role.</span></span> <span data-ttu-id="2e17e-122">Se as cadeias de caracteres corresponderem, a função gravará a ID do dispositivo de formato de onda no local apontado pelo parâmetro *pWaveOutId*.</span><span class="sxs-lookup"><span data-stu-id="2e17e-122">If the strings match, then the function writes the waveform device ID to the location pointed to by parameter *pWaveOutId*.</span></span> <span data-ttu-id="2e17e-123">O chamador pode usar essa ID para abrir o dispositivo de saída de onda que tem a função de dispositivo especificada.</span><span class="sxs-lookup"><span data-stu-id="2e17e-123">The caller can use this ID to open the waveform output device that has the specified device role.</span></span>

<span data-ttu-id="2e17e-124">O Windows Vista dá suporte às \_ mensagens QUERYFUNCTIONINSTANCEIDSIZE e drv \_ QUERYFUNCTIONINSTANCEID drv.</span><span class="sxs-lookup"><span data-stu-id="2e17e-124">Windows Vista supports the DRV\_QUERYFUNCTIONINSTANCEIDSIZE and DRV\_QUERYFUNCTIONINSTANCEID messages.</span></span> <span data-ttu-id="2e17e-125">Eles não têm suporte em versões anteriores do Windows, incluindo o Windows Server 2003, o Windows XP e o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="2e17e-125">They are not supported in earlier versions of Windows, including Windows Server 2003, Windows XP, and Windows 2000.</span></span>

<span data-ttu-id="2e17e-126">A função no exemplo de código anterior Obtém a ID do dispositivo de formato de onda para um dispositivo de renderização, mas, com algumas modificações, ela pode ser adaptada para obter a ID do dispositivo de formato de onda para um dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="2e17e-126">The function in the preceding code example obtains the waveform device ID for a rendering device, but, with a few modifications, it can be adapted to obtain the waveform device ID for a capture device.</span></span> <span data-ttu-id="2e17e-127">O aplicativo pode então chamar **waveInOpen** com essa ID para abrir o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2e17e-127">The application can then call **waveInOpen** with this ID to open the device.</span></span> <span data-ttu-id="2e17e-128">Para alterar o exemplo de código anterior para obter a ID do dispositivo de forma de onda para o dispositivo de ponto de extremidade de captura de áudio atribuído a uma função específica, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="2e17e-128">To change the preceding code example to get the waveform device ID for the audio-capture endpoint device that is assigned to a particular role, do the following:</span></span>

-   <span data-ttu-id="2e17e-129">Substitua todas as chamadas de função **waveOutXxx** no exemplo anterior pelas chamadas de função **waveInXxx** correspondentes.</span><span class="sxs-lookup"><span data-stu-id="2e17e-129">Replace all of the **waveOutXxx** function calls in the preceding example with the corresponding **waveInXxx** function calls.</span></span>
-   <span data-ttu-id="2e17e-130">Alterar identificador tipo HWAVEOUT para HWAVEIN.</span><span class="sxs-lookup"><span data-stu-id="2e17e-130">Change handle type HWAVEOUT to HWAVEIN.</span></span>
-   <span data-ttu-id="2e17e-131">Substitua eRender constante de enumeração [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) por eCapture.</span><span class="sxs-lookup"><span data-stu-id="2e17e-131">Replace [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration constant eRender with eCapture.</span></span>

<span data-ttu-id="2e17e-132">No Windows Vista, as funções **waveOutOpen** e **waveInOpen** sempre atribuem os fluxos de áudio que eles criam para a sessão padrão — a sessão específica do processo que é identificada pelo valor GUID de sessão GUID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="2e17e-132">In Windows Vista, the **waveOutOpen** and **waveInOpen** functions always assign the audio streams that they create to the default session—the process-specific session that is identified by the session GUID value GUID\_NULL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e17e-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2e17e-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e17e-134">Interoperabilidade com APIs de áudio herdadas</span><span class="sxs-lookup"><span data-stu-id="2e17e-134">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



