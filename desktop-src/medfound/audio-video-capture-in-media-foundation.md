---
description: O Microsoft Media Foundation dá suporte à captura de áudio e vídeo.
ms.assetid: 8a9d96f8-1096-4b66-a2ec-8a95d754ea72
title: Captura de áudio/vídeo no Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506c14ee4ab94a27cfafbe18a97ffa8f05676f1f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105789612"
---
# <a name="audiovideo-capture-in-media-foundation"></a><span data-ttu-id="04437-103">Captura de áudio/vídeo no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="04437-103">Audio/Video Capture in Media Foundation</span></span>

<span data-ttu-id="04437-104">O Microsoft Media Foundation dá suporte à captura de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="04437-104">Microsoft Media Foundation supports audio and video capture.</span></span> <span data-ttu-id="04437-105">Os dispositivos de captura de vídeo têm suporte por meio do driver de classe UVC e devem ser compatíveis com o UVC 1,1.</span><span class="sxs-lookup"><span data-stu-id="04437-105">Video capture devices are supported through the UVC class driver and must be compatible with UVC 1.1.</span></span> <span data-ttu-id="04437-106">Os dispositivos de captura de áudio têm suporte por meio da API de sessão de áudio do Windows (WASAPI).</span><span class="sxs-lookup"><span data-stu-id="04437-106">Audio capture devices are supported through Windows Audio Session API (WASAPI).</span></span>

<span data-ttu-id="04437-107">Um dispositivo de captura é representado em Media Foundation por um objeto de origem de mídia, que expõe a interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) .</span><span class="sxs-lookup"><span data-stu-id="04437-107">A capture device is represented in Media Foundation by a media source object, which exposes the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span> <span data-ttu-id="04437-108">Na maioria dos casos, o aplicativo não usará essa interface diretamente, mas usará uma API de nível superior, como o [leitor de origem](source-reader.md) para controlar o dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="04437-108">In most cases, the application will not use this interface directly, but will use a higher-level API such as the [Source Reader](source-reader.md) to control the capture device.</span></span>

## <a name="enumerate-capture-devices"></a><span data-ttu-id="04437-109">Enumerar dispositivos de captura</span><span class="sxs-lookup"><span data-stu-id="04437-109">Enumerate Capture Devices</span></span>

<span data-ttu-id="04437-110">Para enumerar os dispositivos de captura no sistema, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="04437-110">To enumerate the capture devices on the system, perform the following steps:</span></span>

