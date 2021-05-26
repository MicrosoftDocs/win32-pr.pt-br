---
description: Abrindo um serviço
ms.assetid: 722d657d-332a-40df-ac30-bc2050deda74
title: Abrindo um serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b273b8709a4d750085f14075d605f88ed0faa6
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423916"
---
# <a name="opening-a-service"></a><span data-ttu-id="9a755-103">Abrindo um serviço</span><span class="sxs-lookup"><span data-stu-id="9a755-103">Opening a Service</span></span>

<span data-ttu-id="9a755-104">Antes que seu aplicativo possa executar operações em um serviço, por exemplo, enumerando conteúdo ou recuperando descrições de eventos ou métodos com suporte, ele deve abrir o serviço.</span><span class="sxs-lookup"><span data-stu-id="9a755-104">Before your application can perform operations on a service, for example, enumerating content or retrieving descriptions of supported events or methods, it must open the service.</span></span> <span data-ttu-id="9a755-105">No aplicativo WpdServicesApiSample, essa tarefa é demonstrada no módulo do inenumeration. cpp usando as interfaces descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9a755-105">In the WpdServicesApiSample application, this task is demonstrated in the ServiceEnumeration.cpp module using the interfaces described in the following table.</span></span>



| <span data-ttu-id="9a755-106">Interface</span><span class="sxs-lookup"><span data-stu-id="9a755-106">Interface</span></span>                                                              | <span data-ttu-id="9a755-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a755-107">Description</span></span>                                        |
|------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="9a755-108">**IPortableDeviceServiceManager**</span><span class="sxs-lookup"><span data-stu-id="9a755-108">**IPortableDeviceServiceManager**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager) | <span data-ttu-id="9a755-109">Usado para enumerar os serviços em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9a755-109">Used to enumerate the services on a device.</span></span>        |
| [<span data-ttu-id="9a755-110">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="9a755-110">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | <span data-ttu-id="9a755-111">Usado para abrir uma conexão com um serviço de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9a755-111">Used to open a connection to a device service.</span></span>     |
| [<span data-ttu-id="9a755-112">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="9a755-112">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                 | <span data-ttu-id="9a755-113">Usado para manter as informações do cliente do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9a755-113">Used to hold the application's client information.</span></span> |



 

<span data-ttu-id="9a755-114">O método que abre um serviço é [**IPortableDeviceService:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span><span class="sxs-lookup"><span data-stu-id="9a755-114">The method that opens a service is [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span></span> <span data-ttu-id="9a755-115">Esse método usa dois argumentos: um identificador de plug-and-Play (PnP) para o serviço e um objeto [**IPortableDeviceValues**](iportabledevicevalues.md) que contém as informações do cliente do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9a755-115">This method takes two arguments: a Plug-and-Play (PnP) identifier for the service and an [**IPortableDeviceValues**](iportabledevicevalues.md) object that contains the application's client information.</span></span>

<span data-ttu-id="9a755-116">Para obter um identificador de PnP para um determinado serviço, seu aplicativo chama o método [**IPortableDeviceServiceManager:: Getdeviceservices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) .</span><span class="sxs-lookup"><span data-stu-id="9a755-116">To obtain a PnP identifier for a given service, your application calls the [**IPortableDeviceServiceManager::GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) method.</span></span> <span data-ttu-id="9a755-117">Esse método recupera uma matriz de identificadores PnP para serviços de um GUID de categoria de serviço (por exemplo, contatos de serviço).</span><span class="sxs-lookup"><span data-stu-id="9a755-117">This method retrieves an array of PnP identifiers for services of a service category GUID (for example SERVICE Contacts).</span></span>

<span data-ttu-id="9a755-118">O aplicativo de serviço de exemplo recupera um identificador PnP para serviços de contatos dentro do método **EnumerateContactsServices** no módulo Service Enumeration. cpp.</span><span class="sxs-lookup"><span data-stu-id="9a755-118">The sample Service application retrieves a PnP identifier for Contacts services within the **EnumerateContactsServices** method in the ServiceEnumeration.cpp module.</span></span> <span data-ttu-id="9a755-119">O exemplo de código a seguir é obtido deste método.</span><span class="sxs-lookup"><span data-stu-id="9a755-119">The following code sample is taken from this method.</span></span>


```C++
// For each device found, find the contacts service
for (dwIndex = 0; dwIndex < cPnpDeviceIDs; dwIndex++)
{
    DWORD   cPnpServiceIDs = 0;
    PWSTR   pPnpServiceID  = NULL;

    // First, pass NULL as the PWSTR array pointer to get the total number
    // of contacts services (SERVICE_Contacts) found on the device.
    // To find the total number of all services on the device, use GUID_DEVINTERFACE_WPD_SERVICE.
    hr = pServiceManager->GetDeviceServices(pPnpDeviceIDs[dwIndex], SERVICE_Contacts, NULL, &cPnpServiceIDs);
    
    if (SUCCEEDED(hr) && (cPnpServiceIDs > 0))
    {                               
        // For simplicity, we are only using the first contacts service on each device
        cPnpServiceIDs = 1;
        hr = pServiceManager->GetDeviceServices(pPnpDeviceIDs[dwIndex], SERVICE_Contacts, &pPnpServiceID, &cPnpServiceIDs);

        if (SUCCEEDED(hr))
        {
            // We've found the service, display it and save its PnP Identifier
            ContactsServicePnpIDs.Add(pPnpServiceID);

            printf("[%d] ", static_cast<DWORD>(ContactsServicePnpIDs.GetCount()-1));

            // Display information about the device that contains this service.
            DisplayDeviceInformation(pServiceManager, pPnpServiceID);

            // ContactsServicePnpIDs now owns the memory for this string
            pPnpServiceID = NULL;
        }
        else
        {
            printf("! Failed to get the first contacts service from '%ws, hr = 0x%lx\n",pPnpDeviceIDs[dwIndex],hr);
        }
    }
}
```



<span data-ttu-id="9a755-120">Depois que o aplicativo recupera o identificador PnP para o serviço, ele pode configurar as informações do cliente e chamar [**IPortableDeviceService:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span><span class="sxs-lookup"><span data-stu-id="9a755-120">After your application retrieves the PnP identifier for the service, it can set up the client information and call [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span></span>

<span data-ttu-id="9a755-121">No aplicativo de exemplo, esse método é chamado dentro de **ChooseDeviceService** no módulo do inenumeration. cpp.</span><span class="sxs-lookup"><span data-stu-id="9a755-121">In the sample application, this method is called within **ChooseDeviceService** in the ServiceEnumeration.cpp module.</span></span>

<span data-ttu-id="9a755-122">O [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) dá suporte a dois CLSIDs para **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="9a755-122">[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) supports two CLSIDs for **CoCreateInstance**.</span></span> <span data-ttu-id="9a755-123">**CLSID \_ PortableDeviceService** retorna um ponteiro **IPortableDeviceService** que não agrega o marshaler de thread livre; **CLSID \_ PortableDeviceServiceFTM** é um novo CLSID que retorna um ponteiro **IPortableDeviceService** que agrega o marshaler de thread livre.</span><span class="sxs-lookup"><span data-stu-id="9a755-123">**CLSID\_PortableDeviceService** returns an **IPortableDeviceService** pointer that does not aggregate the free-threaded marshaler; **CLSID\_PortableDeviceServiceFTM** is a new CLSID that returns an **IPortableDeviceService** pointer that aggregates the free-threaded marshaler.</span></span> <span data-ttu-id="9a755-124">Caso contrário, ambos os ponteiros darão suporte à mesma funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="9a755-124">Both pointers support the same functionality otherwise.</span></span>

<span data-ttu-id="9a755-125">Os aplicativos que agem em Single Threaded Apartments devem usar **CLSID \_ PortableDeviceServiceFTM,** pois isso elimina a sobrecarga do marshaling de ponteiro de interface.</span><span class="sxs-lookup"><span data-stu-id="9a755-125">Applications that live in Single Threaded Apartments should use **CLSID\_PortableDeviceServiceFTM** as this eliminates the overhead of interface pointer marshaling.</span></span> <span data-ttu-id="9a755-126">**CLSID \_ PortableDeviceService** ainda tem suporte para aplicativos herdados.</span><span class="sxs-lookup"><span data-stu-id="9a755-126">**CLSID\_PortableDeviceService** is still supported for legacy applications.</span></span>


```C++
hr = CoCreateInstance(CLSID_PortableDeviceServiceFTM,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pService));
if (SUCCEEDED(hr))
{
    hr = pService->Open(ContactsServicesArray[uiCurrentService], pClientInformation);
    if (FAILED(hr))
    {
        if (hr == E_ACCESSDENIED)
        {
            printf("Failed to Open the service for Read Write access, will open it for Read-only access instead\n");

            pClientInformation->SetUnsignedIntegerValue(WPD_CLIENT_DESIRED_ACCESS, GENERIC_READ);

            hr = pService->Open(ContactsServicesArray[uiCurrentService], pClientInformation);

            if (FAILED(hr))
            {
                printf("! Failed to Open the service for Read access, hr = 0x%lx\n",hr);
            }
        }
        else
        {
            printf("! Failed to Open the service, hr = 0x%lx\n",hr);
        }
    }
```



## <a name="related-topics"></a><span data-ttu-id="9a755-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9a755-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a755-128">**IPortableDeviceService Interface**</span><span class="sxs-lookup"><span data-stu-id="9a755-128">**IPortableDeviceService Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="9a755-129">**IPortableDeviceValues Interface**</span><span class="sxs-lookup"><span data-stu-id="9a755-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="9a755-130">**IPortableDeviceServiceManager Interface**</span><span class="sxs-lookup"><span data-stu-id="9a755-130">**IPortableDeviceServiceManager Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)
</dt> <dt>

[<span data-ttu-id="9a755-131">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="9a755-131">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



