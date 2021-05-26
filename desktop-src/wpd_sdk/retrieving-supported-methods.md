---
description: Recuperando métodos de serviço com suporte
ms.assetid: 783a6552-9b22-4af4-9252-b443e2624687
title: Recuperando métodos de serviço com suporte
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b021aa868ffaa95df23a729e94d62eae8a0c632e
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423796"
---
# <a name="retrieving-supported-service-methods"></a><span data-ttu-id="61e9c-103">Recuperando métodos de serviço com suporte</span><span class="sxs-lookup"><span data-stu-id="61e9c-103">Retrieving Supported Service Methods</span></span>

<span data-ttu-id="61e9c-104">Os métodos de serviço encapsulam a funcionalidade que cada serviço define e implementa.</span><span class="sxs-lookup"><span data-stu-id="61e9c-104">Service methods encapsulate functionality that each service defines and implements.</span></span> <span data-ttu-id="61e9c-105">Elas são específicas para cada tipo de tipo de serviço e são representadas por um GUID exclusivo.</span><span class="sxs-lookup"><span data-stu-id="61e9c-105">They are specific to each type of service type and are represented by a unique GUID.</span></span>

<span data-ttu-id="61e9c-106">Por exemplo, o serviço Contatos define um método **BeginSync** que os aplicativos chamam para preparar o dispositivo para sincronizar objetos contact e um **método EndSync** para notificar o dispositivo de que a sincronização foi concluída.</span><span class="sxs-lookup"><span data-stu-id="61e9c-106">For example, the Contacts service defines a **BeginSync** method that applications call to prepare the device for synchronizing Contact objects, and an **EndSync** method to notify the device that synchronization has completed.</span></span>

