---
description: Funções de dispositivo para aplicativos DirectSound
ms.assetid: 7d82d67f-aad8-4e5b-ac65-87d75774e613
title: Funções de dispositivo para aplicativos DirectSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3829817f8b00c7288aceb8d0b6d418d5793ae580
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920125"
---
# <a name="device-roles-for-directsound-applications"></a><span data-ttu-id="b2f1b-103">Funções de dispositivo para aplicativos DirectSound</span><span class="sxs-lookup"><span data-stu-id="b2f1b-103">Device Roles for DirectSound Applications</span></span>

> [!Note]  
> <span data-ttu-id="b2f1b-104">A [API MMDevice](mmdevice-api.md) dá suporte a funções de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b2f1b-104">The [MMDevice API](mmdevice-api.md) supports device roles.</span></span> <span data-ttu-id="b2f1b-105">No entanto, a interface do usuário no Windows Vista não implementa o suporte para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="b2f1b-105">However, the user interface in Windows Vista does not implement support for this feature.</span></span> <span data-ttu-id="b2f1b-106">O suporte da interface do usuário para funções de dispositivo pode ser implementado em uma versão futura do Windows.</span><span class="sxs-lookup"><span data-stu-id="b2f1b-106">User interface support for device roles might be implemented in a future version of Windows.</span></span> <span data-ttu-id="b2f1b-107">Para obter mais informações, consulte [funções de dispositivo no Windows Vista](device-roles-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="b2f1b-107">For more information, see [Device Roles in Windows Vista](device-roles-in-windows-vista.md).</span></span>

 

<span data-ttu-id="b2f1b-108">A API do DirectSound não fornece um meio para um aplicativo selecionar o [dispositivo de ponto de extremidade de áudio](audio-endpoint-devices.md) que o usuário atribuiu a uma função de [dispositivo](device-roles.md)específica.</span><span class="sxs-lookup"><span data-stu-id="b2f1b-108">The DirectSound API does not provide a means for an application to select the [audio endpoint device](audio-endpoint-devices.md) that the user has assigned to a particular [device role](device-roles.md).</span></span> <span data-ttu-id="b2f1b-109">No entanto, no Windows Vista, as APIs de áudio principais podem ser usadas em conjunto com um aplicativo DirectSound para habilitar a seleção de dispositivos com base na função do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b2f1b-109">However, in Windows Vista, the core audio APIs can be used in conjunction with a DirectSound application to enable device selection based on device role.</span></span> <span data-ttu-id="b2f1b-110">Com a ajuda das principais APIs de áudio, o aplicativo pode identificar o dispositivo de ponto de extremidade de áudio atribuído a uma função específica, obter o GUID do dispositivo DirectSound para o dispositivo de ponto de extremidade e chamar a função **DirectSoundCreate** ou **DirectSoundCaptureCreate** para criar uma instância de interface **IDirectSound** ou **IDirectSoundCapture** que encapsula o dispositivo de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="b2f1b-110">With the help of the core audio APIs, the application can identify the audio endpoint device that is assigned to a particular role, get the DirectSound device GUID for the endpoint device, and call the **DirectSoundCreate** or **DirectSoundCaptureCreate** function to create an **IDirectSound** or **IDirectSoundCapture** interface instance that encapsulates the endpoint device.</span></span> <span data-ttu-id="b2f1b-111">Para obter mais informações sobre o DirectSound, consulte a documentação do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="b2f1b-111">For more information about DirectSound, see the Windows SDK documentation.</span></span>

<span data-ttu-id="b2f1b-112">O exemplo de código a seguir mostra como obter o GUID do dispositivo DirectSound para o dispositivo de renderização ou de captura que está atualmente atribuído a uma função de dispositivo específica:</span><span class="sxs-lookup"><span data-stu-id="b2f1b-112">The following code example shows how to obtain the DirectSound device GUID for the rendering or capture device that is currently assigned to a particular device role:</span></span>


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



<span data-ttu-id="b2f1b-113">No exemplo de código anterior, a função GetDirectSoundGuid aceita uma direção de fluxo de dados (eRender ou eCapture) e uma função de dispositivo (eConsole, eMultimedia ou eCommunications) como parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="b2f1b-113">In the preceding code example, the GetDirectSoundGuid function accepts a data-flow direction (eRender or eCapture) and a device role (eConsole, eMultimedia, or eCommunications) as input parameters.</span></span> <span data-ttu-id="b2f1b-114">O terceiro parâmetro é um ponteiro pelo qual a função grava um GUID de dispositivo que o aplicativo pode fornecer como um parâmetro de entrada para a função **DirectSoundCreate** ou **DirectSoundCaptureCreate** .</span><span class="sxs-lookup"><span data-stu-id="b2f1b-114">The third parameter is a pointer through which the function writes a device GUID that the application can supply as an input parameter to the **DirectSoundCreate** or **DirectSoundCaptureCreate** function.</span></span>

<span data-ttu-id="b2f1b-115">O exemplo de código anterior Obtém o GUID do dispositivo DirectSound por:</span><span class="sxs-lookup"><span data-stu-id="b2f1b-115">The preceding code example obtains the DirectSound device GUID by:</span></span>

