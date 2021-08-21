---
title: Instruções-vs_2_x
description: Esta seção contém informações de referência para as instruções da versão 2 x do sombreador de vértice \_ .
ms.assetid: fac85f96-0f4b-49a8-9c00-9e68000d1c76
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 579e52349031545fd540a98c7ea12876ae0700f725ea81ee05ac0fed65b09a1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512272"
---
# <a name="instructions---vs_2_x"></a>Instruções – vs \_ 2 \_ x

Esta seção contém informações de referência para as instruções da versão 2 x do sombreador de vértice \_ .

Há vários tipos de instruções de sombreador de vértice, conforme mostrado na tabela. As colunas à direita significam o seguinte:

-   Slots de instrução-número de Slots de instrução usados por cada instrução.
-   Instalação-instruções não aritméticas. Cada sombreador deve ter uma instrução de versão e deve ser a primeira instrução.
-   Aritmética – essas instruções fornecem as operações matemáticas em um sombreador.
-   controle de Flow-essas instruções adicionam recursos de controle de fluxo, como [loop-vs](loop---vs.md)... [ENDLOOP – vs](endloop---vs.md), [If bool-vs](if-bool---vs.md)... [senão](else---vs.md)... [endif](endif---vs.md)e chamadas de sub-rotina.
-   Novas-essas instruções são novas nesta versão.

## <a name="instruction-set"></a>Conjunto de instruções



