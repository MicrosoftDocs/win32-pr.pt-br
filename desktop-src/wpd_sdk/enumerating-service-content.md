---
description: Enumerando o conteúdo do serviço
ms.assetid: 4af4201c-d3f6-4630-91ec-6509c51871a5
title: Enumerando o conteúdo do serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2b701bdab867e96bc9658e2624ea18aa65dfc33
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424246"
---
# <a name="enumerating-service-content"></a><span data-ttu-id="9e030-103">Enumerando o conteúdo do serviço</span><span class="sxs-lookup"><span data-stu-id="9e030-103">Enumerating Service Content</span></span>

<span data-ttu-id="9e030-104">Depois que o aplicativo abre um serviço, ele pode começar a executar operações relacionadas ao serviço.</span><span class="sxs-lookup"><span data-stu-id="9e030-104">After your application opens a service, it can begin performing service-related operations.</span></span> <span data-ttu-id="9e030-105">No caso do aplicativo WpdServicesApiSample, uma dessas operações é a enumeração de conteúdo para um determinado serviço de contatos.</span><span class="sxs-lookup"><span data-stu-id="9e030-105">In the case of the WpdServicesApiSample application, one of these operations is the enumeration of content for a given Contacts service.</span></span> <span data-ttu-id="9e030-106">A tabela a seguir descreve as interfaces usadas.</span><span class="sxs-lookup"><span data-stu-id="9e030-106">The following table describes the interfaces used.</span></span>



