---
description: Recuperando os eventos com suporte de um dispositivo
ms.assetid: 951b300f-03de-4a3d-9356-e3a7b5b17fdb
title: Recuperando os eventos com suporte de um dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a542a34d0938c7e2ff86118818714f18b1224f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506260"
---
# <a name="retrieving-the-events-supported-by-a-device"></a><span data-ttu-id="2033e-103">Recuperando os eventos com suporte de um dispositivo</span><span class="sxs-lookup"><span data-stu-id="2033e-103">Retrieving the Events Supported by a Device</span></span>

<span data-ttu-id="2033e-104">Alguns drivers WPD dão suporte à notificação de eventos.</span><span class="sxs-lookup"><span data-stu-id="2033e-104">Some WPD drivers support event notification.</span></span> <span data-ttu-id="2033e-105">Isso significa que um aplicativo pode se registrar no driver para receber uma notificação quando ocorrer uma ação específica.</span><span class="sxs-lookup"><span data-stu-id="2033e-105">This means that an application can register with the driver to receive a notification when a specific action occurs.</span></span> <span data-ttu-id="2033e-106">Por exemplo, um aplicativo pode se registrar para receber uma notificação quando um objeto é adicionado ou removido.</span><span class="sxs-lookup"><span data-stu-id="2033e-106">For example, an application can register to receive a notification when an object is added or removed.</span></span>

<span data-ttu-id="2033e-107">Há dez eventos predefinidos que um aplicativo pode monitorar.</span><span class="sxs-lookup"><span data-stu-id="2033e-107">There are ten predefined events that an application can monitor.</span></span> <span data-ttu-id="2033e-108">Eles são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2033e-108">They are described in the following table.</span></span>



| <span data-ttu-id="2033e-109">Evento</span><span class="sxs-lookup"><span data-stu-id="2033e-109">Event</span></span>                       | <span data-ttu-id="2033e-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="2033e-110">Description</span></span>                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2033e-111">Recursos do dispositivo atualizados</span><span class="sxs-lookup"><span data-stu-id="2033e-111">Device capabilities updated</span></span> | <span data-ttu-id="2033e-112">Ocorre quando os recursos do dispositivo foram alterados.</span><span class="sxs-lookup"><span data-stu-id="2033e-112">Occurs when the device capabilities have changed.</span></span>                                                                                      |
| <span data-ttu-id="2033e-113">Dispositivo removido</span><span class="sxs-lookup"><span data-stu-id="2033e-113">Device removed</span></span>              | <span data-ttu-id="2033e-114">Ocorre quando o dispositivo está desconectado.</span><span class="sxs-lookup"><span data-stu-id="2033e-114">Occurs when the device is unplugged.</span></span>                                                                                                   |
| <span data-ttu-id="2033e-115">Redefinição do dispositivo</span><span class="sxs-lookup"><span data-stu-id="2033e-115">Device reset</span></span>                | <span data-ttu-id="2033e-116">Ocorre quando o dispositivo é redefinido.</span><span class="sxs-lookup"><span data-stu-id="2033e-116">Occurs when the device has been reset.</span></span>                                                                                                 |
| <span data-ttu-id="2033e-117">Objeto adicionado</span><span class="sxs-lookup"><span data-stu-id="2033e-117">Object added</span></span>                | <span data-ttu-id="2033e-118">Ocorre depois que um novo objeto é disponibilizado no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2033e-118">Occurs after a new object becomes available on the device.</span></span>                                                                             |
| <span data-ttu-id="2033e-119">Objeto removido</span><span class="sxs-lookup"><span data-stu-id="2033e-119">Object removed</span></span>              | <span data-ttu-id="2033e-120">Ocorre depois que um objeto é removido do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2033e-120">Occurs after an object has been removed from the device.</span></span>                                                                               |
| <span data-ttu-id="2033e-121">Transferência de objeto solicitada</span><span class="sxs-lookup"><span data-stu-id="2033e-121">Object transfer requested</span></span>   | <span data-ttu-id="2033e-122">Indica que uma solicitação foi feita para transferir um objeto.</span><span class="sxs-lookup"><span data-stu-id="2033e-122">Indicates that a request has been made to transfer an object.</span></span>                                                                          |
| <span data-ttu-id="2033e-123">Objeto atualizado</span><span class="sxs-lookup"><span data-stu-id="2033e-123">Object updated</span></span>              | <span data-ttu-id="2033e-124">Ocorre após a atualização de um objeto ou de seus filhos.</span><span class="sxs-lookup"><span data-stu-id="2033e-124">Occurs after either an object or its children has been updated.</span></span> <span data-ttu-id="2033e-125">(Os clientes conectados devem atualizar sua exibição do objeto fornecido.)</span><span class="sxs-lookup"><span data-stu-id="2033e-125">(Connected clients should then update their view of the given object.)</span></span> |
| <span data-ttu-id="2033e-126">Formato de armazenamento em andamento</span><span class="sxs-lookup"><span data-stu-id="2033e-126">Storage format in progress</span></span>  | <span data-ttu-id="2033e-127">Ocorre quando o armazenamento do dispositivo está sendo formatado.</span><span class="sxs-lookup"><span data-stu-id="2033e-127">Occurs when the device storage is being formatted.</span></span>                                                                                     |



 

