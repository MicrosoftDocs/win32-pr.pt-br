---
title: Instruções-vs_1_1
description: Esta seção contém informações de referência para as instruções da versão 1 1 do sombreador de vértice \_ .
ms.assetid: db3c14ce-6e50-4931-b07f-966acc7ffb0a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1b4def55dfaca19608599d9c79e20d3e0690832c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104966995"
---
# <a name="instructions---vs_1_1"></a>Instruções-vs \_ 1 \_ 1

Esta seção contém informações de referência para as instruções da versão 1 1 do sombreador de vértice \_ .

Há vários tipos de instruções de sombreador de vértice, conforme mostrado na tabela. As colunas à direita significam o seguinte:

-   Slots de instrução-número de Slots de instrução usados por cada instrução.
-   Instalação-instruções não aritméticas. Cada sombreador deve ter uma instrução de versão e deve ser a primeira instrução.
-   Aritmética – essas instruções fornecem as operações matemáticas em um sombreador.
-   Novas-essas instruções são novas nesta versão.

## <a name="instruction-set"></a>Conjunto de instruções



| Name                                                                           | Descrição                                                                                                     | Slots de instrução | Instalação | Aritmético | Novo |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-------------------|-------|------------|-----|
| [Adicionar-vs](add---vs.md)                                                       | Adicionar dois vetores                                                                                                 | 1                 |       | x          | x   |
| [\_entrada de uso de DCL (SM1, SM2, SM3-vs ASM)](dcl-usage-input-register---vs.md) | Declarar registros de vértice de entrada (consulte [registros-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)) | 0                 | x     |            | x   |
| [def-vs](def---vs.md)                                                       | Definir constantes                                                                                                | 0                 | x     |            | x   |
| [DP3-vs](dp3---vs.md)                                                       | Produto de três componentes do ponto                                                                                     | 1                 |       | x          | x   |
| [DP4-vs](dp4---vs.md)                                                       | Produto de quatro componentes do ponto                                                                                      | 1                 |       | x          | x   |
| [DST-vs](dst---vs.md)                                                       | Calcular o vetor de distância                                                                                   | 1                 |       | x          | x   |
| [exp-vs](exp---vs.md)                                                       | Precisão total 2<sup>x</sup>                                                                                    | 10                |       | x          | x   |
| [exp-vs](exp---vs.md)                                                       | Precisão parcial 2<sup>x</sup>                                                                                 | 1                 |       | x          | x   |
| [FRC-vs](frc---vs.md)                                                       | Componente fracionário                                                                                            | 3                 |       | x          | x   |
| [aceso-vs](lit---vs.md)                                                       | Cálculo de iluminação parcial                                                                                    | 1                 |       | x          | x   |
| [log-vs](log---vs.md)                                                       | ₂ de log de precisão total (x)                                                                                          | 10                |       | x          | x   |
| [LogP-vs](logp---vs.md)                                                     | ₂ de log de precisão parcial (x)                                                                                       | 1                 |       | x          | x   |
| [M3X2-vs](m3x2---vs.md)                                                     | 3x2 multiplicar                                                                                                    | 2                 |       | x          | x   |
| [m3x3-vs](m3x3---vs.md)                                                     | multiplicar a 3x3                                                                                                    | 3                 |       | x          | x   |
| [M3x4-vs](m3x4---vs.md)                                                     | 3x4 multiplicar                                                                                                    | 4                 |       | x          | x   |
| [m4x3-vs](m4x3---vs.md)                                                     | 4x3 multiplicar                                                                                                    | 3                 |       | x          | x   |
| [m4x4-vs](m4x4---vs.md)                                                     | 4x4 multiplicar                                                                                                    | 4                 |       | x          | x   |
| [Mad-vs](mad---vs.md)                                                       | Multiplicar e adicionar                                                                                                | 1                 |       | x          | x   |
| [máx.-vs](max---vs.md)                                                       | Máximo                                                                                                         | 1                 |       | x          | x   |
| [min-vs](min---vs.md)                                                       | Mínimo                                                                                                         | 1                 |       | x          | x   |
| [MOV-vs](mov---vs.md)                                                       | Mover                                                                                                            | 1                 |       | x          | x   |
| [Mul-vs](mul---vs.md)                                                       | Multiplicar                                                                                                        | 1                 |       | x          | x   |
| [Nop-vs](nop---vs.md)                                                       | Nenhuma operação                                                                                                    | 1                 |       | x          | x   |
| [RCP-vs](rcp---vs.md)                                                       | Recíproco                                                                                                      | 1                 |       | x          | x   |
| [RSQ-vs](rsq---vs.md)                                                       | Raiz quadrada recíproca                                                                                          | 1                 |       | x          | x   |
| [SGE-vs](sge---vs.md)                                                       | Comparação maior ou igual a                                                                                   | 1                 |       | x          | x   |
| [SLT-vs](slt---vs.md)                                                       | Menor que comparação                                                                                               | 1                 |       | x          | x   |
| [sub-vs](sub---vs.md)                                                       | Subtrair                                                                                                        | 1                 |       | x          | x   |
| [vs](vs---vs.md)                                                              | Versão                                                                                                         | 0                 | x     |            | x   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




