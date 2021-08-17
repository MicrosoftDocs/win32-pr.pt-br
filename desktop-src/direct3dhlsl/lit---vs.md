---
title: lit – vs
description: Fornece suporte parcial para iluminação calculando coeficientes de iluminação de dois produtos de ponto e um expoente.
ms.assetid: e0ed1a75-6682-4d05-b0e5-dc65e201de98
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3e5b5ff3451424251d778886af3841c673ce5a85d91022db9144c62574c16640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118089319"
---
# <a name="lit---vs"></a>lit – vs

Fornece suporte parcial para iluminação calculando coeficientes de iluminação de dois produtos de ponto e um expoente.

## <a name="syntax"></a>Syntax



| lit dst, src |
|--------------|



 

onde

-   dst é o registro de destino.
-   src é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Iluminado                    | x    | x    | x    | x     | x    | x     |



 

Presume-se que o vetor de origem contenha os valores mostrados no pseudocódigo a seguir.


```
src.x = N*L        ; The dot product between normal and direction to light
src.y = N*H        ; The dot product between normal and half vector
src.z = ignored    ; This value is ignored
src.w = exponent   ; The value must be between -128.0 and 128.0
```



O fragmento de código a seguir mostra as operações executadas.


```
dest.x = 1;
dest.y = 0;
dest.z = 0;
dest.w = 1;

float power = src.w;
const float MAXPOWER = 127.9961f;
if (power < -MAXPOWER)
    power = -MAXPOWER;          // Fits into 8.8 fixed point format
else if (power > MAXPOWER)
    power = MAXPOWER;          // Fits into 8.8 fixed point format

if (src.x > 0)
{
    dest.y = src.x;
    if (src.y > 0)
    {
        // Allowed approximation is EXP(power * LOG(src.y))
        dest.z = (float)(pow(src.y, power));
    }
}
```



A aritmética de precisão reduzida é aceitável na avaliação do componente y de destino (dest.y). Uma implementação deve dar suporte a pelo menos oito bits de fração no argumento de energia. Os produtos de ponto são calculados com vetores normalizados e os limites de fixação são -128 a 128.

O erro deve corresponder a uma [combinação logp - vs](logp---vs.md) e exp - [vs](exp---vs.md) ou não mais de aproximadamente um bit significativo para um componente de cor de 8 bits.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




