---
title: dcl_samplerType (SM2, SM3-PS ASM)
description: Declare uma amostra de sombreador de pixel.
ms.assetid: c90ff5b6-f89a-4993-8a5d-dbbc4a7896b0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 764c3b992cd248a8900c3762c7c9e68abd3bed973ca4f7d44b1705122984f321
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726736"
---
# <a name="dcl_samplertype-sm2-sm3---ps-asm"></a>\_SampleType de DCL (SM2, SM3-PS ASM)

Declare uma amostra de sombreador de pixel.

## <a name="syntax"></a>Syntax

\_amostrador DCL s\#



 

em que:

-   \_SampleType define o tipo de dados de amostra. Isso determina quantas coordenadas são exigidas por cada coordenada de textura durante a amostragem. As dimensões de coordenadas de textura a seguir são definidas.
    -   \_Dimensiona
    -   \_simples
    -   \_volume
-   s \# identifica um amostra em que s é uma abreviação para a amostra e \# é o número de amostra. Os exemplos são pseudo-registros porque você não pode ler ou gravar diretamente neles.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| \_classificador de DCL      |      |      |      |      | x    | x    | x     | x    | x     |



 

Todas as \_ instruções de SampleType de DCL devem aparecer antes da primeira instrução executável.

## <a name="example"></a>Exemplo


```
dcl_cube t0.rgb;  // Define a 3D texture map.

add r0, r0, t0;   // Perturb texture coordinates. 
texld r0, s0, r0; // Load r0 with a color sampled from stage0
                  //   at perturbed texture coordinates r0.
                  // This is a dependent texture read.
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




