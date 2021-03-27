---
title: If (sm4-ASM)
description: Branch baseado em lógico ou resultado.
ms.assetid: 9F4CF9E0-4D9D-4300-B432-432C560F34BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 653c84be0d30a036bf93d852268e44bcca08bbcb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988554"
---
# <a name="if-sm4---asm"></a>If (sm4-ASM)

Branch baseado em lógico ou resultado.



| Se { \_ z \|\_NZ} src0. Select \_ componente |
|--------------------------------------|



 



| Item                                                            | Descrição                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] contém o componente no qual testar a condição.<br/> |



 

## <a name="remarks"></a>Comentários

O formato do token contém o deslocamento da instrução endif correspondente no sombreador como uma conveniência.

O exemplo a seguir mostra como usar essa instrução.

``` syntax
                if_z r0.x // if all bits in r0.x are zero
                   ...
                else // (optional)
                   ...
                endif
                if_nz r1.x // if any bit in r0.x is nonzero
                   ...
                else // (optional)
                   ...
                endif
```

### <a name="restrictions"></a>Restrições

-   Os operandos de origem (se quatro vetores de componente) devem usar um seletor de componente único.
-   O registro de 32 bits fornecido pelo *src0* é testado em um nível de bit. Se qualquer bit for diferente de zero, **se \_ z** será true. Se todos os bits forem zero, **se \_ NZ** será true.
-   Os blocos de controle de fluxo podem aninhar até 64 de profundidade por sub-rotina (e principal). O compilador HLSL não gerará sub-rotinas que excedam esse limite. O comportamento das instruções de fluxo de controle além de 64 níveis de profundidade (por sub-rotina) é indefinido.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



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

[Assembly do Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





