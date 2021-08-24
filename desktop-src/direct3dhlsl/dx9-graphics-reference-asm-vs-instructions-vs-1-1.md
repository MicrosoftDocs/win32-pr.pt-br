---
title: Instruções – vs_1_1
description: Esta seção contém informações de referência para as instruções do sombreador de vértice versão \_ 1 1.
ms.assetid: db3c14ce-6e50-4931-b07f-966acc7ffb0a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f980640009158c6c4dc684158836d1514ca47755fea700ac7cc619f6e7574409
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789086"
---
# <a name="instructions---vs_1_1"></a>Instruções – vs \_ 1 \_ 1

Esta seção contém informações de referência para as instruções do sombreador de vértice versão \_ 1 1.

Há vários tipos de instruções de sombreador de vértice, conforme mostrado na tabela. As colunas à direita significam o seguinte:

-   Slots de instrução – número de slots de instrução usados por cada instrução.
-   Instalação – instruções não aritméticas. Cada sombreador deve ter uma instrução de versão e deve ser a primeira instrução.
-   Aritmética – essas instruções fornecem as operações matemáticas em um sombreador.
-   Novo – essas instruções são novas para esta versão.

## <a name="instruction-set"></a>Conjunto de instruções



| Nome                                                                           | Descrição                                                                                                     | Slots de instrução | Instalação | Aritmético | Novo |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-------------------|-------|------------|-----|
| [add - vs](add---vs.md)                                                       | Adicionar dois vetores                                                                                                 | 1                 |       | x          | x   |
| [entrada de \_ uso dcl (sm1, sm2, sm3 – vs asm)](dcl-usage-input-register---vs.md) | Declarar registros de vértice de entrada [(consulte Registros – vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)) | 0                 | x     |            | x   |
| [def – vs](def---vs.md)                                                       | Definir constantes                                                                                                | 0                 | x     |            | x   |
| [dp3 – vs](dp3---vs.md)                                                       | Produto de ponto de três componentes                                                                                     | 1                 |       | x          | x   |
| [dp4 – vs](dp4---vs.md)                                                       | Produto de ponto de quatro componentes                                                                                      | 1                 |       | x          | x   |
| [dst - vs](dst---vs.md)                                                       | Calcular o vetor de distância                                                                                   | 1                 |       | x          | x   |
| [exp - vs](exp---vs.md)                                                       | Precisão completa 2<sup>x</sup>                                                                                    | 10                |       | x          | x   |
| [exp - vs](exp---vs.md)                                                       | Precisão parcial 2<sup>x</sup>                                                                                 | 1                 |       | x          | x   |
| [frc – vs](frc---vs.md)                                                       | Componente fracionado                                                                                            | 3                 |       | x          | x   |
| [lit – vs](lit---vs.md)                                                       | Cálculo de iluminação parcial                                                                                    | 1                 |       | x          | x   |
| [log – vs](log---vs.md)                                                       | Log de precisão completa(x)                                                                                          | 10                |       | x          | x   |
| [logp – vs](logp---vs.md)                                                     | Log de precisão parcial(x)                                                                                       | 1                 |       | x          | x   |
| [m3x2 – vs](m3x2---vs.md)                                                     | Multiplicação de 3x2                                                                                                    | 2                 |       | x          | x   |
| [m3x3 – vs](m3x3---vs.md)                                                     | Multiplicação de 3x3                                                                                                    | 3                 |       | x          | x   |
| [m3x4 – vs](m3x4---vs.md)                                                     | Multiplicação de 3x4                                                                                                    | 4                 |       | x          | x   |
| [m4x3 – vs](m4x3---vs.md)                                                     | Multiplicação de 4x3                                                                                                    | 3                 |       | x          | x   |
| [m4x4 – vs](m4x4---vs.md)                                                     | Multiplicação de 4x4                                                                                                    | 4                 |       | x          | x   |
| [mad - vs](mad---vs.md)                                                       | Multiplicar e adicionar                                                                                                | 1                 |       | x          | x   |
| [max - vs](max---vs.md)                                                       | Máximo                                                                                                         | 1                 |       | x          | x   |
| [min - vs](min---vs.md)                                                       | Mínimo                                                                                                         | 1                 |       | x          | x   |
| [mov - vs](mov---vs.md)                                                       | Mover                                                                                                            | 1                 |       | x          | x   |
| [mul - vs](mul---vs.md)                                                       | Multiplicar                                                                                                        | 1                 |       | x          | x   |
| [nop – vs](nop---vs.md)                                                       | Nenhuma operação                                                                                                    | 1                 |       | x          | x   |
| [rcp - vs](rcp---vs.md)                                                       | Recíproca                                                                                                      | 1                 |       | x          | x   |
| [rsq - vs](rsq---vs.md)                                                       | Raiz quadrada recíproca                                                                                          | 1                 |       | x          | x   |
| [sge - vs](sge---vs.md)                                                       | Comparação maior ou igual                                                                                   | 1                 |       | x          | x   |
| [slt – vs](slt---vs.md)                                                       | Menor que comparação                                                                                               | 1                 |       | x          | x   |
| [sub - vs](sub---vs.md)                                                       | Subtrair                                                                                                        | 1                 |       | x          | x   |
| [Vs](vs---vs.md)                                                              | Versão                                                                                                         | 0                 | x     |            | x   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




