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
# <a name="retrieving-and-setting-sensor-properties"></a>Recuperando e definindo propriedades do sensor

Este tópico descreve como recuperar e definir valores para propriedades de sensor. A interface [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) fornece os métodos para definir e recuperar valores para propriedades de sensor.

## <a name="retrieving-sensor-properties"></a>Recuperando propriedades do sensor

Você pode recuperar alguns valores de propriedade de um sensor antes que o usuário o habilite. Informações como o nome do fabricante ou o modelo do sensor podem ajudá-lo a decidir se seu programa pode usar o sensor.

Você pode optar por recuperar um único valor de propriedade ou recuperar uma coleção de valores de propriedade juntos. Para recuperar um único valor, chame [**ISensor:: GetProperty**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperty). Para recuperar uma coleção de valores, chame [**ISensor:: GetProperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperties). Você pode recuperar todas as propriedades de um sensor passando **NULL** por meio do primeiro parâmetro para **ISensor:: GetProperties**.

O código de exemplo a seguir cria uma função auxiliar que imprime o valor de uma única propriedade. A função recebe um ponteiro para o sensor do qual recuperar o valor e uma chave de propriedade que contém a propriedade a ser impressa. A função pode imprimir valores para números, cadeias de caracteres e **GUID** s, mas não para outros tipos mais complexos.


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



O código de exemplo a seguir cria uma função que recupera e imprime uma coleção de propriedades. O conjunto de propriedades a serem impressas é definido pela matriz chamada Sensorproperties.


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



## <a name="setting-sensor-properties"></a>Definindo propriedades do sensor

Antes de poder definir valores de propriedade para um sensor, o usuário deve habilitar o sensor. Além disso, nem todas as propriedades do sensor podem ser definidas.

Para definir um ou mais valores para propriedades, chame [**ISensor:: SetProperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-setproperties). Você fornece esse método com um ponteiro [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) que contém a coleção de propriedades a serem definidas e seus valores associados. O método retorna uma interface [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) correspondente que pode conter códigos de erro para propriedades que não puderam ser definidas.

O código de exemplo a seguir cria uma função auxiliar que define um novo valor para a propriedade SENSOR \_ \_ atual \_ propriedade de intervalo de relatório \_ . A função usa um ponteiro para o sensor para o qual definir a propriedade e um valor **ULONG** que indica o novo intervalo de relatório a ser definido. (Observe que a definição de um valor para essa propriedade específica não garante que o sensor aceite o valor especificado. Consulte [**Propriedades do sensor**](sensor-properties.md) para obter informações sobre como essa propriedade funciona.)


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Propriedades do sensor**](sensor-properties.md)
</dt> </dl>

 

 
