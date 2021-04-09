---
description: Para recuperar um objeto de sensor, use a interface ISensorManager. Você pode considerar essa interface como a interface raiz para a API do sensor. Para usar ISensorManager, você deve primeiro chamar o método COM CoCreateInstance.
ms.assetid: 36631bae-f237-4951-9959-6ab6286bd1f7
title: Recuperando um objeto de sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cda6ea04d1a0580c38aef5a0b9c4186b908300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920803"
---
# <a name="retrieving-a-sensor-object"></a>Recuperando um objeto de sensor

Para recuperar um objeto de sensor, use a interface [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager) . Você pode considerar essa interface como a interface raiz para a API do sensor. Para usar **ISensorManager**, você deve primeiro chamar o método com **CoCreateInstance** .

O código de exemplo a seguir cria uma instância do Gerenciador de sensor.


```C++
// Create the sensor manager.
hr = CoCreateInstance(CLSID_SensorManager, 
                        NULL, CLSCTX_INPROC_SERVER,
                        IID_PPV_ARGS(&pSensorManager));

if(hr == HRESULT_FROM_WIN32(ERROR_ACCESS_DISABLED_BY_POLICY))
{
    // Unable to retrieve sensor manager due to 
    // group policy settings. Alert the user.
}
```



Depois de recuperar com êxito um ponteiro para [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager), você pode recuperar sensores por categoria, tipo ou ID. Se você recuperar sensores por tipo ou categoria, receberá um ponteiro para uma interface [**ISensorCollection**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection) que contém todos os sensores disponíveis que pertencem à categoria ou ao tipo solicitado. Se você recuperar um sensor por sua ID, receberá um ponteiro para uma interface [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) que representa o sensor exclusivo que você solicitou.

O código de exemplo a seguir recupera uma coleção de sensores que pertencem à categoria chamada \_ data hora da categoria do sensor de exemplo \_ \_ \_ . Em seguida, o código recupera o primeiro sensor na coleção por seu índice.


```C++
// Get the sensor collection.
hr = pSensorManager->GetSensorsByCategory(SAMPLE_SENSOR_CATEGORY_DATE_TIME, &pSensorColl);
  
if(SUCCEEDED(hr))
{
    ULONG ulCount = 0;

    // Verify that the collection contains
    // at least one sensor.
    hr = pSensorColl->GetCount(&ulCount);

    if(SUCCEEDED(hr))
    {
        if(ulCount < 1)
        {
            wprintf_s(L"\nNo sensors of the requested category.\n");
            hr = E_UNEXPECTED;
        }
    }
}

if(SUCCEEDED(hr))
{
    // Get the first available sensor.
    hr = pSensorColl->GetAt(0, &pSensor);
}
```



Observe que você pode recuperar todos os sensores disponíveis usando a categoria de \_ sensor \_ todos.

De forma semelhante, você pode recuperar sensores de um tipo específico.

O código de exemplo a seguir recupera uma coleção de sensores do tipo chamado \_ tempo de tipo de sensor de exemplo \_ \_ . Em seguida, o código recupera o primeiro sensor na coleção por seu índice.


```C++
// Get the sensor collection.
hr = pSensorManager->GetSensorsByType(SAMPLE_SENSOR_TYPE_TIME, &pSensorColl);
  
if(SUCCEEDED(hr))
{
    ULONG ulCount = 0;

    // Verify that the collection contains
    // at least one sensor.
    hr = pSensorColl->GetCount(&ulCount);

    if(SUCCEEDED(hr))
    {
        if(ulCount < 1)
        {
            wprintf_s(L"\nNo sensors of the requested type.\n");
            hr = E_UNEXPECTED;
        }
    }
}

if(SUCCEEDED(hr))
{
    // Get the first available sensor.
    hr = pSensorColl->GetAt(0, &pSensor);
}
```



Para recuperar um sensor por sua ID, você deve saber a ID exclusiva do sensor. Os sensores geralmente geram essa ID quando conectado pela primeira vez para permitir que você identifique vários sensores da mesma marca e modelo. Isso significa que você provavelmente não saberá a ID do sensor com antecedência. No entanto, se você tiver armazenado uma cópia de uma ID de sensor específica que você recuperou anteriormente, por exemplo, chamando [**ISensor:: GetID**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getid), talvez você queira recuperar o mesmo sensor novamente.

O código de exemplo a seguir mostra como recuperar um sensor usando sua ID.


```C++
ISensor* pSensor = NULL;

// Get the sensor collection.
hr = pSensorManager->GetSensorByID(SAMPLE_SENSOR_TIME_ID, &pSensor);

```



Você também pode recuperar sensores quando eles estiverem disponíveis ao receber um evento do Gerenciador de sensor. Para obter mais informações, consulte [**ISensorManager:: SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ISensorManagerEvents::OnSensorEnter**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanagerevents-onsensorenter)
</dt> </dl>

 

 
