---
description: Enumerando serviços
ms.assetid: 6ee6eecb-3812-45c6-8b27-7dfd6fa82758
title: Enumerando serviços
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2eca8221a9a34bf9e921bcaca00eac99f2a75d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810734"
---
# <a name="enumerating-services"></a><span data-ttu-id="48d75-103">Enumerando serviços</span><span class="sxs-lookup"><span data-stu-id="48d75-103">Enumerating Services</span></span>

<span data-ttu-id="48d75-104">O aplicativo WpdServicesApiSample inclui código que demonstra como um aplicativo pode enumerar todos os serviços de contatos encontrados em qualquer um dos dispositivos conectados no momento a um computador.</span><span class="sxs-lookup"><span data-stu-id="48d75-104">The WpdServicesApiSample application includes code that demonstrates how an application can enumerate all of the Contacts services found on any of the devices currently connected to a computer.</span></span>

<span data-ttu-id="48d75-105">Quando o usuário escolhe a opção "0" na linha de comando, o aplicativo invoca o método **EnumerateContactsServices** encontrado no módulo do perenumeration. cpp.</span><span class="sxs-lookup"><span data-stu-id="48d75-105">When the user chooses option "0" at the command line, the application invokes the **EnumerateContactsServices** method that is found in the ServiceEnumeration.cpp module.</span></span> <span data-ttu-id="48d75-106">Esse método exibe uma lista de todos os dispositivos conectados que dão suporte ao serviço de contatos.</span><span class="sxs-lookup"><span data-stu-id="48d75-106">This method displays a list of all connected devices that support the Contacts service.</span></span>

<span data-ttu-id="48d75-107">Por exemplo, se o WpdServiceSampleDriver for o único dispositivo instalado, o aplicativo retornará três campos de dados: um nome amigável ("dispositivo de exemplo"), um fabricante ("grupo de dispositivos portáteis do Windows") e uma descrição ("dispositivo de serviço de contatos 2000").</span><span class="sxs-lookup"><span data-stu-id="48d75-107">For example, if the WpdServiceSampleDriver is the only installed device, the application returns three fields of data: a Friendly Name ("Sample Device"), a Manufacturer ("Windows Portable Devices Group"), and, a Description ("Contacts Service Device 2000").</span></span>

<span data-ttu-id="48d75-108">O método **EnumerateContactsServices** realiza as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="48d75-108">The **EnumerateContactsServices** method accomplishes the following tasks:</span></span>

-   <span data-ttu-id="48d75-109">Cria uma interface [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) para lidar com a enumeração de dispositivos instalados.</span><span class="sxs-lookup"><span data-stu-id="48d75-109">Creates an [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface to handle enumeration of installed devices.</span></span>
-   <span data-ttu-id="48d75-110">Cria uma interface [**IPortableDeviceServiceManager**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager) para lidar com a enumeração dos serviços em cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48d75-110">Creates an [**IPortableDeviceServiceManager**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager) interface to handle enumeration of the services on each device.</span></span>
-   <span data-ttu-id="48d75-111">Itera através dos dispositivos instalados, pesquisando o serviço de contatos e exibe as informações do dispositivo para qualquer dispositivo que dê suporte a esse serviço.</span><span class="sxs-lookup"><span data-stu-id="48d75-111">Iterates through the installed devices, searching for the Contacts service, and displays the device information for any device that supports this service.</span></span>

<span data-ttu-id="48d75-112">O código a seguir ilustra o método **EnumerateContactsServices** .</span><span class="sxs-lookup"><span data-stu-id="48d75-112">The following code illustrates the **EnumerateContactsServices** method.</span></span>


```C++
// Enumerates all Contacts Services, displaying the associated device of each service.
void EumerateContactsServices(CAtlArray<PWSTR>& ContactsServicePnpIDs)
{
    HRESULT                                 hr              = S_OK;
    DWORD                                   cPnpDeviceIDs   = 0;
    PWSTR*                                  pPnpDeviceIDs   = NULL;
    CComPtr<IPortableDeviceManager>         pPortableDeviceManager;
    CComPtr<IPortableDeviceServiceManager>  pServiceManager;

    // CoCreate the IPortableDeviceManager interface to enumerate
    // portable devices and to get information about them.
    hr = CoCreateInstance(CLSID_PortableDeviceManager,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&pPortableDeviceManager));

    if (FAILED(hr))
    {
        printf("! Failed to CoCreateInstance CLSID_PortableDeviceManager, hr = 0x%lx\n",hr);
    }        

    // Retrieve the IPortableDeviceServiceManager interface to enumerate device services.
    if (SUCCEEDED(hr))
    {
        hr = pPortableDeviceManager->QueryInterface(IID_PPV_ARGS(&pServiceManager));
        if (FAILED(hr))
        {
            printf("! Failed to QueryInterface IID_IPortableDeviceServiceManager, hr = 0x%lx\n",hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        // First, pass NULL as the PWSTR array pointer to get the total number
        // of devices found on the system.
        hr = pPortableDeviceManager->GetDevices(NULL, &cPnpDeviceIDs);

        if (FAILED(hr))
        {
            printf("! Failed to get number of devices on the system, hr = 0x%lx\n",hr);
        }

        if (SUCCEEDED(hr) && (cPnpDeviceIDs > 0))
        {
            // Second, allocate an array to hold the PnPDeviceID strings returned from
            // the IPortableDeviceManager::GetDevices method
            pPnpDeviceIDs = new (std::nothrow) PWSTR[cPnpDeviceIDs];

            if (pPnpDeviceIDs != NULL)
            {
                DWORD dwIndex = 0;

                hr = pPortableDeviceManager->GetDevices(pPnpDeviceIDs, &cPnpDeviceIDs);
                if (SUCCEEDED(hr))
                {   
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
                }

                // Free all returned PnPDeviceID strings
                FreePortableDevicePnPIDs(pPnpDeviceIDs, cPnpDeviceIDs);

                // Delete the array of PWSTR pointers
                delete [] pPnpDeviceIDs;
                pPnpDeviceIDs = NULL;

            }
            else
            {
                printf("! Failed to allocate memory for PWSTR array\n");
            }            
        }
    }
    
    printf("\n%d Contacts Device Service(s) found on the system\n\n", static_cast<DWORD>(ContactsServicePnpIDs.GetCount()));
}
```



## <a name="related-topics"></a><span data-ttu-id="48d75-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="48d75-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48d75-114">**Interface IPortableDeviceManager**</span><span class="sxs-lookup"><span data-stu-id="48d75-114">**IPortableDeviceManager Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)
</dt> <dt>

[<span data-ttu-id="48d75-115">**Interface IPortableDeviceServiceManager**</span><span class="sxs-lookup"><span data-stu-id="48d75-115">**IPortableDeviceServiceManager Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)
</dt> <dt>

[<span data-ttu-id="48d75-116">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="48d75-116">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



