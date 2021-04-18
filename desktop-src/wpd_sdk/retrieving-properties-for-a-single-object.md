---
description: Recuperando propriedades de um único objeto
ms.assetid: e4e3b286-6330-4147-a367-57accf5beae6
title: Recuperando propriedades de um único objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5851b31256659c2ca036bac504a53fa51a20ee14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780658"
---
# <a name="retrieving-properties-for-a-single-object"></a><span data-ttu-id="e0b3b-103">Recuperando propriedades de um único objeto</span><span class="sxs-lookup"><span data-stu-id="e0b3b-103">Retrieving Properties for a Single Object</span></span>

<span data-ttu-id="e0b3b-104">Depois que o aplicativo recupera um identificador de objeto (consulte o tópico [enumerando conteúdo](enumerating-content.md) ) para um determinado objeto, ele pode recuperar informações descritivas sobre esse objeto chamando métodos na [**interface IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) e na [**interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md).</span><span class="sxs-lookup"><span data-stu-id="e0b3b-104">After your application retrieves an object identifier (see the [Enumerating Content](enumerating-content.md) topic) for a given object, it can retrieve descriptive information about that object by calling methods in the [**IPortableDeviceProperties interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) and the [**IPortableDeviceKeyCollection interface**](iportabledevicekeycollection.md).</span></span>

