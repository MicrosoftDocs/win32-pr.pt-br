---
description: Enumerando conteúdo
ms.assetid: 86782a09-4fca-4ae0-beaf-296069e061dc
title: Enumerando conteúdo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2e724b451d714516c4723edcd56936b71e4e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759009"
---
# <a name="enumerating-content"></a><span data-ttu-id="d1f9d-103">Enumerando conteúdo</span><span class="sxs-lookup"><span data-stu-id="d1f9d-103">Enumerating Content</span></span>

<span data-ttu-id="d1f9d-104">O conteúdo em um dispositivo (se esse conteúdo é uma pasta, um catálogo de telefones, um vídeo ou uma imagem ainda) é chamado de objeto na API WPD.</span><span class="sxs-lookup"><span data-stu-id="d1f9d-104">The content on a device (whether that content is a folder, a phone book, a video, or a still image) is called an object in the WPD API.</span></span> <span data-ttu-id="d1f9d-105">Esses objetos são referenciados por identificadores de objeto e descritos por propriedades.</span><span class="sxs-lookup"><span data-stu-id="d1f9d-105">These objects are referenced by object identifiers and described by properties.</span></span> <span data-ttu-id="d1f9d-106">Você pode enumerar os objetos em um dispositivo chamando métodos na [**interface IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice), na interface [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)e na [**interface IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).</span><span class="sxs-lookup"><span data-stu-id="d1f9d-106">You can enumerate the objects on a device by calling methods in the [**IPortableDevice interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice), the [**IPortableDeviceContent interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent), and the [**IEnumPortableDeviceObjectIDs interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).</span></span>

<span data-ttu-id="d1f9d-107">O aplicativo de exemplo demonstra a enumeração de conteúdo na função EnumerateAllContent que é encontrada no módulo ContentEnumeration. cpp.</span><span class="sxs-lookup"><span data-stu-id="d1f9d-107">The sample application demonstrates content enumeration in the EnumerateAllContent function that is found in the ContentEnumeration.cpp module.</span></span> <span data-ttu-id="d1f9d-108">Essa função, por sua vez, chama uma função RecursiveEnumerate que percorre a hierarquia de objetos encontrados no dispositivo selecionado e retorna um identificador de objeto para cada objeto.</span><span class="sxs-lookup"><span data-stu-id="d1f9d-108">This function, in turn, calls a RecursiveEnumerate function that walks the hierarchy of objects found on the selected device and returns an object identifier for each object.</span></span>

