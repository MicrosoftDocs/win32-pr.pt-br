---
description: Este tópico descreve como verificar se um sensor pode fornecer um conjunto específico de campos de dados.
ms.assetid: 918ba4a3-d2ac-47ee-ba29-f7ddf67ffbc5
title: Verificando os campos de dados de sensor com suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfd9cf42d1008ec1bb0e2785ec5113c5a817105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756555"
---
# <a name="checking-for-supported-sensor-data-fields"></a><span data-ttu-id="34a4b-103">Verificando os campos de dados de sensor com suporte</span><span class="sxs-lookup"><span data-stu-id="34a4b-103">Checking for Supported Sensor Data Fields</span></span>

<span data-ttu-id="34a4b-104">Este tópico descreve como verificar se um sensor pode fornecer um conjunto específico de campos de dados.</span><span class="sxs-lookup"><span data-stu-id="34a4b-104">This topic describes how to verify that a sensor can provide a particular set of data fields.</span></span>

<span data-ttu-id="34a4b-105">Depois de recuperar um objeto de sensor, você pode chamar [**ISensor:: GetSupportedDataFields**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getsupporteddatafields) para determinar se o sensor pode fornecer os dados necessários.</span><span class="sxs-lookup"><span data-stu-id="34a4b-105">After you have retrieved a sensor object, you can call [**ISensor::GetSupportedDataFields**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getsupporteddatafields) to determine whether the sensor can provide the data you need.</span></span>

<span data-ttu-id="34a4b-106">O código de exemplo a seguir cria uma função auxiliar que testa se o sensor pode fornecer todos os três campos de dados de exemplo.</span><span class="sxs-lookup"><span data-stu-id="34a4b-106">The following example code creates a helper function that tests whether the sensor can provide all three of the sample data fields.</span></span> <span data-ttu-id="34a4b-107">A função usa um ponteiro para um sensor como entrada e retorna um valor booliano, onde **true** indica que o sensor pode fornecer todos os campos de dados necessários.</span><span class="sxs-lookup"><span data-stu-id="34a4b-107">The function takes a pointer to a sensor as its input and returns a Boolean value, where **TRUE** indicates that the sensor can provide all the data fields required.</span></span>


```C++
BOOL CheckForSupportedDataFields(ISensor* pSensor)
{
    assert(pSensor);

    HRESULT hr = S_OK;
    DWORD cKeys = 0; // Key count.
    BOOL bRet = FALSE;

    IPortableDeviceKeyCollection* pKeys = NULL; // Output

    // CoCreate a key collection to store property keys.
    hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection, 
                                NULL, 
                                CLSCTX_INPROC_SERVER, 
                                IID_PPV_ARGS(&pKeys));

    if(SUCCEEDED(hr))
    {
        hr = pSensor->GetSupportedDataFields(&pKeys);
    }

    if(SUCCEEDED(hr))
    {
        hr = pKeys->GetCount(&cKeys);
    }

    if(SUCCEEDED(hr))
    {
        PROPERTYKEY pk;
        BOOL bHour, bMinute, bSecond = FALSE;

        for (DWORD i = 0; i < cKeys; i++)
        {
            hr = pKeys->GetAt(i, &pk);

            if(SUCCEEDED(hr))
            {
                // Test for the data fields.
                if(IsEqualPropertyKey(pk, SAMPLE_SENSOR_DATA_TYPE_HOUR))
                {
                    bHour = TRUE;
                }
                else if(IsEqualPropertyKey(pk, SAMPLE_SENSOR_DATA_TYPE_MINUTE))
                {
                    bMinute = TRUE;
                }
                else if(IsEqualPropertyKey(pk, SAMPLE_SENSOR_DATA_TYPE_SECOND))
                {
                    bSecond = TRUE;
                }
            }
        }

        // Compute the return value.
        // If all three properties were found,
        // bRet will resolve to TRUE.
        bRet = bHour && bMinute && bSecond;
    }

    SafeRelease(&pKeys);

    return bRet;
}
```



## <a name="related-topics"></a><span data-ttu-id="34a4b-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="34a4b-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34a4b-109">**ISensorDataReport**</span><span class="sxs-lookup"><span data-stu-id="34a4b-109">**ISensorDataReport**</span></span>](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport)
</dt> </dl>

 

 