<span data-ttu-id="e0b3b-105">O método [**IPortableDeviceProperties:: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) recupera uma lista de propriedades especificadas para um determinado objeto.</span><span class="sxs-lookup"><span data-stu-id="e0b3b-105">The [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method retrieves a list of specified properties for a given object.</span></span> <span data-ttu-id="e0b3b-106">(O aplicativo também pode chamar o método GetValues e especificar um valor **nulo** para o parâmetro pKeys para recuperar todas as propriedades de um determinado objeto; no entanto, o desempenho desse método pode ser significativamente mais lento ao recuperar todas as propriedades.)</span><span class="sxs-lookup"><span data-stu-id="e0b3b-106">(Your application could also call the GetValues method and specify a **NULL** value for the pKeys parameter to retrieve all properties for a given object; however, the performance of this method may be significantly slower when retrieving all properties.)</span></span>

<span data-ttu-id="e0b3b-107">No entanto, antes que seu aplicativo chame GetValues, ele precisa identificar as propriedades a serem recuperadas definindo as chaves correspondentes em um [**objeto IPortableDeviceKeyCollection**](iportabledevicekeycollection.md).</span><span class="sxs-lookup"><span data-stu-id="e0b3b-107">Before your application calls GetValues, however, it needs to identify the properties to retrieve by setting corresponding keys in an [**IPortableDeviceKeyCollection object**](iportabledevicekeycollection.md).</span></span> <span data-ttu-id="e0b3b-108">Seu aplicativo identificará as propriedades de interesse chamando o método [**IPortableDeviceKeyCollection:: Add**](iportabledevicekeycollection-add.md) e fornecendo um valor PROPERTYKEY que identifica cada propriedade que será recuperada.</span><span class="sxs-lookup"><span data-stu-id="e0b3b-108">Your application will identify the properties of interest by calling the [**IPortableDeviceKeyCollection::Add**](iportabledevicekeycollection-add.md) method and supplying a PROPERTYKEY value that identifies each property that it will retrieve.</span></span>

<span data-ttu-id="e0b3b-109">A função ReadContentProperties no módulo Contentproperties. cpp do aplicativo de exemplo demonstra como as cinco propriedades foram recuperadas para um objeto selecionado.</span><span class="sxs-lookup"><span data-stu-id="e0b3b-109">The ReadContentProperties function in the ContentProperties.cpp module of the sample application demonstrates how the five properties were retrieved for a selected object.</span></span> <span data-ttu-id="e0b3b-110">A tabela a seguir descreve cada uma dessas propriedades e seu valor REFPROPERTYKEY correspondente.</span><span class="sxs-lookup"><span data-stu-id="e0b3b-110">The following table describes each of these properties and their corresponding REFPROPERTYKEY value.</span></span>



| <span data-ttu-id="e0b3b-111">Propriedade</span><span class="sxs-lookup"><span data-stu-id="e0b3b-111">Property</span></span>                     | <span data-ttu-id="e0b3b-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0b3b-112">Description</span></span>                                                                                                                                      | <span data-ttu-id="e0b3b-113">PROPERTYKEY</span><span class="sxs-lookup"><span data-stu-id="e0b3b-113">PROPERTYKEY</span></span>                         |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="e0b3b-114">Identificador de objeto pai</span><span class="sxs-lookup"><span data-stu-id="e0b3b-114">Parent-object identifier</span></span>     | <span data-ttu-id="e0b3b-115">Uma cadeia de caracteres que especifica o identificador para o pai do objeto fornecido.</span><span class="sxs-lookup"><span data-stu-id="e0b3b-115">A string that specifies the identifier for the given object's parent.</span></span>                                                                            | <span data-ttu-id="e0b3b-116">\_ \_ ID pai do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="e0b3b-116">WPD\_OBJECT\_PARENT\_ID</span></span>             |
| <span data-ttu-id="e0b3b-117">Nome do objeto</span><span class="sxs-lookup"><span data-stu-id="e0b3b-117">Object name</span></span>                  | <span data-ttu-id="e0b3b-118">Uma cadeia de caracteres que especifica o nome do objeto fornecido.</span><span class="sxs-lookup"><span data-stu-id="e0b3b-118">A string that specifies the name of the given object.</span></span>                                                                                            | <span data-ttu-id="e0b3b-119">\_nome do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="e0b3b-119">WPD\_OBJECT\_NAME</span></span>                   |
| <span data-ttu-id="e0b3b-120">Identificador exclusivo persistente</span><span class="sxs-lookup"><span data-stu-id="e0b3b-120">Persistent unique identifier</span></span> | <span data-ttu-id="e0b3b-121">Uma cadeia de caracteres que especifica um identificador exclusivo para o objeto fornecido.</span><span class="sxs-lookup"><span data-stu-id="e0b3b-121">A string that specifies a unique identifier for the given object.</span></span> <span data-ttu-id="e0b3b-122">(Esse identificador é persistente entre as sessões, ao contrário do identificador de objeto.)</span><span class="sxs-lookup"><span data-stu-id="e0b3b-122">(This identifier is persistent across sessions, unlike the object identifier.)</span></span> | <span data-ttu-id="e0b3b-123">\_ \_ \_ ID exclusiva persistente do objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="e0b3b-123">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span> |
| <span data-ttu-id="e0b3b-124">Formato do objeto</span><span class="sxs-lookup"><span data-stu-id="e0b3b-124">Object format</span></span>                | <span data-ttu-id="e0b3b-125">Um GUID (identificador global exclusivo) que especifica o formato do arquivo correspondente a um determinado objeto.</span><span class="sxs-lookup"><span data-stu-id="e0b3b-125">A globally unique identifier (GUID) that specifies the format of the file corresponding to a given object.</span></span>                                       | <span data-ttu-id="e0b3b-126">\_formato de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="e0b3b-126">WPD\_OBJECT\_FORMAT</span></span>                 |
| <span data-ttu-id="e0b3b-127">Tipo de conteúdo do objeto</span><span class="sxs-lookup"><span data-stu-id="e0b3b-127">Object content type</span></span>          | <span data-ttu-id="e0b3b-128">Um GUID que especifica o tipo de conteúdo associado a um determinado objeto.</span><span class="sxs-lookup"><span data-stu-id="e0b3b-128">A GUID that specifies the type of content associated with a given object.</span></span>                                                                        | <span data-ttu-id="e0b3b-129">\_tipo de \_ conteúdo de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="e0b3b-129">WPD\_OBJECT\_CONTENT\_TYPE</span></span>          |



 

<span data-ttu-id="e0b3b-130">O trecho a seguir da função ReadContentProperties demonstra como o aplicativo de exemplo usou a [**interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) e o método [**IPortableDeviceKeyCollection:: Add**](iportabledevicekeycollection-add.md) para identificar as propriedades que ele recuperaria.</span><span class="sxs-lookup"><span data-stu-id="e0b3b-130">The following excerpt from the ReadContentProperties function demonstrates how the sample application used the [**IPortableDeviceKeyCollection interface**](iportabledevicekeycollection.md) and the [**IPortableDeviceKeyCollection::Add**](iportabledevicekeycollection-add.md) method to identify the properties it would retrieve.</span></span>


```C++
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
        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_PARENT_ID);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_PARENT_ID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_NAME);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_NAME to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_PERSISTENT_UNIQUE_ID);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_PERSISTENT_UNIQUE_ID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_FORMAT);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_FORMAT to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_CONTENT_TYPE);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_CONTENT_TYPE to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }
    }
}
```



<span data-ttu-id="e0b3b-131">Depois que o aplicativo de exemplo definir as chaves apropriadas, ele chamou o método [**IPortableDeviceProperties:: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) para recuperar os valores especificados para o objeto fornecido.</span><span class="sxs-lookup"><span data-stu-id="e0b3b-131">Once the sample application set the appropriate keys, it called the [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method to retrieve the specified values for the given object.</span></span>


```C++
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
```



## <a name="related-topics"></a><span data-ttu-id="e0b3b-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e0b3b-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0b3b-133">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="e0b3b-133">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="e0b3b-134">**Interface IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="e0b3b-134">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="e0b3b-135">**Interface IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="e0b3b-135">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="e0b3b-136">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="e0b3b-136">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



