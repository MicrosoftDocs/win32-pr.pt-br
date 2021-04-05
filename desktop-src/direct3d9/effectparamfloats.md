---
description: Define os números de ponto flutuante do efeito. Este modelo substitui o modelo EffectFloats.
ms.assetid: 7b41d0dc-209f-4ade-a7ed-aa54f421e520
title: EffectParamFloats
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0954ce7679691920c2e104277d12a48f7a34ddf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104009945"
---
# <a name="effectparamfloats"></a>EffectParamFloats

Define os números de ponto flutuante do efeito. Este modelo substitui o modelo [**EffectFloats**](effectfloats.md) .

``` syntax
template EffectParamFloats
{
    < 3014B9A0-62F5-478c-9B86-E4AC9F4E418B >
    STRING ParamName;
    DWORD nFloats;
    array float Floats[nFloats];
} 
```

Em que:

-   ParamName-nome da matriz de floats.
-   nFloats-número de valores de ponto flutuante na matriz.
-   Flutua \[ nFloats \] -matriz de valores de ponto flutuante.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



