---
description: Recuperando propriedades de vários objetos
ms.assetid: 0d0c6b3d-23bc-4628-a684-14bb9e18967f
title: Recuperando propriedades de vários objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c069f6a28b923339f66f8423f211eff4704ef6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765096"
---
# <a name="retrieving-properties-for-multiple-objects"></a><span data-ttu-id="c06d6-103">Recuperando propriedades de vários objetos</span><span class="sxs-lookup"><span data-stu-id="c06d6-103">Retrieving Properties for Multiple Objects</span></span>

<span data-ttu-id="c06d6-104">Alguns drivers de dispositivo dão suporte à recuperação de propriedades para vários objetos em uma única chamada de função; Isso é conhecido como uma recuperação em massa.</span><span class="sxs-lookup"><span data-stu-id="c06d6-104">Some device drivers support the retrieval of properties for multiple objects in a single function call; this is referred to as a bulk retrieval.</span></span> <span data-ttu-id="c06d6-105">Há dois tipos de operações de recuperação em massa: o primeiro tipo recupera propriedades para uma lista de objetos e o segundo tipo recupera propriedades para todos os objetos de um determinado formato.</span><span class="sxs-lookup"><span data-stu-id="c06d6-105">There are two types of bulk retrieval operations: the first type retrieves properties for a list of objects, and the second type retrieves properties for all objects of a given format.</span></span> <span data-ttu-id="c06d6-106">O exemplo descrito nesta seção demonstra o primeiro.</span><span class="sxs-lookup"><span data-stu-id="c06d6-106">The example described in this section demonstrates the former.</span></span>

<span data-ttu-id="c06d6-107">Seu aplicativo pode executar uma recuperação em massa usando as interfaces descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c06d6-107">Your application can perform a bulk retrieval using the interfaces described in the following table.</span></span>



