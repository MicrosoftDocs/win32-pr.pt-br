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
# <a name="requesting-user-permissions"></a><span data-ttu-id="fa70e-104">Solicitando permissões de usuário</span><span class="sxs-lookup"><span data-stu-id="fa70e-104">Requesting User Permissions</span></span>

<span data-ttu-id="fa70e-105">Este tópico descreve como solicitar permissões do usuário para usar sensores.</span><span class="sxs-lookup"><span data-stu-id="fa70e-105">This topic describes how to request permissions from the user to use sensors.</span></span> <span data-ttu-id="fa70e-106">Para obter informações básicas sobre permissões na API do sensor, consulte [Managing User Permissions](managing-user-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="fa70e-106">For background information about permissions in the Sensor API, see [Managing User Permissions](managing-user-permissions.md).</span></span>

<span data-ttu-id="fa70e-107">Os exemplos a seguir ilustram alguns dos cenários comuns em que você pode optar por solicitar permissões de usuário.</span><span class="sxs-lookup"><span data-stu-id="fa70e-107">The following examples illustrate some of the common scenarious where you can choose to request user permissions.</span></span>

<span data-ttu-id="fa70e-108">O código de exemplo a seguir solicita apenas permissões para todos os sensores recuperados do Gerenciador de sensor, por tipo, usando uma chamada de método assíncrono.</span><span class="sxs-lookup"><span data-stu-id="fa70e-108">The following example code simply requests permissions for all sensors retrieved from the sensor manager, by type, using an asynchronous method call.</span></span> <span data-ttu-id="fa70e-109">A plataforma abrirá uma caixa de diálogo para solicitar ao usuário apenas habilitar os sensores que ainda não estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="fa70e-109">The platform will open a dialog box to prompt the user only to enable sensors that are not already enabled.</span></span> <span data-ttu-id="fa70e-110">Para determinar se o usuário habilitou quaisquer sensores nesse caso, você deve manipular o evento [**ISensorEvents:: OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) .</span><span class="sxs-lookup"><span data-stu-id="fa70e-110">To determine whether the user enabled any sensors in this case, you must handle the [**ISensorEvents::OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) event.</span></span>


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



<span data-ttu-id="fa70e-111">Você pode optar por testar o estado do sensor de forma síncrona antes de tentar recuperar os dados.</span><span class="sxs-lookup"><span data-stu-id="fa70e-111">You can choose to test the sensor state synchronously before attempting to retrieve data.</span></span> <span data-ttu-id="fa70e-112">O código de exemplo a seguir demonstra essa técnica.</span><span class="sxs-lookup"><span data-stu-id="fa70e-112">The following example code demonstrates this technique.</span></span>


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



<span data-ttu-id="fa70e-113">O código de exemplo a seguir solicita ao usuário permissões de sensor se uma tentativa de recuperar um relatório de dados de um sensor específico falhar.</span><span class="sxs-lookup"><span data-stu-id="fa70e-113">The following example code prompts the user for sensor permissions if an attempt to retrieve a data report from a particular sensor fails.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="fa70e-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fa70e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa70e-115">**ISensorManager**</span><span class="sxs-lookup"><span data-stu-id="fa70e-115">**ISensorManager**</span></span>](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager)
</dt> <dt>

[<span data-ttu-id="fa70e-116">Gerenciando permissões de usuário</span><span class="sxs-lookup"><span data-stu-id="fa70e-116">Managing User Permissions</span></span>](managing-user-permissions.md)
</dt> </dl>

 

 
