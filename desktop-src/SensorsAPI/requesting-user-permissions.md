---
description: Este tópico descreve como solicitar permissões do usuário para usar sensores. Para obter informações básicas sobre permissões na API do sensor, consulte Managing User Permissions.
ms.assetid: e43ad497-86f1-4804-a67a-0aeb56b80d7f
title: Solicitando permissões de usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41e103426388d2db49bb5a8fb01d3370207ec49b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501523"
---
# <a name="requesting-user-permissions"></a>Solicitando permissões de usuário

Este tópico descreve como solicitar permissões do usuário para usar sensores. Para obter informações básicas sobre permissões na API do sensor, consulte [Managing User Permissions](managing-user-permissions.md).

Os exemplos a seguir ilustram alguns dos cenários comuns em que você pode optar por solicitar permissões de usuário.

O código de exemplo a seguir solicita apenas permissões para todos os sensores recuperados do Gerenciador de sensor, por tipo, usando uma chamada de método assíncrono. A plataforma abrirá uma caixa de diálogo para solicitar ao usuário apenas habilitar os sensores que ainda não estão habilitados. Para determinar se o usuário habilitou quaisquer sensores nesse caso, você deve manipular o evento [**ISensorEvents:: OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) .


```C++
// Get the sensor collection.
hr = pSensorManager->GetSensorsByType(SAMPLE_SENSOR_TYPE_TIME, &pSensorColl);

if(SUCCEEDED(hr))
{
    // Request permissions for all sensors
    // in the collection.
    hr = pSensorManager->RequestPermissions(0, pSensorColl, FALSE);
}

```



Você pode optar por testar o estado do sensor de forma síncrona antes de tentar recuperar os dados. O código de exemplo a seguir demonstra essa técnica.


```C++
if(SUCCEEDED(hr))
{
   // Check the current sensor state.
   SensorState state = SENSOR_STATE_NOT_AVAILABLE;

   hr = pSensor->GetState(&state);

   if(SUCCEEDED(hr))
   {
       if(state == SENSOR_STATE_ACCESS_DENIED)
       {
           wprintf_s(L"\nSensor not enabled, requesting permissions...\n");
           hr = pSensorManager->RequestPermissions(0, pSensorColl, TRUE);

           if(hr == HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED) ||
              hr == HRESULT_FROM_WIN32(ERROR_CANCELLED)) 
           {
               wprintf_s(L"\nYou have previously denied access to this sensor.\n");
               wprintf_s(L"Please use the Location and Other Sensors control panel\n");
               wprintf_s(L"to enable the WDK Time Sensor and run this program again.\n");
           }
       }
   }
}

if(SUCCEEDED(hr))
{
    // Get the data report.
    hr = pSensor->GetData(&pReport);
}
```



O código de exemplo a seguir solicita ao usuário permissões de sensor se uma tentativa de recuperar um relatório de dados de um sensor específico falhar.


```C++
if(SUCCEEDED(hr))
{
    // Get the data report.
    hr = pSensor->GetData(&pReport);

    if(E_ACCESSDENIED == hr)
    {
       wprintf_s(L"\nSensor not enabled, requesting permissions...\n");
       hr = pSensorManager->RequestPermissions(0, pSensorColl, TRUE);

       if(hr == HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED) ||
          hr == HRESULT_FROM_WIN32(ERROR_CANCELLED)) 
       {
           wprintf_s(L"\nYou have previously denied access to this sensor.\n");
           wprintf_s(L"Please use the Location and Other Sensors control panel\n");
           wprintf_s(L"to enable the WDK Time Sensor and run this program again.\n");
       }
    }
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager)
</dt> <dt>

[Gerenciando permissões de usuário](managing-user-permissions.md)
</dt> </dl>

 

 
