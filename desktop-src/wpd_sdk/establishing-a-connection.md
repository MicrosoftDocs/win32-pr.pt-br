---
description: Estabelecer uma conexão
ms.assetid: 16286da5-5979-413b-a4db-ca157b10a571
title: Estabelecer uma conexão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ea922b3cd44430dc7c213a513c44fa8ef2ab9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011818"
---
# <a name="establishing-a-connection"></a><span data-ttu-id="bd0eb-103">Estabelecer uma conexão</span><span class="sxs-lookup"><span data-stu-id="bd0eb-103">Establishing a Connection</span></span>

<span data-ttu-id="bd0eb-104">Depois que o usuário seleciona um dispositivo, a função ChooseDevice, por sua vez, chama o método [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) para estabelecer uma conexão entre o aplicativo e o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bd0eb-104">Once the user selects a device, the ChooseDevice function, in turn, calls the [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) method to establish a connection between the application and the device.</span></span> <span data-ttu-id="bd0eb-105">O método IPortableDevice:: Open usa dois argumentos:</span><span class="sxs-lookup"><span data-stu-id="bd0eb-105">The IPortableDevice::Open method takes two arguments:</span></span>

-   <span data-ttu-id="bd0eb-106">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome Plug and Play do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bd0eb-106">A pointer to a null-terminated string that specifies the Plug and Play name of the device.</span></span> <span data-ttu-id="bd0eb-107">(Essa cadeia de caracteres é recuperada chamando o método [**IPortableDeviceManager:: Devices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) .)</span><span class="sxs-lookup"><span data-stu-id="bd0eb-107">(This string is retrieved by calling the [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) method.)</span></span>
-   <span data-ttu-id="bd0eb-108">Um ponteiro para uma [**interface IPortableDeviceValues**](iportabledevicevalues.md) que especifica as informações do cliente para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bd0eb-108">A pointer to an [**IPortableDeviceValues interface**](iportabledevicevalues.md) that specifies client information for the application.</span></span>


```C++
// CoCreate the IPortableDevice interface and call Open() with
// the chosen PnPDeviceID string.
hr = CoCreateInstance(CLSID_PortableDeviceFTM,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(ppDevice));
if (SUCCEEDED(hr))
{
    hr = (*ppDevice)->Open(pPnpDeviceIDs[uiCurrentDevice], pClientInformation);
    if (FAILED(hr))
    {
        if (hr == E_ACCESSDENIED)
        {
            printf("Failed to Open the device for Read Write access, will open it for Read-only access instead\n");
            pClientInformation->SetUnsignedIntegerValue(WPD_CLIENT_DESIRED_ACCESS, GENERIC_READ);
            hr = (*ppDevice)->Open(pPnpDeviceIDs[uiCurrentDevice], pClientInformation);
            if (FAILED(hr))
            {
                printf("! Failed to Open the device, hr = 0x%lx\n",hr);
                // Release the IPortableDevice interface, because we cannot proceed
                // with an unopen device.
                (*ppDevice)->Release();
                *ppDevice = NULL;
            }
        }
        else
        {
            printf("! Failed to Open the device, hr = 0x%lx\n",hr);
            // Release the IPortableDevice interface, because we cannot proceed
            // with an unopen device.
            (*ppDevice)->Release();
            *ppDevice = NULL;
        }
    }
}
else
{
    printf("! Failed to CoCreateInstance CLSID_PortableDeviceFTM, hr = 0x%lx\n",hr);
}
```



<span data-ttu-id="bd0eb-109">Para o Windows 7, o [**IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice) dá suporte a dois CLSIDs para **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="bd0eb-109">For Windows 7, [**IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice) supports two CLSIDs for **CoCreateInstance**.</span></span> <span data-ttu-id="bd0eb-110">**CLSID \_ do PortableDevice** retorna um ponteiro **IPortableDevice** que não agrega o marshaler de thread livre; **CLSID \_ do PortableDeviceFTM** é um novo CLSID que retorna um ponteiro **IPortableDevice** que agrega o marshaler de thread livre.</span><span class="sxs-lookup"><span data-stu-id="bd0eb-110">**CLSID\_PortableDevice** returns an **IPortableDevice** pointer that does not aggregate the free-threaded marshaler; **CLSID\_PortableDeviceFTM** is a new CLSID that returns an **IPortableDevice** pointer that aggregates the free-threaded marshaler.</span></span> <span data-ttu-id="bd0eb-111">Os dois ponteiros também dão suporte à mesma funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="bd0eb-111">Both pointers support the same functionality otherwise.</span></span>

<span data-ttu-id="bd0eb-112">Aplicativos que residem em Apartments de thread único devem usar **CLSID \_ PortableDeviceFTM** , pois isso elimina a sobrecarga do marshaling do ponteiro de interface.</span><span class="sxs-lookup"><span data-stu-id="bd0eb-112">Applications that live in Single Threaded Apartments should use **CLSID\_PortableDeviceFTM** as this eliminates the overhead of interface pointer marshaling.</span></span> <span data-ttu-id="bd0eb-113">**CLSID \_ do O PortableDevice** ainda tem suporte para aplicativos herdados.</span><span class="sxs-lookup"><span data-stu-id="bd0eb-113">**CLSID\_PortableDevice** is still supported for legacy applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd0eb-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bd0eb-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd0eb-115">**Selecionando um dispositivo**</span><span class="sxs-lookup"><span data-stu-id="bd0eb-115">**Selecting a Device**</span></span>](selecting-a-device.md)
</dt> </dl>

 

 



