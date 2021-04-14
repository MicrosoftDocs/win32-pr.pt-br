---
description: Este tópico descreve como enumerar os dispositivos de captura de vídeo no sistema de usuários e como criar uma instância de um dispositivo.
ms.assetid: b1267478-329b-4e46-a2ed-1ec11d2e2e6d
title: Enumerando dispositivos de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ccdbcf9df284cdccda09939d2d8a27174a2299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370526"
---
# <a name="enumerating-video-capture-devices"></a><span data-ttu-id="2943b-103">Enumerando dispositivos de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="2943b-103">Enumerating Video Capture Devices</span></span>

<span data-ttu-id="2943b-104">Este tópico descreve como enumerar os dispositivos de captura de vídeo no sistema do usuário e como criar uma instância de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2943b-104">This topic describes how to enumerate the video capture devices on the user's system, and how create an instance of a device.</span></span>

<span data-ttu-id="2943b-105">Para enumerar os dispositivos de captura de vídeo no sistema, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="2943b-105">To enumerate the video capture devices on the system, do the following:</span></span>

1.  <span data-ttu-id="2943b-106">Chame [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para criar um repositório de atributos.</span><span class="sxs-lookup"><span data-stu-id="2943b-106">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store.</span></span> <span data-ttu-id="2943b-107">Essa função recebe um ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="2943b-107">This function receives an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="2943b-108">Chame [**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid) para definir o atributo de [ \_ tipo de origem do \_ atributo \_ \_ MF DEVSOURCE](mf-devsource-attribute-source-type.md) .</span><span class="sxs-lookup"><span data-stu-id="2943b-108">Call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid) to set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute.</span></span> <span data-ttu-id="2943b-109">Defina o valor do atributo como **MF \_ DEVSOURCE \_ atributo \_ Source \_ tipo \_ VIDCAP \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="2943b-109">Set the attribute value to **MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**.</span></span>
3.  <span data-ttu-id="2943b-110">Chame [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources).</span><span class="sxs-lookup"><span data-stu-id="2943b-110">Call [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources).</span></span> <span data-ttu-id="2943b-111">Essa função recebe uma matriz de ponteiros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) e o tamanho da matriz.</span><span class="sxs-lookup"><span data-stu-id="2943b-111">This function receives an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers and the array size.</span></span> <span data-ttu-id="2943b-112">Cada ponteiro representa um dispositivo de captura de vídeo distinto.</span><span class="sxs-lookup"><span data-stu-id="2943b-112">Each pointer represents a distinct video capture device.</span></span>

<span data-ttu-id="2943b-113">Para criar uma instância de um dispositivo de captura:</span><span class="sxs-lookup"><span data-stu-id="2943b-113">To create an instance of a capture device:</span></span>

-   <span data-ttu-id="2943b-114">Chame [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) para obter um ponteiro para a interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) .</span><span class="sxs-lookup"><span data-stu-id="2943b-114">Call [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) to get a pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span>

<span data-ttu-id="2943b-115">O código a seguir mostra estas etapas:</span><span class="sxs-lookup"><span data-stu-id="2943b-115">The following code shows these steps:</span></span>


```C++
HRESULT CreateVideoDeviceSource(IMFMediaSource **ppSource)
{
    *ppSource = NULL;

    IMFMediaSource *pSource = NULL;
    IMFAttributes *pAttributes = NULL;
    IMFActivate **ppDevices = NULL;

    // Create an attribute store to specify the enumeration parameters.
    HRESULT hr = MFCreateAttributes(&pAttributes, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    // Source type: video capture devices
    hr = pAttributes->SetGUID(
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE, 
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Enumerate devices.
    UINT32 count;
    hr = MFEnumDeviceSources(pAttributes, &ppDevices, &count);
    if (FAILED(hr))
    {
        goto done;
    }

    if (count == 0)
    {
        hr = E_FAIL;
        goto done;
    }

    // Create the media source object.
    hr = ppDevices[0]->ActivateObject(IID_PPV_ARGS(&pSource));
    if (FAILED(hr))
    {
        goto done;
    }

    *ppSource = pSource;
    (*ppSource)->AddRef();

done:
    SafeRelease(&pAttributes);

    for (DWORD i = 0; i < count; i++)
    {
        SafeRelease(&ppDevices[i]);
    }
    CoTaskMemFree(ppDevices);
    SafeRelease(&pSource);
    return hr;
}
```



<span data-ttu-id="2943b-116">Depois de criar a origem de mídia, libere os ponteiros de interface e libere a memória para a matriz:</span><span class="sxs-lookup"><span data-stu-id="2943b-116">After you create media source, release the interface pointers and free the memory for the array:</span></span>


```C++
    SafeRelease(&pAttributes);

    for (DWORD i = 0; i < count; i++)
    {
        SafeRelease(&ppDevices[i]);
    }
    CoTaskMemFree(ppDevices);
```



## <a name="related-topics"></a><span data-ttu-id="2943b-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2943b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2943b-118">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="2943b-118">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