<span data-ttu-id="61e9c-107">Os aplicativos podem consultar programaticamente os métodos com suporte e acessar esses métodos e seus atributos usando a interface [**IPortableDeviceServiceCapabilities.**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)</span><span class="sxs-lookup"><span data-stu-id="61e9c-107">Applications can programmatically query the supported methods and access these methods and their attributes by using the [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span>

<span data-ttu-id="61e9c-108">Os métodos de serviço não devem ser confundidos com comandos WPD.</span><span class="sxs-lookup"><span data-stu-id="61e9c-108">Service methods should not be confused with WPD commands.</span></span> <span data-ttu-id="61e9c-109">Os comandos WPD fazem parte da DDI (Interface de Driver de Dispositivo) WPD padrão e são o mecanismo de comunicação entre um aplicativo WPD e o driver.</span><span class="sxs-lookup"><span data-stu-id="61e9c-109">WPD commands are part of the standard WPD Device Driver Interface (DDI), and are the mechanism for communication between a WPD application and the driver.</span></span> <span data-ttu-id="61e9c-110">Os comandos são predefinidos, agrupados por categorias, por exemplo, WPD CATEGORY COMMON e são representados \_ \_ por uma estrutura PROPERTYKEY.</span><span class="sxs-lookup"><span data-stu-id="61e9c-110">Commands are predefined, grouped by categories, for example, WPD\_CATEGORY\_COMMON, and are represented by a PROPERTYKEY structure.</span></span> <span data-ttu-id="61e9c-111">Para obter mais informações, consulte o [**tópico Comandos.**](commands.md)</span><span class="sxs-lookup"><span data-stu-id="61e9c-111">For more information, see the [**Commands**](commands.md) topic.</span></span>

<span data-ttu-id="61e9c-112">O aplicativo WpdServicesApiSample inclui código que demonstra como um aplicativo pode recuperar os métodos com suporte por um determinado serviço Contacts usando as interfaces na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="61e9c-112">The WpdServicesApiSample application includes code that demonstrates how an application can retrieve the methods supported by a given Contacts service by using the interfaces in the following table.</span></span>



| <span data-ttu-id="61e9c-113">Interface</span><span class="sxs-lookup"><span data-stu-id="61e9c-113">Interface</span></span>      | <span data-ttu-id="61e9c-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="61e9c-114">Description</span></span>         |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61e9c-115">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="61e9c-115">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | <span data-ttu-id="61e9c-116">Usado para recuperar a interface **IPortableDeviceServiceCapabilities** para acessar os métodos de serviço com suporte.</span><span class="sxs-lookup"><span data-stu-id="61e9c-116">Used to retrieve the **IPortableDeviceServiceCapabilities** interface to access the supported service methods.</span></span> |
| [<span data-ttu-id="61e9c-117">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="61e9c-117">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | <span data-ttu-id="61e9c-118">Fornece acesso aos métodos com suporte, atributos de método e parâmetros de método.</span><span class="sxs-lookup"><span data-stu-id="61e9c-118">Provides access to the supported methods, method attributes and method parameters.</span></span>                             |
| [<span data-ttu-id="61e9c-119">**IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="61e9c-119">**IPortableDevicePropVariantCollection**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="61e9c-120">Contém a lista de métodos com suporte.</span><span class="sxs-lookup"><span data-stu-id="61e9c-120">Contains the list of supported methods.</span></span>                                                                        |
| [<span data-ttu-id="61e9c-121">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="61e9c-121">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="61e9c-122">Contém os atributos para um método e para parâmetros de um determinado método.</span><span class="sxs-lookup"><span data-stu-id="61e9c-122">Contains the attributes for a method and for a given method's parameters.</span></span>                                      |
| [<span data-ttu-id="61e9c-123">**IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="61e9c-123">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="61e9c-124">Contém os parâmetros para um determinado método.</span><span class="sxs-lookup"><span data-stu-id="61e9c-124">Contains the parameters for a given method.</span></span>                                                                    |



 

<span data-ttu-id="61e9c-125">Quando o usuário escolhe a opção "5" na linha de comando, o aplicativo invoca o método **ListSupportedMethods** que é encontrado no módulo permethods. cpp.</span><span class="sxs-lookup"><span data-stu-id="61e9c-125">When the user chooses option "5" at the command line, the application invokes the **ListSupportedMethods** method that is found in the ServiceMethods.cpp module.</span></span>

<span data-ttu-id="61e9c-126">Observe que, antes de recuperar a lista de eventos, o aplicativo de exemplo abre um serviço de contatos em um dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="61e9c-126">Note that prior to retrieving the list of events, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="61e9c-127">Em WPD, um método é descrito por seu nome, direitos de acesso, parâmetros e dados relacionados.</span><span class="sxs-lookup"><span data-stu-id="61e9c-127">In WPD, a method is described by its name, access rights, parameters, and related data.</span></span> <span data-ttu-id="61e9c-128">O aplicativo de exemplo exibe um nome amigável, por exemplo, "CustomMethod" ou um GUID.</span><span class="sxs-lookup"><span data-stu-id="61e9c-128">The sample application displays a user-friendly name, for example, "CustomMethod", or a GUID.</span></span> <span data-ttu-id="61e9c-129">O nome do método ou GUID é seguido pelos dados do Access ("leitura/gravação"), o nome de qualquer formato associado e os dados do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="61e9c-129">The method name or GUID is followed by access data ("Read/Write"), the name of any associated format, and the parameter data.</span></span> <span data-ttu-id="61e9c-130">Esses dados incluem o nome do parâmetro, uso, VARTYPE e Form.</span><span class="sxs-lookup"><span data-stu-id="61e9c-130">This data includes the parameter name, usage, VARTYPE, and form.</span></span>

<span data-ttu-id="61e9c-131">Cinco métodos no módulo Service Methods. cpp dão suporte à recuperação de métodos (e dados relacionados) para o serviço de contatos fornecido: **ListSupportedMethods**, **DisplayMethod**, **DisplayMethodAccess**, **DisplayFormat** e **DisplayMethodParameters**.</span><span class="sxs-lookup"><span data-stu-id="61e9c-131">Five methods in the ServiceMethods.cpp module support the retrieval of methods (and related data) for the given Contacts service: **ListSupportedMethods**, **DisplayMethod**, **DisplayMethodAccess**, **DisplayFormat**, and **DisplayMethodParameters**.</span></span> <span data-ttu-id="61e9c-132">O método **ListSupportedMethods** recupera uma contagem de métodos com suporte e o identificador GUID para cada um; em seguida, ele chama o método **DisplayMethod** .</span><span class="sxs-lookup"><span data-stu-id="61e9c-132">The **ListSupportedMethods** method retrieves a count of supported methods and the GUID identifier for each; it then calls the **DisplayMethod** method.</span></span> <span data-ttu-id="61e9c-133">O método **DisplayMethod** chama o método [**IPortableDeviceServiceCapapbilities:: getmethodattributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) para recuperar as opções, os parâmetros e assim por diante do método fornecido.</span><span class="sxs-lookup"><span data-stu-id="61e9c-133">The **DisplayMethod** method calls the [**IPortableDeviceServiceCapapbilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) method to retrieve the given method's options, parameters, and so on.</span></span> <span data-ttu-id="61e9c-134">Depois que o **DisplayMethod** recupera os dados do método, ele renderiza o nome (ou GUID), as restrições de acesso, o formato associado (se houver) e as descrições de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="61e9c-134">After the **DisplayMethod** retrieves the method data, it renders the name (or GUID), the access restrictions, the associated format (if any), and the parameter descriptions.</span></span> <span data-ttu-id="61e9c-135">**DisplayMethodAccess**, **DisplayFormat** e **DisplayMethodParameters** são funções auxiliares que renderizam seus respectivos campos de dados.</span><span class="sxs-lookup"><span data-stu-id="61e9c-135">The **DisplayMethodAccess**, **DisplayFormat**, and **DisplayMethodParameters** are helper functions that render their respective fields of data.</span></span>

<span data-ttu-id="61e9c-136">O método **ListSupportedMethods** invoca o método [**IPortableDeviceService:: Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) para recuperar uma interface [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .</span><span class="sxs-lookup"><span data-stu-id="61e9c-136">The **ListSupportedMethods** method invokes the [**IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="61e9c-137">Usando essa interface, ele recupera os métodos com suporte chamando o [**método IPortableDeviceServiceCapabilities::GetSupportedMethods.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods)</span><span class="sxs-lookup"><span data-stu-id="61e9c-137">Using this interface, it retrieves the supported methods by calling the [**IPortableDeviceServiceCapabilities::GetSupportedMethods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) method.</span></span> <span data-ttu-id="61e9c-138">O **método GetSupportedMethods** recupera os GUIDs para cada método compatível com o serviço e copia esse GUID em [**um objeto IPortableDevicePropVariantCollection.**](iportabledevicepropvariantcollection.md)</span><span class="sxs-lookup"><span data-stu-id="61e9c-138">The **GetSupportedMethods** method retrieves the GUIDs for each method supported by the service and copies that GUID into an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="61e9c-139">O código a seguir usa o **método ListSupportedMethods.**</span><span class="sxs-lookup"><span data-stu-id="61e9c-139">The following code uses the **ListSupportedMethods** method.</span></span>


```C++
// List all supported methods on the service
void ListSupportedMethods(IPortableDeviceService* pService)
{
    HRESULT hr              = S_OK;
    DWORD   dwNumMethods    = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pMethods;

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

    // Get all methods supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedMethods(&pMethods);
        if (FAILED(hr))
        {
            printf("! Failed to get supported methods from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported methods found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pMethods->GetCount(&dwNumMethods);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported methods, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Methods Found on the service\n\n", dwNumMethods);

    // Loop through each method and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumMethods; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pMethods->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have a method.  It is assumed that
                // methods are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayMethod(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }    
}
```



<span data-ttu-id="61e9c-140">Depois que o método **ListSupportedMethods** recupera o GUID para cada evento com suporte pelo serviço determinado, ele invoca o método **DisplayMethod** para recuperar os atributos específicos do método.</span><span class="sxs-lookup"><span data-stu-id="61e9c-140">After the **ListSupportedMethods** method retrieves the GUID for each event supported by the given service, it invokes the **DisplayMethod** method to retrieve the method-specific attributes.</span></span> <span data-ttu-id="61e9c-141">Esses atributos incluem: o nome amigável de script do método, as restrições de acesso necessárias, qualquer formato associado e a lista de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="61e9c-141">These attributes include: the method's script-friendly name , required access restrictions, any associated format, and list of parameters.</span></span>

<span data-ttu-id="61e9c-142">O **método DisplayMethod** invoca o método [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) para recuperar uma coleção de atributos para o método determinado.</span><span class="sxs-lookup"><span data-stu-id="61e9c-142">The **DisplayMethod** method invokes the [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) method to retrieve a collection of attributes for the given method.</span></span> <span data-ttu-id="61e9c-143">Em seguida, ele chama [**o método IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) para recuperar o nome do método.</span><span class="sxs-lookup"><span data-stu-id="61e9c-143">It then calls the [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) method to retrieve the method's name.</span></span> <span data-ttu-id="61e9c-144">O **DisplayMethod** chama [**IPortableDeviceValues::GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md) para recuperar as restrctions de acesso.</span><span class="sxs-lookup"><span data-stu-id="61e9c-144">The **DisplayMethod** calls the [**IPortableDeviceValues::GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md) to retrieve the access restrctions.</span></span> <span data-ttu-id="61e9c-145">Depois disso, ele chama [**IPortableDeviceValues::GetGuidValue**](iportabledevicevalues-getguidvalue.md) para recuperar qualquer formato associado.</span><span class="sxs-lookup"><span data-stu-id="61e9c-145">After this, it calls [**IPortableDeviceValues::GetGuidValue**](iportabledevicevalues-getguidvalue.md) to retrieve any associated format.</span></span> <span data-ttu-id="61e9c-146">E, por fim, **DisplayMethod** chama [**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) para recuperar os dados do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="61e9c-146">And, finally, the **DisplayMethod** calls the [**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) to retrieve the parameter data.</span></span> <span data-ttu-id="61e9c-147">Ele passa os dados retornados por esses métodos para as funções auxiliares **DisplayMethodAccess,** **DisplayFormat** e **DisplayMethodParameters,** que renderizarão as informações para o método determinado.</span><span class="sxs-lookup"><span data-stu-id="61e9c-147">It passes the data returned by these methods to the **DisplayMethodAccess**, **DisplayFormat**, and **DisplayMethodParameters** helper functions, which render the information for the given method.</span></span>

<span data-ttu-id="61e9c-148">O código a seguir usa o **método DisplayMethod.**</span><span class="sxs-lookup"><span data-stu-id="61e9c-148">The following code uses the **DisplayMethod** method.</span></span>


```C++
// Display basic information about a method
void DisplayMethod(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Method)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    // Get the method attributes which describe the method
    HRESULT hr = pCapabilities->GetMethodAttributes(Method, &pAttributes);
    if (FAILED(hr))
    {
        printf("! Failed to get the method attributes, hr = 0x%lx\n",hr);
    }

    if (SUCCEEDED(hr))
    {
        PWSTR   pszMethodName  = NULL;
        DWORD   dwMethodAccess = WPD_COMMAND_ACCESS_READ;
        GUID    guidFormat     = GUID_NULL;

        CComPtr<IPortableDeviceValues>          pOptions;
        CComPtr<IPortableDeviceKeyCollection>   pParameters;

        // Display the name of the method if available. Otherwise, fall back to displaying the GUID.
        hr = pAttributes->GetStringValue(WPD_METHOD_ATTRIBUTE_NAME, &pszMethodName);
        if (SUCCEEDED(hr))
        {
            printf("%ws", pszMethodName);
        }
        else
        {
            printf("%ws", (PWSTR)CGuidToString(Method));
        }       

        // Display the method access if available, otherwise default to WPD_COMMAND_ACCESS_READ access
        hr = pAttributes->GetUnsignedIntegerValue(WPD_METHOD_ATTRIBUTE_ACCESS, &dwMethodAccess);
        if (FAILED(hr))
        {
            dwMethodAccess = WPD_COMMAND_ACCESS_READ;
            hr = S_OK;
        }
        printf("\n\tAccess: ");
        DisplayMethodAccess(dwMethodAccess);

        // Display the associated format if specified.
        // Methods that have an associated format may only be supported for that format.
        // Methods that don't have associated formats generally apply to the entire service.
        hr = pAttributes->GetGuidValue(WPD_METHOD_ATTRIBUTE_ASSOCIATED_FORMAT, &guidFormat);
        if (SUCCEEDED(hr))
        {
            printf("\n\tAssociated Format: ");
            DisplayFormat(pCapabilities, guidFormat);
        }

        // Display the method parameters, if available
        hr = pAttributes->GetIPortableDeviceKeyCollectionValue(WPD_METHOD_ATTRIBUTE_PARAMETERS, &pParameters);
        if (SUCCEEDED(hr))
        {
            DisplayMethodParameters(pCapabilities, Method, pParameters);
        }
        
        CoTaskMemFree(pszMethodName);
        pszMethodName = NULL;

    }
}
```



<span data-ttu-id="61e9c-149">A **função auxiliar DisplayMethodAccess** recebe um valor DWORD que contém as opções de acesso do método.</span><span class="sxs-lookup"><span data-stu-id="61e9c-149">The **DisplayMethodAccess** helper function receives a DWORD value that contains the method's access options.</span></span> <span data-ttu-id="61e9c-150">Ele compara esse valor com WPD COMMAND ACCESS READ e \_ \_ \_ WPD \_ COMMAND ACCESS \_ READWRITE para determinar o privilégio de acesso \_ do método.</span><span class="sxs-lookup"><span data-stu-id="61e9c-150">It compares this value to WPD\_COMMAND\_ACCESS\_READ and WPD\_COMMAND\_ACCESS\_READWRITE to determine the method's access privilege.</span></span> <span data-ttu-id="61e9c-151">Usando o resultado, ele renderiza uma cadeia de caracteres que indica a restrição de acesso para o método fornecido.</span><span class="sxs-lookup"><span data-stu-id="61e9c-151">Using the result, it renders a string indicating the access restriction for the given method.</span></span>

<span data-ttu-id="61e9c-152">O código a seguir usa a função auxiliar **DisplayMethodAccess** .</span><span class="sxs-lookup"><span data-stu-id="61e9c-152">The following code uses the **DisplayMethodAccess** helper function.</span></span>


```C++
void DisplayMethodAccess(
    DWORD   dwAccess)
{
    switch(static_cast<WPD_COMMAND_ACCESS_TYPES>(dwAccess))
    {
        case WPD_COMMAND_ACCESS_READ:
            printf("Read");
            break;
            
        case WPD_COMMAND_ACCESS_READWRITE:
            printf("Read/Write");
            break;

        default:
            printf("Unknown Access");
            break;
    }
}
```



<span data-ttu-id="61e9c-153">A função auxiliar **DisplayMethod** recebe um objeto [**IPORTABLEDEVICESERVICECAPABILITIES**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) e o GUID do método como parâmetros.</span><span class="sxs-lookup"><span data-stu-id="61e9c-153">The **DisplayMethod** helper function receives an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) object and the method's GUID as parameters.</span></span> <span data-ttu-id="61e9c-154">Usando o objeto **IPortableDeviceServiceCapabilities** , ele invoca o método [**IPortableDeviceServiceCapabilities:: getmethodattributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) para recuperar os atributos do método e renderizá-los na janela do console do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="61e9c-154">Using the **IPortableDeviceServiceCapabilities** object, it invokes the [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) method to retrieve the method attributes and render them in the application's console window.</span></span>

<span data-ttu-id="61e9c-155">A função auxiliar **DisplayMethodParameters** recebe um objeto [**IPORTABLEDEVICESERVICECAPABILITIES**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) , o GUID do método e um objeto IPortableDeviceKeyCollection que contém os parâmetros do método.</span><span class="sxs-lookup"><span data-stu-id="61e9c-155">The **DisplayMethodParameters** helper function receives an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) object, the method's GUID, and an IPortableDeviceKeyCollection object containing the method parameters.</span></span> <span data-ttu-id="61e9c-156">Usando o objeto [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) , ele invoca o método [**IPortableDeviceServiceCapabilities:: GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes) para recuperar o nome, o uso, o VarType e o formato do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="61e9c-156">Using the [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) object, it invokes the [**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes) method to retrieve the parameter's name, usage, VARTYPE, and form.</span></span> <span data-ttu-id="61e9c-157">Ele renderiza essas informações na janela do console do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="61e9c-157">It renders this information in the application's console window.</span></span>

<span data-ttu-id="61e9c-158">O código a seguir usa a função auxiliar **DisplayMethodParameters** .</span><span class="sxs-lookup"><span data-stu-id="61e9c-158">The following code uses the **DisplayMethodParameters** helper function.</span></span>


```C++
// Display the method parameters.
void DisplayMethodParameters(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Method,
    IPortableDeviceKeyCollection*       pParameters)
{
    DWORD   dwNumParameters = 0;

    // Get the number of parameters for this event.
    HRESULT hr = pParameters->GetCount(&dwNumParameters);
    if (FAILED(hr))
    {
        printf("! Failed to get number of parameters, hr = 0x%lx\n",hr);
    }

    printf("\n\t%d Method Parameters:\n", dwNumParameters);

    // Loop through each parameter and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumParameters; dwIndex++)
        {
            PROPERTYKEY parameter;
            hr = pParameters->GetAt(dwIndex, &parameter);

            if (SUCCEEDED(hr))
            {
                CComPtr<IPortableDeviceValues> pAttributes;

                // Display the parameter's Name, Usage, Vartype, and Form
                hr = pCapabilities->GetMethodParameterAttributes(Method, parameter, &pAttributes);
                if (FAILED(hr))
                {
                    printf("! Failed to get the method parameter attributes, hr = 0x%lx\n",hr);
                }

                if (SUCCEEDED(hr))
                {
                    PWSTR   pszParameterName    = NULL;
                    DWORD   dwAttributeVarType  = 0;
                    DWORD   dwAttributeForm     = WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED;
                    DWORD   dwAttributeUsage    = (DWORD)-1;

                    hr = pAttributes->GetStringValue(WPD_PARAMETER_ATTRIBUTE_NAME, &pszParameterName);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tName: %ws\n", pszParameterName);
                    }
                    else
                    {
                        printf("! Failed to get the method parameter name, hr = 0x%lx\n",hr);
                    }

                    // Read the WPD_PARAMETER_ATTRIBUTE_USAGE value, if specified. 
                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_USAGE, &dwAttributeUsage);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tUsage: ");
                        DisplayParameterUsage(dwAttributeUsage);
                        printf("\n");
                    }
                    else
                    {
                        printf("! Failed to get the method parameter usage, hr = 0x%lx\n",hr);
                    }

                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_VARTYPE, &dwAttributeVarType);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tVARTYPE: ");
                        DisplayVarType(static_cast<VARTYPE>(dwAttributeVarType));
                        printf("\n");
                    }
                    else
                    {
                        printf("! Failed to get the method parameter VARTYPE, hr = 0x%lx\n",hr);
                    }

                    // Read the WPD_PARAMETER_ATTRIBUTE_FORM value.
                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_FORM, &dwAttributeForm);
                    if (FAILED(hr))
                    {
                        // If the read fails, assume WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED
                        dwAttributeForm = WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED;
                        hr = S_OK;
                    }

                    printf("\t\tForm: ");
                    DisplayParameterForm(dwAttributeForm);
                    printf("\n");

                    CoTaskMemFree(pszParameterName);
                    pszParameterName = NULL;
                }
                
                printf("\n");
            }
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="61e9c-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="61e9c-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61e9c-160">**IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="61e9c-160">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="61e9c-161">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="61e9c-161">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="61e9c-162">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="61e9c-162">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[<span data-ttu-id="61e9c-163">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="61e9c-163">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="61e9c-164">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="61e9c-164">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



