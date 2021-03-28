---
title: switch (sm4-ASM)
description: Transfere o controle para um bloco de instruções diferente dentro do corpo do comutador, dependendo do valor de um seletor.
ms.assetid: ECAEECFD-B955-4356-B5C9-1D6A04C71D8F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feed346b8aa33feecc13fe2a6ffad59c961b0173
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006892"
---
# <a name="switch-sm4---asm"></a>switch (sm4-ASM)

Transfere o controle para um bloco de instruções diferente dentro do corpo do comutador, dependendo do valor de um seletor.



| alternar src0. \_ componente selecionado |
|---------------------------------|



 



| Item                                                            | Descrição                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[no \] seletor da instrução switch.<br/> |



 

## <a name="remarks"></a>Comentários

Uma construção **de** / [comutador](endswitch--sm4---asm-.md) endswitch se comporta exatamente como uma construção de **comutador** na linguagem C, com a seguinte exceção: para instruções padrão D3D11 [Case](case--sm4---asm-.md) / [](default--sm4---asm-.md) que se enquadram no próximo **caso**, o / **padrão** sem uma [interrupção](break--sm4---asm-.md) não pode ter nenhum código. Ele é permitido para várias instruções **Case** , incluindo **Default**, para aparecer sequencialmente, compartilhando o mesmo bloco de código.

A condição deve ser um componente de registro de 32 bits ou uma quantidade imediata. A comparação de igualdade é bit-a-bit (Integer).

Como com qualquer instrução de sombreador no D3D11, o hardware pode ou não implementar o constructo de **comutador** diretamente.

As instruções **switch** podem ser aninhadas. Cada bloco **switch** conta como um nível em relação ao limite de profundidade de aninhamento de controle de fluxo de 64 por sub-rotina e Main, independentemente do número de instruções **Case** . O compilador HLSL não gerará sub-rotinas que excedam esse limite. O comportamento das instruções de fluxo de controle além de 64 níveis de profundidade por sub-rotina é indefinido.

O exemplo a seguir mostra como usar essa instrução.

``` syntax
                ...
                switch r0.x
                default: // falling through
                case 3
                    switch r1.x
                    case 4
                        ...
                        break
                    case 5
                        ...
                        break
                    endswitch
                    break
                case 0
                    break
                endswitch
```

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

 

 





