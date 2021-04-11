---
description: Especificando informações do cliente
ms.assetid: 275fda71-61ef-4b50-96fe-bdc0c0266646
title: Especificando informações do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f6ca094b627b6c2cee16ec587a8c850cd17f78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170998"
---
# <a name="specifying-client-information"></a><span data-ttu-id="f2a42-103">Especificando informações do cliente</span><span class="sxs-lookup"><span data-stu-id="f2a42-103">Specifying Client Information</span></span>

<span data-ttu-id="f2a42-104">As informações do cliente fornecidas no segundo argumento são usadas por alguns drivers de dispositivo para otimizar o desempenho do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f2a42-104">The client information supplied in the second argument is used by some device drivers to optimize device performance.</span></span> <span data-ttu-id="f2a42-105">No mínimo, o aplicativo deve fornecer uma cadeia de caracteres contendo seu nome, um número de versão principal, um número de versão secundária e um número de revisão.</span><span class="sxs-lookup"><span data-stu-id="f2a42-105">At a minimum, your application should provide a string containing its name, a major version number, a minor version number, and a revision number.</span></span> <span data-ttu-id="f2a42-106">Esses são os campos fornecidos pelo aplicativo de exemplo.</span><span class="sxs-lookup"><span data-stu-id="f2a42-106">These are the fields supplied by the sample application.</span></span>


```C++
#define CLIENT_NAME         L"WPD Sample Application"
#define CLIENT_MAJOR_VER    1
#define CLIENT_MINOR_VER    0
#define CLIENT_REVISION     2
```



<span data-ttu-id="f2a42-107">A `GetClientInformation` função no aplicativo de exemplo cria e popula uma interface **IPortableDeviceValues** com informações do cliente.</span><span class="sxs-lookup"><span data-stu-id="f2a42-107">The `GetClientInformation` function in the sample application creates and populates an **IPortableDeviceValues** interface with client information.</span></span> <span data-ttu-id="f2a42-108">Essa função tem duas partes principais.</span><span class="sxs-lookup"><span data-stu-id="f2a42-108">This function has two primary parts.</span></span> <span data-ttu-id="f2a42-109">A primeira parte cria uma instância de um objeto de valores de dispositivo portátil chamando a função CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="f2a42-109">The first part creates an instance of a portable device-values object by calling the CoCreateInstance function.</span></span>


```C++
HRESULT hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(ppClientInformation));
```



<span data-ttu-id="f2a42-110">A segunda parte define as informações do cliente no objeto de valores de dispositivo portátil.</span><span class="sxs-lookup"><span data-stu-id="f2a42-110">The second part sets the client information in the portable device-values object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Attempt to set all bits of client information
    hr = (*ppClientInformation)->SetStringValue(WPD_CLIENT_NAME, CLIENT_NAME);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_NAME, hr = 0x%lx\n",hr);
    }

    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_MAJOR_VERSION, CLIENT_MAJOR_VER);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_MAJOR_VERSION, hr = 0x%lx\n",hr);
    }

    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_MINOR_VERSION, CLIENT_MINOR_VER);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_MINOR_VERSION, hr = 0x%lx\n",hr);
    }

    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_REVISION, CLIENT_REVISION);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_REVISION, hr = 0x%lx\n",hr);
    }

    //  Some device drivers need to impersonate the caller in order to function correctly.  Since our application does not
    //  need to restrict its identity, specify SECURITY_IMPERSONATION so that we work with all devices.
    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_SECURITY_QUALITY_OF_SERVICE, SECURITY_IMPERSONATION);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_SECURITY_QUALITY_OF_SERVICE, hr = 0x%lx\n",hr);
    }
}
else
{
    printf("! Failed to CoCreateInstance CLSID_PortableDeviceValues, hr = 0x%lx\n",hr);
}
```



## <a name="related-topics"></a><span data-ttu-id="f2a42-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f2a42-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2a42-112">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="f2a42-112">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="f2a42-113">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="f2a42-113">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="f2a42-114">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="f2a42-114">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



