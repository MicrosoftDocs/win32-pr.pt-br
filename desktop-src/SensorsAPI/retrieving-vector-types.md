---
description: Algumas propriedades e campos de dados contêm matrizes de informações.
ms.assetid: 85e3b953-be36-4d60-b04e-4f572d0b9564
title: Recuperando tipos de vetor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4945b45e4e78b6c4f9f9e0fb4b3848f813549105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501522"
---
# <a name="retrieving-vector-types"></a><span data-ttu-id="4b824-103">Recuperando tipos de vetor</span><span class="sxs-lookup"><span data-stu-id="4b824-103">Retrieving Vector Types</span></span>

<span data-ttu-id="4b824-104">Algumas propriedades e campos de dados contêm matrizes de informações.</span><span class="sxs-lookup"><span data-stu-id="4b824-104">Some properties and data fields contain arrays of information.</span></span> <span data-ttu-id="4b824-105">Por exemplo, a \_ propriedade de curva de resposta leve da propriedade sensor \_ \_ \_ contém uma matriz de inteiros sem sinal de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="4b824-105">For example, the SENSOR\_PROPERTY\_LIGHT\_RESPONSE\_CURVE property contains an array of 4-byte unsigned integers.</span></span> <span data-ttu-id="4b824-106">No entanto, quando você recebe essas matrizes por meio da API do sensor, elas são sempre representadas como tipo \_ \| UI1 de vetor, uma matriz de caracteres de byte único, independentemente do tipo real dos dados na matriz.</span><span class="sxs-lookup"><span data-stu-id="4b824-106">However, when you receive such arrays through the Sensor API, they are always represented as type VT\_VECTOR\|UI1, an array of single-byte characters, regardless of the actual type of the data in the array.</span></span> <span data-ttu-id="4b824-107">Para esses tipos, você deve ter cuidado para converter variáveis de matriz para o tipo de dados correto para a propriedade ou o campo de dados.</span><span class="sxs-lookup"><span data-stu-id="4b824-107">For these types, you must be careful to cast array variables to the correct data type for the property or data field.</span></span>

<span data-ttu-id="4b824-108">Para obter informações sobre propriedades, campos de dados e seus tipos, consulte [constantes](constants.md).</span><span class="sxs-lookup"><span data-stu-id="4b824-108">For information about properties, data fields, and their types, see [Constants](constants.md).</span></span>

<span data-ttu-id="4b824-109">O código de exemplo a seguir mostra como converter os dados recuperados \_ na \_ curva de resposta clara da propriedade sensor \_ \_ para o tipo correto.</span><span class="sxs-lookup"><span data-stu-id="4b824-109">The following example code shows how to cast the data retrieved in SENSOR\_PROPERTY\_LIGHT\_RESPONSE\_CURVE to the correct type.</span></span>


```C++
PROPVARIANT pvCurve;
PropVariantInit(&pvCurve);

// Retrieve the property value.
hr = pSensor->GetProperty(SENSOR_PROPERTY_LIGHT_RESPONSE_CURVE, &pvCurve);
if (SUCCEEDED(hr))
{
    if ((VT_UI1|VT_VECTOR) == V_VT(pvCurve)) // Note actual type of UI1
    {
        // Cast the array to UINT, a 4-byte unsigned integer.

        // Item count for the array.
        UINT  cElement = pvCurve.caub.cElems/sizeof(UINT);
        // Array pointer.
        UINT* pElement = (UINT*)(pvCurve.caub.pElems);

        // Use the array.
    }
}

// Remember to free the PROPVARIANT when done.
PropVariantClear(&pvCurve);
```



 

 



