---
description: Funções de dispositivo para aplicativos do DirectShow
ms.assetid: 54f42bda-b4a0-465c-9ce6-9102d2908776
title: Funções de dispositivo para aplicativos do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df8b43ddd56870b65fc9ec1e3bb600e8e6b79528
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456884"
---
# <a name="device-roles-for-directshow-applications"></a><span data-ttu-id="7539e-103">Funções de dispositivo para aplicativos do DirectShow</span><span class="sxs-lookup"><span data-stu-id="7539e-103">Device Roles for DirectShow Applications</span></span>

> [!Note]  
> <span data-ttu-id="7539e-104">A [API MMDevice](mmdevice-api.md) dá suporte a funções de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7539e-104">The [MMDevice API](mmdevice-api.md) supports device roles.</span></span> <span data-ttu-id="7539e-105">No entanto, a interface do usuário no Windows Vista não implementa o suporte para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="7539e-105">However, the user interface in Windows Vista does not implement support for this feature.</span></span> <span data-ttu-id="7539e-106">O suporte da interface do usuário para funções de dispositivo pode ser implementado em uma versão futura do Windows.</span><span class="sxs-lookup"><span data-stu-id="7539e-106">User interface support for device roles might be implemented in a future version of Windows.</span></span> <span data-ttu-id="7539e-107">Para obter mais informações, consulte [funções de dispositivo no Windows Vista](device-roles-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="7539e-107">For more information, see [Device Roles in Windows Vista](device-roles-in-windows-vista.md).</span></span>

 

<span data-ttu-id="7539e-108">A API do DirectShow não fornece um meio para um aplicativo selecionar o [dispositivo de ponto de extremidade de áudio](audio-endpoint-devices.md) atribuído a uma [função de dispositivo](device-roles.md)específica.</span><span class="sxs-lookup"><span data-stu-id="7539e-108">The DirectShow API does not provide a means for an application to select the [audio endpoint device](audio-endpoint-devices.md) that is assigned to a particular [device role](device-roles.md).</span></span> <span data-ttu-id="7539e-109">No entanto, no Windows Vista, as APIs de áudio principais podem ser usadas em conjunto com um aplicativo do DirectShow para habilitar a seleção de dispositivos com base na função do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7539e-109">However, in Windows Vista, the core audio APIs can be used in conjunction with a DirectShow application to enable device selection based on device role.</span></span> <span data-ttu-id="7539e-110">Com a ajuda das principais APIs de áudio, o aplicativo pode:</span><span class="sxs-lookup"><span data-stu-id="7539e-110">With the help of the core audio APIs, the application can:</span></span>

-   <span data-ttu-id="7539e-111">Identifique o dispositivo de ponto de extremidade de áudio que o usuário atribuiu a uma função de dispositivo específica.</span><span class="sxs-lookup"><span data-stu-id="7539e-111">Identify the audio endpoint device that the user has assigned to a particular device role.</span></span>
-   <span data-ttu-id="7539e-112">Crie um filtro de renderização de áudio do DirectShow com uma interface [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) que encapsula o dispositivo de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="7539e-112">Create a DirectShow audio rendering filter with an [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) interface that encapsulates the audio endpoint device.</span></span>
-   <span data-ttu-id="7539e-113">Crie um grafo do DirectShow que incorpore o filtro.</span><span class="sxs-lookup"><span data-stu-id="7539e-113">Build a DirectShow graph that incorporates the filter.</span></span>

<span data-ttu-id="7539e-114">Para obter mais informações sobre o DirectShow e o [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter), consulte a documentação do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="7539e-114">For more information about DirectShow and [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter), see the Windows SDK documentation.</span></span>

<span data-ttu-id="7539e-115">O exemplo de código a seguir mostra como criar um filtro de renderização de áudio do DirectShow que encapsula o dispositivo de ponto de extremidade de renderização atribuído a uma função de dispositivo específica:</span><span class="sxs-lookup"><span data-stu-id="7539e-115">The following code example shows how to create a DirectShow audio rendering filter that encapsulates the rendering endpoint device that is assigned to a particular device role:</span></span>


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



<span data-ttu-id="7539e-116">No exemplo de código anterior, a função CreateAudioRenderer aceita uma função de dispositivo (eConsole, eMultimedia ou eCommunications) como um parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="7539e-116">In the preceding code example, the CreateAudioRenderer function accepts a device role (eConsole, eMultimedia, or eCommunications) as an input parameter.</span></span> <span data-ttu-id="7539e-117">O segundo parâmetro é um ponteiro pelo qual a função grava o endereço de uma instância de interface [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="7539e-117">The second parameter is a pointer through which the function writes the address of an [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) interface instance.</span></span> <span data-ttu-id="7539e-118">Além disso, o exemplo mostra como usar o método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) para atribuir o fluxo de áudio na instância **IBaseFilter** a uma sessão de áudio de processo CRUZado com uma GUID de sessão específica do aplicativo (especificada pela constante **guidAudioSessionId** ).</span><span class="sxs-lookup"><span data-stu-id="7539e-118">In addition, the example shows how to use the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method to assign the audio stream in the **IBaseFilter** instance to a cross-process audio session with an application-specific session GUID (specified by the **guidAudioSessionId** constant).</span></span> <span data-ttu-id="7539e-119">O terceiro parâmetro na chamada de **ativação** aponta para uma estrutura que contém o GUID de sessão e o sinalizador de processo cruzado.</span><span class="sxs-lookup"><span data-stu-id="7539e-119">The third parameter in the **Activate** call points to a structure that contains the session GUID and cross-process flag.</span></span> <span data-ttu-id="7539e-120">Se o usuário executar várias instâncias do aplicativo, os fluxos de áudio de todas as instâncias usarão o mesmo GUID de sessão e, portanto, pertencerão à mesma sessão.</span><span class="sxs-lookup"><span data-stu-id="7539e-120">If the user runs multiple instances of the application, then the audio streams from all the instances use the same session GUID and thus belong to the same session.</span></span>

<span data-ttu-id="7539e-121">Como alternativa, o chamador pode especificar **NULL** como o terceiro parâmetro na chamada de [**ativação**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) para atribuir o fluxo à sessão padrão como a sessão específica do processo com o valor GUID de sessão GUID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="7539e-121">Alternatively, the caller can specify **NULL** as the third parameter in the [**Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) call to assign the stream to the default session as the process-specific session with session GUID value GUID\_NULL.</span></span> <span data-ttu-id="7539e-122">Para obter mais informações, consulte **IMMDevice:: Activate**.</span><span class="sxs-lookup"><span data-stu-id="7539e-122">For more information, see **IMMDevice::Activate**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7539e-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7539e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7539e-124">Interoperabilidade com APIs de áudio herdadas</span><span class="sxs-lookup"><span data-stu-id="7539e-124">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