| Name                                                                           | Descrição                                                                                                                                                            | Slots de instrução | Instalação | Aritmético | Controle de fluxo | Novo |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|-------|------------|--------------|-----|
| [ABS-vs](abs---vs.md)                                                       | Valor absoluto                                                                                                                                                         | 1                 |       | x          |              |     |
| [Adicionar-vs](add---vs.md)                                                       | Adicionar dois vetores                                                                                                                                                        | 1                 |       | x          |              |     |
| [interrupção vs](break---vs.md)                                                   | Sair de um [loop-vs](loop---vs.md)... [ENDLOOP-vs](endloop---vs.md) ou [Rep](rep---vs.md)... bloco [endrep](endrep---vs.md)                                  | 1                 |       |            | x            | x   |
| [interromper \_ comp-vs](break-comp---vs.md)                                        | Interromper condicionalmente de um [loop-vs](loop---vs.md)... [ENDLOOP-vs](endloop---vs.md) ou [Rep](rep---vs.md)... bloco [endrep](endrep---vs.md) , com uma comparação | 3                 |       |            | x            | x   |
| [breakp-vs](breakp---vs.md)                                                 | Sair de um [loop-vs](loop---vs.md)... [ENDLOOP-vs](endloop---vs.md) ou [Rep](rep---vs.md)... bloco [endrep](endrep---vs.md) , com base em um predicado            | 3                 |       |            | x            | x   |
| [Call-vs](call---vs.md)                                                     | Chamar uma sub-rotina                                                                                                                                                      | 2                 |       |            | x            |     |
| [callnz bool-vs](callnz-bool---vs.md)                                       | Chamar uma sub-rotina se um registro booliano não for zero                                                                                                                    | 3                 |       |            | x            |     |
| [callnz Pred – vs](callnz-pred---vs.md)                                       | Chamar uma sub-rotina se um registro de predicado não for zero                                                                                                                  | 3                 |       |            | x            | x   |
| [CRS-vs](crs---vs.md)                                                       | Produto cruzado                                                                                                                                                          | 2                 |       | x          |              |     |
| [\_entrada de uso de DCL (SM1, SM2, SM3-vs ASM)](dcl-usage-input-register---vs.md) | Declarar registros de vértice de entrada (consulte [registros-vs. \_ 2 \_ x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md))                                                        | 0                 | x     |            |              |     |
| [def-vs](def---vs.md)                                                       | Definir constantes                                                                                                                                                       | 0                 | x     |            |              |     |
| [DEFB-vs](defb---vs.md)                                                     | Definir uma constante booliana                                                                                                                                              | 0                 | x     |            |              |     |
| [defi-vs](defi---vs.md)                                                     | Definir uma constante de inteiro                                                                                                                                             | 0                 | x     |            |              |     |
| [DP3-vs](dp3---vs.md)                                                       | Produto de três componentes do ponto                                                                                                                                            | 1                 |       | x          |              |     |
| [DP4-vs](dp4---vs.md)                                                       | Produto de quatro componentes do ponto                                                                                                                                             | 1                 |       | x          |              |     |
| [DST-vs](dst---vs.md)                                                       | Calcular o vetor de distância                                                                                                                                          | 1                 |       | x          |              |     |
| [else-vs](else---vs.md)                                                     | Iniciar um bloco [else-vs](else---vs.md)                                                                                                                              | 1                 |       |            | x            |     |
| [endif-vs](endif---vs.md)                                                   | Encerrar um [If bool-vs](if-bool---vs.md)... bloco [else-vs](else---vs.md)                                                                                             | 1                 |       |            | x            |     |
| [ENDLOOP-vs](endloop---vs.md)                                               | Fim de um bloco de [loop vs](loop---vs.md)                                                                                                                              | 2                 |       |            | x            |     |
| [endrep-vs](endrep---vs.md)                                                 | Fim de um bloco de repetição                                                                                                                                                  | 2                 |       |            | x            |     |
| [exp-vs](exp---vs.md)                                                       | Precisão total 2<sup>x</sup>                                                                                                                                           | 1                 |       | x          |              |     |
| [exp-vs](exp---vs.md)                                                       | Precisão parcial 2<sup>x</sup>                                                                                                                                        | 1                 |       | x          |              |     |
| [FRC-vs](frc---vs.md)                                                       | Componente fracionário                                                                                                                                                   | 1                 |       | x          |              |     |
| [se bool-vs](if-bool---vs.md)                                               | Iniciar um bloco [bool-vs](if-bool---vs.md) (usando uma condição booliana)                                                                                            | 3                 |       |            | x            |     |
| [Se \_ comp-vs](if-comp---vs.md)                                              | Iniciar um bloco [bool-vs](if-bool---vs.md) , com uma comparação                                                                                                     | 3                 |       |            | x            | x   |
| [se Pred-vs](if-pred---vs.md)                                               | Iniciar um bloco [bool-vs](if-bool---vs.md) com uma condição de predicado                                                                                             | 3                 |       |            | x            | x   |
| [rótulo – vs](label---vs.md)                                                   | Rótulo                                                                                                                                                                  | 0                 |       |            | x            |     |
| [aceso-vs](lit---vs.md)                                                       | Cálculo de iluminação parcial                                                                                                                                           | 3                 |       | x          |              |     |
| [log-vs](log---vs.md)                                                       | ₂ de log de precisão total (x)                                                                                                                                                 | 1                 |       | x          |              |     |
| [LogP-vs](logp---vs.md)                                                     | ₂ de log de precisão parcial (x)                                                                                                                                              | 1                 |       | x          |              |     |
| [loop-vs](loop---vs.md)                                                     | Loop                                                                                                                                                                   | 3                 |       |            | x            |     |
| [LRP-vs](lrp---vs.md)                                                       | Interpolação linear                                                                                                                                                   | 2                 |       | x          |              |     |
| [M3X2-vs](m3x2---vs.md)                                                     | 3x2 multiplicar                                                                                                                                                           | 2                 |       | x          |              |     |
| [m3x3-vs](m3x3---vs.md)                                                     | multiplicar a 3x3                                                                                                                                                           | 3                 |       | x          |              |     |
| [M3x4-vs](m3x4---vs.md)                                                     | 3x4 multiplicar                                                                                                                                                           | 4                 |       | x          |              |     |
| [m4x3-vs](m4x3---vs.md)                                                     | 4x3 multiplicar                                                                                                                                                           | 3                 |       | x          |              |     |
| [m4x4-vs](m4x4---vs.md)                                                     | 4x4 multiplicar                                                                                                                                                           | 4                 |       | x          |              |     |
| [Mad-vs](mad---vs.md)                                                       | Multiplicar e adicionar                                                                                                                                                       | 1                 |       | x          |              |     |
| [máx.-vs](max---vs.md)                                                       | Máximo                                                                                                                                                                | 1                 |       | x          |              |     |
| [min-vs](min---vs.md)                                                       | Mínimo                                                                                                                                                                | 1                 |       | x          |              |     |
| [MOV-vs](mov---vs.md)                                                       | Mover                                                                                                                                                                   | 1                 |       | x          |              |     |
| [Mova-vs](mova---vs.md)                                                     | Mover dados de um ponto flutuante registrar para o registro de endereço (a0)                                                                                                  | 1                 |       | x          |              |     |
| [Mul-vs](mul---vs.md)                                                       | Multiplicar                                                                                                                                                               | 1                 |       | x          |              |     |
| [Nop-vs](nop---vs.md)                                                       | Nenhuma operação                                                                                                                                                           | 1                 |       | x          |              |     |
| [NRM-vs](nrm---vs.md)                                                       | Normalizar um vetor 4D                                                                                                                                                  | 3                 |       | x          |              |     |
| [pow-vs](pow---vs.md)                                                       | x<sup>y</sup>                                                                                                                                                          | 3                 |       | x          |              |     |
| [RCP-vs](rcp---vs.md)                                                       | Recíproco                                                                                                                                                             | 1                 |       | x          |              |     |
| [Rep-vs](rep---vs.md)                                                       | Repetir                                                                                                                                                                 | 3                 |       |            | x            |     |
| [RET-vs](ret---vs.md)                                                       | Fim de uma sub-rotina ou principal                                                                                                                                     | 1                 |       |            | x            |     |
| [RSQ-vs](rsq---vs.md)                                                       | Raiz quadrada recíproca                                                                                                                                                 | 1                 |       | x          |              |     |
| [setp \_ comp-vs](setp-comp---vs.md)                                          | Definir o registro de predicado                                                                                                                                             | 1                 |       |            | x            | x   |
| [SGE-vs](sge---vs.md)                                                       | Comparação maior ou igual a                                                                                                                                          | 1                 |       | x          |              |     |
| [sgn-vs](sgn---vs.md)                                                       | Assinar                                                                                                                                                                   | 3                 |       | x          |              |     |
| [Sincos-vs](sincos---vs.md)                                                 | Seno e cosseno                                                                                                                                                        | 8                 |       | x          |              |     |
| [SLT-vs](slt---vs.md)                                                       | Menor que comparação                                                                                                                                                      | 1                 |       | x          |              |     |
| [sub-vs](sub---vs.md)                                                       | Subtrair                                                                                                                                                               | 1                 |       | x          |              |     |
| [vs](vs---vs.md)                                                              | Versão                                                                                                                                                                | 0                 | x     |            |              |     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