<span data-ttu-id="2033e-128">Para obter uma lista das constantes associadas a esses eventos, consulte o tópico [constantes do evento](event-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="2033e-128">For a list of the constants associated with these events, see the [Event Constants](event-constants.md) topic.</span></span>

<span data-ttu-id="2033e-129">A função ListSupportedEvents no módulo DeviceCapabilities. cpp demonstra a recuperação de eventos com suporte em um determinado dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2033e-129">The ListSupportedEvents function in the DeviceCapabilities.cpp module demonstrates the retrieval of events supported by a given device.</span></span>

<span data-ttu-id="2033e-130">Seu aplicativo pode recuperar os identificadores para eventos com suporte de um dispositivo usando as interfaces descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2033e-130">Your application can retrieve the identifiers for events supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="2033e-131">Interface</span><span class="sxs-lookup"><span data-stu-id="2033e-131">Interface</span></span>                                                                                      | <span data-ttu-id="2033e-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="2033e-132">Description</span></span>                                               |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="2033e-133">**Interface IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2033e-133">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="2033e-134">Fornece acesso aos métodos de recuperação de evento com suporte.</span><span class="sxs-lookup"><span data-stu-id="2033e-134">Provides access to the supported-event retrieval methods.</span></span> |
| [<span data-ttu-id="2033e-135">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="2033e-135">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="2033e-136">Usado para enumerar e armazenar dados de categoria funcional.</span><span class="sxs-lookup"><span data-stu-id="2033e-136">Used to enumerate and store functional-category data.</span></span>     |



 

<span data-ttu-id="2033e-137">A primeira tarefa realizada pelo aplicativo de exemplo é a recuperação de um objeto [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) , que é usado para recuperar os eventos com suporte pelo dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="2033e-137">The first task accomplished by the sample application is the retrieval of an [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) object, which is used to retrieve the events supported by the given device.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pEvents;
DWORD dwNumEvents = 0;

if (pDevice == NULL)
{
    printf("! A NULL IPortableDevice interface pointer was received\n");
    return;
}


// Get an IPortableDeviceCapabilities interface from the IPortableDevice interface to
// access the device capabilities-specific methods.
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}
```



<span data-ttu-id="2033e-138">Os eventos com suporte são recuperados chamando o método [**IPortableDeviceCapabilities:: GetSupportedEvents**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedevents) .</span><span class="sxs-lookup"><span data-stu-id="2033e-138">The supported events are retrieved by calling the [**IPortableDeviceCapabilities::GetSupportedEvents**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedevents) method.</span></span> <span data-ttu-id="2033e-139">Esse método recupera uma coleção de identificadores de eventos para o dispositivo fornecido e os armazena em um objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) apontado pelo argumento pEvents.</span><span class="sxs-lookup"><span data-stu-id="2033e-139">This method retrieves a collection of event identifiers for the given device and stores them in an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object pointed to by the pEvents argument.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetSupportedEvents(&pEvents);
    if (FAILED(hr))
    {
        printf("! Failed to get supported events from the device, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="2033e-140">A próxima etapa é recuperar a contagem de eventos com suporte para que o aplicativo possa iterar por meio do objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) e recuperar o identificador de cada um.</span><span class="sxs-lookup"><span data-stu-id="2033e-140">The next step is to retrieve the count of supported events so that the application can iterate through the [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object and retrieve the identifier for each.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pEvents->GetCount(&dwNumEvents);
    if (FAILED(hr))
    {
        printf("! Failed to get number of supported events, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Supported Events Found on the device\n\n", dwNumEvents);

// Loop through each event and display its name
if (SUCCEEDED(hr))
{
    for (DWORD dwIndex = 0; dwIndex < dwNumEvents; dwIndex++)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);
        hr = pEvents->GetAt(dwIndex, &pv);
        if (SUCCEEDED(hr))
        {
            // We have an event.  It is assumed that
            // events are returned as VT_CLSID VarTypes.

            if (pv.puuid != NULL)
            {
                // Display the event name
                DisplayEvent(*pv.puuid);
                printf("\n");
                // Display the event options
                DisplayEventOptions(pCapabilities, *pv.puuid);
                printf("\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="2033e-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2033e-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2033e-142">**Constantes de evento**</span><span class="sxs-lookup"><span data-stu-id="2033e-142">**Event Constants**</span></span>](event-constants.md)
</dt> <dt>

[<span data-ttu-id="2033e-143">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="2033e-143">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="2033e-144">**Interface IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2033e-144">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="2033e-145">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="2033e-145">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="2033e-146">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="2033e-146">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