| <span data-ttu-id="c06d6-108">Interface</span><span class="sxs-lookup"><span data-stu-id="c06d6-108">Interface</span></span>                                                                                      | <span data-ttu-id="c06d6-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c06d6-109">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="c06d6-110">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="c06d6-110">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="c06d6-111">Fornece acesso aos métodos específicos de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="c06d6-111">Provides access to the content-specific methods.</span></span>                   |
| [<span data-ttu-id="c06d6-112">**Interface IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="c06d6-112">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="c06d6-113">Usado para identificar as propriedades a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="c06d6-113">Used to identify the properties to be retrieved.</span></span>                   |
| [<span data-ttu-id="c06d6-114">**Interface IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="c06d6-114">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="c06d6-115">Usado para determinar se um determinado driver dá suporte a operações em massa.</span><span class="sxs-lookup"><span data-stu-id="c06d6-115">Used to determine whether a given driver supports bulk operations.</span></span> |
| [<span data-ttu-id="c06d6-116">**Interface IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="c06d6-116">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | <span data-ttu-id="c06d6-117">Dá suporte à operação de recuperação em massa.</span><span class="sxs-lookup"><span data-stu-id="c06d6-117">Supports the bulk retrieval operation.</span></span>                             |
| [<span data-ttu-id="c06d6-118">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="c06d6-118">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="c06d6-119">Usado para armazenar os identificadores de objeto para a operação em massa.</span><span class="sxs-lookup"><span data-stu-id="c06d6-119">Used to store the object identifiers for the bulk operation.</span></span>       |



 

<span data-ttu-id="c06d6-120">A função ReadContentPropertiesBulk no módulo Contentproperties. cpp do aplicativo de exemplo demonstra uma operação de recuperação em massa.</span><span class="sxs-lookup"><span data-stu-id="c06d6-120">The ReadContentPropertiesBulk function in the sample application's ContentProperties.cpp module demonstrates a bulk retrieval operation.</span></span>

<span data-ttu-id="c06d6-121">A primeira tarefa realizada neste exemplo é determinar se o driver fornecido oferece suporte a operações em massa.</span><span class="sxs-lookup"><span data-stu-id="c06d6-121">The first task accomplished in this sample is determining whether or not the given driver supports bulk operations.</span></span> <span data-ttu-id="c06d6-122">Isso é feito chamando QueryInterface na interface IPortableDeviceProperties e verificando a existência de IPortableDevicePropertiesBulk.</span><span class="sxs-lookup"><span data-stu-id="c06d6-122">This is accomplished by calling QueryInterface on the IPortableDeviceProperties interface and checking for the existence of IPortableDevicePropertiesBulk.</span></span>


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CGetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceKeyCollection>         pPropertiesToRead;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;


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



<span data-ttu-id="c06d6-123">Se o driver oferecer suporte a operações em massa, a próxima etapa será criar uma instância da [**interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) e especificar as chaves que correspondem às propriedades que o aplicativo irá recuperar.</span><span class="sxs-lookup"><span data-stu-id="c06d6-123">If the driver supports bulk operations, the next step is to create an instance of the [**IPortableDeviceKeyCollection interface**](iportabledevicekeycollection.md) and to specify the keys that correspond to the properties that the application will retrieve.</span></span> <span data-ttu-id="c06d6-124">Para obter uma descrição desse processo, consulte o tópico [Recuperando propriedades de um único objeto](retrieving-properties-for-a-single-object.md) .</span><span class="sxs-lookup"><span data-stu-id="c06d6-124">For a description of this process, see the [Retrieving Properties for a Single Object](retrieving-properties-for-a-single-object.md) topic.</span></span>

<span data-ttu-id="c06d6-125">Depois que as chaves apropriadas forem especificadas, o aplicativo de exemplo criará uma instância da [**interface IPortableDevicePropertiesBulkCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk).</span><span class="sxs-lookup"><span data-stu-id="c06d6-125">After the appropriate keys are specified, the sample application creates an instance of the [**IPortableDevicePropertiesBulkCallback interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk).</span></span> <span data-ttu-id="c06d6-126">O aplicativo usará os métodos nesta interface para acompanhar o progresso da operação de recuperação em massa assíncrona.</span><span class="sxs-lookup"><span data-stu-id="c06d6-126">The application will use the methods in this interface to track the progress of the asynchronous bulk-retrieval operation.</span></span>


```C++
if (SUCCEEDED(hr))
{
    pCallback = new CGetBulkValuesCallback();
    if (pCallback == NULL)
    {
        hr = E_OUTOFMEMORY;
        printf("! Failed to allocate CGetBulkValuesCallback, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="c06d6-127">A próxima função que o aplicativo de exemplo chama é a função auxiliar CreateIPortableDevicePropVariantCollectionWithAllObjectIDs.</span><span class="sxs-lookup"><span data-stu-id="c06d6-127">The next function that the sample application calls is the CreateIPortableDevicePropVariantCollectionWithAllObjectIDs helper function.</span></span> <span data-ttu-id="c06d6-128">Essa função cria uma lista de todos os identificadores de objeto disponíveis para fins de exemplo.</span><span class="sxs-lookup"><span data-stu-id="c06d6-128">This function creates a list of all available object identifiers for example purposes.</span></span> <span data-ttu-id="c06d6-129">(Um aplicativo do mundo real limitaria a lista de identificadores a um determinado conjunto de objetos.</span><span class="sxs-lookup"><span data-stu-id="c06d6-129">(A real-world application would limit the list of identifiers to a particular set of objects.</span></span> <span data-ttu-id="c06d6-130">Por exemplo, um aplicativo pode criar uma lista de identificadores para todos os objetos no momento em uma determinada exibição de pasta.)</span><span class="sxs-lookup"><span data-stu-id="c06d6-130">For instance, an application may create a list of identifiers for all of the objects currently in a given folder view.)</span></span>

<span data-ttu-id="c06d6-131">Conforme observado acima, a função auxiliar enumera recursivamente todos os objetos em um determinado dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c06d6-131">As noted above, the helper function recursively enumerates all objects on a given device.</span></span> <span data-ttu-id="c06d6-132">Ele retorna essa lista em uma [**interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contém um identificador para cada objeto encontrado.</span><span class="sxs-lookup"><span data-stu-id="c06d6-132">It returns this list in an [**IPortableDevicePropVariantCollection interface**](iportabledevicepropvariantcollection.md) that contains an identifier for each object that it found.</span></span> <span data-ttu-id="c06d6-133">A função auxiliar é definida no módulo ContentEnumeration. cpp.</span><span class="sxs-lookup"><span data-stu-id="c06d6-133">The helper function is defined in the module ContentEnumeration.cpp.</span></span>


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



<span data-ttu-id="c06d6-134">Depois que as etapas anteriores forem realizadas, o aplicativo de exemplo iniciará a recuperação de propriedade assíncrona.</span><span class="sxs-lookup"><span data-stu-id="c06d6-134">Once the previous steps are accomplished, the sample application initiates the asynchronous property retrieval.</span></span> <span data-ttu-id="c06d6-135">Isso é feito fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c06d6-135">This is accomplished by doing the following:</span></span>

1.  <span data-ttu-id="c06d6-136">Chamando IPortableDevicePropertiesBulk:: QueueGetValuesByObjectList, que enfileira uma solicitação para a recuperação de propriedade em massa.</span><span class="sxs-lookup"><span data-stu-id="c06d6-136">Calling IPortableDevicePropertiesBulk::QueueGetValuesByObjectList, which queues a request for the bulk property retrieval.</span></span> <span data-ttu-id="c06d6-137">(Observe que, embora a solicitação seja enfileirada, ela não é iniciada.)</span><span class="sxs-lookup"><span data-stu-id="c06d6-137">(Note that although the request is queued, it is not started.)</span></span>
2.  <span data-ttu-id="c06d6-138">Chamando IPortableDevicePropertiesBulk:: Start para iniciar a solicitação em fila.</span><span class="sxs-lookup"><span data-stu-id="c06d6-138">Calling IPortableDevicePropertiesBulk::Start to initiate the queued request.</span></span>

<span data-ttu-id="c06d6-139">Essas etapas são demonstradas no trecho de código a seguir do aplicativo de exemplo.</span><span class="sxs-lookup"><span data-stu-id="c06d6-139">These steps are demonstrated in the following code excerpt from the sample application.</span></span>


```C++
   if (SUCCEEDED(hr))
   {
       hr = pPropertiesBulk->QueueGetValuesByObjectList(pObjectIDs,
                                                        pPropertiesToRead,
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
           printf("! QueueGetValuesByObjectList Failed, hr = 0x%lx\n", hr);
       }
   }
```



## <a name="related-topics"></a><span data-ttu-id="c06d6-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c06d6-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c06d6-141">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="c06d6-141">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="c06d6-142">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="c06d6-142">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="c06d6-143">**Interface IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="c06d6-143">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="c06d6-144">**Interface IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="c06d6-144">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="c06d6-145">**Interface IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="c06d6-145">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[<span data-ttu-id="c06d6-146">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="c06d6-146">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="c06d6-147">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="c06d6-147">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



