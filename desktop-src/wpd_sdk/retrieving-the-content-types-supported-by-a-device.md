---
description: Recuperando os tipos de conteúdo com suporte de um dispositivo
ms.assetid: 1cedb8d9-2476-420c-bab4-c8a032af781b
title: Recuperando os tipos de conteúdo com suporte de um dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e1b37160065be3130fca687f5f3277d9108a6ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765095"
---
# <a name="retrieving-the-content-types-supported-by-a-device"></a><span data-ttu-id="890d7-103">Recuperando os tipos de conteúdo com suporte de um dispositivo</span><span class="sxs-lookup"><span data-stu-id="890d7-103">Retrieving the Content Types Supported by a Device</span></span>

<span data-ttu-id="890d7-104">Conforme observado no tópico [recuperando as categorias funcionais com suporte de um dispositivo](retrieving-the-functional-categories-supported-by-a-device.md) , os dispositivos portáteis do Windows podem dar suporte a uma ou mais categorias funcionais.</span><span class="sxs-lookup"><span data-stu-id="890d7-104">As noted in the [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic, Windows Portable Devices may support one or more functional categories.</span></span> <span data-ttu-id="890d7-105">Qualquer categoria funcional específica pode dar suporte a um ou mais tipos de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="890d7-105">Any given functional category may support one or more content types.</span></span> <span data-ttu-id="890d7-106">Por exemplo, a categoria de armazenamento pode dar suporte a tipos de conteúdo de pasta, áudio e imagem.</span><span class="sxs-lookup"><span data-stu-id="890d7-106">For example, the storage category may support content types of folder, audio, and image.</span></span>

<span data-ttu-id="890d7-107">Para obter uma descrição dos tipos de conteúdo com suporte no WPD, consulte o tópico [**\_ tipo de conteúdo WPD \_ \_ todos**](wpd-content-type-all.md) .</span><span class="sxs-lookup"><span data-stu-id="890d7-107">For a description of the content types supported by WPD, see the [**WPD\_CONTENT\_TYPE\_ALL**](wpd-content-type-all.md) topic.</span></span>

<span data-ttu-id="890d7-108">A função ListSupportedContentTypes no módulo DeviceCapabilities. cpp demonstra a recuperação de tipos de conteúdo para as categorias funcionais com suporte de um dispositivo selecionado.</span><span class="sxs-lookup"><span data-stu-id="890d7-108">The ListSupportedContentTypes function in the DeviceCapabilities.cpp module demonstrates the retrieval of content types for the functional categories supported by a selected device.</span></span>

<span data-ttu-id="890d7-109">Seu aplicativo pode recuperar as categorias funcionais com suporte de um dispositivo usando as interfaces descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="890d7-109">Your application can retrieve the functional categories supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="890d7-110">Interface</span><span class="sxs-lookup"><span data-stu-id="890d7-110">Interface</span></span>                                                                                      | <span data-ttu-id="890d7-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="890d7-111">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="890d7-112">**Interface IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="890d7-112">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="890d7-113">Fornece acesso aos métodos de recuperação de categoria funcional.</span><span class="sxs-lookup"><span data-stu-id="890d7-113">Provides access to the functional-category retrieval methods.</span></span> |
| [<span data-ttu-id="890d7-114">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="890d7-114">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="890d7-115">Usado para enumerar e armazenar dados de categoria funcional.</span><span class="sxs-lookup"><span data-stu-id="890d7-115">Used to enumerate and store functional-category data.</span></span>         |



 

<span data-ttu-id="890d7-116">O código encontrado na função ListSupportedContentTypes é quase idêntico ao código encontrado na função ListFunctionalCategories.</span><span class="sxs-lookup"><span data-stu-id="890d7-116">The code found in the ListSupportedContentTypes function is almost identical to the code found in the ListFunctionalCategories function.</span></span> <span data-ttu-id="890d7-117">(Consulte o tópico [recuperando categorias funcionais com suporte em um dispositivo](retrieving-the-functional-categories-supported-by-a-device.md) .) A única diferença é a chamada para o método [**IPortableDeviceCapabilities:: GetSupportedContentTypes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedcontenttypes) , que aparece dentro do loop que itera pelas categorias funcionais.</span><span class="sxs-lookup"><span data-stu-id="890d7-117">(See the [Retrieving Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic.) The one difference is the call to the [**IPortableDeviceCapabilities::GetSupportedContentTypes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedcontenttypes) method, which appears within the loop that iterates through the functional categories.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pCategories;
DWORD dwNumCategories   = 0;

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
// We will use these categories to enumerate functional objects
// that fall within them.
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalCategories(&pCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get functional categories from the device, hr = 0x%lx\n",hr);
    }
}

// Get the number of functional categories found on the device.
if (SUCCEEDED(hr))
{
    hr = pCategories->GetCount(&dwNumCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get number of functional categories, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Functional Categories Found on the device\n\n", dwNumCategories);

// Loop through each functional category and display its name and supported content types.
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

            if ((pv.puuid != NULL)      &&
                (pv.vt    == VT_CLSID))
            {
                // Display the functional category name
                printf("Functional Category: ");
                DisplayFunctionalCategory(*pv.puuid);
                printf("\n");

                // Display the content types supported for this category
                CComPtr<IPortableDevicePropVariantCollection> pContentTypes;
                hr = pCapabilities->GetSupportedContentTypes(*pv.puuid, &pContentTypes);
                if (SUCCEEDED(hr))
                {
                    printf("Supported Content Types: ");
                    DisplayContentTypes(pContentTypes);
                    printf("\n\n");
                }
                else
                {
                    printf("! Failed to get supported content types from the device, hr = 0x%lx\n",hr);
                }
            }
            else
            {
                printf("! Invalid functional category found\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="890d7-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="890d7-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="890d7-119">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="890d7-119">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="890d7-120">**Interface IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="890d7-120">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="890d7-121">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="890d7-121">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="890d7-122">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="890d7-122">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



