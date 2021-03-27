---
title: texdepth-PS
description: Calcule os valores de profundidade a serem usados no teste de comparação de buffer de profundidade para este pixel.
ms.assetid: f7128dbb-a5f3-4e95-b53b-7432439ae0c4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3eb5cd337108d08efee465c136adf1afb4921123
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103823438"
---
# <a name="texdepth---ps"></a>texdepth-PS

Calcule os valores de profundidade a serem usados no teste de comparação de buffer de profundidade para este pixel.

## <a name="syntax"></a>Syntax



| texdepth DST |
|--------------|



 

onde

-   DST é o registro de destino.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texdepth              |      |      |      | x    |      |      |       |      |       |



 

Essa instrução usa R5. r/R5. g no teste de comparação de buffer de profundidade para este pixel. Os dados nos canais azul e alfa são ignorados. Se r5. g = 0, o resultado de R5. r/R5. g = 1,0.

O registro temporário R5 é o único registro que essa instrução pode usar.

Depois de executar essa instrução, o registro temporário R5 não estará disponível para uso adicional no sombreador.

Quando a multiamostragem, o uso dessa instrução elimina a maior parte do benefício do buffer de profundidade de resolução mais alto. Como o sombreador de pixel é executado uma vez por pixel, a saída de valor de profundidade única por [texm3x2depth-PS](texm3x2depth---ps.md) ou texdepth será usada para cada um dos testes de comparação de profundidade de subpixel.

## <a name="examples"></a>Exemplos

Aqui está um exemplo usando texdepth.


```
ps_1_4              
texld  r0, t0        // Sample texture from texture stage 0 (dest 
                     //   register number) into r0
                     // Use texture coordinate data from t0
texcrd r1.rgb, t1    // Load a second set of texture coordinate data into r1
add    r5.rg, r0, r1 // Add the two sets of texture coordinate data
phase                // Phase marker, required when using texdepth instruction
texdepth  r5         // Calculate pixel depth as r5.r / r5.g
                     // Do other color calculations with shader output r0
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




