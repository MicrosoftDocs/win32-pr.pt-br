---
description: Este tópico descreve como recuperar e definir valores para propriedades de sensor. A interface ISensor fornece os métodos para definir e recuperar valores para propriedades de sensor.
ms.assetid: 7d10e5b4-bae7-4564-84eb-75c6a2eeef8f
title: Recuperando e definindo propriedades do sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f64bf0e253f47ae2d8cd1f4945f3b87aa3406b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811281"
---
# <a name="retrieving-and-setting-sensor-properties"></a><span data-ttu-id="aa560-104">Recuperando e definindo propriedades do sensor</span><span class="sxs-lookup"><span data-stu-id="aa560-104">Retrieving and Setting Sensor Properties</span></span>

<span data-ttu-id="aa560-105">Este tópico descreve como recuperar e definir valores para propriedades de sensor.</span><span class="sxs-lookup"><span data-stu-id="aa560-105">This topic describes how to retrieve and set values for sensor properties.</span></span> <span data-ttu-id="aa560-106">A interface [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) fornece os métodos para definir e recuperar valores para propriedades de sensor.</span><span class="sxs-lookup"><span data-stu-id="aa560-106">The [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) interface provides the methods to set and retrieve values for sensor properties.</span></span>

## <a name="retrieving-sensor-properties"></a><span data-ttu-id="aa560-107">Recuperando propriedades do sensor</span><span class="sxs-lookup"><span data-stu-id="aa560-107">Retrieving Sensor Properties</span></span>

<span data-ttu-id="aa560-108">Você pode recuperar alguns valores de propriedade de um sensor antes que o usuário o habilite.</span><span class="sxs-lookup"><span data-stu-id="aa560-108">You can retrieve some property values from a sensor before the user has enabled it.</span></span> <span data-ttu-id="aa560-109">Informações como o nome do fabricante ou o modelo do sensor podem ajudá-lo a decidir se seu programa pode usar o sensor.</span><span class="sxs-lookup"><span data-stu-id="aa560-109">Information such as the manufacturer's name or the model of the sensor can help you to decide whether your program can use the sensor.</span></span>

<span data-ttu-id="aa560-110">Você pode optar por recuperar um único valor de propriedade ou recuperar uma coleção de valores de propriedade juntos.</span><span class="sxs-lookup"><span data-stu-id="aa560-110">You can choose to retrieve a single property value, or to retrieve a collection of property values together.</span></span> <span data-ttu-id="aa560-111">Para recuperar um único valor, chame [**ISensor:: GetProperty**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperty).</span><span class="sxs-lookup"><span data-stu-id="aa560-111">To retrieve single value, call [**ISensor::GetProperty**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperty).</span></span> <span data-ttu-id="aa560-112">Para recuperar uma coleção de valores, chame [**ISensor:: GetProperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperties).</span><span class="sxs-lookup"><span data-stu-id="aa560-112">To retrieve a collection of values, call [**ISensor::GetProperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperties).</span></span> <span data-ttu-id="aa560-113">Você pode recuperar todas as propriedades de um sensor passando **NULL** por meio do primeiro parâmetro para **ISensor:: GetProperties**.</span><span class="sxs-lookup"><span data-stu-id="aa560-113">You can retrieve all properties for a sensor by passing **NULL** through the first parameter to **ISensor::GetProperties**.</span></span>

<span data-ttu-id="aa560-114">O código de exemplo a seguir cria uma função auxiliar que imprime o valor de uma única propriedade.</span><span class="sxs-lookup"><span data-stu-id="aa560-114">The following example code creates a helper function that prints the value of a single property.</span></span> <span data-ttu-id="aa560-115">A função recebe um ponteiro para o sensor do qual recuperar o valor e uma chave de propriedade que contém a propriedade a ser impressa.</span><span class="sxs-lookup"><span data-stu-id="aa560-115">The function receives a pointer to the sensor from which to retrieve the value and a property key that contains the property to print.</span></span> <span data-ttu-id="aa560-116">A função pode imprimir valores para números, cadeias de caracteres e **GUID** s, mas não para outros tipos mais complexos.</span><span class="sxs-lookup"><span data-stu-id="aa560-116">The function can print values for numbers, strings, and **GUID** s, but not other, more complex types.</span></span>


