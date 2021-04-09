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
# <a name="retrieving-a-sensor-object"></a><span data-ttu-id="73596-105">Recuperando um objeto de sensor</span><span class="sxs-lookup"><span data-stu-id="73596-105">Retrieving a Sensor Object</span></span>

<span data-ttu-id="73596-106">Para recuperar um objeto de sensor, use a interface [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager) .</span><span class="sxs-lookup"><span data-stu-id="73596-106">To retrieve a sensor object, you use the [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager) interface.</span></span> <span data-ttu-id="73596-107">Você pode considerar essa interface como a interface raiz para a API do sensor.</span><span class="sxs-lookup"><span data-stu-id="73596-107">You can think of this interface as the root interface for the Sensor API.</span></span> <span data-ttu-id="73596-108">Para usar **ISensorManager**, você deve primeiro chamar o método com **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="73596-108">To use **ISensorManager**, you must first call the COM **CoCreateInstance** method.</span></span>

<span data-ttu-id="73596-109">O código de exemplo a seguir cria uma instância do Gerenciador de sensor.</span><span class="sxs-lookup"><span data-stu-id="73596-109">The following example code creates an instance of the sensor manager.</span></span>


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



<span data-ttu-id="73596-110">Depois de recuperar com êxito um ponteiro para [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager), você pode recuperar sensores por categoria, tipo ou ID.</span><span class="sxs-lookup"><span data-stu-id="73596-110">After successfully retrieving a pointer to [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager), you can retrieve sensors by category, type, or ID.</span></span> <span data-ttu-id="73596-111">Se você recuperar sensores por tipo ou categoria, receberá um ponteiro para uma interface [**ISensorCollection**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection) que contém todos os sensores disponíveis que pertencem à categoria ou ao tipo solicitado.</span><span class="sxs-lookup"><span data-stu-id="73596-111">If you retrieve sensors by type or category, you receive a pointer to an [**ISensorCollection**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection) interface that contains all the available sensors that belong to the requested category or type.</span></span> <span data-ttu-id="73596-112">Se você recuperar um sensor por sua ID, receberá um ponteiro para uma interface [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) que representa o sensor exclusivo que você solicitou.</span><span class="sxs-lookup"><span data-stu-id="73596-112">If you retrieve a sensor by its ID, you receive a pointer to an [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) interface that represents the unique sensor you requested.</span></span>

<span data-ttu-id="73596-113">O código de exemplo a seguir recupera uma coleção de sensores que pertencem à categoria chamada \_ data hora da categoria do sensor de exemplo \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="73596-113">The following example code retrieves a collection of sensors that belong to the category named SAMPLE\_SENSOR\_CATEGORY\_DATE\_TIME.</span></span> <span data-ttu-id="73596-114">Em seguida, o código recupera o primeiro sensor na coleção por seu índice.</span><span class="sxs-lookup"><span data-stu-id="73596-114">The code then retrieves the first sensor in the collection by its index.</span></span>


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



<span data-ttu-id="73596-115">Observe que você pode recuperar todos os sensores disponíveis usando a categoria de \_ sensor \_ todos.</span><span class="sxs-lookup"><span data-stu-id="73596-115">Note that you can retrieve all of the available sensors by using SENSOR\_CATEGORY\_ALL.</span></span>

<span data-ttu-id="73596-116">De forma semelhante, você pode recuperar sensores de um tipo específico.</span><span class="sxs-lookup"><span data-stu-id="73596-116">In a similar way, you can retrieve sensors of a particular type.</span></span>

<span data-ttu-id="73596-117">O código de exemplo a seguir recupera uma coleção de sensores do tipo chamado \_ tempo de tipo de sensor de exemplo \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="73596-117">The following example code retrieves a collection of sensors of the type named SAMPLE\_SENSOR\_TYPE\_TIME.</span></span> <span data-ttu-id="73596-118">Em seguida, o código recupera o primeiro sensor na coleção por seu índice.</span><span class="sxs-lookup"><span data-stu-id="73596-118">The code then retrieves the first sensor in the collection by its index.</span></span>


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



<span data-ttu-id="73596-119">Para recuperar um sensor por sua ID, você deve saber a ID exclusiva do sensor.</span><span class="sxs-lookup"><span data-stu-id="73596-119">To retrieve a sensor by its ID, you must know the unique ID for the sensor.</span></span> <span data-ttu-id="73596-120">Os sensores geralmente geram essa ID quando conectado pela primeira vez para permitir que você identifique vários sensores da mesma marca e modelo.</span><span class="sxs-lookup"><span data-stu-id="73596-120">Sensors usually generate this ID when first connected to enable you to identify multiple sensors of the same make and model.</span></span> <span data-ttu-id="73596-121">Isso significa que você provavelmente não saberá a ID do sensor com antecedência.</span><span class="sxs-lookup"><span data-stu-id="73596-121">This means that you probably will not know the sensor ID in advance.</span></span> <span data-ttu-id="73596-122">No entanto, se você tiver armazenado uma cópia de uma ID de sensor específica que você recuperou anteriormente, por exemplo, chamando [**ISensor:: GetID**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getid), talvez você queira recuperar o mesmo sensor novamente.</span><span class="sxs-lookup"><span data-stu-id="73596-122">However, if you have stored a copy of a particular sensor ID that you previously retrieved, for example by calling [**ISensor::GetID**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getid), you may want to retrieve the same sensor again.</span></span>

<span data-ttu-id="73596-123">O código de exemplo a seguir mostra como recuperar um sensor usando sua ID.</span><span class="sxs-lookup"><span data-stu-id="73596-123">The following example code shows how to retrieve a sensor by using its ID.</span></span>


```C++
ISensor* pSensor = NULL;

// Get the sensor collection.
hr = pSensorManager->GetSensorByID(SAMPLE_SENSOR_TIME_ID, &pSensor);

```



<span data-ttu-id="73596-124">Você também pode recuperar sensores quando eles estiverem disponíveis ao receber um evento do Gerenciador de sensor.</span><span class="sxs-lookup"><span data-stu-id="73596-124">You can also retrieve sensors when they become available by receiving an event from the sensor manager.</span></span> <span data-ttu-id="73596-125">Para obter mais informações, consulte [**ISensorManager:: SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink).</span><span class="sxs-lookup"><span data-stu-id="73596-125">For more information, see [**ISensorManager::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink).</span></span>

## <a name="related-topics"></a><span data-ttu-id="73596-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="73596-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73596-127">**ISensorManagerEvents::OnSensorEnter**</span><span class="sxs-lookup"><span data-stu-id="73596-127">**ISensorManagerEvents::OnSensorEnter**</span></span>](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanagerevents-onsensorenter)
</dt> </dl>

 

 
