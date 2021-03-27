---
title: Limites de aninhamento de controle de fluxo
description: As instruções de controle de fluxo do sombreador de vértice têm duas restrições especiais.
ms.assetid: c9f80a97-8245-4974-a284-7974e2d2e504
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4ebb5b491e074c2275081aa3fe629a2486a24c6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637232"
---
# <a name="flow-control-nesting-limits"></a>Limites de aninhamento de controle de fluxo

As instruções de controle de fluxo do sombreador de vértice têm duas restrições especiais. As profundidades de aninhamento restringem o número de instruções que podem ser chamadas dentro umas das outras. Além disso, cada instrução tem uma contagem de Slots de instrução que se aplica ao número máximo de instruções às quais um sombreador pode dar suporte.

> [!Note]  
> Ao usar os \* \_ perfis de \_ sombreador HLSL de 4% do \_ nível \_ 9 \_ x, você usa implicitamente os perfis do [Shader Model 2. x](dx-graphics-hlsl-sm2.md) para dar suporte ao hardware compatível com Direct3D 9. Os perfis do modelo de sombreador 2. x dão suporte a um comportamento de controle de fluxo mais limitado que o [sombreador modelo 4. x](dx-graphics-hlsl-sm4.md) e perfis posteriores.

 

## <a name="depth-count-per-instruction-for-vs_2_0"></a>Contagem de profundidade por instrução para vs \_ 2 \_ 0

Cada instrução conta com base em um ou mais limites de profundidade de aninhamento. Esta tabela mostra a contagem de profundidade que cada instrução adiciona ou subtrai da profundidade existente:



| Instrução                              | Aninhamento estático | Aninhamento dinâmico | aninhamento de loop/representante | aninhamento de chamadas | Contagem de fluxos estáticos                        |
|------------------------------------------|----------------|-----------------|------------------|--------------|------------------------------------------|
| [se bool-vs](if-bool---vs.md)         | 0              | 0               | 0                | 0            | 1                                        |
| [Se \_ comp-vs](if-comp---vs.md)        | N/D            | N/D             | N/D              | N/D          | N/D                                      |
| [se Pred-vs](if-pred---vs.md)         | N/D            | N/D             | N/D              | N/D          | N/D                                      |
| [else-vs](else---vs.md)               | 0              | 0               | 0                | 0            | 1 ([se bool-vs](if-bool---vs.md) apenas) |
| [endif-vs](endif---vs.md)             | -1             | 0               | 0                | 0            | 0                                        |
| [Rep-vs](rep---vs.md)                 | 0              | 0               | 1                | 0            | 1                                        |
| [endrep-vs](endrep---vs.md)           | 0              | 0               | -1               | 0            | 0                                        |
| [loop-vs](loop---vs.md)               | 0              | 0               | 1                | 0            | 1                                        |
| [ENDLOOP-vs](endloop---vs.md)         | 0              | 0               | -1               | 0            | 0                                        |
| [interrupção vs](break---vs.md)             | N/D            | N/D             | N/D              | N/D          | N/D                                      |
| [interromper \_ comp-vs](break-comp---vs.md)  | N/D            | N/D             | N/D              | N/D          | N/D                                      |
| [breakp-vs](breakp---vs.md)           | N/D            | N/D             | N/D              | N/D          | N/D                                      |
| [Call-vs](call---vs.md)               | 0              | 0               | 0                | 1            | 1                                        |
| [callnz bool-vs](callnz-bool---vs.md) | 0              | 0               | 0                | 1            | 1                                        |
| [callnz Pred – vs](callnz-pred---vs.md) | N/D            | N/D             | N/D              | N/D          | N/D                                      |
| [RET-vs](ret---vs.md)                 | 0              | 0               | 0                | -1           | 0                                        |
| [setp \_ comp-vs](setp-comp---vs.md)    | N/D            | N/D             | N/D              | N/D          | N/D                                      |



 

### <a name="nesting-depth"></a>Profundidade de aninhamento

A profundidade do aninhamento define quantas instruções podem ser chamadas dentro umas das outras. Cada tipo de instrução tem um ou mais limites de aninhamento:



| Tipo de instrução  | Máximo                               |
|-------------------|---------------------------------------|
| Aninhamento estático    | Somente limitado pela contagem de fluxos estáticos |
| Aninhamento dinâmico   | N/D                                   |
| aninhamento de loop/representante  | 1                                     |
| aninhamento de chamadas      | 1                                     |
| Contagem de fluxos estáticos | 16                                    |



 

