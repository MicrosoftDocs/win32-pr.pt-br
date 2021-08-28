---
description: Este tópico descreve como recuperar dados de um sensor, de forma síncrona e assíncrona.
ms.assetid: 4ae80816-5e53-4ed1-9300-4b38c22d65e2
title: Recuperando valores de dados do sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e240b9bc14d917db0e0c4280ad957aa139369eb7762abfcd69441d25e66857d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960026"
---
# <a name="retrieving-sensor-data-values"></a>Recuperando valores de dados do sensor

Este tópico descreve como recuperar dados de um sensor, de forma síncrona e assíncrona.

## <a name="retrieving-data-synchronously"></a>Recuperando dados de forma síncrona

Você pode recuperar dados do sensor de forma síncrona chamando [**ISensor::GetData.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getdata)

O código de exemplo a seguir recupera um relatório de dados do sensor e recupera três valores de campo de dados individuais. O sensor de exemplo fornece dados personalizados sobre a hora local atual em campos de dados de hora, minuto e segundo. A variável chamada pSensor contém um ponteiro para [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) que representa o sensor que fornece os dados.


```C++
if(SUCCEEDED(hr))
{
    // Get the data report.
    hr = pSensor->GetData(&pReport);
}
  
if(SUCCEEDED(hr))
{
    PROPVARIANT var = {};

    hr = pReport->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_HOUR, &var);

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulHour = var.ulVal;                
        }
    }

    PropVariantClear(&var);

    hr = pReport->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_MINUTE, &var);

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulMinute = var.ulVal;
        }
    }

    PropVariantClear(&var);

    hr = pReport->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_SECOND, &var);

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
        // Print the local time to the console window.
        wprintf_s(L"\nCurrent local time is: \n");
        wprintf_s(L"%02d:%02d:%02d (synchronous)\n\n", ulHour, ulMinute, ulSecond);
    }

```



## <a name="retrieving-data-asynchronously"></a>Recuperando dados de forma assíncrona

Você pode receber dados do sensor de forma assíncrona registrando-se para receber o evento [**ISensorEvents::OnDataUpdated.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) Para entender como receber retornos de chamada de evento de sensor, consulte [Usando eventos de API do sensor](using-sensor-api-events.md).

O código de exemplo a seguir mostra uma implementação de [**ISensorEvents::OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) que recupera valores de dados do relatório de dados fornecido pelo evento. O sensor de exemplo fornece dados personalizados sobre a hora local atual em campos de dados de hora, minuto e segundo.


```C++
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
```



 

 
