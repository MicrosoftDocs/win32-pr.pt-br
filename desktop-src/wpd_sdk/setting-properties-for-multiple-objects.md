---
description: Definindo propriedades para vários objetos
ms.assetid: 0686ba54-4782-42a4-8fdb-2325fc8d8bc2
title: Definindo propriedades para vários objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e951662d9920cb22db0a417f1af94f3eb7eb4d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764176"
---
# <a name="setting-properties-for-multiple-objects"></a><span data-ttu-id="e8c49-103">Definindo propriedades para vários objetos</span><span class="sxs-lookup"><span data-stu-id="e8c49-103">Setting Properties for Multiple Objects</span></span>

<span data-ttu-id="e8c49-104">Alguns drivers de dispositivo dão suporte à definição de propriedades para vários objetos em uma única chamada de função — isso é conhecido como uma gravação em massa.</span><span class="sxs-lookup"><span data-stu-id="e8c49-104">Some device drivers support setting properties for multiple objects in a single function call—this is referred to as a bulk write.</span></span> <span data-ttu-id="e8c49-105">Seu aplicativo pode executar uma gravação em massa usando as interfaces descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e8c49-105">Your application can perform a bulk write using the interfaces described in the following table.</span></span>



| <span data-ttu-id="e8c49-106">Interface</span><span class="sxs-lookup"><span data-stu-id="e8c49-106">Interface</span></span>                                                                                      | <span data-ttu-id="e8c49-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e8c49-107">Description</span></span>                                                  |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="e8c49-108">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="e8c49-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="e8c49-109">Fornece acesso aos métodos específicos de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="e8c49-109">Provides access to the content-specific methods.</span></span>             |
| [<span data-ttu-id="e8c49-110">**Interface IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="e8c49-110">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="e8c49-111">Fornece acesso aos métodos específicos da propriedade.</span><span class="sxs-lookup"><span data-stu-id="e8c49-111">Provides access to the property-specific methods.</span></span>            |
| [<span data-ttu-id="e8c49-112">**Interface IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="e8c49-112">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | <span data-ttu-id="e8c49-113">Dá suporte à operação de gravação em massa.</span><span class="sxs-lookup"><span data-stu-id="e8c49-113">Supports the bulk write operation.</span></span>                           |
| [<span data-ttu-id="e8c49-114">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="e8c49-114">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="e8c49-115">Usado para armazenar os identificadores de objeto para a operação em massa.</span><span class="sxs-lookup"><span data-stu-id="e8c49-115">Used to store the object identifiers for the bulk operation.</span></span> |
| [<span data-ttu-id="e8c49-116">**Interface IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="e8c49-116">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)           | <span data-ttu-id="e8c49-117">Usado para identificar as propriedades a serem gravadas.</span><span class="sxs-lookup"><span data-stu-id="e8c49-117">Used to identify the properties to be written.</span></span>               |



 

<span data-ttu-id="e8c49-118">A `WriteContentPropertiesBulk` função no módulo contentproperties. cpp do aplicativo de exemplo demonstra uma operação de gravação em massa.</span><span class="sxs-lookup"><span data-stu-id="e8c49-118">The `WriteContentPropertiesBulk` function in the sample application's ContentProperties.cpp module demonstrates a bulk write operation.</span></span>

<span data-ttu-id="e8c49-119">A primeira tarefa realizada neste exemplo é determinar se o driver fornecido oferece suporte a operações em massa.</span><span class="sxs-lookup"><span data-stu-id="e8c49-119">The first task accomplished in this sample is determining whether or not the given driver supports bulk operations.</span></span> <span data-ttu-id="e8c49-120">Isso é feito chamando QueryInterface em um objeto **IPortableDeviceProperties** e verificando a existência de **IPortableDevicePropertiesBulk**.</span><span class="sxs-lookup"><span data-stu-id="e8c49-120">This is accomplished by calling QueryInterface on an **IPortableDeviceProperties** object and checking for the existence of **IPortableDevicePropertiesBulk**.</span></span>


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}



if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}



if (SUCCEEDED(hr))
{
    hr = pProperties->QueryInterface(IID_PPV_ARGS(&pPropertiesBulk));
    if (FAILED(hr))
    {
        printf("This driver does not support BULK property operations.\n");
    }
}
```



<span data-ttu-id="e8c49-121">A próxima tarefa envolve a criação de um objeto **IPortableDeviceValuesCollection** .</span><span class="sxs-lookup"><span data-stu-id="e8c49-121">The next task entails creating an **IPortableDeviceValuesCollection** object.</span></span> <span data-ttu-id="e8c49-122">Esse é o objeto que contém os valores de propriedade que o exemplo gravará.</span><span class="sxs-lookup"><span data-stu-id="e8c49-122">This is the object that contains the property values that the sample will write.</span></span>


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
if (SUCCEEDED(hr))
{
    hr = CoCreateInstance(CLSID_PortableDeviceValuesCollection,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IPortableDeviceValuesCollection,
                          (VOID**) &pPropertiesToWrite);
    if (FAILED(hr))
    {
        printf("! Failed to CoCreate IPortableDeviceValuesCollection for bulk property values, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="e8c49-123">Depois disso, o exemplo cria uma instância da [**interface IPortableDevicePropertiesBulkCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk).</span><span class="sxs-lookup"><span data-stu-id="e8c49-123">After this, the sample creates an instance of the [**IPortableDevicePropertiesBulkCallback interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk).</span></span> <span data-ttu-id="e8c49-124">O aplicativo usará os métodos nesta interface para acompanhar o progresso da operação de gravação em massa assíncrona.</span><span class="sxs-lookup"><span data-stu-id="e8c49-124">The application will use the methods in this interface to track the progress of the asynchronous bulk-write operation.</span></span>


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
if (SUCCEEDED(hr))
{
    pCallback = new CSetBulkValuesCallback();
    if (pCallback == NULL)
    {
        hr = E_OUTOFMEMORY;
        printf("! Failed to allocate CSetBulkValuesCallback, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="e8c49-125">A próxima função que o aplicativo de exemplo chama é a `CreateIPortableDevicePropVariantCollectionWithAllObjectIDs` função auxiliar.</span><span class="sxs-lookup"><span data-stu-id="e8c49-125">The next function that the sample application calls is the `CreateIPortableDevicePropVariantCollectionWithAllObjectIDs` helper function.</span></span> <span data-ttu-id="e8c49-126">Essa função enumera recursivamente todos os objetos em um determinado dispositivo e retorna uma [**interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contém um identificador para cada objeto encontrado.</span><span class="sxs-lookup"><span data-stu-id="e8c49-126">This function recursively enumerates all objects on a given device and returns an [**IPortableDevicePropVariantCollection interface**](iportabledevicepropvariantcollection.md) that contains an identifier for each object that it found.</span></span> <span data-ttu-id="e8c49-127">Essa função é definida no módulo ContentEnumeration. cpp.</span><span class="sxs-lookup"><span data-stu-id="e8c49-127">This function is defined in the module ContentEnumeration.cpp.</span></span>


```C++
// 7) Call our helper function CreateIPortableDevicePropVariantCollectionWithAllObjectIDs
// to enumerate and create an IPortableDevicePropVariantCollection with the object
// identifiers needed to perform the bulk operation on.
if (SUCCEEDED(hr))
{
    hr = CreateIPortableDevicePropVariantCollectionWithAllObjectIDs(pDevice,
                                                                    pContent,
                                                                    &pObjectIDs);
}
```



<span data-ttu-id="e8c49-128">O objeto **IPortableDevicePropVariantCollection** contém uma coleção de valores **PROPVARIANT** indexados do mesmo VarType.</span><span class="sxs-lookup"><span data-stu-id="e8c49-128">The **IPortableDevicePropVariantCollection** object holds a collection of indexed **PROPVARIANT** values of the same VARTYPE.</span></span> <span data-ttu-id="e8c49-129">Nesse caso, esses valores contêm um determinado identificador de objeto para cada objeto encontrado no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e8c49-129">In this case, these values contain a given object identifier for each object found on the device.</span></span>

<span data-ttu-id="e8c49-130">Os identificadores de objeto e suas respectivas propriedades de nome são armazenados em um objeto [**IPortableDeviceValuesCollection**](iportabledevicevalues.md) .</span><span class="sxs-lookup"><span data-stu-id="e8c49-130">The object identifiers and their respective name properties are stored in an [**IPortableDeviceValuesCollection**](iportabledevicevalues.md) object.</span></span> <span data-ttu-id="e8c49-131">As propriedades de nome são organizadas para que o primeiro objeto receba uma propriedade Name de "NewName0", o segundo objeto recebe uma propriedade Name de "NewName1" e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="e8c49-131">The name properties are organized so that the first object is assigned a name property of "NewName0", the second object is assigned a name property of "NewName1", and so on.</span></span>

<span data-ttu-id="e8c49-132">O trecho a seguir do exemplo demonstra como o objeto **IPortableDeviceValuesCollection** foi inicializado com identificadores de objeto e novas cadeias de caracteres de nome.</span><span class="sxs-lookup"><span data-stu-id="e8c49-132">The following excerpt from the sample demonstrates how the **IPortableDeviceValuesCollection** object was initialized with object identifiers and new name strings.</span></span>


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
if (SUCCEEDED(hr))
{
    hr = pObjectIDs->GetCount(&cObjectIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get number of objectIDs from IPortableDevicePropVariantCollection, hr = 0x%lx\n", hr);
    }
}


if (SUCCEEDED(hr))
{
    for(DWORD dwIndex = 0; (dwIndex < cObjectIDs) && (hr == S_OK); dwIndex++)
    {
        CComPtr<IPortableDeviceValues>  pValues;
        PROPVARIANT                     pv = {0};

        PropVariantInit(&pv);
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IPortableDeviceValues,
                              (VOID**) &pValues);
        if (FAILED(hr))
        {
            printf("! Failed to CoCreate CLSID_PortableDeviceValues, hr = 0x%lx\n", hr);
        }

        // Get the Object ID whose properties we will set
        if (hr == S_OK)
        {
            hr = pObjectIDs->GetAt(dwIndex, &pv);
            if (FAILED(hr))
            {
                printf("! Failed to get next Object ID from list, hr = 0x%lx\n", hr);
            }
        }

        // Save them into the IPortableDeviceValues so the driver knows which object this proeprty set belongs to
        if (hr == S_OK)
        {
            hr = pValues->SetStringValue(WPD_OBJECT_ID, pv.pwszVal);
            if (FAILED(hr))
            {
                printf("! Failed to set WPD_OBJECT_ID, hr = 0x%lx\n", hr);
            }
        }

        // Set the new values.  In this sample, we attempt to set the name property.
        if (hr == S_OK)
        {
            CAtlStringW strValue;
            strValue.Format(L"NewName%d", dwIndex);

            hr = pValues->SetStringValue(WPD_OBJECT_NAME, strValue.GetString());
            if (FAILED(hr))
            {
                printf("! Failed to set WPD_OBJECT_NAME, hr = 0x%lx\n", hr);
            }
        }

        // Add this property set to the collection
        if (hr == S_OK)
        {
            hr = pPropertiesToWrite->Add(pValues);
            if (FAILED(hr))
            {
                printf("! Failed to add values to collection, hr = 0x%lx\n", hr);
            }
        }
        PropVariantClear(&pv);
    }
}
```



<span data-ttu-id="e8c49-133">Depois que o exemplo cria o objeto **IPortableDeviceValuesCollection** que contém o identificador de objeto e os pares de nome, ele pode iniciar a operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="e8c49-133">Once the sample creates the **IPortableDeviceValuesCollection** object that contains the object identifier and name pairs, it can begin the asynchronous operation.</span></span>

<span data-ttu-id="e8c49-134">A operação de gravação assíncrona começa quando o exemplo chama o método [**IPortableDevicePropertiesBulk:: QueueSetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuesetvaluesbyobjectlist) .</span><span class="sxs-lookup"><span data-stu-id="e8c49-134">The asynchronous write operation begins when the sample calls the [**IPortableDevicePropertiesBulk::QueueSetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuesetvaluesbyobjectlist) method.</span></span> <span data-ttu-id="e8c49-135">Esse método notifica o driver de que uma operação em massa está prestes a começar.</span><span class="sxs-lookup"><span data-stu-id="e8c49-135">This method notifies the driver that a bulk operation is about to begin.</span></span> <span data-ttu-id="e8c49-136">Depois disso, o exemplo chama o método [**IPortableDeviceBulk:: Start**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-start) para começar a gravar os novos valores de nome.</span><span class="sxs-lookup"><span data-stu-id="e8c49-136">After this, the sample calls the [**IPortableDeviceBulk::Start**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-start) method to begin actually writing the new name values.</span></span>


```C++
   HRESULT                                       hr                = S_OK;
   GUID                                          guidContext       = GUID_NULL;
   CSetBulkValuesCallback*                       pCallback         = NULL;
   CComPtr<IPortableDeviceProperties>            pProperties;
   CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
   CComPtr<IPortableDeviceValues>                pObjectProperties;
   CComPtr<IPortableDeviceContent>               pContent;
   CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
   CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
   DWORD                                         cObjectIDs        = 0;
   if (SUCCEEDED(hr))
   {
       hr = pPropertiesBulk->QueueSetValuesByObjectList(pPropertiesToWrite,
                                                        pCallback,
                                                        &guidContext);


       if(SUCCEEDED(hr))
       {
           // Cleanup any previously created global event handles.
           if (g_hBulkPropertyOperationEvent != NULL)
           {
               CloseHandle(g_hBulkPropertyOperationEvent);
               g_hBulkPropertyOperationEvent = NULL;
           }

           // In order to create a simpler to follow example we create and wait infinitly
           // for the bulk property operation to complete and ignore any errors.
           // Production code should be written in a more robust manner.
           // Create the global event handle to wait on for the bulk operation
           // to complete.
           g_hBulkPropertyOperationEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
           if (g_hBulkPropertyOperationEvent != NULL)
           {
               // Call Start() to actually being the Asynchronous bulk operation.
               hr = pPropertiesBulk->Start(guidContext);
               if(FAILED(hr))
               {
                   printf("! Failed to start property operation, hr = 0x%lx\n", hr);
               }
           }
           else
           {
               printf("! Failed to create the global event handle to wait on for the bulk operation. Aborting operation.\n");
           }
       }
       else
       {
           printf("! QueueSetValuesByObjectList Failed, hr = 0x%lx\n", hr);
       }
   }
```



<span data-ttu-id="e8c49-137">Observe que o exemplo espera um período infinitamente longo de tempo para a operação ser concluída.</span><span class="sxs-lookup"><span data-stu-id="e8c49-137">Note that the sample waits an infinitely long period of time for the operation to complete.</span></span> <span data-ttu-id="e8c49-138">Se esse fosse um aplicativo de produção, o código precisaria ser modificado.</span><span class="sxs-lookup"><span data-stu-id="e8c49-138">If this were a production application, the code would need to be modified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8c49-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e8c49-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8c49-140">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="e8c49-140">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="e8c49-141">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="e8c49-141">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="e8c49-142">**Interface IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="e8c49-142">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="e8c49-143">**Interface IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="e8c49-143">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[<span data-ttu-id="e8c49-144">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="e8c49-144">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="e8c49-145">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="e8c49-145">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