| <span data-ttu-id="9e030-107">Interface</span><span class="sxs-lookup"><span data-stu-id="9e030-107">Interface</span></span>                                                            | <span data-ttu-id="9e030-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9e030-108">Description</span></span>                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e030-109">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="9e030-109">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | <span data-ttu-id="9e030-110">Usado para recuperar a interface IPortableDeviceContent2 para acessar o conteúdo no serviço.</span><span class="sxs-lookup"><span data-stu-id="9e030-110">Used to retrieve the IPortableDeviceContent2 interface to access content on the service.</span></span>         |
| [<span data-ttu-id="9e030-111">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="9e030-111">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | <span data-ttu-id="9e030-112">Usado para recuperar a interface IEnumPortableDeviceObjectIDs para enumerar objetos no serviço.</span><span class="sxs-lookup"><span data-stu-id="9e030-112">Used to retrieve the IEnumPortableDeviceObjectIDs interface to enumerate objects on the service.</span></span> |
| [<span data-ttu-id="9e030-113">**IEnumPortableDeviceObjectIDs**</span><span class="sxs-lookup"><span data-stu-id="9e030-113">**IEnumPortableDeviceObjectIDs**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids) | <span data-ttu-id="9e030-114">Usado para enumerar objetos no serviço.</span><span class="sxs-lookup"><span data-stu-id="9e030-114">Used to enumerate objects on the service.</span></span>                                                        |



 

<span data-ttu-id="9e030-115">O código de enumeração de conteúdo é encontrado no módulo ContentEnumeration. cpp.</span><span class="sxs-lookup"><span data-stu-id="9e030-115">The content enumeration code is found in the ContentEnumeration.cpp module.</span></span> <span data-ttu-id="9e030-116">Esse código reside nos métodos **EnumerateAllContent** e **RecursiveEnumerate** .</span><span class="sxs-lookup"><span data-stu-id="9e030-116">This code resides in the **EnumerateAllContent** and the **RecursiveEnumerate** methods.</span></span> <span data-ttu-id="9e030-117">O método anterior chama o último.</span><span class="sxs-lookup"><span data-stu-id="9e030-117">The former method calls the latter.</span></span>

<span data-ttu-id="9e030-118">O método **EnumerateContent** usa um ponteiro para um objeto [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9e030-118">The **EnumerateContent** method takes a pointer to an [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) object as its one parameter.</span></span> <span data-ttu-id="9e030-119">Esse objeto corresponde a um serviço que o aplicativo abriu anteriormente quando ele chamou o método [**IPortableDeviceService:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open) .</span><span class="sxs-lookup"><span data-stu-id="9e030-119">This object corresponds to a service that the application opened earlier when it called the [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open) method.</span></span>

<span data-ttu-id="9e030-120">O método **EnumerateContent** cria um objeto [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) e passa esse objeto para o método [**IPortableDeviceService:: content**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-content) .</span><span class="sxs-lookup"><span data-stu-id="9e030-120">The **EnumerateContent** method creates an [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) object and passes this object to the [**IPortableDeviceService::Content**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-content) method.</span></span> <span data-ttu-id="9e030-121">Esse método, por sua vez, recupera o conteúdo no nível raiz do serviço e, em seguida, começa recursivamente a recuperar o conteúdo encontrado abaixo da raiz.</span><span class="sxs-lookup"><span data-stu-id="9e030-121">This method, in turn, retrieves the content at the root level of the service, and then recursively begins to retrieve content found beneath the root.</span></span>

<span data-ttu-id="9e030-122">O código a seguir corresponde ao método **EnumerateContent** .</span><span class="sxs-lookup"><span data-stu-id="9e030-122">The following code corresponds to the **EnumerateContent** method.</span></span>


```C++
// Enumerate all content on the service starting with the
// "DEVICE" object
void EnumerateAllContent(
    IPortableDeviceService* pService)
{
    HRESULT                          hr = S_OK;
    CComPtr<IPortableDeviceContent2> pContent;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceContent2 interface from the IPortableDeviceService interface to
    // access the content-specific methods.
    hr = pService->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent2 from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Enumerate content starting from the "DEVICE" object.
    if (SUCCEEDED(hr))
    {
        printf("\n");
        RecursiveEnumerate(WPD_DEVICE_OBJECT_ID, pContent);
    }
}
```



<span data-ttu-id="9e030-123">O código a seguir corresponde ao **método RecursiveEnumerate.**</span><span class="sxs-lookup"><span data-stu-id="9e030-123">The following code corresponds to the **RecursiveEnumerate** method.</span></span> <span data-ttu-id="9e030-124">O método RecursiveEnumerate instanciou uma interface **IEnumPortableDeviceObjectIDs** para o objeto pai fornecido e chama **IEnumPortableDeviceObjectIDs::Next**, recuperando um lote de objetos filho imediatos.</span><span class="sxs-lookup"><span data-stu-id="9e030-124">The RecursiveEnumerate method instantiates an **IEnumPortableDeviceObjectIDs** interface for the supplied parent object, and calls **IEnumPortableDeviceObjectIDs::Next**, retrieving a batch of immediate child objects.</span></span> <span data-ttu-id="9e030-125">Para cada objeto filho, RecursiveEnumerate é chamado novamente para retornar seus objetos filho descendentes e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="9e030-125">For each child object, RecursiveEnumerate is called again to return its descendent child objects, and so on.</span></span>


```C++
// Recursively called function which enumerates using the specified
// object identifier as the parent.
void RecursiveEnumerate(
    PCWSTR                   pszObjectID,
    IPortableDeviceContent2* pContent)
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
        printf("! Failed to get IEnumPortableDeviceObjectIDs from IPortableDeviceContent2, hr = 0x%lx\n",hr);
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



## <a name="related-topics"></a><span data-ttu-id="9e030-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9e030-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e030-127">**IEnumPortableDeviceObjectIDs**</span><span class="sxs-lookup"><span data-stu-id="9e030-127">**IEnumPortableDeviceObjectIDs**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[<span data-ttu-id="9e030-128">**IPortableDeviceContent2 Interface**</span><span class="sxs-lookup"><span data-stu-id="9e030-128">**IPortableDeviceContent2 Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="9e030-129">**IPortableDeviceService Interface**</span><span class="sxs-lookup"><span data-stu-id="9e030-129">**IPortableDeviceService Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="9e030-130">Abrindo um serviço</span><span class="sxs-lookup"><span data-stu-id="9e030-130">Opening a Service</span></span>](opening-a-service.md)
</dt> <dt>

[<span data-ttu-id="9e030-131">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="9e030-131">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



