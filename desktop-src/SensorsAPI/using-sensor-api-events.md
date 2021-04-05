---
description: A API do sensor fornece notificações de eventos por meio de interfaces de retorno de chamada.
ms.assetid: 0c396d54-cb2e-4b07-999f-3f4001db2a02
title: Usando eventos de API do sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a54fcb14138c1b20470a2b716e5cce86235c3102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922099"
---
# <a name="using-sensor-api-events"></a><span data-ttu-id="e030a-103">Usando eventos de API do sensor</span><span class="sxs-lookup"><span data-stu-id="e030a-103">Using Sensor API Events</span></span>

<span data-ttu-id="e030a-104">A API do sensor fornece notificações de eventos por meio de interfaces de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e030a-104">The Sensor API provides event notifications through callback interfaces.</span></span>

<span data-ttu-id="e030a-105">Para receber o evento notificações, o programa deve implementar as interfaces de retorno de chamada COM necessárias.</span><span class="sxs-lookup"><span data-stu-id="e030a-105">To receive event notfications, your program must implement the required COM callback interfaces.</span></span> <span data-ttu-id="e030a-106">Para receber eventos de sensores, você deve implementar [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span><span class="sxs-lookup"><span data-stu-id="e030a-106">To receive events from sensors, you must implement [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span></span> <span data-ttu-id="e030a-107">Para receber eventos do Gerenciador de sensor, você deve implementar [**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents).</span><span class="sxs-lookup"><span data-stu-id="e030a-107">To receive events from the sensor manager, you must implement [**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents).</span></span>

<span data-ttu-id="e030a-108">O código de exemplo a seguir cria uma classe que implementa [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span><span class="sxs-lookup"><span data-stu-id="e030a-108">The following example code creates a class that implements [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span></span>


```C++
class CMyEvents : public ISensorEvents
{
public:

    STDMETHODIMP QueryInterface(REFIID iid, void** ppv)
    {
        if (ppv == NULL)
        {
            return E_POINTER;
        }
        if (iid == __uuidof(IUnknown))
        {
            *ppv = static_cast<IUnknown*>(this);
        }
        else if (iid == __uuidof(ISensorEvents))
        {
            *ppv = static_cast<ISensorEvents*>(this);
        }
        else
        {
            *ppv = NULL;
            return E_NOINTERFACE;
        }
        AddRef();
        return S_OK;
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef); 
    }

    STDMETHODIMP_(ULONG) Release()
    {
        ULONG count = InterlockedDecrement(&m_cRef);
        if (count == 0)
        {
            delete this;
            return 0;
        }
        return count;
    }

    //
    // ISensorEvents methods.
    //

    STDMETHODIMP OnEvent(
            ISensor *pSensor,
            REFGUID eventID,
            IPortableDeviceValues *pEventData)
    {
        HRESULT hr = S_OK;

        // Handle custom events here.

        return hr;
    }

    STDMETHODIMP OnDataUpdated(
            ISensor *pSensor,
            ISensorDataReport *pNewData)
    {
        HRESULT hr = S_OK;

        if(NULL == pNewData ||
           NULL == pSensor)
        {
            return E_INVALIDARG;
        }

        ULONG ulHour = 0;
        ULONG ulMinute = 0;
        ULONG ulSecond = 0;

        PROPVARIANT var = {};

        hr = pNewData->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_HOUR, &var);

        if(SUCCEEDED(hr))
        {
            if(var.vt == VT_UI4)
            {
                // Get the hour value.
                ulHour = var.ulVal;                
            }
        }

        PropVariantClear(&var);

        if(SUCCEEDED(hr))
        {
            hr = pNewData->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_MINUTE, &var);
        }

        if(SUCCEEDED(hr))
        {
            if(var.vt == VT_UI4)
            {
                // Get the hour value.
                ulMinute = var.ulVal;
            }
        }

        PropVariantClear(&var);

        if(SUCCEEDED(hr))
        {
            hr = pNewData->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_SECOND, &var);
        }

        if(SUCCEEDED(hr))
        {
            if(var.vt == VT_UI4)
            {
                // Get the hour value.
                ulSecond = var.ulVal;
            }
        }

        PropVariantClear(&var);

        if(SUCCEEDED(hr))
        {
            // Print
            wprintf_s(L"Current local time is: \n");
            wprintf_s(L"%02d:%02d:%02d (asynchronous)\n", ulHour, ulMinute, ulSecond);
        }

        return hr;
    }

    STDMETHODIMP OnLeave(
            REFSENSOR_ID sensorID)
    {
        HRESULT hr = S_OK;

        // Peform any housekeeping tasks for the sensor that is leaving.
        // For example, if you have maintained a reference to the sensor,
        // release it now and set the pointer to NULL.

        return hr;
    }

    STDMETHODIMP OnStateChanged(
            ISensor* pSensor,
            SensorState state)
    {
        HRESULT hr = S_OK;

        if(NULL == pSensor)
        {
            return E_INVALIDARG;
        }


        if(state == SENSOR_STATE_READY)
        {
            wprintf_s(L"\nTime sensor is now ready.");
        }
        else if(state == SENSOR_STATE_ACCESS_DENIED)
        {
            wprintf_s(L"\nNo permission for the time sensor.\n");
            wprintf_s(L"Enable the sensor in the control panel.\n");
        }
  

        return hr;
    }

    private:
        long m_cRef;

};

```



<span data-ttu-id="e030a-109">Depois de implementar a interface de retorno de chamada, você pode fornecer um sensor específico com um ponteiro para uma instância de sua classe de retorno de chamada para começar a receber notificações de eventos do sensor.</span><span class="sxs-lookup"><span data-stu-id="e030a-109">After implementing the callback interface, you can provide a particular sensor with a pointer to an instance of your callback class to start receiving event notifications from the sensor.</span></span>

<span data-ttu-id="e030a-110">O código de exemplo a seguir cria uma instância da classe de retorno de chamada e, em seguida, solicita o evento notificações de um sensor.</span><span class="sxs-lookup"><span data-stu-id="e030a-110">The following example code creates an instance of the callback class, and then requests event notifcations from a sensor.</span></span>


```C++
CMyEvents* pEventClass = NULL;
ISensorEvents* pMyEvents = NULL;

if(SUCCEEDED(hr))
{
    // Create an instance of the event class.
    pEventClass = new(std::nothrow) CMyEvents();        
}

if(SUCCEEDED(hr))
{
    // Retrieve the pointer to the callback interface.
    hr = pEventClass->QueryInterface(IID_PPV_ARGS(&pMyEvents));
}

if(SUCCEEDED(hr))
{
    // Start receiving events.
    hr = pSensor->SetEventSink(pMyEvents);
} 

```



<span data-ttu-id="e030a-111">Você pode escrever código semelhante para receber eventos do Gerenciador de sensor.</span><span class="sxs-lookup"><span data-stu-id="e030a-111">You can write similar code to receive events from the sensor manager.</span></span>

<span data-ttu-id="e030a-112">O código de exemplo a seguir mostra como parar de receber notificações de eventos.</span><span class="sxs-lookup"><span data-stu-id="e030a-112">The following example code shows how to stop receiving event notifications.</span></span>


```C++
if(SUCCEEDED(hr))
{
    hr = pSensor->SetEventSink(NULL);
}
```



## <a name="requesting-a-report-interval"></a><span data-ttu-id="e030a-113">Solicitando um intervalo de relatório</span><span class="sxs-lookup"><span data-stu-id="e030a-113">Requesting a Report Interval</span></span>

<span data-ttu-id="e030a-114">Você pode sugerir um valor para a frequência com que seu aplicativo recebe eventos de atualização de dados.</span><span class="sxs-lookup"><span data-stu-id="e030a-114">You can suggest a value for how frequently your applicaton receives data-updated events.</span></span> <span data-ttu-id="e030a-115">No entanto, os sensores não são necessários para fornecer eventos em qualquer intervalo específico.</span><span class="sxs-lookup"><span data-stu-id="e030a-115">However, sensors are not required to provide events at any particular interval.</span></span> <span data-ttu-id="e030a-116">Você deve estar ciente de que seu valor sugerido pode não corresponder ao intervalo de relatório real que o sensor usa para gerar eventos.</span><span class="sxs-lookup"><span data-stu-id="e030a-116">You should be aware that your suggested value might not match the actual report interval the sensor uses to raise events.</span></span> <span data-ttu-id="e030a-117">Para saber o intervalo real do relatório, recupere o valor da propriedade \_ sensor \_ atual do intervalo de \_ relatório \_ , conforme descrito em [recuperando e definindo propriedades do sensor](setting-and-retrieving-sensor-properties.md).</span><span class="sxs-lookup"><span data-stu-id="e030a-117">To know the actual report interval, retrieve the value for the SENSOR\_PROPERTY\_CURRENT\_REPORT\_INTERVAL property, as described in [Retrieving and Setting Sensor Properties](setting-and-retrieving-sensor-properties.md).</span></span>

<span data-ttu-id="e030a-118">O código de exemplo a seguir cria uma função auxiliar que solicita um novo valor para a propriedade SENSOR \_ \_ atual \_ propriedade de intervalo de relatório \_ .</span><span class="sxs-lookup"><span data-stu-id="e030a-118">The following example code creates a helper function that requests a new value for the SENSOR\_PROPERTY\_CURRENT\_REPORT\_INTERVAL property.</span></span> <span data-ttu-id="e030a-119">A função usa um ponteiro para o sensor para o qual definir a propriedade e um valor **ULONG** que indica o novo intervalo de relatório a ser definido.</span><span class="sxs-lookup"><span data-stu-id="e030a-119">The function takes a pointer to the sensor for which to set the property, and a **ULONG** value that indicates the new report interval to be set.</span></span>


```C++
HRESULT SetCurrentReportInterval(ISensor* pSensor, ULONG ulNewInterval)
{
    assert(pSensor);

    HRESULT hr = S_OK;

    IPortableDeviceValues* pPropsToSet = NULL; // Input
    IPortableDeviceValues* pPropsReturn = NULL; // Output

    // Create the input object.
    hr = CoCreateInstance(__uuidof(PortableDeviceValues),
                            NULL,
                            CLSCTX_INPROC_SERVER,                           
                            IID_PPV_ARGS(&pPropsToSet));

    if(SUCCEEDED(hr))
    {
        // Add the current report interval property.
        hr = pPropsToSet->SetUnsignedIntegerValue(SENSOR_PROPERTY_CURRENT_REPORT_INTERVAL, ulNewInterval);
    }

    if(SUCCEEDED(hr))
    {
        // Only setting a single property, here.
        hr = pSensor->SetProperties(pPropsToSet, &pPropsReturn);
    }

    // Test for failure.
    if(hr == S_FALSE)
    {
        HRESULT hrError = S_OK;
      
        // Check results for failure.
        hr = pPropsReturn->GetErrorValue(SENSOR_PROPERTY_CURRENT_REPORT_INTERVAL, &hrError);

        if(SUCCEEDED(hr))
        {
            // Print an error message.
            wprintf_s(L"\nSetting current report interval failed with error 0x%X\n", hrError);

            // Return the error code.
            hr = hrError;
        }
    }
    else if(hr == E_ACCESSDENIED)
    {
        // No permission. Take appropriate action.
    }

    SafeRelease(&pPropsToSet);
    SafeRelease(&pPropsReturn);
   
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="e030a-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e030a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e030a-121">Sobre eventos de API do sensor</span><span class="sxs-lookup"><span data-stu-id="e030a-121">About Sensor API Events</span></span>](about-sensor-events.md)
</dt> </dl>

 

 



