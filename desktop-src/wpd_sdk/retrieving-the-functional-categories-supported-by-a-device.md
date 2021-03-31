---
description: Recuperando as categorias funcionais com suporte de um dispositivo
ms.assetid: 7748e111-9987-4685-8fc8-10c5d4631080
title: Recuperando as categorias funcionais com suporte de um dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6514c6255fa089dc235b5edd8a25b5ef581aee84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829201"
---
# <a name="retrieving-the-functional-categories-supported-by-a-device"></a><span data-ttu-id="1433c-103">Recuperando as categorias funcionais com suporte de um dispositivo</span><span class="sxs-lookup"><span data-stu-id="1433c-103">Retrieving the Functional Categories Supported by a Device</span></span>

<span data-ttu-id="1433c-104">Os dispositivos portáteis do Windows podem oferecer suporte a uma ou mais categorias funcionais.</span><span class="sxs-lookup"><span data-stu-id="1433c-104">Windows Portable Devices may support one or more functional categories.</span></span> <span data-ttu-id="1433c-105">Essas categorias são descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1433c-105">These categories are described in the following table.</span></span>



| <span data-ttu-id="1433c-106">Categoria</span><span class="sxs-lookup"><span data-stu-id="1433c-106">Category</span></span>                    | <span data-ttu-id="1433c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1433c-107">Description</span></span>                                                                          |
|-----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1433c-108">Captura de áudio</span><span class="sxs-lookup"><span data-stu-id="1433c-108">Audio capture</span></span>               | <span data-ttu-id="1433c-109">O dispositivo pode ser usado para gravar áudio.</span><span class="sxs-lookup"><span data-stu-id="1433c-109">The device can be used to record audio.</span></span>                                              |
| <span data-ttu-id="1433c-110">Informações de renderização</span><span class="sxs-lookup"><span data-stu-id="1433c-110">Rendering information</span></span>       | <span data-ttu-id="1433c-111">O dispositivo fornece dados que descrevem os arquivos de mídia que são capazes de renderizar.</span><span class="sxs-lookup"><span data-stu-id="1433c-111">The device provides data describing the media files that it is capable of rendering.</span></span> |
| <span data-ttu-id="1433c-112">SMS (serviço de mensagens curtas)</span><span class="sxs-lookup"><span data-stu-id="1433c-112">Short message service (SMS)</span></span> | <span data-ttu-id="1433c-113">O dispositivo dá suporte a mensagens de texto.</span><span class="sxs-lookup"><span data-stu-id="1433c-113">The device supports text messaging.</span></span>                                                  |
| <span data-ttu-id="1433c-114">Captura de imagem ainda</span><span class="sxs-lookup"><span data-stu-id="1433c-114">Still image capture</span></span>         | <span data-ttu-id="1433c-115">O dispositivo pode ser usado para capturar imagens ainda.</span><span class="sxs-lookup"><span data-stu-id="1433c-115">The device can be used to capture still images.</span></span>                                      |
| <span data-ttu-id="1433c-116">Armazenamento</span><span class="sxs-lookup"><span data-stu-id="1433c-116">Storage</span></span>                     | <span data-ttu-id="1433c-117">O dispositivo pode ser usado para armazenar arquivos.</span><span class="sxs-lookup"><span data-stu-id="1433c-117">The device can be used to store files.</span></span>                                               |



 

<span data-ttu-id="1433c-118">A função ListFunctionalCategories no módulo DeviceCapabilities. cpp demonstra a recuperação de categorias funcionais para um dispositivo selecionado.</span><span class="sxs-lookup"><span data-stu-id="1433c-118">The ListFunctionalCategories function in the DeviceCapabilities.cpp module demonstrates the retrieval of functional categories for a selected device.</span></span>

<span data-ttu-id="1433c-119">Seu aplicativo pode recuperar as categorias funcionais com suporte de um dispositivo usando as interfaces descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1433c-119">Your application can retrieve the functional categories supported by a device by using the interfaces described in the following table.</span></span>



| <span data-ttu-id="1433c-120">Interface</span><span class="sxs-lookup"><span data-stu-id="1433c-120">Interface</span></span>                                                                                      | <span data-ttu-id="1433c-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="1433c-121">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="1433c-122">**Interface IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1433c-122">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="1433c-123">Fornece acesso aos métodos de recuperação de categoria funcional.</span><span class="sxs-lookup"><span data-stu-id="1433c-123">Provides access to the functional-category retrieval methods.</span></span> |
| [<span data-ttu-id="1433c-124">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="1433c-124">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="1433c-125">Usado para enumerar e armazenar dados de categoria funcional.</span><span class="sxs-lookup"><span data-stu-id="1433c-125">Used to enumerate and store functional-category data.</span></span>         |



 

<span data-ttu-id="1433c-126">A primeira tarefa realizada pelo aplicativo de exemplo é a recuperação de um objeto [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) , que é usado para recuperar as categorias funcionais no dispositivo selecionado.</span><span class="sxs-lookup"><span data-stu-id="1433c-126">The first task accomplished by the sample application is the retrieval of an [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) object, which is used to retrieve the functional categories on the selected device.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pCategories;
DWORD dwNumCategories = 0;

if (pDevice == NULL)
{
    printf("! A NULL IPortableDevice interface pointer was received\n");
    return;
}

// Get an IPortableDeviceCapabilities interface from the IPortableDevice interface to
// access the device capabilities-specific methods.
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}

// Get all functional categories supported by the device.
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalCategories(&pCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get functional categories from the device, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="1433c-127">As categorias recuperadas são armazenadas em um objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="1433c-127">The retrieved categories are stored in an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="1433c-128">A próxima etapa é a enumeração e a exibição das categorias com suporte.</span><span class="sxs-lookup"><span data-stu-id="1433c-128">The next step is the enumeration and display of the supported categories.</span></span> <span data-ttu-id="1433c-129">A primeira etapa que o aplicativo de exemplo realiza é recuperar a contagem de categorias com suporte.</span><span class="sxs-lookup"><span data-stu-id="1433c-129">The first step that the sample application accomplishes is to retrieve the count of supported categories.</span></span> <span data-ttu-id="1433c-130">Em seguida, ele usa essa contagem para iterar por meio do objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contém as categorias com suporte.</span><span class="sxs-lookup"><span data-stu-id="1433c-130">It then uses this count to iterate through the [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object that contains the supported categories.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pCategories->GetCount(&dwNumCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get number of functional categories, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Functional Categories Found on the device\n\n", dwNumCategories);

// Loop through each functional category and display its name
if (SUCCEEDED(hr))
{
    for (DWORD dwIndex = 0; dwIndex < dwNumCategories; dwIndex++)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);
        hr = pCategories->GetAt(dwIndex, &pv);
        if (SUCCEEDED(hr))
        {
            // We have a functional category.  It is assumed that
            // functional categories are returned as VT_CLSID
            // VarTypes.

            if (pv.puuid != NULL)
            {
                // Display the functional category name
                DisplayFunctionalCategory(*pv.puuid);
                printf("\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="1433c-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1433c-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1433c-132">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="1433c-132">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="1433c-133">**Interface IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1433c-133">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="1433c-134">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="1433c-134">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="1433c-135">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="1433c-135">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



