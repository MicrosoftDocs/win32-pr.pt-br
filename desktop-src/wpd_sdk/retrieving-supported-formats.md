---
description: Recuperando formatos de serviço com suporte
ms.assetid: b54dfeda-c2a3-42ec-895f-9abbbd4dd2ec
title: Recuperando formatos de serviço com suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ed8021d8feefaaad3da7905e17e8c658dfb19e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766491"
---
# <a name="retrieving-supported-service-formats"></a><span data-ttu-id="43f1c-103">Recuperando formatos de serviço com suporte</span><span class="sxs-lookup"><span data-stu-id="43f1c-103">Retrieving Supported Service Formats</span></span>

<span data-ttu-id="43f1c-104">O aplicativo WpdServicesApiSample inclui código que demonstra como um aplicativo pode recuperar os formatos com suporte de um determinado serviço Contacts chamando métodos das interfaces na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="43f1c-104">The WpdServicesApiSample application includes code that demonstrates how an application can retrieve the formats supported by a given Contacts service by calling methods of the interfaces in the following table.</span></span>



|                                                                                      |                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43f1c-105">Interface</span><span class="sxs-lookup"><span data-stu-id="43f1c-105">Interface</span></span>                                                                            | <span data-ttu-id="43f1c-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="43f1c-106">Description</span></span>                                                                                           |
| [<span data-ttu-id="43f1c-107">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="43f1c-107">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | <span data-ttu-id="43f1c-108">Usado para recuperar a interface **IPortableDeviceServiceCapabilities** para acessar os eventos com suporte.</span><span class="sxs-lookup"><span data-stu-id="43f1c-108">Used to retrieve the **IPortableDeviceServiceCapabilities** interface to access the supported events.</span></span> |
| [<span data-ttu-id="43f1c-109">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="43f1c-109">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | <span data-ttu-id="43f1c-110">Fornece acesso aos eventos e atributos de evento com suporte.</span><span class="sxs-lookup"><span data-stu-id="43f1c-110">Provides access to the supported events and event attributes.</span></span>                                         |
| [<span data-ttu-id="43f1c-111">**IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="43f1c-111">**IPortableDevicePropVariantCollection**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="43f1c-112">Contém a lista de formatos com suporte.</span><span class="sxs-lookup"><span data-stu-id="43f1c-112">Contains the list of supported formats.</span></span>                                                               |
| [<span data-ttu-id="43f1c-113">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="43f1c-113">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="43f1c-114">Contém os atributos de um determinado formato.</span><span class="sxs-lookup"><span data-stu-id="43f1c-114">Contains the attributes for a given format.</span></span>                                                           |



 

<span data-ttu-id="43f1c-115">Quando o usuário escolhe a opção "3" na linha de comando, o aplicativo invoca o método **ListSupportedFormats** encontrado no módulo percapabilities. cpp.</span><span class="sxs-lookup"><span data-stu-id="43f1c-115">When the user chooses option "3" at the command line, the application invokes the **ListSupportedFormats** method that is found in the ServiceCapabilities.cpp module.</span></span>

<span data-ttu-id="43f1c-116">Observe que, antes de recuperar a lista de eventos, o aplicativo de exemplo abre um serviço de contatos em um dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="43f1c-116">Note that prior to retrieving the list of events, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="43f1c-117">Em WPD, um formato é descrito por atributos que especificam o nome e (opcionalmente) o tipo MIME de um determinado formato.</span><span class="sxs-lookup"><span data-stu-id="43f1c-117">In WPD, a format is described by attributes that specify the name and (optionally) the MIME type of a given format.</span></span> <span data-ttu-id="43f1c-118">Esses atributos são definidos no arquivo de cabeçalho thePortableDevice. h.</span><span class="sxs-lookup"><span data-stu-id="43f1c-118">These attributes are defined in thePortableDevice.h header file.</span></span> <span data-ttu-id="43f1c-119">Para obter uma descrição dos atributos com suporte, consulte o tópico [atributos](attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="43f1c-119">For a description of supported attributes, refer to the [Attributes](attributes.md) topic.</span></span>

<span data-ttu-id="43f1c-120">No caso do aplicativo de exemplo, se o WpdServiceSampleDriver for o único dispositivo instalado, o driver retornará dois formatos com suporte para seu serviço de contato: "AbstractContactFormat" e "VCard2Format".</span><span class="sxs-lookup"><span data-stu-id="43f1c-120">In the case of the sample application, if the WpdServiceSampleDriver is the only installed device, the driver returns two supported formats for its Contact service: "AbstractContactFormat" and "VCard2Format".</span></span> <span data-ttu-id="43f1c-121">Esses formatos correspondem ao **\_ \_ \_ \_ contato abstrato do formato de objeto WPD** e aos atributos **\_ \_ \_ VCARD2 de formato de objeto WPD** encontrados em PortableDevice. h.</span><span class="sxs-lookup"><span data-stu-id="43f1c-121">These formats correspond to the **WPD\_OBJECT\_FORMAT\_ABSTRACT\_CONTACT** and the **WPD\_OBJECT\_FORMAT\_VCARD2** attributes found in PortableDevice.h.</span></span>

<span data-ttu-id="43f1c-122">Dois métodos no módulo percapabilities. cpp oferecem suporte à recuperação de formatos com suporte para o serviço de contatos: **ListSupportedFormats** e **DisplayFormat**.</span><span class="sxs-lookup"><span data-stu-id="43f1c-122">Two methods in the ServiceCapabilities.cpp module support the retrieval of supported formats for the Contacts service: **ListSupportedFormats** and **DisplayFormat**.</span></span> <span data-ttu-id="43f1c-123">O primeiro recupera o identificador GUID para cada formato com suporte.</span><span class="sxs-lookup"><span data-stu-id="43f1c-123">The former retrieves the GUID identifier for each supported format.</span></span> <span data-ttu-id="43f1c-124">O último converte esse GUID em uma cadeia de caracteres amigável.</span><span class="sxs-lookup"><span data-stu-id="43f1c-124">The latter converts this GUID into a user-friendly string.</span></span>

<span data-ttu-id="43f1c-125">O método **ListSupportedFormats** invoca o método [**IPortableDeviceService:: Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) para recuperar uma interface [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .</span><span class="sxs-lookup"><span data-stu-id="43f1c-125">The **ListSupportedFormats** method invokes the [**IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="43f1c-126">Usando essa interface, ele recupera os formatos com suporte chamando o método [**IPortableDeviceServiceCapabilities:: GetSupportedFormats**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformats) .</span><span class="sxs-lookup"><span data-stu-id="43f1c-126">Using this interface, it retrieves the supported formats by calling the [**IPortableDeviceServiceCapabilities::GetSupportedFormats**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformats) method.</span></span> <span data-ttu-id="43f1c-127">O método **GetSupportedFormats** recupera o GUID para cada formato suportado pelo serviço e copia esse GUID em um objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="43f1c-127">The **GetSupportedFormats** method retrieves the GUID for each format supported by the service and copies that GUID into an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="43f1c-128">O código a seguir usa o método **ListSupportedFormats** .</span><span class="sxs-lookup"><span data-stu-id="43f1c-128">The following code uses the **ListSupportedFormats** method.</span></span>


```C++
// List all supported formats on the service
void ListSupportedFormats(
    IPortableDeviceService* pService)
{
    HRESULT hr              = S_OK;
    DWORD   dwNumFormats    = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pFormats;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceCapabilities interface from the IPortableDeviceService interface to
    // access the service capabilities-specific methods.
    hr = pService->Capabilities(&pCapabilities);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceCapabilities from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Get all formats supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedFormats(&pFormats);
        if (FAILED(hr))
        {
            printf("! Failed to get supported formats from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported formats found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pFormats->GetCount(&dwNumFormats);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported formats, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Formats Found on the service\n\n", dwNumFormats);

    // Loop through each format and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumFormats; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pFormats->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have a format.  It is assumed that
                // formats are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayFormat(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }
}
```



<span data-ttu-id="43f1c-129">Depois que o método **ListSupportedFormats** recupera o GUID para cada formato suportado pelo serviço fornecido, ele invoca o método **DisplayFormat** para exibir o nome amigável do script para cada formato; por exemplo, "VCard2".</span><span class="sxs-lookup"><span data-stu-id="43f1c-129">After the **ListSupportedFormats** method retrieves the GUID for each format supported by the given service, it invokes the **DisplayFormat** method to display the script friendly name for each format; for example, "VCard2".</span></span>

<span data-ttu-id="43f1c-130">O método **DisplayFormat** invoca o método [**IPortableDeviceServiceCapabilities:: getformatattributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) recuperar uma coleção de atributos para o GUID de formato fornecido.</span><span class="sxs-lookup"><span data-stu-id="43f1c-130">The **DisplayFormat** method invokes the [**IPortableDeviceServiceCapabilities::GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) method retrieve a collection of attributes for the given format GUID.</span></span> <span data-ttu-id="43f1c-131">Em seguida, ele chama o método [**IPortableDeviceValues:: GetStringValue**](iportabledevicevalues-getstringvalue.md) e solicita que o driver retorne um nome amigável para o script para o formato fornecido.</span><span class="sxs-lookup"><span data-stu-id="43f1c-131">It then calls the [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) method and requests that the driver return a script-friendly name for the given format.</span></span>

<span data-ttu-id="43f1c-132">O código a seguir usa o método **DisplayFormat** .</span><span class="sxs-lookup"><span data-stu-id="43f1c-132">The following code uses the **DisplayFormat** method.</span></span>


```C++
// Display basic information about a format
void DisplayFormat(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Format)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    HRESULT hr = pCapabilities->GetFormatAttributes(Format, &pAttributes);

    if (SUCCEEDED(hr))
    {
        PWSTR pszFormatName = NULL;
        hr = pAttributes->GetStringValue(WPD_FORMAT_ATTRIBUTE_NAME, &pszFormatName);

        // Display the name of the format if it is available, otherwise fall back to displaying the GUID.
        if (SUCCEEDED(hr))
        {
            printf("%ws", pszFormatName);
        }
        else
        {
            printf("%ws", (PWSTR)CGuidToString(Format));
        }       

        CoTaskMemFree(pszFormatName);
        pszFormatName = NULL;
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="43f1c-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="43f1c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43f1c-134">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="43f1c-134">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="43f1c-135">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="43f1c-135">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[<span data-ttu-id="43f1c-136">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="43f1c-136">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="43f1c-137">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="43f1c-137">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



