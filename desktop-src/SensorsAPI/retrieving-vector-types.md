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
# <a name="retrieving-vector-types"></a>Recuperando tipos de vetor

Algumas propriedades e campos de dados contêm matrizes de informações. Por exemplo, a \_ propriedade de curva de resposta leve da propriedade sensor \_ \_ \_ contém uma matriz de inteiros sem sinal de 4 bytes. No entanto, quando você recebe essas matrizes por meio da API do sensor, elas são sempre representadas como tipo \_ \| UI1 de vetor, uma matriz de caracteres de byte único, independentemente do tipo real dos dados na matriz. Para esses tipos, você deve ter cuidado para converter variáveis de matriz para o tipo de dados correto para a propriedade ou o campo de dados.

Para obter informações sobre propriedades, campos de dados e seus tipos, consulte [constantes](constants.md).

O código de exemplo a seguir mostra como converter os dados recuperados \_ na \_ curva de resposta clara da propriedade sensor \_ \_ para o tipo correto.


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



 

 



