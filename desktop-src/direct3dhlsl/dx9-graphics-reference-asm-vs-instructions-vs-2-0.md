---
title: Instruções – vs_2_0
description: Esta seção contém informações de referência para as instruções do sombreador de vértice versão \_ 2 0.
ms.assetid: f5ca3e44-3c71-4221-9381-cea521d984e0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0baaa0fb9523e59e3dafdb0a7dd1dd7856325c518f06995da4d768929982b6f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744466"
---
# <a name="instructions---vs_2_0"></a>Instruções – \_ versus 2 \_ 0

Esta seção contém informações de referência para as instruções do sombreador de vértice versão \_ 2 0.

Há vários tipos de instruções de sombreador de vértice, conforme mostrado na tabela. As colunas à direita significam o seguinte:

-   Slots de instrução – número de slots de instrução usados por cada instrução.
-   Instalação – instruções não aritméticas. Cada sombreador deve ter uma instrução de versão e deve ser a primeira instrução.
-   Aritmética – essas instruções fornecem as operações matemáticas em um sombreador.
-   Flow controle – estas instruções adicionam recursos de controle de fluxo, como [loop](loop---vs.md)... [endloop](endloop---vs.md), [se](if-bool---vs.md)... [else](else---vs.md)... [endif - vs](endif---vs.md). e chamadas de sub-rotina.
-   Novo – essas instruções são novas para esta versão.

## <a name="instruction-set"></a>Conjunto de instruções



