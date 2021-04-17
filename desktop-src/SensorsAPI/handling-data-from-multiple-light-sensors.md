---
description: Usando dados de sensor claro
ms.assetid: 98272df5-08c0-4392-a74b-2919bbdcb022
title: Usando dados de sensor claro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ccf1c032b4100174afd6073d8c43db27bce3892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762898"
---
# <a name="using-light-sensor-data"></a><span data-ttu-id="5547e-103">Usando dados de sensor claro</span><span class="sxs-lookup"><span data-stu-id="5547e-103">Using Light Sensor Data</span></span>

<span data-ttu-id="5547e-104">Há duas maneiras recomendadas de interpretar e usar dados de Lux que vêm de sensores de luz ambiente.</span><span class="sxs-lookup"><span data-stu-id="5547e-104">There are two recommended ways of interpreting and using lux data that comes from ambient light sensors.</span></span>

-   <span data-ttu-id="5547e-105">Aplique uma transformação aos dados para que o nível de luz normalizado possa ser usado na proporção direta para comportamentos de programa ou interações.</span><span class="sxs-lookup"><span data-stu-id="5547e-105">Apply a transform to the data so that the normalized light level can be used in direct proportion to program behaviors or interactions.</span></span> <span data-ttu-id="5547e-106">Um exemplo seria variar o tamanho de um botão em seu programa na proporção direta para os dados normalizados (ou um intervalo dos dados normalizados, que corresponde a áreas externas, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="5547e-106">An example would be to vary the size of a button in your program in direct proportion to the normalized data (or a range of the normalized data, corresponding to outdoors, for example).</span></span> <span data-ttu-id="5547e-107">Essa abordagem oferece a implementação ideal.</span><span class="sxs-lookup"><span data-stu-id="5547e-107">This approach gives the optimal implementation.</span></span>
-   <span data-ttu-id="5547e-108">Lide com intervalos de dados do Lux e mapeie comportamentos e reações do programa para os limites superior e inferior desses intervalos de dados do Lux.</span><span class="sxs-lookup"><span data-stu-id="5547e-108">Deal with ranges of lux data, and map program behaviors and reactions to the upper and lower thresholds of these ranges of lux data.</span></span> <span data-ttu-id="5547e-109">Essa é uma maneira simples de responder às condições de iluminação e pode não produzir a experiência do usuário ideal.</span><span class="sxs-lookup"><span data-stu-id="5547e-109">This is a simple way to respond to lighting conditions and may not yield the optimal user experience.</span></span> <span data-ttu-id="5547e-110">No entanto, essa abordagem funcionará bem se não for possível fazer transições suaves.</span><span class="sxs-lookup"><span data-stu-id="5547e-110">However, this approach works fine if smooth transitions are not feasible.</span></span>

## <a name="handling-data-from-multiple-light-sensors"></a><span data-ttu-id="5547e-111">Tratamento de dados de vários sensores leves</span><span class="sxs-lookup"><span data-stu-id="5547e-111">Handling Data from Multiple Light Sensors</span></span>

<span data-ttu-id="5547e-112">Para produzir a aproximação mais precisa das condições de iluminação atuais, você pode usar dados de vários sensores de luz ambiente.</span><span class="sxs-lookup"><span data-stu-id="5547e-112">To produce the most accurate approximation of the current lighting conditions, you can use data from multiple ambient light sensors.</span></span> <span data-ttu-id="5547e-113">Como os sensores de luz ambiente podem ser parcialmente ou totalmente obscuros por sombras ou objetos que abrangem o sensor, vários sensores posicionados de distância podem fornecer uma aproximação muito melhor das condições de iluminação atuais do que um único sensor.</span><span class="sxs-lookup"><span data-stu-id="5547e-113">Because ambient light sensors can be partly or fully obscured by shadows or objects that cover the sensor, multiple sensors placed some distance apart can provide a much better approximation of the current lighting conditions than a single sensor.</span></span>

<span data-ttu-id="5547e-114">Para acompanhar os dados provenientes de vários sensores, você pode usar as duas técnicas a seguir:</span><span class="sxs-lookup"><span data-stu-id="5547e-114">To keep track of the data coming from multiple sensors, you can use the following two techniques:</span></span>

-   <span data-ttu-id="5547e-115">O valor de dados mais recente para cada sensor de luz ambiente pode ser retido, juntamente com o carimbo de data/hora do relatório de dados do sensor para cada uma dessas leituras.</span><span class="sxs-lookup"><span data-stu-id="5547e-115">The most recent data value for each ambient light sensor can be retained, along with the time stamp from the sensor data report for each of these readings.</span></span> <span data-ttu-id="5547e-116">O último [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) recebido para cada sensor de leitura pode ser retido e pode fornecer ambos os valores para referência posterior.</span><span class="sxs-lookup"><span data-stu-id="5547e-116">The last [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) received for each sensor reading could be retained and could provide both values for later reference.</span></span> <span data-ttu-id="5547e-117">Ao se referir ao carimbo de data/hora de cada relatório de dados do sensor, os dados podem ser gerenciados com base em sua idade.</span><span class="sxs-lookup"><span data-stu-id="5547e-117">By referring to the time stamp for each sensor data report, the data can be managed based on its age.</span></span> <span data-ttu-id="5547e-118">Por exemplo, se os dados tiverem mais de 2 segundos de idade, eles poderão ser omitidos.</span><span class="sxs-lookup"><span data-stu-id="5547e-118">For example, if the data is more than 2 seconds old, it could be omitted.</span></span> <span data-ttu-id="5547e-119">Com base nos valores de dados de sensor mais recentes, a leitura mais alta pode ser usada porque o sensor correspondente seria presumido não ser obscurecido.</span><span class="sxs-lookup"><span data-stu-id="5547e-119">Based on the newer sensor data values, the highest reading could be used because the corresponding sensor would be presumed not to be obscured.</span></span>
-   <span data-ttu-id="5547e-120">Você pode usar o valor do último sensor de luz ambiente relatado.</span><span class="sxs-lookup"><span data-stu-id="5547e-120">You can use the last ambient light sensor value reported.</span></span> <span data-ttu-id="5547e-121">Essa implementação não seria ideal porque os valores de vários sensores não são comparados entre si para obter o resultado mais preciso.</span><span class="sxs-lookup"><span data-stu-id="5547e-121">This implementation would not be optimal because the values from multiple sensors are not compared to one another to obtain the most accurate result.</span></span> <span data-ttu-id="5547e-122">Não recomendamos esse método.</span><span class="sxs-lookup"><span data-stu-id="5547e-122">We do not recommend this method.</span></span>

## <a name="example-code"></a><span data-ttu-id="5547e-123">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="5547e-123">Example Code</span></span>

<span data-ttu-id="5547e-124">O código de exemplo a seguir mostra uma implementação para o evento [**OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) .</span><span class="sxs-lookup"><span data-stu-id="5547e-124">The following example code shows an implementation for the [**OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) event.</span></span> <span data-ttu-id="5547e-125">O manipulador de eventos chama uma função auxiliar, chamada **UpdateUI**, que altera a interface do usuário com base no valor Lux.</span><span class="sxs-lookup"><span data-stu-id="5547e-125">The event handler calls a helper function, named **UpdateUI**, that changes the user interface based on the lux value.</span></span> <span data-ttu-id="5547e-126">Escrever a implementação do UpdateUI cabe a você.</span><span class="sxs-lookup"><span data-stu-id="5547e-126">Writing the implementation of UpdateUI is up to you.</span></span>


```C++
// Override of ISensorEvents::OnDataUpdated
// Part of an event sink implementation for ISensorEvents
STDMETHODIMP CALSEventSink::OnDataUpdated(
    ISensor* pSensor, 
    ISensorDataReport* pNewData)
{
    HRESULT hr = S_OK;
   
    if(pSensor == NULL ||
       pNewData == NULL)
    {
         return E_POINTER;
    }

    // Declare and initialize the PROPVARIANT
    PROPVARIANT lightLevel;
    PropVariantInit(&lightLevel);

    // Get the sensor reading from the ISensorDataReport object
    hr = pNewData->GetSensorValue(
        SENSOR_DATA_TYPE_LIGHT_LEVEL_LUX, 
        &lightLevel);

    if(SUCCEEDED(hr))
    {
        if(lightlevel.vt == VT_R4)
        {
            // Extract the float value from the PROPVARIANT object
            float luxValue = lightLevel.fltVal;

            // Normalize the light sensor data
            double lightNormalized = ::log10(luxValue) / 5.0;

            // Handle UI changes based on the normalized LUX data
            // which ranges from 0.0 - 1.0 for a lux range of 
            // 0 lux to 100,000 lux. 
            UpdateUI(lightNormalized);
        }
    }

    // Release the variant.     
    PropVariantClear(&lightLevel);

    return hr;
}
```



 

 
