---
title: Recuperando as propriedades do objeto WPD
description: O aplicativo WpdServiceApiSample demonstra como um aplicativo pode recuperar as propriedades de objeto de conteúdo com suporte de um determinado serviço de contatos.
ms.assetid: 7fbd6f65-366a-49ea-a680-be77ca0d64f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98e57258993d0a81f68042195db2caf338c97c53
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404309"
---
# <a name="retrieving-wpd-object-properties"></a><span data-ttu-id="36da1-103">Recuperando as propriedades do objeto WPD</span><span class="sxs-lookup"><span data-stu-id="36da1-103">Retrieving WPD object properties</span></span>

<span data-ttu-id="36da1-104">Os serviços geralmente contêm objetos filho que pertencem a um dos formatos aos quais cada serviço dá suporte.</span><span class="sxs-lookup"><span data-stu-id="36da1-104">Services often contain child objects that belong to one of the formats that each service supports.</span></span> <span data-ttu-id="36da1-105">Por exemplo, um serviço de contatos pode dar suporte a vários objetos de contato do formato de contato abstrato.</span><span class="sxs-lookup"><span data-stu-id="36da1-105">For example, a Contacts service may support multiple contact objects of the Abstract Contact format.</span></span> <span data-ttu-id="36da1-106">Cada objeto de contato é descrito pelas propriedades relacionadas (nome do contato, número de telefone, endereço de email e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="36da1-106">Each contact object is described by related properties (contact name, phone number, email address, and so on).</span></span>

<span data-ttu-id="36da1-107">O aplicativo WpdServiceApiSample inclui código que demonstra como um aplicativo pode recuperar as propriedades de objeto de conteúdo com suporte em um determinado serviço de contatos.</span><span class="sxs-lookup"><span data-stu-id="36da1-107">The WpdServiceApiSample application includes code that demonstrates how an application can retrieve the content-object properties supported by a given Contacts service.</span></span> <span data-ttu-id="36da1-108">Este exemplo usa as seguintes interfaces.</span><span class="sxs-lookup"><span data-stu-id="36da1-108">This sample uses the following interfaces.</span></span>



| <span data-ttu-id="36da1-109">Interface</span><span class="sxs-lookup"><span data-stu-id="36da1-109">Interface</span></span> | <span data-ttu-id="36da1-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="36da1-110">Description</span></span>    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36da1-111">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="36da1-111">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | <span data-ttu-id="36da1-112">Recupera a interface **IPortableDeviceContent2** para acessar os métodos de serviço com suporte.</span><span class="sxs-lookup"><span data-stu-id="36da1-112">Retrieves the **IPortableDeviceContent2** interface to access the supported service methods.</span></span> |
| [<span data-ttu-id="36da1-113">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="36da1-113">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | <span data-ttu-id="36da1-114">Fornece acesso aos métodos específicos de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="36da1-114">Provides access to the content-specific methods.</span></span>                                             |
| [<span data-ttu-id="36da1-115">**IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="36da1-115">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)       | <span data-ttu-id="36da1-116">Recupera os valores de Propriedade do objeto.</span><span class="sxs-lookup"><span data-stu-id="36da1-116">Retrieves the object property values.</span></span>                                                        |
| [<span data-ttu-id="36da1-117">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="36da1-117">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)               | <span data-ttu-id="36da1-118">Mantém os valores de propriedade que foram lidos para esse objeto.</span><span class="sxs-lookup"><span data-stu-id="36da1-118">Holds the property values that were read for that object.</span></span>                                    |
| [<span data-ttu-id="36da1-119">**IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="36da1-119">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md) | <span data-ttu-id="36da1-120">Contém os parâmetros para um determinado método.</span><span class="sxs-lookup"><span data-stu-id="36da1-120">Contains the parameters for a given method.</span></span>                                                  |



 

<span data-ttu-id="36da1-121">Quando o usuário escolhe a opção "7" na linha de comando, o aplicativo invoca o método **ReadContentProperties** encontrado no módulo contentproperties. cpp.</span><span class="sxs-lookup"><span data-stu-id="36da1-121">When the user chooses option "7" at the command line, the application invokes the **ReadContentProperties** method that is found in the ContentProperties.cpp module.</span></span>

<span data-ttu-id="36da1-122">Esse método recupera as quatro propriedades a seguir para o objeto de contato especificado.</span><span class="sxs-lookup"><span data-stu-id="36da1-122">This method retrieves the following four properties for the specified contact object.</span></span>



| <span data-ttu-id="36da1-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="36da1-123">Property</span></span>                     | <span data-ttu-id="36da1-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="36da1-124">Description</span></span>                                                                                                                                                                                                      | <span data-ttu-id="36da1-125">PROPERTYKEY dos serviços de dispositivo</span><span class="sxs-lookup"><span data-stu-id="36da1-125">Device Services PROPERTYKEY</span></span>     | <span data-ttu-id="36da1-126">PROPERTYKEY de WPD equivalente \_</span><span class="sxs-lookup"><span data-stu-id="36da1-126">Equivalent WPD\_PROPERTYKEY</span></span>         |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|-------------------------------------|
| <span data-ttu-id="36da1-127">Identificador de objeto pai</span><span class="sxs-lookup"><span data-stu-id="36da1-127">Parent-object identifier</span></span>     | <span data-ttu-id="36da1-128">Uma cadeia de caracteres que especifica o identificador para o pai do objeto fornecido.</span><span class="sxs-lookup"><span data-stu-id="36da1-128">A string that specifies the identifier for the given object's parent.</span></span>                                                                                                                                            | <span data-ttu-id="36da1-129">PKEY \_ GenericObj \_ parentID</span><span class="sxs-lookup"><span data-stu-id="36da1-129">PKEY\_GenericObj\_ParentID</span></span>      | <span data-ttu-id="36da1-130">\_ \_ ID pai do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="36da1-130">WPD\_OBJECT\_PARENT\_ID</span></span>             |
| <span data-ttu-id="36da1-131">Nome do objeto</span><span class="sxs-lookup"><span data-stu-id="36da1-131">Object name</span></span>                  | <span data-ttu-id="36da1-132">Uma cadeia de caracteres que especifica o nome do objeto fornecido</span><span class="sxs-lookup"><span data-stu-id="36da1-132">A string that specifies the name of the given object</span></span>                                                                                                                                                             | <span data-ttu-id="36da1-133">PKEY \_ \_ nome GenericObj</span><span class="sxs-lookup"><span data-stu-id="36da1-133">PKEY\_GenericObj\_Name</span></span>          | <span data-ttu-id="36da1-134">\_nome do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="36da1-134">WPD\_OBJECT\_NAME</span></span>                   |
| <span data-ttu-id="36da1-135">Identificador exclusivo persistente</span><span class="sxs-lookup"><span data-stu-id="36da1-135">Persistent unique identifier</span></span> | <span data-ttu-id="36da1-136">Uma cadeia de caracteres que especifica um identificador exclusivo para o objeto fornecido.</span><span class="sxs-lookup"><span data-stu-id="36da1-136">A string that specifies a unique identifier for the given object.</span></span> <span data-ttu-id="36da1-137">Esse identificador é persistente entre as sessões, ao contrário do identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="36da1-137">This identifier is persistent across sessions, unlike the object identifier.</span></span> <span data-ttu-id="36da1-138">Para serviços, isso precisa ser uma representação de cadeia de caracteres de um GUID.</span><span class="sxs-lookup"><span data-stu-id="36da1-138">For services, this needs to be a string-representation of a GUID.</span></span> | <span data-ttu-id="36da1-139">PKEY \_ GenericObj \_ PersistentUID</span><span class="sxs-lookup"><span data-stu-id="36da1-139">PKEY\_GenericObj\_PersistentUID</span></span> | <span data-ttu-id="36da1-140">\_ \_ \_ ID exclusiva persistente do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="36da1-140">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span> |
| <span data-ttu-id="36da1-141">Formato do objeto</span><span class="sxs-lookup"><span data-stu-id="36da1-141">Object format</span></span>                | <span data-ttu-id="36da1-142">Um GUID (identificador global exclusivo) que especifica o formato do arquivo correspondente a um determinado objeto</span><span class="sxs-lookup"><span data-stu-id="36da1-142">A globally unique identifier (GUID) that specifies the format of the file corresponding to a given object</span></span>                                                                                                        | <span data-ttu-id="36da1-143">PKEY \_ GenericObj \_ objectformat</span><span class="sxs-lookup"><span data-stu-id="36da1-143">PKEY\_GenericObj\_ObjectFormat</span></span>  | <span data-ttu-id="36da1-144">\_formato de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="36da1-144">WPD\_OBJECT\_FORMAT</span></span>                 |



 

-   <span data-ttu-id="36da1-145">ID do pai</span><span class="sxs-lookup"><span data-stu-id="36da1-145">Parent ID</span></span>
-   <span data-ttu-id="36da1-146">Name</span><span class="sxs-lookup"><span data-stu-id="36da1-146">Name</span></span>
-   <span data-ttu-id="36da1-147">PersistentUID</span><span class="sxs-lookup"><span data-stu-id="36da1-147">PersistentUID</span></span>
-   <span data-ttu-id="36da1-148">Formatar</span><span class="sxs-lookup"><span data-stu-id="36da1-148">Format</span></span>

<span data-ttu-id="36da1-149">Observe que, antes de recuperar as propriedades de conteúdo, o aplicativo de exemplo abre um serviço de contatos em um dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="36da1-149">Note that prior to retrieving the content properties, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="36da1-150">O código a seguir para o método **ReadContentProperties** demonstra como o aplicativo usa a interface [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) para recuperar uma interface [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) .</span><span class="sxs-lookup"><span data-stu-id="36da1-150">The following code for the **ReadContentProperties** method demonstrates how the application uses the [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) interface to retrieve an [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) interface.</span></span> <span data-ttu-id="36da1-151">Ao passar o PROPERTYKEYS das propriedades solicitadas para o método [**IPortableDeviceProperties:: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) , **ReadContentProperties** recupera os valores solicitados e os exibe na janela do console.</span><span class="sxs-lookup"><span data-stu-id="36da1-151">By passing the PROPERTYKEYS of the requested properties to the [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method, **ReadContentProperties** retrieves the requested values, and then displays them to the console window.</span></span>


```C++
// Reads properties for the user specified object.
void ReadContentProperties(
    IPortableDeviceService*    pService)
{
    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    HRESULT                               hr              = S_OK;
    WCHAR                                 szSelection[81] = {0};
    CComPtr<IPortableDeviceProperties>    pProperties;
    CComPtr<IPortableDeviceValues>        pObjectProperties;
    CComPtr<IPortableDeviceContent2>      pContent;
    CComPtr<IPortableDeviceKeyCollection> pPropertiesToRead;

    // Prompt user to enter an object identifier on the device to read properties from.
    printf("Enter the identifer of the object you wish to read properties from.\n>");
    hr = StringCbGetsW(szSelection,sizeof(szSelection));
    if (FAILED(hr))
    {
        printf("An invalid object identifier was specified, aborting property reading\n");
    }

    // 1) Get an IPortableDeviceContent2 interface from the IPortableDeviceService interface to
    // access the content-specific methods.
    if (SUCCEEDED(hr))
    {
        hr = pService->Content(&pContent);
        if (FAILED(hr))
        {
            printf("! Failed to get IPortableDeviceContent2 from IPortableDeviceService, hr = 0x%lx\n",hr);
        }
    }

    // 2) Get an IPortableDeviceProperties interface from the IPortableDeviceContent2 interface
    // to access the property-specific methods.
    if (SUCCEEDED(hr))
    {
        hr = pContent->Properties(&pProperties);
        if (FAILED(hr))
        {
            printf("! Failed to get IPortableDeviceProperties from IPortableDeviceContent2, hr = 0x%lx\n",hr);
        }
    }

    // 3) CoCreate an IPortableDeviceKeyCollection interface to hold the property keys
    // we wish to read.
    hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&pPropertiesToRead));
    if (SUCCEEDED(hr))
    {
        // 4) Populate the IPortableDeviceKeyCollection with the keys we wish to read.
        // NOTE: We are not handling any special error cases here so we can proceed with
        // adding as many of the target properties as we can.
        if (pPropertiesToRead != NULL)
        {
            HRESULT hrTemp = S_OK;
            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_ParentID);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_ParentID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_Name);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_Name to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_PersistentUID);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_PersistentUID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_ObjectFormat);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_ObjectFormat to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

        }
    }

    // 5) Call GetValues() passing the collection of specified PROPERTYKEYs.
    if (SUCCEEDED(hr))
    {
        hr = pProperties->GetValues(szSelection,         // The object whose properties we are reading
                                    pPropertiesToRead,   // The properties we want to read
                                    &pObjectProperties); // Driver supplied property values for the specified object
        if (FAILED(hr))
        {
            printf("! Failed to get all properties for object '%ws', hr= 0x%lx\n", szSelection, hr);
        }
    }

    // 6) Display the returned property values to the user
    if (SUCCEEDED(hr))
    {
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_ParentID,        NAME_GenericObj_ParentID);
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_Name,            NAME_GenericObj_Name);
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_PersistentUID,   NAME_GenericObj_PersistentUID);
        DisplayGuidProperty  (pObjectProperties, PKEY_GenericObj_ObjectFormat,    NAME_GenericObj_ObjectFormat);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="36da1-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="36da1-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36da1-153">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="36da1-153">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="36da1-154">**IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="36da1-154">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="36da1-155">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="36da1-155">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