```C++
HRESULT PrintSensorProperty(ISensor* pSensor, REFPROPERTYKEY pk)
{
    assert(pSensor);

    HRESULT hr = S_OK;

    PROPVARIANT pv = {};

    hr = pSensor->GetProperty(pk, &pv);

    if(SUCCEEDED(hr))
    {
        if(pv.vt == VT_UI4)  // Number
        {
            wprintf_s(L"\nSensor integer value: %u\n", pv.ulVal);
        }
        else if(pv.vt == VT_LPWSTR)  // String
        {
            wprintf_s(L"\nSensor string value: %s\n", pv.pwszVal);
        }
        else if(pv.vt == VT_CLSID)  // GUID
        {
            int iRet = 0;

            // Convert the GUID to a string.
            OLECHAR wszGuid[39] = {}; // Buffer for string.
            iRet = ::StringFromGUID2(*(pv.puuid), wszGuid, 39);

            assert(39 == iRet); // Count of characters returned for GUID.

            wprintf_s(L"\nSensor GUID value: %s\n", wszGuid);
        }
        else  // Interface or vector
        {
            wprintf_s(L"\nSensor property is a compound type. Unable to print value.");
        }
    }

    PropVariantClear(&pv);

    return hr;    
}
```



<span data-ttu-id="aa560-117">O código de exemplo a seguir cria uma função que recupera e imprime uma coleção de propriedades.</span><span class="sxs-lookup"><span data-stu-id="aa560-117">The following example code creates a function that retrieves and prints a collection of properties.</span></span> <span data-ttu-id="aa560-118">O conjunto de propriedades a serem impressas é definido pela matriz chamada Sensorproperties.</span><span class="sxs-lookup"><span data-stu-id="aa560-118">The set of properties to print is defined by the array named SensorProperties.</span></span>


```C++
HRESULT PrintSensorProperties(ISensor* pSensor)
{
    assert(pSensor);

    HRESULT hr = S_OK;

    DWORD cVals = 0; // Count of returned properties.
    IPortableDeviceKeyCollection* pKeys = NULL; // Input
    IPortableDeviceValues* pValues = NULL;  // Output

    // Properties to print.
    const PROPERTYKEY SensorProperties[] =
    {
        SENSOR_PROPERTY_MANUFACTURER,
        SENSOR_PROPERTY_SERIAL_NUMBER,
        SENSOR_PROPERTY_DESCRIPTION,
        SENSOR_PROPERTY_FRIENDLY_NAME
    };

    // CoCreate a key collection to store property keys.
    hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection, 
                                NULL, 
                                CLSCTX_INPROC_SERVER,                                 
                                IID_PPV_ARGS(&pKeys));

    if(SUCCEEDED(hr))
    {
        // Add the properties to the key collection.
        for (DWORD dwIndex = 0; dwIndex < ARRAYSIZE(SensorProperties); dwIndex++)
        {
            hr = pKeys->Add(SensorProperties[dwIndex]);

            if(FAILED(hr))
            {
                // Unexpected.
                // This example returns the failed HRESULT.
                // You may choose to ignore failures, here.
                break;
            }
        }
    }

    if(SUCCEEDED(hr))
    {
        // Retrieve the properties from the sensor.
        hr = pSensor->GetProperties(pKeys, &pValues);
    }

    if(SUCCEEDED(hr))
    {
        // Get the number of values returned.        
        hr = pValues->GetCount(&cVals);
    }

    if(SUCCEEDED(hr))
    {
        PROPERTYKEY pk; // Keys
        PROPVARIANT pv = {}; // Values

        // Loop through the values;
        for (DWORD i = 0; i < cVals; i++)
        {
            // Get the value at the current index.
            hr = pValues->GetAt(i, &pk, &pv);

            if(SUCCEEDED(hr))
            { 
                // Find and print the property.
                if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_MANUFACTURER))
                {
                    wprintf_s(L"\nManufacturer: %s\n", pv.pwszVal);
                }
                else if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_SERIAL_NUMBER))
                {
                    wprintf_s(L"Serial number: %s\n", pv.pwszVal);
                }
                else if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_FRIENDLY_NAME))
                {
                    wprintf_s(L"Friendly name: %s\n", pv.pwszVal);
                }
                else if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_DESCRIPTION))
                {
                    wprintf_s(L"Description: %s\n", pv.pwszVal);
                }
            }

            PropVariantClear(&pv);
        } // end i loop        
    }

    SafeRelease(&pKeys);
    SafeRelease(&pValues);

    return hr;
};
```



