---
description: Usando dados de sensor claro
ms.assetid: 98272df5-08c0-4392-a74b-2919bbdcb022
title: Usando dados de sensor claro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae4f7047301c7d31d18014bb09512d1f3944c418a34c153a87c001f95fb63a8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425122"
---
# <a name="using-light-sensor-data"></a>Usando dados de sensor claro

Há duas maneiras recomendadas de interpretar e usar dados de Lux que vêm de sensores de luz ambiente.

-   Aplique uma transformação aos dados para que o nível de luz normalizado possa ser usado na proporção direta para comportamentos de programa ou interações. Um exemplo seria variar o tamanho de um botão em seu programa na proporção direta para os dados normalizados (ou um intervalo dos dados normalizados, que corresponde a áreas externas, por exemplo). Essa abordagem oferece a implementação ideal.
-   Lide com intervalos de dados do Lux e mapeie comportamentos e reações do programa para os limites superior e inferior desses intervalos de dados do Lux. Essa é uma maneira simples de responder às condições de iluminação e pode não produzir a experiência do usuário ideal. No entanto, essa abordagem funcionará bem se não for possível fazer transições suaves.

## <a name="handling-data-from-multiple-light-sensors"></a>Tratamento de dados de vários sensores leves

Para produzir a aproximação mais precisa das condições de iluminação atuais, você pode usar dados de vários sensores de luz ambiente. Como os sensores de luz ambiente podem ser parcialmente ou totalmente obscuros por sombras ou objetos que abrangem o sensor, vários sensores posicionados de distância podem fornecer uma aproximação muito melhor das condições de iluminação atuais do que um único sensor.

Para acompanhar os dados provenientes de vários sensores, você pode usar as duas técnicas a seguir:

-   O valor de dados mais recente para cada sensor de luz ambiente pode ser retido, juntamente com o carimbo de data/hora do relatório de dados do sensor para cada uma dessas leituras. O último [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) recebido para cada sensor de leitura pode ser retido e pode fornecer ambos os valores para referência posterior. Ao se referir ao carimbo de data/hora de cada relatório de dados do sensor, os dados podem ser gerenciados com base em sua idade. Por exemplo, se os dados tiverem mais de 2 segundos de idade, eles poderão ser omitidos. Com base nos valores de dados de sensor mais recentes, a leitura mais alta pode ser usada porque o sensor correspondente seria presumido não ser obscurecido.
-   Você pode usar o valor do último sensor de luz ambiente relatado. Essa implementação não seria ideal porque os valores de vários sensores não são comparados entre si para obter o resultado mais preciso. Não recomendamos esse método.

## <a name="example-code"></a>Código de exemplo

O código de exemplo a seguir mostra uma implementação para o evento [**OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) . O manipulador de eventos chama uma função auxiliar, chamada **UpdateUI**, que altera a interface do usuário com base no valor Lux. Escrever a implementação do UpdateUI cabe a você.


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



 

 