-   <span data-ttu-id="b2f1b-116">Criar uma instância de interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) que representa o dispositivo de ponto de extremidade de áudio que tem a direção de fluxo de dados e a função de dispositivo especificadas.</span><span class="sxs-lookup"><span data-stu-id="b2f1b-116">Creating an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface instance that represents the audio endpoint device that has the specified data-flow direction and device role.</span></span>
-   <span data-ttu-id="b2f1b-117">Abrindo o repositório de propriedades do dispositivo de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="b2f1b-117">Opening the property store of the audio endpoint device.</span></span>
-   <span data-ttu-id="b2f1b-118">Obtendo a propriedade [**PKEY \_ AudioEndpoint \_ GUID**](pkey-audioendpoint-guid.md) do repositório de propriedades.</span><span class="sxs-lookup"><span data-stu-id="b2f1b-118">Getting the [**PKEY\_AudioEndpoint\_GUID**](pkey-audioendpoint-guid.md) property from the property store.</span></span> <span data-ttu-id="b2f1b-119">O valor da propriedade é uma representação de cadeia de caracteres do GUID do dispositivo DirectSound para o dispositivo de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="b2f1b-119">The property value is a string representation of the DirectSound device GUID for the audio endpoint device.</span></span>
-   <span data-ttu-id="b2f1b-120">Chamar a função [**CLSIDFromString**](https://www.bing.com/search?q=**CLSIDFromString**) para converter a representação da cadeia de caracteres do GUID do dispositivo em uma estrutura de GUID.</span><span class="sxs-lookup"><span data-stu-id="b2f1b-120">Calling the [**CLSIDFromString**](https://www.bing.com/search?q=**CLSIDFromString**) function to convert the string representation of the device GUID to a GUID structure.</span></span> <span data-ttu-id="b2f1b-121">Para obter mais informações sobre o **CLSIDFromString**, consulte a documentação do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="b2f1b-121">For more information about **CLSIDFromString**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="b2f1b-122">Depois de obter um GUID de dispositivo da função GetDirectSoundGuid, o aplicativo pode chamar **DirectSoundCreate** ou **DIRECTSOUNDCAPTURECREATE** com esse GUID para criar o dispositivo de captura ou a renderização do DirectSound que encapsula o dispositivo de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="b2f1b-122">After obtaining a device GUID from the GetDirectSoundGuid function, the application can call **DirectSoundCreate** or **DirectSoundCaptureCreate** with this GUID to create the DirectSound rendering or capture device that encapsulates the audio endpoint device.</span></span> <span data-ttu-id="b2f1b-123">Quando o DirectSound cria um dispositivo dessa forma, ele sempre atribui o fluxo de áudio do dispositivo à sessão padrão — a sessão de áudio específica do processo que é identificada pelo valor GUID da sessão GUID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="b2f1b-123">When DirectSound creates a device in this way, it always assigns the device's audio stream to the default session—the process-specific audio session that is identified by the session GUID value GUID\_NULL.</span></span>

<span data-ttu-id="b2f1b-124">Se o aplicativo exigir que o DirectSound atribua o fluxo a uma sessão de áudio de processo cruzado ou a uma sessão com um GUID de sessão não **nulo** , ele deverá chamar o método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) para criar um objeto **IDirectSound** ou **IDirectSoundCapture** em vez de usar a técnica mostrada no exemplo de código anterior.</span><span class="sxs-lookup"><span data-stu-id="b2f1b-124">If the application requires DirectSound to assign the stream to a cross-process audio session or to a session with a non-**NULL** session GUID, it should call the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method to create an **IDirectSound** or **IDirectSoundCapture** object instead of using the technique shown in the preceding code example.</span></span> <span data-ttu-id="b2f1b-125">Para obter um exemplo de código que mostra como usar o método **Activate** para especificar uma sessão de áudio de processo cruzado ou um GUID de sessão não **nulo** para um fluxo, consulte [funções de dispositivo para aplicativos do DirectShow](device-roles-for-directshow-applications.md).</span><span class="sxs-lookup"><span data-stu-id="b2f1b-125">For a code example that shows how to use the **Activate** method to specify a cross-process audio session or a non-**NULL** session GUID for a stream, see [Device Roles for DirectShow Applications](device-roles-for-directshow-applications.md).</span></span> <span data-ttu-id="b2f1b-126">O exemplo de código nessa seção mostra como criar um filtro do DirectShow, mas, com pequenas modificações, o código pode ser adaptado para criar um dispositivo DirectSound.</span><span class="sxs-lookup"><span data-stu-id="b2f1b-126">The code example in that section shows how to create a DirectShow filter, but, with minor modifications, the code can be adapted to create a DirectSound device.</span></span>

<span data-ttu-id="b2f1b-127">A função GetDirectSoundGuid no exemplo de código anterior chama a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar um enumerador para os dispositivos de ponto de extremidade de áudio no sistema.</span><span class="sxs-lookup"><span data-stu-id="b2f1b-127">The GetDirectSoundGuid function in the preceding code example calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an enumerator for the audio endpoint devices in the system.</span></span> <span data-ttu-id="b2f1b-128">A menos que o programa de chamada chamou anteriormente a função [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar a biblioteca com, a chamada **CoCreateInstance** falhará.</span><span class="sxs-lookup"><span data-stu-id="b2f1b-128">Unless the calling program previously called either the [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) function to initialize the COM library, the **CoCreateInstance** call will fail.</span></span> <span data-ttu-id="b2f1b-129">Para obter mais informações sobre **CoCreateInstance**, **CoInitialize** e **CoInitializeEx**, consulte a documentação do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="b2f1b-129">For more information about **CoCreateInstance**, **CoInitialize**, and **CoInitializeEx**, see the Windows SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2f1b-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b2f1b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2f1b-131">Interoperabilidade com APIs de áudio herdadas</span><span class="sxs-lookup"><span data-stu-id="b2f1b-131">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