## <a name="setting-sensor-properties"></a><span data-ttu-id="aa560-119">Definindo propriedades do sensor</span><span class="sxs-lookup"><span data-stu-id="aa560-119">Setting Sensor Properties</span></span>

<span data-ttu-id="aa560-120">Antes de poder definir valores de propriedade para um sensor, o usuário deve habilitar o sensor.</span><span class="sxs-lookup"><span data-stu-id="aa560-120">Before you can set property values for a sensor, the user must enable the sensor.</span></span> <span data-ttu-id="aa560-121">Além disso, nem todas as propriedades do sensor podem ser definidas.</span><span class="sxs-lookup"><span data-stu-id="aa560-121">Also, not all sensor properties can be set.</span></span>

<span data-ttu-id="aa560-122">Para definir um ou mais valores para propriedades, chame [**ISensor:: SetProperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-setproperties).</span><span class="sxs-lookup"><span data-stu-id="aa560-122">To set one or more values for properties, call [**ISensor::SetProperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-setproperties).</span></span> <span data-ttu-id="aa560-123">Você fornece esse método com um ponteiro [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) que contém a coleção de propriedades a serem definidas e seus valores associados.</span><span class="sxs-lookup"><span data-stu-id="aa560-123">You provide this method with an [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) pointer that contains the collection of properties to set, and their associated values.</span></span> <span data-ttu-id="aa560-124">O método retorna uma interface [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) correspondente que pode conter códigos de erro para propriedades que não puderam ser definidas.</span><span class="sxs-lookup"><span data-stu-id="aa560-124">The method returns a corresponding [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) interface that may contain error codes for properties that could not be set.</span></span>

<span data-ttu-id="aa560-125">O código de exemplo a seguir cria uma função auxiliar que define um novo valor para a propriedade SENSOR \_ \_ atual \_ propriedade de intervalo de relatório \_ .</span><span class="sxs-lookup"><span data-stu-id="aa560-125">The following example code creates a helper function that sets a new value for the SENSOR\_PROPERTY\_CURRENT\_REPORT\_INTERVAL property.</span></span> <span data-ttu-id="aa560-126">A função usa um ponteiro para o sensor para o qual definir a propriedade e um valor **ULONG** que indica o novo intervalo de relatório a ser definido.</span><span class="sxs-lookup"><span data-stu-id="aa560-126">The function takes a pointer to the sensor for which to set the property, and a **ULONG** value that indicates the new report interval to be set.</span></span> <span data-ttu-id="aa560-127">(Observe que a definição de um valor para essa propriedade específica não garante que o sensor aceite o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="aa560-127">(Note that setting a value for this particular property does not guarantee that the sensor will accept the specified value.</span></span> <span data-ttu-id="aa560-128">Consulte [**Propriedades do sensor**](sensor-properties.md) para obter informações sobre como essa propriedade funciona.)</span><span class="sxs-lookup"><span data-stu-id="aa560-128">See [**Sensor Properties**](sensor-properties.md) for information about how this property works.)</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="aa560-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa560-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa560-130">**Propriedades do sensor**</span><span class="sxs-lookup"><span data-stu-id="aa560-130">**Sensor Properties**</span></span>](sensor-properties.md)
</dt> </dl>

 

 
