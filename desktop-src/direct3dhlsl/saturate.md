---
title: Saturação (referência de HLSL)
description: Coloca o resultado de uma operação aritmética de ponto flutuante de precisão simples ou dupla para \ 0,0 f... 1,0 f \ intervalo.
ms.assetid: ce3e79c7-c3e6-4a2c-910a-2cd568aece50
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 25e771bd53dbb8a4b0d2eaf8162675cd556c071344b249562defe4a06e715f5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790739"
---
# <a name="saturate-hlsl-reference"></a>Saturação (referência de HLSL)

Coloca o resultado de uma operação aritmética de ponto flutuante de precisão única ou dupla para \[ 0,0 f... 1,0 intervalo de f \] .



| \_saturação |
|-------|



 

O modificador de resultado de instrução **saturação** executa a seguinte operação nos valores de resultado de uma operação aritmética de ponto flutuante que se comparou \_ com ela:

`min(1.0f, max(0.0f, value))`

em que min () e Max () na expressão acima se comportam de forma que [mín](min--sm4---asm-.md)., [máx](max--sm4---asm-.md)., [DMín](dmin--sm5---asm-.md)ou [DMáx](dmax--sm5---asm-.md) operem.

`_sat(NaN)` Retorna 0, pelas regras para min e Max.

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Esse modificador tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modificadores de instrução](instruction-modifiers.md)
</dt> </dl>

 

 




