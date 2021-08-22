---
title: swapc (SM5-ASM)
description: Executa uma troca condicional inteligente de componentes dos valores entre dois registros de entrada.
ms.assetid: 3DFCEB82-076E-4AFA-915F-47390A355B7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d09d52bd497c7819500c11c4464907e4a7854bb305ed0e31d53b897ba4cf7e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119486256"
---
# <a name="swapc-sm5---asm"></a>swapc (SM5-ASM)

Executa uma troca condicional inteligente de componentes dos valores entre dois registros de entrada.



| swapc dest0 \[ . Mask \] , dest1 \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle \] , src2 \[ . swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Item                                                               | Descrição                                                                                     |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[em \] registrar com máscaras de gravação não vazias arbitrárias. Deve ser diferente de *dest1*.<br/> |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[em \] registrar com máscaras de gravação não vazias arbitrárias. Deve ser diferente de *dest0*.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[o no \] fornece 4 condições. Um valor inteiro diferente de zero significa **true**. <br/>               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>    | \[em \] um dos valores a serem trocados.<br/>                                              |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/>    | \[em \] um dos valores a serem trocados.<br/>                                              |



 

## <a name="remarks"></a>Comentários

A codificação dessa instrução tenta expressar compactar várias trocas condicionais paralelas de escalares entre os registros de 2 4 componentes, com flexibilidade secundária na disposição dos pares de números envolvidos na troca.

A escolha de Register e Value para *src0*, *src1* e *src2* não são restringidas de forma alguma, como [movc](movc--sm4---asm-.md).

A semântica dessa instrução pode ser descrita pelas operações equivalentes com a instrução **movc** . O pior caso é mostrado no exemplo a seguir, garantindo que os registros de destino não sejam atualizados até o final.

``` syntax
                swapc dest0[.mask], 
                      dest1[.mask],
                      src0[.swizzle],
                      src1[.swizzle],
                      src2[.swizzle]

                expands to:

                movc temp[dest0 s mask], 
                     src0[.swizzle], 
                     src2[.swizzle], src1[.swizzle]

                movc dest1[.mask], 
                     src0[.swizzle], 
                     src1[.swizzle], src2[.swizzle]

                mov  dest0.mask, temp
```

Você pode escolher como lidar com a tarefa, se não diretamente. Por exemplo, o mesmo efeito pode ser obtido por uma sequência de até quatro trocas condicionais simples, ou como acima, duas instruções de **movc** de vetor, além de qualquer sobrecarga para garantir que os valores de origem não sejam sobrescritodos por operações anteriores no meio da expansão.

Use esta instrução para classificação.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa instrução tem suporte nos seguintes modelos de sombreador:



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | não        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | não        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