1.  <span data-ttu-id="04437-111">Chame a função [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para criar um repositório de atributos.</span><span class="sxs-lookup"><span data-stu-id="04437-111">Call the [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) function to create an attribute store.</span></span>
2.  <span data-ttu-id="04437-112">Defina o atributo de [ \_ tipo de origem do \_ atributo \_ \_ MF DEVSOURCE](mf-devsource-attribute-source-type.md) com um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="04437-112">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute to one of the following values:</span></span>

    | <span data-ttu-id="04437-113">Valor</span><span class="sxs-lookup"><span data-stu-id="04437-113">Value</span></span>                                                    | <span data-ttu-id="04437-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="04437-114">Description</span></span>                      |
    |----------------------------------------------------------|----------------------------------|
    | <span data-ttu-id="04437-115">**\_tipo de origem do atributo MF DEVSOURCE \_ \_ \_ \_ AUDCAP \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="04437-115">**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_GUID**</span></span> | <span data-ttu-id="04437-116">Enumere dispositivos de captura de áudio.</span><span class="sxs-lookup"><span data-stu-id="04437-116">Enumerate audio capture devices.</span></span> |
    | <span data-ttu-id="04437-117">**\_tipo de origem do atributo MF DEVSOURCE \_ \_ \_ \_ VIDCAP \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="04437-117">**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**</span></span> | <span data-ttu-id="04437-118">Enumere dispositivos de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="04437-118">Enumerate video capture devices.</span></span> |

    

     

3.  <span data-ttu-id="04437-119">Chame a função [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) .</span><span class="sxs-lookup"><span data-stu-id="04437-119">Call the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function.</span></span> <span data-ttu-id="04437-120">Essa função aloca uma matriz de ponteiros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="04437-120">This function allocates an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers.</span></span> <span data-ttu-id="04437-121">Cada ponteiro representa um objeto de ativação para um dispositivo no sistema.</span><span class="sxs-lookup"><span data-stu-id="04437-121">Each pointer represents an activation object for one device on the system.</span></span>
4.  <span data-ttu-id="04437-122">Chame o método [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) para criar uma instância da fonte de mídia de um dos objetos de ativação.</span><span class="sxs-lookup"><span data-stu-id="04437-122">Call the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method to create an instance of the media source from one of the activation objects.</span></span>

<span data-ttu-id="04437-123">O exemplo a seguir cria uma origem de mídia para o primeiro dispositivo de captura de vídeo na lista de enumeração:</span><span class="sxs-lookup"><span data-stu-id="04437-123">The following example creates a media source for the first video capture device in the enumeration list:</span></span>


```C++
HRESULT CreateVideoCaptureDevice(IMFMediaSource **ppSource)
{
    *ppSource = NULL;

    UINT32 count = 0;

    IMFAttributes *pConfig = NULL;
    IMFActivate **ppDevices = NULL;

    // Create an attribute store to hold the search criteria.
    HRESULT hr = MFCreateAttributes(&pConfig, 1);

    // Request video capture devices.
    if (SUCCEEDED(hr))
    {
        hr = pConfig->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE, 
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
            );
    }

    // Enumerate the devices,
    if (SUCCEEDED(hr))
    {
        hr = MFEnumDeviceSources(pConfig, &ppDevices, &count);
    }

    // Create a media source for the first device in the list.
    if (SUCCEEDED(hr))
    {
        if (count > 0)
        {
            hr = ppDevices[0]->ActivateObject(IID_PPV_ARGS(ppSource));
        }
        else
        {
            hr = MF_E_NOT_FOUND;
        }
    }

    for (DWORD i = 0; i < count; i++)
    {
        ppDevices[i]->Release();
    }
    CoTaskMemFree(ppDevices);
    return hr;
}
```



<span data-ttu-id="04437-124">Você pode consultar os objetos de ativação para vários atributos, incluindo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="04437-124">You can query the activation objects for various attributes, including the following:</span></span>

-   <span data-ttu-id="04437-125">O atributo de [ \_ \_ \_ \_ nome amigável do atributo MF DEVSOURCE](mf-devsource-attribute-friendly-name.md) contém o nome de exibição do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="04437-125">The [MF\_DEVSOURCE\_ATTRIBUTE\_FRIENDLY\_NAME](mf-devsource-attribute-friendly-name.md) attribute contains the display name of the device.</span></span> <span data-ttu-id="04437-126">O nome de exibição é adequado para mostrar ao usuário, mas pode não ser exclusivo.</span><span class="sxs-lookup"><span data-stu-id="04437-126">The display name is suitable for showing to the user, but might not be unique.</span></span>
-   <span data-ttu-id="04437-127">Para dispositivos de vídeo, o atributo de [ \_ DEVSOURCE MF tipo de \_ \_ fonte VIDCAP de \_ \_ \_ \_ link simbólico](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) contém o link simbólico para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="04437-127">For video devices, the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) attribute contains the symbolic link to the device.</span></span> <span data-ttu-id="04437-128">O link simbólico identifica exclusivamente o dispositivo no sistema, mas não é uma cadeia de caracteres legível.</span><span class="sxs-lookup"><span data-stu-id="04437-128">The symbolic link uniquely identifies the device on the system, but is not a readable string.</span></span>
-   <span data-ttu-id="04437-129">Para dispositivos de áudio, o atributo [MF \_ DEVSOURCE do tipo de \_ \_ fonte \_ \_ AUDCAP ponto de extremidade da \_ \_ ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md) contém a ID do ponto de extremidade de áudio do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="04437-129">For audio devices, the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ENDPOINT\_ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md) attribute contains the audio endpoint ID of the device.</span></span> <span data-ttu-id="04437-130">A ID do ponto de extremidade de áudio é semelhante a um link simbólico.</span><span class="sxs-lookup"><span data-stu-id="04437-130">The audio endpoint ID is similar to a symbolic link.</span></span> <span data-ttu-id="04437-131">Ele identifica exclusivamente o dispositivo no sistema, mas não é uma cadeia de caracteres legível.</span><span class="sxs-lookup"><span data-stu-id="04437-131">It uniquely identifies the device on the system, but is not a readable string.</span></span>