## <a name="depth-count-per-instruction-for-vs_2_x"></a>Contagem de profundidade por instrução para vs \_ 2 \_ x

Cada instrução conta com base em um ou mais limites de profundidade de aninhamento. Esta tabela mostra a contagem de profundidade que cada instrução adiciona ou subtrai da profundidade existente:



| Instrução                              | Aninhamento estático                       | Aninhamento dinâmico                                                           | aninhamento de loop/representante | aninhamento de chamadas | Contagem de fluxos estáticos                        |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|------------------------------------------|
| [se bool-vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | 1                                        |
| [Se \_ comp-vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | 0                                        |
| [se Pred-vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | 0                                        |
| [else-vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | 1 ([se bool-vs](if-bool---vs.md) apenas) |
| [endif-vs](endif---vs.md)             | -1 ([se bool-vs](if-bool---vs.md)) | -1 ([se Pred-vs](if-pred---vs.md) ou [se \_ comp-vs](if-comp---vs.md)) | 0                | 0            | 0                                        |
| [Rep-vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | 1                                        |
| [endrep-vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | 0                                        |
| [loop-vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | 1                                        |
| [ENDLOOP-vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | 0                                        |
| [interrupção vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | 0                                        |
| [interromper \_ comp-vs](break-comp---vs.md)  | 0                                    | 1,-1                                                                     | 0                | 0            | 0                                        |
| [breakp-vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | 0                                        |
| [Call-vs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | 1                                        |
| [callnz bool-vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | 1                                        |
| [callnz Pred – vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | 0                                        |
| [RET-vs](ret---vs.md)                 | 0                                    | -1 ([callnz Pred-vs](callnz-pred---vs.md))                             | 0                | -1           | 0                                        |
| [setp \_ comp-vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | 0                                        |



 

### <a name="nesting-depth"></a>Profundidade de aninhamento

A profundidade do aninhamento define quantas instruções podem ser chamadas dentro umas das outras. Cada tipo de instrução tem um ou mais limites de aninhamento:



| Tipo de instrução  | Máximo                                                                              |
|-------------------|--------------------------------------------------------------------------------------|
| Aninhamento estático    | Somente limitado pela contagem de fluxos estáticos                                                |
| Aninhamento dinâmico   | 0 ou 24, consulte D3DCAPS9. VS20Caps.DynamicFlowControlDepth                               |
| aninhamento de loop/representante  | 1 a 4, consulte D3DCAPS9. VS20Caps.StaticFlowControlDepth                                 |
| aninhamento de chamadas      | 1 a 4, consulte D3DCAPS9. VS20Caps. StaticFlowControlDepth (independente do limite de loop/representante) |
| Contagem de fluxos estáticos | 16                                                                                   |



 

## <a name="depth-count-per-instruction-for-vs_2_sw"></a>Contagem de profundidade por instrução para vs \_ 2 \_ SW

Cada instrução conta com base em um ou mais limites de profundidade de aninhamento. Esta tabela mostra a contagem de profundidade que cada instrução adiciona ou subtrai da profundidade existente:



| Instrução                              | Aninhamento estático                       | Aninhamento dinâmico                                                           | aninhamento de loop/representante | aninhamento de chamadas | Contagem de fluxos estáticos |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|-------------------|
| [se bool-vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | N/D               |
| [Se \_ comp-vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | N/D               |
| [se Pred-vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | N/D               |
| [else-vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [endif-vs](endif---vs.md)             | -1 ([se bool-vs](if-bool---vs.md)) | -1 ([se Pred-vs](if-pred---vs.md) ou [se \_ comp-vs](if-comp---vs.md)) | 0                | 0            | N/D               |
| [Rep-vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | N/D               |
| [endrep-vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | N/D               |
| [loop-vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | N/D               |
| [ENDLOOP-vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | N/D               |
| [interrupção vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [interromper \_ comp-vs](break-comp---vs.md)  | 0                                    | 1,-1                                                                     | 0                | 0            | N/D               |
| [breakp-vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [Call-vs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | n/d               |
| [callnz bool-vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | n/d               |
| [callnz Pred – vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | n/d               |
| [RET-vs](ret---vs.md)                 | 0                                    | -1 ([callnz Pred-vs](callnz-pred---vs.md))                             | 0                | -1           | N/D               |
| [setp \_ comp-vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | N/D               |



 

### <a name="nesting-depth"></a>Profundidade de aninhamento

A profundidade do aninhamento define quantas instruções podem ser chamadas dentro umas das outras. Cada tipo de instrução tem um ou mais limites de aninhamento:



| Tipo de instrução  | Máximo  |
|-------------------|----------|
| Aninhamento estático    | 24       |
| Aninhamento dinâmico   | 24       |
| aninhamento de loop/representante  | 4        |
| aninhamento de chamadas      | 4        |
| Contagem de fluxos estáticos | Sem limite |



 

## <a name="depth-count-per-instruction-for-vs_3_0"></a>Contagem de profundidade por instrução para vs \_ 3 \_ 0

Cada instrução conta com base em um ou mais limites de profundidade de aninhamento. Esta tabela mostra a contagem de profundidade que cada instrução adiciona ou subtrai da profundidade existente:



| Instrução                              | Aninhamento estático                       | Aninhamento dinâmico                                                           | aninhamento de loop/representante | aninhamento de chamadas | Contagem de fluxos estáticos |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|-------------------|
| [se bool-vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | N/D               |
| [Se \_ comp-vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | N/D               |
| [se Pred-vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | N/D               |
| [else-vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [endif-vs](endif---vs.md)             | -1 ([se bool-vs](if-bool---vs.md)) | -1 ([se Pred-vs](if-pred---vs.md) ou [se \_ comp-vs](if-comp---vs.md)) | 0                | 0            | N/D               |
| [Rep-vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | N/D               |
| [endrep-vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | N/D               |
| [loop-vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | N/D               |
| [ENDLOOP-vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | N/D               |
| [interrupção vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [interromper \_ comp-vs](break-comp---vs.md)  | 0                                    | 1,-1                                                                     | 0                | 0            | N/D               |
| [breakp-vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [Call-vs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | n/d               |
| [callnz bool-vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | n/d               |
| [callnz Pred – vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | n/d               |
| [RET-vs](ret---vs.md)                 | 0                                    | -1 ([callnz Pred-vs](callnz-pred---vs.md))                             | 0                | -1           | N/D               |
| [setp \_ comp-vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | N/D               |



 

### <a name="nesting-depth"></a>Profundidade de aninhamento

A profundidade do aninhamento define quantas instruções podem ser chamadas dentro umas das outras. Cada tipo de instrução tem um ou mais limites de aninhamento:



| Tipo de instrução  | Máximo  |
|-------------------|----------|
| Aninhamento estático    | 24       |
| Aninhamento dinâmico   | 24       |
| aninhamento de loop/representante  | 4        |
| aninhamento de chamadas      | 4        |
| Contagem de fluxos estáticos | Sem limite |



 

## <a name="depth-count-per-instruction-for-vs_3_sw"></a>Contagem de profundidade por instrução para vs \_ 3 \_ SW

Cada instrução conta com base em um ou mais limites de profundidade de aninhamento. Esta tabela mostra a contagem de profundidade que cada instrução adiciona ou subtrai da profundidade existente:



| Instrução                              | Aninhamento estático                       | Aninhamento dinâmico                                                           | aninhamento de loop/representante | aninhamento de chamadas | Contagem de fluxos estáticos |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|-------------------|
| [se bool-vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | N/D               |
| [Se \_ comp-vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | N/D               |
| [se Pred-vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | N/D               |
| [else-vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [endif-vs](endif---vs.md)             | -1 ([se bool-vs](if-bool---vs.md)) | -1 ([se Pred-vs](if-pred---vs.md) ou [se \_ comp-vs](if-comp---vs.md)) | 0                | 0            | N/D               |
| [Rep-vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | N/D               |
| [endrep-vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | N/D               |
| [loop-vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | N/D               |
| [ENDLOOP-vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | N/D               |
| [interrupção vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [interromper \_ comp-vs](break-comp---vs.md)  | 0                                    | 1,-1                                                                     | 0                | 0            | N/D               |
| [breakp-vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [Call-vs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | n/d               |
| [callnz bool-vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | n/d               |
| [callnz Pred – vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | n/d               |
| [RET-vs](ret---vs.md)                 | 0                                    | -1 ([callnz Pred-vs](callnz-pred---vs.md))                             | 0                | -1           | N/D               |
| [setp \_ comp-vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | N/D               |



 

### <a name="nesting-depth"></a>Profundidade de aninhamento

A profundidade do aninhamento define quantas instruções podem ser chamadas dentro umas das outras. Cada tipo de instrução tem um ou mais limites de aninhamento:



| Tipo de instrução  | Máximo  |
|-------------------|----------|
| Aninhamento estático    | 24       |
| Aninhamento dinâmico   | 24       |
| aninhamento de loop/representante  | 4        |
| aninhamento de chamadas      | 4        |
| Contagem de fluxos estáticos | Sem limite |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




