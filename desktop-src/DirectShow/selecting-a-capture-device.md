---
description: Selecionando um dispositivo de captura
ms.assetid: 8f92873d-569a-48af-a913-6d4cce65640f
title: Selecionando um dispositivo de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b599728c6bd2d98b89285b6008923aa4fb2a3aef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105758048"
---
# <a name="selecting-a-capture-device"></a><span data-ttu-id="8e5a8-103">Selecionando um dispositivo de captura</span><span class="sxs-lookup"><span data-stu-id="8e5a8-103">Selecting a Capture Device</span></span>

<span data-ttu-id="8e5a8-104">Para selecionar um dispositivo de captura de áudio ou vídeo, use o [enumerador de dispositivo do sistema](system-device-enumerator.md), descrito no tópico [usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="8e5a8-104">To select an audio or video capture device, use the [System Device Enumerator](system-device-enumerator.md), described in the topic [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span> <span data-ttu-id="8e5a8-105">O enumerador de dispositivo do sistema retorna uma coleção de monikers de dispositivo, selecionada por categoria de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-105">The System Device Enumerator returns a collection of device monikers, selected by device category.</span></span> <span data-ttu-id="8e5a8-106">Um *moniker* é um objeto com que contém informações sobre outro objeto.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-106">A *moniker* is a COM object that contains information about another object.</span></span> <span data-ttu-id="8e5a8-107">Os monikers permitem que o aplicativo Obtenha informações sobre um objeto sem realmente criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-107">Monikers enable the application to get information about an object without actually creating the object.</span></span> <span data-ttu-id="8e5a8-108">Posteriormente, o aplicativo pode usar o moniker para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-108">Later, the application can use the moniker to create the object.</span></span> <span data-ttu-id="8e5a8-109">Para obter mais informações sobre monikers, consulte a documentação de [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker).</span><span class="sxs-lookup"><span data-stu-id="8e5a8-109">For more information about monikers, see the documentation for [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker).</span></span>

<span data-ttu-id="8e5a8-110">Para usar o enumerador de dispositivo do sistema, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-110">To use the System Device Enumerator, perform the following steps.</span></span>

1.  <span data-ttu-id="8e5a8-111">Chame [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para criar uma instância do enumerador de dispositivo do sistema.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-111">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create an instance of the System Device Enumerator.</span></span>
2.  <span data-ttu-id="8e5a8-112">Chame [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) e especifique a categoria de dispositivo como um GUID.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-112">Call [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) and specify the device category as a GUID.</span></span> <span data-ttu-id="8e5a8-113">Para dispositivos de captura, as categorias a seguir são relevantes.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-113">For capture devices, the following categories are relevant.</span></span> 

    | <span data-ttu-id="8e5a8-114">GUID da categoria</span><span class="sxs-lookup"><span data-stu-id="8e5a8-114">Category GUID</span></span>                       | <span data-ttu-id="8e5a8-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e5a8-115">Description</span></span>           |
    |-------------------------------------|-----------------------|
    | <span data-ttu-id="8e5a8-116">**\_AUDIOINPUTDEVICECATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="8e5a8-116">**CLSID\_AudioInputDeviceCategory**</span></span> | <span data-ttu-id="8e5a8-117">Dispositivos de captura de áudio</span><span class="sxs-lookup"><span data-stu-id="8e5a8-117">Audio capture devices</span></span> |
    | <span data-ttu-id="8e5a8-118">**\_VIDEOINPUTDEVICECATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="8e5a8-118">**CLSID\_VideoInputDeviceCategory**</span></span> | <span data-ttu-id="8e5a8-119">Dispositivos de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="8e5a8-119">Video capture devices</span></span> |

    

     

    <span data-ttu-id="8e5a8-120">Se uma câmera de vídeo tiver um microfone integrado, ela aparecerá em ambas as categorias.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-120">If a video camera has an integrated microphone, it appears in both categories.</span></span> <span data-ttu-id="8e5a8-121">No entanto, a câmera e o microfone são tratados como dispositivos separados pelo sistema, para fins de enumeração, criação de dispositivos e streaming de dados.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-121">However, the camera and microphone are treated as separate devices by the system, for purposes of enumeration, device creation, and data streaming.</span></span>

3.  <span data-ttu-id="8e5a8-122">O método [**CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) retorna um ponteiro para a interface [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) .</span><span class="sxs-lookup"><span data-stu-id="8e5a8-122">The [**CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) method returns a pointer to the [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) interface.</span></span> <span data-ttu-id="8e5a8-123">Para enumerar os monikers, chame [**IEnumMoniker:: Next**](/windows/win32/api/objidl/nf-objidl-ienummoniker-next).</span><span class="sxs-lookup"><span data-stu-id="8e5a8-123">To enumerate the monikers, call [**IEnumMoniker::Next**](/windows/win32/api/objidl/nf-objidl-ienummoniker-next).</span></span>

<span data-ttu-id="8e5a8-124">O código a seguir cria um enumerador para uma categoria de dispositivo especificada.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-124">The following code creates an enumerator for a specified device category.</span></span>


```C++
#include <windows.h>
#include <dshow.h>

#pragma comment(lib, "strmiids")

HRESULT EnumerateDevices(REFGUID category, IEnumMoniker **ppEnum)
{
    // Create the System Device Enumerator.
    ICreateDevEnum *pDevEnum;
    HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL,  
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pDevEnum));

    if (SUCCEEDED(hr))
    {
        // Create an enumerator for the category.
        hr = pDevEnum->CreateClassEnumerator(category, ppEnum, 0);
        if (hr == S_FALSE)
        {
            hr = VFW_E_NOT_FOUND;  // The category is empty. Treat as an error.
        }
        pDevEnum->Release();
    }
    return hr;
}
```



<span data-ttu-id="8e5a8-125">A interface [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) enumera uma lista de interfaces [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) , cada uma representando um moniker de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-125">The [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) interface enumerates a list of [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interfaces, each of which represents a device moniker.</span></span> <span data-ttu-id="8e5a8-126">O aplicativo pode ler as propriedades do moniker ou usar o moniker para criar um filtro de captura do DirectShow para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-126">The application can read properties from the moniker, or use the moniker to create a DirectShow capture filter for the device.</span></span> <span data-ttu-id="8e5a8-127">As propriedades de moniker são retornadas como valores de **variante** .</span><span class="sxs-lookup"><span data-stu-id="8e5a8-127">Moniker properties are returned as **VARIANT** values.</span></span> <span data-ttu-id="8e5a8-128">As propriedades a seguir têm suporte dos monikers de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-128">The following properties are supported by device monikers.</span></span>



| <span data-ttu-id="8e5a8-129">Propriedade</span><span class="sxs-lookup"><span data-stu-id="8e5a8-129">Property</span></span>       | <span data-ttu-id="8e5a8-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e5a8-130">Description</span></span>                                                               | <span data-ttu-id="8e5a8-131">Tipo de VARIANTE</span><span class="sxs-lookup"><span data-stu-id="8e5a8-131">VARIANT Type</span></span> |
|----------------|---------------------------------------------------------------------------|--------------|
| <span data-ttu-id="8e5a8-132">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8e5a8-132">"FriendlyName"</span></span> | <span data-ttu-id="8e5a8-133">O nome do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-133">The name of the device.</span></span>                                                   | <span data-ttu-id="8e5a8-134">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="8e5a8-134">**VT\_BSTR**</span></span> |
| <span data-ttu-id="8e5a8-135">Ndescrição</span><span class="sxs-lookup"><span data-stu-id="8e5a8-135">"Description"</span></span>  | <span data-ttu-id="8e5a8-136">Uma descrição do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-136">A description of the device.</span></span>                                              | <span data-ttu-id="8e5a8-137">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="8e5a8-137">**VT\_BSTR**</span></span> |
| <span data-ttu-id="8e5a8-138">DevicePath</span><span class="sxs-lookup"><span data-stu-id="8e5a8-138">"DevicePath"</span></span>   | <span data-ttu-id="8e5a8-139">Uma cadeia de caracteres exclusiva que identifica o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-139">A unique string that identifies the device.</span></span> <span data-ttu-id="8e5a8-140">(Somente dispositivos de captura de vídeo.)</span><span class="sxs-lookup"><span data-stu-id="8e5a8-140">(Video capture devices only.)</span></span> | <span data-ttu-id="8e5a8-141">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="8e5a8-141">**VT\_BSTR**</span></span> |
| <span data-ttu-id="8e5a8-142">"WaveInID"</span><span class="sxs-lookup"><span data-stu-id="8e5a8-142">"WaveInID"</span></span>     | <span data-ttu-id="8e5a8-143">O identificador de um dispositivo de captura de áudio.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-143">The identifier for an audio capture device.</span></span> <span data-ttu-id="8e5a8-144">(Somente dispositivos de captura de áudio.)</span><span class="sxs-lookup"><span data-stu-id="8e5a8-144">(Audio capture devices only.)</span></span> | <span data-ttu-id="8e5a8-145">**\_I4 VT**</span><span class="sxs-lookup"><span data-stu-id="8e5a8-145">**VT\_I4**</span></span>   |



 

<span data-ttu-id="8e5a8-146">As propriedades "FriendlyName" e "Description" são adequadas para exibição em uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-146">The "FriendlyName" and "Description" properties are suitable for displaying in a UI.</span></span>

-   <span data-ttu-id="8e5a8-147">A propriedade "FriendlyName" está disponível para cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-147">The "FriendlyName" property is available for every device.</span></span> <span data-ttu-id="8e5a8-148">Ele contém um nome legível para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-148">It contains a human-readable name for the device.</span></span>
-   <span data-ttu-id="8e5a8-149">A propriedade "Description" está disponível apenas para dispositivos DV e D-VHS/MPEG.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-149">The "Description" property is available only for DV and D-VHS/MPEG camcorder devices.</span></span> <span data-ttu-id="8e5a8-150">Para obter mais informações, consulte [Driver MSDV](msdv-driver.md) e [Driver MSTape](mstape-driver.md).</span><span class="sxs-lookup"><span data-stu-id="8e5a8-150">For more information, see [MSDV Driver](msdv-driver.md) and [MSTape Driver](mstape-driver.md).</span></span> <span data-ttu-id="8e5a8-151">Se disponível, ele contém uma descrição do dispositivo que é mais específico do que a propriedade "FriendlyName".</span><span class="sxs-lookup"><span data-stu-id="8e5a8-151">If available, it contains a description of the device which is more specific than the "FriendlyName" property.</span></span> <span data-ttu-id="8e5a8-152">Normalmente, ele inclui o nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-152">Typically it includes the vendor name.</span></span>
-   <span data-ttu-id="8e5a8-153">A propriedade "DevicePath" não é uma cadeia de caracteres legível, mas é garantido que seja exclusivo para cada dispositivo de captura de vídeo no sistema.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-153">The "DevicePath" property is not a human-readable string, but is guaranteed to be unique for each video capture device on the system.</span></span> <span data-ttu-id="8e5a8-154">Você pode usar essa propriedade para distinguir entre duas ou mais instâncias do mesmo modelo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-154">You can use this property to distinguish between two or more instances of the same model of device.</span></span>
-   <span data-ttu-id="8e5a8-155">Se a propriedade "WaveInID" estiver presente, isso significa que o filtro de captura do DirectShow usa as APIs de áudio da forma de [onda](../multimedia/waveform-audio.md) internamente para se comunicar com o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-155">If the "WaveInID" property is present, it means the DirectShow capture filter uses the [Waveform Audio](../multimedia/waveform-audio.md) APIs internally to communicate with the device.</span></span> <span data-ttu-id="8e5a8-156">O valor da propriedade "WaveInID" corresponde ao identificador usado pelas funções \**Wave \** _, como [_ *waveInOpen* \*](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen).</span><span class="sxs-lookup"><span data-stu-id="8e5a8-156">The value of the "WaveInID" property corresponds to the identifier used by the \**waveIn\** _ functions, such as [_ *waveInOpen*\*](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen).</span></span>

<span data-ttu-id="8e5a8-157">Para ler as propriedades do moniker, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-157">To read properties from the moniker, perform the following steps.</span></span>

1.  <span data-ttu-id="8e5a8-158">Chame [**IMoniker:: BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) para obter um ponteiro para a interface [**IPropertyBag**](../com/ipropertybag-and-ipersistpropertybag.md) .</span><span class="sxs-lookup"><span data-stu-id="8e5a8-158">Call [**IMoniker::BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) to get a pointer to the [**IPropertyBag**](../com/ipropertybag-and-ipersistpropertybag.md) interface.</span></span>
2.  <span data-ttu-id="8e5a8-159">Chame **IPropertyBag:: Read** para ler a propriedade.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-159">Call **IPropertyBag::Read** to read the property.</span></span>

<span data-ttu-id="8e5a8-160">O exemplo de código a seguir mostra como enumerar uma lista de monikers de dispositivo e obter as propriedades.</span><span class="sxs-lookup"><span data-stu-id="8e5a8-160">The following code example shows how to enumerate a list of device monikers and get the properties.</span></span>


```C++
void DisplayDeviceInformation(IEnumMoniker *pEnum)
{
    IMoniker *pMoniker = NULL;

    while (pEnum->Next(1, &pMoniker, NULL) == S_OK)
    {
        IPropertyBag *pPropBag;
        HRESULT hr = pMoniker->BindToStorage(0, 0, IID_PPV_ARGS(&pPropBag));
        if (FAILED(hr))
        {
            pMoniker->Release();
            continue;  
        } 

        VARIANT var;
        VariantInit(&var);

        // Get description or friendly name.
        hr = pPropBag->Read(L"Description", &var, 0);
        if (FAILED(hr))
        {
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
        }
        if (SUCCEEDED(hr))
        {
            printf("%S\n", var.bstrVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Write(L"FriendlyName", &var);

        // WaveInID applies only to audio capture devices.
        hr = pPropBag->Read(L"WaveInID", &var, 0);
        if (SUCCEEDED(hr))
        {
            printf("WaveIn ID: %d\n", var.lVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Read(L"DevicePath", &var, 0);
        if (SUCCEEDED(hr))
        {
            // The device path is not intended for display.
            printf("Device path: %S\n", var.bstrVal);
            VariantClear(&var); 
        }

        pPropBag->Release();
        pMoniker->Release();
    }
}

void main()
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (SUCCEEDED(hr))
    {
        IEnumMoniker *pEnum;

        hr = EnumerateDevices(CLSID_VideoInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        hr = EnumerateDevices(CLSID_AudioInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        CoUninitialize();
    }
}
```



<span data-ttu-id="8e5a8-161">Para criar um filtro de captura do DirectShow para o dispositivo, chame o método [**IMoniker:: BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) para obter um ponteiro [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="8e5a8-161">To create a DirectShow capture filter for the device, call the [**IMoniker::BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) method to get an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) pointer.</span></span> <span data-ttu-id="8e5a8-162">Em seguida, chame [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para adicionar o filtro ao grafo de filtro:</span><span class="sxs-lookup"><span data-stu-id="8e5a8-162">Then call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add the filter to the filter graph:</span></span>


```C++
IBaseFilter *pCap = NULL;
hr = pMoniker->BindToObject(0, 0, IID_IBaseFilter, (void**)&pCap);
if (SUCCEEDED(hr))
{
    hr = m_pGraph->AddFilter(pCap, L"Capture Filter");
}
```



## <a name="related-topics"></a><span data-ttu-id="8e5a8-163">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8e5a8-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e5a8-164">Captura de áudio</span><span class="sxs-lookup"><span data-stu-id="8e5a8-164">Audio Capture</span></span>](audio-capture.md)
</dt> <dt>

[<span data-ttu-id="8e5a8-165">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="8e5a8-165">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 