<span data-ttu-id="d1f9d-109">Como observado, a função RecursiveEnumerate recupera um identificador de objeto para cada objeto encontrado no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1f9d-109">As noted, the RecursiveEnumerate function retrieves an object identifier for each object found on the device.</span></span> <span data-ttu-id="d1f9d-110">O identificador de objeto é um valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d1f9d-110">The object identifier is a string value.</span></span> <span data-ttu-id="d1f9d-111">Depois que o aplicativo recupera esse identificador, ele pode obter informações de objeto mais descritivas (como o nome do objeto, o identificador para o pai do objeto e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="d1f9d-111">Once your application retrieves this identifier, it can obtain more descriptive object information (such as the object's name, the identifier for the object's parent, and so on).</span></span> <span data-ttu-id="d1f9d-112">Essas informações descritivas são chamadas de propriedades de objeto (ou metadados).</span><span class="sxs-lookup"><span data-stu-id="d1f9d-112">This descriptive information is referred to as object properties (or metadata).</span></span> <span data-ttu-id="d1f9d-113">Seu aplicativo pode recuperar essas propriedades chamando membros da [**interface IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties).</span><span class="sxs-lookup"><span data-stu-id="d1f9d-113">Your application can retrieve these properties by calling members of the [**IPortableDeviceProperties interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties).</span></span>

<span data-ttu-id="d1f9d-114">A função EnumerateAllContent começa recuperando um ponteiro para uma [**interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent).</span><span class="sxs-lookup"><span data-stu-id="d1f9d-114">The EnumerateAllContent function begins by retrieving a pointer to an [**IPortableDeviceContent interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent).</span></span> <span data-ttu-id="d1f9d-115">Ele recupera esse ponteiro chamando o método [**IPortableDevice:: content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) .</span><span class="sxs-lookup"><span data-stu-id="d1f9d-115">It retrieves this pointer by calling the [**IPortableDevice::Content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) method.</span></span>


```C++
void EnumerateAllContent(
    IPortableDevice* pDevice)
{
    HRESULT                         hr = S_OK;
    CComPtr<IPortableDeviceContent> pContent;

    if (pDevice == NULL)
    {
        printf("! A NULL IPortableDevice interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceContent interface from the IPortableDevice interface to
    // access the content-specific methods.
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }

    // Enumerate content starting from the "DEVICE" object.
    if (SUCCEEDED(hr))
    {
        printf("\n");
        RecursiveEnumerate(WPD_DEVICE_OBJECT_ID, pContent);
    }
}
```



<span data-ttu-id="d1f9d-116">Depois de recuperar o ponteiro para a interface IPortableDeviceContent, a função EnumerateAllContent chama a função RecursiveEnumerate, que percorre a hierarquia de objetos encontrados no dispositivo fornecido e retorna um identificador de objeto para cada um.</span><span class="sxs-lookup"><span data-stu-id="d1f9d-116">Once it retrieves the pointer to the IPortableDeviceContent interface, the EnumerateAllContent function calls the RecursiveEnumerate function, which walks the hierarchy of objects found on the given device and returns an object identifier for each.</span></span>

<span data-ttu-id="d1f9d-117">A função RecursiveEnumerate começa recuperando um ponteiro para uma [**interface IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).</span><span class="sxs-lookup"><span data-stu-id="d1f9d-117">The RecursiveEnumerate function begins by retrieving a pointer to an [**IEnumPortableDeviceObjectIDs interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).</span></span> <span data-ttu-id="d1f9d-118">Essa interface expõe os métodos que um aplicativo usa para navegar na lista de objetos encontrados em um determinado dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1f9d-118">This interface exposes the methods that an application uses to navigate the list of objects found on a given device.</span></span>

<span data-ttu-id="d1f9d-119">Neste exemplo, a função RecursiveEnumerate chama o método [**IEnumPortableDeviceObjectIDs:: Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) para atravessar a lista de objetos.</span><span class="sxs-lookup"><span data-stu-id="d1f9d-119">In this sample, the RecursiveEnumerate function calls the [**IEnumPortableDeviceObjectIDs::Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) method to traverse the list of objects.</span></span>

<span data-ttu-id="d1f9d-120">Cada chamada para o método [**IEnumPortableDeviceObjects:: Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) solicita um lote de 10 identificadores.</span><span class="sxs-lookup"><span data-stu-id="d1f9d-120">Each call to the [**IEnumPortableDeviceObjects::Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) method requests a batch of 10 identifiers.</span></span> <span data-ttu-id="d1f9d-121">(Esse valor é especificado pelo número \_ OBJETOS \_ para \_ solicitar constante que é fornecida como o primeiro argumento.)</span><span class="sxs-lookup"><span data-stu-id="d1f9d-121">(This value is specified by the NUM\_OBJECTS\_TO\_REQUEST constant that is supplied as the first argument.)</span></span>


```C++
#define NUM_OBJECTS_TO_REQUEST  10

// Recursively called function which enumerates using the specified
// object identifier as the parent.
void RecursiveEnumerate(
    PCWSTR                  pszObjectID,
    IPortableDeviceContent* pContent)
{
    CComPtr<IEnumPortableDeviceObjectIDs> pEnumObjectIDs;

    // Print the object identifier being used as the parent during enumeration.
    printf("%ws\n",pszObjectID);

    // Get an IEnumPortableDeviceObjectIDs interface by calling EnumObjects with the
    // specified parent object identifier.
    HRESULT hr = pContent->EnumObjects(0,               // Flags are unused
                                       pszObjectID,     // Starting from the passed in object
                                       NULL,            // Filter is unused
                                       &pEnumObjectIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get IEnumPortableDeviceObjectIDs from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }

    // Loop calling Next() while S_OK is being returned.
    while(hr == S_OK)
    {
        DWORD  cFetched = 0;
        PWSTR  szObjectIDArray[NUM_OBJECTS_TO_REQUEST] = {0};
        hr = pEnumObjectIDs->Next(NUM_OBJECTS_TO_REQUEST,   // Number of objects to request on each NEXT call
                                  szObjectIDArray,          // Array of PWSTR array which will be populated on each NEXT call
                                  &cFetched);               // Number of objects written to the PWSTR array
        if (SUCCEEDED(hr))
        {
            // Traverse the results of the Next() operation and recursively enumerate
            // Remember to free all returned object identifiers using CoTaskMemFree()
            for (DWORD dwIndex = 0; dwIndex < cFetched; dwIndex++)
            {
                RecursiveEnumerate(szObjectIDArray[dwIndex],pContent);

                // Free allocated PWSTRs after the recursive enumeration call has completed.
                CoTaskMemFree(szObjectIDArray[dwIndex]);
                szObjectIDArray[dwIndex] = NULL;
            }
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="d1f9d-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1f9d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1f9d-123">**Interface IEnumPortableDeviceObjectIDs**</span><span class="sxs-lookup"><span data-stu-id="d1f9d-123">**IEnumPortableDeviceObjectIDs Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[<span data-ttu-id="d1f9d-124">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="d1f9d-124">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="d1f9d-125">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="d1f9d-125">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="d1f9d-126">**Interface IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="d1f9d-126">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="d1f9d-127">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="d1f9d-127">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



