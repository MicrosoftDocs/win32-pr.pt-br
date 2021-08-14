---
title: switch (sm4 – asm)
description: Transfere o controle para um bloco de instrução diferente dentro do corpo da opção, dependendo do valor de um seletor.
ms.assetid: ECAEECFD-B955-4356-B5C9-1D6A04C71D8F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39cb304c1ccf59c188a4e1f20f2b136897d833c80d6eb67cb0eb683d628ab9aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724347"
---
# <a name="switch-sm4---asm"></a>switch (sm4 – asm)

Transfere o controle para um bloco de instrução diferente dentro do corpo da opção, dependendo do valor de um seletor.



| componente switch src0.selected \_ |
|---------------------------------|



 



| Item                                                            | Descrição                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[no \] seletor da instrução switch.<br/> |



 

## <a name="remarks"></a>Comentários

Um constructo switch endswitch se comporta exatamente como um constructo de opção na linguagem C, com a seguinte exceção: para instruções padrão de caso / [](endswitch--sm4---asm-.md) D3D11  que se enquadram no padrão de caso seguinte sem uma quebra não podem ter nenhum [](case--sm4---asm-.md) / [](default--sm4---asm-.md)  /  código. [](break--sm4---asm-.md) É permitido que várias instruções **case,** incluindo **padrão,** apareçam sequencialmente, compartilhando o mesmo bloco de código.

A condição deve ser um componente de registro de 32 bits ou uma quantidade imediata. A comparação de igualdade é bit a bit (inteiro).

Assim como com qualquer instrução de sombreador no D3D11, o hardware pode ou não implementar o constructo **do comuador** diretamente.

**Instruções** switch podem ser aninhadas. Cada **bloco de** opção conta como um nível em relação ao limite de profundidade de aninhamento do controle de fluxo de 64 por sub-rotina e principal, independentemente do número de instruções **case.** O compilador HLSL não gerará sub-rotinas que excedem esse limite. O comportamento das instruções de fluxo de controle além de 64 níveis de profundidade por sub-rotina é indefinido.

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

Essa instrução se aplica aos seguintes estágios do sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