| Nome                                                                           | Descrição                                                                                                     | Slots de instrução | Instalação | Aritmético | Controle de fluxo | Novo |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-------------------|-------|------------|--------------|-----|
| [abs – vs](abs---vs.md)                                                       | Valor absoluto                                                                                                  | 1                 |       | x          |              | x   |
| [add - vs](add---vs.md)                                                       | Adicionar dois vetores                                                                                                 | 1                 |       | x          |              |     |
| [call - vs](call---vs.md)                                                     | Chamar uma sub-rotina                                                                                               | 2                 |       |            | x            | x   |
| [callnz bool – vs](callnz-bool---vs.md)                                       | Chamar uma sub-rotina se um registro booliana não for zero                                                             | 3                 |       |            | x            | x   |
| [crs – vs](crs---vs.md)                                                       | Produto cruzado                                                                                                   | 2                 |       | x          |              | x   |
| [entrada de \_ uso dcl (sm1, sm2, sm3 – vs asm)](dcl-usage-input-register---vs.md) | Declarar registros de vértice de entrada (consulte [Registros – vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md)) | 0                 | x     |            |              |     |
| [def – vs](def---vs.md)                                                       | Definir constantes                                                                                                | 0                 | x     |            |              |     |
| [defb – vs](defb---vs.md)                                                     | Definir uma constante booliana                                                                                       | 0                 | x     |            |              | x   |
| [defi – vs](defi---vs.md)                                                     | Definir uma constante de inteiro                                                                                      | 0                 | x     |            |              | x   |
| [dp3 – vs](dp3---vs.md)                                                       | Produto de ponto de três componentes                                                                                     | 1                 |       | x          |              |     |
| [dp4 – vs](dp4---vs.md)                                                       | Produto de ponto de quatro componentes                                                                                      | 1                 |       | x          |              |     |
| [dst - vs](dst---vs.md)                                                       | Calcular o vetor de distância                                                                                   | 1                 |       | x          |              |     |
| [else - vs](else---vs.md)                                                     | Iniciar um [outro – vs](else---vs.md) bloco                                                                       | 1                 |       |            | x            | x   |
| [endif - vs](endif---vs.md)                                                   | Encerrar um [se bool - vs](if-bool---vs.md)... [else - vs](else---vs.md) block                                      | 1                 |       |            | x            | x   |
| [endloop – vs](endloop---vs.md)                                               | Fim de um [loop – vs](loop---vs.md) bloco                                                                       | 2                 |       |            | x            | x   |
| [endrep – vs](endrep---vs.md)                                                 | Fim de um bloco de repetição                                                                                           | 2                 |       |            | x            | x   |
| [exp - vs](exp---vs.md)                                                       | Precisão completa 2<sup>x</sup>                                                                                    | 1                 |       | x          |              |     |
| [exp - vs](exp---vs.md)                                                       | Precisão parcial 2<sup>x</sup>                                                                                 | 1                 |       | x          |              |     |
| [frc – vs](frc---vs.md)                                                       | Componente fracionado                                                                                            | 1                 |       | x          |              |     |
| [se bool - vs](if-bool---vs.md)                                               | Iniciar um [se bool - vs](if-bool---vs.md) bloco (usando uma condição booliana)                                     | 3                 |       |            | x            | x   |
| [label – vs](label---vs.md)                                                   | Rótulo                                                                                                           | 0                 |       |            | x            | x   |
| [lit – vs](lit---vs.md)                                                       | Cálculo de iluminação parcial                                                                                    | 3                 |       | x          |              |     |
| [log – vs](log---vs.md)                                                       | Log de precisão completa(x)                                                                                          | 1                 |       | x          |              |     |
| [logp – vs](logp---vs.md)                                                     | Log de precisão parcial(x)                                                                                       | 1                 |       | x          |              |     |
| [loop – vs](loop---vs.md)                                                     | Loop                                                                                                            | 3                 |       |            | x            | x   |
| [lrp – vs](lrp---vs.md)                                                       | Interpolação linear                                                                                            | 2                 |       | x          |              | x   |
| [m3x2 – vs](m3x2---vs.md)                                                     | Multiplicação de 3x2                                                                                                    | 2                 |       | x          |              |     |
| [m3x3 – vs](m3x3---vs.md)                                                     | Multiplicação de 3x3                                                                                                    | 3                 |       | x          |              |     |
| [m3x4 – vs](m3x4---vs.md)                                                     | Multiplicação de 3x4                                                                                                    | 4                 |       | x          |              |     |
| [m4x3 – vs](m4x3---vs.md)                                                     | Multiplicação de 4x3                                                                                                    | 3                 |       | x          |              |     |
| [m4x4 – vs](m4x4---vs.md)                                                     | Multiplicação de 4x4                                                                                                    | 4                 |       | x          |              |     |
| [mad - vs](mad---vs.md)                                                       | Multiplicar e adicionar                                                                                                | 1                 |       | x          |              |     |
| [max - vs](max---vs.md)                                                       | Máximo                                                                                                         | 1                 |       | x          |              |     |
| [min - vs](min---vs.md)                                                       | Mínimo                                                                                                         | 1                 |       | x          |              |     |
| [mov - vs](mov---vs.md)                                                       | Mover                                                                                                            | 1                 |       | x          |              |     |
| [mova - vs](mova---vs.md)                                                     | Mover dados de um registro de ponto flutuante para o registro de endereço (a0)                                           | 1                 |       | x          |              | x   |
| [mul - vs](mul---vs.md)                                                       | Multiplicar                                                                                                        | 1                 |       | x          |              |     |
| [nop – vs](nop---vs.md)                                                       | Nenhuma operação                                                                                                    | 1                 |       | x          |              |     |
| [nrm - vs](nrm---vs.md)                                                       | Normalizar um vetor 4D                                                                                           | 3                 |       | x          |              | x   |
| [pow - vs](pow---vs.md)                                                       | x<sup>y</sup>                                                                                                   | 3                 |       | x          |              | x   |
| [rcp - vs](rcp---vs.md)                                                       | Recíproca                                                                                                      | 1                 |       | x          |              |     |
| [Rep-vs](rep---vs.md)                                                       | Repetir                                                                                                          | 3                 |       |            | x            | x   |
| [RET-vs](ret---vs.md)                                                       | Fim de uma sub-rotina ou principal                                                                              | 1                 |       |            | x            | x   |
| [RSQ-vs](rsq---vs.md)                                                       | Raiz quadrada recíproca                                                                                          | 1                 |       | x          |              |     |
| [SGE-vs](sge---vs.md)                                                       | Comparação maior ou igual a                                                                                   | 1                 |       | x          |              |     |
| [sgn-vs](sgn---vs.md)                                                       | Assinar                                                                                                            | 3                 |       | x          |              | x   |
| [Sincos-vs](sincos---vs.md)                                                 | Seno e cosseno                                                                                                 | 8                 |       | x          |              | x   |
| [SLT-vs](slt---vs.md)                                                       | Menor que comparação                                                                                               | 1                 |       | x          |              |     |
| [sub-vs](sub---vs.md)                                                       | Subtrair                                                                                                        | 1                 |       | x          |              |     |
| [vs](vs---vs.md)                                                              | Versão                                                                                                         | 0                 | x     |            |              |     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