<span data-ttu-id="04437-132">O exemplo a seguir usa uma matriz de ponteiros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) e imprime o nome de exibição de cada dispositivo na janela de depuração:</span><span class="sxs-lookup"><span data-stu-id="04437-132">The following example takes an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers and prints the display name of each device to the debug window:</span></span>


```C++
void DebugShowDeviceNames(IMFActivate **ppDevices, UINT count)
{
    for (DWORD i = 0; i < count; i++)
    {
        HRESULT hr = S_OK;
        WCHAR *szFriendlyName = NULL;
    
        // Try to get the display name.
        UINT32 cchName;
        hr = ppDevices[i]->GetAllocatedString(
            MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME,
            &szFriendlyName, &cchName);

        if (SUCCEEDED(hr))
        {
            OutputDebugString(szFriendlyName);
            OutputDebugString(L"\n");
        }
        CoTaskMemFree(szFriendlyName);
    }
}
```



<span data-ttu-id="04437-133">Se você já souber o link simbólico para um dispositivo de vídeo, há outra maneira de criar a origem da mídia para o dispositivo:</span><span class="sxs-lookup"><span data-stu-id="04437-133">If you already know the symbolic link for a video device, there is another way to create the media source for the device:</span></span>

1.  <span data-ttu-id="04437-134">Chame [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para criar um repositório de atributos.</span><span class="sxs-lookup"><span data-stu-id="04437-134">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store.</span></span>
2.  <span data-ttu-id="04437-135">Defina o atributo do [ \_ \_ \_ \_ tipo de origem DEVSOURCE](mf-devsource-attribute-source-type.md) do atributo MF como **MF \_ DEVSOURCE \_ atributo \_ Source \_ tipo \_ VIDCAP \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="04437-135">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute to **MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**.</span></span>
3.  <span data-ttu-id="04437-136">Defina o atributo de [ \_ \_ \_ \_ \_ \_ \_ link DEVSOURCE do tipo de origem MF VIDCAP](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) para o link simbólico.</span><span class="sxs-lookup"><span data-stu-id="04437-136">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) attribute to the symbolic link.</span></span>
4.  <span data-ttu-id="04437-137">Chame a função [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) ou [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="04437-137">Call either the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) or [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) function.</span></span> <span data-ttu-id="04437-138">O primeiro retorna um ponteiro [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) .</span><span class="sxs-lookup"><span data-stu-id="04437-138">The former returns an [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) pointer.</span></span> <span data-ttu-id="04437-139">O último retorna um ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) para um objeto de ativação.</span><span class="sxs-lookup"><span data-stu-id="04437-139">The latter returns an [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer to an activation object.</span></span> <span data-ttu-id="04437-140">Você pode usar o objeto de ativação para criar a origem.</span><span class="sxs-lookup"><span data-stu-id="04437-140">You can use the activation object to create the source.</span></span> <span data-ttu-id="04437-141">(Um objeto de ativação pode ser empacotado para outro processo, portanto, será útil se você quiser criar a origem em outro processo.</span><span class="sxs-lookup"><span data-stu-id="04437-141">(An activation object can be marshaled to another process, so it is useful if you want to create the source in another process.</span></span> <span data-ttu-id="04437-142">Para obter mais informações, consulte [Activation Objects](activation-objects.md).)</span><span class="sxs-lookup"><span data-stu-id="04437-142">For more information, see [Activation Objects](activation-objects.md).)</span></span>

<span data-ttu-id="04437-143">O exemplo a seguir usa o link simbólico de um dispositivo de vídeo e cria uma fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="04437-143">The following example takes the symbolic link of a video device and creates a media source.</span></span>


```C++
HRESULT CreateVideoCaptureDevice(PCWSTR *pszSymbolicLink, IMFMediaSource **ppSource)
{
    *ppSource = NULL;
    
    IMFAttributes *pAttributes = NULL;
    IMFMediaSource *pSource = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 2);

    // Set the device type to video.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE,
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
            );
    }


    // Set the symbolic link.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK,
            (LPCWSTR)pszSymbolicLink
            );            
    }

    if (SUCCEEDED(hr))
    {
        hr = MFCreateDeviceSource(pAttributes, ppSource);
    }

    SafeRelease(&pAttributes);
    return hr;    
}
```



<span data-ttu-id="04437-144">Há uma maneira equivalente de criar um dispositivo de áudio a partir da ID do ponto de extremidade de áudio:</span><span class="sxs-lookup"><span data-stu-id="04437-144">There is an equivalent way to create an audio device from the audio endpoint ID:</span></span>

1.  <span data-ttu-id="04437-145">Chame [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para criar um repositório de atributos.</span><span class="sxs-lookup"><span data-stu-id="04437-145">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store.</span></span>
2.  <span data-ttu-id="04437-146">Defina o atributo do [ \_ \_ \_ \_ tipo de origem DEVSOURCE](mf-devsource-attribute-source-type.md) do atributo MF como **MF \_ DEVSOURCE \_ atributo \_ Source \_ tipo \_ AUDCAP \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="04437-146">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute to **MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_GUID**.</span></span>
3.  <span data-ttu-id="04437-147">Defina o atributo de [ \_ ID de ponto de \_ \_ \_ \_ \_ extremidade \_ AUDCAP de DEVSOURCE MF](mf-devsource-attribute-source-type-audcap-endpoint-id.md) para a ID do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="04437-147">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ENDPOINT\_ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md) attribute to the endpoint ID.</span></span>
4.  <span data-ttu-id="04437-148">Chame a função [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) ou [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="04437-148">Call either the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) or [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) function.</span></span>

<span data-ttu-id="04437-149">O exemplo a seguir usa uma ID de ponto de extremidade de áudio e cria uma origem de mídia.</span><span class="sxs-lookup"><span data-stu-id="04437-149">The following example takes an audio endpoint ID and creates a media source.</span></span>


```C++
HRESULT CreateAudioCaptureDevice(PCWSTR *pszEndPointID, IMFMediaSource **ppSource)
{
    *ppSource = NULL;
    
    IMFAttributes *pAttributes = NULL;
    IMFMediaSource *pSource = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 2);

    // Set the device type to audio.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE,
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_GUID
            );
    }

    // Set the endpoint ID.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID,
            (LPCWSTR)pszEndPointID
            ); 
    }

    if (SUCCEEDED(hr))
    {
        hr = MFCreateDeviceSource(pAttributes, ppSource);
    }

    SafeRelease(&pAttributes);
    return hr;    
}
```



## <a name="use-a-capture-device"></a><span data-ttu-id="04437-150">Usar um dispositivo de captura</span><span class="sxs-lookup"><span data-stu-id="04437-150">Use a capture device</span></span>

<span data-ttu-id="04437-151">Depois de criar a origem de mídia para um dispositivo de captura, use o [leitor de origem](source-reader.md) para obter dados do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="04437-151">After you create the media source for a capture device, use the [Source Reader](source-reader.md) to get data from the device.</span></span> <span data-ttu-id="04437-152">O leitor de origem fornece amostras de mídia que contêm os dados de áudio ou quadros de vídeo de captura.</span><span class="sxs-lookup"><span data-stu-id="04437-152">The Source Reader delivers media samples that contain the capture audio data or video frames.</span></span> <span data-ttu-id="04437-153">A próxima etapa depende do cenário do seu aplicativo:</span><span class="sxs-lookup"><span data-stu-id="04437-153">The next step depends on your application scenario:</span></span>

-   <span data-ttu-id="04437-154">Visualização de vídeo: Use Microsoft Direct3D ou Direct2D para exibir o vídeo.</span><span class="sxs-lookup"><span data-stu-id="04437-154">Video preview: Use Microsoft Direct3D or Direct2D to display the video.</span></span>
-   <span data-ttu-id="04437-155">Captura de arquivo: Use o [gravador de coletor](sink-writer.md) para codificar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="04437-155">File capture: Use the [Sink Writer](sink-writer.md) to encode the file.</span></span>
-   <span data-ttu-id="04437-156">Visualização de áudio: use [WASAPI](/windows/desktop/CoreAudio/wasapi).</span><span class="sxs-lookup"><span data-stu-id="04437-156">Audio preview: Use [WASAPI](/windows/desktop/CoreAudio/wasapi).</span></span>

<span data-ttu-id="04437-157">Se você quiser combinar a captura de áudio com a captura de vídeo, use a *fonte de mídia agregada*.</span><span class="sxs-lookup"><span data-stu-id="04437-157">If you want to combine audio capture with video capture, use the *aggregate media source*.</span></span> <span data-ttu-id="04437-158">A fonte de mídia agregada contém uma coleção de fontes de mídia e combina todos os seus fluxos em um único objeto de origem de mídia.</span><span class="sxs-lookup"><span data-stu-id="04437-158">The aggregate media source contains a collection of media sources and combines all of their streams into a single media source object.</span></span> <span data-ttu-id="04437-159">Para criar uma instância da fonte de mídia agregada, chame a função [**MFCreateAggregateSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaggregatesource) .</span><span class="sxs-lookup"><span data-stu-id="04437-159">To create an instance of the aggregate media source, call the [**MFCreateAggregateSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaggregatesource) function.</span></span>

## <a name="shut-down-the-capture-device"></a><span data-ttu-id="04437-160">Desligar o dispositivo de captura</span><span class="sxs-lookup"><span data-stu-id="04437-160">Shut down the capture device</span></span>

<span data-ttu-id="04437-161">Quando o dispositivo de captura não for mais necessário, você deverá desligar o dispositivo chamando o [**desligamento**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) no objeto [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) obtido chamando [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) ou [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="04437-161">When the capture device is no longer needed, you must shut down the device by calling [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) object you obtained by calling [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) or [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span> <span data-ttu-id="04437-162">A falha ao chamar o **desligamento** pode resultar em links de memória porque o sistema pode manter uma referência a recursos de **IMFMediaSource** até que o **desligamento** seja chamado.</span><span class="sxs-lookup"><span data-stu-id="04437-162">Failure to call **Shutdown** can result in memory links because the system may keep a reference to **IMFMediaSource** resources until **Shutdown** is called.</span></span>


```C++
if (g_pSource)
{
    g_pSource->Shutdown();
    g_pSource->Release();
    g_pSource = NULL;
}
```



<span data-ttu-id="04437-163">Se você alocou uma cadeia de caracteres que contém o link simbólico para um dispositivo de captura, deverá liberar esse objeto também.</span><span class="sxs-lookup"><span data-stu-id="04437-163">If you allocated a string containing the symbolic link to a capture device, you should release this object as well.</span></span>


```C++
    CoTaskMemFree(g_pwszSymbolicLink);
    g_pwszSymbolicLink = NULL;

    g_cchSymbolicLink = 0;
```



## <a name="related-topics"></a><span data-ttu-id="04437-164">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="04437-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04437-165">Captura de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="04437-165">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> </dl>

 

 
